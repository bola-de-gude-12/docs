---
title: Frequently Asked Questions About General Business Functionality
date: 25-06-2024
description: Frequently asked questions about general business functionality in Document Output
id: DO-111
lang: en
---

# General Business Functionality FAQ

In this section, you can find answers to some of the most frequently asked questions about general business functionality in Document Output. The answers provide information on matters from issues with missing templates to why a profile isn't loaded automatically.

## How do I resolve an issue with missing templates or Output Profiles?
If you find that you're missing templates and/or Output Profiles in Document Output, it is likely due to setup issues resulting from an incomplete installation. This can occur during both new installations and upgrades.

To solve this:

* Run the setup guide by selecting the search icon and entering **Document Output Assisted Setup Guide**. By running this guide, you should be able to resolve the missing templates and Output Profiles issue and ensure that your installation is properly configured.

> [!NOTE]
>
> The Document Output Assisted Setup Guide does not modify settings or customized email templates. Its primary purpose is to ensure that new templates or output profiles are appropriately recognized and available.

## The OIOUBL profile doesn't load automatically, why?

You can view it with the code displayed below. If it is not 'DK', then OIOUBL will not be automatically loaded.

```
0 references | 0% Coverage
Local procedure TestProcedure()
var
	EnvironmentInfo: Codeunit "Environment Information";
begin
	Message(EnvironmentInfo.GetApplicationFamily())
end;
```

Where to apply it?

If you use an on-premises installation, you can use powershell to set Application Family. See example 3 in this Microsoft article: [Set-NAVApplication](https://learn.microsoft.com/en-us/powershell/module/microsoft.dynamics.nav.management/set-navapplication?view=businesscentral-ps-22) (external link).

## Can I send documents without sending an email?

Yes, you can use Document Output to send electronic documents (e-docs) like receipts and other files in XML format without sending an email. However, Document Output does not support this functionality if you intend to send documents in formats other than e-docs, such as regular documents (non-electronic). The system is designed specifically for handling and delivering e-documents; therefore, it does not provide the option to send regular documents, such as PDFs.

## How can I select the GLN when sending XML files to customers?

Currently, you can only change this setting manually for every customer. To do that:

1. Open the **Customer card**, and on the right panel, select **Document Output**. 
2. In the **Continia Delivery Network** FactBox, select **Additional Setup**. 
3. Go to the **Receiver Type** field and select *GLN* in the dropdown menu.

##  Why is the Document Output FactBox grayed out?

If you are unable to select options in the Document Output FactBox, it is often due to missing reports or misalignment of the report.

To solve this issue, check the following:

1. Is the report being used in multiple instances? Ensure the report is only used in *one* template at a time to avoid conflicts. To check this, Open **Email templates** and check the **Report ID** and **Report Name** columns.
2. Do the report name and ID match? To check this, open **Email Templates** and verify that the report ID and name are correctly aligned. 
3. Is a report selected on the **Email Template** card? To check this, open **Email Templates**, select the template, and check the **Report ID** and **Report Name** fields.

For more information about email templates, refer to the [Working with Email Templates](@DO-52) article.