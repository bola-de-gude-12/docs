---
title: Activating Continia eDocuments
date: 06-05-2025
description:  
id: DC-178
lang: en
---

# Activating Continia eDocuments

This article describes how to activate Continia eDocuments. The activation is the first part of the overall setup process:

* Activating Continia eDocuments (this article)
* [Setting up Continia eDocuments](@DC-179), including XML structures and stylesheet import, if applicable
* [Setting up the Continia Delivery Network](@DC-75), unless this has been done at an earlier stage
* [Setting up Customers and Vendors](@DC-180)

> [!NOTE]
> If you're an existing user of Continia Document Capture, you must activate Continia eDocuments as described below. If you're a new user, it's activated and set up for you automatically.

## To activate Continia eDocuments

To activate Continia eDocuments and convert any existing XML templates:

> [!NOTE]
> Steps 1-3 are only required if you're using Document Capture 24.0 or older.

1. Choose the {{search}} icon, enter **Continia Feature Management**, and then choose the related link.
1. In the list of features, locate **Continia eDocuments**. In the **Enabled** column on the right side of the table, select the box to enable Continia eDocuments.
1. A dialog appears, asking if you're sure that you want to enable the feature. Select **Yes** to confirm.
1. The **Continia eDocuments Setup** assisted setup guide opens. Select **Next** to start the guide.
1. In the **Import from** dropdown menu, select the method you want to use to import your eDocuments configuration settings. Select **Next** to continue.
1. The **Continia eDocuments Setup** page opens. This allows you to copy your existing customer and vendor templates and convert them into templates that can be used with Continia eDocuments. Do one of the following:
   * To copy and convert your existing templates, select **Next** in the lower-right corner of the page.
      > [!IMPORTANT]
      > Note that no existing templates are deleted or replaced – they're only copied and converted, nothing is lost.
   * For a fresh start, enable the **Do not copy and convert any XML templates** setting – and then select **Next** in the lower-right corner of the page. If you change your mind, you can copy and convert the templates later.
1. In the lower-right corner of the page, select **Finish** to complete the assisted setup guide.

Continia eDocuments has been activated. To start using it to send and receive business documents, you must also set it up. This process is described in [Setting up Continia eDocuments](@DC-179).

> [!IMPORTANT]
> If you choose to copy and convert existing templates in step 6 above, note that no XML master templates are copied and converted – only supported XML templates (vendor templates). This is because the master template setup is different for Continia eDocuments. Continia eDocuments only requires one master template per document type (covering all electronic formats, such as **PEPPOLBIS3** and **OIOUBL**), whereas until now there has been one master template per electronic format for every document type.
> 
> This also means that any configuration you may have previously carried out for existing XML master templates (for example, in terms of automatic matching or approval) must be performed again once you've migrated to Continia eDocuments. You only have to do this once, though – then you're all set.