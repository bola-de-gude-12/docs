---
title: Editing the Document Output FactBox on Customer Cards
date: 24-08-2022
description:  
id: DO-27
lang: en
---

# Editing the Document Output FactBox on Customer Cards

With Continia Document Output installed on your system, customer cards in Dynamics 365 Business Central will include a FactBox in the upper-right corner with useful information related to customers, such as email recipient and Output Profile, for easy reference and editing.

The first time you install Document Output, all existing customer cards in Business Central will automatically get a Document Output FactBox. The information in this FactBox will either be empty or automatically filled out, if possible.

To edit the information in the Document Output FactBox on a customer card, follow these steps:

1. Choose the {{search}} icon, enter **Customers**, and then choose the related link.
1. Select the customer for which you want to edit Document Output FactBox information.
1. In the Document Output FactBox, select the field to the right of the information you want to edit.
1. Make the desired changes, and exit the page to save all changes.  

 > [!TIP]
 > Explanatory notes on selected editable fields:
 >
 > * **Email Recipient**: Specifies the email recipient. The options are **Email Template Group**, **Email Template**, **All**. It's possible to create TO, CC, and BCC recipients for both email and contacts.
 > * **Log**: Logs all sent emails, prints, and electronic documents associated with the customer specified here.
 > * **Output Profile**: Specifies how this customer receives different types of documents.
 > * **Automatic Statement**: Here you can choose between two options: **Manual**, which lets you use the **Email/Print Statement** page, and **Automatic**, which will generate/send a statement automatically. More information in the article [Generating statements automatically](@DO-30).
 > * **Send Statement Code**: This is where you specify under which circumstances statements are sent by choosing a code from a list.