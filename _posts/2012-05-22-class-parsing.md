---
title:  Class Parsing
layout: default
---

One of the keystones of the SilverStripe framework is its ability to extract
reflection information about classes, and then use this for various purposes
such as providing permissions, building databases and much more. Rather than
relying on explicit registries for things, SilverStripe will look for classes
that implement interfaces or extend other classes.

As such a very important component of SilverStripe is a utility that parses
each PHP file in the project, and extracts the classes and interfaces within,
as well as information such as which class they extend, interfaces they
implement and more.

As part of my work will involve supporting namespaces, this will need to be
redone. The current implementation has only rudimentary support for namespaces,
and only supports using fully qualified names.

As such my first goal is to write a basic parser that will take a token stream,
and extract fully qualified class, interface and trait names, as well as
information on abstract and final classes, inheritance, and implementations.

This will be quite simple - the parser only needs to recognise subsets of token
arrangements, such as namespace and use declarations, as well as classes,
interfaces and trait declarations. At the moment I'm implementing it as a simple
class that takes a token stream and iterates through each token in a `parse`
method. When a token such as `T_NAMESPACE` or `T_USE` is encountered it jumps
into a private method which parses that declaration and extracts the required
information.

The implementation of this is quite similar to the
[PHP Token Reflection](https://github.com/Andrewsville/PHP-Token-Reflection)
library, which I am using as a guide for implementation. This is a very high
quality library, but is too large for our needs.

Once this is done all information will be fed through a resolve method which
will use the information on which namespaces have been used or aliased

This is much more robust than the existing method, and will help enable first
class namespace support in the SilverStripe Framework. There are a couple of
shortcomings, such as not supporting class_alias, but it will cover the vast
majority of use cases.

	<?php
	class SilverStripe\Framework\Reflection\PhpFileParser {
		
		public function parse($stream); // Main parse loop.
		public function resolve($name); // Resolves a name to a FQN.
		
		private function parseNamespace(); // Parses namespace declarations.
		private function parseUse();       // Parses use declarations.
		private function parseClass();     // Parses class declarations.
		private function parseInterface(); // Parses interface declarations.
		private function parseTrait();     // Parses trait declarations.
		private function parseName();      // Parses partially or fully qualified names.
		
	}

I've also started thinking about how autoloading will work, and how it will
integrate with Composer. This will probably be the next area I work on.
