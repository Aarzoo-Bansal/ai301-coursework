# Unit 1 — Issue Selection

Path: `beat-1-sandbox/unit-1/selection.md`

Record of the issue carried into Unit 2, and of the evaluation runs that produced
`eval-run.txt`. This file is graded at the path above; a copy kept anywhere else in
the repository is not read.

Complete every labelled field below. Each is graded on its own; content placed under the
wrong label is not graded.

---

## Selected issue

**[Issue link](https://github.com/codepath/pathreview-ai301-fa26-s3/issues/69)**

[The individual Path Review issue page. A link to the repository or the issue list
does not satisfy this field.]

**Verdict output**

 Your rubric has no preferred checks — all five are required — so the accepted ordering is driven entirely by the fit profile, which is what scope.md says fit is for.

  Accepted, in fit order

  1. #69 — Output parser crashes on a top-level JSON array fallback
  The best fit by your profile on every axis you named: Python backend logic in rag/generator/output_parser.py, a debugging task with a concrete expected behavior (.items() on a parsed list raises
  AttributeError; the fallback should handle arrays), and real automated-testing work — the fix isn't done until you remove the @pytest.mark.xfail for manifest H-02 and the covering test in
  tests/unit/test_output_parser.py goes green. That's implementation plus testing at a well-defined scope, which your profile prefers over a docs change.

  2. #73 — README and .env.example disagree about which LLM API key to set
  Accepted and the cleanest issue procedurally — zero comments, zero claims, no linked PR — but it's documentation only, with no code, no reproduction, and no test. Your profile takes small doc changes as
  acceptable rather than preferred, so it ranks second despite being the least contested.


  #68 — Keyword search raises ZeroDivisionError when the index is empty
  unclaimed fails: PR #74 by Momik-jpg is open and formally linked via Fixes #68. Worth noting the cost, since fit can't rescue a rejected issue: on your profile this was the strongest fit of the three —
  Python, a posted reproduction, and an H-01 xfail to remove — and it's sunk purely on contention.

  [
    {
      "item": "https://github.com/codepath/pathreview-ai301-fa26-s3/issues/69",
      "checks": [
        {"name": "maintainer-active", "grade": "pass", "evidence": "Last default-branch commit 2026-09-16 by Aburke225, a human non-bot contributor, 7 days before the 2026-09-23 capture date."},
        {"name": "repo-active", "grade": "pass", "evidence": "archived=false and last default-branch commit 2026-09-16 is within 90 days of 2026-09-23."},
        {"name": "newcomer-scope", "grade": "pass", "evidence": "One bounded outcome: 'output_parser.py calls .items() on the parsed value and raises AttributeError... The fallback path should handle array
  responses', plus removing the H-02 xfail marker. Two named files, 2-4 hours, no unresolved design debate."},
        {"name": "unclaimed", "grade": "pass", "evidence": "assignees: [], no cross-referenced PR in the timeline; the three claim comments (Yina-Mu, tonybuii2003, hanluu1) are all author_association NONE,
  i.e. classmates, which the scope.md Path Review house rule says do not block."},
        {"name": "contribution-policy", "grade": "pass", "evidence": "docs/CONTRIBUTING.md and .github/PULL_REQUEST_TEMPLATE.md contain no AI clause; no AI_POLICY.md exists. Silence passes."}
      ],
      "verdict": "accept"
    },
    {
      "item": "https://github.com/codepath/pathreview-ai301-fa26-s3/issues/73",
      "checks": [
        {"name": "maintainer-active", "grade": "pass", "evidence": "Last default-branch commit 2026-09-16 by Aburke225, a human non-bot contributor, 7 days before the 2026-09-23 capture date."},
        {"name": "repo-active", "grade": "pass", "evidence": "archived=false and last default-branch commit 2026-09-16 is within 90 days of 2026-09-23 (no releases, but the OR is satisfied)."},
        {"name": "newcomer-scope", "grade": "pass", "evidence": "One bounded outcome across two named files: 'README.md tells you to add OPENROUTER_API_KEY... .env.example doesn't list that variable... Make
  the two files agree.' Estimated effort 1-2 hours; core/config.py settles which keys are correct."},
        {"name": "unclaimed", "grade": "pass", "evidence": "assignees: [], zero comments, and the only timeline cross-reference is to issue #53 (is_pr=False), so no linked PR."},
        {"name": "contribution-policy", "grade": "pass", "evidence": "docs/CONTRIBUTING.md and .github/PULL_REQUEST_TEMPLATE.md contain no AI clause; no AI_POLICY.md exists. Silence passes."}
      ],
      "verdict": "accept"
    },
    {
      "item": "https://github.com/codepath/pathreview-ai301-fa26-s3/issues/68",
      "checks": [
        {"name": "maintainer-active", "grade": "pass", "evidence": "Last default-branch commit 2026-09-16 by Aburke225, a human non-bot contributor, 7 days before the 2026-09-23 capture date."},
        {"name": "repo-active", "grade": "pass", "evidence": "archived=false and last default-branch commit 2026-09-16 is within 90 days of 2026-09-23."},
        {"name": "newcomer-scope", "grade": "pass", "evidence": "One bounded outcome: guard KeywordSearcher.index() against an empty corpus and remove the H-01 xfail; two named files, 2-4 hours, with a
  working reproduction already posted in the thread."},
        {"name": "unclaimed", "grade": "fail", "evidence": "Open linked PR: timeline shows 'cross-referenced -> #74 is_pr=True state=open fix: handle empty keyword search indexes', body 'Fixes #68', opened by
  Momik-jpg and not merged."},
        {"name": "contribution-policy", "grade": "pass", "evidence": "docs/CONTRIBUTING.md and .github/PULL_REQUEST_TEMPLATE.md contain no AI clause; no AI_POLICY.md exists. Silence passes."}
      ],
      "verdict": "reject"
    }
  ]

  Take #69. One open question your rubric still leaves unsettled, now that the house rule is the only thing standing between you and a shared issue: it neutralizes classmates' claim comments but not their
  open PRs, which is exactly what rejected #68. If you think a student PR shouldn't block either, that's a one-line edit to the unclaimed row — and it would move #68 back into the accepted set, at the top on
  fit.

[Your skill's live-mode output for this issue, pasted verbatim and ending with the
fenced JSON verdict block. A summary does not satisfy this field.]

**The verdict must record `accept` for this issue.** Choose an issue your own skill
accepts. If your skill rejects every candidate you try, that is a signal about your
rubric rather than about the issues: revise it and re-run — retries are unlimited and a
partial re-run costs about $0.20 — or run the skill on different candidates. Output
recording `reject` for the issue you chose earns no credit for this field.

```
paste the output here, including the closing JSON block
```

---

## Eval iterations

Quote source text directly in each field below. Paraphrase does not satisfy them.

**Run history**

[The agreement score of each run you did, in order. A single run is a complete answer if
only one run occurred. **The last score in your list must match the agreement line in the
`eval-run.txt` you committed** — that file is the record of your final run.]

**Issue analysis**

[One scored issue, identified by id (`issue-01` through `issue-20`; the `calib-`
issues are not scored). State your rubric's decision, the gold label, and the
reasoning that produced your rubric's result.]

**Check rationale**

[One check from the `rubric.md` uploaded to `tools/issue-select/`, quoted as it is
currently written, with the reasoning behind its current form.]

**Trade-offs**

[What the quoted check gives up. Any one of these is a complete answer: an issue whose
result it changes, a canary you re-ran with `--only`, a case you accept it will miss, or a
stated reason nothing changed elsewhere. "Nothing changed, and here is how I know" earns
the point in full when the reason follows.]

---

## Selection rationale

Graded on whether all three are answered, in your own words. Not on how good the
reasoning is, and not on length — a short honest answer to each earns the full marks.
This is also the basis for the claim comment you write in Unit 2.

**Selection rationale**

[Answer all three:

1. The issue's fit to your interests and to the time available.
2. What the verdict identified correctly, and what you weighed that the rubric could
   not.
3. The anticipated difficulty in claiming it.]

---

Related paths: `eval-run.txt` in this directory; your skill's files in
`tools/issue-select/`.
