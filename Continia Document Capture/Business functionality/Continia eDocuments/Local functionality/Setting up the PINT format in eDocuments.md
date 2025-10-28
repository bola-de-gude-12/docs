---
title: Setting up the PINT format in eDocuments
date: 15-10-2025
description: How to start sending and receiving electronic documents in the PINT format.
id: DC-464
lang: en
---

# Setting up the PINT format in eDocuments

This article describes how to configure your setup to send and receive electronic documents in the PINT format.

>[!NOTE]
>The minimum versions of Continia Document Capture required to use PINT are 25.3 and 26.1.

## To add PINT to Document Capture

To start sending and receiving electronic documents in the PINT format:
1.	Search ({{search}}) for and select **Set Up Document Capture**.
2.	In the dropdown list by the **Action** field, select **Import Configuration**.
3.	In the dropdown list by the **Import from** field, select **Online**.
4.	If the default localization is incorrect, select the correct one in the dropdown list by the **Localization** field.
5.	Click **Next** and wait for the system to import the configuration.
6.	Look for **PINT** and **PINTANZ** under the **Name** column of the **Select what to include** table, and select the corresponding electronic formats under the Include column.
7.	Click **Next** > **Finish**.

## To register the PINT A-NZ profiles

1.	Search ({{search}}) for and select **Continia Delivery Network Participations**.
2.	On the **Continia Delivery Network Participations** page, select the desired participation and, on the action bar, click **Edit**.

   >[!NOTE]
   >If you don’t have any participations set up, refer to [Setting up the Continia Delivery Network](@DC-75).

3.	In the **Continia Delivery Network Onboarding** assisted setup guide, click **Next** until you reach the **Peppol Registration** step.
4.	At the bottom of the page, add a row to the table and, under the **Type**, column, select **Group**.
5.	Under the **Code** column, add **PEPPOL PINT A-NZ**.
6.	Under the **Document Category** column, select the category to be associated with the new group.
7.	Under the **Profile Direction** column, select **Both** so you can send and receive documents in this format. 
8.	Click **Next** > **Finish**.
