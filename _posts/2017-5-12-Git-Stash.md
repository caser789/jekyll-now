---
layout: post
title: Git Stash
---

```
git stash --include-untracked
git stash -u

git stash save "changes in progress for issue #12345"

git stash list
git stash list --oneline

git stash show cc7b784

git stash show -p cc7b784 # in patch style

git stash apply stash@{1} # will not remove that stash

git stash pop stash@{2}
```
