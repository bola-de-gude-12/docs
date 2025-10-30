---
title: Release plan for Document Capture
date: 28-10-2025
id: DC-56
lang: en
vars:
  solution_name: Document Capture
description: The Document Capture roadmap provides an overview of upcoming functionality
---

# Release plan for Document Capture

```meta
id: DC-56
lang: en
date: 2025-10-29
description: The Document Capture roadmap provides an overview of upcoming functionality.
```

{% include "../../.gitbook/includes/detailed-changelogs-overview.md" %}



| Feature                                                                           |              Public preview              |                              General availability                              |
| --------------------------------------------------------------------------------- | :--------------------------------------: | :----------------------------------------------------------------------------: |
| \[eDocuments first]\(@DC-467)                                                     | <i class="fa-check">:check:</i> Sep 2025 |                    <i class="fa-check">:check:</i> Sep 2025                    |
| \[Support for the SimplerInvoicing format in the Netherlands]\(@DC-419)           | <i class="fa-check">:check:</i> Sep 2025 | <i class="fa-check">:check:</i> Sep 2025[<sup>7</sup>](overview.md#footnote-7) |
| \[Option to embed PDF files]\(@DC-465)                                            | <i class="fa-check">:check:</i> Sep 2025 |                    <i class="fa-check">:check:</i> Oct 2025                    |
| \[Lookup in template field translations]\(@DC-468)                                | <i class="fa-check">:check:</i> Sep 2025 |                    <i class="fa-check">:check:</i> Oct 2025                    |
| \[Processing documents with rounding issues]\(@DC-469)                            | <i class="fa-check">:check:</i> Sep 2025 |                    <i class="fa-check">:check:</i> Oct 2025                    |
| \[Capturing item tracking information]\(@DC-470)                                  | <i class="fa-check">:check:</i> Sep 2025 |                    <i class="fa-check">:check:</i> Oct 2025                    |
| \[Support for Business Central's sustainability feature]\(@DC-322)                | <i class="fa-check">:check:</i> Sep 2025 |                    <i class="fa-check">:check:</i> Oct 2025                    |
| \[eDocument validation]\(@DC-466)                                                 |                     -                    |                 Nov 2025[<sup>9</sup>](overview.md#footnote-9)                 |
| \[Support for the FA(3) format in Poland]\(@DC-417)                               |                     -                    |                Nov 2025[<sup>10</sup>](overview.md#footnote-10)                |
| \[Support for OData V4 for the Continia Web Approval Portal]\(@DC-432)            |                     -                    |                    N/A[<sup>1</sup>](overview.md#footnote-1)                   |
| \[One email for all companies to notify about open approval entries]\(@DC-406)    |                     -                    |                    N/A[<sup>1</sup>](overview.md#footnote-1)                   |
| \[Continia eDocuments Support for OIOUBL 3.0]\(@DC-410)                           |                     -                    |                    N/A[<sup>2</sup>](overview.md#footnote-2)                   |
| \[Checking PDF signatures]\(@DC-409)                                              |                     -                    |                    N/A[<sup>3</sup>](overview.md#footnote-3)                   |
| \[Optimized export of users - part 2]\(@DC-431)                                   |                     -                    |                    N/A[<sup>4</sup>](overview.md#footnote-4)                   |
| \[Identification of account numbers using artificial intelligence]\(@DC-412)      |                     -                    |                    N/A[<sup>5</sup>](overview.md#footnote-5)                   |
| \[Support for sales shipments]\(@DC-415)                                          |                     -                    |                    N/A[<sup>8</sup>](overview.md#footnote-8)                   |
| \[Support for the EHF format for eOrders in Norway]\(@DC-416)                     |                     -                    |                    N/A[<sup>8</sup>](overview.md#footnote-8)                   |
| \[Educational page to improve user knowledge of eDocuments and formats]\(@DC-411) |                     -                    |                    N/A[<sup>8</sup>](overview.md#footnote-8)                   |
| \[Simpler eDocuments onboarding]\(@DC-414)                                        |                     -                    |                    N/A[<sup>8</sup>](overview.md#footnote-8)                   |
| \[Handle XML files received via email using the eDocuments framework]\(@DC-401)   |                     -                    |                    N/A[<sup>8</sup>](overview.md#footnote-8)                   |

***

1. The release date for this feature is yet to be determined.
2. The release of this feature depends on the official release of OIOUBL 3.0, which the Danish Business Authority (Erhvervsstyrelsen) is currently working on.
3. As Continia has yet to see legal or business demands regarding the checking of signatures on incoming PDFs, this feature has been postponed to a later version of Document Capture.
4. The first part of this feature addressed most problems related to the user update. Therefore, there's no longer need to implement the second part of the optimization.
5. After looking into the possibilities, Continia has concluded that, for now, the use of artificial intelligence to determine account numbers wouldn't reduce processing time.
6. This feature was released in May 2025, in line with the requirements by the Australian and New Zealand governments.
7. This feature will be released either as part of a hotfix or of a service pack.
8. Due to changes in focus and legislation, Continia has decided to postpone the release of this feature.
9. This feature will be released as part of a service pack in November 2025.
10. Due to the official version of the KSeF API being available only at the end of September, this feature can't be released in October – but will be released with the next service pack.

## Detailed changelog

For each change to Document Capture, Continia’s detailed changelog is updated with a description of what has changed. For the full changelogs, see \[Detailed changelogs for Document Capture]\(@DC-449).
