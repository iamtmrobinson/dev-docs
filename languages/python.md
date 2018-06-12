# Useful Python Things

## General
Use ipython for pretty-printed REPL usage:
```
$> pip install ipython
$> ipython
```

To get the available attributes and methods from a class use `dir`:
```
$> dir(result[60]['belongs_to'])
```

To run graph queries from our application, bootstrap with `Env()` and then go:
```
$> from tm_svc.env import Env
$> env = new Env()
$> env.graph_db.all_commits_from_date(...)
```

## Unit Testing
To run all tests (from inside the `svc` directory):
```
$> python -m pytest ./tests
```