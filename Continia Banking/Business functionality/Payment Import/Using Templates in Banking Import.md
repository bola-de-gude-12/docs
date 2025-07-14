---
title: Using Field Templates in Banking Import
date: 04-02-2025
description: Learn how you can make use of Continia Banking templates.
id: CB-161
lang: en
---

# Using field templates in Banking Import

Field templates in Continia Banking Import allow users to create and reuse configurations for text fields.  This article provides an overview of key templates you can use and configure.

On the [Banking Import Setup](@CB-14) page, you can define templates to control different aspects of the reconciliation and posting process. The import settings defined in the setup are used as default values. However, they can be adjusted as needed on the following pages:

* The Bank Account Card page
* The Search Rule Card page
* The Payment Reference Rule Card page

## Payment Import FastTab

The **Default Statement Description Field Template** specifies the default field used for the statement description (in the Bank Account Reconciliation) and transaction text (in the Payment Reconciliation Journal) when importing bank transactions. It helps ensure consistent and clear transaction records by using predefined fields.

### Default templates

TRANSACDETAILTEXT
- **Description** - Detail text from the Bank Transaction Detail table.
- **Field Selection Text** - specifies the Detail Text field from the bank transaction detail for matching.
- **Example**: `<Bank Transaction Detail|Detail Text>`

TRANSACPOSTDESC
- **Description** - Bank Transaction Line Posting Description
- **Field Selection Text** - specifies the Posting Description field from the bank transaction line for matching.
- **Example**: `<Bank Transaction Line|Posting Description>`

TRANSACPOSTDESCS
- **Description**: Bank Transaction Line Posting Description and Posting Description 2
- **Field Selection Text** - specifies both Posting Description and Posting Description 2 fields from the bank transaction line for more comprehensive matching.
- **Example**: `<Bank Transaction Line|Posting Description> <Bank Transaction Line|Posting Description 2>`

To create a custom template:

1. On the **Banking Import Setup** page, navigate to the **Import** FastTab, and in **Default Statement Description Field Template** field, select the three dots.
2. On the **Bank Statement Description Templates** page, select **New**.
3. Add a **Template Code** and **Description**. 
4. In the **Field Selection Text**, select the three dots to specify which fields to search. You can select multiple fields and these will be applied for the statement description and transaction text when importing bank transactions. 

## Matching FastTab

The **Default Search Field Template** allows you to specify which fields to use when matching bank transactions during reconciliation. You can create your own custom templates by selecting the three dots.

### Default templates

**BANKTRANSACCODE**

- **Description**: Bank Transaction Code
- **Example**: `<Bank Acc. Reconciliation Line|Bank Transaction Code>`

**DESCTRANSACDETAILS**

- **Description**: Combines Description, Transaction Text, and Detail Text for improved matching.
- **Example**: `<Bank Acc. Reconciliation Line|Description> <Bank Acc. Reconciliation Line|Transaction Text> <Bank Acc. Reconciliation Line Detail|Detail Text>`

**DESCTRANSACTEXT**

- **Description**: Uses both Description and Transaction Text for matching.
- **Example**: `<Bank Acc. Reconciliation Line|Description> <Bank Acc. Reconciliation Line|Transaction Text>`

**DETAILTEXT**

- **Description**: Focuses only on Detail Text for matching transactions.
- **Example**: `<Bank Acc. Reconciliation Line Detail|Detail Text>`

**DOMAINFAMILY**

- **Description**: Uses Domain Code, Family Code, and Sub-Family Code for classification-based matching.
- **Example**: `<Bank Acc. Reconciliation Line|Domain Code> <Bank Acc. Reconciliation Line|Family Code> <Bank Acc. Reconciliation Line|Sub-Family Code>`

To create a custom template:

1. On the **Banking Import Setup** page, navigate to the **Matching** FastTab, and in **Default Search Field Template** field, select the three dots.
2. On the **Search Field Templates** page, select **New**.
3. Add a **Template Code** and **Description**. 
4. In the **Field Selection Text**, select the three dots to specify which fields to search. You can select multiple fields and these will be applied when the search field selection code is used in a search rule.



## Amount Difference FastTab

The **Posting Description Template** defines the format for transaction descriptions, particularly when handling amount differences in bank reconciliation. These templates ensure consistency in transaction descriptions. Default templates are available, but custom templates can also be created.

### Default templates

**ACCNORELATEDPRTYNME**

- **Description**: Account No and Related-Party Name
- **Description Pattern**: Payment from `<Bank Acc. Reconciliation Line|Account No.>` `<Bank Acc. Reconciliation Line|Related-Party Name>`
- **Example**: Payment from ABCDEFGH 84DA2D6A72D44E68B148AE8786B2BC3E

**DESCRIPTION**

- **Description**: Description
- **Description Pattern**: `<Bank Acc. Reconciliation Line|Description>`
- **Example**: 87A7C14094B54A038AEC67856013E893

**RELATEDPRTYNME**

- **Description**: Related-Party Name
- **Description Pattern**: Payment from `<Bank Acc. Reconciliation Line|Related-Party Name>`
- **Example**: Payment from 3F328BAA0B634D579051169587033BAC

**RELATEDPRTYNMEVALDAT**

- **Description**: Related-Party Name and Value Date
- **Description Pattern**: Payment from `<Bank Acc. Reconciliation Line|Account No.>` `<Bank Acc. Reconciliation Line|Value Date>`
- **Example**: Payment from ABCDEFGH 01/22/26

**TRANSACTIONTEXT**

- **Description**: Transaction Text
- **Description Pattern**: `<Bank Acc. Reconciliation Line|Transaction Text>`
- **Example**: CADC1E40D142473282EBBC1CAD4B930C

To create a custom template:

1. On the **Banking Import Setup** page, navigate to the **Amount Difference** FastTab, and in **Posting Description Template** field, select the three dots.
2. On the **Search Field Templates** page, select **New**.
3. Add a **Template Code** and **Description**. 
4. In the **Description Pattern** field, select the three dots to specify which fields to search. You can select multiple fields and these will be applied when the search field selection code is used in a search rule.
