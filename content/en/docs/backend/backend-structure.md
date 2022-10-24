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
weight: 100
toc: true
---

## Packages

For a general overview on Spring packages, see 
[Project Structure and Best Practices](https://medium.com/the-resonant-web/spring-boot-2-0-project-structure-and-best-practices-part-2-7137bdcba7d3).

Centralis22's backend implementation contains the following packages:
| Name | Comments |
| ---  | ---      |
| Config | Config. |
| Handler | Classes to communicate with frontend. |
| Model | Java objects used by the backend. Can be serialized from/to DB and frontend. |
| Repository | DB query methods. See [Spring Data JPA](https://docs.spring.io/spring-data/jpa/docs/current/reference/html/#repositories). |
| Security | Classes to validate a user and save his login information. |
| Service | Classes directly related to Centralis's requirements. |
| Util | Supplementary classes to help services. |
