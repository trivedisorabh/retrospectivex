# Retrospectivex

[![CircleCI](https://circleci.com/gh/dreamingechoes/retrospectivex.svg?style=shield)](https://circleci.com/gh/dreamingechoes/retrospectivex)
[![Ebert](https://ebertapp.io/github/dreamingechoes/retrospectivex.svg)](https://ebertapp.io/github/dreamingechoes/retrospectivex)

:warning: **Work in progress** :warning:

Phoenix application to create retrospective boards.

There's an example administrator in the seeds to use for testing purposes:

- **email**: example@example.com
- **password**: 123456

## Setup development environment with Docker

This project is Docker friendly from day one. To start working on it:

* Setup the web container with `docker-compose build web`.
* Install dependencies with `docker-compose run web mix deps.get`.
* Create your database with `docker-compose run web mix ecto.create`.
* Migrate your database with `docker-compose run web mix ecto.migrate`.
* Run seeds for default data with `docker-compose run web mix run priv/repo/seeds.exs`.
* Install Node.js dependencies with `docker-compose run web bash -c "cd assets; npm install"`.
* Start the application with `docker-compose up`

## Setup testing environment with Docker

This step assumes you already followed instructions from previous paragraph.

* Create your testing database with `docker-compose run web env MIX_ENV=test mix ecto.create`.
* Migrate your testing database with `docker-compose run web env MIX_ENV=test mix ecto.migrate`.
* Run the test suite with `docker-compose run web env MIX_ENV=test mix test`.
* Run the test suite with coverage report on `cover` folder with: `docker-compose run web env MIX_ENV=test mix coveralls.html`.

----------------------------

This project was developed by [dreamingechoes](https://github.com/dreamingechoes).
It adheres to its [code of conduct](https://github.com/dreamingechoes/base/blob/master/files/CODE_OF_CONDUCT.md) and
[contributing guidelines](https://github.com/dreamingechoes/base/blob/master/files/CONTRIBUTING.md), and uses an equivalent [license](https://github.com/dreamingechoes/base/blob/master/files/LICENSE).
