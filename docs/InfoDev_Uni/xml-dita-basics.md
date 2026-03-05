---
layout: single
title: XML & DITA Basics
permalink: /InfoDev-Uni/xml-dita-basics/
---

# Using XML and DITA

The simplest XML document looks like this:

```xml
<?xml version="1.0"?>
<note>
  <to>User</to>
  <from>Acme</from>
  <heading>Reminder</heading>
  <body>Don't forget to check the docs!</body>
</note>
```

DITA is an application of XML for technical content. A minimal topic example:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE topic PUBLIC "-//OASIS//DTD DITA Topic//EN" "topic.dtd">
<topic id="example">
  <title>Example Topic</title>
  <body>
    <p>This is a simple DITA topic.</p>
  </body>
</topic>
```

To author with DITA, write XML documents using the DITA DTD or schema and assemble them into maps for publication.
