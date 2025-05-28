---
title: RSXML
description: A free, public Python package for authoring Riverscapes projects
banner: true
---

The [Riverscapes Consortium](https://riverscapes.net) has developed a standard for packaging data related to riverscapes health so that it can be shared and discovered via the [Riverscapes Data Exchange](https://data.riverscapes.net).

The standard consists of a small, simple XML text file that sits in the root folder of the data being described. This file lists all the datasets, reports, log files etc. It is the backbone of the Riverscapes Data Exchange and is what allows for effective curation and discovery of data. The file is always called `project.rs.xml`. It can be written by hand, but is much easier if you script its generation to avoid mistakes and increase reuse.

RSXML is a free, public Python package that allows Riverscapes tool developers to easily author `project.rs.xml` project files. It is available as a pip module from the PyPi online respoitory of Python packages.

[https://pypi.org/project/rsxml/](https://pypi.org/project/rsxml/)

RSXML includes documentation on how to use it to author projects, including code examples. Contact a Riverscapes Application Support Specialist (support@riverscapes.freshdesk.com) if you have data that you want to add to the Riverscapes Data Exchange and need help using RSXML to author project files.
