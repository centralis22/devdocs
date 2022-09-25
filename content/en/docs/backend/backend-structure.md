---
title: "Backend Structure"
description: "Spring Boot Project Structure."
lead: "Spring Boot Project Structure."
date: 2022-09-24T00:00:00+00:00
lastmod: 2022-09-24T00:00:00+00:00
draft: false
images: []
menu:
  docs:
    parent: "backend"
weight: 520
toc: true
---

## Packages

For an general overview, see 
[Project Structure and Best Practices](https://medium.com/the-resonant-web/spring-boot-2-0-project-structure-and-best-practices-part-2-7137bdcba7d3).

Centralis22's backend implementation contains the following packages:
| Name | Comments |
| ---  | ---      |
| Config | Config. |
| Handler | Communication with frontend. |
| Model | Java objects used in services. Can be serialized from/to DB and frontend. |
| Repository | DB query methods. |
| Service | Crucial methods that are directly related to the purpose of the application. |
| Util | Supplementary methods to help services. |
