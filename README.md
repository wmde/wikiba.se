# Wikiba.se website

This repo contains the resources of the [wikiba.se website](https://wikiba.se).

[![Build Status](https://travis-ci.org/wmde/wikiba.se.svg?branch=master)](https://travis-ci.org/wmde/wikiba.se)

## Installation

Run the install command:

    composer install

## Site generation

For development:

    vendor/bin/sculpin generate --watch --server

For deployment:

    vendor/bin/sculpin generate --env=prod

You can also run sculpin in a docker container:

    docker run --rm -it -p 8000:8000 -v "/$PWD://app" php:latest sh -c "cd //app; vendor/bin/sculpin help"

## Running the tests

Change into the root directory of the project and run

    phpunit
