---
title: Getting Notified of Remaining OCR License Pages
date: 06-09-2023
id: DC-153
lang: en
---

# Getting Notified of Remaining OCR License Pages

For Document Capture on-premises, you can set up notifications to alert users in your organization when you're running out of pages in your OCR license. This enables you to take timely action, so that you avoid having documents moved to the error folder because the limit has been reached.

> \[!NOTE] Such notifications are only displayed for users of [on-premises OCR](<Getting notified of remaining OCR license pages.md#on-premises-ocr>), as there's no page-processing limit as such for Continia Cloud OCR. However, seeing that the Continia Cloud OCR base license includes a maximum of 1,000 OCR pages per month and that you'll be charged a minor fee for any pages processed in excess of that, it may still be relevant for you to keep an eye on your page consumption. You can easily do so in the **Document Capture Setup**, as described below under [Continia Cloud OCR](<Getting notified of remaining OCR license pages.md#continia-cloud-ocr>).

## On-premises OCR

To get an overview of your OCR license status and set a page threshold at which notifications are displayed, follow these steps:

1. Search \{{search\}} for and select **Document Capture Setup**.
2.  On the **OCR License Pages** FastTab, you can check the following details related to your OCR page consumption:

    \


    | Field               | Description                                                                                                                                                                               |
    | ------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
    | **Warning Pages**   | Allows you to specify a threshold for when notifications should be displayed.                                                                                                             |
    | **Remaining Pages** | Indicates how many pages you have left to process in your license. Together with **Warning Pages**, this field determines when notifications are displayed.                               |
    | **Total Pages**     | Specifies how many pages are included in your license in total. By default, 10,000 pages are included per month for on-premises OCR, but you can purchase additional pages, if necessary. |
    | **Last Updated**    | Indicates the exact date and time when the above fields were last updated.                                                                                                                |

    \

3. Under **Warning Pages**, enter the number of documents you think should remain in order for a notification to be triggered.

When the number of remaining pages in your license is equal to or lower than the number you enter under **Warning Pages**, users will be notified that the license is approaching its limit. This notification is displayed to the users when they select **Import Files** from the Role Center, or when they go to any of the pages **Ready to Import**, **Document Journal**, or **Document Capture Setup**.

## Continia Cloud OCR

To get an overview of your OCR license status, follow these steps:

1. Search \{{search\}} for and select **Document Capture Setup**.
2.  On the **OCR License Pages** FastTab, you can check the following details related to your OCR page consumption:

    \


    | Field            | Description                                                                                                                                                  |
    | ---------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
    | **Used Pages**   | Indicates how many pages you've processed in your license.                                                                                                   |
    | **Total Pages**  | Specifies how many pages are included in your license in total. By default, 1,000 pages are included at no additional cost per month for Continia Cloud OCR. |
    | **Last Updated** | Indicates the exact date and time when the above fields were last updated.                                                                                   |

When the number displayed under **Used Pages** exceeds the one under **Total Pages**, you'll be charged a minor fee per excess page.

## Related information

[Configuring Cloud OCR](../../../../Continia%20Document%20Capture/Development%20and%20Administration/On-Premises/Deployment/@DC-141/)\
[Configuring On-Premises OCR](../../../../Continia%20Document%20Capture/Development%20and%20Administration/On-Premises/Deployment/@DC-150/)\
[Continia Notifications](../../../../Continia%20Document%20Capture/Development%20and%20Administration/On-Premises/Deployment/@DC-131/)
