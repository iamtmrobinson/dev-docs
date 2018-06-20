# Git

## Branching

Clear local (merged) branches:
```
git branch --merged | egrep -v "(^\*|master|dev)" | xargs git branch -d
```

Remove local references to remote branches that have been deleted:
```
git fetch -p origin
```
