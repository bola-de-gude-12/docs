---
title: Reviewing remittance advice setups
description: Learn how reviewing the Remittance Advice Setup Check Page helps ensure accurate configurations and reduce errors. 
date: 11-06-2025	
id: CB-246
lang: en
---

# Reviewing remittance advice setups

After completing payments, you can generate the remittance advice to notify recipients of the payment details. Accurate remittance information is essential for ensuring that payment notifications are sent correctly and can be matched with the corresponding invoices. Misconfigured setups can lead to failed notifications, missing details, or delays in reconciliation. 

To help identify and resolve such issues efficiently, Continia Banking includes a dedicated **Remittance Advice Setup Check** page that lists the results of automatic checks and guides you through the necessary corrective actions. 

Use the **Remittance Advice Setup Check** page when:
* Remittance advices fail to send.
* Vendor or customer setups are incomplete.
* Errors appear during payment export or validation.
* You need a quick health check of remittance configurations.

>[!NOTE]
>Warnings related to remittance advice do not block payment processing. All issues can be addressed after payment processing, ensuring that payment operations to proceed uniterrupted while maintaining accurate remittance records.

The **Remittance Advice Setup Check** page allows you to activate and manage a series of configuration checks related to remittance notifications. By enabling these checks, you can verify that your setup is correct and identify any areas that require attention.

To enable remittance checks:

1. Search ({{search}}) for and select **Remittance Advice Setup Check**. Alternatively, you can open the page from:
   * The **Continia Banking Setup**: on the Continia Banking Setup page, open the Troubleshooting page, and on the action bar, select **Actions** > **Export Remittance Advice Setup Check**. 
   * The **Suggestion validation** - when using the advanced mode of banking export, enhanced suggestion validation is available. On the Payment Card, in the **Payment Suggestion Errors** section, click the error to view more details. This opens the Remittance Advice Setup Check page.
   * The **Remittance Advice Outbox** - on the action bar, select **Setup** > **Export Remittance Advice Setup Check**. For more information, see the [Working with the Remittance Advice Outbox](@CB-249) article.
2. On the **Remittance Advice Setup Check** page, the following checks are listed:
   * **Email Account Setup Check** - verifies whether an active email account is configured. If no valid email account is found, remittance notifications cannot be sent via email.
   * **Mail Account Setup Check** - verifies that all accounts have the necessary remittance information, such as recipient email addresses and banking  export configurations. Accounts missing required information are listed for your review and correction.
   * **Report Selection Setup Check** - confirms that the default remittance report is available and correctly configured. This report is automatically configured initialization of Banking Export but if you changed the settings and the report selection is missing  or modified, you will be alerted. This check is run in the background by default.
   * **Custom Report Selection Setup Check** - verifies that any custom report selections are  properly configured and flags any missing or incomplete setups.
3. On the action bar, the **Setups** and **Accounts** tabs offer you direct access to the pages for which issues are identified. For example, go to **Accounts** > **Show Vendors** to see vendors missing an email address. Only relevant actions are enabled.
4. After making changes, re-run the troubleshooting page to confirm issues are resolved.

Regularly reviewing the **Remittance Advice Setup Check** page and [Remittance Advice Outbox](@CB-249) helps ensure accurate configurations and reduce errors. 