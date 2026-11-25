---
name: bigpicture
description: Step back and critically check current work against the overall intent. Use for /bigpicture, "big picture", or when a plan has grown past the problem that started it and the question is whether the work still makes sense, is needed, or is over-engineered.
disable-model-invocation: true
---

> _Lane-agent adaptation: read `docs/harness/lane-agents.md` at the pstack root before following this file. The owner's hard stops there override anything in it._

# Big Picture

Run this when deep in execution and about to add machinery, ask for an approval, or push through a blocker. Also run it when the human asks what this is even about.

1. **State the big picture.** Two sentences at most: what the whole effort is for, in the words of the original request. Quote the actual goal, not the current subtask.
2. **State the immediate issue.** The specific blocker or decision in front of you, in one paragraph.
3. **Test the premise.** Write down the one premise the current approach assumes. Check it against the purpose: does the original goal still need this step, or is the goal already met without it? Two or more fixes that share one premise failing the same gate means attack the premise, not the next fix (`../principle-attack-the-premise/SKILL.md`).
4. **Is this needed?** Sort every active piece of work into three piles: required by the original request, useful but optional, and added by the approach itself. Say which pile each piece is in.
5. **Is this over-engineered?** Count what stands between here and done: artifacts, reviews, agents, guards, wrappers. If deleting a step makes its own problems vanish with it, delete the step (`../principle-subtract-before-you-add/SKILL.md`, `../principle-laziness-protocol/SKILL.md`). Prefer the smallest change that meets the goal.
6. **Verdict.** In plain words: continue, simplify (name what to delete), or stop (name what is already achieved). Give the smallest sound path forward and the one decision, if any, that genuinely belongs to the human.

Rules:

- Evidence over theorizing. Label facts, reports and opinions separately.
- "No, this is not needed" is a good answer.
- Never add machinery to pass this check.
- If the verdict stops work, say what to delete or stand down, not only what to keep.
- A simpler alternative is not verified by being simpler. Hold it to the same evidence standard as the plan it replaces; an unproven shortcut is its own risk, and a step that depends on something never identified or never tested is not a small step.
