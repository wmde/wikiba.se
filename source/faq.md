---
layout: default
title: FAQ
nav_name: faq
---

# Frequently asked questions

### What is the difference between Wikibase and Wikidata?

**[Wikibase](https://wikiba.se)** is the suite of knowledge base software for managing linked open data, originally written for and still used by the Wikidata project. 

**[Wikidata](https://www.wikidata.org)** is the largest instance of Wikibase, a free knowledge base that anyone can edit. Its data is used by Wikipedia, by its sister projects and by anyone else who wants to make use of a large amount of open general-purpose data.

### Where can I find the source code?
Here's our [github mirror](https://github.com/wikimedia/mediawiki-extensions-Wikibase). 

If you're interested in contributing code, check out our [programmer's guide](https://www.mediawiki.org/wiki/Wikibase/Programmer%27s_guide_to_Wikibase), after which you can [request a developer account](https://www.mediawiki.org/wiki/Developer_account).

### How can I set up my own Wikibase instance?
Use our quick and easy [setup with Docker]({{site.url}}/install). Or take a look at our [Docker repository](https://github.com/wmde/wikibase-docker), or the containers themselves over on [Docker hub](https://hub.docker.com/r/wikibase/).

### Where can I report issues or problems with Wikibase?
You're welcome to raise an issue on our [phabricator instance](https://phabricator.wikimedia.org/project/profile/3363/), where you can log in with your [Wikimedia unified account](https://meta.wikimedia.org/wiki/Help:Unified_login) or a Wikitech [developer account](https://www.mediawiki.org/wiki/Developer_account). 

Before you do, you may want to review the [bug report guidelines](https://www.mediawiki.org/wiki/How_to_report_a_bug).

### Is there a list of Wikibase instances?
On our [User base]({{site.url}}/userbase) page we highlight several notable instances, but for more comprehensive information you can check out the [voluntary Wikibase registry](http://wikibase-registry.wmflabs.org/wiki/Main_Page), the list of [federated query endpoints](https://www.mediawiki.org/wiki/Wikidata_Query_Service/User_Manual/SPARQL_Federation_endpoints) and the [user group](https://meta.wikimedia.org/wiki/Wikibase_Community_User_Group/Reports/2018). 


### Where can I find more info about the query service?

Here's Wikidata's [query service manual](https://www.mediawiki.org/wiki/Wikidata_Query_Service/User_Manual) and some [SPARQL examples](https://www.wikidata.org/wiki/Wikidata:SPARQL_query_service/queries/examples).

### How do federated queries work?

Wikibase supports [SPARQL's federated querying](https://www.w3.org/TR/sparql11-federated-query/) against these [endpoints](https://www.mediawiki.org/wiki/Wikidata_Query_Service/User_Manual/SPARQL_Federation_endpoints). 

There's also an interesting [blog post](https://addshore.com/2018/04/wikibase-of-wikibases/) that demonstrates some federated querying in the context of the Wikibase registry.

### How can I get data into Wikibase?

First, definitely make [QuickStatements](https://www.wikidata.org/wiki/Help:QuickStatements) your friend. There is also the Python-based [Wikidata integrator](https://github.com/SuLab/WikidataIntegrator), which is (as you might imagine) Wikidata-focused but can of course be used with any Wikibase instance.


