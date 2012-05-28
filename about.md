---
title:  About
layout: default
---

About
=====

The current SilverStripe module system is quite haphazard, with different parts
of the framework responsible for loading things from modules, and procedural
bootstrap code. Goals while reworking this include:

* Proper module priority.
* Full namespace support.
* Ability to have modules in subfolders.
* More consistent way to load resources (classes, css, templates, js?) from modules.
* More to come...

## Possible implementation points

* Refactoring project structures to suit a defined module management system
* Developer API to module management within the framework (eg ModuleManager->listModules())
    * Enable/Disable modules via code (that could eventually have a CMS interface?)
    * Blocks of code that execute
        * When the module is enabled
        * Every request when the module is enabled
        * When the module is de-activated
* Additional metadata on top of the defaults provided by packagist/composer
* Tooling for module authors?
    * to automatically generate module JSON descriptors
    * publishing updates after git commits/tags
