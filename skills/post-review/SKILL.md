---
name: post-review
description: Use when someone shares a draft social media post, thread, carousel or newsletter section and asks if it is ready, how to improve it, or for a score. Scores the draft on hook, single idea, proof, voice, network format and call to action, and returns concrete corrections. Never publishes or schedules anything.
---

# Post review

A post fails for a few predictable reasons: a weak first line, two ideas fighting, claims without proof, a voice that is not the author's, a format that ignores the network, or no clear next step. Score each one and fix the lowest first.

## Inputs

- The draft and the network (LinkedIn, X, Instagram, Threads, newsletter...).
- `.agents/voice.md` and `.agents/product-context.md` if they exist.
- The goal of the post (reach, comments, clicks, leads) if the author knows it.

## Scorecard

Score each criterion from 0 to 2 (0 missing, 1 weak, 2 strong). Total out of 12.

| Criterion | 2 means |
|---|---|
| Hook | The first line (before "see more") makes the target reader stop: a specific claim, number, tension or question, not a greeting or a generic statement |
| One idea | The whole post serves one idea that fits in a sentence; nothing could be cut without losing it |
| Proof | Claims are backed by an example, number, story or source the author can stand behind |
| Voice | Sounds like `voice.md`: vocabulary, rhythm and stance match; no phrases the author would never use |
| Network format | Length, line breaks, hashtags, links and media fit the network's norms and where the link should go |
| CTA | One clear next step that matches the goal, or a deliberate choice to have none |

## How to review

1. State the idea of the post in one sentence. If you cannot, the "one idea" score is 0 and that is the first fix.
2. Score each criterion and quote the exact part of the draft that justifies the score.
3. For every score below 2, give a corrected version of that part, not advice. For the hook, offer three alternatives with different angles.
4. Check facts and news: any claim about a third party, a statistic or a recent event needs a primary source. Mark it if missing.
5. Return the revised draft with changes kept to what the scores required.

## Rules

- Never publish, schedule, post or send anything, and never ask for credentials to do it.
- Keep the author's voice. Corrections that make the post sound generic are wrong even if they "read better".
- No engagement bait the network penalizes or that misleads (fake questions, "comment YES", false claims).
- Do not invent numbers, stories or testimonials to strengthen the proof; ask the author for real ones.

## Output

```
Idea: one sentence
Score: 9/12 — hook 1, one idea 2, proof 1, voice 2, format 2, CTA 1
Fixes (lowest first):
- criterion — quoted part — corrected version
Hook alternatives: 1. ... 2. ... 3. ...
Sources needed: - claim — why
Revised draft: ...
```

## Known failures

_Record real mistakes here with a date and the rule that prevents them._
