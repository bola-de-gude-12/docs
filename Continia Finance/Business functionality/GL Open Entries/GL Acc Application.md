---
title: GL Acc Application in Continia Finance
date: 03-09-2023
description: 
id: CF-84
lang: en
---

# Automatic Application G/L Account

When you use the automatic application of G/L accounts, it generates predefined entries on a G/L account that is managed by open entries, which are then applied automatically. You can choose the criteria for analysis, such as document number, external document number, and more. Additionally, you can use individual customer fields to analyze the application, such as the global dimensions used. You can use up to three fields for this purpose.

To apply G/L accounts automatically:

1. On the Continia Finance menu, select **G/L Open Entries** > **G/L Acc. Application**.

2. In the **Posting Date** field, enter the date you want to display on the entries created by the batch job. Remember that if you enter a date earlier than the earliest posting date of the open entries, the system will automatically select the earliest posting date from the entries as the posting date.

3. You can define the criteria for analyzing the application process, such as using document numbers and external document numbers:

    * **Analyze Document No.** - determines whether open entries should be automatically applied based on matching document numbers.
    * **Analyze External Document No.** - specifies if open entries should be automatically applied based on matching external document numbers.
    * **Analyze Remaining Amount** - indicates whether pairs of open entries with equal total amounts should be automatically applied.
4. You can also use specific fields for analysis. To do that, activate **Analyze Individual Field** and select the field in the **Use Field no** field. You can select up to three fields to automatically apply open entries based on their values. 
5. Confirm the automatic application function by selecting OK. Once confirmed, a message will appear indicating the number of applications made according to your setup. 
