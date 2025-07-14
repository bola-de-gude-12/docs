---
title: Merge Tables
date: 23-04-2023
description: Learn how to use merge tables in the email body to convey source document information.
id: DO-167
lang: en
---

# Merge Tables

This article explains what merge tables are and how they're used to display source document information, for example from sales invoices or shipment notices, in the email body so the receiver doesn't have to open an attachment to access important information.

Merge tables in the email body efficiently present merge fields in an organized manner. Unlike standard tables, merge tables in Document Output offer enhanced flexibility.

Primarily, merge tables dynamically adjust their structure to accommodate varying amounts of data, ensuring optimal presentation, regardless of content. For instance, sales invoices often feature varying numbers of invoice lines, while reminder documents may contain differing quantities of document numbers.

Moreover, merge tables support functionalities such as summing columns or rows of data, and they facilitate the application of style templates so that visuals are maintained across different tables.

There will be three main sections in this walkthrough:
* [To create a merge table for an email template](#to-edit-a-merge-table-in-an-email-template), which will show how to edit the general data for a merge table and add/delete/move lines.
* [To edit the table layout](#to-edit-the-table-layout), which shows you how to edit the row and column headings.
* [To edit the table style](#to-edit-the-table-style), which shows you how to style the table rows with color, background color, padding, etc.

<iframe src="https://player.vimeo.com/video/915148852?h=1face23e05&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" width="560" height="315" frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write" title="DO Learn_1e Merge tables"></iframe>  
<br>

This video is part of the course [Get started using Document Output](https://learn.continia.com/get-started-using-document-output) on Continia Learn.

## To create a merge table for an email template

Document Output offers predefined merge tables for some email templates, but not all, so in some cases you'll need to create a new one from scratch. In cases where there are existing templates, you can easily just edit them to make them fit the needs of your company.

To create a merge table for an email template, do the following:

1. Choose the {{search}} icon, enter **Email Templates**, and then choose the related link.
2. Select the email template for which you want to create a merge table.
3. In the action bar, select **Template** > **Merge Tables**.
4. Select **New**, which will create a merge table card for a new merge table. There are four FastTabs of which you can edit fields in three. The fourth, called **Sample**, gives you a preview of how the merge table will look in the email body. The FastTabs with editable fields are: <ul><li><b>General</b> - here you edit the general information for the merge table, including description, table no., and line/sub table no. </li><li><b>Html table</b> - here you edit the table width and type</li><li><b>Merge table fields</b> - here you add/delete/move table lines and edit the fields in the table</li></ul>
6. In the **Merge table fields** FastTab, you can use the actions: <ul><li><b>New Line</b> to add a new line to the table</li><li><b>Delete Line</b> to delete a line from the table</li><li><b>Move Up</b> to move a line in the table up</li><li><b>Move Down</b> to move a line down in the table</li></ul>These are the most important fields: <ul><li><b>Number</b> - this field displays the place in the line hierarchy this line appears</li><li><b>Get Field From</b> - specify from where the data is retrieved, either a table or a codeunit</li><li><b>Field Type</b> - choose a field type for the field: texts, hyperlink, link to email address, or picture</li><li><b>Field</b> - choose a merge field from a list</li><li><b>Bold</b> - check to make the field bold</li><li><b>Text alignment</b> - choose alignment, left, right, justified, or center</li><li><b>Column Width</b> - enter a value in % or px for the column width</li>

## To edit the table layout
Now that you've created a merge table, it's time to take a look at editing the table layout, which concerns column and row headers.

To edit the table layout for a merge table, follow these steps:

1. While in the merge table card for the merge table you want to edit, select **Table Layout** in the action bar.
2. In addition to the **Sample** FastTab, which shows a preview of your merge table, there are three<a href="#footnote-1"><sup>1</sup></a> FastTabs with options for editing your table layout: <ul><li><b>General</b> - used for general information</li><li><b>Top rows</b> - used for adding/deleting lines and creating new rows on top of the table itself</li><li><b>Bottom rows</b> - used for adding/deleting lines and creating new rows in below the table itself</li></ul>Edit the table to suit your needs.

<small style>
<div class="footnotes">
 <hr />
 <ol>
 <li id="footnote-1">If the table is set to be row oriented, there will be four FastTabs in addition to the <b>Sample</b> tab. The additional one is called <b>Left Column</b> and is used to add, delete and edit the layout for headers on each row.</li>
 </ol>
</div>
</small>

## To edit the table style

Next you have the option to edit the table style, which concerns colors, width, etc. in the table itself.

To edit the table style for a merge table, follow these steps:

1. While in the merge table card for the merge table you want to edit, select **Table Style** in the action bar.
2. Optional: You also have the option to choose from a number of predetermined styles, whcih can then be edited, so you create your own template that can be applied to any other table across different email templates, instead of building one from scratch. To choose a predetermined style, select **Select Table Style** in the action bar, and then choose a style.
3. In addition to the **Sample** FastTab, which shows a placeholder table, there are two FastTabs with options for editing your table layout: <ul><li><b>Template</b> - used for general information and editing table border color and width (note that you can search for and add colors using the standard hex color codes)</li><li><b>Lines</b> - used for editing color, background color, border width, border color, row/column in bold, and padding for rows (note that you can search for and add colors using the standard hex color codes)</li></ul> Edit the table to suit your needs.