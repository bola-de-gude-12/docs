---
title: Approving contract invoices in Document Capture
date: 08-01-2025
description: How to set up the automatic approval of contract invoices.
id: DC-89
lang: en
---

# Approving Contract Invoices

With the Purchase Contracts module, you can have any contract invoice (that is, any purchase invoice that's linked to a purchase contract) approved automatically when the invoice is registered. You can also set up a variance amount or percentage for each contract line, so that invoices whose amounts relate to the contract amounts within the specified variance are automatically approved upon registration.

For the sake of simplicity, this article uses invoices as an example. However, the functionality works just as well with contract credit memos.

> [!NOTE]
> To set up a variance amount or percentage, line recognition must be enabled in the relevant template. Without line recognition enabled, the feature only works when the invoice and contract line amounts match exactly.

## To enable automatic approval of contract invoices

Before Document Capture can automatically approve contract invoices, you must enable this feature on both the **Purchase Contract** and **Template Card** pages.

### On the Purchase Contract page

To enable automatic approval on the **Purchase Contract** page:

1. Choose the {{search}} icon, enter **Purchase Contracts**, and then choose the related link to open the **Purchase Contracts** page.
1. In the list of contracts, in the **No.** column, select the number of the contract whose related invoices you want to be approved automatically. This opens the **Purchase Contract** page.
1. **Optional**: On the **General** FastTab, select the **Price Type** field, and then select **Variable Amount**. This allows you to add variances in steps 5-6 below.
1. In the **Auto Approve Within Variance** field, select **Yes**.
1. **Optional**: To set up a variance percentage for a line, go to the **Lines** FastTab, select the relevant line, and then enter the percentage under **Max. Allowed Line Variance %**. Repeat this step for any additional lines you want to set up a variance for.
1. **Optional**: To set up a variance amount for a line, select the relevant line on the **Lines** FastTab, and then enter the amount under **Max. Allowed Line Variance**. Repeat this step for any additional lines you want to set up a variance for.

   > [!NOTE]
   > The **Max. Allowed Line Variance** field may have to be added first to be visible. To do this, [personalize the page](https://docs.microsoft.com/en-us/dynamics365/business-central/ui-personalization-user) as follows:
   >
   > 1. Select the {{settings}} icon > **Personalize** > **+ Field** to open the **Add Field to Page** pane.
   > 2. Select the **Lines** section, and then drag the **Max. Allowed Line Variance** field from the pane to the table in the selected section.
   > 3. Select **Done** to close the **Personalizing** banner.

By default, contract invoices that are up to 3 days early or late when compared with the contract start date (for the first invoice) or with the date in the latest invoice (for subsequent invoices) can still be auto-approved. To change this:

1. Choose the {{search}} icon, enter **Purchase Contracts Setup**, and then choose the related link to open the **Purchase Contracts Setup** page.
2. On the **Approval** FastTab, enter the desired formula in the **Max. Allowed Approval Date Variance** field. For example, 5D (five days).   

### On the Template Card page

To ensure that registered contract invoices are actually sent for approval automatically, you must configure the second step of the registration process on the **Template Card** page. To do this, follow these steps:

1. Search ({{search}}) for and select **Document Categories**.
1. Select the **PURCHASE** code to open the document journal.
1. In the list of documents, select the invoice whose template you want to edit.
1. On the action bar, click **Template** > **Template Card** to open the **Template Card** page.
1. On the **Purchase Documents** FastTab, under **Registration**, select the **Invoice Reg. Step 2** field, and then select **Submit for Approval**.

   > [!NOTE]
   > By following the instructions above, you’re only enabling automatic approval for the template that’s assigned to the selected invoice. If you instead enable it for the master template, all newly created templates will automatically have it enabled too. To learn more, see [Working with Templates](@DC-18).

## To approve contract invoices

Once you've completed both parts of the setup process as described above, you can have any contract invoice automatically approved simply by registering it:

1. Search ({{search}}) for and select **Document Categories**.
1. Select the **PURCHASE** code to open the document journal.
1. In the list of documents, select the invoice that you want to register.
1. On the action bar, click **Process** > **Register**.

This both registers and automatically approves the invoice, and the **Purchase Invoice** page opens. On the **General** FastTab, the **Approval Comments** field displays the text **The invoice was automatically approved**.

## Scenarios

The scenarios below exemplify the auto-approval logic.

### First contract invoice

If there are no other invoices related to the purchase contract – be them posted or unposted –, Document Capture only auto-approves the new invoice if its posting date is either the same as or later than the start date of the contract.

### Unposted purchase invoice exists

If there’s one or more unposted invoices related to the purchase contract, Document Capture doesn’t auto-approve the new invoice because it can’t perform the required date check.

**Posted purchase invoice exists**

If there’s one or more posted invoices related to the purchase contract, Document Capture auto-approves the new invoice – provided that this invoice passes the date check.

### Posted and unposted invoices exist

If there are both posted and unposted invoices related to the purchase contract, Document Capture ignores the unposted invoices, performs the date check based on the latest posted invoice, and auto-approves the new invoice – provided that this invoice passes the date check.


## Related information

[Creating Purchase Contracts](@DC-86)  
[Purchase Contract Approvals](@DC-87)  
[Creating Contract Invoices](@DC-88)  
[Viewing the Purchase Contract Archive](@DC-90)  