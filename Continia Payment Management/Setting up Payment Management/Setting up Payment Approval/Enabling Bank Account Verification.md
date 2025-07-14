---
title: Enabling bank account verification Payment Management
date: 03-04-2024
description: Use trusted bank accounts for secure payments. 
id: PM-350
lang: en
---

# Enabling Bank Account Verification

To enhance the security of Payment Management processes, you can enable bank account verification within the Payment Approval module. By activating bank account verification, you can monitor the verification status of bank accounts and track the updates made to account details, such as changes in bank account number, IBAN, and SWIFT. This can help identify any suspicious activities or discrepancies in the account and lets you take necessary actions to ensure the safety and security of the account, safeguarding against fraud. 

Once the Payment Approval module is activated in Payment Management, the **Use Bank Account Verification** field will be visible in the Payment Management Setup. If this option is enabled, payments can't be approved for unverified bank accounts.

## Requirements

The minimum requirements for setting up Bank Account Verification are:

* Payment Approval Workflow module activated.
* Permission set requirements - to enable and apply bank account verification, users must have one of the following permissions sets: 
  * CPM BANK ACC. VERIF.
  * CPM Admin
  * CPM365 APPRADMIN
  * SUPER

## To enable bank account verification

In the Payment Management Setup, you can enable bank account verification to secure your payment approval process, providing added protection by preventing unverified bank accounts from being approved or processed for payments. 

If for verified banks one of the following fields is changed, the **Verified** status will be revoked, and re-verification is necessary: Bank Branch No., Bank Account No., IBAN, Swift Code, Transit No., and Bank Clearing Code.

To enable bank account verification:

1. Use the search icon, enter **Payment Management Setup**, and select the related link.
2. On the **Purchase and Payment** FastTab, navigate to **Use Bank Account Verification** and enable it. 

   > [!TIP]
   >
   > You can now choose to trust all banks you've used in previous payments. Opting for **Yes** will assign the **Verified** status to these bank accounts, saving you time.

3. Alternatively, you can use the Payment Approval Assisted Setup to not only enable bank account verification but to also determine whether users and administrators can verify their own changes. To do that, use the {{search}} icon, enter **Assisted Setups**, and select **Payment Approval Setup**. 

4. The following fields are available to determine how you want to apply bank account verification:

   * **Use Bank Account Verification** - if enabled changes to bank account information must be verified before they are approved. 
   * **Enable Verifiers to Approve Own Changes** - if enabled, this option allows users to approve the changes they make to bank account information. This goes for users with the CPM BANK ACC. VERIF. permission set. 
   * **Enable Approval Admins to Approve Own Changes** - if enabled, this option allows the approval administrators to approve the changes they make to bank account information. This goes for users with the CPM365 APPRADMIN permission set.
   * **Block Payment Export** - if enabled, payments will not be exported until the bank account information is verified.

## To verify bank accounts

Once bank account verification is activated, you will be made aware of bank accounts that are new or that changed their settings. 

To verify a new bank account:

1. Open the Vendor Bank Account card, Customer Bank Account card, or Employee card that you want to verify, and on the action bar, select **Verify Bank Account**.
2. On the **Bank Account Verification** page you can now check the bank account's most important fields. 
3. If you trust the bank account, and want to assign the **Verified** status, go to the **Verification Method** field and select one of the following options: Email, Phone,  Other.
4. Optionally, you can use the **Comments** field for additional information. 
5. Select **Ok** to confirm the bank account information.

Depending on the settings in the [Payment Approval Setup](@PM-350#to-enable-bank-account-verification), users are allowed to verify changes to bank account information. If the **Enable Verifiers to Approve Own Changes** option is disabled and a user updates a vendor's bank account number, then any other user who checks that vendor's bank account card will see a message notifying them that the information has been changed by another user. The user can then choose to approve or reject the change. If they reject it, then the information will be reverted to the last approved version.

![](/images/PM365/verification.png)

## To view the verification status of bank accounts

Once you enable the Bank Account Verification feature and assigned statuses to bank accounts, the following statuses are visible on for example Payment Journals and Payment Approval Entries:

* **New Bank Account** - indicates whether any prior payments were made to this account using its current details.
* **Bank Account Verification Status** - indicates the current verification status of this bank account.

These columns help you give insight in security of the bank accounts you are working with. For example, when on a payment line, the **New Bank Account** column is unchecked, you already made payments to this bank account and trust it. If the **New Bank Account** column is checked and the **Bank Account Verification Status** is on *Pending Verification*, probably because the account specifications changed and verification is revoked.

## To view the verification status history of bank accounts

The ability to track the verification status history of bank accounts provides valuable insights into changes in their specifications over time. By monitoring the verification status of bank accounts, you can track the updates made to account details, such as changes in bank account number, IBAN, and other relevant details. This can help in identifying any suspicious activities or discrepancies in the account, and take necessary actions to ensure the safety and security of the account.

To view the verification status history:

* Open the Vendor Bank Account card, Customer Bank Account card, or Employee card that you want to verify and on the action bar, select **Verification History**. On the **Bank Account Verification Entry** page, you can see a a list of all the verifications for this bank account. It includes the actual change made to the bank account in the **Field** and **Value** field and information about the user who validated the change.

