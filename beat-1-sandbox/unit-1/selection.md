# Unit 1 — Issue Selection

Path: `beat-1-sandbox/unit-1/selection.md`

---

## Selected issue

**Issue:** [#69 — Output parser crashes on a top-level JSON array fallback](https://github.com/codepath/pathreview-ai301-fa26-s3/issues/69)

### Verdict output

Your rubric has no preferred checks — all five are required — so the accepted ordering is driven entirely by the fit profile, which is what scope.md says fit is for.

Accepted, in fit order

1. #69 — Output parser crashes on a top-level JSON array fallback

The best fit by your profile on every axis you named: Python backend logic in rag/generator/output_parser.py, a debugging task with a concrete expected behavior (.items() on a parsed list raises AttributeError; the fallback should handle arrays), and real automated-testing work — the fix isn't done until you remove the @pytest.mark.xfail for manifest H-02 and the covering test in tests/unit/test_output_parser.py goes green. That's implementation plus testing at a well-defined scope, which your profile prefers over a docs change.

2. #73 — README and .env.example disagree about which LLM API key to set

Accepted and the cleanest issue procedurally — zero comments, zero claims, no linked PR — but it's documentation only, with no code, no reproduction, and no test. Your profile takes small doc changes as acceptable rather than preferred, so it ranks second despite being the least contested.

Rejected

#68 — Keyword search raises ZeroDivisionError when the index is empty

unclaimed fails: PR #74 by Momik-jpg is open and formally linked via Fixes #68. Worth noting the cost, since fit can't rescue a rejected issue: on your profile this was the strongest fit of the three — Python, a posted reproduction, and an H-01 xfail to remove — and it's sunk purely on contention.

```json
[
  {
    "item": "https://github.com/codepath/pathreview-ai301-fa26-s3/issues/69",
    "checks": [
      {
        "name": "maintainer-active",
        "grade": "pass",
        "evidence": "Last default-branch commit 2026-09-16 by Aburke225, a human non-bot contributor, 7 days before the 2026-09-23 capture date."
      },
      {
        "name": "repo-active",
        "grade": "pass",
        "evidence": "archived=false and last default-branch commit 2026-09-16 is within 90 days of 2026-09-23."
      },
      {
        "name": "newcomer-scope",
        "grade": "pass",
        "evidence": "One bounded outcome: 'output_parser.py calls .items() on the parsed value and raises AttributeError... The fallback path should handle array responses', plus removing the H-02 xfail marker. Two named files, 2-4 hours, no unresolved design debate."
      },
      {
        "name": "unclaimed",
        "grade": "pass",
        "evidence": "assignees: [], no cross-referenced PR in the timeline; the three claim comments (Yina-Mu, tonybuii2003, hanluu1) are all author_association NONE, i.e. classmates, which the scope.md Path Review house rule says do not block."
      },
      {
        "name": "contribution-policy",
        "grade": "pass",
        "evidence": "docs/CONTRIBUTING.md and .github/PULL_REQUEST_TEMPLATE.md contain no AI clause; no AI_POLICY.md exists. Silence passes."
      }
    ],
    "verdict": "accept"
  },
  {
    "item": "https://github.com/codepath/pathreview-ai301-fa26-s3/issues/73",
    "checks": [
      {
        "name": "maintainer-active",
        "grade": "pass",
        "evidence": "Last default-branch commit 2026-09-16 by Aburke225, a human non-bot contributor, 7 days before the 2026-09-23 capture date."
      },
      {
        "name": "repo-active",
        "grade": "pass",
        "evidence": "archived=false and last default-branch commit 2026-09-16 is within 90 days of 2026-09-23 (no releases, but the OR is satisfied)."
      },
      {
        "name": "newcomer-scope",
        "grade": "pass",
        "evidence": "One bounded outcome across two named files: 'README.md tells you to add OPENROUTER_API_KEY... .env.example doesn't list that variable... Make the two files agree.' Estimated effort 1-2 hours; core/config.py settles which keys are correct."
      },
      {
        "name": "unclaimed",
        "grade": "pass",
        "evidence": "assignees: [], zero comments, and the only timeline cross-reference is to issue #53 (is_pr=False), so no linked PR."
      },
      {
        "name": "contribution-policy",
        "grade": "pass",
        "evidence": "docs/CONTRIBUTING.md and .github/PULL_REQUEST_TEMPLATE.md contain no AI clause; no AI_POLICY.md exists. Silence passes."
      }
    ],
    "verdict": "accept"
  },
  {
    "item": "https://github.com/codepath/pathreview-ai301-fa26-s3/issues/68",
    "checks": [
      {
        "name": "maintainer-active",
        "grade": "pass",
        "evidence": "Last default-branch commit 2026-09-16 by Aburke225, a human non-bot contributor, 7 days before the 2026-09-23 capture date."
      },
      {
        "name": "repo-active",
        "grade": "pass",
        "evidence": "archived=false and last default-branch commit 2026-09-16 is within 90 days of 2026-09-23."
      },
      {
        "name": "newcomer-scope",
        "grade": "pass",
        "evidence": "One bounded outcome: guard KeywordSearcher.index() against an empty corpus and remove the H-01 xfail; two named files, 2-4 hours, with a working reproduction already posted in the thread."
      },
      {
        "name": "unclaimed",
        "grade": "fail",
        "evidence": "Open linked PR: timeline shows 'cross-referenced -> #74 is_pr=True state=open fix: handle empty keyword search indexes', body 'Fixes #68', opened by Momik-jpg and not merged."
      },
      {
        "name": "contribution-policy",
        "grade": "pass",
        "evidence": "docs/CONTRIBUTING.md and .github/PULL_REQUEST_TEMPLATE.md contain no AI clause; no AI_POLICY.md exists. Silence passes."
      }
    ],
    "verdict": "reject"
  }
]
```

---

## Eval iterations

### Run history

I ran the full evaluation multiple times while revising the rubric. The agreement scores, in order, were:

```text
agreement: 13/20 scored items  (bar: 18/20: below the bar)
agreement: 15/20 scored items  (bar: 18/20: below the bar)
agreement: 16/20 scored items  (bar: 18/20: below the bar)
agreement: 17/20 scored items  (bar: 18/20: below the bar)
agreement: 19/20 scored items  (bar: 18/20: PASS)
agreement: 17/20 scored items  (bar: 18/20: below the bar)
agreement: 19/20 scored items  (bar: 18/20: PASS)
```

The final score matches the committed `eval-run.txt`:

```text
agreement: 19/20 scored items  (bar: 18/20: PASS)
```

### Issue analysis

I analyzed `issue-19`. The final eval output was:

```text
issue-19  accept  reject   NO     failed: newcomer-scope
```

My rubric decided `reject`, while the gold label was `accept`.

The result came from my `newcomer-scope` check. The issue contained multiple suspected causes and possible implementation directions for the same bug. My rubric was intentionally conservative about work that might require deeper investigation or changes to core behavior, so it still classified this issue as outside the scope I wanted for a first contribution.

The gold label treated the different causes and implementation suggestions as parts of one bounded outcome rather than separate pieces of work. This remained the only disagreement in my final run.

### Check rationale

The current `newcomer-scope` check in my uploaded `rubric.md` is:

> `| newcomer-scope | Issue body, issue comment thread, labels/opener role, and linked-PR history | Pass if the issue asks for one bounded contribution outcome. Multiple files, pages, modules, suspected causes, or implementation steps still count as one bounded outcome when they all serve the same requested result. A terse description or missing reproduction steps do not fail this check by themselves, especially when the issue was opened by a maintainer or carries a good-first-issue label. Fail if the issue is explicitly an umbrella/tracking issue, is a pure usage/support question, has unresolved design debate with no maintainer-settled direction, requires unspecified changes to core internals, has a required product/design input explicitly marked TBD or otherwise missing, or has multiple abandoned implementation attempts indicating hidden difficulty. | required |`

I arrived at this wording after earlier versions of the check rejected issues that were actually bounded. One earlier version required an issue to have "enough information to begin work," which was too subjective and caused terse but valid issues to fail.

I also learned from the eval iterations that the number of files, modules, suspected causes, or implementation steps is not by itself a good measure of scope. The current check therefore focuses on whether the work serves one bounded outcome and uses more specific rejection evidence such as umbrella issues, unresolved design decisions, missing required inputs, or multiple abandoned implementation attempts.

### Trade-offs

The current `newcomer-scope` check intentionally favors avoiding ambiguous or unexpectedly large first contributions. The trade-off is that it can reject an issue that is technically involved but still considered sufficiently bounded by the gold label.

The final run demonstrates this directly:

```text
issue-19  accept  reject   NO     failed: newcomer-scope
```

I accept this false negative because loosening the scope rule further could also allow genuinely open-ended or unresolved implementation work to pass. Even with this conservative choice, the final rubric matched 19 of 20 scored issues and passed every category floor:

```text
categories: claimed 4/4  clear-accept 7/8  dead-repo 3/3  policy 1/1  scope 4/4
agreement: 19/20 scored items  (bar: 18/20: PASS)
```

---

## Selection rationale

1. **Fit to my interests and available time**

   I chose issue #69 because it matches the type of work I am most interested in: Python backend logic, debugging, and automated testing. The failure is concrete because the parser calls `.items()` on a top-level JSON array and raises an `AttributeError`. The issue also identifies the relevant implementation and test files. Its estimated 2–4 hour scope makes it reasonable for the time available.

2. **What the verdict identified correctly and what I weighed separately**

   The verdict correctly identified that the repository is active, the issue has one bounded outcome, there is no open linked PR, the contribution policy permits the workflow, and the task matches my stated preference for implementation and testing work.

   I also considered the learning value myself. Issue #73 was simpler and had less contention, but it was primarily a documentation change. I preferred #69 because it gives me a real bug to reproduce, understand, fix, and verify with an automated test.

3. **Anticipated difficulty in claiming it**

   I expect some contention because several classmates have already left claim comments on #69. However, there is currently no linked open PR, and the Path Review house rule used by my skill says classmates' claim comments alone do not block an issue. Before claiming it in Unit 2, I will need to check the issue again to make sure no new open PR or blocking claim has appeared.

---

Related paths: `eval-run.txt` in this directory; skill files in `tools/issue-select/`.
