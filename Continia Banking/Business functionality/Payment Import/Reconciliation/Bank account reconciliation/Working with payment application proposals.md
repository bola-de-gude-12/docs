---
title: Working with Payment Application Proposals in Continia Banking
date: 04-02-2025
description: Learn how to review payment application proposals.
id: CB-19
lang: en
---

# Working with payment application proposals

The Payment Application Proposal feature plays a crucial role in the reconciliation process by automatically identifying potential matches between bank statement lines and ledger entries. These proposals contain detailed information about the matches and are generated through automatic matching based on specific criteria. 

On the **Bank Account Reconciliation** page, you can easily see the number of **Payment Application Proposals** associated with each line. If multiple proposals are found but not applied automatically, users have the flexibility to manually apply them. Simply review the proposals and manually apply each proposal as needed. In instances where a Payment Application Proposal is automatically created, and the statement amount matches the remaining ledger entry amount, the automatic application takes place without user intervention.

To access comprehensive details of Payment Application proposals, select the corresponding field, invoking the **Payment Application Review** page to open. You can view, delete, apply, or unapply proposals.

To review a proposal:

1. On the **Bank Account Reconciliation** page, navigate to the line and in the Proposals column, select the number. Alternatively, select the line, and on the action bar, select **Application Proposals**.

2. On the **Payment Application Review** page, you can see a comprehensive overview of the line that is up for reconciliation with general information, proposals, totals, notifications, and more. The following table lists the sections available on the **Payment Application Review** page and their functions:

   | Section                      | Description                                                  |
   | ---------------------------- | ------------------------------------------------------------ |
   | General                      | The general section includes the transaction date, statement amount, description, and account details. You can access specific details of a reconciliation line by selecting **Details**, if available. If there's a discrepancy between the Statement Amount and the Applied Amount, a notification appears on the general tab, alerting users that the difference must be resolved before the line is ready for posting. |
   | Payment Application Proposal | In this section, you can find the proposals identified through automatic matching.  You can apply, unapply, or delete entries, ensuring precise reconciliation. <br />Use the fields to learn more about the details involved with the proposal. For example, the **Found By** field helps you understand how the proposal was identified. This field can have the following values: <ol><li>**Document No.** - identified by document number. </li><li>**External Document No.** - identified by external document number. </li><li>**End To End ID** - a unique ID for payments made with Banking Export. </li><li>**Payment Reference Rule** - identified by a specific [payment reference rule](@CB-164). </li><li>**Manual Application** - when a user manually applies a ledger entry.</li></ol><br />The **Applied Amount** field is highlighted green when it matches the **Statement Amount**. If discrepancies exist, it turns bold and red. |
   | Totals                       | The **Totals** section displays the cumulative figures for the reconciliation line, dynamically recalculating as the user applies, unapplies, or deletes payment application proposals. The **Applied Amount** will turn green if the **Statement Amount** and the **Applied Amount** match. If the difference does not equal zero, the amount displays in bold and red. |
   | Notifications                | The notifications at the top of the **Payment Application Preview** page serve to assist users by providing guidance during the bank statement reconciliation process. For example, if a line displays the status **Awaiting Cash Receipt Journal**, the notification indicates that payment application proposals have been transferred to the cash receipt journal. To reconcile this line, you are prompted to post the relevant entries within the journal. |
   | Related Party Information    | This section of the page displays details provided by the bank regarding the related party involved in the payment, whether it's the recipient or sender. This information is visible only if there is relevant data available from the bank. |
   | Actions                      | On the action bar, select to apply or remove a proposal. You can select multiple lines and apply actions to all of them. |

1. Once you have viewed all the details of the reconciliation line and have found the possible entry to apply, you are now ready to proceed with the reconciliation process. 

    

   
