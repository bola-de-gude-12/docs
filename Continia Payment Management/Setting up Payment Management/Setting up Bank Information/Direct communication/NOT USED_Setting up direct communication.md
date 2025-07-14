---
title: Setting up direct communication
description: How to set up direct communication
date: 12-08-2021
id: 
lang: en
---
# Setting up Direct Communication

To use Direct Communication, the service must be enabled from the assisted [bank account setup](@PM-3). For a smooth signup process, it's recommended that you read the [Prerequisites](#prerequisites) before setting up direct communication. 

For more information about direct communication see the article [Bank Communication](@PM-158).

> [!IMPORTANT]
>
> If you [migrate from Payment Management FOB to the Payment Management app version](@PM-53), you can reuse your User Number/Function ID but you need to order a new code from your bank. Then, when you set up your bank accounts in the assisted [bank account setup](https://docs.continia.com/en-us/continia-payment-management/setting-up-payment-management/setting-up-bank-information/setting-up-bank-accounts#to-set-up-company-bank-accounts), you are asked for the new code.   
> 

## Prerequisites

Before you start setting up direct communication for a bank account, make sure you have the following prerequisites:

- The *Direct Communication* module must be activated in your Payment Management subscription. For more information on how to activate modules in Business Central see [Continia Solution Management](@PM-8). If you are using the on-premises version of Business Central, the license granule "6.016.860 - Continia Payment Management Direct Communication" must have been added to your license file. For more information, see [Managing Licenses](@PM-176).
- Your company must be activated as a production company, as you can't use direct communication in a test company, sandbox, or demo environment.
- You must have Payment Management Administrator credentials. This permission set is required for setting up Payment Management and running the assisted **Bank Account Setup**.

> [!NOTE]
>
> Additional prerequisites for enabling direct communication may exist for your bank as some banks require a certificate or token to authenticate the connection to Business Central, while other banks use a digital service such as Bizcuit and Tietoevry. You can localize your bank in the [Bank Integration](@PM-98) to read more about the prerequisites for onboarding your bank to direct communication.

## To set up direct communication

The Direct Communication service is configured in the assisted [bank account setup](@PM-3). In the guide, on the bank account overview, you can choose the preferred type of communication by using the dropdown menu in the **Communication** column. When having enabled direct communication for the bank account you must choose **Next** to begin the configuration of direct communication.

You'll find a detailed description of the prerequisites and information needed to configure direct communication for your bank in the [Bank Integration](@PM-98).



## Related information

[Bank Communication](@PM-158)  
[Bank Integration](@PM-98)  
[Bank Account Setup](@PM-3)  
[Manage Tokens and Certificates](@PM-175)  
[Authentication with Bizcuit](@PM-165)  