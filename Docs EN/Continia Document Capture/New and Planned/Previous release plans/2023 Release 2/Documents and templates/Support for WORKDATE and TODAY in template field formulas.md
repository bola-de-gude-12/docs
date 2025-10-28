---
title: Support for WORKDATE and TODAY in Template Field Formulas
date: 29-11-2024
description:
id: DC-306
lang: en
---

# Support for WORKDATE and TODAY in Template Field Formulas

| Feature | Public preview | General availability online |
| --- | :-: | :-: |
| Support for **WORKDATE** and **TODAY** in template field formulas | - | {{checkmark}} Oct 2023 |

## Business value

By supporting this standard Microsoft Dynamics 365 Business Central feature, Continia Document Capture will save you a lot of time and hassle, as you'll no longer have to enter the work date or today's date manually for every incoming document. In case you want to apply one of these dates, Document Capture will simply add it to all relevant documents for you once you've set this up.

## Feature details

In the **Template Field Card**, on the **General** FastTab, you'll now be able to enter **WORKDATE** or **TODAY** under **Formula**. This will automatically insert the specified date into the applicable template field for all documents using that template. So if, for example, you set this up using **WORKDATE** for the template field **Due Date** and the work date is April 30, 2023, the **Due Date** field under **Document Header** in the document journal of all incoming documents with this template will read **04/30/23**.

For more information, see [The template field card](@DC-19#the-template-field-card).