---
title: Enhanced Automatic Statements
date: 31-01-2025
description:  
id: DO-211
lang: en
---

# Enhanced Automatic Statements
Document Output offers enhanced options for creating and sending customer statements automatically. Using the Automatic Documents functionality, you can configure profiles to suit specific customer needs, such as defining the statement period, due dates, and output method. This guide covers how to set up automated statement distribution, assign profiles to customers, and manage statement scheduling and conditions.

<iframe src=https://player.vimeo.com/video/1028417355?h=cd8ade5086&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479 width="560" height="315" frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write; encrypted-media" title="Set up Automatic Documents"></iframe>  
<br>

This video is part of the course [Get started using Document Output](https://learn.continia.com/get-started-using-document-output) on Continia Learn.

> [!NOTE]
> If you're upgrading from a version before 2024 R2, activate the **Enhanced Automatic Statement** feature in **Continia Feature Management**. The legacy **Send Customer Statements** page is no longer used in this version.  


## To create automatic statement profiles

To create a new profile for automatic statement distribution, follow these steps:

1. Select the {{search}} icon, enter **Automatic Documents**, and select the related link. OR in the Role Center, navigate to **Document Output** > **Setup** > **Automatic Documents** > **Automatic Documents**.  
1. In the action bar, select **New**, or **Edit List** if you want to edit an existing profile.
1. Fill in **Code** and one or both of **Automatic Period Statement** and **Automatic Due Date Statement**, depending on the profile's requirements, to create a new statement profile.

### To configure period-based statements

In the **Automatic Period Statement** setup, you define criteria for when a statement should be generated and sent. You can choose a predefined one, or you can create a new one, and here's how you do that:

1. On the **Automated Documents** page, select **Edit List**.
1. Select the **Automatic Period Statement** field for the line you want to edit.
1. Select **New**.
1. Fill in or change the desired fields. These are some of the important fields to consider filling in:<br><ul><li><b>Send statement if</b>: Choose criteria such as entries exist within the specified period, outstanding or balance due on the account, or entries or balance due in the period.</li><li><b>Period Start Date Type</b> - Select either <b>Date formula</b>, but remember to define the period length in <b>Period Date Formula</b>, or <b>First open entry date</b>, where you set the start date based on the first open entry.</li><li>In <b>Period End Date Type</b>, you have four options: **Date formula** should be selected when **Date formula** has also been selected in **Period Start Date Type**; **Last entry date**: The period end date will be defined by the last entry date; **Last open entry date**: The period end date will be defined by the last open entry date; **Last bank posting date**: The latest bank posting date is used as end date for the period.</li><li><b>Period start date of month</b> - Enter the day of the month on which the period should start. If you leave it blank, the default selection is the first day of the month.</li><li><b>Sending interval</b> - Define how frequently the statement is sent, with options to set specific days or weekdays for sending.</li></ul>

> [!TIP]
> Check **Description**, which shows the outcome of the logic, to make sure that everything is as it's supposed to be.

> [!NOTE]
> It's possible to build a date formula that will behave in a faulty way without it causing an error. If, for example, the period defined in **Period Date Formula** is shorter than the interval in **Sending Interval**, then the statement will ignore parts of the period between the current and the last sending date, but no error message will be displayed.  

### To set up due date profiles

If the **Send statement if** field includes **Balance Due** or **Entries in period or Balance Due**, you can set up a due date profile to include a grace period:

1. On the **Automated Documents** page, select **Edit List**.
1. Select the **Automatic Period Statement** field for the line you want to edit.
1. Select **New** or **Edit List**.
1. In **Balance Due Date Formula**, specify a grace period for additional processing time, if needed.

## To pause statement generation

To avoid sending statements if the balance is negative, configure it in **Automatic Period Statement**. This is how you do it:

1. Select the {{search}} icon, enter **Automatic Documents**, and select the related link. OR in the Role Center, navigate to **Document Output** > **Setup** > **Automatic Documents** > **Automatic Documents**.  
1. Select **Edit List**.
1. Select the **Automatic Period Statement** field for the line you want to edit, and select **Show details** in the rolldown menu.
1. Select the **Do not send if negative balance** field to avoid sending statements if there's a negative balance.

## To choose email templates and output

You can configure the output method and the email template on the **Automatic Period Statement** page and the **Automatic Due Date Statement** page.

Configure the email template and output method on **Automatic Period Statement**:

1. Select the {{search}} icon, enter **Automatic Documents**, and select the related link. OR in the Role Center, navigate to **Document Output** > **Setup** > **Automatic Documents** > **Automatic Documents**.  
1. Select **Edit List**.
1. In **Automatic Period Statement**, select the dropdown menu and then **Show details**.
1. In **Email Template Code**, choose an email template, which would typically be the "Statement" template.
1. In **Output**, select your preferred output method:<ul><li><b>Journal</b> will send statements to the **Customer Statement Journal** for review</li><li><b>Email</b> will email statements directly to customers</li></ul>

Configure the email template and output method on **Automatic Due Date Statement**:

1. Select the {{search}} icon, enter **Automatic Documents**, and select the related link. OR in the Role Center, navigate to **Document Output** > **Setup** > **Automatic Documents** > **Automatic Documents**.  
1. Select **Edit List**.
1. In **Automatic Due Date Statement**, select the dropdown menu and then **Show details**.
1. In **Email Template Code**, choose an email template, which would typically be the "Statement" template.
1. In **Output**, select your preferred output method:<ul><li><b>Journal</b> will send statements to the **Customer Statement Journal** for review</li><li><b>Email</b> will email statements directly to customers</li></ul>

## To assign automatic statement profiles to customers

After setting up profiles, you can assign them to customers. This is how you do it:

1. Select the {{search}} icon, enter **Customers**, and select the related link.
2. Select the desired customer, and go to the **Document Output** FactBox.
3. Select the three dots to the right of **Automatic Documents**.
4. In the **General** FastTab, in **Automatic Documents**, select a statement profile.
6. In the **Document Output** FactBox, select the three dots to the right of **Automatic statement**.
7. In the **Statement** FastTab, in **Automatic statement**, select **Automatic**.

## To review schedules for automatic statement

To view scheduled and sent statements for a customer:

1. Select the {{search}} icon, enter **Customers**, and select the related link.
2. Select the desired customer.
3. In the **Document Output** FactBox, select the **Document Output** rolldown menu, and select **Customer Actions**.
4.  In the action bar, select **Statement** > **Calendar** to see scheduled and past statement dates.
