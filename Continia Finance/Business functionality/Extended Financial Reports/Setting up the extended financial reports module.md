---
title: Setting up the Extended Financial Reports module in Continia Finance
date: 10-09-2024
description: Learn more about setting up Extended Financial Reports and adding Account groups.
id: CF-97
lang: en
---

# Setting up the Extended Financial Reports Module

To begin using the Extended Financial Reports module, you need to configure certain values in the setup. You can do this manually in the **Extended Financial Reports Setup**, or you can use the assisted setup available in the **Continia Finance** section. You can manually configure Balance, VAT, and Extended Views and Lists in the **Extended Financial Reports Setup**, or you can use the assisted setup available in the Continia Finance section for a guided process. This setup ensures that the module is tailored to your specific financial reporting needs.

## To set up Balance and VAT

To set up the Extended Financial Reports module using the assisted setup:

1. Choose the {{search}} icon, enter **Assisted Setup**, and select the related link.
2. In the **Continia Finance** section, select **Set up Balance and VAT** and, in the action bar, select **Start Setup**.
3. The wizard lets you define up to four different account groups to categorize and organize G/L account groups by assigning captions for a clearer overview in the **Extended G/L Accounts** section. If you leave these fields empty, the headlines in the extended Account Overview display **Account Group 1...4**. To learn more about G/L Account Groups in the Extended Financial Reports module, refer to the [Working with G/L Account Groups](@CF-98) article.

To set up the Extended Financial Reports module:

1. Choose the {{search}} icon, enter **Balance and VAT Setup**, and select the related link.

2. On the **G/L Account Group 1 - 4 Captions** fields, you can categorize and organize G/L account groups by assigning captions to have a clearer overview in the Extended G/L Accounts section. If you leave these fields empty, the headlines in the extended Account Overview will display *Account Group 1...4*. To learn more about G/L Account Groups in the Extended Financial Reports module, refer to the [Working with G/L Account Groups](@CF-98) article.

3. Navigate to the **Purch VAT Next Month** section to set the following fields:

   | **Option**                     | **Description**                                              |
   | ------------------------------ | ------------------------------------------------------------ |
   | Enable VAT Correction          | By activating **Enable VAT Correction** and setting up three specific G/L accounts, you establish where transfer postings for the next month's input tax deduction occur. Additionally, you define the source code to be transferred to these postings or entries. The document entrance date is automatically set as the posting date on all invoice and credit memo purchasing documents. This feature is also available in all purchase journals, but the general journal template must be set to **Purchase**. While this option is active, you can still change the value of the document entrance date before posting, but entering a date for posting is mandatory. |
   | Bal. Account VAT Base          | Specify the G/L account to which the gross amount of the transfer postings will be posted. A posting is made on the original posting date, with the origin invoice recorded as a credit amount and the origin credit note recorded as a debit amount. On the document entrance date, the corresponding offsetting entry is made. |
   | Account VAT Base Next Month    | Select the G/L account to which the net amount will be posted on the original posting date for VAT base of the following month. |
   | Account VAT Base Last Month    | Define the G/L account to which the net amount will be posted on the document entrance date. (VAT base origin last month) |
   | VAT Correct Jnl. Template Name | This field is used as a default for the general journal template name in the **Correct VAT Entries** report to be run – but it can be changed there manually. |
   | VAT Correct Jnl. Batch Name    | This field is used as a default for the general journal batch name in the **Correct VAT Entries** report to be run – but it can be changed there manually. |
   | Source Code VAT Correction     | Specify the source code that the system will use to enter the input tax postings/entries for the next month's repostings. It is advisable to create a distinct source code, such as VST FOLGE. |
   | Allow Doc. Entrance Date From  | If a plausibility check is also to be performed on the document entrance date, the permitted, earliest document entrance date can be entered here. |
   | Allow Doc. Entrance Date To    | If a plausibility check is also to be performed on the document entrance date, the latest permitted document entrance date can be entered here. |
   | Default Doc. Entrance Date     | In this section, you have three choices: **Posting date**, **None**, and **Document date**. Choosing **Posting date** sets the document entrance date to match the posting date automatically. Opting for **Document date** sets the document entrance date to align with the document date. Selecting **None** leaves the field empty, requiring manual entry by the user; otherwise, an error message prompts completion before posting. |

   
## To set up Extended Lists and Reports

You must complete the setup window for Extended Lists and Reports for each company managed with Business Central.

To set up the Extended Lists and Reports module using the assisted setup:

1. Choose the {{search}} icon, enter **Assisted Setup**, and select the related link.
2. In the **Continia Finance** section, select **Set up Extended Views and Lists**.
3. The wizard allows you to modify the external document number. Even after posting, you can modify the **External Document No.** field of entries using the wizard. You can select the specific types of entries for which the **External Document No.** should be editable.

To set up Extended Views and Lists:

1. Choose the {{search}} icon and search for **Extended Views and Lists Setup**, and select the related link. 

2. Use the settings to customize your reports. For example, use the following fields:

   | **Option**            | **Description**                                              |
   | :-------------------- | :----------------------------------------------------------- |
   | Use Section Lining    | Enable to enhance readability by highlighting alternate lines of trial balance in gray. |
   | Show. Bal. Account    | Enabling this option shows balancing accounts in extended entry previews. If the system detects more than one balancing account, it labels them as VARIOUS and display their numbers separated by a semicolon. If there isn't enough space, the list ends with dots. |
   | Search Bal. Account   | Specify whether the system should search for balancing accounts using Transaction or Document No. information. |
   | Show with FA Postings | If you select **Balancing Account**, the balance account and its name display according to the G/L entry in the **Bal. Account No.** field. If you select **FA Name**, the fixed asset number appears in the **Bal. Account** field, and the asset name in **Bal. Account Name** for two-line postings (for example, the *Calculate Depreciation* batch job). <br />Note: Single line postings follow the "Balance Account" logic by default. |

3. In the action bar, you can use the **Set up Last Posting at** functionality to populate the **Last Posting at** field across all G/L accounts, customer records, and vendor profiles. This field allows you to, for instance, filter out customers or vendors with whom you haven't had any recent business interactions.

<style>

 .content table tr td:nth-child(1) {

 width: 250px;

 }

 .content table tr td:nth-child(2) {

 width: 550px;

 }

</style>
