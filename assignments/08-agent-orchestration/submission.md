# Week 8 — Agent Orchestration: The Recipe Box Sprint

This submission contains my completed Week 8 Agent Orchestration assignment, including concurrent agent development and a generator–critic workflow.

**Repository:** https://github.com/hacerdilarakivrak/recipe-box-week8

**Writeup:** https://github.com/hacerdilarakivrak/recipe-box-week8/blob/main/writeup.md

## Summary

- **Concurrent Agents:** Implemented Shopping List and Tag Filter concurrently using two independent GitHub Copilot agents.
- **Git Worktree Isolation:** Used separate Git worktrees and branches to prevent agents from overwriting each other's changes.
- **Concurrency Evidence:** Verified overlapping agent execution using timestamps from exported conversation records.
- **Generator–Critic Workflow:** Implemented Ingredient Scaling through two revision rounds based on independent critic feedback.
- **Final Approval:** Received the Critic's approval after addressing correctness, test coverage, and documentation issues.
- **Human Supervision:** Maintained control over agent permissions, commits, merges, and pushes.
- **Verification:** All 13 pytest tests passed, and all three features were integrated into the main branch.

The complete source code, tests, concurrency evidence, generator–critic transcript, autonomy notes, and lessons learned are available in the repository and writeup linked above.
