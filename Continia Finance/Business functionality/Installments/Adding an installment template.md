---
title: Adding an installment template in Continia Finance
date: 23-10-2024
description: Learn how to create templates for scheduled payments.
id: CF-102
lang: en
---

# Adding an Installment Template

The Installment module in Continia Finance simplifies the management and monitoring of scheduled payments. You can create one-time installment plans for specific transactions, offering flexibility in payment management. Additionally, installment templates can be established for recurring payments or specific customers, making it easier to [apply installment plans](@CF-105) consistently. 

To add an installment template:

1. Use the {{search}} icon, enter **Installment Templates**, and select the related link. Alternatively, on the **Installment Payments Setup** page, on the action bar, select **Install Templates**. 
2. On the action bar, select **New** to add a new template.
3. Enter a unique code and a description.
4. On the action bar, select **Installment Template Lines**. Now, you can enter information for the specific settings of the template. For example, to divide the payment over three periods with a different percentage of the due amount. 
5. On the **Installment Template Lines** page, you can now define the exact allocation of the installments to be made in the future. You can make an allocation manually in the installment payment template lines. Alternatively, in the **Split** area, you also have an option for the system to calculate the lines automatically. Use the following fields to configure the template:

   | Field                                | Description                                                  |
   | ------------------------------------ | ------------------------------------------------------------ |
   | No. of Splits                        | The number of installments you would like to split the payment into. For example, 4. |
   | Split Description                    | The description of the rates, avoiding predefined texts if you want to use different texts per line. Placeholders are available for this purpose. |
   | Split Due Date Formula               | Save a valid due date formula using common values such as days, weeks, months, or years. Negative formulas generate an error.<br><br />Example 1: Split to 4 positions with the setup +1M:<br/> <br />Rate 1 = Due date of the original entry <br />Rate 2 = Due date of the original entry +1 month <br />Rate 3 = Due date of the original entry +2 month <br />Rate 4 = Due date of the original entry +3 month<br><br />Example 2: Split to 4 positions with the setup +2W:<br><br />Rate 1 = Due date of the original entry <br />Rate 2 = Due date of the original entry +2 weeks <br />Rate 3 = Due date of the original entry +4 weeks <br />Rate 4 = Due date of the original entry +6 weeks |
   | Installment used for Residual Amount | Specifies whether any remaining amount should be added by default to the first or last installment to ensure the total distribution equals 100%. A residual amount can occur when dividing payments into installments. For example, if an invoice of EUR 1,000 is divided into three equal installments, the system may not divide the amount evenly due to rounding. In this case, the small remainder would be automatically applied to either the first or last installment – depending on the selected option. |
   | Start Date for Evaluation            | The Evaluation Start Date is used to validate and determine the actual due date after applying the due date formula. This is a processing-only value that isn't saved to the database, and does not affect the evaluation due date on installment template lines. |

   

<style>


 .content table tr td:nth-child(1) {
 width: 230px;
 }
 .content table tr td:nth-child(2) {
 width: 570px;
 }
</style>

