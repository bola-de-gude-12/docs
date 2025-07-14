---
title: Release plan for Document Capture
date: 14-07-2025
description: The Document Capture roadmap, which lists all planned features.
id: DC-56
lang: en
---

# Release plan for Document Capture

{{include "new-and-planned-overview" "Document Capture"}}

| Feature                                                      |     Public preview     |                     General availability                     |
| ------------------------------------------------------------ | :--------------------: | :----------------------------------------------------------: |
| [Ability to handle payment means in Continia eDocuments](Documents and Templates/Ability to handle payment means in Continia eDocuments.md) | {{checkmark}} Mar 2025 |                    {{checkmark}} Apr 2025                    |
| [Inclusion of Document Capture files when copying, correcting, and canceling posted purchase invoices](Purchase Documents/Inclusion of Document Capture files when copying, correcting, and canceling posted purchase invoices.md) | {{checkmark}} Mar 2025 |                    {{checkmark}} Apr 2025                    |
| [Document matching improvements regarding units of measure](Order and Receipt Matching/Document matching improvements regarding units of measure.md) | {{checkmark}} Mar 2025 |                    {{checkmark}} Apr 2025                    |
| [Resending eBilling documents](Documents and Templates/Resending eBilling documents.md) | {{checkmark}} Mar 2025 |                    {{checkmark}} Apr 2025                    |
| [Improved usability and stability in Continia eDocuments](@DC-434) | {{checkmark}} Mar 2025 |                    {{checkmark}} Apr 2025                    |
| [Allow testing of eDocuments in sandboxes](@DC-400)          | {{checkmark}} Mar 2025 |                    {{checkmark}} Apr 2025                    |
| [Improve XML structure pages for easier customization](@DC-402) | {{checkmark}} Mar 2025 |                    {{checkmark}} Apr 2025                    |
| [Support for the PINT Billing and PINT A-NZ Billing formats in APAC](Documents and Templates/Support for the PINT Billing and PINT A-NZ Billing formats in APAC.md) | {{checkmark}} May 2025 | {{checkmark}} May 2025<a href="#footnote-6"><sup>6</sup></a> |
| [Support for the SimplerInvoicing format in the Netherlands](Documents and Templates/Support for the SimplerInvoicing format in the Netherlands.md) |           -            |        Sep 2025<a href="#footnote-7"><sup>7</sup></a>        |
| [Support for the FA(3) format in Poland](Documents and Templates/Support for the FA2 format in Poland.md) |           -            |                           Oct 2025                           |
| [Option to embed PDF files](@DC-465)                         |           -            |                           Oct 2025                           |
| [eDocument validation](@DC-466)                              |           -            |                           Oct 2025                           |
| [eDocuments first](@DC-467)                                  |           -            |                           Oct 2025                           |
| [Lookup in template field translations](@DC-468)             |           -            |                           Oct 2025                           |
| [Processing documents with rounding issues](@DC-469)         |           -            |                           Oct 2025                           |
| [Capturing item tracking information](@DC-470)               |           -            |                           Oct 2025                           |
| [Support for OData V4 for the Continia Web Approval Portal](Web Approval Portal/Support for OData V4 for the Continia Web Approval Portal.md) |           -            |          N/A<a href="#footnote-1"><sup>1</sup></a>           |
| [One email for all companies to notify about open approval entries](Document Approval/One email for all companies to notify about open approval entries.md) |           -            |          N/A<a href="#footnote-1"><sup>1</sup></a>           |
| [Continia eDocuments Support for OIOUBL 3.0](Documents and Templates/Continia eDocuments support for OIOUBL 3.0.md) |           -            |          N/A<a href="#footnote-2"><sup>2</sup></a>           |
| [Checking PDF signatures](Documents and Templates/Checking PDF signatures.md) |           -            |          N/A<a href="#footnote-3"><sup>3</sup></a>           |
| [Optimized export of users - part 2](Web Approval Portal/Optimized export of users – part 2.md) |           -            |          N/A<a href="#footnote-4"><sup>4</sup></a>           |
| [Identification of account numbers using artificial intelligence](Documents and Templates/Identification of account numbers using artificial intelligence.md) |           -            |          N/A<a href="#footnote-5"><sup>5</sup></a>           |
| [Support for sales shipments](Documents and Templates/Support for sales shipments.md) |           -            |          N/A<a href="#footnote-1"><sup>8</sup></a>           |
| [Support for the EHF format for eOrders in Norway](Documents and Templates/Support for the EHF format for eOrders in Norway.md) |           -            |          N/A<a href="#footnote-1"><sup>8</sup></a>           |
| [Educational page to improve user knowledge of eDocuments and formats](Documents and Templates/Educational page to improve user knowledge of eDocuments and formats.md) |           -            |          N/A<a href="#footnote-1"><sup>8</sup></a>           |
| [Simpler eDocuments onboarding](Documents and Templates/Simpler eDocuments onboarding.md) |           -            |          N/A<a href="#footnote-1"><sup>8</sup></a>           |
| [Handle XML files received via email using the eDocuments framework](@DC-401) |           -            |          N/A<a href="#footnote-1"><sup>8</sup></a>           |


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
    <li id="footnote-7">This feature will be released either as a hotfix or as a service pack.</li>
    <li id="footnote-8">Due to changes in focus and legislation, Continia has decided to postpone the release of this feature.</li>
  </ol>
</div>



</small>

## Detailed changelog

For each change to Document Capture, Continia’s detailed changelog is updated with a description of what has changed. For the full changelogs, see [Detailed changelogs for Document Capture](@DC-449).

## Related information

[Feature management](/Continia Document Capture/Development and Administration/Feature Management.md)  
[Previous release plans](@DC-45)  
[Business functionality](@DC-49)  
[Comparison of features in different versions of Document Capture](@DC-46)  