---
title:  Timeline
layout: default
---

General timeline
========

The project can be broken down into two main phases or outcomes - the first is
to refactor the module system, and the second is to integrate with Composer. The
current (very rough) planned timeline is:

* **7th - 21st May** Project and API planning, and discussion on how the system
  should be implemented.
* **21st May** GSOC starts.
* **21st May - 9th July** Refactoring the module system.
* **9th July** Midterm evaluations.
* **9th July - 13th August** Integration with Composer.
* **13th August** GSOC finishes.

This will be expanded on as GSOC approaches.

### May 21 - May 28

**Planned**

* Autoloading investigation - PSR, manifest only?
* Writing a PHP class parser to work around limitations of first loading all classes, as well as being able to generate more specific data to SS

**Completed**

* Initial class parser implementation (https://gist.github.com/2818026)
* Initial proof of concept composer installer (https://github.com/ajshort/silverstripe-composer-installer)

### May 28 - June 4

**Planned**

* Mailing list post for community input on whether interim composer support is desired
* Will be putting together test examples of class parser to demonstrate fringe cases
* Application / Module structure development
** https://gist.github.com/dc9b7db44d1fac52fd8b
* Clarify module project relationship (vikas' other module website project)

**Completed**

* Mailing list post at https://groups.google.com/group/silverstripe-dev/browse_thread/thread/dd629a5aab12d796
* Test examples pending
* Discussion has taken place with Vikas, appears to be headed in the correct direction


### June 4 - June 21

**Planned**

* Minimal updates; exam period 


** Completed

* Work to bring the module and application structure into sapphire core
* https://github.com/ajshort/sapphire/commit/198944452172a0e24494cae59be0d6a5f8b39c05
* https://github.com/ajshort/sapphire/commit/6b6b5d796189d96e09be6108596abc6a2a2a82d2
* https://github.com/ajshort/sapphire/commit/f0d22888b167edf95cfa68dd005d02a3eeb65cdb
* https://github.com/ajshort/sapphire/commit/6c93d10a3081677ae04cd15c87199c6b26057a46
* https://github.com/ajshort/sapphire/commit/eef5c8fb1c89ee9cb4dbd57eb4c7d4a4ae016e30
* https://github.com/ajshort/sapphire/commit/c342eeff36c6f41117cc9b318eb663d2f908495b
* https://github.com/ajshort/sapphire/commit/1f5eb960f05550fc5e470c4e2961862a5f482d2b
* https://github.com/ajshort/sapphire/commit/7f74642b180843e94c96b702b69b84710a0dfe8d
* https://github.com/ajshort/sapphire/commit/33a08d48cbc760f228b0c3d21a471fdf4e3a7c09


### June 25 - July 2

** Planned **

* Rewrite config manifest generation to fix some issues 

** Completed **

* https://github.com/ajshort/sapphire/commit/7be7fa8f3c387ded83fdcd41bd466c86154febd9
* https://github.com/ajshort/sapphire/commit/d00f6c8b0622c641920562943282a97ee46f7eb5


