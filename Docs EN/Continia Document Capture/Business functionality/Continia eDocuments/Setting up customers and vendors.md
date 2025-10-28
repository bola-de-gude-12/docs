---
title: Setting up customers and vendors for Continia eDocuments
date: 17-09-2025
description: How to set up customers and vendors to use Continia eDocuments.
id: DC-180
lang: en
---

# Setting up customers and vendors for Continia eDocuments

Once you've [activated Continia eDocuments](@DC-178) and [set it up](@DC-179), you must set up your vendors and/or customers to use it. This process is described in the sections below.

## Checking a business partner's eDocument receiving capabilities

Although you can take for granted the fact that a customer or vendor you're doing business with is able to physically receive documents, it's not always clear if they can also receive eDocuments. However, Continia eDocuments allows you to do just that: check if the customer/vendor you need to send an eDocument to is capable of receiving it.

To enable this feature:

1. Search ({{search}}) for and select **Continia eDocuments Setup**.
2. On the **Automations** FastTab, enable the **Update Documents Receiving Capabilities** setting.
3. The status of **Update Documents Receiving Capabilities** changes to **Ready**, indicating that the task responsible for updating the eDocuments participation cache is running.

You can now verify if a customer or vendor is part of an eDocuments network. The instructions below use vendors as an example:

1. Search for ({{search}}) and select **Vendors**.
2. On the **Vendors** page, click **Related** > **Vendor** > **Continia eDocuments Vendor Setup**.
3. If the **eDocuments Receiving Capabilities** FactBox is empty, click **Recheck eDocuments Receiving Capabilities** on the action bar. Once the FactBox is populated, you can go through the types of document the vendor can receive – and via which network.

Additionally, if you attempt to send an eDocument to a customer or vendor who's unable to receive it, an error is shown to indicate why. For example, the receiver might not be registered on the network.

## Setting up customers and vendors

There are two ways to set up business partners, so their network connection settings match the settings configured on your end.

