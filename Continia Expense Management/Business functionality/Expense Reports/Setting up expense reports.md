---
title: Setting up expense reports
date: 26-03-2025
description: Learn to enable, disable, and set up Expense Reports to suit your workflow
lang: en
id: EM-306
---
# Setting Up Expense Reports

Learn how to enable, disable, and set up expense reports in Microsoft Dynamics 365 Business Central. You can manage all of this from the Expense Management Setup page.

## Enabling or disabling expense reports
You must enable the Expense Reports feature if it wasn't enabled during your initial setup of Continia Expense Management. Conversely, if your organization prefers not to use expense reports, you may want to disable it entirely. 

To enable or disable expense reports:

1. Search {{search}} for Expense Management Setup, then choose the related link.
1. Under **General**, in **Application Areas**, go to **Expense Report**.
1. Select your preferred option:
   | Option | Description |
   | --- | --- |
   | **Disabled** | Expense users cannot create or submit expense reports. The **New Report** button won't be visible in the Expense app, and the **Report** tab won't be visible in the Expense portal. In Business Central, all settings related to expense reports will be unavailable. |
   | **Optional** | Expense users can create and submit expense reports. The **New Report** button will be visible in the Expense app, and the **Report** tab will be visible in the Expense portal, along with the buttons and tabs for ordinary expenses, mileages, and per diems, (if they've already been enabled). |
   | **Mandatory** | Expense users can *only* create and submit expense reports – not expenses, mileages, and per diems. The **New Report** button will be larger as it will be the only one available in the Expense app, just as the **Report** tab will be the only one available in the Expense portal. In the Role Center, the **Expense Reports** cue will be the only available cue. |

You've now enabled/disabled expense reports according to your setup preferences.

## Configuring expense reports
After you've enabled expense reports, you can configure some of the basic settings to suit the requirements of your organization. 

To configure your expense reports settings:

1. Search {{search}} for Expense Management Setup, then choose the related link.
1. Under **Expense Report**, edit the settings as needed:
   * **Auto submit for approval**: If you enable this, then all expense reports that are error-free will be automatically submitted for approval.
   * **Enable Departure and Return Date/Time**: Enable this to display the **Departure Date Time** and **Return Date Time** fields for each expense report created in the Expense app and the Expense portal. This allows expense users to enter the start and end dates and times for any business travels. The two new fields will also be visible on the **Configured Fields** page. They're named **ER-DEPARTURE DT** and **ER-RETURN DATETIME**. To view or edit the fields, search for and open the **Configured Fields** page, then on the action bar, select **Home** > **Expense Report**.

      > [!TIP]
      > To make it *mandatory* for expense users to enter start and end dates for every expense report, go to each of the fields in the list and select their boxes in the **Mandatory** column.
     
   * **Expense Report Pre-approval**: Use this option to specify if and how your expense reports should be preapproved. Select your preferred option:
     
      | Option | Description |
      | --- | --- |
      | **Disabled** | No preapproval is required for expense users to submit their expense reports. |
      | **Optional** | Any expense user creating an expense report in the Expense app or the Expense portal will be presented with a dialog asking if the report requires preapproval. The **Pre-approval Amount (LCY)** field will be visible in the app and the portal. If the expense user selects **No** in the dialog, then no preapproval is required for the report to be submitted. If the user selects **Yes**, the user must enter a preapproval amount and submit the report for preapproval before any further changes can be made (following the completion of the preapproval process). |
      | **Mandatory** | Expense users must enter a preapproval amount for each expense report. Whenever they create an expense report in either the Expense App or the Expense Portal, the **Pre-approval Amount (LCY)** field will be visible as a mandatory field that they must fill out to submit the expense report for preapproval. No additional changes can then be made until the expense report has been preapproved. |

You have now configured Expense Reports.

## Grouping ledger entries by expense report or document type
In some situations it makes sense to group ledger entries instead of submitting them separately, (for example, where there are a lot of entries for the same expense report). Using the Posting Group Method, you can group ledger entries by expense report or by document type.

The Posting Grouping Method has two ways of grouping entries:

- Single entry per expense report - creates a single entry for the expense report
- Separate entries per document type - groups entries based on expense, mileage, or per diem

To group ledger entries:

1. Search {{search}}  for **Expense Management Setup**, then choose the related link.
1. Under **Expense Report**, navigate to the **Posting Group Method** field.
1. Using the dropdown menu, choose either **Single entry per expense report**, or **Separate entries per document type**.

### Grouping exceptions

Currently, entries cannot be grouped by the following methods. 

- Balancing Account (for example, by different payment types)
- Different currencies
- Different dimensions
- Vendor No.

## Adding additional field codes

You may find it useful to add extra configured fields to an expense report, such as a project number or task number. If you have added the same configured field to the expense, per diem, and mileage document types, then the field value in the expense report will be inherited for all the documents added to the expense report.

## Related information
For more information about expense reports, see: 

[Setting up Pre-approval of Expense Reports](@EM-272)

[Submitting and Managing Expense Reports](@EM-294)

[Viewing Multiple Comments in Expense Reports](@EM-301)

[Overview of Expense Reports](@EM-44)