# Homeworks

## Guide

- Each group MUST create a Pull Request to this repo, with a file named `Answer.md` inside this `Homeworks` folder.
- Set the Pull Request name as your Group name. For example: `Group 1`
- Write out your Group's members and other notices in the Pull Request description.
- Write out steps and commands that you made to complete each homework in the answer file.

## Homework 1

Write bash aliases that:
- Delete all stopped containers
- Delete docker images that have no tag
- Stop all running containers

## Homework 2

We already know that Docker actually runs inside the system. Give an example that explain how we can tell a process is running inside or outside docker container. Hint: process tree.

## Homework 3

Working repo: https://github.com/vigov5/framgiatw_flask_demo

Write a `Dockerfile` that set-up project's environment

- Create virtualenv folder: `venv`, instal python and required packages listed in `requirements.txt`
- Create DB and user according to config in `config.py`
- Run migration with alembic
- Run `python seed.py` to generate messages
- Run server on port `5000` with `gunicorn` or development server with command: `python  run.py`

## Homework 4

Working repo: https://github.com/vigov5/framgiatw_flask_demo

Write a `docker-compose` file that:
- Create 3 container: `nginx`, `code`, `mysql`
- `code` container is web server running on `gunicorn` on port `8000`. Source code is mounted to this container.
- `mysql` is DB container that web server connect to
- `nginx` is gate-way container, run on port `8080`. When we access, request is forwarded to `code` container.