The recommended way is to [use the eCandidates feature](#to-automatically-set-up-customers-and-vendors), which offers automatic discovery and network registration of participants. Identified participants can then be connected individually or in batches, considerably speeding up the process.

However, it’s also possible to manually set up [customers](#to-manually-set-up-customers) and [vendors](#to-manually-set-up-vendors). Both methods are covered here.

### To automatically set up customers and vendors

1.	Search ({{search}}) for and select **eCandidates**.
2.	If you don’t see any eCandidates in the table, click **Refresh List** on the action bar.

>[!NOTE]
>If you still don’t see any eCandidates in the table, click **Show all eCandidates** to list those who are currently not registered in any of the networks you participate in.

3.	Before selecting a connection method, check the values under the **Network Registrations** column – as you might have eCandidates registered in different networks.
4.	Select the desired eCandidates and, on the action bar, click **Connect**. Alternatively, click **Batch Connect** on the action bar to connect all listed eCandidates in one go.

>[!TIP]
>To quickly look up a customer or vendor, select it and click **Show Customer** or **Show Vendor** on the action bar to open the related card.

5. In the **Connect eCandidates** dialog box, under **eDocuments**, check the value of the **From Participation** field and select a value for the **Electronic Format** field. Note that, if using the batch connect method, all eCandidates must be registered in the same network selected in **From Participation** – and they must be able to receive the format set in **Electronic Format**. 

6. Under **Send eDocuments Automatically**, customize the values of the **Customer** and **Vendor** fields if needed. When you’re done, click **OK**.   

7. A dialog box confirms how many, if any, eCandidates have been connected. If needed, go through the process again using different values for **From Participation** and/or **Electronic Format**.

You're now ready to use Continia eDocuments to send electronic documents to the connected business partners.

>[!NOTE]
>If there are many customers and vendors linked to your company, checking if they have active registrations in the supported networks can be time consuming. To speed up this process, follow the first set of instructions under [Checking eDocument receiving capabilities](#checking-a-business-partners-edocument-receiving-capabilities). 

<div style="padding:56.25% 0 0 0;position:relative;"><iframe src=https://player.vimeo.com/video/1116129248?h=fce8677bab&badge=0&autopause=0&player_id=0&app_id=58479%22 frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write" style="position:absolute;top:0;left:0;width:100%;height:100%;" title="DC_Welcome_to_Document_Capture"></iframe></div><script src=https://player.vimeo.com/api/player.js></script>

### To manually set up customers

1. Search ({{search}}) for and select **Customers**.

> [!TIP]
> Alternatively, click **Customers** on the navigation bar on the Role Center.

<ol start="2">
<li>On the <strong>Customers</strong> page, in the list of customers, click the name of the customer you want to set up to use Continia eDocuments. This opens the <strong>Customer Card</strong>.</li>
<li>On the action bar, click <strong>Related</strong> > <strong>Customer</strong> > <strong>Continia eDocuments Setup</strong> to open the <strong>Continia eDocuments Customer Setup</strong> page.</li>
<li>On the <strong>General</strong> FastTab, using the fields on the left side, specify how you as a vendor would like to exchange documents with the selected customer:</li>
<ul>
<li>Send In Electronic Format - select the electronic format you want to use when sending electronic documents to this customer.</li>
<li>Send From Participation - select the participation you want to use when sending electronic documents to this customer. For more information on participations, see <a href="https://docs.continia.com/en-us/continia-document-capture/setting-up-document-capture/setting-up-general-business-functionality/setting-up-the-continia-delivery-network#the-list-of-participations">Setting up the Continia Delivery Network</a>.</li>
<li>Send eDocuments Automatically - select which documents should be sent automatically when posted – if any.</li>
</ul>
</ol>
<ol start="5">
<li>On the right side of the FastTab, under <strong>Customer Identification</strong>, specify how to identify the customer:</li>
<ol type="a">
<li>In <strong>Type</strong>, select the type of identifier that you want to use to identify the customer.</li>
<li>If you selected <strong>Other</strong> under <strong>Type</strong> in step 5a above, click the three dots on the right side of the <strong>Scheme ID</strong> field to open the <strong>Continia Delivery Network Identifiers</strong> page. From the list of identifiers, select the one that you want to use for this customer, and then click <strong>OK</strong> to return to the <strong>Continia eDocuments Customer Setup</strong> page.</li>
</ol>
</ol>

>[!NOTE]
>If you selected **VAT** or **GLN** in step 5a, the **Scheme ID** field will be unavailable and autofilled with the correct identifier based on your selection and the related metadata that's available in the Continia Delivery Network.

<ol>
<ol type="a" start="3">
<li>In <strong>Recipient ID</strong>, enter the customer's exact ID, unless this has been autofilled.</li>
</ol>
</ol>

>[!NOTE]
>As in step 5b, if you selected **VAT** or **GLN** in step 5a, the **Recipient ID** field will be autofilled with the correct ID, if this is available for the selected customer.

<ol start="6">
<li><strong>Optional</strong>: On the <strong>Export Setup</strong> FastTab, make any adjustments to the settings, if necessary.</li>
<li>Return to the <strong>Customer Card</strong>.</li>
<li>On the <strong>General</strong> FastTab, go to <strong>Document Sending Profile</strong> and select <strong>CONTINIAEDOCUMENTS</strong>.</li>
<li>Repeat steps 2-8 for any additional customers you want to set up.</li>
</ol>
You're now ready to use Continia eDocuments to send electronic documents to the selected customers. If necessary, you can add other customers at a later stage.

### To manually set up vendors

1. Search ({{search}}) for and select **Vendors**.

>[!TIP]
>Alternatively, click **Vendors** on the navigation bar on the Role Center.

<ol start="2">
<li>On the <strong>Vendors</strong> page, in the list of vendors, select the name of the vendor you want to set up to use Continia eDocuments. This opens the <strong>Vendor Card</strong>.</li>
<li>On the action bar, click <strong>Related</strong> > <strong>Vendor</strong> > <strong>Continia eDocuments Setup</strong> to open the <strong>Continia eDocuments Vendor Setup</strong> page.</li>
<li>On the <strong>General</strong> FastTab, using the fields on the left side, specify how you as a customer would like to exchange documents with the selected vendor:</li>
<ul>
<li>Send in Electronic Format - select the electronic format you want to use when sending electronic documents to this vendor.</li>
<li>Send From Participation - select the participation you want to use when sending electronic documents to this vendor. For more information on participations, see <a href="https://docs.continia.com/en-us/continia-document-capture/setting-up-document-capture/setting-up-general-business-functionality/setting-up-the-continia-delivery-network#the-list-of-participations">Setting up the Continia Delivery Network</a>.</li>
<li>Send Purchase Orders Automatically - enable it if purchase orders should be sent automatically when released.</li>
</ul>
</ol>
<ol start="5">
<li>On the right side of the FastTab, under <strong>Vendor Identification</strong>, specify how to identify the vendor:</li>
<ol type="a">
<li>In <strong>Type</strong>, select the type of identifier you want to use to identify the vendor.</li>
<li>If you selected <strong>Other</strong> under <strong>Type</strong> in step 5a above, click the three dots on the right side of the <strong>Scheme ID</strong> field to open the <strong>Continia Delivery Network Identifiers</strong> page. From the list of identifiers, select the one that you want to use for this vendor, and then select <strong>OK</strong> to return to the <strong>Continia eDocuments Vendor Setup</strong> page.</li></ol>
</ol>

>[!NOTE]
>If you selected **VAT** or **GLN** in step 5a, the **Scheme ID** field becomes unavailable – and it's automatically filled out with the correct identifier, based on your selection and the related metadata that's available in the Continia Delivery Network.

<ol>
<ol type="a" start="3">
<li>In <strong>Vendor ID Value</strong>, enter the vendor's exact ID, unless this has been autofilled.</li></ol>
</ol>

>[!NOTE]
>As in step 5b, if you selected **VAT** or **GLN** in step 5a, the **Vendor ID Value** field is automatically filled out with the correct ID – if this is available for the selected vendor.

<ol start="6">
<li>Return to the <strong>Vendor Card</strong>.</li>
<li>On the <strong>General</strong> FastTab, go to <strong>Document Sending Profile</strong> and select <strong>CONTINIAEDOCUMENTS</strong>.</li>
<li>Repeat steps 2-7 for any additional vendors you want to set up.</li></ol>
You're now ready to use Continia eDocuments to send electronic documents to the selected vendors. If necessary, you can add other vendors at a later stage.