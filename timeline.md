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
  * https://gist.github.com/dc9b7db44d1fac52fd8b
* Clarify module project

**Completed**


