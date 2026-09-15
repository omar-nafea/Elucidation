---
name: explain-from-first-principles
description: Explain and demonstrate any concept from its underlying problem and first principles through advanced practical use. Use when the user wants deep understanding, progressive examples, the reasons behind each idea, meaningful edge cases, or production/backend relevance rather than a documentation summary.
---

# Explain from First Principles

Teach the concept so the learner can reason about it, choose when to use it, and implement or apply it—not merely repeat its terminology.

## Frame the Lesson

Infer the learner's level, domain, and technology from the request. If they are absent, assume a technically curious beginner and use a broadly recognizable example. State any assumption that materially shapes the explanation.

Set a dependency floor: introduce only the prerequisite ideas needed for the next step, and define jargon on first use. Do not recurse into unrelated fundamentals.

Start with the real problem that exists without the concept. Identify the actors or parts, constraints, forces, and invariant the concept must preserve. Then derive the concept as a response to that pressure.

## Evolve the Concept

Use one running example and improve it in stages:

1. Show the simplest direct approach before the concept exists.
2. Expose the concrete limitation or failure that motivates change.
3. Introduce the smallest form of the concept that resolves it.
4. Add important variants only when a new requirement makes them necessary.
5. Finish with an advanced, production-realistic implementation or application.

At every stage explain:

- **What changed** and how it works.
- **Why it became necessary** at this stage.
- **Benefit** in the requested domain, especially backend systems when relevant.
- **Cost or tradeoff** introduced by the change.
- **When to use it** and when the earlier, simpler form is enough.

Keep examples cumulative so the learner can see the evolution. For programming topics, prefer small runnable examples in the user's language or framework. If none is named, use compact language-neutral pseudocode and avoid framework-specific ceremony.

## Cover the Meaningful Space

Include what materially applies to the concept:

- precise definition, boundaries, and internal mechanism;
- common variants and how to choose among them;
- lifecycle, composition, and data or control flow;
- common failures, edge cases, misconceptions, and anti-patterns;
- testing, debugging, and observability;
- security, performance, concurrency, and failure recovery when relevant;
- migration from a simpler approach and when not to use the concept.

Interpret “all cases” as all meaningful common cases, important edge cases, and major alternatives—not an unbounded catalog. Explicitly name material exclusions or context-dependent areas.

When three or more alternatives need comparison, use a compact decision table. Use a diagram or trace only when it makes relationships or execution order clearer than prose.

## Keep It Honest

Separate universal principles from language, framework, and organizational conventions. Verify version-sensitive claims against current primary documentation when the example depends on a specific technology.

Do not invent a backend benefit. If the concept has no meaningful backend application, say so briefly and explain where it does apply.

Do not hide tradeoffs, present an advanced pattern as universally superior, or add abstraction before the running example creates a need for it.

End with concise decision rules the learner can reuse, followed by a short self-check or practical exercise that tests reasoning rather than terminology.
