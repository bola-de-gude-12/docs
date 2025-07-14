---
title: Setting up customers and vendors for Continia eDocuments
date: 19-03-2025
description: How to set up customers and vendors to use Continia eDocuments.
id: DC-180
lang: en
---

# Setting up customers and vendors for Continia eDocuments

Once you've [activated Continia eDocuments](@DC-178) and [set it up](@DC-179), you must set up your vendors and/or customers to use it. This process is described in the sections below.

## eDocument receiving capabilities

Although you can take for granted the fact that a customer or vendor you're doing business with is able to physically receive documents, it's not always clear if they can also receive eDocuments. However, Continia eDocuments allows you to do just that: check if the customer/vendor you need to send an eDocument to is capable of receiving it.

To enable this feature:

1. Choose the {{search}} icon, enter **Continia eDocuments Setup**, and then choose the related link.
2. On the **Automations** FastTab, enable the setting under **Update Documents Receiving Capabilities**.
3. The status of **Update Documents Receiving Capabilities** changes to **Ready**, indicating that the task responsible for updating the eDocuments participation cache is running.

You can now verify if a customer or vendor is part of an eDocuments network. The instructions below use vendors as an example:

1. Choose the {{search}} icon, enter **Vendors**, and then choose the related link.
2. On the **Vendors** page, select **Related** > **Vendor** > **Continia eDocuments Vendor Setup**.
3. If the **eDocuments Receiving Capabilities** FactBox is empty, select the **Recheck eDocuments Receiving Capabilities** action on the action bar. Once the FactBox is populated, you can go through the types of document the vendor can receive – and via which network.

Additionally, if you attempt to send an eDocument to a customer or vendor who's unable to receive it, an error is shown to indicate why. For example, the receiver might not be registered on the network.

## To set up vendors

To set up vendors so that you can exchange electronic documents with them via Continia eDocuments:

1. Choose the {{search}} icon, enter **Vendors**, and then choose the related link.

   > [!TIP]
   > Alternatively, you can select **Vendors** in the navigation bar on the Role Center.

<ol start="2">
<li>On the <strong>Vendors</strong> page, in the list of vendors, select the name of the one that you want to set up to use Continia eDocuments. This opens the <strong>Vendor Card</strong>.</li>
<li>On the action bar, click <strong>Related</strong> > <strong>Vendor</strong> > <strong>Continia eDocuments Setup</strong> to open the <strong>Continia eDocuments Vendor Setup</strong> page.</li>
<li>On the <strong>General</strong> FastTab, using the fields on the left side, specify how you as a customer would like to exchange documents with the selected vendor:</li>
<ul>
<li>Send In Electronic Format - select the electronic format that you want to use when sending electronic documents to this vendor.</li>
<li>Send From Participation - select the participation that you want to use when sending electronic documents to this vendor. For more information about participations, see <a href="https://docs.continia.com/en-us/continia-document-capture/setting-up-document-capture/setting-up-general-business-functionality/setting-up-the-continia-delivery-network#the-list-of-participations">Setting up the Continia Delivery Network</a>.</li>
<li>Send Purchase Orders Automatically - enable it if purchase orders should be sent automatically when released.</li>
</ul>
</ol>
<ol start="5">
<li>On the right side of the FastTab, under <strong>Vendor Identification</strong>, specify how to identify the vendor:</li>
<ol type="a">
<li>In <strong>Type</strong>, select the type of identifier that you want to use to identify the vendor.</li>
<li>If you selected <strong>Other</strong> under <strong>Type</strong> in step 5a above, select the three dots on the right side of the <strong>Scheme ID</strong> field to open the <strong>Continia Delivery Network Identifiers</strong> page. From the list of identifiers, select the one that you want to use for this vendor, and then select <strong>OK</strong> to return to the <strong>Continia eDocuments Vendor Setup</strong> page.</li></ol>
</ol>

   > [!NOTE]
   > If you selected **VAT** or **GLN** in step 5a, the **Scheme ID** field becomes unavailable – and it's automatically filled out with the correct identifier, based on your selection and the related metadata that's available in the Continia Delivery Network.

