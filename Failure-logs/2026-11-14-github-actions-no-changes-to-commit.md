# GitHub Actions — No Changes to Commit

**Date:** 14 November 2026

### Problem
The GitHub Actions workflow failed during the Git commit step when there were no new events and the history files hadn't changed.

### Cause
Git cannot create a commit when there are no staged changes. It returns a non-zero exit code, causing GitHub Actions to mark the step as failed.


### Solution
I added `|| true` to the commit command:


git commit -m "updating event links" || true


This allows the workflow to continue even when there are no changes to commit.
---

Status: fixed
