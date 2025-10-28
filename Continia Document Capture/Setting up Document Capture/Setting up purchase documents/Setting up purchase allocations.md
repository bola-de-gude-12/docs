---
title: Setting up purchase allocations in Document Capture
date: 15-10-2025
description: How to set up purchase allocations in Document Capture.
id: DC-41
lang: en
---

# Setting up purchase allocations

Purchase allocation is the act of temporarily posting the amounts of a purchase document (an invoice or a credit memo) to the general ledger (G/L). When the purchase document is sent for approval, a purchase allocation – a header with a number of lines – is created. The manual or automatic posting of this purchase allocation then generates both allocation entries and corresponding G/L entries, and these temporary entries are later reversed and made permanent as such in the G/L, once the document has been approved and posted. In this way, purchase allocation allows you to provisionally preregister document amounts which can then later be converted into actual G/L entries.

For example, when you receive a purchase invoice, the invoice amounts aren't immediately visible in the G/L, but you can make them appear in the G/L through the use of purchase allocations. This may be useful or even necessary for auditing purposes or similar. If you enable automatic purchase allocation, one or more provisional purchase allocation entries are created and posted to the G/L once you send the invoice for approval. When the invoice is then approved and posted, Continia Document Capture reverses these provisional entries and replaces them with actual entries in the G/L.

