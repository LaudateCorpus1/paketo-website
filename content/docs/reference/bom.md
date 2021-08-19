---
title: "Paketo Bill of Materials"
weight: 300
menu:
  main:
    parent: reference
    indentifier: bom
aliases:
  - /docs/buildpacks/bom/
---

## What is the Bill of Materials?

When using Paketo buildpacks to build your app image, you have access to a
natively created Bill of Materials. This is 

### Accessing the Bill of Materials

{{< code/copyable >}}
pack inspect-buildpack node-app --bom
{{< /code/copyable >}}


Notes from Frankie
The places this could go
Concepts (What is a BOM? Why?)
How-to (BOM has its own page. How to view BOM)
Indidual buildpacks (Maybe how to see the node modules in the image? how to see the node engine) (This is potentially not useful now wait for users to ask question)
Reference (What will get added to the BOM) (STILL INDIVIDUAL) (Don't worry right now)
What is the useful information to show up in reference from the BOM
