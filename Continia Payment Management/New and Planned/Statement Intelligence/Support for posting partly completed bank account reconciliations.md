---
title: Support for posting partly completed bank account reconciliations
description: Statement Intelligence will support the ability to partly post completed reconciliations in Statement Intelligence.
date: 30-09-2022
id: PM-79
lang: en
---

# Support for Posting Partly Completed Bank Account Reconciliations

| Feature | General availability online | Public preview |
| --- | :-: | :-: |
| Support for partly posting of bank account reconciliations | N/A | - |

> [!IMPORTANT]
>
> We have made a conscious decision not to develop this feature. The reason for this stems from our reliance on the starting and ending balances to manage the import of statements. If we allow partial posting, it might mess up this process. This could result in statements not being imported or matched correctly, and in some cases, things might stop working altogether.

## Business value

Companies that receive large bank account statements have requested the possibility to post partly reconciled bank account reconciliations in Payment Management. Continia aims to help these companies by making this feature update available with the next release of Payment Management. With this new addition to Statement Intelligence, the user will be able to post those bank statement lines that are fully reconciled and have status OK.

## Feature details

With this addition to Statement Intelligence it will be possible to post selected lines in the bank account reconciliation instead of all lines. The lines available for posting will depend on the reconciliation status. 
