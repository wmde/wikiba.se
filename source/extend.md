---
layout: default
title: Extending Wikibase
nav_name: extend

---


## Extending Wikibase

* [Templates](extend#Templates)
* [Extensions](extend#Extensions)
* [Gadgets](extend#Gadgets)
* [Other additions](extend#Other-additions)

Wikibase is a powerful and extensible piece of software, and the state you find it in when you've just launched your Docker images is almost certainly not the state you'll want it in when you're finished setting it up.

### Templates

[MediaWiki templates](https://www.mediawiki.org/wiki/Help:Templates) work like text macros, replacing defined words marked by `{{ '{{' }} {{ '}}' }}` with longer strings of text. They're powerful and very easy to write.

Some few that Wikibase users find useful:

* [SPARQL](http://wikidata.org/wiki/Template:SPARQL): SPARQL query syntax highlighting
* [Q](https://www.wikidata.org/wiki/Template:Q): creates a direct link to an item
* [Property](https://www.wikidata.org/wiki/Template:Property): displays a localized label for a property

To view the templates installed on your instance, navigate to `<your instance URL>/wiki/Special:AllPages?from=&to=&namespace=10`

You can also check out this helpful third-party overview of templates: [ryadel.com](https://www.ryadel.com/en/how-to-add-wikipedia-mbox-templates-to-your-own-mediawiki/)

#### Lua 

Templates can call modules written in [Lua](https://www.mediawiki.org/wiki/Extension:Wikibase_Client/Lua), making templates even more powerful. Check out the [tutorial](https://www.mediawiki.org/wiki/Lua/Tutorial) and see the [scripting language section](#Scripting>) below.


### Extensions

The wide variety of [extensions](https://www.mediawiki.org/wiki/Manual:Extensions) that modify how your installation looks and works actually includes Wikibase itself, but there are many others that Wikibase users often install depending on their instance's needs.

You can browse and download many extensions with the MediaWiki [ExtensionDistributor](https://www.mediawiki.org/wiki/Special:ExtensionDistributor).

[These install instructions](https://www.mediawiki.org/wiki/Manual:Extensions#Installing_an_extension) should cover most cases, but some extensions have special instructions called out separately below.

To view the extensions you currently have installed, navigate to `<your Wikibase URL>/wiki/Special:Version#mw-version-ext`.

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
* [Wikibase Quality Constraints](https://www.mediawiki.org/wiki/Extension:WikibaseQualityConstraints) ([install](https://github.com/wikimedia/mediawiki-extensions-WikibaseQualityConstraints)): impose constraints on your data. See also the [constraints portal](https://www.wikidata.org/wiki/Help:Property_constraints_portal).
 * [Detailed reference for Lua in MW/Scribunto](https://www.mediawiki.org/wiki/Extension:Wikibase_Client/Lua)
* [CLDR](https://www.mediawiki.org/wiki/Extension:CLDR): 
* [Universal Language Selector](https://www.mediawiki.org/wiki/Extension:UniversalLanguageSelector):
* [Property Suggester](https://www.mediawiki.org/wiki/Extension:PropertySuggester): 

And last but not least:

* [Gadgets](https://www.mediawiki.org/wiki/Extension:Gadgets): enables the use of gadgets (see below). You may well find that this extension is already installed on your instance, but [make sure](#Extensions): it needs to be installed and enabled before implementing anything listed in the next section!

### Gadgets

Gadgets are small, optional-per-user interface modifications. Some examples can be found in the [MediaWiki gadget list](https://www.mediawiki.org/wiki/Extension:Gadgets#List_of_gadget_scripts) and [Wikidata's installed gadgets](https://www.wikidata.org/wiki/Special:Gadgets), and here's a guide to [writing your own](https://www.mediawiki.org/wiki/Gadget_kitchen).

Here's how to [install a gadget](https://www.mediawiki.org/wiki/Extension:Gadgets#Installation).

The following are some popular gadget choices for Wikibase users:

* Merge
* labelLister
* currentDate





### Other additions

As if templates, extensions and gadgets weren't enough, there are many other ways you can customize your Wikibase installation. Here are some of the most common.


#### Interface messages

As an administrator (with [editInterface](https://www.mediawiki.org/wiki/Editinterface) permissions), you can customize the messages displayed to the user by Wikibase. A complete list of them can be found on the **Special:AllMessages** page of your instance: `<your instance URL>/wiki/Special:AllMessages`

Consult the [System message](https://www.mediawiki.org/wiki/Help:System_message) documentation for more information.

#### Sitelinks

Although the Docker images handle most of the config changes shown in the [Wikibase install documentation](https://www.mediawiki.org/wiki/Wikibase/Installation), [sitelinks](https://www.wikidata.org/wiki/Help:Sitelinks) are a notable exception. Setting up sitelinks allows Wikibase to link to other wikis.

First, complete the [sitelinks section of the install doc](https://www.mediawiki.org/wiki/Wikibase/Installation#Enable_Sitelinks). Then consult the [sites table](https://www.mediawiki.org/wiki/Help:System_message) for further guidance.

#### Sorted properties/statements

Wikibase's content displays in the order in which it was added to the database. To change the default order, you'll need to use a sorted properties list.

Learn more about it on the [Sorted Properties](https://www.mediawiki.org/wiki/Manual:Interface/Wikibase-SortedProperties) page, and check out [Wikidata's own Sorted Properties](https://www.wikidata.org/w/index.php?title=MediaWiki:Wikibase-SortedProperties) for inspiration.

### Know your local settings

You can add any number of extensions, templates and gadgets, and they vary widely both in popularity and in ease of installation. To use many of these add-ons, you'll need to make changes to the [LocalSettings.php](https://www.mediawiki.org/wiki/Manual:LocalSettings.php) file on your MediaWiki/Wikibase Docker instance (often `docker_wikibase_1`). 

Although this manual isn't meant to replace a grounding in Docker, the following commands may help you get at and edit this very important file:

#### Copy the file to your local directory
```
docker cp docker_wikibase_1:/var/www/html/LocalSettings.php LocalSettings.php
```
#### After editing the file on your local computer, copy it back
```
docker cp LocalSettings.php docker_wikibase_1:/var/www/html/LocalSettings.php 
```

Read [Adam Shorland's excellent blog post](https://addshore.com/2018/06/customizing-wikibase-config-in-the-docker-compose-example/) for more detail on modifying files on containers,

