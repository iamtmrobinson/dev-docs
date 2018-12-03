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
