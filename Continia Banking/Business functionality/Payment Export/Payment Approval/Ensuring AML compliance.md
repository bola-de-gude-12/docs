---
title: Ensuring AML Compliance in Continia Banking
date: 17-03-2025
description: Learn more about how Continia Banking helps you adhere to Norway's Anti-Money Laundering act.
id: CB-211
lang: en

---
# Ensuring AML compliance in Continia Banking

Continia Banking prioritizes security and compliance, ensuring full adherence to Norway's Anti-Money Laundering (AML) act. To meet regulatory requirements, the system allows identity information to be attached to each payment, ensuring that every transaction can be traced back to the individual responsible for initiating it within their organization.

> [!IMPORTANT]
>
> Continia Banking obscures the Social Security Numbers (SSNs) in user interfaces while retaining their full values in the File Archive.

## To set up an approval workflow set up for the payment journal

To comply with AML regulations, a payment approval workflow must be set up for the payment journal. Without this workflow, payments cannot be processed in compliance with AML requirements.

Payment Approval workflows can be created for Continia Banking-enabled payment journals and set up to require approval of either the payment journal batch combined or the individual lines. 

You can use the **Security Setup** Assisted Setup to configure approval workflows for a journal. If a Payment Approval workflow has been created for a payment journal, all payments must be sent for approval before they can be sent to the bank. Additionally, complying to AML regulation means [entering an identification number for the approver](#to-add-approver-identity-information-for-approvers), which can be a SSN or a national ID. 

Depending on the bank, multiple approvers with a SSN may be required. Refer to the Payment Approval Workflow documentation for detailed setup instructions.

## To add approver identity information for approvers

To comply with the AML Act, any user authorized to send payments must enter their Social Security Number (SSN) on the **User Setup** page. 

To add the SSN to the User Setup:
1. Search ({{search}}) for and select **User Setup. 
2. Navigate to the user that you want to add the SSN for and in the **Debtor Approver ID** field enter the number. To protect sensitive information, the SSN is masked upon entry for security. Please note that this number will be shared with the bank to comply with the AML regulations. 

> [!NOTE]
>
> In some cases, banks also require the Business Central GUID (Globally Unique Identifier), a unique identifier assigned to each user in the system. In this case, Continia Banking sets it up for the bank, and it is automatically sent.

## To enable AML compliance on the Bank Card
If the bank supports AML compliance, on the **Bank Card** page, under the **General** FastTab, within the **Anti-Money Laundering Compliance** section, you can enable **Pre-approve Payments**. 

