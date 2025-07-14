---
title: Generating Statements Automatically
date: 08-04-2024
description:  
id: DO-30
lang: en
---

# Generating Statements Automatically

This article describes the procedure for generating statements automatically and sending them to the **Document Queue**.  
<br>
<iframe src="https://player.vimeo.com/video/900778992?h=8290086837&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" width="560" height="315" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" title="DO Learn_3c Automatic statements"></iframe>

This video is part of the course [Get started using Document Output](https://learn.continia.com/get-started-using-document-output) on Continia Learn.

## To set up automatic generation of statements

To begin generating statements for a customer automatically, follow these steps:

1. Choose the {{search}} icon, enter **Customers**, and then choose the related link.
1. Select the customer to which you want to send statements automatically.
1. In the Document Output FactBox, to the right of **Automatic Statement**, select **Manual**.
1. In the **Statement** FastTab, in the **Automatic Statement** field, select **Automatic**.
1. In the **Send Statement Code** field, select **Select from full list**.
1. In the action bar, select **Edit List**.
1. Select a statement code, and in the same line select **Statement** in the **Email Template Code** column.
1. Optional: You can also select **New** in the action bar to configure a new statement code.
> [!NOTE] The **Output** column is set to **Journal** as default, which means that statements will be listed in the customer statement journal for visual validation before they are sent. You have the option to set the **Output** column to **Email**, which means that statements will be sent automatically from the job queue after having been generated.
9. Select **OK** to save and exit the page.
10. In the **First Statement Start Date** field, select the start date from which statements will be sent out.    

To fully automate the process of generating statements and sending them to a customer, you need to set up a job queue with a specific Codeunit, which you can read about in the article [Setting up Job Queues](@DO-44).