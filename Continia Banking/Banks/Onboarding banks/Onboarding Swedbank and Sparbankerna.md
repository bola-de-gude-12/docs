---
title: Onboarding Swedbank and Sparbankerna
description: Onboarding Swedbank and Sparbankerna with direct communication
date: 24-05-2025
id: CB-239
lang: en
---

# Onboarding Swedbank and Sparbankerna

To onboard for direct communication with **Swedbank** or **Sparbankerna** in Sweden, there are two required steps that must be completed in order:
1. **Request an ISO agreement** from the bank.
2. **Set up the connection** using the Continia Banking Assisted Setup.

> [!NOTE]
>  It may take approximately **1–3 days** after the agreement is established for the bank integration to become active.

## To request an agreement
To request an agreement:
1. **Contact your bank representative** at Swedbank or Sparbankerna via phone or email to initiate an **ISO Agreement** for the Continia Banking solution.
2. Sign the agreement on paper or via e-signature. Once the agreement is completed, the bank will email the following details to your contact email:
   - **Payment Agreement (B-avtal)** – Bank Agreement Number
   - **Reporting Agreement (R-avtal)**
   - Additional key information: **Corporate ID**, **Contact Email**, **Bank Agreement Number**


> [!NOTE]
>  If you are onboarding multiple legal entities, this information can differ per company. Always confirm you have the correct data for the correct company. An incorrect match will prevent the connection from being established.

## To set up direct communication

To set up direct communication using the Continia Banking Assisted Setup:
1. Search ({{search}}) for and select **Bank Account Setup**.
2. Select a bank account from Swedbank or Sparbankerna, and select **Next**.
3. Select **SWEDBANKISO20022** as the Bank System and select **Next**.
4. When prompted, enter the following information exactly as provided by the bank:
   - **Corporate ID**
     - Must match the ID from the bank. This identifier is always 12 digits long, consisting of a 2-digit prefix followed by the 10-digit corporate ID.
     - The initial zero and hyphen will be removed automatically
     - *Example: 123456789123*
   - **VAT Registration Number**
     - Specific to the company being onboarded
   - **Contact Email**
     - Must match the email address used in the ISO agreement
   - **Company Name**
     - Must be entered exactly as registered with the bank
   - **Bank Agreement Number**
     - Must match exactly
     - Format: 16 characters ending in **B001**
     - *Example: 123456789123B001*
5. Click **Next** to complete the setup.

The status will display as one of the following:
- **Pending**
  - Bank has not yet activated the connection (allow 1–3 days), or
  - Information entered does not exactly match the bank's records (Corporate ID, Contact Email, Agreement Number)
- **Active**
  - The integration is complete and you can now export payments and import bank statements via Continia Banking.