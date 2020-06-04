---
layout: default
title: Docker quick start
nav_name: install

---
## Quick start with Docker

### Introduction

We’ve put together a set of machines in Docker that should have you up and running in no time. This configuration starts an empty instance of Wikibase, a MediaWiki front end with query interface, a query backend, ElasticSearch, and a QuickStatements bulk editing service.

### Before you start

- You’ll need to have [docker](https://docs.docker.com/get-started/) and [docker-compose](https://docs.docker.com/compose/install/) installed on the computer where you want to run your Wikibase instance. 
- Together, these Docker machines require at least 4GB of memory. 
    - Check out Docker’s [documentation on resource constraints](https://docs.docker.com/config/containers/resource_constraints/). 

- An empty Wikibase running on Docker requires at minimum 6GB of disk storage.  

### Getting the machine images running

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

### Using your new instance

Once all the services have started, you can begin the exciting process of filling up, extending and customizing your empty instance of Wikibase. Take a look at our [setup resources page]({{site.url}}/setup) to get started.

