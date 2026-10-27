---
name: verify-code-changes
description: Run the complete project test suite after code changes, including user-authored changes presented for review. Use for code edits and code-change reviews in this repository.
---

# Verify code changes

Use this workflow after changing source or test code in this repository, and when the user asks you to review code changes they made.

1. Finish the requested code edits before verifying.
2. Run the complete test command documented in the repository's `AGENTS.md` from its stated working directory. This ensures newly added tests are included by the project's test discovery. If the documented executable is unavailable, use an equivalent launcher or configured workspace runtime; if neither is available, report the blocker.
3. Report the command actually run, working directory, and actual pass/fail result. If the suite cannot run, report the blocker and do not claim it passed.

When the user asks only for review of their edits, run the suite and report failures without changing their code unless they also asked you to fix it.
