---
title: Setting up bank accounts in the Export Module
description: How to activate and set up a bank account.
date: 01-10-2024	
id: CB-37
lang: en
---

# Setting up bank accounts

To fully use Continia Banking features, your company’s bank accounts must be configured using the assisted bank account setup. Continia supports both manual file exchange and direct communication between Business Central and your bank. Direct communication enables automated data exchange through web services, eliminating the need for file imports and exports. Note that this depends on whether your bank supports the direct communication method.

When you configure a bank account with Continia Banking, it automatically creates the corresponding bank and bank system in Business Central. The bank system defines how the data is validated and processed during import/export.

To activate and set up a bank account:

1. Select **Activate** on the notification to activate the company.
2. After activating, the Bank Account Setup wizard opens to guide you through the next steps. On the **Bank Accounts Setup** page, select the bank account that you want to set up for Banking. Alternatively, search ({{search}}) for and select **Assisted Setup**. Scroll down to the Continia Banking section and select **Set up bank accounts**. 
3. Go to the **Communication type** columns, select one of the following options, and click **Next**:
   * **Direct** - select this option for automated communication between Business Central and your bank. This method ensures real-time integration without manual file handling.
   * **Manual** - select this option if you prefer or require traditional file-based communication. 
   * **Storage Account** - select this option if your bank delivers files via cloud storage. 
4. Enter the IBAN and any other required bank information, then select **Next**. Use the details provided by your bank, as the specific information required may vary depending on the bank you are connecting to. For additional information about specific banks, refer to the documentation in the [Banks section](@CB-79).
5. If the bank is not supported, you can choose to receive email notifications about possible support in the future. Click **Next**.
6. Select **Finish**. After you've set up the bank account, the status in the **Bank Accounts** overview will be set to *Ready*, and the bank account will be ready for use.