<ol>
<ol type="a" start="3">
<li>In <strong>Vendor ID Value</strong>, enter the vendor's exact ID, unless this has been autofilled.</li></ol>
</ol>

   > [!NOTE]
   > As in step 5b, if you selected **VAT** or **GLN** in step 5a, the **Vendor ID Value** field is automatically filled out with the correct ID – if this is available for the selected vendor.

<ol start="6">
<li>Return to the <strong>Vendor Card</strong>.</li>
<li>On the <strong>General</strong> FastTab, go to <strong>Document Sending Profile</strong> and select <strong>CONTINIAEDOCUMENTS</strong>.</li>
<li>Repeat steps 2-7 for any additional vendors you want to set up.</li></ol>
You're now all set up and ready to use Continia eDocuments to send electronic documents to the selected vendors. If necessary, you can of course always add additional vendors at a later stage.

## To set up customers

In order to set up customers so that you can exchange electronic documents with them via Continia eDocuments, follow these steps:

1. Choose the {{search}} icon, enter **Customers**, and then choose the related link.

   > [!TIP]
   > Alternatively, you can select **Customers** in the navigation bar on the Role Center.

<ol start="2">
<li>On the <strong>Customers</strong> page, in the list of customers, select the name of the one that you want to set up to use Continia eDocuments. This opens the <strong>Customer Card</strong>.</li>
<li>On the action bar, click <strong>Related</strong> > <strong>Customer</strong> > <strong>Continia eDocuments Setup</strong> to open the <strong>Continia eDocuments Customer Setup</strong> page.</li>
<li>On the <strong>General</strong> FastTab, using the fields on the left side, specify how you as a vendor would like to exchange documents with the selected customer:</li>
<ul>
<li>Send In Electronic Format - select the electronic format that you want to use when sending electronic documents to this customer.</li>
<li>Send From Participation - select the participation that you want to use when sending electronic documents to this customer. For more information about participations, see <a href="https://docs.continia.com/en-us/continia-document-capture/setting-up-document-capture/setting-up-general-business-functionality/setting-up-the-continia-delivery-network#the-list-of-participations">Setting up the Continia Delivery Network</a>.</li>
<li>Send eDocuments Automatically - select which documents should be sent automatically when posted – if any.</li>
</ul>
</ol>
<ol start="5">
<li>On the right side of the FastTab, under <strong>Customer Identification</strong>, specify how to identify the customer:</li>
<ol type="a">
<li>In <strong>Type</strong>, select the type of identifier that you want to use to identify the customer.</li>
<li>If you selected <strong>Other</strong> under <strong>Type</strong> in step 5a above, select the three dots on the right side of the <strong>Scheme ID</strong> field to open the <strong>Continia Delivery Network Identifiers</strong> page. From the list of identifiers, select the one that you want to use for this customer, and then select <strong>OK</strong> to return to the <strong>Continia eDocuments Customer Setup</strong> page.</li>
</ol>
</ol>

   > [!NOTE]
   > If you selected **VAT** or **GLN** in step 5a, the **Scheme ID** field will be unavailable and autofilled with the correct identifier based on your selection and the related metadata that's available in the Continia Delivery Network.

<ol>
<ol type="a" start="3">
<li>In <strong>Recipient ID</strong>, enter the customer's exact ID, unless this has been autofilled.</li>
</ol>
</ol>

   > [!NOTE]
   > As in step 5b, if you selected **VAT** or **GLN** in step 5a, the **Recipient ID** field will be autofilled with the correct ID, if this is available for the selected customer.

<ol start="6">
<li><strong>Optional</strong>: On the <strong>Export Setup</strong> FastTab, make any adjustments to the settings, if necessary.</li>
<li>Return to the <strong>Customer Card</strong>.</li>
<li>On the <strong>General</strong> FastTab, go to <strong>Document Sending Profile</strong> and select <strong>CONTINIAEDOCUMENTS</strong>.</li>
<li>Repeat steps 2-8 for any additional customers you want to set up.</li>
</ol>

You're now all set up and ready to use Continia eDocuments to send electronic documents to the selected customers. If necessary, you can of course always add additional customers at a later stage.