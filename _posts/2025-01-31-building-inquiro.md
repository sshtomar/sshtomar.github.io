---
layout: post
title: "Building Inquiro: When Code Becomes Cheap"
date: 2025-01-31
---

Kailash Nadh recently wrote that LLMs have inverted the old adage: "Talk is cheap, show me the code" has become "Code is cheap, show me the talk."

He's right. And I have proof.

I built [Inquiro](https://inquiro.dev)—a statistical analysis platform for researchers—in weeks, not months. Not because I cut corners. Because code is cheap now, and what I had was the talk.

## The Inversion

For decades, typing was the bottleneck. You could imagine features faster than you could implement them. Ideas were cheap; execution was expensive.

That's over.

"Programming is 90% thinking and 10% typing" was always true in spirit. Now it's true literally. The thinking—what Nadh calls "the talk"—is the scarce resource. The ability to articulate what you want, to architect systems, to imagine solutions. The code follows.

Inquiro required design sensibility, statistical knowledge, and architectural judgment. It needed someone who understood what researchers actually need, why standard errors matter, how assumption checks should surface in a UI. The implementation? AI handled most of it.

## What I Actually Did

I didn't write Inquiro. I directed it.

I described what I wanted: a clean interface that signals rigor. A pipeline that generates reproducible Python code with proper diagnostics. Automatic checks for heteroskedasticity, influential observations, pre-trend validation. Results that researchers can trust and cite.

AI became a collaborator that never tired. For well-defined problems—parsing outputs, formatting tables, handling edge cases—it generated working code faster than I could type. For ambiguous problems—how should the UX respond when an assumption fails?—I still had to think. AI implemented my answers.

Marc Andreessen describes this as the superpowered individual: "The really great people are becoming spectacularly great. If you're very good at it and you can really harness AI, you can become not just great, but spectacularly productive."

I felt this. The multiplier was real—maybe 3-5x overall. But gains weren't uniform. Boilerplate: 10x faster. Complex statistical logic: 2x. Novel UX decisions: same speed, but with more options to consider.

## The Combination Effect

Andreessen also talks about what he calls the "Mexican standoff" between product managers, engineers, and designers. Everyone now believes they can do each other's jobs—and they're correct.

But the real insight is this: "The additive effect of being good at two things is more than double. The additive effect of being good at three things is more than triple. You become a super relevant specialist in the combination of the domains."

Building Inquiro required that combination. Product sense to know what researchers need. Engineering judgment to architect the system. Statistical knowledge to ensure methodological rigor. Design intuition to make it usable.

I'm not world-class at any one of these. But I'm competent at all of them. And AI amplified each one. The combination—plus leverage—let me build what would have required a team.

## The Nadh Warning

Nadh raises a concern worth taking seriously: younger developers risk never building foundational skills, becoming dependent on tools they don't understand.

I agree this is a risk. But I'd frame it differently.

AI doesn't eliminate the need for understanding—it raises the bar for what understanding means. You can't evaluate AI output without knowing what good looks like. You can't direct implementation without knowing what you're building. You can't debug generated code without understanding the system.

The builders who thrive won't be those who type fastest. They'll be those who think clearest. Who can articulate problems precisely. Who know enough about enough domains to spot when AI is wrong.

Code is cheap. Judgment is not.

## What I Learned

Inquiro embeds methodological best practices from J-PAL, DIME, and other research institutions. It knows about cluster-robust standard errors, pre-trend validation, influential observations—not because I hardcoded rules, but because I could articulate what rigor looks like and AI could implement it.

The product exists because I had the talk. The vision, the requirements, the quality bar. AI provided the code.

That's the shift. Not AI doing the work. AI making the work cheap enough that one person with clear thinking can build what previously required many.

Show me the talk.

---

**Sources:**
- Kailash Nadh, [Code is Cheap](https://nadh.in/blog/code-is-cheap/)
- Marc Andreessen on Lenny's Podcast, [The AI Future](https://www.youtube.com/watch?v=87Pm0SGTtN8)
