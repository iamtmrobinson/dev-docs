# Python

## General

Use ipython for pretty-printed REPL usage:

```
pip install ipython
ipython
```

To get the available attributes and methods from a class use `dir`:

```
dir(result[60]['belongs_to'])
```

To run graph queries from our application, bootstrap with `Env()` and then do:

```
from tm_svc import env
my_env = env.Env()
my_env.graph_db.all_commits_from_date(...)
```

Debugging an Intent in the REPL:

```
from tm_svc import env
environment = env.Env()

intent_string = 'Please get commits from tm_web'

get_commits_intent = environment.intents.detect_intent(intent_string)

team_id = 'T7T62HUQ0'
user_tom_robinson = { 'user': 'U9J1ZSB34' }

get_commits_intent.action(team_id, user_tom_robinson)
```

For auto reload: (https://stackoverflow.com/questions/1907993/autoreload-of-modules-in-ipython)

I did this in the REPL:

```
%load_ext autoreload
%autoreload 2
```

Then did the `ipython profile create` stuff from the answer below for doing it automatically in the future.

## Unit Testing

To run all tests (from inside the `svc` directory):

```
python -m pytest ./tests
```

Output to stdout regardless of whether a test passes or fails:

```
python -m pytest ./tests -s
```

## Logging

Formatted strings:

```
f'There were {len(commits)} commits.'
```

Logging information from a class:

```
import logging

# Above the class def:
log=logging.getLogger(__name__)

# To log:
log.info(',smdkadsnc')
```
