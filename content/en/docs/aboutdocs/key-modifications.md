---
title: "Key Modifications"
description: "Modifications to the Doks template."
lead: "Modifications to the Doks template."
date: 2022-09-20T00:00:00+00:00
lastmod: 2022-09-20T00:00:00+00:00
draft: false
images: []
menu:
  docs:
    parent: "aboutdocs"
weight: 820
toc: true
---

## Basic Modifications

Basic modifications are made according to the 
[Doks tutorial](https://getdoks.org/docs/tutorial/introduction/).

## Theme Modifications

Theme modifications are located in `./layouts/` and `./static/css`.

## Functional Modifcations

- `./partials/header/header.html` has been hard-coded to direct to 
the project subdomain `/devdocs` to support Github project pages. 
On local testing, clicking `Centralis` and `Get Started` will lead to 
`404`.

- `./layouts/index.html` has been modified to suit the project.
