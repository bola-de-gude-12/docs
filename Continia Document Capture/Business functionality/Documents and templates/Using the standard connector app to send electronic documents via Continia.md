---
title: Using the standard connector app to send electronic documents via Continia
date: 26-08-2025
description: How to configure Continia's E-Document Connector application.
id: DC-173
lang: en
---

# Using the standard connector app to send electronic documents via Continia

Microsoft Dynamics 365 Business Central includes a standard connector app that allows you to send electronic documents without relying directly on third-party extensions.

One of these possibilities available via the connector is **E-Document Connector - Continia**, which uses Continia as the eDocument service provider and is available on the **Extension Management** page.

For more information, see [Connectors overview](https://learn.microsoft.com/en-us/connectors/overview) (Microsoft article).

## Considerations when using the connector

* The configuration uses standard Business Central logic to generate XML documents, not Continia apps. Continia only acts as the transportation layer, ensuring documents move from Business Central through the electronic network to the recipient – and vice versa.
* Participation approval takes approximately 1-2 working days. To check the approval status, go to **E-Document Services > Continia > Set up service integration > No. of Participations > Registration Status**.
* The recipient is responsible for handling the receiving side.

## To set up the E-Document Connector - Continia

The following steps describe how to configure Continia as the standard service provider for electronic document formats using the standard connector.

1. Search ({{search}}) for and select **Extension Management**, then search for and install **E-Document Connector - Continia**.
2.	Create an e-document service by following Microsoft’s documentation, then select **Continia** in the **Service Integration** field.
3.	On the action bar, click **Set up service integration** and, on the **Continia E-Document External Connection Setup** page, click **Register** new participation on the action bar to begin the onboarding process.
   >[!NOTE]
   >You must repeat this process to register additional participations. For example, once to register Peppol and another to register NemHandel.
   
4.	Enter your partner’s PartnerZone credentials. This is only required when you first go through the onboarding.
5.	Enter your company’s legal information. Make sure that this information is accurate, as it’s validated via KYC procedures.
6.	Enter your company’s billing details. If you need to edit this at a later date, go to **E-Document Services > Continia > Set up service integration > Subscription > Edit**.
7.	Select the document types you would like to send and receive. If unsure, select all available types.
8.	**OPTIONAL:** If you need more granularity, click **Advanced Setup** to select the desired network profiles and associate an e-document service code to each one of them. You can also do this after completing the onboarding guide by editing the participation.
9.	After completing the onboarding, return to the created e-document service page (e.g.: CONTINIA) and select the value of the **No. of Network Profiles** field under the **General** FastTab.
10.	In the **E-Document Service Network Profiles** dialog box, click **Add** on the action bar. For each network in which you participate (e.g.: Peppol, NemHandel), you must configure e-document services because each service can only handle one format. E.g.: If you setup an e-document service that sends and receives XRechnung documents, select XRechnung profiles.
11.	Return to the **E-Document Service** page and, on the action bar, click **Configure documents to export**. Check the list of source document types and, if needed, add types by clicking **New** on the action bar.

>[!TIP]
>For information on how to set up sending profiles and workflows, see [Set up e-documents](https://learn.microsoft.com/en-us/dynamics365/business-central/finance-how-setup-edocuments) (Microsoft article).

## To edit a connector participation

To edit a participation that’s already set up in the connector:

1.	Search ({{search}}) for and select **E-Document Services**.
2.	Click the code of the desired service. E.g.: CONTINIA.
3.	On the action bar, click **Set up service integration**.
4.	Click the value in the **No. of Participations** field, then click **Edit** on the action bar.
5.	Enable the I confirm toggle at the bottom of the dialog box, then click **Next**.
6.	Apply the required changes.
