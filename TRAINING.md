<!--
*******************************************************************************
Copyright (c) 2026 Qorix GmbH

SPDX-License-Identifier: Apache-2.0
*******************************************************************************
-->

# Onboarding training: Quality, Safety and Security Manager

This repository is your own copy of a training module, `Training_Module`. It is built like a real
S-CORE module: the module template, the S-CORE process description and the same tooling we use in
Performance. Nothing you do here can break a real project, so try things, break the build and
repair it.

The module is fictive. Some of its documents are wrong on purpose. Finding out what is wrong, and
proving it, is the training.

## The week

You have **five working days**. Every task is an issue in this repository, labelled `stage-0` to
`stage-6`. Work through them in order.

| Day | Stages | Done in the evening |
| --- | --- | --- |
| 1 | 0 environment, 1 git | environment works, first pull request merged |
| 2 | 2 build | all defect branches are green |
| 3 | 3 process, 4 review | findings recorded, reviews submitted |
| 4 | 5 module | template update rebased and merged, your role's document filled in |
| 5 | 6 wrap-up | cross-review, formal review and retrospective done |

## Rules

1. **Every issue is closed by a merged pull request** whose description says `Closes #<n>`, with
   green CI. One pull request may close several issues. An issue closed by hand counts as open.
2. **Some issues you create yourself.** The task tells you when. On GitHub, choose
   **Issues → New issue → Training finding** (the template is in
   `.github/ISSUE_TEMPLATE/training_finding.md`) and add the labels `stage-<n>` and your role. An issue must be workable
   without asking you: what is wrong, where, and how one recognises that it is fixed.
3. **The commit carries the reasoning.** Say what you checked and what it returned. In Performance
   the pull request is the approval record, and the reasoning has nowhere else to live.
4. **You merge your own pull requests** once CI is green. Your supervisors read the closed issues
   and pull requests after the week.

## Help

Once in the week you can book a **15-minute help call** with a supervisor. Choose the moment
yourself. Otherwise you work on your own: the issue texts, this file and the linked process
documentation are meant to be enough.

## Getting started

```bash
git clone git@github.com:qorix-group/GuC_onboarding_<name>.git
cd GuC_onboarding_<name>
git remote add upstream https://github.com/eclipse-score/module_template.git
pre-commit install
rm -rf _build && bazel run //:docs
```

`upstream` is the public S-CORE module template this repository was made from. Then open the issue
labelled `stage-0`.
