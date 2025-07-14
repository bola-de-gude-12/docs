---
title: Setting up the G/L Open Entries Module in Continia Finance
date: 26-02-2024
description: Learn more about how to configure the G/L Open Entries module.
id: CF-96
lang: en
---



# Setting up the G/L Open Entries Module

This article describes how you can configure the basic settings of the G/L Open Entries module and how you can (de)activate it on G/L account cards.

## To configure the G/L Open Entries module

To start using the G/L Open Entries module, there are a few things to set up. For example, choose to generate open entries from existing records, adjust hyperlink displays in reports, and restrict using two G/L open accounts for application.

To set up the G/L Open Entries module using the assisted setup:

1. Use the ![Search](https://docs.continia.com/images/search_small.png) icon, enter **Assisted Setup**, and select the related link.
2. In the **Continia Finance** section, select **Set up G/L Open Entries**.
3. The wizard will now let you request open entries for one or more G/L accounts and take action on accounts with non-zero balances. If a G/L Account has a balance of zero, any new Ledger Entries made on this account will be treated as G/L Open Entries. If the balance is not equal to zero, you will be prompted to either Open All Entries or Selected Entries.

   If you choose **Selected Entries**, a new page will appear where you can select entries. If the total amount of the selected entries is zero, you can activate the building process. Afterwards, all the selected entries and any new entries will be managed as Open Entries.

To set up the G/L Open Entries module:

1. Use the search icon, enter **G/L Open Entries Setup**, and select the related link.
2. Once you enable the G/L Open Entries Setup, any new Ledger Entries made on G/L Accounts with a zero balance will be treated as G/L Open Entries. However, if the balance is not equal to zero, you will be prompted to either Open All Entries or Selected Entries. There are also additional settings that can be configured.
3. There are also additional settings that can be configured.
   * **Colored Hyperlinks in Report** - enable hyperlinks in reports to appear in blue. You can select the account number to open the G/L Account Card if not enabled.
   * **Prevent two Open G/L Accounts in one Gen. Journal Line** - when you activate this feature, it prevents both the account and balance account from being designated as Open Entry G/L Accounts at the same time. This setting restricts the use of two G/L open accounts for application. Otherwise, an error message will be displayed, indicating that posting two G/L Open Accounts on one general journal line is not permitted, and you will be prompted to split the line into two separate lines.
   * **Use Ledger Entry Comments** - when activated, it lets you use comments to enhance the clarity and context of entries within your G/L, customer, and vendor accounts. 

## To allow open entries for G/L accounts

Once the module is activated and set up, you can create open entries for G/L accounts, like for transit accounts, where pending payments aren't immediately shown in the bank statement.

To allow open entries for a G/L Account, you can:

* Open the **Chart of Accounts**, navigate to the G/L account, and select the checkbox in the **G/L Open Entries** column.
* On the **G/L Account card**, navigate to the **Continia Finance** FastTab and enable **Build Open Entries**.

On the **Finance** FastTab of the G/L Account card, you can also set the following:

* **Open Balance** - specifies the balance of the account. You can click the amount to open the General Ledger Entries page. 

## To deactivate build open entries

If you activate the Build Open Entries option on the G/L account card and later decide to deactivate it, a dialog box will appear asking if you want to stop creating open entries. If you select **Yes**, the system will only deactivate the checkbox if the remaining amount of all entries equals zero. If the remaining amount does not equal zero, an error message will display.

To deactivate open entries for a G/L account:

1. Use the search icon, enter **G/L Open Entries Setup**, and select the related link.

2. On the **General** FastTab, navigate to the **Create Open Entries** field and disable it.

Alternatively, you can open the G/L Account Card, navigate to the Continia Finance FastTab, and disable Build Open Entries there.

