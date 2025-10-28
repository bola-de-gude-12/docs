---
title: Setting up the SimplerInvoicing format in eDocuments
date: 30-09-2025
description: How to set up the SI-UBL format in Continia eDocuments.
id: DC-489
lang: en
---

# Setting up the SimplerInvoicing format in eDocuments

This article describes how to configure your setup to send and receive electronic documents in the Dutch SI-UBL format, also known as SimplerInvoicing.

## To add SI-UBL to Document Capture

To start sending and receiving electronic documents in the SI-UBL format:

1.	Search ({{search}}) for and select **Set Up Document Capture**.
2.	In the dropdown list by the **Action** field, select **Import Configuration**.
3.	In the dropdown list by the **Import from field**, select **Online**.
4.	In the **Localization** field, make sure that NL (i.e.: Netherlands) is selected.
5.	Click **Next** and wait for the system to import the configuration.
6.	Look for **SIUBL2** under the **Name** column of the **Select what to include** table, and select the corresponding electronic formats under the Include column.
7.	Click **Next**, then click **Finish**.

## To register the SimplerInvoicing profiles

1.	Search ({{search}}) for and select **Continia Delivery Network Participations**.
2.	On the **Continia Delivery Network Participations** page, select the desired participation and, on the action bar, click **Edit**.

   >[!NOTE]
   >If you don’t have any valid participations set up, see [Setting up the Continia Delivery Network](@DC-75).

3. In the **Continia Delivery Network Onboarding** assisted setup guide, click **Next** until you reach the **Peppol Registration** step.
4.	At the bottom of the dialog box, select the SI-UBL 2.0 Invoice and SI-UBL 2.0 Credit Note profiles. For each selected profile, you must also select a profile role (i.e.: customer, supplier, or both).
5.	Click **Next**, then click **Finish**.

## To exchange SimplerInvoicing documents

1.	Search ({{search}}) for and select **Customers** or **Vendors**.
2.	Click the desired customer or vendor to open its card.
3.	On the **eDocuments** FastTab, click the three dots by the **Electronic Format** field and select **SIUBL2**.
4.	Click **OK**.
