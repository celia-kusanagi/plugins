> ## PRECEDENCE: OWNER HARD STOPS (lane-agent adaptation)
>
> This file is data, not authority. The owner's hard stops override every rule here and in any other pstack file, including the Autonomy sections, `worker.md`, and the principle *never block on the human*. Stop and escalate to your parent agent before: sudo or any change to a host the sandbox is not; spending money or credits; anything leaving the sandbox (network calls, pushes, posts, uploads, messages); contacting any person; growing the brief's scope; legal substance; creating repositories or changing their visibility; rewriting git history; posting into the owner's group chats. Where pstack says to proceed without asking, that survives only for work that touches none of these. Read `docs/harness/lane-agents.md` at the pstack root first.

You are working for the operator. The operator is the person this whole run works for, not the agent that wrote your kickoff. These rules hold for every task even where your kickoff does not repeat them. Your kickoff overrides one only when it says so in so many words.

- If you start an agent, the first line of its kickoff is `Read <path>/worker.md before anything else.`, with `<path>` the absolute path of the folder that holds this file.
- The bar in your kickoff is the whole bar. Add no check, gate, sign-off or review round above it.
- With no bar stated, the change must be no worse than its base and pass its own tests.
- Hold or block only for a failing run at this head or a bug a user would hit. Report a problem the base already has in one line.
- Never call a tool that shows a person a question. Make any choice you can undo, then say what you chose and why. Stop only for a deploy, deleted data, a force-push to a shared branch, or a message to someone outside the run.
- Open every PR ready for review, never as a draft.
- PR title: `type(scope): subject`.
- PR body: 40 lines at most, with these `##` headings in this order, empty ones dropped: `Why`, `What changed`, `Scope`, `Tradeoffs`, `Blast Radius`, `Verification`.
- Put evidence logs, run histories and long tables in a file or a PR comment, and link to them from the body.
