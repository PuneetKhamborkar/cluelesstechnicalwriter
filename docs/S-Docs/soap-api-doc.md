---
layout: single
title: SOAP API
permalink: /S-Docs/soap-api/
toc: true
sidebar: S-Docs
---

## AcmeTasker SOAP API

The SOAP service uses XML-based messages over HTTP. The WSDL is available at:

```
https://api.acmetasker.com/soap?wsdl
```

## Namespaces

- http://acmetasker.com/soap – primary namespace

## Operations & Examples

### GetTasks

**Request:**
```xml
<soapenv:Envelope xmlns:soapenv=\"http://schemas.xmlsoap.org/soap/envelope/\" xmlns:tsk=\"http://acmetasker.com/soap\">
  <soapenv:Header/>
  <soapenv:Body>
    <tsk:GetTasksRequest>
      <tsk:status>open</tsk:status>
    </tsk:GetTasksRequest>
  </soapenv:Body>
</soapenv:Envelope>
```

**Response:**
```xml
<soapenv:Envelope xmlns:soapenv=\"http://schemas.xmlsoap.org/soap/envelope/\">
  <soapenv:Body>
    <tsk:GetTasksResponse>
      <tsk:Task>
        <tsk:id>1</tsk:id>
        <tsk:title>Example</tsk:title>
      </tsk:Task>
    </tsk:GetTasksResponse>
  </soapenv:Body>
</soapenv:Envelope>
```

### CreateTask

Accepts task details and returns the new ID.

### UpdateTask

Updates an existing task based on ID.

### DeleteTask

Removes a task by ID.

## Error Handling

Faults return a standard SOAP Fault element with faultcode and faultstring.

## Data Types

The WSDL defines complex types such as Task, User, and Project with relevant fields.

## Authentication

API key passed as a SOAP header element `<tsk:ApiKey>YOUR_KEY</tsk:ApiKey>`.

## Sample WSDL snippet

```xml
<definitions xmlns=\"http://schemas.xmlsoap.org/wsdl/\" ...>
  <types>
    <xsd:schema targetNamespace=\"http://acmetasker.com/soap\">
      <xsd:complexType name=\"Task\">
        <xsd:sequence>
          <xsd:element name=\"id\" type=\"xsd:int\"/>
          <xsd:element name=\"title\" type=\"xsd:string\"/>
        </xsd:sequence>
      </xsd:complexType>
    </xsd:schema>
  </types>
</definitions>
```

Clients should generate stubs using tools like wsdl2java or svcutil.

For more details and sample projects, see the developer portal.
