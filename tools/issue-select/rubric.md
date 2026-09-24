# Rubric: is this a good first issue?

<!--
THIS IS THE PART YOU WRITE. The skill in SKILL.md executes whatever checks
you define here. It ships empty on purpose: the judgment is your work.

A filled rubric must contain:

1. At least one row in the checks table. Each row needs all four columns:
   - Check: a short name (used in the output JSON).
   - Evidence: exactly what to look at, and where. Name the source
     (repo-facts block, issue body, comment thread, or the locations in
     references/evidence-guide.md). "The repo" is not a source; "the last
     5 default-branch commit dates" is.
   - Pass condition: a condition someone else could apply and get your
     answer. Prefer thresholds with numbers ("a maintainer commented
     within 30 days") over adjectives ("maintainer is responsive").
   - Weight: `required` (a fail here rejects the issue) or `preferred`
     (never changes the verdict; a nice-to-have that helps rank the
     issues you accept).

2. A verdict rule below the table: how the check grades combine into
   accept or reject, including how `unclear` is treated. The verdict
   space is binary. If you write no rule for `unclear`, the skill treats
   it as fail.

Cover what actually kills first contributions. The lecture named four
families: the maintainer is alive, the repo is in use, the scope fits a
newcomer, and nobody else is already on it. A rubric that ignores a family
will fail eval issues designed around that family.
-->

## Checks

| Check | Evidence | Pass condition | Weight |
|---|---|---|---|
| maintainer-active | The maintainer first-response sample in the repo-facts block and maintainer activity in the issue comment thread | Pass if either 1. an Owner, Member, or collaborator responded to a recent issue within 60 days, OR 2. at least one of the last 5 default-branch commits is a recent non-bot human contribution. | required |

| repo-active | The archived flag, last 5 default-branch commits, and latest release fields in the repo-facts block |Pass if the repository is not archived and either at least one of the last 5 default-branch commits is within 90 days of the capture date or the latest release is within 180 days. | required |

| newcomer-scope | Issue body, issue comment thread, labels/opener role, and linked-PR history | Pass if the issue asks for one bounded contribution outcome. Multiple files, pages, modules, suspected causes, or implementation steps still count as one bounded outcome when they all serve the same requested result. A terse description or missing reproduction steps do not fail this check by themselves, especially when the issue was opened by a maintainer or carries a good-first-issue label. Fail if the issue is explicitly an umbrella/tracking issue, is a pure usage/support question, has unresolved design debate with no maintainer-settled direction, requires unspecified changes to core internals, has a required product/design input explicitly marked TBD or otherwise missing, or has multiple abandoned implementation attempts indicating hidden difficulty. | required |

| unclaimed | this issue: assignees, linked PR state in the repo-facts block, and claim comments in the issue thread |Pass if there is no current assignee, no open linked PR, and no unresolved recent comment indicating another contributor is actively working on the issue. Old claims that were explicitly abandoned, unassigned, or followed only by closed PRs do not count as active claims. | required |

| contribution-policy | The contribution policy field in the repo-facts block and any AI-specific contribution policy described there | Pass if the repository does not explicitly prohibit AI-generated or AI-assisted code/documentation. Policies requiring disclosure, testing, human review, or personal understanding pass. No stated AI policy also passes. | required |
## Verdict rule

Accept the issue only if every required check passes. Reject the issue if any required check fails. Treat `unclear` as fail for required checks. Preferred checks do not change the accept/reject verdict and are used only to rank accepted issues.
<!-- State how the grades above combine into accept or reject, and how
unclear is treated. Example shape (write your own): "accept if every
required check passes; preferred checks never change the verdict, they
rank accepted issues; unclear counts as fail." -->
