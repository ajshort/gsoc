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