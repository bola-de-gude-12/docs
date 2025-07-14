---
title: The Netherlands and PM What to know
description: What to know about using PM in the Netherlands.
date: 13-06-2025
id: PM-400
lang: en
---



# The Netherlands and PM FAQ

## How can I Match Batch Payments for ABN Amro?

To use a search rule to match batch payments when using ABN Amro:

1. On the **Bank Acc Reconciliation** page, on the action bar select **Rules** > **Payment Identification Search Rules**. 
2. On the **Pmt. Ident. Search Rules** page, on the action bar, and select **New** to add a rule.
3. Enter the following information for the fields:
   * **Bank Account No.** - enter the bank account number that you want to match batch payments for. You need to define this per bank account. 
   * **Line No.** - specifies the line number relevant to the transaction.
   * **Reference Field** - select Payment Information ID.
   * **Search Text** - enter Referentie: *

![Payment identification search rule](/images/PM365/search-rule-additional.png)

After importing the bank statement with batch payments, the payments will now be automatically matched according to the rule.

## How can I solve the IBAN not found error for Rabobank?

When I try to communicate with Rabobank to import bank statements or export payments, I encounter an error about an IBAN that was not found:

`De volgende fout is opgetreden voor Bankrekening RABO-D-XXX met IBAN NLXXRABO0XXXXXXXXX: `
`No account was found from the supplied IBAN`

Why does this error occur, and how can I solve it?

An issue with the refresh token likely causes this error. When directly communicating with Rabobank, it is necessary to authenticate the web service connection between Business Central and Rabobank using a token.

To make sure the authentication is set up correctly:

1. Check the existence of the *Refresh Token.xml* file in the **File Archive**:
   * if present, it's likely that the refresh token has expired. Refresh tokens expire after 30 days and are updated automatically when used.
   * If not present, the issue might have originated from the bank account not being linked to the certificate during the initial setup.
1. To resolve these issues, first delete the authentication access key: go to the bank card, and on the action bar, select **Connection** > **Authentication Access Key**. 
1. On the **Authentication Access Keys** page, select the access key, and on the action bar, select **Delete Authentication Access Key**.
1. Now rerun the Bank Account Assisted Setup.
1. Select **Next** to start the assisted setup.
1. On the **Bank System** field, select Rabobank,  and select OK.
1. Select **Next** to continue.
1. Select **Connect to Rabobank**. You are now directed to the login page of your bank. 
1. Log in to your bank, select one or multiple accounts, and select **Confirm**. A token is sent to Business Central. Continia uses this token to start the communication with your bank account.
1. Select **Next**. Now you can make payments and download account statements. 

If you have a job queue running that imports the bank statements automatically, follow these steps to resume automatic imports:
1. Open the bank account reconciliation page for a Rabobank bank account.
2. Click **Related** > **Page** > **Show More Columns**.
3. Click **Import Bank Statements**.
4. Click **Import Only** and in the pop-up field, enter the date you want the bank statements from. After completing these steps, the job queue resumes importing bank statements automatically.



## The Netherlands and PM - What to know 

What are the version recommendations, solution limitations, and known issues for using Payment Management in relation to banks in the Netherlands?

For more information, see the article on [The Netherlands and PM - What to know – Continia Help Center (zendesk.com)](https://continia.zendesk.com/hc/en-us/articles/16971574047378-The-Netherlands-and-PM-What-to-know)

