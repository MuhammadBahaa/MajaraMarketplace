# Changelog

## 1.0.2 - 2026-07-22

Release-infrastructure update:

- Publish the generated Marketplace package through the registered SSH key.
- No skill behavior, review rules, documentation content, or output contracts changed.

## 1.0.1 - 2026-07-22

Documentation-only release:

- Add the official Skill Craft article cover to the plugin package.
- Link the practical Skill Craft introduction from the plugin README.
- No skill behavior, review rules, or output contracts changed.

## 1.0.0 - 2026-07-22

Initial public release on the `majarrah-marketplace` distribution repo:
SkillCraft review craft for agent skills and plugins.
Both skills were developed test-first in the read-craft plugin and moved
here before any release (evidence: TESTING.md).

- `skill-craft-review` — technical review of agent skills and plugins
  via a fixed 10-dimension walk (loading/portability, discoverability,
  scope, behavior simulation & safety, form-vs-failure, discipline
  enforcement, token efficiency, examples, testing evidence,
  plugin-level), reviewer-stance rules (verdict binds to the submission;
  a reviewer's own fixes never clear findings; hidden instructions are
  stop-and-escalate), required Safety scan and Token cost lines
  (tokens ≈ bytes ÷ 4; flagged waste = per-activation saving), a
  findings table grouped by checklist rule, a severity-mapped
  report contract, and a closing Decision block — the approval
  hand-off: a Call restating the verdict as the approver's next
  action, plus up to three approver-only open questions (policy,
  environment, team norms) or an explicit `none`. Built on the superpowers `writing-skills` skill
  v6.0.3 (MIT, (c) 2025 Jesse Vincent); near-verbatim upstream copy
  retained (one documented trim — a runtime-directory links sentence
  that doesn't resolve here; see its provenance header) with per-check
  provenance tags (inherited / adapted / skillcraft), gated to
  dimension-9 use, and verified against upstream through v6.1.1.
- `skill-walkthrough` — guided, organized read of a skill for a human
  reviewer, in one five-part skeleton (description & trigger cases,
  workflows & steps, rules with loopholes quoted, output/blast-radius,
  tools & scripts with hidden-instruction check), closed by a Decision
  block; delivered complete in one message, in the reader's language.
