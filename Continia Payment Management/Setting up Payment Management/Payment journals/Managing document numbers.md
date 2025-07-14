---
title: Managing document numbers
description: Information on how to manage the document numbers for suggested payment journal lines.
date: 06-10-2021
id: PM-198
lang: en
---

# Managing Document Numbers

In the **Payment Journal Setup** you can define how you want Payment Management to manage the payment journal lines suggested in the payment journal. 

Payment journal lines suggested in a payment journal are created with a **Document No** specified on the journal line. As per default payment lines will all be created with the same document number. In the **Payment Journal Setup** in the field **New Document No. per**, you can specify if payment journal lines should be created with the same document number, depending on the following payment criteria:

- **Journal**. All suggested payment lines, will be created with the same document number.
- **Vendor**. All suggested payment lines with the same vendor number, will be created with the same document number.
- **Line**. All suggested payment lines will be created with individual document numbers.
- **Posting Date**. All suggested payment lines with the same posting date, will be created with the same document number.

To make sure you don't receive any posting errors caused by the document number order, you can enable the **Allow Renumbering of Journal Lines** function in the payment journal setup. This will ensure document numbers are automatically renumbered before the journal lines are posted.

