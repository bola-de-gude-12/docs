---
title: Merge Fields in Document Output
date: 29-11-2024
description: See how to set up and use merge fields in Document Output
id: DO-212
lang: en
---

# Merge Fields in Document Output

This article describes how to use and set up merge fields in **Continia Document Output**. Merge fields enable the solution to fetch data from Microsoft Dynamics 365 Business Central fields or codeunits. The fetched data can then be used in email templates to dynamically populate content with relevant master data or contextual values.

For example:
- Add a document number to the naming convention for attached report PDFs.
- Include the output of a codeunit that counts the number of documents included in an email.
- Fetch and display the name of the recipient.

## How merge fields work

Continia Document Output uses the **Document Output Field Table** to establish a path from the source data to the merge field in the email template. The path depends on the Business Central table linked to the email template. Since the path can vary based on table relations, merge fields must be set up individually for each email template.

Merge fields are configured on each individual email template. A unique number must be assigned to each merge field.

For signature templates, any merge fields used in the signature must also be configured on the email templates where the signature templates are applied.

## To configure merge fields
In the following section, you'll find the procedure for how to configure merge fields. By following these steps, you can set up and manage merge fields effectively to enhance the dynamic capabilities of your email templates in Continia Document Output.

1. Choose the {{search}} icon, enter **Email Templates**, and then choose the related link.

1. Select an email template, and select the number in **No. of Merge Fields** in the **General** FastTab to access the field table.

1. Select **New** and assign a unique number in the **Number** field.

1. Provide a description in **Description**.

1. Choose a type in **Choose the Field Type**. The options are:
   - **Text**: Inserts the value as plain text.
   - **Hyperlink**: Inserts the value as a clickable web link.
   - **Link to Email Address**: Inserts a clickable email link.
   - **Picture**: Inserts an image.
   
1. Set the data source in **Get Field From**. The options are:
     - **Table**: Fetches data from the table linked to the email template or its relations.
     
     - **Setup Table**: Fetches data from a setup table with a single record.
     
     - **Sales Person**: Fetches data from the **Salesperson/Purchaser** table linked to the current user.
     
     - **Employee**: Fetches data from the **Employee** table via the Salesperson/Purchaser link.
     
       > [!NOTE]
       >
       > While the "Sales Person" uses the link to current user for fetching a field value from the "Salesperson/Purchaser" table, the "Employee" does not have a direct link like that. It also relies on the "Salesperson/Purchaser" link to the current user for identifying the correct employee record using the Salesperson/Purchaser code.
     
     - **UserID**: Fetches the current user ID.
     
     - **Company Name**: Fetches the name of the current company.
     
     - **Codeunit**: Fetches the output of a specified codeunit (see the developer guide for custom codeunits).
     
     - **User Full Name**: Fetches the full name of the current user.
     
1. Configure Additional Settings:
   - **Get From Table**: Automatically populated, blank, or offers a table choice based on the selected data source.
   - **Get From Field**: Select the specific field to fetch data from. Click **Finish** to add the field or **Next** to open related tables if applicable.
   - **Format String**: Enter formatting codes to specify how fetched data is presented.
   - **Web Address**: Enter the URL for a hyperlink or email link.
   - **Show Text**: Enter static text to overwrite or append data using `%1` as a placeholder for field or codeunit data.
   - **Width** and **Height**: Specify dimensions for images inserted into the email.
   - **Codeunit ID**: Enter the codeunit ID (see the developer guide for details).
   - **Codeunit Parameter**: Specify the value to extract from the codeunit.