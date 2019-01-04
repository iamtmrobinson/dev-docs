# Git

## Branching

Operates on references under `refs/remotes/...` It doesn't affect local branches
```
git fetch --prune
```

Clear local (merged) branches:
```
git branch --merged | egrep -v "(^\*|master|dev)" | xargs git branch -d
```

Force remove local branches:
```
git branch -D branch_name
```

## Reverting

Find the revision you wish to revert (**not** the revision you wish to revert _to_) using `git log`. Then use the hash to revert:
```
git revert 2eb9064466437acff735b338cbb4ad16e48a89b2
```

The change will be reverted and you can use `git show` on the latest revision in `git log` to see what was changed in the revert.

`git push` to complete the revert.