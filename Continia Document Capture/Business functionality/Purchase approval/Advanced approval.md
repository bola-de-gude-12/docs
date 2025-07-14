---
title: Advanced approval in Document Capture
date: 07-07-2025
description: A description of advanced approval and how it works, including illustrative examples.
id: DC-38
lang: en
---

# Advanced approval

As an alternative to [standard purchase approval](Standard purchase approval.md) and [approval flows](@DC-33) in Continia Document Capture, in which approval routes are fixed and predetermined based exclusively on invoice amounts, advanced approval allows for a faster and more flexible approval process based on both invoice amounts and [dimensions](https://docs.microsoft.com/en-us/dynamics365/business-central/finance-dimensions). This means that:

* You can define the dimensions that help to identify all approvers for any invoice that's sent for approval.
* The next approver isn't identified until the current approver has approved all relevant invoice lines.
* Document lines due to be approved by the current approver are marked in bold, both on the **Purchase Approval Entries** page in Microsoft Dynamics 365 Business Central and on the Continia Web Approval Portal.

The advanced approval concept is best explained using scenarios, which are provided [below](#advanced-approval-scenarios). Note that this article uses invoices for illustrative purposes, although the functionality works equally well with credit memos.

> [!NOTE]
> In order to work, advanced approval must be enabled and set up. To do this, see [Setting up advanced approval](@DC-31).

## Advanced approval scenarios

For advanced approval, the dimensions you define – together with the invoice line amounts – determine who gets to approve any invoice sent for approval.

>[!NOTE]
>If a document doesn't have values for the dimensions specified in the advanced approval, Document Capture only takes the line amount total into consideration when selecting the approver.

In these scenarios, an advanced approval group has been set up with the dimension **Department Code** applied, and the users Robin Bettencourt, Esther Henderson, and Otis Falls have been added as approvers. They have different approval limits for the two dimension values **Production** and **Sales**:

<br>

| Approver | Department | Approval limit |
| --- | --- | --- |
| Robin Bettencourt | Production | $25,000 |
| Esther Henderson | Sales | $25,000 |
| Otis Falls | Production, Sales | $40,000 |

For descriptive purposes and ease of understanding, these scenarios are based on the one dimension **Department Code** and only three approvers in the approval group. However, you can have multiple dimensions and numerous approvers involved – adding both flexibility and complexity.

### Scenario A

An invoice with the following line dimension values and amounts is sent for approval:

<br>

| Line no. | Department | Amount |
| --- | --- | --- |
| 1 | Production | $5,000 |
| 2 | Sales | $5,000 |

In theory, this invoice could be sent to Otis Falls for full approval, as he has permission and sufficient approval limit to approve both of the dimension values and, consequently, both lines. However, Otis Falls is the highest-ranking approver and Document Capture strives to burden high-ranking approvers the least. Therefore, the invoice is sent first to Robin Bettencourt, whose approval permission matches the dimension value of the first line (**Production**). When Robin has approved the first line, the invoice is forwarded to Esther Henderson – whose approval permission matches the second line (**Sales**). When Esther has approved the second line, the invoice is fully approved.


### Scenario B

Another invoice with the following line dimension values and amounts is sent for approval:

<br>

| Line no. | Department | Amount |
| --- | --- | --- |
| 1 | Production | $20,000 |
| 2 | Production | $20,000 |
| 3 | Sales | $20,000 |

For this invoice, none of the three approvers can approve all lines – so its approval has to be split between them. Robin Bettencourt has permission to approve invoice lines with the dimension value **Production**, but his approval limit of $25,000 is insufficient here, as the two **Production** lines (lines 1 and 2) come to a total of $40,000. For this reason, the first approver has to be Otis Falls, whose approval limit is sufficient for him to approve the first two invoice lines.

Although Otis also has permission to approve **Sales** lines, he's unable to approve the remaining invoice line because the total of the three lines would then exceed his approval limit. So line 3 must instead be approved by a second approver, Esther Henderson, who can approve **Sales** lines for up to $25,000. This is enough to cover the approval of this remaining line. With Esther's approval of line 3, the invoice is fully approved.

## Four-eye approval scenarios

If you always want at least two approvers to approve invoices, [enable the four-eye approval setting](@DC-31#to-set-up-advanced-approval-groups). This plays out differently depending on how you set it up. Using the same approval group as [above](#advanced-approval-scenarios), the following scenarios illustrate the different flows.

### Scenario A

In this scenario, **Invoice** was selected when four-eye approval was enabled and set up.

An invoice with multiple lines that require multiple approvers is sent for approval. Since more than one approver is already required, four-eye approval is applied automatically, and there's no need for Document Capture to identify additional approvers. This is the case in scenarios A and B above, in which both invoices have multiple lines requiring multiple approvers. If four-eye approval had been enabled in these scenarios, the outcome would have been the same.

### Scenario B

In this scenario, **Invoice** was selected when four-eye approval was enabled and set up.

An invoice is sent for approval, but this one only has one line:

<br>

| Line no. | Department | Amount |
| --- | --- | --- |
| 1 | Sales | $21,000 |

Two of the approvers in the approval group have the required permissions and approval limits to approve this line: Esther Henderson (who can approve **Sales** lines for up to $25,000) and Otis Falls (who can approve **Sales** and/or **Production** lines for up to $40,000). As Esther has the lower approval limit of the two, she's identified as the first approver. When Esther has approved the line, the invoice is sent to Otis.

### Scenario C

In this scenario, **Invoice Full Amount** was selected when four-eye approval was enabled and set up. Therefore, at least two approvers must approve the total amount of each invoice.

An invoice is sent for approval, this time with the following line dimension values and amounts:

<br>

| Line no. | Department | Amount |
| --- | --- | --- |
| 1 | Production | $7,000 |
| 2 | Production | $16,000 |

Robin Bettencourt has permission to approve **Production** lines, and his approval limit of $25,000 covers both lines – that is, the total invoice amount – so he's identified as the first approver. When Robin has approved the two lines, the invoice is forwarded to Otis Falls, who also has the required permission and approval limit to approve both lines. When Otis has approved the lines as the second pair of eyes in the four-eye approval process, the invoice is fully approved.

> [!NOTE]
> When you [set up advanced approval groups](/continia-document-capture/setting-up-document-capture/setting-up-document-approval/setting-up-advanced-approval#to-set-up-advanced-approval-groups), you can select **Purchaser** under **First Entry Created by** to always have the purchaser assigned as the first approver. However, if **Four Eyes Approval** is set to **Invoice Full Amount and Dimensions**, instead of **Invoice**, the purchaser doesn't count as one of the two approvers required.





<style>
  .content table tr td:nth-child(1) {
    width: 300px;
  }
  .content table tr td:nth-child(2) {
    width: 300px;
  }  
</style>