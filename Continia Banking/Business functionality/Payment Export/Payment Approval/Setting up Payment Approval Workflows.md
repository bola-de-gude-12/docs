---
title: Creating Payment Approval Workflows in Continia Banking
date: 08-10-2024
description: Walkthrough of how to create and set up workflows using Payment Approval.
id: CB-31
lang: en
---

# Setting up Payment Approval Workflows
With the Security module, you can set up a secure and safe approval process for approving vendor, employee, and customer payments. You can set up one approval workflow per payment journal and specify whether the lines must be approved individually or if the entire batch must be approved as one. You can only set up and use Payment Approval on Continia Banking-enabled payment journals.

> [!IMPORTANT]
>
> Only users with the Admin or SUPER permission set can create or modify payment approval workflows.

## To set up an approval workflow for a payment journal

To create a new approval workflow, you must use the assisted **Set up Security** guide. 

1. Search ({{search}}) for and select **Assisted Setup**. 

1. Scroll to the **Continia Banking** section at the bottom of the page, and select **Set up security**. 

1. If you have enabled **Use Bank Account Verification** in the Banking Export Setup, the first step in the process is to decide how you want to implement bank account verification. The following fields are available for configuration:

    * **Use Bank Account Verification** - if enabled changes to bank account information must be verified before they are approved.
    * **Enable Verifiers to Approve Own Changes** - if enabled, this option allows users to approve the changes they make to bank account information. This goes for users with the CB BANK ACC. VERIF. permission set.
    * **Enable Approval Admins to Approve Own Changes** - if enabled, this option allows the approval administrators to approve the changes they make to bank account information. This goes for users with the CB365 ADMIN permission set.
    * **Block Payment Export** - if enabled, payments will not be exported until the bank account information is verified.

1. On the same page, you can switch on using workflows. 

1. Next, you have the option to verify existing bank accounts. Click **Next** to proceed. 

1. Now select the payment journal batch for which you want to create the approval workflow. 

     Check the **Approval Workflow** column to see if an approval workflow has already been created for the payment journal. If you continue to create a new approval workflow for a payment journal with an existing approval workflow, you'll overwrite the existing workflow. 

1. Next, add the approvers that you want to add to the approval flow. You can only select users already created in the User Setup. For each approver the following settings are optional:

    | Setting                     | Description                                                  |
    | --------------------------- | ------------------------------------------------------------ |
    | Approval Amount Limit (LCY) | Enter the maximum amount the user is permitted to approve. The order of the approvers changes based on the amount, starting with the approver with the lowest amount limit. The default limit is 1.00. |
    | Email                       | Enter or alter the user's email address.                     |
    | Email Notification          | Indicate whether the approver must receive approval request notification emails. The options are: **Never**, **Instantly**, and **Daily**. |

1. In the **Send Approval Requests To** drop-down menu, specify who of the listed approvers should receive the approval request. See the following table for detailed information. 
   <br />

   | Setting                     | Description                                                  |
   | --------------------------- | ------------------------------------------------------------ |
   | All                         | An approval request will be sent to all approvers in the list regardless of their specified approval amount limit. Therefore, when you select this option, any value in the **Approval Amount Limit (LCY)** field will be cleared. This is the default setting.<br />For example, use this setting if you want the payment to be approved by all the approvers on the list. |
   | First qualified             | The approval request will be sent to the first approver with an approval amount limit value that equals or exceeds the total value of the payment journal batch or line submitted for approval.<br /><br />For example, if the approvers are three accountants with different approval amount limits set: $1000, $10,000, and $100,000. If the payment amount is $900, the approval request only goes to the accountant who can approve amounts up to $1000. If the payment amount is $15,000, the approval request goes to the third accountant on the list, who can approve amounts up to $100,000. |
   | All to first qualified      | An approval request will be sent to all approvers in the list, starting with the approver with the lowest amount limit value and ending with the first qualified approver.<br />The approval request will be sent to the first approver with an approval amount limit value that equals or exceeds the total value of the payment journal batch or line submitted for approval.<br /><br />For example, there are three accountants and one manager in the finance department. The approval amounts assigned to each accountant determine how many approvers are needed. The accountants can approve $10,000, $150,000, and $10,000,000 respectively. If the amount is $10,000, only one accountant has to approve the payment, but if the payment amount is higher than $10,000 and below $150,000, a second approver is required. If the payment amount exceeds $150,000, three accountants must approve the payment. |
   | Initial and first qualified | An approval request is sent to the approver with the lowest amount limit value and the first qualified approver.<br />The approval request will be sent to the first approver with an approval amount limit value that equals or exceeds the total value of the payment journal batch or line submitted for approval.<br /><br />For example, if there are three accountants and the head of administration in the finance department. Each accountant is responsible for a different approval amount, and the head of administration must approve every payment. Suppose you now specify different amounts for each accountant (e.g., $1000, $10,000, $100,000) and $1 for the head of administration. In that case, the approval request for every payment goes to the head of administration and the first eligible accountant. |
   | All up to limit             | This setting dictates the required number of approvals for a journal batch or individual lines. Contrary to the sequential All method, the All up to limit option streamlines approval requests by sending them simultaneously to all designated approvers. For instance, if two accountants and a CEO are assigned, but the Required No. of Approvers is set to two, the CEO's approval becomes redundant once both accountants approve. Approval occurs promptly upon meeting the specified approval count.<br/><br/>Upon reaching the approval limit, all pending requests are automatically approved and labeled as Approval completed by %1, Required number of approvals reached, signifying fulfillment of the required approvals. |

   <br />

1. If you choose the **All up to limit** approval method, go to the **Required No. of Approvers** field, and specify the exact number of approvers you require.

1. Next, specify the following settings for the approval workflow.

   | Setting                                    | Description                                                  |
   | ------------------------------------------ | ------------------------------------------------------------ |
   | Approval Type                              | Select **Journal Batch Approval** if you want users to request approval of all the lines in the journal batch combined. All journal lines must be valid before sending the approval request for batch approval to work. To post the payment of a batch, all lines must have status paid or sent. <br /><br />Select **Journal Line Approval** if you want users to request approval for each individual journal line. |
   | Field Restriction                          | Select whether you want to lock fields to make sure data is not changed while the payment is in the approval process. The options are: **All Fields** or **Sensitive Fields** only (e.g.: Name, Address, IBAN, SWIFT, Currency Code, Branch No., and Account No). <br /><br />If switched on, a user who tries to change a field that is part of a payment in the approval process receives an error message. |
   | Max. Amount (LCY) Allowed Without Approval | Specify the maximum amount of a journal batch or line (depending on the specified approval type), up to which the payments can be exported to the bank without approval. |

   <br />

   On the last step of the assisted guide, select **Finish** to save your changes and close the assisted setup guide.

> [!TIP]
>
> You can also access the assisted **Set up approval workflows** guide from the Payment Journal Setup page. From the actions menu, select **Actions** > **Workflow** > **Setup Approvals**.



## To set up mandatory payment approval on a bank account

In addition to setting up the payment journal to require payment approval, you can also ensure that a payment can never be made from a specific bank account without approval. In this way, a payment from that bank account can never be made from a payment journal that doesn't have Payment Approval set up. 

1. Search ({{search}}) for and select **Bank Accounts**. 
2. Select the relevant bank account.
3. On the **General** FastTab, enable the **Mandatory Payment Approval** setting. 







<style>
  .content table tr td:nth-child(1) {
    width: 150px;
  }
  .content table tr td:nth-child(2) {
    width: 580px;
  }  
</style>
