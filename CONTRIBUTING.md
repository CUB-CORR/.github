# Contributing to CUB-CORR

## Opening an issue

Pick one of the three issue forms on the "New issue" page:

| Form | Use it for | Label |
|---|---|---|
| **Bug** | Code crashes, returns a wrong result, or behaves differently than documented | none |
| **Concept / data problem** | A clinical concept or variable returns wrong, missing or unstable values, or needs a new definition | `variable` |
| **Task** | A feature, refactoring, documentation, tooling or infrastructure change | none |

Labels are only set in repositories that have them; `gh issue create --label` fails on a label the repository lacks, so check with `gh label list` first.

One problem per issue. Put the conclusion first and the evidence after it. Use counts, shares and aggregated plots, never patient-level data. An issue that still needs information can carry the `draft` label.

If an issue can only start after another one is done, add that one under **Relationships → Blocked by**. The project board reads the Blocker field from there.

## Creating issues from the command line or an agent

`gh issue create --body …` and the API skip the forms. Write the body with the same `###` headings, in this order, so the issue reads the same as one created from the web form. Drop optional sections that you would leave empty, and keep the required ones.

**Bug:** title `Bug: …`

```markdown
### Problem
### How to reproduce
### Expected behavior
### Cause and proposed fix   (optional)
### Version                  (optional)
```

**Concept / data problem:** title `Concept: …`, label `variable`

```markdown
### Affects
### Kind
One of: Wrong or missing values · Values change between runs, windows or observation levels ·
Improvement of an existing concept · New concept
### Problem
### Evidence
### Proposal                 (optional)
### Status
One of: Reported, not analyzed yet · Analyzed, fix to be written · Code ready
### Depends on               (optional)
```

**Task:**

```markdown
### Why
### What to do
### Done when                (optional)
### Out of scope             (optional)
### Depends on               (optional)
```

Example:

```shell
gh issue create --repo CUB-CORR/corr-vars --title "Concept: …" --label variable --body-file issue.md
```
