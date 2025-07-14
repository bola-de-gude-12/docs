---
title: Adding a Payment Service Agreement to Continia Banking
date: 31-03-2025
description: Describes how to set up Payment Service Providers and their PSP agreements to help you differentiate between multiple payment streams for a PSP. 
id: CB-181
lang: en
---

# Setting up a payment service agreement

Continia Banking supports file imports from third-party payment service providers (PSPs), including eCommerce marketplaces (such as bol.com) and payment services (such as PayPal and Klarna). Continia Banking includes preset PSPs that you can configure by adding agreements. PSP agreements help you differentiate between multiple payment streams for a PSP. For example, you can apply different bank accounts or general ledger (G/L) accounts for posting fees.

> [!TIP]
>
> We continuously add support for new PSPs. If your preferred PSP is not listed, contact us to learn more about available options.

Before you can import PSP payments into cash receipt journals, you must add and configure a PSP agreement first. 

> [!NOTE]
>
> You can enable the Payment Service Provider module from the **Continia Feature Management** page. 

To set up a PSP agreement:

1. Search ({{search}}) for and select **PSP Agreement Setup**.
2. On the **PSP Agreement Setup** page, select **Next**.

3. On the **PSP Agreement** **Setup** page, add a new line, enter the following details, then click **Next**:

     * **Name** - enter a name for the PSP agreement. *(Required)*
     * **Payment Service Provider** - select the PSP code to link the agreement to the provider. You may be prompted to select how to import the rules:
          - Import the rules from the default rule template - this option applies a predefined set of rules based on the system’s default template. 
          - Import the rules from an existing PSP Agreement - this option copies the rules from an already established PSP Agreement.
     * **Bal. Account Type** - specify the account type associated with the PSP (Bank Account or G/L Account).
     * **Bal. Account No.** - select the bank account number to use as the balancing account in the cash receipt journal. *(Required)*
4. Configure **PSP External Reference Rules** to match imported transactions to ledger entries. Continia provides default reference rules in the **PSP Search Rule Template**. You can also define custom rules. These rules can be configured for ongoing sales orders, invoices, and credit memos, as well as for customer ledger entries and posted sales invoices and credit memos.
5. Configure PSP reconciliation settings and select **Next**:
   - **Extended Search** - enable to expand the search criteria to improve transaction matching by considering the reference number, posting date, and amount.
   - **Posting Date Tolerance** - defines the number of days allowed for variations in the posting date when matching transactions.
   - **Default Currency Code** -  sets the default currency for transactions when the imported file does not specify a currency code.
   - **Default Customer No.** - assigns a default customer number when the system cannot match the transaction to an existing customer.
6. Adjust PSP search rules if needed. To disable a rule, select the **Disable** field. Ensure that each rule has an associated **Account No.** On the action bar, select **Edit** to open the PSP Search Rule page. This page gives you access to more settings. 

     > [!NOTE]
     >
     > The PSP Search Rule Template includes fields for common invoice separations. If you need additional fields, you can create a custom rule.

7. Select **Finish** to complete the setup or **Next** to add another PSP agreement.

## Related information

[bol.com](@CB-174)  
[Buckaroo](@CB-253)  
[Klarna](@CB-175)  
[PayPal](@CB-172)  
[Adyen](@CB-173)  
[Mollie](@CB-176)  
[Worldline](@CB-180)  
[NetsEasy](@CB-179)  
[MultiSafepay](@CB-177)  

