# agile-board

This page explains the pull requests sent by [@eastagiletracker](https://github.com/eastagiletracker). [East Agile Tracker](https://eastagiletracker.com) is an agile project tracker built by [East Agile](https://github.com/EastAgile); we build it around real repositories rather than demo data, so we take a public repository's own history, re-render it as a working board, and then do a piece of genuine work on that repository and manage it there — a program we call **agile-board**. If you're reading this, you probably just received one.

## Why did I get a PR from this account?

Your repository is public, active, and had something we could genuinely help with: an open issue, an enhancement a maintainer asked for or labelled, a `TODO` or `FIXME` in your own code, a failing or skipped test, a broken build or type error, a file missing from your published package, or a concrete security finding. We picked one, built it, and sent it. You didn't ask for it, so it's built to cost you as little as possible: merging, closing, or ignoring it are all fine, and no response is expected.

## What's actually in the PR?

One contribution, to code that runs. Not a typo sweep, not a README rewrite, not a reformat, not a refactor nobody asked for — those are excluded by the rules the pipeline runs under, because they cost you review time and give you nothing back.

Before a PR is opened, the change has to clear three gates:

- **Reproduced on your default branch, today.** The defect is demonstrated at your current HEAD — not inferred from an issue that may have been fixed months ago. The command and its output are in the PR body, so you can replay it in a minute.
- **Baselined against your own suite.** Your tests, lint and build are run on the clean tree first, then again with the change. Anything already failing is recorded as yours and left alone; anything *newly* failing means the PR is not sent at all.
- **Covered by a test.** A regression test that fails without the change and passes with it, plus the edges the change touches. Where a harness can't reach it, the PR body carries a manual verification you can replay.

If a candidate can't clear those, we don't send a thinner PR — we send nothing.

## What is the board link in the PR?

A live East Agile Tracker project built from your repository's public history: issues imported as stories, pull requests as labelled stories, milestones as epics. The contribution appears there as a story, so you can see the work in context rather than as a lone diff.

It is built only from data already public on GitHub — nothing is read from your machine, no credentials are involved, and nothing is written back to your repository. The board is readable without an account, and its URL is posted in exactly one place: your own pull request. Where the PR invites you to, sign in with your GitHub account to claim ownership of the board; otherwise ignore it. Nothing in the PR depends on it.

## What happens if I merge it?

The change lands, and nothing else does. The PR touches only the files the contribution needs — no workflow files, no hooks, no CI additions, no unrelated formatting or import reordering, and no dependency changes beyond what the fix itself requires (those are called out in the body when they happen).

## Will I get more of these?

No. At most one pull request per repository, ever — merged, closed, or ignored, that count is final.

## Who runs this?

The East Agile team — the account itself is automated (a machine account, in GitHub's classification). The contribution is built with agentic AI under rules the team wrote, and every PR passes deterministic gates before it can be opened: the reproduction, the baseline comparison, and the regression test above are all blocking. If you'd rather reach a person, contact Lawrence W. Sinclair ([@lwsinclair](https://github.com/lwsinclair)), CEO of East Agile.

## How do I make this stop?

Comment `no-more-prs` on any of our pull requests. That stops us across **all** of your repositories, not just the one you comment on, and it's permanent. We also honor an AI-contribution ban or a no-PRs policy stated in your `CONTRIBUTING`, `README`, or `.github/` — repositories with one are skipped before any work begins.
