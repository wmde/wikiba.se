---
layout: default
title: Federation
nav_name: fed

---
## Federation 

There's a lot of excitement around the concept of federation in Wikibase, but "federation" means different things to different people. Below we lay out the different meanings of the term and show you what's currently available.

### Federated querying

The [federated query](https://www.w3.org/TR/sparql11-federated-query/) is a property of SPARQL that allows your search to include multiple endpoints.

Federated SPARQL querying works in Wikibase. You can see a partial, example list of federation endpoints used by Wikidata [here](https://www.mediawiki.org/wiki/Wikidata_Query_Service/User_Manual/SPARQL_Federation_endpoints). 

The [Wikibase registry](https://wikibase-registry.wmflabs.org/wiki/Main_Page) also has some useful information, including some ideas for conventions that would facilitate federated querying, such as the [same-as](https://wikibase-registry.wmflabs.org/wiki/Item:Q54) property.

Finally, there's an interesting [blog post](https://addshore.com/2018/04/wikibase-of-wikibases/) that demonstrates some federated querying in the context of the Wikibase registry.

### Federation and Wikidata

Instead of creating a set of [properties](https://www.mediawiki.org/wiki/Wikibase/DataModel/Primer) from scratch on a new instance of Wikibase, it will eventually be possible to configure a new Wikibase instance to obtain a robust, living and constantly updated property set from [Wikidata](https://www.wikidata.org/).

You can read more about this feature and its development in this [preliminary document](https://doc.wikimedia.org/Wikibase/master/php/md_docs_components_repo-federated-properties.html) and its [Phabricator project](https://phabricator.wikimedia.org/project/view/4604/).

#### What it's not

Federating with Wikidata's properties doesn't amount to mirroring Wikidata. Though [some want to do just that](http://wiki.bitplan.com/index.php/Get_your_own_copy_of_WikiData) in order to overcome rate limits, and [dumps are produced regularly](https://dumps.wikimedia.org/wikidatawiki/), such an endeavor is by no means an easy task and likely won't accomplish what you're aiming for.

### Two-way federation

Two-way federation of data between Wikibase instances is not yet implemented and probably a long way off. The aforementioned Federated Properties project is the first step of a longer journey in this direction.

