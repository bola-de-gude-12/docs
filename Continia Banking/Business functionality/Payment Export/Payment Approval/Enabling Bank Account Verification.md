---
title: Enabling bank account verification in Continia Banking
date: 24-02-2025
description: Use trusted bank accounts for secure payments. 
id: CB-30
lang: en
---

# Enabling Bank Account Verification

To enhance the security of Continia Banking processes, you can enable bank account verification within the Security module. By activating bank account verification, you can monitor the verification status of bank accounts and track the updates made to account details, such as changes in bank account number, IBAN, and SWIFT. This can help identify any suspicious activities or discrepancies in the account and lets you take necessary actions to ensure the safety and security of the account, safeguarding against fraud. 

Once the Security module is activated in Continia Banking, the **Use Bank Account Verification** field will be visible in the Continia Banking Setup. If this option is enabled, payments can't be approved for unverified bank accounts.

## Requirements

The minimum requirements for setting up Bank Account Verification are:

* Payment Approval Workflow module activated.
* Permission set requirements - to enable and apply bank account verification, users must have one of the following permissions sets: 
  * CB BANK ACC. VERIF.
  * CB Admin
  * Admin
  * SUPER

## To enable bank account verification

In the Continia Banking Setup, you can enable bank account verification to secure your payment approval process, providing added protection by preventing unverified bank accounts from being approved or processed for payments. 

To enable bank account verification using the assisted setup:

1. Search ({{search}}) for and select **Assisted Setup**.
2. In the **Continia Banking** section, select **Set up Security**.
3. The wizard will now let you enable Bank account verification. 

To enable bank account verification:

1. Search ({{search}}) for and select **Banking Export Setup**.
2. On the **Approval** FastTab, navigate to **Use Bank Account Verification** and enable it. 
   
   > [!TIP]
   >
   > You can now choose to trust all banks you've used in previous payments. Opting for **Yes** will assign the **Verified** status to these bank accounts, saving you time.
   

If for verified banks one of the following fields is changed, the **Verified** status will be revoked, and re-verification is necessary:
   * Bank Branch No.
   * Bank Account No.
   * IBAN
   * Swift Code
   * Transit No.
   * Bank Clearing Code

## To verify a new bank account

Once bank account verification is activated, you will be made aware of bank accounts that are new or accounts with changes. 

To verify a new bank account:

1. Open the Vendor Bank Account Card, Customer Bank Account Card, or Employee Card that you want to verify, and on the action bar, select **Verify Bank Account**.
2. On the **Bank Account Verification** page you can now check the bank accounts most important fields. 
3. If you trust the bank account, and want to assign the **Verified** status, go to the **Verification Method** field and select one of the following options:
   * Email
   * Phone
   * Other
4. Optionally, you can use the **Comments** field for additional information. 
5. Select **Ok** to confirm the bank account information.

## To view the verification status of bank accounts

Once you enable the Bank Account Verification feature and assigned statuses to bank accounts, the following statuses are visible on for example Payment Journals and Payment Approval Entries:

* **New Bank Account** - indicates whether any prior payments were made to this account using its current details.
* **Bank Account Verification Status** - indicates the current verification status of this bank account.

These columns help you give insight in security of the bank accounts you are working with. For example, when on a payment line, the **New Bank Account** column is unchecked, you already made payments to this bank account and trust it. If the **New Bank Account** column is checked and the **Bank Account Verification Status** is on *Pending Verification*, probably because the account specifications changed and verification is revoked.

## To view the verification status history of bank accounts

The ability to track the verification status history of bank accounts provides valuable insights into changes in their specifications over time. By monitoring the verification status of bank accounts, you can track the updates made to account details, such as changes in bank account number, IBAN, and other relevant details. This can help in identifying any suspicious activities or discrepancies in the account, and take necessary actions to ensure the safety and security of the account.

To view the verification status history:

* Open the Vendor Bank Account Card, Customer Bank Account Card, or Employee Card that you want to verify and on the action bar, select **Verification History**. On the **Bank Account Verification Entry** page, you can see a a list of all the verifications for this bank account. It includes the actual change made to the bank account in the **Field** and **Value** field and information about the user who validated the change.

