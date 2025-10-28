---
title: Release plan for Document Capture
date: 28-10-2025
description: The Document Capture roadmap provides an overview of upcoming functionality.
id: DC-56
lang: en
---

# Release plan for Document Capture

{{include "new-and-planned-overview" "Document Capture"}}

| Feature                                                      |     Public preview     |                     General availability                     |
| ------------------------------------------------------------ | :--------------------: | :----------------------------------------------------------: |
| [eDocuments first](@DC-467)                                  | {{checkmark}} Sep 2025 |                    {{checkmark}} Sep 2025                    |
| [Support for the SimplerInvoicing format in the Netherlands](@DC-419) | {{checkmark}} Sep 2025 | {{checkmark}} Sep 2025<a href="#footnote-7"><sup>7</sup></a> |
| [Option to embed PDF files](@DC-465)                         | {{checkmark}} Sep 2025 |                    {{checkmark}} Oct 2025                    |
| [Lookup in template field translations](@DC-468)             | {{checkmark}} Sep 2025 |                    {{checkmark}} Oct 2025                    |
| [Processing documents with rounding issues](@DC-469)         | {{checkmark}} Sep 2025 |                    {{checkmark}} Oct 2025                    |
| [Capturing item tracking information](@DC-470)               | {{checkmark}} Sep 2025 |                    {{checkmark}} Oct 2025                    |
| [Support for Business Central's sustainability feature](@DC-322) | {{checkmark}} Sep 2025 |                    {{checkmark}} Oct 2025                    |
| [eDocument validation](@DC-466)                              |           -            |        Nov 2025<a href="#footnote-9"><sup>9</sup></a>        |
| [Support for the FA(3) format in Poland](@DC-417)            |           -            |       Nov 2025<a href="#footnote-10"><sup>10</sup></a>       |
| [Support for OData V4 for the Continia Web Approval Portal](@DC-432) |           -            |          N/A<a href="#footnote-1"><sup>1</sup></a>           |
| [One email for all companies to notify about open approval entries](@DC-406) |           -            |          N/A<a href="#footnote-1"><sup>1</sup></a>           |
| [Continia eDocuments Support for OIOUBL 3.0](@DC-410) |           -            |          N/A<a href="#footnote-2"><sup>2</sup></a>           |
| [Checking PDF signatures](@DC-409) |           -            |          N/A<a href="#footnote-3"><sup>3</sup></a>           |
| [Optimized export of users - part 2](@DC-431) |           -            |          N/A<a href="#footnote-4"><sup>4</sup></a>           |
| [Identification of account numbers using artificial intelligence](@DC-412) |           -            |          N/A<a href="#footnote-5"><sup>5</sup></a>           |
| [Support for sales shipments](@DC-415) |           -            |          N/A<a href="#footnote-8"><sup>8</sup></a>           |
| [Support for the EHF format for eOrders in Norway](@DC-416) |           -            |          N/A<a href="#footnote-8"><sup>8</sup></a>           |
| [Educational page to improve user knowledge of eDocuments and formats](@DC-411) |           -            |          N/A<a href="#footnote-8"><sup>8</sup></a>           |
| [Simpler eDocuments onboarding](@DC-414) |           -            |          N/A<a href="#footnote-8"><sup>8</sup></a>           |
| [Handle XML files received via email using the eDocuments framework](@DC-401) |           -            |          N/A<a href="#footnote-8"><sup>8</sup></a>           |


<small style>

<div class="footnotes">
  <hr />
  <ol>
    <li id="footnote-1">The release date for this feature is yet to be determined.</li>
    <li id="footnote-2">The release of this feature depends on the official release of OIOUBL 3.0, which the Danish Business Authority (Erhvervsstyrelsen) is currently working on.</li>
    <li id="footnote-3">As Continia has yet to see legal or business demands regarding the checking of signatures on incoming PDFs, this feature has been postponed to a later version of Document Capture.</li>
    <li id="footnote-4">The first part of this feature addressed most problems related to the user update. Therefore, there's no longer need to implement the second part of the optimization.</li>
    <li id="footnote-5">After looking into the possibilities, Continia has concluded that, for now, the use of artificial intelligence to determine account numbers wouldn't reduce processing time.</li>
    <li id="footnote-6">This feature was released in May 2025, in line with the requirements by the Australian and New Zealand governments.</li>
    <li id="footnote-7">This feature will be released either as part of a hotfix or of a service pack.</li>
    <li id="footnote-8">Due to changes in focus and legislation, Continia has decided to postpone the release of this feature.</li>
    <li id="footnote-9">This feature will be released as part of a service pack in November 2025.</li>
    <li id="footnote-10">Due to the official version of the KSeF API being available only at the end of September, this feature can't be released in October – but will be released with the next service pack.</li>
  </ol>
</div>

</small>

## Detailed changelog

For each change to Document Capture, Continia’s detailed changelog is updated with a description of what has changed. For the full changelogs, see [Detailed changelogs for Document Capture](@DC-449).