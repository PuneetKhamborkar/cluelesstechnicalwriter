---
layout: single
title: DITA vs Diátaxis
permalink: /InfoDev-Uni/dita-vs-diataxis/
toc: true
sidebar: InfoDev_Uni
---

DITA and Diátaxis solve different problems.

Most people compare them directly. That is where confusion starts.

DITA is about **structure and reuse**  
Diátaxis is about **user intent and content type**

You don’t choose one over the other. You use them together.

---

# What is DITA?

DITA (Darwin Information Typing Architecture) is a structured documentation framework.

It helps you:
- Break content into reusable pieces
- Maintain consistency at scale
- Publish across multiple formats

## Core Building Blocks

### Topics
- Concept → explains something
- Task → step-by-step instructions
- Reference → factual information

### Maps
- Define how topics are organized
- Control output structure

### Reuse
- Content references (conref)
- Key references (keyref)

---

## When to Use DITA

- Large documentation sets
- Multiple products or versions
- Need for content reuse
- Enterprise environments

---

## What is Diátaxis?

Diátaxis is a documentation framework focused on **how users consume content**.

It answers one simple question:

👉 What does the user need right now?

---

## The 4 Content Types

### Tutorials (Learning)
- Step-by-step
- Beginner-friendly
- Focus on doing

**Example:**  
Build your first API call

---

### How-to Guides (Problem solving)
- Goal-oriented
- Not beginner-level
- Direct and practical

**Example:**  
How to integrate payment gateway

---

### Reference (Information)
- Facts only
- No storytelling
- Complete and precise

**Example:**  
API endpoint documentation

---

### Explanation (Understanding)
- Deep dive
- Concepts and reasoning

**Example:**  
How authentication works

---

## When to Use Diátaxis

- Developer documentation
- API documentation
- Product documentation
- Any user-facing content

---

# Key Difference

| Aspect            | DITA                          | Diátaxis                      |
|------------------|-------------------------------|-------------------------------|
| Focus            | Structure                     | User intent                   |
| Goal             | Reuse and consistency         | Clarity and usability         |
| Content Type     | Concept, Task, Reference      | Tutorial, How-to, Reference, Explanation |
| Usage            | Enterprise documentation      | Modern documentation systems  |
| Thinking Style   | System-driven                 | User-driven                   |

---

# The Real Insight

DITA tells you:

👉 “How to structure content internally”

Diátaxis tells you:

👉 “How to present content to users”

---

# How They Work Together

This is where most writers level up.

You can:
- Use **DITA topics** to create structured content
- Apply **Diátaxis** to decide how that content is written

### Example

A DITA task can become:
- A Tutorial (if beginner-focused)
- A How-to guide (if problem-focused)

A DITA concept can become:
- Explanation content

A DITA reference stays:
- Reference

---

# Common Mistakes

- Mixing all content types into one page
- Writing tutorials like references
- Using DITA without thinking about users
- Ignoring structure in Diátaxis

---

# Practical Workflow

1. Start with Diátaxis  
   → What does the user need?

2. Then use DITA  
   → How should this be structured?

3. Write content  
   → Keep it focused and clean

---

# Final Thought

If you only use DITA:
You get structured but confusing documentation.

If you only use Diátaxis:
You get clear but inconsistent documentation at scale.

If you use both:
👉 You get scalable, user-focused documentation.

That is what modern technical writing looks like.