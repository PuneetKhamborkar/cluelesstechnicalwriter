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

| Element            | HTML                            | Markdown                 | Asciidoc                          | ReST                               |
|--------------------|---------------------------------|--------------------------|-----------------------------------|------------------------------------|
| Heading level 1    | <h1>Title</h1>                | # Title                | = Title =                       | Title\n=====                    |
| Heading level 2    | <h2>Sub</h2>                  | ## Sub                 | == Sub ==                       | Sub\n----                        |
| Bold               | <strong>text</strong>         | **text**               | *text*                          | **text**                         |
| Italic             | <em>text</em>                 | *text*                 | _text_                          | *text*                           |
| Link               | <a href= url>link</a>      | [link](url)            | link:url[]                      | `link <url>`__                  |
| Image              | <img src=img alt=alt> | ![alt](img)            | image::img[alt]                 | `.. image:: img\n    :alt: alt`  |
| Unordered list     | <ul><li>item</li></ul>        | - item                 | * item                          | - item                           |
| Ordered list       | <ol><li>one</li></ol>         | 1. one                 | . one                           | 1. one                           |
| Nested list        | see HTML nesting                | - outer\n  - inner    | * outer\n** inner             | - outer\n  - inner              |
| Blockquote         | <blockquote>quote</blockquote>| > quote                | ____\nquote\n____            | > quote                          |
| Code block         | <pre><code>code</code></pre>  | <code>`code`</code>  | ``\ncode\n``             | ``\ncode\n``             |
| Inline code        | <code>code</code>             | ` code `             | ` code `                      | ` code `                      |
| Table              | <table>...</table>            | pipe-delimited           | pipe-delimited                    | grid or simple table syntax       |

## Example Table in Markdown

`
| Name  | Age |
|-------|-----|
| Alice | 30  |
` 

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

