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
* `licenses`: dependency licenses in SPDX format
* `deprecation-date`: dependency deprecation date
* `source uri`: URI to upstream source dependency
* `source hash`: hash of the upstream source dependency
* `CPE`: common platform enumeration
* `pURL`: package URL

## Why is this helpful?
The information from the Bill of Materials is largely used to help understand the dependencies involved in your app's secure software supply chain.

#### Vulnerability Scanning
The Bill of Materials can be passed to one of the many existent vulnerability scanning tools, such as [Dependency Track](https://dependencytrack.org/), [Trivy](https://github.com/aquasecurity/trivy), and others, in order to identify vulnerabilities.

The BOM contains two fields that are primarily concerned with vulnerability identification:
* CPEs (common platform enumerations): standard notation to look up dependency version-specific vulnerabilities and related patches in the the [NIST National Vulnerabilty Database](https://nvd.nist.gov/products/cpe/search)
* pURLS (package URLs): [a universal representation](https://github.com/package-url/purl-spec) of package location regardkess if vendor, project, or ecosystem

#### Compliance Checking
The inclusion of license information in the Bill of Materials helps with application legal compliance, by providing the information in a consumable way for each dependency involved with your application image.

The licenses in the Paketo BOM are obtained from license scanning tools. Due to the unstandardized nature of license inclusion in software, the detection tools assign "confidence scores" to each license. We include **every license** discovered by the scanning tools in the BOM, regardless of the "confidence score" that the tool has provided to avoid risk of missing an important license. Because of this feature, advance compliance checking may be required to filter out false positive licenses that may be included.

#### Format
TODO
