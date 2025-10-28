---
title: Minimize that files are overwritten
date: 11-12-2024
description:
id: DC-378
lang: en
---

# Minimize that Files Are Overwritten

| Feature | Public preview | General availability online |
| --- | :-: | :-: |
| Minimize that files are overwritten | - | {{checkmark}} Oct 2022 |

## Business value
By ensuring that file names are unique, it can be prevented that documents imported into a wrongly configured test system will overwrite files created in a production system.

## Feature details
When new documents are imported, various related files are created (PDF, TIFF, PNG, XML, or HTML files). When these files are stored in the local file system or Azure blob, the file name includes the document number from Business Central. 

When a test system is created as a copy of a production system, the configuration related to file storage must be changed. If the configuration is not changed, the test system will use the same storage location as the production system. This can lead to loss of files in the production system as documents imported into the test system will get the same file name potentially already is used in the production system.

To prevent this, a GUID will be added to the file name. This means that the file name will be unique even when files are created for the same document in a production and test system.
