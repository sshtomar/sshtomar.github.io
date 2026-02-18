---
layout: post
title: "RAG for Miners"
date: 2025-02-18
---

I recently worked on building and evaluating a RAG-based Q&A system for a heavy equipment manufacturer. The bot answers questions from technical documentation -- manuals, parts catalogs, specs, service bulletins -- for operators running underground drilling rigs.

The tooling is mature. We used Databricks and Azure. Technically it was a plumbing job.

The real work was understanding how miners actually use the thing, where it fails them, and whether it moves the needle for the business.

![Underground drilling rig](/assets/images/rag-mining/drilling-rig.png)

## Miners do not like to type

We built and tested the system with well-formed technical questions. Tested with internal technical stakeholders as well.

When we went for customer trials, the average query was 30 characters. Some were a single word.

"fuses"

"oil"

"brakes are not working"

These are people underground, wearing gloves, on a tablet bolted to a drilling rig. They type the minimum they think will get them an answer.

![Operator using tablet underground](/assets/images/rag-mining/operator-tablet.png)

Every LLM app has this gap. The team tests with careful prompts. Real users show up with fragments, typos, and single keywords. The golden dataset I ended up with -- built from actual thumbs-up production feedback -- had almost no overlap with test queries provided by internal technical stakeholders. Not just different questions. Different grammar, different length, different assumptions about what the system already knows.

## The failure modes

We manually reviewed hundreds of responses and categorized the failures. Hallucination and retrieval misses.

Credits to sensei [@sh_reya](https://x.com/sh_reya) and [@HamelHusain](https://x.com/HamelHusain).

We also categorized our queries using topic modelling -- something I picked from [@jxnlco](https://x.com/jxnlco).

This pattern is everywhere in production RAG systems and almost never measured. Standard evals ask: did it retrieve relevant documents? Is the answer grounded? Is it correct? Nobody asks: when the system couldn't answer, did it fail usefully or just shrug?

Measure the non-answer rate.

## Build evaluations from production feedback

I split evaluation into two tiers: quality metrics and exploration signals. More teams should do this.

Quality metrics drive pass/fail decisions. They need to be deterministic where possible and calibrated against real data. We started with simple rule-based checks: is the response non-empty? Reasonable length? Includes source citations? Completed without errors? Latency acceptable?

Then we added checks for the specific failure modes we found by reading thumbs-down feedback: the graceful non-answer pattern, formatting problems, filler responses that bury the actual answer.

These rule-based checks caught the majority of real issues without a single LLM call.

Exploration signals are LLM-as-judge scorers for finding interesting traces to review -- not for automated decisions. When we validated generic judges (relevance, correctness) against human-labeled data, agreement was near-perfect. But domain-specific judges -- "does the answer reference the right product?" or "are safety warnings included?" -- dropped below 90%. Useful for surfacing traces worth looking at. Not reliable enough for quality gates.

The practical takeaway: deterministic scorers first. They're boring and they work. LLM judges second, and only after you've validated them against human judgment.

## Would this thing actually make money?

Stakeholder asked this. It's the right question.

The end users are mining companies running million-dollar drilling rigs underground. When a rig breaks, the operator either fixes it or waits for a technician. Every hour of downtime is lost production.

The bot collapses the time between "something's wrong" and "I know what to do." Finding a part number, looking up a procedure, identifying a fault code. Even small time savings per incident compound across hundreds of machines.

But a bot that shrugs at 1 in 6 queries trains users to stop trusting it. Users would leave silently. Once they stop asking, ROI drops to zero regardless of how good the technology is.

This is what most teams get wrong about LLM ROI. They benchmark accuracy and project value from success cases. But adoption is driven by failure cases.

![Break room inside the Kittila mine, Finland, almost 1000 meters underground](/assets/images/rag-mining/break-room.png)
