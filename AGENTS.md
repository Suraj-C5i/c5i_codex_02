# Repository guidance

This is a self-contained Day 2 training bundle about project-specific agent instructions. Keep edits grounded in the lesson materials and preserve the exercises' stated learning goals.

## Read by task

- For bundle purpose or session flow, read [`README.md`](README.md).
- For checkout changes, read [`learner/starter/README.md`](learner/starter/README.md), [`learner/starter/task_card.md`](learner/starter/task_card.md), [`learner/starter/src/checkout.py`](learner/starter/src/checkout.py), and [`learner/starter/tests/test_checkout.py`](learner/starter/tests/test_checkout.py). The task card defines the requested behavior; source and tests show the current contract.
- For A/B run evidence, use [`learner/starter/comparison_worksheet.md`](learner/starter/comparison_worksheet.md).
- For Skills, plugins, or MCP exercises, consult [`learner/skill_and_mcp_lab.md`](learner/skill_and_mcp_lab.md).
- For an SDK integration exercise, first use [`learner/integration_task_template.md`](learner/integration_task_template.md), then the relevant grounding guidance in `learner/skill_and_mcp_lab.md`. The instructor must supply the library, pinned version, contract, approved component, and local check.

## Project facts and working rules

- The learner starter is a small Python project with no package installation required. Its current public function is `calculate_total(items)`, which returns a `float`; item shape and behavior are documented in the starter README, source, and tests.
- After every code change, or when reviewing user-authored code changes, follow [`.agents/skills/verify-code-changes/SKILL.md`](.agents/skills/verify-code-changes/SKILL.md) and run the full documented starter check from its directory: `python3 -m unittest discover -s tests -v`. Report the actual result.
- Keep code changes within the task card's scope. Preserve existing calls and contracts unless the task explicitly changes them; do not add dependencies or alter the item schema unless requested.
- For the lab's no-guidance baseline, use a clean starter copy outside this bundle and under a parent with no `AGENTS.md` in its ancestor chain. This root file applies when the starter remains inside this bundle. Put learner-authored `AGENTS.md` only in the guided copy.
- Keep integration exercises local and verifiable with mocks or fakes. Follow the integration template's limits on production access, credentials, and customer/payment data.
- Work from files that exist in the checkout. If a referenced file is absent, requirements conflict, or an integration detail is missing, state the evidence and ask for clarification instead of inventing a project fact or policy.
- Treat `.git/` and `.DS_Store` as repository or filesystem metadata, not lesson or application source.
