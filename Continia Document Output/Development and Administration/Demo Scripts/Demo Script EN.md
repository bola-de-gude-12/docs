---
title: Continia Document Output Demo Script
date: 16-06-2025
description:
id: DO-34
lang: en
---

# Continia Document Output Demo Script

This demo script provides a step-by-step description of how to make a complete demonstration of the standard features in Continia Document Output.

The purpose of the Continia demo systems is to give Continia partners an environment to educate end customers, and to present and test the latest versions of Document Output. Basic knowledge of Document Output is required.

This demo environment is already set up and ready to use, and it's always updated to the latest version of Document Output.

The script covers the following processes:

<br>

| Processes | Description |
| --- | --- |
| [Starting a demo](#starting-a-demo) | How to start a demo of Document Output. |
| [Email elements](#email-elements) | Demonstrates the structure of a generated email. |
| [Template elements](#template-elements) | How to build an email, including email template lines. |
| [Setting up customer cards](#setting-up-customer-cards) | How to set up the Document Output FactBox on customer cards. |
| [Sending documents](#sending-documents) | How to send different types of documents manually. |
| [Sending documents to the Document Queue](#sending-documents-to-the-document-queue) | How to manually add posted documents to be dispatched from the Document Queue automatically. |
| [Sending documents automatically](#sending-documents-automatically) | How to run jobs to identify documents based on set criteria and put them in the Document Queue for automatic dispatch. |
| [Using the email log](#using-the-email-log) | How to use the Document Output Log. |

## Starting a demo 

Download the two files listed in the demo wizard and place them in a folder you can easily find again. These will be used to demonstrate some of the ways that Document Output can handle attachments.

The system will be set up with your own email address as the test recipient under **Document Output Setup**. This enables you to receive emails that are sent in the course of the demo. This will also overwrite all existing email addresses in Business Central when emails are sent from the demo environment.

It is recommended to set a rule in your email client so that emails sent from the demo environment will not be mixed in with your regular work emails in the inbox. Disabling teaching tips in the demo environment will also provide a cleaner experience.

It is recommended to ensure that all jobs listed under **Job Queue Entries** are running without error.

## Email elements

1. The first section will focus on the elements that make up an email with a sales invoice attached. The purpose is to show the structure of a generated email and explain how each part is governed by different settings in the template.
2. Go to **Document Output** section in the Role Center, under **Unhandled Posted Sales**, select the **Sales Invoices** cue.
3. Choose an invoice for customer **40000**, and select **Open E-Mail** in the action bar. 
4. Explain how the subject and the greeting are made using merge fields.
5. Show the parts of the email body that are plain text.
6. Explain how the two tables are entirely merged in.
7. Explain how the signature is a separate template that uses merge fields.
8. Scroll to the two images and explain how they are retrieved.
9. Show the attached PDF invoice in the FactBox on the right.
10. Select **Mail** and then select **Send**.
11. Return to the Role Center.

## Template elements

This section will show the elements in the template that build the email that was shown in the previous step. Templates, with their template lines, make up the framework that governs the customization of emails and the settings used for generating them.

### Email templates – general

1. Select **Document Output** in the navigation menu.
2. Select **Setup** and then select **Email Templates**.
3. Explain the two FactBoxes on the right.
4. Scroll down and select **SALESINVOICE**.
5. In the General FastTab, select **Show More**.
6. Explain the different fields in the **General** FastTab. Make sure to cover the possibility of activating either variants or dimensions for the template lines. Show the **Recipient Setup Lines**, and explain the **From Email** functions.
7. Explain the FactBoxes and their use.
8. Open and explain the settings in each of the **FastTabs** below the template lines.
9. Select **Template** in the action bar. **Select Merge Tables** and show the 3 default tables.
10. Select **1** and explain the settings and show the **Sample preview** at the bottom.
11. Select **Table Layout** in the action bar and open the **Left Column** FastTab. Explain the settings for table layout and close the page.
12. Select **Table Style** and explain the settings. Close the page.
13. Select **Select Table Style** and show some of the standard styles. Return to the **SALESINVOICE** template card.

### Email template lines

1. In the **Email Template Lines** FastTab, go to the first template line.
2. Explain the three **Background PDF** actions and **Merge PDF**.
3. Explain other settings on the template line.
4. Go to **Email Template** menu, select **Edit HTML Template**, and explain the difference between the use of merge fields in the subject line and in the email body.
5. Open the **Insert merge item** from the HTML tool bar and explain the three different merge types.
6. Add a new line after the last **Merge table** in the text body, and place the cursor at the beginning of the new line.
7. Type “**%**” and start typing “**shipment**”. Explain how the **merge field selector** narrows down the choices in accordance with your typing and the available merge choices.
8. Select “**tabel-3**”, and explain that the procedure for **Merge fields** as well as **Signatures** is the same.
9. Go to the **Signatures** FactBox and select **1** to the right of **SIG-DEFAULT**.
10. Select **SIG-DEFAULT** and explain the use of merge fields.
11. Go to the **Template Merge Fields** FactBox and show the list merge fields.
12. Go back to **Edit HTML Template** and go to the **Signatures** FactBox.
13. This time select the **1** to the right of **SIG-ADVERTISE**.
14. Select **SIG-ADVERTISE** and explain that it's possible to set up a variant with a time frame in which the signature is active. Explain that the banner image was dragged and dropped into the editor body.
15. Return to the Role Center.

### Email template lines based on dimension.

1. Search for **Email Templates**.
2. Select the **SALESCRMEMO** template.
3. Go to the **General** FastTab, select the **Dimension Code** field, select **Select from full list**, and select **CUSTOMERGROUP.**
4. Go to the **Email Template Lines** FastTab, and choose the line at the top by selecting the top left field.
5. Go to **Email Template** in the action bar and select **Edit HTML Template.**
6. Open your Windows file manager in the location to where the two test files have been downloaded. Drag the file called **DEFAULT** to the body text section of the editor. A file attachment box will pop up. Drop the file into the box. This will attach the file to all emails sent using this template. Note that the attachment will now be visible in the FactBox on the right.
7. Close the window and stay on the **SALESCRMEMO** template. 
8. On the **Email Template Lines** FastTab, in the action bar, select **Manage** > **Copy Line**.
9. In the dialog that appears, select **Yes** to open the **Copy Email Template Line** dialog. In the **Customergroup Code** field, select the three dots on the right, and then select **LARGE** > **OK**.
10. Go to the **PDF Password field** and enter “1234”.
11. In the action bar, select **Email Template** > **Edit HTML Template**.
12. Enter **LARGE ACCOUNT** in the email body's first line, and add a line change after that.
13. Return to your Windows file manager and the location where the two test files are. Attach the file called **VARIANT** in the same way you attached the first file.
14. Select **Save E-Mail Template** in the action bar, and close the page.
15. In the new template line, ensure that the **Enabled** field has a checkmark.
16. Close the page and return to the Role Center.

## Setting up customer cards

When you use Continia Document Output, you will get access to a lot of FactBoxes and actions. Customer cards will include a FactBox that may be configured with useful customer information.

To edit the FactBox for customer 50000:

1. Select **Customers** in the navigation bar.
2. Select **Customer 50000**. Show the Document Output FactBox on the customer card.
3. Select the zero (0) next to the **Email Recipients** field.
4. Create a new entry, select **Document Type** and select **Email Template**.
5. Select the **Document Code** field, and choose **Select** from full list.
6. Select **STATEMENT** and set **Recipient Type** to **To** and **Email Type** to **Contact**.
7. Choose **Contact No.** and select a contact from the list. This will send all emails using the **STATEMENT** template to the selected contact.
8. Close the page.
9. Select the three dots to the right of **Output Profile** in the Document Output FactBox.
10. Go to the **General** FastTab, select the **Output Profile** field, and select **Select from full list**.
11. Explain the columns for the Output Profiles and how the settings work for whether documents should be processed: Sent as an email, eDocument, printed or as a combination of these.
12. Select **EMAIL** in **Profile Code**.
13. Show the password field, and explain how customers can have unique passwords applied to PDF files sent to them.
14. Go to the **Continia Delivery Network** FastTab, and explain the option for a direct connection to an access point for PEPPOL and NemHandel.
15. Select **Additional Setup** and show the eDocument settings.
16. Close the page and return to the Role Center.

## Sending documents

The following shows the various ways documents can be sent, with examples of how this can also be automated.

### To manually send documents

This section describes how to send documents manually. With Document Output, you can send emails with attached documents and send emails using a queue.

### To send from Business Central record

1. Search for **Sales Orders**, and choose a sales order for **Customer 10000**. *In the Document Output FactBox, you can see the different email addresses for the different types of documents that are configured on the customer card.*
2. In the action bar, select **Document Output** > **Send Email**. *This will send the Order Confirmation.*
3. Show the email in the email log in the FactBox (a log of all emails sent with this order confirmation).
4. Chose the next open order for **Customer 10000**.
5. In the action bar, select **Document Output** > **Post and send/print**.
6. In the dialogue, select **Ship and Invoice**, and then select **OK**. *A shipment and sales invoice email will now be sent.*
7. Go to the email client and view the emails.

### To send from Unhandled Cues

1. Go to the Role Center.
2. Under **Document Output > Unhandled Posted Sales**, select the **Sales Shipments** Cue.
3. Highlight a shipment for **Customer 10000.** In the action bar, select **Actions** > **Print** > **Print/Email (SMTP)**.

### To send with edit

1. Go to the Role Center.
2. Under **Document Output**, under **Unhandled Finance**, select **Issued Reminders**.
3. Highlight the line with **Customer 20000**.
4. In the action bar, select **Open E-Mail**. *The email will open, and you can see an attached reminder and a zip file with the open documents.*
5. Open the zip file and show the open documents.
6. Type **DEMO EDIT** in the email body
7. In the action bar, select **Mail** > **Send**.
8. Return to the Role Center

### To send manual statements

1. Search for **E-mail/Print Statement**.
2. Set the **Date Filter** field to **03/01/23..03/31/24**.
3. Enable **Emails**.
4. Enable **Entries in period**. *Document Output will now filter for customers with entries in the selected period.*
5. Choose the line with **Customer 20000**.
6. In the action bar, select **Open Email**. *The email will now open, and you will see an attached PDF statement and a zipped folder with open documents.*
7. Open the PDF statement and show it.
8. Open the zip file and show the open documents in the folder.
9. In the action bar, select **Mail** > **Send**, and then review the email in Outlook.

### To send remittance advice

We can send remittance advice with a payment overview from payment journals and the **Unhandled Remittance Advice** pages to vendors.

1. Search for **Payment Journals** and select **Payment Journals**.
2. In the action bar, select **Prepare** > **Suggest Vendor Payments**. A dialog page will open, select **OK**.
3. Payment lines are now created.
4. In the action bar, select **Document Output** > **Email Rem.** **Advice**.
5. Select a customer, and then select **Send Email** in the action bar.

Go to your email client and show how all remittance advice have been consolidated into a single PDF.

## Sending documents to the Document Queue

This section will demonstrate how to manually add posted documents to be dispatched from the Document Queue automatically. For the purpose of this demo, the job queue entry that is used is set up to run **Email Jobs** every 60 seconds. (The job queue entry should run Codeunit **6175283 “NAV App. Server E-Mail Job Mgt”**.)

1. Go to the Role Center, and scroll to the **Document Output** section.
2. Under **Unhandled Posted Sales**, select the **Sales Credit Memos** cue.
3. Select **Send all to Queue** in the action bar.
4. Close the page, go to the **Document Output** section in the Role Center, and find **Queues**. Select the **Document Queue** cue.
5. Show the documents pending in the queue and refresh the page (F5) until they are dispatched.  If the job doesn’t run automatically, it may have stalled. Search for **Job Queue Entries**, pause the CDO NAV App.serverE-MailJobMgt job, and reset the status to **Ready**.
6. Go to your email client and show how Document Output has used a different template variant for one of the emails. Open the PDF in that email and use the password chosen from earlier.

## Sending documents automatically

This will demonstrate how Document Output can run jobs to identify documents based on set criteria and put them in the Document Queue for automatic dispatch. In this example, **Posted Invoice** is used. The function is the same for emails or eDocuments sent through a network or attached to a file or printed out.

1. Go to the Role Center
2. Go to the **Document Output** navigation menu. Select **Setup** and chose **Email Jobs**.
3. Select **New** in the action bar, and fill in **INVOICE** in the **Job No.** field.
4. Set type to **Email Template** in the **Type** column.
5. In **Email Template Code**, choose **SALESINVOICE**.
6. Select the **Table Filter** field. In **Field Number**, select the 3 dots and search for **posting date**. Select the number in the **No**. column for the posting date line.
7. **In Field Filter** enter **>=t**, and press [Enter] to save the changes.
8. Close the window.
9. Put checkmarks in all weekday checkboxes as well as the Enabled checkbox.
10. Search for **Sales Invoices**, and select **New**. In **Customer No**, type **10000** and press [TAB].
11. Go to the **Lines** FastTab, and choose the **No.** field. Select the item listed at the top.
12. Enter **10** in the **Quantity** field, and press [Enter].
13. Select **Post** in the action bar. Select **Yes** and then **No**. 
      *This will move the posted invoice to the Document Output Queue and the queue will dispatch
      it at set intervals, in the background without locking up the system.*
14. Show the received email in the email client.

## Sending order confirmations automatically

This setup will be practically identical to the one for sending sales invoices automatically.

1. Search for **Email Jobs** and select the **Email Jobs** page.
2. Select **New** in the action bar, and fill in unique **Job No.** (letters and/or digits). 
3. Set type to **Email Template** in the **Type** column.
4. In **Email Template Code**, choose **SALESORDER**.
5. Select the **Table Filter** field. In **Field Number**, select the 3 dots and search for **Status**. Select the number in the **No.** column on the status line.
6. In **Field Filter**, enter **Released** and press [Enter] to save the changes.
7. Close the window.
8. Put a checkmark in all weekday checkboxes as well as the **Enabled** checkbox.
9. Go to the Role Center, scroll to **Ongoing Sales** section, and select the **Sales Orders** cue. Choose a sales order and release it.
*This will now generate an order confirmation email for the released order and place it into the Document Output Queue and the Queue will dispatch it.*
10. Show the email in the email client.

## Sending statements automatically

This section describes how to set up automatic statements for Customer 50000 on the customer card.

1. Search for **Customers** and select customer **50000**. In the FactBox, select the three dots to the right of **Automatic Documents**.
2. Expand the **Automatic Documents** field and select **Select from full list**.
3. Select **Edit list**, expand the **Automatic Period Statement** field, and select **Select from full List**  -> **Edit list**.
4. In the line with code **BAL-1M**, go to the **Email Template Code** field and select the STATEMENT template and then **OK**. 
5. Expand the **Automatic Due Data Statement** field and select **Select from full list**.
6. Select **New**, and give it code “5D”. In **Send statement if Balance Date Formula**, enter “-5D”.
7. Select the **STATEMENT** template in the **Email Template Code** field, and then select **OK**.
8. Select **OK** once more, and in the Statement tab, change the **Automatic Statement** field to **Automatic**. Exit the page.
9. Go to **Customer Actions** in the Document Output roll-down at the top of the Factbox.
10. Select **Statement** in the action bar and select **Calendar**. Explain the Statement schedule.

## Using the email log

In Document Output, you can log all documents, both on customers and in the general log, which you can find via the **Document Output** menu.

1. Search for **Customers**.
2. Select **Customer 10000**.
3. Check the log in the FactBox.  
    *Here you can see all the documents that have been sent using Document Output. A log can also be accessed from the FactBoxes in each of the email templates. Here the log will show the usage log for the particular template that is opened.* 
4. Select any entry, and then select **Open Mail** in the action bar.
5. Close any open pages and return to the Role Center.
6. Search for **Document Output Log**. *This is an overview of all documents sent through Document Output. (If it has a check mark for log on the template.)*
7. Select any entry in the log, and then select **Open Mail** in the action bar.
