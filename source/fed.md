---
layout: default
title: Federation
nav_name: fed

---
## Federation 

There's a lot of excitement around the concept of federation in Wikibase, but "federation" means different things to different people. Below we lay out the different meanings of the term and show you what's currently available.

### Federated querying

[Federated queries](https://www.w3.org/TR/sparql11-federated-query/) is a property of SPARQL that allows your search to include multiple endpoints.

Federated SPARQL querying works in Wikibase. You can see a partial, example list of federation endpoints used by Wikidata [here](https://www.mediawiki.org/wiki/Wikidata_Query_Service/User_Manual/SPARQL_Federation_endpoints). 

The [Wikibase registry](https://wikibase-registry.wmflabs.org/wiki/Main_Page) also has some useful information, including some ideas for conventions that would facilitate federated querying, such as the [same-as](https://wikibase-registry.wmflabs.org/wiki/Item:Q54) property.

### Federation and Wikidata

Instead of creating a set of [properties](https://www.mediawiki.org/wiki/Wikibase/DataModel/Primer) from scratch on a new instance of Wikibase, it will soon be possible to configure a new Wikibase instance to obtain a robust, living and constantly updated property set from [Wikidata](https://www.wikidata.org/).

You can read more about this feature and its development in this [preliminary document](https://doc.wikimedia.org/Wikibase/master/php/md_docs_components_repo-federated-properties.html) and its [Phabricator project](https://phabricator.wikimedia.org/project/view/4604/).

### Two-way federation

Two-way federation of data between Wikibase instances is not yet implemented and probably a long way off. The aforementioned Federated Properties project is a first step toward this functionality.

