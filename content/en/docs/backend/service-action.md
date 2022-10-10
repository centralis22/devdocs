---
title: "service.action"
description: "service.action package"
lead: "service.action package"
date: 2022-09-25T00:00:00+00:00
lastmod: 2022-09-25T00:00:00+00:00
draft: false
images: []
menu:
  docs:
    parent: "backend"
weight: 600
toc: true
---

## ActionDispatcher

Calls the corresponding `ActionHandler` depending on action type. Prevents 
bloating calling functions with if-else's.

## ActionHandler

Interface for concrete action handler implementations. Standardize code.