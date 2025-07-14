---
title: G/L Open Entries - Demo
date: 09-02-2024
description: Demo scenario to explain the G/L Open Entries module.
id: CF-45
lang: en
---

# G/L Open Entries Demo

The G/L Open Entries module allows you to create open entries on G/L accounts, which is similar to creating entries for customers and vendors. This feature is especially useful for recording inventory costs such as cash in transit, items in transit, or liabilities from social security contributions.

The start a demo scenario for G/L Open Entries:

1. Select the search icon, enter **Continia Demo Scenarios**, and select the related link.
2. On the **Continia Demo Scenarios** page, select one of the two scenarios for G/L Open Entries, and on the action bar, select **Run Scenario**:
   * **G/L Open Entries: Base** - generates pre-defined entries on a G/L account, which are then available for manual application.
   * **G/L Open Entries: Automatic application** - generates predefined entries on open entries managed G/L account, which is then automatically applied.



## G/L Open Entries: base

This demo scenario creates predetermined entries on a G/L account, which can be manually applied. We recommend you follow the steps of the guided experience of the Continia Demo Scenarios.

To start a demo scenario:

1. Use the {{search}} icon, enter **Continia Demo Scenarios,** and select the related link.
2. Select **G/L Open Entries: base,** and on the action bar, select **Run Scenario**. 
3. This setup will run you through the following steps:
   * Show G/L accounts ready for open entries
   * Create open entries and post them
   * Print a list of open entries
   * Apply entries

To show how to enable the build open entries field:

1. To enable the **Build Open Entries** field on the **G/L Account Card**, go to the **Continia Finance** FastTab. This field is automatically enabled when using the Demodata tool. 
   ![Open Entries](/images/CFI/gl-build-open-entries.png)

To show and post G/L Account open entries:

1. You can show that as a result of the postings made in the background, several open entries are available for manual application on the G/L account Transit, which is set to open entries managed.
   ![Entries](/images/CFI/gl-open-entries.png)

2. Go to the **General Journal** for DEMODATA to show that it is provided with accounting records. You can post these records to demonstrate the manual application of entries.
   ![Post entries](/images/CFI/gl-post.png)

3. Go to **Open G/L Accounts** to show an overview of G/L accounts managed on an open-entry basis with the corresponding open G/L entries in it, which are directly available for manual application via this page.

4. Demonstrate that via **Set Applies-to ID**, you can carry out or present the manual application of open G/L entries.
   ![Set applies to ID](/images/CFI/gl-set-applies-to.png)

5. Post the made application via the function **Post Application**.

6. Show the function **Apply Partial Payment**.

7. View the created entries, including the remaining amount, via the G/L account card of the open entry managed account.

8. Demonstrate the possibility unapplying entries. 

   

## Automatic Application

This demo scenario generates predefined entries on an open entries managed G/L account, which are then automatically applied. We recommend you follow the steps of the guided experience of the Continia Demo Scenarios.

To start a demo scenario:

1. Use the {{search}} icon, enter **Continia Demo Scenarios,** and select the related link.

2. Select **G/L Open Entries: automatic application** and on the action bar, select **Run Scenario**. 

3. This setup will run you through the following steps:

   * Show G/L Accounts - see the G/L Accounts that are ready for Open Entries or create a new one.
   * Create Open Entries - select Post to create some sample lines and post them.
   * List of Open Entries - print the list of open entries.
   * Apply Entries - select Apply to start the batch job.

   

To show the automatic application of G/L open entries:

1. Go to **G/L Open Entries** > **G/L Acc. Application**. 

2. On the **Automatic Application G/L Accoun**t page, show the criteria that can be used to analyze the application, such as the posting date, document numbers, and so on.

3. Explain that you can also use individual customer fields to analyze the application to be made.

4. Confirm the function automatic application with **OK**. You will see a message with the corresponding number of made applications according to your setup.

5. Go to the G/L account card to explain the options to view the balance and remaining amount.

   > [!TIP]
   >
   > You can delete transaction data by selecting **Run Object** > **Delete transaction data** if you want to start a new demo.
