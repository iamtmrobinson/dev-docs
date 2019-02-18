# Pip

## Install modules

Run the following inside your pipenv shell:

`pip install -r requirements.txt`

## Remove all modules

`pip uninstall -y -r <(pip freeze)`

## Pipenv

Virtual environments created by Pipenv are stored in `~/.virtualenvs` and are named by the project name and a hash of its location e.g. `model-Kovkq8ZR`

Check if a project has an env already by running the following command in the project directory:
`pipenv --venv`

### Running the project

Run `pipenv shell` to enter the shell where a project has its own pip instance.
