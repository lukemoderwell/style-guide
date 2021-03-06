# Github style guide

As Github users, we want to ensure our commit messages and PR requests follow similar guidelines across all work.

## Table of Contents

* [Commit Messages](#commit-messages)
* [Pull Requests](#pull-requests)
* [Review Process](#review-process)
* [Merging](#merging)

## Commit Messages

In general, use correct-ish grammar and punctuation. We aren't going to go crazy enforcing this, but try to refrain from things like `lol made sum codez kthxbai`. Funny commit messages, while hilarious, usually aren't helpful for future us.

All commit messages should be prepended with the JIRA ticket number. This keeps master's commit history organized once commits get pulled in. It allows for anyone to easily see what ticket a commit was made for.

```bash
git commit -m "PROJ-123: I made a thing do another thing"
```

If you aren't working on a JIRA ticket, consider what you're doing and maybe make a JIRA ticket for it. If you absolutely do not need a JIRA ticket, that's fine - just make a commit without a ticket number.

## Pull Requests

A PR title should be a quick summary of the work you did. More details can be added in the description field of your PR. 

Similar to commit messages, make sure to include your JIRA ticket number in the PR title.

```
PROJ-123:  Making a thing do a thing.
```

## Review Process

This is less of a style thing and more of a process thing, but I figured it should live here with the other Github stuff.

Github's review process is pretty good, but requires some manual management to fit how we do things. When you open a PR, make sure to assign two reviewers (and let them know you assigned them). When you push a change to an open PR, remove any existing reviews (both Approvals and Changes Required).

If you are the second of the two assigned approvers to approve the PR, move its associated ticket into Testing.


## Merging

When merging master into your branch (in case of conflicts), you can either `git merge` or `git rebase` - it is up to the developer.

When merging a PR into master, always `Squash & Merge`. Review all the commits and remove any that you think are unnecessary - things like `Code fixes` or `Merge conflicts` aren't really needed in the history.

