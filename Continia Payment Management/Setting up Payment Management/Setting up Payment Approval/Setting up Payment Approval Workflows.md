---
title: Creating Payment Approval Workflows in Payment Management
date: 30-09-2022
description: Walkthrough of how to create and set up workflows using Payment Approval.
id: PM-254
lang: en
---

# Setting up payment approval workflows
> [!NOTE]
>
> If you're using the on-premises version of Business Central (version 18 or later is required), ask your Continia partner to add the [relevant license granule](@PM-18) to your license file.

With the Payment Approval module, you can set up a secure and safe approval process for approving vendor, employee, and customer payments. You can set up one approval workflow per payment journal and specify whether the lines must be approved individually or if the entire batch must be approved as one. You can only set up and use Payment Approval on Payment Management-enabled payment journals.

> [!IMPORTANT]
>
> Only users with the CPM365 APPRADMIN or SUPER permission set can create or modify payment approval workflows.



## To set up an approval workflow for a payment journal

To create a new approval workflow, you must use the assisted Payment Approval Workflow Setup guide. 

1. Use the ![Search for page or report](/images/search_small.png) icon, search for **Assisted Setup** and select the related link. 

1. Scroll to the **Continia Payment Management** section at the bottom of the page, and select **Set up approval workflows**. 

1. In the first step of the guide, select the payment journal batch for which you want to create the approval workflow. 

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
   | All up to limit             | This setting determines the number of approval requests necessary to approve a journal batch or individual lines. The "All until limit" option introduces a different approach to approval requests than the "All" method. <br />With the "All" method, approval requests are sent in sequence. For example, if two accountants and a CEO are designated approvers, the CEO will only receive an approval request after the first two accountants have already approved. If either of the accountants declines the request, the CEO will not be involved in the process. <br />Using the "All until limit" method, all designated approvers receive notifications simultaneously. The  "Approval Limit" field indicates the number of approvals needed to authorize the entire request. For example, if there are two accountants and a CEO assigned for approval, but the "Required No. of Approvers" is set to two, the CEO's approval becomes unnecessary once both accountants approve the request. Approval is granted as soon as the required number of approvals is reached. |

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

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Bank Accounts**, then select the related link. 
2. Select the relevant bank account.
3. On the **General** FastTab, enable the **Mandatory Payment Approval** setting. 



## Related information

[Editing payment approval workflows](@PM-255)  
[Working with payment approvals](@PM-256)     



<style>
  .content table tr td:nth-child(1) {
    width: 150px;
  }
  .content table tr td:nth-child(2) {
    width: 580px;
  }  
</style>
