# Heroku GitHub Action Example

An example workflow, using [the GitHub Action for Heroku](https://github.com/actions/heroku) to deploy [a static website](site/), [octozen.herokuapp.com](https://octozen.herokuapp.com).

## Workflow

The [example workflow](.github/main.workflow) will trigger on every push to this repo.

For pushes to a _feature_ branch, the workflow will:

1. Log in to Heroku Container Registry
1. Tell Heroku to build, then push the Docker image needed to deploy a _staging_ Heroku app
1. Tell Heroku to release the pushed Docker image to the _staging_ Heroku app

For pushes to the _default_ branch (`master`), in addition to the above Actions, the workflow will:

1. Tell Heroku to release the pushed Docker image to the _production_ Heroku app

## License

This repository is [licensed under CC0-1.0](LICENSE), which waives all copyright restrictions.
