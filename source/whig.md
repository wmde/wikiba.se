---
layout: default
title: What have I got?
nav_name: whig

---
## Wikibase components in Docker

### Docker

The Wikibase installation assumes you are fairly familiar with Docker. If you need a little more information, check out Docker's own [quick start](https://docs.docker.com/get-started/) and their [overview of docker-compose](https://docs.docker.com/compose/).

Although you shouldn't need it for most typical Wikibase activity, here's one very useful command that allows you to connect to a running instance inside docker:

```
docker exec -it <instance name> bash
```

### Under the hood

The Wikibase Docker install provides a MediaWiki instance with the Wikibase extension, the SPARQL query service frontend and backend, a query proxy and an instance of QuickStatements. Details on all of these can be found on the [wikibase-docker](https://github.com/wmde/wikibase-docker) GitHub repository.

https://github.com/wikimedia/mediawiki-extensions-Wikibase/tree/master/docs


### Wikibase

The Wikibase machine contains a running instance of [MediaWiki](https://www.mediawiki.org/wiki/MediaWiki) with the Wikibase extension.


### Other helpful resources

- [Learning Wikibase](http://learningwikibase.com/)
- [Wikidata Query Service Tutorial](http://wikidata.wwwnlsrc4.supercp.com/)
