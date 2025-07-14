---
title: Working with intermediary banks
date: 02-06-2025
description: Learn how to add the details for an intermediary bank.
id: CB-244
lang: en
---

# Working with intermediary banks

An intermediary bank (also referred to as intermediary agent or correspondent bank) is a financial institution that acts as an intermediary between two banks, usually in different countries, to facilitate international transactions. For example, if your bank in the US does not have a direct relationship with a supplier’s bank in Europe, an intermediary bank with accounts at both banks can facilitate the transfer. With Continia Banking, you can enter intermediary bank details to make sure payments are properly routed through intermediary banks when the primary bank cannot transfer funds directly. 

On the **Vendor Bank Account Card**, Continia Banking introduces three fields related to intermediary banks in the **Transfer** FastTab. These fields allow you to record the necessary intermediary bank information for each vendor bank account. Some fields may be hidden by default and can be revealed by selecting **Show more**. 

To add intermediary bank details:
1. Search ({{search}}) for and select **Vendors**.
2. Select a vendor to open the **Vendor Card**. 
3. On the action bar, select **Vendor** > **Bank Accounts**. 
4. Select a bank and on the **Vendor Bank Account Card**, navigate to the **Transfer** FastTab and click **Show more** to display the **Intermediary Bank** section. 
5. You now have access to the following fields:
   - **SWIFT Code** - select the unique SWIFT/BIC code identifying the intermediary bank for secure international transactions.
   - **Bank Name** - this field is automatically filled after selecting the SWIFT Code.
   - **Country/Region Code** - select the country or region where the intermediary bank is located.
6. After you post a purchase invoice, intermediary bank fields remain available for editing if changes are needed. 
   * If **Advanced mode** is activated in **Banking Export Setup**, you can use the payment suggestion feature:
     * On the **Payment Card**, under the **Banks** FastTab, the intermediary bank fields are automatically populated with the details from the vendor bank account. You can modify these fields if needed before finalizing the payment.
   * If Advanced mode is **not** activated, you can open the payment journal:
     * On the **Payment Journal**, suggest payments. You cannot modify the intermediary bank values here. If you must edit these values, delete the line and change the intermediary bank values on the vendor bank account card. 

When you export or send payments, the intermediary bank fields are included in the inhouse payment file. This ensures all necessary intermediary information is transmitted to your bank for processing the international payment.
