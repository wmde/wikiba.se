---
layout: default
title: Importing data
nav_name: import

---
## Importing data into Wikibase

Perhaps the greatest challenge of a clean, empty database is that of properly filling it up with what you want to put in it.  Wikibase is no exception; this section covers the most common and useful tools for getting data into Wikibase.

### QuickStatements

[QuickStatements](https://www.wikidata.org/wiki/Help:QuickStatements) is the tool you'll find already running in your Docker setup. It's more than an import tool; it can be used to edit and modify data. It also has a fairly snazzy interface, which you'll find on your Wikibase instance under `<your Wikibase url>/tools/quickstatements`.

The essential help document linked above is packed with useful information far too intricate to be summarized here, but it's worth noting that [OpenRefine](https://www.wikidata.org/wiki/Wikidata:Tools/OpenRefine) data ([see below]({{site.url}}/import#OpenRefine)) can be exported to QuickStatements format.

### WikibaseImport

[WikibaseImport](https://github.com/filbertkm/WikibaseImport) is a MediaWiki [extension](extend) and flexible, powerful command-line tool that allows you to import into Wikibase using exports of data from other Wikibase instances. It's best for seasoned Wikibase users who have a firm grasp of Wikibase's [data architecture](https://www.mediawiki.org/wiki/Wikibase/DataModel) and are comfortable using command-line tools on their instance's web server.

To install WikibaseImport, follow its [install instructions](https://github.com/filbertkm/WikibaseImport#install). You can also find more information on working with extensions on our [Extending Wikibase]({{site.url}}/extend) page.

### Wikibase Integrator

[WikibaseIntegrator](https://github.com/Mystou/WikibaseIntegrator), also known as WikiData Integrator, is a Python tool

### OpenRefine

https://www.wikidata.org/wiki/Wikidata:Tools/OpenRefine

but
https://github.com/OpenRefine/OpenRefine/issues/2144
