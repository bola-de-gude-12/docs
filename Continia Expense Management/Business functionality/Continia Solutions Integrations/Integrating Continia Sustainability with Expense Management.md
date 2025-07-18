---
title: Integrating Continia Sustainability with Expense Management
date: 14-10-2024
id: EM-265
lang: en
---

# Integrating Continia Sustainability with Expense Management

If your organization has Continia Sustainability installed, you can benefit from integrating it with Continia Expense Management. Such integration will enable Continia Sustainability to perform carbon-emission calculations based on data captured by Expense Management, thereby helping you to track your environmental impact. Once you've installed Continia Sustainability, a number of features specific to this solution will automatically be available in Expense Management, as detailed below under [Sustainability-specific functionality in Expense Management](<Integrating Continia Sustainability with Expense Management.md#sustainability-specific-functionality-in-expense-management>).

Provided that you initially installed Continia Sustainability in trial mode, you can adapt your trial data to the needs of your organization and then deploy the customized data to your production environment. This is the recommended approach.

> \[!TIP] To minimize setup time, Continia highly recommends that you customize your trial data to your business needs and then export this data to your production environment using the configuration file. Otherwise, you have to set up everything manually, which can be very time-consuming.

There may be reasons for you to ignore the above recommendation. If you choose to do so, you must link Continia Sustainability with Expense Management from scratch by manually creating all necessary fields, field dependencies, and posting setups. For more details on this, see [Linking Continia Sustainability with Expense Management without the use of trial data](<Integrating Continia Sustainability with Expense Management.md#linking-continia-sustainability-with-expense-management-without-the-use-of-trial-data>) below.

## Sustainability-specific functionality in Expense Management

When Continia Sustainability has been installed, a number of changes are automatically made to the Expense Management app. More specifically, these changes are made to the **Expense Types**, **Expense Posting Setup**, and **Configured Fields** pages:

* On the **Expense Types** page, a new column – **Continia Sustainability Dependency** – is added.
* On the **Expense Posting Setup** page, two new columns – **Environmental Account Type** and **Environmental Account No.** – are added.
* On the **Configured Fields** page, an extended set of field types is added.

These columns and field types link the posting functionality of Continia Sustainability with Expense Management, providing Continia Sustainability with the necessary data to perform carbon-emission calculations.

## Linking Continia Sustainability with Expense Management without the use of trial data

Continia highly recommends that you start by setting up a trial environment and then export the trial data from this environment to the new production environment, as mentioned in the introduction above.

For trial environments, Continia has prepared a setup with data for certain expense types that are configured to ask for additional information when each expense type is selected by an expense user. The trial data depends on the selected localization, as localization settings (such as environmental accounts and emission types) are mostly based on the emission factor sets that are used in the relevant country or provided by the individual national government.

If, for some reason, you choose not to use trial data in your production environment, you must link Continia Sustainability with Expense Management manually from scratch, which can be done in two ways:

* [Through the **Expense Posting Setup**](<Integrating Continia Sustainability with Expense Management.md#to-link-the-solutions-using-the-expense-posting-setup>)
* [Using the **Continia Sustainability Dependency** feature](<Integrating Continia Sustainability with Expense Management.md#to-link-the-solutions-using-continia-sustainability-dependency>)

Below you'll find information on both approaches.

### To link the solutions using the Expense Posting Setup

The **Expense Posting Setup** enables you to manually link Continia Sustainability with Expense Management. This page has two new columns, **Environmental Account Type** and **Environmental Account No.**, which you must fill in to start tracking carbon emissions from employee expenses.

For example, to create a new expense type for taxi expenses, follow these steps:

1. Choose the \{{search\}} icon, enter **Expense Types**, and then choose the related link.
2. In the action bar, select **New** to create a new line in the table.
3. In the **Code** column, enter a relevant code for the expense type, such as **TRAVEL-TAXI**.
4.  In the **Description** column, enter a relevant description for the expense type, such as **Travel (taxi)**.

    > \[!NOTE] You can find more information on how to set up new expense types in [Setting up Expense Types](../../../Continia%20Expense%20Management/Business%20functionality/Continia%20Solutions%20Integrations/@EM-41/).
5. In the action bar, select **Setup** to open the **Expense Posting Setup** page.
6. In the **Posting Account Type** column, select **G/L Account**.
7. In the **Posting Account No.** column, select the number of the account that you want to use for this expense type.
8. In the **Environmental Account Type** column, select the account type that you want to use, such as **Business Travel**.
9. In the **Environmental Account No.** column, select the number of the account that you want to use.

You've now set up posting to Continia Sustainability for the expense type **TRAVEL-TAXI**. This means that whenever an expense user creates an expense with the expense type **TRAVEL-TAXI**, this expense will be posted automatically in Continia Sustainability.

### To link the solutions using Continia Sustainability Dependency

The **Continia Sustainability Dependency** feature allows you to configure additional fields that will be displayed when expense users create expenses in the Expense App or the Expense Portal.

For example, to create a new Continia Sustainability dependency for hotel expenses where emission factors differ from country to country, follow these steps:

1. Choose the \{{search\}} icon, enter **Expense Types**, and then choose the related link.
2. In the action bar, select **Edit List**.
3. In the **Continia Sustainability Dependency** column, open the dropdown menu for the expense type that you want to create the dependency for – in this case **HOTEL** – and then select **HOTEL COUNTRY**.
4. Choose the \{{search\}} icon, enter **Configured Fields**, and then choose the related link.
5. In the table, select an empty line at the bottom, and then select **HOTEL COUNTRY** from the list that opens. In the **Hide visibility by default** column, select the checkbox.
6. In the table, select an empty line at the bottom, and then select **NUMBER OF NIGHTS** from the list that opens. In the **Hide visibility by default** column, select the checkbox.
7. In the table, in the **FIELD CODE** column, locate **EXPENSE TYPE**, and then select the field in the **Field Dependencies** column to open the **Field Type Dependencies** page.
8.  In the action bar, select **New** to link a dependency (hotel country) to the **HOTEL** expense type, and then make the following selections for the new line:

    \


    | Condition            | Value | Reference Field Type Code | Expectation       |
    | -------------------- | ----- | ------------------------- | ----------------- |
    | Has a specific value | HOTEL | HOTEL COUNTRY             | Must have a value |

    \

9.  In the action bar, select **New** to link another dependency (number of nights) to the **HOTEL** expense type, and then make the following selections for the new line:

    \


    | Condition            | Value | Reference Field Type Code | Expectation       |
    | -------------------- | ----- | ------------------------- | ----------------- |
    | Has a specific value | HOTEL | NUMBER OF NIGHTS          | Must have a value |

You've now set up field dependencies for the expense type **HOTEL**. This means that expense users will be asked to add additional details for **HOTEL COUNTRY** and **NUMBER OF NIGHTS** when they create expenses in the Expense App or the Expense Portal.
