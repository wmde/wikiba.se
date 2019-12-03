# Wikiba.se website

This repo contains the resources of the [wikiba.se website](http://wikiba.se).

[![Build Status](https://travis-ci.org/wmde/Wikiba.se.svg?branch=master)](https://travis-ci.org/wmde/Wikiba.se)

<<<<<<< HEAD
## Prerequisites

- [PHP](https://www.php.net/manual/en/install.php) with the [php-xml](https://stackoverflow.com/questions/38793676/php-xml-extension-not-installed) extension installed
- [phpunit](https://phpunit.de/getting-started/phpunit-8.html) (for testing)
- [Composer](https://getcomposer.org/doc/00-intro.md)

=======
>>>>>>> parent of 3422476... spruced up install instructions just a bit
## Installation

Assuming you have the php-xml extension installed in your system, run the install command:

    composer install

## Site generation

For development:

    vendor/bin/sculpin generate --watch --server

For deployment:

    vendor/bin/sculpin generate --env=prod

You can also run Sculpin in a docker container:

    docker run --rm -it -p 8000:8000 -v "/$PWD://app" php:latest sh -c "cd //app; vendor/bin/sculpin help"

## Running the tests

Change into the root directory of the project and run

    phpunit
