---
title: National Westminister
description: Integration with the bank system National Westminister
date: 15-07-2024
id: PM-287
lang: en
---

# National Westminister

With Payment Management, you can use direct communication to send bank data between National Westminister and Microsoft Dynamics 365 Business Central. For direct communication between your bank and Microsoft Dynamics 365 Business Central, [Payment Management collaborates with Yapily](@PM-268), an Open Banking payment service provider. 

This article lists the file format requirements for direct communication. 

To learn more about how to set up direct or manual communication:

- Manual communication - refer to the general [To set up bank accounts to use manual communication](@PM-3#to-set-up-bank-accounts-to-use-manual-communication) article. 
- Direct communication using Yapily - refer to the [Onboarding Yapily to use Direct Communication](@PM-268) article.

> [!NOTE]
>
> Connecting banks through Yapily is only supported for Business Central version 24 or higher.

## To connect with NatWest manually

When initiating manual communication with NatWest, the following features are supported:

| Communication | Send payments | Import status                                | Update status                                | Import payments                              | Reconcile                                    |
| ------------- | ------------- | -------------------------------------------- | -------------------------------------------- | -------------------------------------------- | -------------------------------------------- |
| Manual        | CSV           | <p style="text-align: center;">{{cross}}</p> | <p style="text-align: center;">{{cross}}</p> | <p style="text-align: center;">{{cross}}</p> | <p style="text-align: center;">{{cross}}</p> |

## To connect with Yapily Connect
### Supported functionality
{{include "yapily-fees"}}
For direct communication between your bank and Microsoft Dynamics 365 Business Central, you can use Yapily Connect. Yapily is an Open Banking payment service provider.

Before you can establish direct communication with your bank through Yapily, it is necessary to grant Yapily the required permissions. For more information about granting permissions, please contact your bank or refer to the [Preparing for Direct Communication Through Yapily](@PM-397) article. 

| Communication | Send payments             | Import status                                | Update status             | Import payments                              | Reconcile                 |
| ------------- | ------------------------- | -------------------------------------------- | ------------------------- | -------------------------------------------- | ------------------------- |
| Direct        | [Yapily Connect](@PM-268) | <p style="text-align: center;">{{cross}}</p> | [Yapily Connect](@PM-268) | <p style="text-align: center;">{{cross}}</p> | [Yapily Connect](@PM-268) |


{{include "yapily-payments"}}

| Functionality         | <p style="text-align: center;">National </br>Westminister bank</p> | <p style="text-align: center;">Natwest</br> Bankline</br></p> |
| --------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Faster Payment Single | <p style="text-align: center;">{{checkmark}}</p>             | <p style="text-align: center;">{{checkmark}}</p>             |
| Faster Payment Bulk   | <p style="text-align: center;">{{checkmark}}</p>             | <p style="text-align: center;">{{checkmark}}</p>             |
| International Single  | <p style="text-align: center;">{{cross}}</p>                 | <p style="text-align: center;">{{cross}}</p>                 |
| Bank Reconciliation   | <p style="text-align: center;">{{checkmark}}</p>             | <p style="text-align: center;">{{checkmark}}</p>             |
| Status File           | <p style="text-align: center;">{{checkmark}}</p>             | <p style="text-align: center;">{{checkmark}}</p>             |
| Direct Debit          | <p style="text-align: center;">{{cross}}</p>                 | <p style="text-align: center;">{{cross}}</p>                 |



> [!NOTE]
>
> Bank restrictions for bulk payments may apply. Refer to the [Bulk payments](https://docs.yapily.com/pages/payments/bulk-payments/additional-information/#known-restrictions) article on doc.yapily.com for more information.



### To set up your NatWest account for Yapily

To allow users to use open banking through Yapily with NatWest, you must add privileges to existing roles or assign users with a new custom role.

To create a custom role:

1. On NatWest, navigate to **Administration** > **Manage Roles**, and below the role list on the right select **Create Role**.
2. Enter a name and description for the new role and select the appropriate privileges. 
3. Go to the **Save & Add / Display other types of privileges** field and select **Third Party Provider consents**, and select **Save & go**.
4. Select the following checkboxes: 
   * Create and manage own account information consents
   * Manage all account information consents
   * I acknowledge that by assigning these privileges ....share data with third-party providers
5. Go to the **Save & Add / Display other types of privileges** field, select **Third Party Provider consents**, select **Save & go** and select **Continue**.



To approve the new role:

* Navigate to **Administration** > **Smartcard authorisation** and approve the newly created role.



To assign the new role to the user:

1. Navigate to **Administration** > **Manage Users** > **Edit roles** and select the new role.
2. Navigate to **Administration** > **Smartcard authorisation** and approve the newly assigned role.





## Related information

[About direct and manual bank communication](@PM-158)  

[Onboarding Yapily to use Direct Communication](@PM-268)