As described below, you can configure Document Capture to create and post purchase allocation entries [automatically](#to-create-and-post-purchase-allocation-entries-automatically), or it can be set up to enable you to do this [manually](#to-create-and-post-purchase-allocation-entries-manually). Note that this article focuses on invoices, although purchase allocation works equally well with credit memos.

## To create and post purchase allocation entries automatically

1. Search ({{search}}) for and select **Document Capture Setup**.
1. On the action bar, click **Setup** > **Purchase Approval** to open the **Document Capture Setup / Purchase Approval** page.
1. Under **Purchase Allocation**, enable purchase allocation by turning on the **Enable** switch.
1. In **Amounts**, specify if Document Capture should use purchase invoice lines or imported amounts to retrieve the amounts used for purchase allocation. Note that if you select **Use Lines or Imported Amounts**, purchase invoice lines are given priority, but if no such lines exist, imported amounts are used instead.

   > [!NOTE]
   > If you choose **Always use Imported Amounts** here, **G/L Account Type** can't be configured in step 5 below – and the purchase allocation accounts you set up in **Vendor Posting Groups** is used for the creation and posting of purchase allocation entries. For more information, see [To configure posting accounts](#to-configure-posting-accounts) below.
   > 
   > The term imported amount refers to the total amount of the invoice.

1. In **G/L Account Type**, specify which cost accounts to use when purchase allocation entries are created. You have the following options:
   * **Use Posting Setup** - Document Capture uses the purchase allocation accounts you've set up in the **General Posting Setup**. To set up these accounts, see [General Posting Setup](#general-posting-setup) below.
   * **Use Account on Purchase Lines** - Document Capture uses the G/L accounts assigned to each of the purchase invoice lines. If some invoice lines don't have a G/L account assigned, the **General Posting Setup** is used instead. See [To configure posting accounts](#to-configure-posting-accounts) for more details.
1. Enable automatic creation and posting of purchase allocation entries by turning on the **Post Automatically** setting.
1. In **Posting Date on Reversal**, select which posting date should be used when purchase allocation entries are reversed. You can choose either the original date when the purchase allocation was posted or the date when the invoice is posted.

When you send an invoice for approval, provisional purchase allocation entries are created and posted to the G/L, and these provisional purchase allocation entries are automatically reversed and replaced with actual entries in the G/L once the invoice has been approved and posted.

## To create and post purchase allocation entries manually

To create and post purchase allocation entries manually, you must first enable and configure purchase allocation in the **Document Capture Setup**. To do this, follow the [guide above](#to-create-and-post-purchase-allocation-entries-automatically), but skip step 6 to leave **Post Automatically** disabled.

Once you've completed the setup guide, you can create and post purchase allocation entries manually:

1. In the Role Center, under **Continia Document Capture Activities**, go to **Purchase Approval - Invoices** and select **Open PIs** to open the list of open purchase invoices.
1. From the list, select the invoice for which you want to create and post purchase allocation entries.
1. On the action bar, click **Related** > **Invoice** > **Allocations** to open the **Purchase Allocation List**.
1. On the action bar, click **New** to create a new purchase allocation.
1. On the **Purchase Allocation** page, on the action bar, click **Create Lines** to fill all required fields with the relevant data. You can also do this manually under **Lines**.
1. On the action bar, click **Post** to post the purchase allocation to the G/L.

> [!NOTE]
> When the invoice has been approved and posted, the purchase allocation is reversed. This reversal is carried out automatically, regardless of whether the purchase allocation was created and posted automatically or manually.

> [!TIP]
> If you want to view the posting history of a purchase allocation, go to that allocation's **Purchase Allocation** page, and then select **Find entries** on the action bar. This opens the **Find entries** page, which provides an overview of the selected allocation.

## To configure posting accounts

When you set up either automatic or manual creation and posting of purchase allocations as described above, you must specify which amounts to assign under **Amounts** and which cost accounts to use under **G/L Account Type**. No matter what you specify in these fields, you must also set up accounts in [**Vendor Posting Groups**](#vendor-posting-groups). The balance accounts you assign here are always used for the creation and posting of purchase allocations, whereas the purchase allocation accounts you assign here are only used in certain scenarios – just like the purchase allocation accounts from the [**General Posting Setup**](#general-posting-setup), which you may also have to set up.

Which of the purchase allocation accounts is used depends on what you select under **Amounts** and **G/L Account Type** in the **Document Capture Setup**:

<br>

| Selected settings | Resulting action |
| --- | --- |
| Under **Amounts**: <ul><li><b>Always use Imported Amounts</b></li></ul> | With this setting (**G/L Account Type** is not applicable here), the purchase allocation accounts you've assigned in **Vendor Posting Groups** are used. Only one account is used for the total invoice amount (also known as the imported amount) – regardless of the number of invoice lines – and this account is assigned based on the posting group of the vendor that sent the invoice. <br><br> For more information on how to assign vendor posting group accounts, see [**Vendor Posting Groups**](#vendor-posting-groups) below. |
| Under **Amounts**: <ul><li><b>Use Lines or Imported Amounts</b></li></ul> Under **G/L Account Type**: <ul><li><b>Use Posting Setup</b></li></ul> | With these combined settings, the purchase allocation accounts from the **General Posting Setup** are used, so you must remember to set this up as well. One purchase allocation entry is posted for each invoice line, and to each individual invoice line Document Capture assigns the purchase allocation account that matches that particular invoice line's combination of **Gen. Bus. Posting Group** and **Gen. Prod. Posting Group** as specified by you. <br><br> For more information, see [**General Posting Setup**](#general-posting-setup) below. |
| Under **Amounts**: <ul><li><b>Use Lines or Imported Amounts</b></li></ul> Under **G/L Account Type**: <ul><li><b>Use Account on Purchase Lines</b></li></ul> | With these combined settings, one purchase allocation entry is posted for each invoice line, using the accounts already present in the individual invoice lines themselves. <br><br> However, if some invoice lines don't have a G/L account assigned, the **General Posting Setup** is used instead. In such cases, Document Capture posts one purchase allocation entry for each invoice line with no G/L account assigned, again using the purchase allocation account that matches that particular invoice line's combination of **Gen. Bus. Posting Group** and **Gen. Prod. Posting Group** as specified by you. <br><br> For more information, see [**General Posting Setup**](#general-posting-setup) below. |

### General Posting Setup

To set up purchase allocation accounts in the **General Posting Setup**:

1. Search ({{search}}) for and select **General Posting Setup**.
1. On the action bar, click **Edit List**.

   > [!NOTE]
   > The list is in fact a table, and each line of the table represents a combination of a general business posting group (for the vendor of an invoice) and a general product posting group (for the G/L account or item of an invoice line). When the combination of a table line matches that of an invoice line, the purchase allocation account that you've assigned to that table line is set up as the cost account of the matching invoice line.

1. Locate the table line that you want to assign a purchase allocation account to, and select **Purch. Account (Allocation)**.
1. Select the three dots on the right of the **Purch. Account (Allocation)** field to open the **G/L Account List**. In the list, under **No.**, select the account that you want to assign to the selected table line.
1. Repeat steps 3-4 for every additional table line that you want to assign accounts to.

The accounts you've assigned are then used for the purchase allocation entries that are created and posted to the G/L when you send an invoice for approval – but only when the following conditions apply:

* In the **Document Capture Setup**, under **Purchase Allocation** > **Amounts**, the option **Use Lines or Imported Amounts** must be selected.
* There must be one or more lines in the invoice.
* One of the following:
   * In the **Document Capture Setup**, under **Purchase Allocation** > **G/L Account Type**, the option **Use Posting Setup** must be selected.
   * The relevant purchase invoice line(s) must be of a different type than G/L account.

### Vendor Posting Groups:

To set up accounts in **Vendor Posting Groups**, follow these steps:

1. Search ({{search}}) for and select **Vendor Posting Groups**.
1. On the action bar, click **Edit List**.
1. Locate the table line that you want to assign an account to, and select **Payable Account (Allocation)**.
1. Click the three dots on the right of the **Payable Account (Allocation)** field to open the **G/L Account List**. In the list, under **No.**, select the account that you want to assign to the selected table line.
1. Under **Purch. Account (Allocation)**, select the three dots on the right of the field to open the **G/L Account List**. In the list, under **No.**, select the account that you want to assign to the selected table line.
1. Repeat steps 3-5 for every additional table line that you want to assign accounts to.

The accounts you've assigned are then used as follows for the purchase allocation entries that are created and posted when you send an invoice for approval:

* **Payable Account (Allocation)** - the balance account – is always used.
* **Purch. Account (Allocation)** - the cost account – is only used when **Always use Imported Amounts** has been selected in the **Document Capture Setup**.







<style>
  .content table tr td:nth-child(1) {
    width: 180px;
  }
  .content table tr td:nth-child(2) {
    width: 550px;
  }  
</style>