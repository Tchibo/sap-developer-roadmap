---
tags:
  - nodejs
  - framework
  - backend
links:
  - "[[Node.js]]"
  - "[[JavaScript]]"
  - "[[TypeScipt]]"
source:
aliases:
---

In [[SAP Capire]] applications built with [[Node.js]], the application logic is technically based on Express middleware. Event handlers that developers implement for CRUD operations or custom events are in fact middleware functions registered on the Express framework. This means that whenever a request reaches the [[SAP Capire|CAP]] service layer, the corresponding handler is executed within the Express pipeline. Understanding this concept helps [[SAP Capire|CAP]] developers see how their application logic integrates into the [[Node.js]] runtime, making it clearer how requests are processed and how additional middleware, such as authentication or logging, can be applied consistently.

**Source**
- [Roadmap.sh - JavaScript Developer](https://roadmap.sh/javascript)
- [Website - ExpressJS](https://expressjs.com/)