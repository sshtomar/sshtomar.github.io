# Interface Craft — Working Knowledge Library

> A collection of principles and frameworks to help guide design decisions, iterate with intention, and consistently raise the bar for quality in your work.

Source: [interfacecraft.dev/library](https://www.interfacecraft.dev/library)

---

## 1. Noticing

**A foundational skill necessary to develop an eye for details.**

URL: [/library/noticing](https://www.interfacecraft.dev/library/noticing)

Sections: Learning to notice · Reactions as data · What to notice · Building the habit

### Learning to notice

References a fable about Louis Agassiz, a 19th century Harvard naturalist. He gave a student a sunfish and told him to write down everything he noticed. The student thought he was done after an hour, but Agassiz kept saying "keep looking." After a week, the student had prepared a detailed report — the lesson being that our first reaction is almost always shallow. Noticing is a practice of truly considering, and staying with it longer.

### Reactions as data

When you notice something, it's a chance to build your intuition and taste. Try a lot of things and notice your reactions to them.

Examples cited:
- Chef William Bradley (Addison, 3 Star Michelin) tried dozens of plates for his signature dish Eggs & Rice before finding a heavy stone piece that perfectly complemented the dish
- Nicolas (founding designer of Vercel) noticed a corner radius was off in Apple's WWDC Mail app window
- Joseph Alessio noticed that Apple Card's gradient is semantically dynamic based on spending categories
- Josh noticed something off in the animation origin of Vercel's analytics page

### What to notice

- **Moments of hesitation** — What caused it? Uncertainty? Lack of trust?
- **Expectation gaps** — Where did your mental model break?
- **Emotional shifts** — Why are you suddenly annoyed? What triggered a smile?
- **When something's missing** — What were you looking for?
- **What's being assumed** — What is the interface assuming? What's hidden vs surfaced?
- **How it looks to you** — Cheap or crafted? Typography feel right? Clear hierarchy?
- **How it makes you feel** — Fast or sluggish? Durable or fragile?

### Building the habit

Exercise: Find something you use regularly and spend 10 minutes just noticing. Write down what you find. Be specific — don't just say "it feels nice" or "the design is clean." Write down *why*.

---

## 2. Conceptual Range

**Exploring a wide range of disparate solutions before committing.**

URL: [/library/conceptual-range](https://www.interfacecraft.dev/library/conceptual-range)

Sections: Dangers of early commitment · What breadth actually looks like · How to push past the obvious · Breadth as a hedge against taste

### Dangers of early commitment

When designing a photo backup interface, the instinct is to optimize manual selection (tap, drag, group select). But a simple question reveals the flaw: why do users need to do anything at all? Automatic backup requires no interface.

The danger is immediately going deep on a single assumption rather than exploring fundamentally different approaches.

### What breadth actually looks like

Variations of the same idea (e.g., different numpad layouts for a tip input) show conceptual depth but not range. True range means structurally different directions — preset buttons vs. a slider vs. a gamified experience. Each has different pros/cons and provokes different reactions.

### How to push past the obvious

- **Remove (or add) a constraint** — What if this wasn't a screen? What if it happened automatically?
- **Blend from other domains** — How would this work as a game? What if Muji made it?
- **Invert the problem** — Instead of finding what they want, help eliminate what they don't
- **Set an arbitrary range** — Force yourself to come up with 5, 12, or 20 ideas
- **Optimize for facets** — What if this was 10/10 on durability? Differentiation? Desirability?

Example: Devin Jacoviello and Pablo Delcan explored 15 conceptual directions for the cover of Stewart Brand's *Maintenance of Everything* before going deep on the chosen direction.

### Breadth as a hedge against taste

Your taste is limited by what you've seen. Going straight to depth on a familiar idea robs you of the chance to explore the unfamiliar. Heston Blumenthal's famous "Scrambled Egg and Bacon Ice Cream" exists because of extremely broad conceptual exploration.

---

## 3. Conceptual Depth

**Refining a solution through intentional iteration.**

URL: [/library/conceptual-depth](https://www.interfacecraft.dev/library/conceptual-depth)

Sections: The spectrum · The nature of the journey · Tactical steps · Takeaway

### The spectrum

Think of any concept on a spectrum from 1 to 10. Level 1 is the default/minimum. Level 10 is the best version you can possibly imagine. Most work ships at levels 1-3, not because that's all that's possible, but because it's easy to stop pushing.

### The nature of the journey

- **Early levels**: Fixing obvious problems, resolving edge cases, addressing what's in front of you
- **Later levels**: Discovery and invention — no longer clear what might make it better, but pushing to see what's possible. Breakthroughs can be unexpected. Sometimes it's maniacally forcing yourself to refine, reduce, and hack away at the unessential.

Examples:
- Devin and Pablo iterated 70+ times on the *Maintenance of Everything* cover after choosing the direction
- Andy Allen designed "the world's most satisfying checkbox" through extensive refinement

### Tactical steps

- **Zoom in** — Pick one thing and give it all your attention. What if this was the only thing?
- **Remove something** — Take away what's not working. Did you actually need it?
- **Name what isn't working** — Even if you can't fix it, articulate the problem
- **Reference the best** — Find exceptional, world-class examples. Notice them. Let them reveal gaps
- **Generate more** — Sometimes there's no easier way to improve than to create more options
- **Critique** — Critique it yourself or get feedback. Consider your facets of quality

### Takeaway

Most work stops far before it realizes its potential. The discipline: pick a direction and push it as far as it can go. Spend more time than you think necessary.

---

## 4. Live Tuning

**Creating an immediate connection to what you are creating.**

URL: [/library/live-tuning](https://www.interfacecraft.dev/library/live-tuning)

Sections: The big idea · Taking it further · Get started · DialKit

### The big idea

Live tuning (also called parametric visualization) means exposing key parameters so you can adjust them in real time and feel the difference instantly. Duration, easing, spacing, shadows, blurs, position, scale — whatever you're dialing in, make it adjustable on the fly.

### Taking it further

Feeling the difference between values instantly builds intuition faster. You can also leverage this to find combinations you never would have landed on by guessing or iterating one by one.

Example: When exploring generative graphics for collection cards, used Claude to create a toggle showing many random iterations of the graphic at once, with adjustable count and columns, to see a wide range of possibilities.

### Get started

Starter prompt for v0 or Claude:

> Create a visual stack of cards that look slightly scattered, like someone tossed them on a table. Add a floating control panel with sliders to adjust: rotation range (how much each card tilts), vertical offset between cards, shadow blur and opacity. Update the cards in real time as I drag the sliders.

### DialKit

A simple library called DialKit that provides an instantly beautiful, useful parameter tuning panel for anything. Demonstrated in the Collaborating with AI collection.

---

## 5. Uncommon Care

**Pushing beyond to make people feel something.**

URL: [/library/uncommon-care](https://www.interfacecraft.dev/library/uncommon-care)

Sections: People notice · Leaning into humanity · Why it matters now · Going above and beyond · Prompts

### People notice

True care shows up in the places most people overlook — edge cases, error states, conditions only a few customers see. What people really feel and remember are moments when someone went further than they had to.

Examples:
- **Porsche 928** (1970s): Clutch pedal tread pattern spelled out "928"
- **Little Guy** (Daniel Kuntz): Custom screws where the screw head holes form the company logo

These choices are "breadcrumbs" — evidence you're using a product made by someone who deeply cared.

### Leaning into humanity

AI gives immense leverage over work. The question: do we fill saved time with more pedestrian work, or pour more of ourselves into what we create?

Example: Before launching Interface Craft, wrote 100 personalized notes for past colleagues, mentors, and friends who might sign up (matched to email, not name, to avoid misidentification). Most probably never saw them, but it brought joy and made those who did feel seen.

### Why it matters now

As AI makes it trivial to produce passable work, the bar for "good enough" collapses. The way to stand out is to go beyond — to make people feel something. That requires time, effort, and care that can't be automated.

### Going above and beyond

- Built self-serve invoice download instead of manually emailing Stripe PDFs
- Added Purchasing Power Parity, then retroactively refunded users from PPP-eligible countries who had already purchased at full price
- Worked with Vercel and Anthropic to get every founding member at least one month of pro access to AI tools

### Prompts

- Where are you stopping at good enough? What would it look like to push beyond?
- What's the skeleton in the closet of what you're working on?
- Where are you limiting yourself because it feels uncomfortable to lean in?

---

## 6. Separation of Concerns

**Focusing attention on resolving discrete concerns.**

URL: [/library/separation-of-concerns](https://www.interfacecraft.dev/library/separation-of-concerns)

Sections: The design process · In practice · A note on fidelity and collaboration · Intentionality

### The design process

Reference: Jenny Wen's talk on how the traditional design process no longer serves us. Even as tools change, there's value in applying intention and separating areas of concern. Sometimes that looks "dangerously close to a wireframe."

### In practice

When building confidence in an interaction (like the Interface Craft homepage cards), you don't need fully designed cards with complete generative artwork. Start fast and loose with key questions:
- Is this direction worth pursuing?
- Will it feel as good as I'm imagining?
- Should I expand range and explore another approach?

All you need is a "breakable toy." Only refine details once you know the direction is right.

Includes a Framer Motion card fan/hover prototype prompt for creating a minimal interaction demo with 5 white cards in a fan pattern, spring physics hover, and click-to-expand behavior.

### A note on fidelity and collaboration

Work at a fidelity level conducive to the audience and decision at hand. Sometimes whiteboard sketches suffice; other times you need shippable-level fidelity. The point is to be intentional about what you're trying to resolve.

### Intentionality

Before diving in, mentally identify what concern you're resolving or question you're answering. Then use the right tool/format and go as far as needed.

Note: Everything in the Library at launch (website, purchase experience, content, tools) was created in just over 4 weeks from mid-January to early February 2026, exclusively on nights and weekends — made possible by applying maximum effort with continual intentionality.

---

## 7. Facets of Quality

**Defining and improving the attributes that matter most to you.**

URL: [/library/facets-of-quality](https://www.interfacecraft.dev/library/facets-of-quality)

Sections: Defining your facets · Putting them to use · Structure for critique and planning · Takeaway

### Defining your facets

Facets aren't general qualities all products should have (usefulness, intuitiveness, reliability) but specific external characteristics you want users to perceive — what they see, experience, feel.

Interface Craft's facets:
1. **Crafted** — Feels well-made by someone who spent their life honing their trade. Considered and created with care.
2. **Fidgetable** — Feels fun, interactive, playful. Almost physical.
3. **Authentic** — True expression, genuine care for design and humanity. Made with love.
4. **Expansive** — Substantial, a living body of work that accumulates in breadth, depth, and value.
5. **Inventive** — Novel. Something different, something you've never seen before, in a way that inspires.

### Putting them to use

Visualize facets in a radar chart (scale of 1-5 or 1-10). 1 = absolute minimum, top = best you can imagine.

Initial release self-evaluation (Feb 10, 2026):
- Crafted: 3
- Fidgetable: 3.5
- Authentic: 4.5
- Expansive: 1.5
- Inventive: 3.5

This creates a guide for the next release — you know exactly what needs work.

Can also stack-rank facets by importance. Works for teams or solo — creates shared language for discussing quality.

### Structure for critique and planning

Enables precise feedback: instead of "it needs more work," say "this doesn't feel inventive enough — if we're targeting a 4, this feels like going backwards."

Measuring facets over time doubles as a planning tool.

### Takeaway

Define what matters, evaluate rigorously, and improve with relentless iteration.

---

## 8. Less, but Better

**A discipline of minimalism.**

URL: [/library/less-but-better](https://www.interfacecraft.dev/library/less-but-better)

A principle from Dieter Rams. Fight the tendency to add more features, scope, flourish. Design less, then refine and iterate until it's great.

Also quotes Bruce Lee: "It is not daily increase but daily decrease, hack away the unessential."

Example: The Interface Craft pre-launch website — a single page with two typefaces, three sizes, two neutral colors, one button. The hero is a set of cards with animated graphics, simple colors, and one key interaction. As little as possible, executed to an incredibly high bar. The result was incredibly effective. Adding more would have halved the impact.

---

## 9. Recreate Everything

**A way of rapidly learning and growing your skillset.**

URL: [/library/recreate-everything](https://www.interfacecraft.dev/library/recreate-everything)

Sections: The Weight of Paper · Demonstration · Bias towards doing

### Core idea

The best way to learn is to do it. Follow a simple rule: anything that inspires you or makes you wonder "how did they do that?" — try to recreate it. Ideally as soon as possible, while the spark of curiosity is fresh.

### The Weight of Paper

Reference: Marijana Pavlinovic's project — an homage to her grandfather's stamp collection. The "Give Feedback" interaction features a postcard with a genie-like transition reminiscent of macOS.

### Demonstration

Not knowing how to build that genie effect on the web, immediately spun up a playground and started prompting Claude Code iteratively:

1. Start with a basic card that animates down toward a button with spring physics
2. Add the "genie" pinch effect — bottom pinches inward while top stays wide (using Three.js mesh/displacement)
3. Make the deformation organic with nice curves
4. Make the sides concave — curve inward like being sucked toward the button

The result was rough and unpolished, but the goal was just to learn the technique (separation of concerns). Done in a few minutes, now a new tool in the toolbelt.

### Bias towards doing

Don't just be inspired — actually try and make it. Share it. That's the best way to learn.

---

## 10. Industry Standards

**Understanding the invisible bar that users expect.**

URL: [/library/industry-standards](https://www.interfacecraft.dev/library/industry-standards)

Sections: Hard truths · Platform standards · So where's the bar? · Default, then innovate · Takeaway

### Hard truths

Apps used daily (Instagram, Notion, TikTok, iOS, Linear, Figma, YouTube, Telegram) form an invisible bar — the industry standard. If your product doesn't meet it, people immediately discount it. They assume it's poorly made and won't tell you why.

Applies everywhere: portfolio work, prototypes for stakeholders, MVPs in sales demos.

### Platform standards

iOS provides Human Interface Guidelines, standardized APIs, system components. The web is messier — no centralized operator — but the standard still exists, set by popular sites and tools.

### So where's the bar?

Interactive exercise: 6 financial iOS app detail views to rank from worst to best and place "the bar." The point isn't having the right ranking but developing awareness of where the standard is. The industry standard is the **floor**, not the goal — ideally you go well beyond it.

### Default, then innovate

Simple advice: start with how iOS would design it, then improve. (For web: start with the default shadcn + Tailwind app, then improve.)

Examples:
- **Family** (fintech app): Looks like an Apple-made app. Took iOS defaults (tableviews, view transitions), showed respect for platform standards, but innovated on every aspect. Benji (designer/founder) has written about "Family Values."
- **Raycast**: Mac app that feels completely native but everything is a little to a lot better than Apple's Spotlight.

### Takeaway

Start with the defaults. Understand the standards. Then innovate. Don't start from scratch and end up below what everyone expects.

---

*Saved from interfacecraft.dev/library on 2026-02-14*
