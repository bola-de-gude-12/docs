---
title: Automatic Import of Credit Card Transactions
date: 17-01-2025
description: An introduction to the automatic import of credit card transactions into Continia Expense Management
id: EM-202
lang: en
---

# Automatic Import of Credit Card Transactions 

Having your credit card transactions automatically imported directly into Continia Expense Management is the straightforward way to optimize your business. It helps you keep track of all employee expenses and credit cards, and is by far the easiest way to get your transactions into Microsoft Dynamics 365 Business Central.

Your options for importing credit card transactions into Expense Management depend on what credit card(s) you use in your organization. Continia supports all major credit cards, including Mastercard, Visa, American Express, and Eurocard, as well as a large number of other types of cards. To learn more about the various options and find out what must be done to set everything in motion, select your type of credit card below:
* [Activating credit card agreements](Activating credit card agreements.md)
* [American Express](Importing American Express transactions.md)
* [Mastercard](@EM-279)
* [Visa](@EM-281)
* [Eurocard](@EM-162)
* [Other cards](Importing transactions from other cards.md)

In general, Continia supports thousands of scenarios and a multitude of banks worldwide. All you need to do is ask your bank to get in touch with [your Continia partner](/Continia Expense Management/Getting Started/Resellers and Partners/Find a Reseller.md), and your partner will take it from there, of course provided that your bank is on board and technically capable of sending transactions to Expense Management.

> [!IMPORTANT]
> If you're unsure as to whether your bank can export transactions to Expense Management, please contact your bank and ask them to reach out to [your Continia partner](/Continia Expense Management/Getting Started/Resellers and Partners/Find a Reseller.md). Your Continia partner will then work with Continia to find the best possible solution for your organization.

## To set up automatic import of credit card transactions

To have credit card transactions imported automatically into Expense Management, follow these steps closely:

1. Contact your bank to set up an agreement for them to send credit card transactions to Expense Management.
   > [!NOTE]
   > An agreement with the bank must be in place before you request activation in Business Central. You can't request a bank agreement from within Business Central.
1. As there are specific procedures for each of the different credit cards, notify your bank that relevant guidelines and information for the different card types can be found using the links below, if necessary:
   * [American Express](Importing American Express transactions.md)
   * [Mastercard](@EM-279)
   * [Visa](@EM-281)
   * [Eurocard](@EM-162)
   * [Other cards](Importing transactions from other cards.md)
1. Wait for confirmation from your bank that the agreement has been activated and the bank has started sending credit card transactions to Continia. Once you've received the confirmation, you're ready to request activation in Business Central.
1. To activate an agreement in Expense Management, follow these steps:
   1. Choose the {{search}} icon, enter **Bank Agreements**, and then choose the related link.
   1. In the action bar, select **Request New Agreement** to open the **Bank Agreement Activation** assisted setup guide.
   1. Select **Next**.
   1. Fill in all fields with the relevant transaction details.
      > [!NOTE]
      > To ensure that the transaction you submit is included in the data sent by your bank to Continia, be sure to select a transaction that was carried out after your bank confirmed that the agreement was activated. Your chosen transaction should have taken place at least 1-2 days after the date when your bank started delivering transaction data to Continia.
      > 
      > Avoid using fees and other generic transactions. The more unique the text and amount are, the better.
      > 
      > If you don't know the last six digits of the card number, entering the last four digits is usually sufficient.
   1. When you've entered all details, select **Next**.
   1. Select **Finish** to close the assisted setup guide.

You've now requested activation of the agreement in Business Central, and your request is sent to Continia for processing. The status of the request is set to **Pending**.

## Viewing the request status and dealing with issues

To view the status of your activation request, go to the **Bank Agreements** page, and from the action bar, select **Activation Request Log** to open the **Agreement Activation Log** page. In the list of requests, locate the one you submitted, and check its status in the **Request Status** column.

When the activation request has been approved, its status will change. Make sure you synchronize with Continia Online before checking the status of your activation request (from the **Bank Agreements** page, select **Force Synchronize with Continia Online**). The status is only updated once you've synchronized with Continia Online. Note that it may take up to 48 hours to process you activation request.

If your activation request status changes to **Rejected**, please go through [the above guide](#to-set-up-automatic-import-of-credit-card-transactions) again to see if you've missed anything.

> [!NOTE]
> By far the most common reason for a rejected activation request is that the submitted transaction occurred before the date when your bank started sending transactions to Expense Management.
> 
> Another common reason is that you haven't received a confirmation from your bank that they've activated the agreement.

If you're still having trouble, please submit a support ticket. Your support ticket must include the following information, as we're unable to assist you without these details:

* Client ID
* Company GUID
* Bank name
* Bank agreement number (supplied by your bank)

> [!TIP]
> Note that many banks use different terms, such as *file delivery ID*, *company ID*, or *recipient ID*.
> 
> For information on how to find client credentials and company GUID, see [How to find Client Credentials and Company GUID](https://continia.zendesk.com/hc/en-us/articles/360020019300-How-to-find-Client-Credentials-and-Company-GUID) (only available to Continia partners).

## Related information
[Importing American Express Transactions](Importing American Express transactions.md)  
[Importing Mastercard Transactions](@EM-279)  
[Importing Visa Transactions](@EM-281)  
[Importing Transactions from Other Cards](Importing transactions from other cards.md)  
[Manual File Import](Manual file import.md)  
[Finding a Reseller of Continia Expense Management](/Continia Expense Management/Getting Started/Resellers and Partners/Find a Reseller.md)  