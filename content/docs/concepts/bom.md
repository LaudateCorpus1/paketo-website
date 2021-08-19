---
title: "Bill of Materials"
weight: 440
menu:
  main:
    parent: "concepts"
aliases:
  - /docs/bom/
---

In the Getting Started tutorial, you used the Paketo builder to build a Node.js app. Once you have the final app image, you can access metadata about all of the dependencies present in the final app image with the Bill of Materials.

## What is the bill of materials?

A bill of materials (BOM) is an industry standard mechanism of surfacing metadata about dependencies in images or applications. The metadata consists of various fields such as:
* `version`: the dependency version
* `uri`: URI to compiled dependency
* `hash`: hash (such as SHA256) of the dependency
* `licenses`: dependency licenses in SPDX foramt
* `deprecation-date`: dependency deprecation date
* `source uri`: URI to upstream source dependency
* `source hash`: hash of the upstream source dependency
* `CPE`: common platform enumeration
* `pURL`: package URL

The information from the Bill of Materials is largely used to help understand the dependencies involved in your app's secure software supply chain. The Bill of Materials can be passed to one of the many existent vulnerability scanning tools in order to identify vulnerabilities. It can also be used for compliance checking, as an easy way to see the licenses for all packages involved.

