---
layout: default
title: Extending Wikibase
nav_name: extend

---
## Extending Wikibase

Wikibase is a powerful and extensible piece of software, and the state you find it in when you've just launched your Docker images is almost certainly not the state you'll want it in when you're finished setting it up.

### Know your local settings

You can add any number of extensions, templates and gadgets, and they vary widely both in popularity and in ease of installation. To use many of these add-ons, you'll need to make changes to the [LocalSettings.php](https://www.mediawiki.org/wiki/Manual:LocalSettings.php) file on your MediaWiki/Wikibase Docker instance (`docker_wikibase_1`, probably). 

Although this manual isn't meant to replace a grounding in Docker, the following commands may help you get at and edit this very important file:

#### Copy the file to your local directory
```
docker cp docker_wikibase_1:/var/www/html/LocalSettings.php LocalSettings.php
```
#### After editing the file on your local computer, copy it back
```
docker cp LocalSettings.php docker_wikibase_1:/var/www/html/LocalSettings.php 
```




### Configuration changes

Although the Docker images handle most of the config changes shown in the [Wikibase install documentation](https://www.mediawiki.org/wiki/Wikibase/Installation), you're probably still going to make some edits to LocalSettings.php, whether it's to enable and configure sitelinks or to add 

#### Sitelinks

[Sitelinks](https://www.wikidata.org/wiki/Help:Sitelinks) are a common addition to Wikibase. They allow the site to link to other Mediawiki sites 

https://www.mediawiki.org/wiki/Wikibase/Installation#Enable_Sitelinks

https://www.mediawiki.org/wiki/Manual:Sites_table


#### Sorted properties

https://www.mediawiki.org/wiki/Manual:Interface/Wikibase-SortedProperties

### Templates

https://www.mediawiki.org/wiki/Help:Templates

To view already installed templates, Special:AllPages?from=&to=&namespace=10

https://www.ryadel.com/en/how-to-add-wikipedia-mbox-templates-to-your-own-mediawiki/


### Extensions

https://www.mediawiki.org/wiki/Manual:Extensions

https://www.mediawiki.org/wiki/Manual:Extensions#Installing_an_extension

View installed: /wiki/Special:Version#mw-version-ext

#### Spam protection and management
https://www.mediawiki.org/wiki/Extension:Nuke
https://www.mediawiki.org/wiki/Extension:ConfirmEdit
https://www.mediawiki.org/wiki/Extension:TorBlock 


https://www.mediawiki.org/wiki/Extension:AdvancedSearch

#### Wikibase-specific

https://www.mediawiki.org/wiki/Extension:Scribunto
https://www.mediawiki.org/wiki/Extension:CLDR 
https://www.mediawiki.org/wiki/Extension:OAuth (needed for some tools)
https://www.mediawiki.org/wiki/Extension:UniversalLanguageSelector 

https://www.mediawiki.org/wiki/Extension:Gadgets

### Gadgets

Gadgets are
