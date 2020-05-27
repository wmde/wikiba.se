---
layout: default
title: What have I got?
nav_name: whig

---
## Wikibase components in Docker

### Before we get started

The Wikibase installation assumes you are fairly familiar with Docker. If you need a little more information, check out Docker's own [quick start](https://docs.docker.com/get-started/) and their [overview of docker-compose](https://docs.docker.com/compose/).

Although you shouldn't need it for most typical Wikibase activity, here's one very useful command that allows you to connect to a running instance inside docker:

```
docker exec -it <instance name> bash
```

### Under the hood

https://github.com/wikimedia/mediawiki-extensions-Wikibase/tree/master/docs

Now that you've completed the [install](install), if you run `docker-compose ps` you should see something like this:

```
          Name                        Command               State          Ports        
----------------------------------------------------------------------------------------
docker_elasticsearch_1     /usr/local/bin/docker-entr ...   Up      9200/tcp, 9300/tcp  
docker_mysql_1             docker-entrypoint.sh mysqld      Up      3306/tcp            
docker_quickstatements_1   /bin/bash /entrypoint.sh         Up      0.0.0.0:9191->80/tcp
docker_wdqs-frontend_1     /entrypoint.sh nginx -g da ...   Up      0.0.0.0:8282->80/tcp
docker_wdqs-proxy_1        /bin/sh -c "/entrypoint.sh"      Up      0.0.0.0:8989->80/tcp
docker_wdqs-updater_1      /entrypoint.sh /runUpdate.sh     Up                          
docker_wdqs_1              /entrypoint.sh /runBlazegr ...   Up      9999/tcp            
docker_wikibase_1          /bin/bash /entrypoint.sh         Up      0.0.0.0:8181->80/tcp
```

### Wikibase

The Wikibase machine contains a running instance of [MediaWiki](https://www.mediawiki.org/wiki/MediaWiki) with the Wikibase extension.


### Other helpful resources

- [Learning Wikibase](http://learningwikibase.com/)
- [Wikidata Query Service Tutorial](http://wikidata.wwwnlsrc4.supercp.com/)
