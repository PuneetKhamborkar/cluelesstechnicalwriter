---
layout: single
title: Markup Language Comparison
permalink: /InfoDev-Uni/markup-comparison/
toc: true
sidebar: InfoDev_Uni
---

This document compares **HTML**, **Markdown**, **Asciidoc**, and **ReStructuredText (ReST)** syntax for common elements. Each language has its strengths and typical use cases; choose the one that fits your tooling and audience.

- **HTML** is the standard markup for web pages; verbose but highly expressive.
- **Markdown** is lightweight and easy to read in plain text, popular on GitHub and many CMSs.
- **Asciidoc** offers more features than Markdown (tables, footnotes, includes) and is used for technical documentation.
- **ReST** is used by Python projects and Sphinx; it provides rich directives and is extensible.

## Syntax Comparison Table

![Comparison Table of Markup Languages](/assets/images/Comparison_of_documentation_syntax_elements.png)

## Block Elements

All four syntaxes support paragraphs separated by blank lines. HTML requires <p> tags, whereas the others do not.

## Footnotes and References

- **Markdown:** limited support, often using extensions (e.g., [^1]).
- **Asciidoc:** built-in footnotes using footnote:[text].
- **ReST:** uses [1]_ notation with a corresponding footnote definition.

## Pros &amp; Cons

- **HTML:** powerful but not human-friendly to write manually.
- **Markdown:** easy for authors, but lacks advanced features without extensions.
- **Asciidoc:** a good balance for technical docs, with built-in features and conversion to multiple formats.
- **ReST:** excellent for documentation with Sphinx; learning curve steeper.

Feel free to extend this document with additional examples, directives, or language-specific idioms.

