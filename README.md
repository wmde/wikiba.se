# Wikiba.se website

This repo contains the resources of the [wikiba.se website](https://wikiba.se).

[![Build Status](https://travis-ci.org/wmde/wikiba.se.svg?branch=master)](https://travis-ci.org/wmde/wikiba.se)

## Prerequisites

- [PHP](https://www.php.net/manual/en/install.php) with the [php-xml](https://stackoverflow.com/questions/38793676/php-xml-extension-not-installed) extension installed
- [Composer](https://getcomposer.org/doc/00-intro.md)

## Installation
Run the install command:

    composer install

This will install all dependencies, including [Sculpin](https://sculpin.io/).

## Site generation

For development and testing:

    composer dev

For deployment to production:

    composer build

You can also run Sculpin in a docker container:

    docker run --rm -it -p 8000:8000 -v "/$PWD://app" php:latest sh -c "cd //app; vendor/bin/sculpin help"

## Running the tests

Change into the root directory of the project and run

    composer test
