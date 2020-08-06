---
layout: default
title: Importing data
nav_name: import

---
## Importing data into Wikibase

* [QuickStatements]({{site.url}}/import#quickstatements)
* [WikibaseImport]({{site.url}}/import#wikibaseimport)
* [WikibaseIntegrator]({{site.url}}/import#wikibaseintegrator)
* [OpenRefine]({{site.url}}/import#openrefine)

Perhaps the greatest challenge of a clean, empty database is that of properly filling it up with what you want to put in it.  Wikibase is no exception; this section covers the most common and useful tools for getting data into Wikibase.

### [QuickStatements](https://www.wikidata.org/wiki/Help:QuickStatements)

QuickStatements is the useful import tool you'll find already running in your Docker setup. It's more than an import tool; it can be used to edit and modify data. You can find the easy-to-use QuickStatements interface on your Wikibase instance by navigating to `<your Wikibase url>/tools/quickstatements`.

The essential help document linked above is packed with useful information far too intricate to be summarized here, but it's worth noting that [OpenRefine](https://www.wikidata.org/wiki/Wikidata:Tools/OpenRefine) data ([see below]({{site.url}}/import#OpenRefine)) can be exported to QuickStatements format.

### [WikibaseImport](https://github.com/Wikidata/WikibaseImport)

WikibaseImport is a MediaWiki [extension]({{site.url}}/extend#Extensions) and a flexible, powerful command-line tool that allows you to import into Wikibase using exports of data from other Wikibase instances. It's best for experienced Wikibase users who have a firm grasp of Wikibase's [data architecture](https://www.mediawiki.org/wiki/Wikibase/DataModel) and are comfortable using command-line tools on their instance's web server. (See the [maintenance section]({{site.url}}/maint) for more information on working directly with a container)

To install WikibaseImport, follow its [install instructions](https://github.com/Wikidata/WikibaseImport#install). You can also find more information on working with extensions on our [Extending Wikibase]({{site.url}}/extend) page.

### [WikibaseIntegrator](https://github.com/Mystou/WikibaseIntegrator)

Wikibase Integrator, also known as Wikidata Integrator, is a Python tool for creating sophisticated bots that can read from and write to Wikibase. It was developed to improve on [Pywikibot]()'s handling of the MediaWiki API and integrate tightly with the Wikibase SPARQL endpoint.

Read [here](https://www.wikidata.org/wiki/User:ProteinBoxBot) how the developers put WikibaseIntegrator to work.

### [OpenRefine](https://www.wikidata.org/wiki/Wikidata:Tools/OpenRefine)

Originally developed by Google, OpenRefine is now a community-supported data management tool that can handle large bodies of data and wrangle them into a format suitable for importing into Wikidata.

While OpenRefine support for Wikibase users is not yet available, progress on this feature is likely coming in the future. For more information, see this [discussion on adding support for Wikimedia Commons](https://github.com/OpenRefine/OpenRefine/issues/2144).
