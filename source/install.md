---
layout: default
title: Docker quick start
nav_name: install

---
# Quick start with Docker

## Introduction

We’ve put together a set of machines in Docker that should have you up and running in no time. This configuration starts an empty instance of Wikibase, a MediaWiki front end with query interface, a query backend, ElasticSearch, and a QuickStatements bulk editing service.

## Before you start

- You’ll need to have [docker](https://docs.docker.com/get-started/) and [docker-compose](https://docs.docker.com/compose/install/) installed on the computer where you want to run your Wikibase instance. 
- Together, these Docker machines require at least 4GB of memory. 
    - Check out Docker’s [documentation on resource constraints](https://docs.docker.com/config/containers/resource_constraints/). 

- An empty Wikibase running on Docker requires at minimum 6GB of disk storage.  

## Getting the machine images running

1. Download the [docker-compose file](https://raw.githubusercontent.com/wmde/wikibase-docker/master/docker-compose.yml) and place it on the computer where Docker Engine and docker-compose are installed. 
2. In the directory that now contains the `docker-compose.yml` file, run the following to pull the needed Docker machine images:

   `docker-compose pull`

3. Start the machine images in the background: 

   `docker-compose up -d`

   (To view the continuous output, you can run `docker-compose logs -f`)

4. Verify that all the services have started. 
    1. Run `docker-compose ps`. You should see eight images in an “Up” state. 
    2. Check the logs for success or errors -- for example, using this command:

    `docker-compose logs --tail="20" -t`

    3. Try to load the front end and the query interface in your browser (see below). 

## Using your new instance

Once all the services have started, you can begin to explore your empty instance of Wikibase.

- **Visit the front page!** [http://localhost:8181/](http://localhost:8181/)  
  - Don't forget to [change](http://localhost:8181/w/index.php?title=Special:ChangeCredentials/MediaWiki%5CAuth%5CPasswordAuthenticationRequest&returnto=Special%3APreferences) the default username and password: _WikibaseAdmin_ / _WikibaseDockerAdminPass_ 
- **Visit the query service!** [http://localhost:8282/](http://localhost:8282/) 
- **Add some data!** Get started here: [https://www.wikidata.org/wiki/Help:QuickStatements](https://www.wikidata.org/wiki/Help:QuickStatements)  

  

## Maintenance
 
### Stop the containers

This command stops the Docker containers, leaving the machines (and of course all data) intact:

`docker-compose stop`

As you might imagine, you can use `docker-compose start` to start them again.

### Delete only the containers

This command removes the containers but preserves all data in MySQL, Mediawiki and the query service in Docker volumes.

`docker-compose down`
 
### Remove the containers and data

WARNING: this will remove ALL of the data you may have added to MediaWiki, Wikibase, the QueryService and ElasticSearch.

`docker-compose down --volumes`

## Reference

Below you'll find much more information on managing your Wikibase install with Docker.
- [README-compose.md](https://github.com/wmde/wikibase-docker/blob/master/README-compose.md) from the [wikibase-docker](https://github.com/wmde/wikibase-docker) repository
- 






