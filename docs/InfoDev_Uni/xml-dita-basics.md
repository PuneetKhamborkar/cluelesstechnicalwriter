---
layout: single
title: XML & DITA Basics
permalink: /InfoDev-Uni/xml-dita-basics/
---

# Using XML and DITA

XML (eXtensible Markup Language) is a general-purpose markup language that uses angle-bracket syntax to represent hierarchical data. DITA (Darwin Information Typing Architecture) is an XML application designed specifically for technical documentation.

## Basic XML Example

The simplest XML document looks like this:

`xml
<?xml version= 1.0?>
<note>
  <to>User</to>
  <from>Acme</from>
  <heading>Reminder</heading>
  <body>Don't forget to check the docs!</body>
</note>
`

Each element must be closed, and nesting must be well-formed. XML documents may include attributes, namespaces, and a DOCTYPE declaration when validating against a DTD.

## DITA Topic Example

DITA is an application of XML for technical content. A minimal topic example:

`xml
<?xml version=1.0 encoding=UTF-8?>
<!DOCTYPE topic PUBLIC -//OASIS//DTD DITA Topic//EN topic.dtd>
<topic id=example>
  <title>Example Topic</title>
  <body>
    <p>This is a simple DITA topic.</p>
  </body>
</topic>
`

### Common DITA Elements
- <title>: the title of the topic.
- <body>: contains the content, typically <p>, <section>, <task>, or <concept>.
- <section>: a logical subsection within the body.

## DITA Maps
A DITA map (<code>.ditamap</code>) assembles topics into a publication. Example:

`xml
<map>
  <title>Manual</title>
  <topicref href=intro.dita/>
  <topicref href=usage.dita/>
</map>
`

Maps control navigation and can include metadata, branches, and conditional processing attributes.

## Working with DITA
1. Write individual topic files using a text editor or a DITA-aware application such as oXygen XML Editor.
2. Create a map file that references those topics.
3. Use an output processor (e.g., DITA-OT) to transform the map into HTML, PDF, or other formats.

## Advanced Features
- **Conref** (content reference): reuse chunks of content across topics.
- **Keyrefs**: reference topics or images by key.
- **Conditional processing**: include or exclude content based on attributes like udience or product.

## Tools and Workflow
- **DITA Open Toolkit (DITA-OT)**: open-source processor for publishing.
- **Authoring tools**: oXygen, XMetaL, Arbortext.
- **Version control**: treat DITA files like any other text files in Git.

## Best Practices
- Keep topics short and focused (one main idea per topic).
- Use meaningful IDs and filenames.
- Leverage reuse mechanisms to avoid duplication.
- Validate your XML against the DITA DTD or schema regularly.

By following these basics, you can start authoring structured technical documentation that scales across products and audiences.

