---
layout: default
title: Extending Wikibase
nav_name: extend

---


## Extending Wikibase

* [Templates]({{site.url}}/extend#templates)
* [Extensions]({{site.url}}/extend#extensions)
* [Gadgets]({{site.url}}/extend#gadgets)
* [Other additions]({{site.url}}/extend#other-additions)

Wikibase is a powerful and extensible piece of software, and a large amount of what it can do lies beyond the fairly stripped-down state Wikibase is in when you run your Docker images for the first time. 

On this page you can take a quick, link-heavy tour of the resources available to help you extend your instance and give it the functionality you want and need it to have.

### Templates

[MediaWiki templates](https://www.mediawiki.org/wiki/Help:Templates) work a bit like text macros in that they contain content meant to be [transcluded](https://www.mediawiki.org/wiki/Transclusion) into other wiki pages. But their functionality can extend far beyond simple text replacement when scripting comes into play (see [Lua]({{site.url}}/extend#Lua) below).

To view the templates installed on your (or any) instance, navigate to `<your Wikibase URL>/wiki/Special:AllPages?from=&to=&namespace=10`.

While there is no single repository for MediaWiki templates, Wikipedia does offer a robust [template resource page](https://en.wikipedia.org/wiki/Wikipedia:Template_index), and they are easily turned up in web searches and by looking through what's installed on any given instance of MediaWiki. When you find a template you want to use, follow [these instructions](https://www.mediawiki.org/wiki/Help:Templates#Copying_from_one_wiki_to_another) to start using it on your instance.

A few templates that Wikibase users often find useful:

* [SPARQL](http://wikidata.org/wiki/Template:SPARQL): SPARQL query syntax highlighting
* [Q](https://www.wikidata.org/wiki/Template:Q): creates a direct link to an item
* [Property](https://www.wikidata.org/wiki/Template:Property): displays a localized label for a property

You can also check out this helpful third-party overview of templates: [ryadel.com](https://www.ryadel.com/en/how-to-add-wikipedia-mbox-templates-to-your-own-mediawiki/)

#### Lua 

Templates can call modules written in the [Lua](https://www.mediawiki.org/wiki/Extension:Wikibase_Client/Lua) scripting language, making them more powerful. Check out the [tutorial](https://www.mediawiki.org/wiki/Lua/Tutorial) and see the [scripting language section](#scripting) below.


### Extensions

The wide variety of [extensions](https://www.mediawiki.org/wiki/Manual:Extensions) that modify how your installation looks and works actually includes Wikibase itself, but there are many others that Wikibase users often install depending on their instance's needs.

You can browse and download many extensions with the MediaWiki [ExtensionDistributor](https://www.mediawiki.org/wiki/Special:ExtensionDistributor).

[These install instructions](https://www.mediawiki.org/wiki/Manual:Extensions#Installing_an_extension) should cover most cases, but some extensions have special instructions called out separately below.

To view the extensions you currently have installed, navigate to `<your Wikibase URL>/wiki/Special:Version#mw-version-ext`.

Note that the following list doesn't include extensions meant for importing data into Wikibase, several options for which are covered in some detail over at [Importing data]({{site.url}}/import).

#### General utility

* [Advanced Search](https://www.mediawiki.org/wiki/Extension:AdvancedSearch): expands the search form with many additional options
* [Visual Editor](https://www.mediawiki.org/wiki/Extension:VisualEditor): offers an optional rich-text editor (see also the [project page](https://www.mediawiki.org/wiki/VisualEditor))

#### Scripting

* [Scribunto](https://www.mediawiki.org/wiki/Extension:Scribunto): enables the embedding of scripting languages into MediaWiki, currently only [Lua](https://www.mediawiki.org/wiki/Lua_scripting). This enables, among other powerful applications for scripting, the use of Lua modules in templates ([see above](#Lua)).
 * [Lua tutorial for MW/Scribunto](https://www.mediawiki.org/wiki/Extension:Scribunto/Lua_reference_manual)
 * [Differences from standard Lua](https://www.mediawiki.org/wiki/Extension:Scribunto/Lua_reference_manual#Differences_from_standard_Lua)

#### Content management and spam protection

* [Abuse Filter](https://www.mediawiki.org/wiki/Extension:AbuseFilter): create filters for editing to forestall abusive activity
* [Nuke](https://www.mediawiki.org/wiki/Extension:Nuke): enable mass deletion of pages
* [Confirm Edit](https://www.mediawiki.org/wiki/Extension:ConfirmEdit): add CAPTCHA checks before an edit is confirmed
* [Tor Block](https://www.mediawiki.org/wiki/Extension:TorBlock): restrict access for Tor exit nodes

#### Wikibase-specific

* [OAuth](https://www.mediawiki.org/wiki/Extension:OAuth): implements [OAuth](https://oauth.net/), required for some tools to work correctly with Wikibase
 * [Detailed reference for Lua in MW/Scribunto](https://www.mediawiki.org/wiki/Extension:Wikibase_Client/Lua)
* [CLDR](https://www.mediawiki.org/wiki/Extension:CLDR): contains and manages locale-specific information regarding the display of data in different languages and formats
* [Universal Language Selector](https://www.mediawiki.org/wiki/Extension:UniversalLanguageSelector): allows users to configure an interface language of their choice
* [Property Suggester](https://www.mediawiki.org/wiki/Extension:PropertySuggester): adds useful auto-suggestion of properties for manual edits

#### Data quality and constraints

You can manage the quality of your Wikibase data by imposing constraints (which are actually more like guidelines).

[Wikibase Quality Constraints](https://www.mediawiki.org/wiki/Extension:WikibaseQualityConstraints) ([install](https://github.com/wikimedia/mediawiki-extensions-WikibaseQualityConstraints)) is a powerful extension that helps you impose constraints on your data. 

See also the [constraints portal](https://www.wikidata.org/wiki/Help:Property_constraints_portal) which offers many constraints-oriented resources and tips on how to implement them effectively.

#### Last but not least

The [Gadgets](https://www.mediawiki.org/wiki/Extension:Gadgets) extension enables the use of gadgets (see below). You may well find that this extension is already installed on your instance, but [make sure](#Extensions): it needs to be installed and enabled before implementing anything listed in the next section!

### Gadgets

Gadgets are small, optional-per-user interface modifications. Some examples can be found in the [MediaWiki gadget list](https://www.mediawiki.org/wiki/Extension:Gadgets#List_of_gadget_scripts) and [Wikidata's installed gadgets](https://www.wikidata.org/wiki/Special:Gadgets)

Here's a guide to [writing your own](https://www.mediawiki.org/wiki/Gadget_kitchen), and here's how to [install a gadget](https://www.mediawiki.org/wiki/Extension:Gadgets#Installation).

### Other additions

As if templates, extensions and gadgets weren't enough, there are many other ways you can customize your Wikibase installation. Here are some of the most commonly used. 

#### Interface messages

As an administrator (with [editInterface](https://www.mediawiki.org/wiki/Editinterface) permissions), you can customize the messages displayed to the user by Wikibase. A complete list of them can be found on the **Special:AllMessages** page of your instance: `<your instance URL>/wiki/Special:AllMessages`

Consult the [System message](https://www.mediawiki.org/wiki/Help:System_message) documentation for more information.

#### Sitelinks

[Sitelinks](https://www.wikidata.org/wiki/Help:Sitelinks) allow Wikibase's MediaWiki interface to link to other wikis in a more useful way than a simple hyperlink. A good example is the language selector on Wikipedia pages; it relies on sitelinks established to wikis in other languages.

Although the Docker images handle most of the config changes shown in the [Wikibase install documentation](https://www.mediawiki.org/wiki/Wikibase/Installation), sitelinks are a notable exception. 

To get sitelinks working, first work through the [sitelinks section of the install doc](https://www.mediawiki.org/wiki/Wikibase/Installation#Enable_Sitelinks). Then consult the [sites table](https://www.mediawiki.org/wiki/Help:System_message) for further guidance.

#### Sorted properties/statements

Wikibase's content displays in the order in which it was added to the database. To change the default order, you'll need to use a sorted properties list.

Learn more about it on the [Sorted Properties](https://www.mediawiki.org/wiki/Manual:Interface/Wikibase-SortedProperties) page, and check out [Wikidata's own Sorted Properties](https://www.wikidata.org/w/index.php?title=MediaWiki:Wikibase-SortedProperties) for inspiration.

#### Pywikibot

For more advanced users who seek tools to help them manage their data, there's [Pywikibot](https://www.mediawiki.org/wiki/Manual:Pywikibot). It started life as a tool made for Wikipedia but was adapted to work on other Wikimedia projects, including Wikibase installations. Pywikibot amounts to a [collection of scripts](https://www.mediawiki.org/wiki/Manual:Pywikibot/Scripts) that can change and manipulate data programmatically, potentially saving large amounts of manual work.

Check out the [third-party wiki quick start](https://www.mediawiki.org/wiki/Manual:Pywikibot/Third-party_Wiki_Quick_Start) for Pywikibot to see if it might be right for your installation.

