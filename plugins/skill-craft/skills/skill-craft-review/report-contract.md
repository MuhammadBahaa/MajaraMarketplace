# Review Report Contract

Use exactly this structure:

```markdown
# Skill review: <name>
**Verdict:** READY | READY-WITH-FIXES | NEEDS-WORK | BLOCKED — <one sentence why>
**Safety scan:** hidden instructions: none found | <F-refs> · unguarded destructive ops: none | <F-refs>
**Token cost:** description ~<n> · body ~<n> · support files ~<n> · flagged waste ~<n> (tokens ≈ bytes ÷ 4)

## Findings
| ID | Severity | Rule | Location | Issue → concrete fix |
(rows grouped by checklist dimension, in checklist order — Rule is
`D<n> <short name>`, e.g. `D4 safety`, or `general` when no dimension
fits; within a group, most severe first. Every finding gets an ID
(F1, F2, ...), a severity, and a fix.)

## Dimension coverage
| # | Dimension | Status |
(one row per checklist dimension: clean | F-refs | n/a — why | not reviewed — why)

## Enhancements
(improvements beyond defects — structure, discoverability, tooling)

## Done well
(one specific author-written strength, or `none — no defensible strength
found`; never praise your own fixes)

## Not reviewed
(what you could not verify, and how the author can — e.g., cold trigger test)

## Decision
**Call:** approve as-is | approve — queue the listed fixes | hold — fix the majors, then re-review | do not approve — F<n> needs a human first
**Open questions:** (up to three only the approver can answer, each with one line on why it matters — or `none`)
```

Fill every slot and dimension row, even when clean. Measure tokens per file as
bytes ÷ 4; flagged waste is the content a finding says to cut. Give every
finding an F-id and concrete fix.

| Worst finding | Meaning | Verdict | Call |
|---|---|---|---|
| `[blocker]` | won't load/trigger, dangerous, or defeats safety | BLOCKED | do not approve; named F-id needs a human |
| `[major]` | misfires, is rationalized away, or wastes serious context | NEEDS-WORK | hold; fix majors and re-review |
| `[minor]` | clarity or consistency defect | READY-WITH-FIXES | approve; queue fixes |
| `[polish]` or none | nice-to-have or clean | READY | approve as-is |

Decision adds no judgment. Open questions are at most three approver-only
policy, environment, or team-norm choices. Defects stay in Findings; if no
question exists, write `none`.
