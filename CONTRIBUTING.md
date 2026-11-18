# Contributing to CUB-CORR

## Opening an issue

Pick one of the issue forms on the "New issue" page. Each form sets the issue type:

| Form | Use it for | Type | Label |
|---|---|---|---|
| **Bug** | Code crashes, returns a wrong result, or behaves differently than documented | Bug | none |
| **Concept bug** | A clinical concept or variable returns wrong, missing or unstable values | Bug | `variable` |
| **Feature** | New functionality, a new concept, or an improvement to something that works | Feature | none |
| **Task** | A specific piece of work, such as refactoring, documentation, tooling or infrastructure | Task | none |

One problem per issue. Put the conclusion first and the evidence after it. Use counts, shares and aggregated plots, never patient-level data. An issue that still needs information can carry the `draft` label.

Labels are only set in repositories that have them. `gh issue create --label` fails on a label the repository lacks, so check with `gh label list` first.

If an issue can only start after another one is done, add that one under **Relationships → Blocked by**. The project board reads the Blocker field from there.

## Creating issues from the command line or an agent

`gh issue create --body …` and the API skip the forms. Set the type with `--type`, and write the body with the same `###` headings, in this order, so the issue reads the same as one created from the web form. Drop optional sections that you would leave empty, and keep the required ones.

**Bug:** `--type Bug`

```markdown
### Problem
### How to reproduce
### Expected behavior
### Cause and proposed fix   (optional)
### Version                  (optional)
```

**Concept bug:** `--type Bug --label variable`

```markdown
### Affects
### Problem
### Evidence
### Proposal                 (optional)
### Status
One of: Reported, not analyzed yet · Analyzed, fix to be written · Code ready
### Depends on               (optional)
```

**Feature:** `--type Feature`

```markdown
### Why
### Proposal
### Affects                  (optional)
### Depends on               (optional)
```

**Task:** `--type Task`

```markdown
### Why
### What to do
### Done when                (optional)
### Out of scope             (optional)
### Depends on               (optional)
```

Example:

```shell
gh issue create --repo CUB-CORR/corr-vars --type Bug --label variable --title "…" --body-file issue.md
```
