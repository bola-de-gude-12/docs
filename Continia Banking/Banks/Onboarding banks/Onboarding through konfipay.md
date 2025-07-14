---
title: konfipay and Continia Banking
description: Learn how to set up integration through konfipay.
date: 27-03-2025
id: CB-143
lang: en
---

# Onboarding through konfipay

Continia Banking collaborates with konfipay to provide a seamless payment solution integrated with Microsoft Dynamics 365 Business Central for banks in Germany, Austria, and Switzerland. This integration simplifies your financial workflows by allowing you to easily download bank account statements and initiate payments directly within Business Central.

> [!TIP]
>
> Continia Banking is constantly working on adding support for new banks. Currently, direct communication for DACH banks is handled through konfipay, but other options will be available in the future. For an overview of currently supported banks, refer to the [Banks overview](@CB-79) article.

## To prepare for direct communication through konfipay

Before you can establish a connection with konfipay, a few requirements must be met:

- **Agreement** – you must first establish an agreement with konfipay to enable connectivity. For more information, see [www.konfipay.de](https://www.konfipay.de)
- **API Key** – to connect konfipay with Continia Banking, you’ll need an [API key](https://wiki.konfipay.de/konfipay/api-keys). The API key grants access to the konfipay API, allowing you to retrieve account transactions. It is essential that the associated account has the required permissions for performing transactions and adding bank accounts. To obtain the API key, go to [konfipay API Management](https://portal.konfipay.de/App/ApiManagement/Keys) and copy the key.



## To set up direct communication through konfipay

Once you have met the agreement and API key prerequisites, you are ready to onboard konfipay.

To set up direct communication through konfipay:

1. Search ({{search}}) for and select **Bank Account Setup**.
2. On the **Bank Account Setup** page, choose an existing bank account or create a new one.
3. To enable direct communication through konfipay, select **Direct Communication** in the **Communication** column, then click **Next**.
4. On the **konfipay Assisted Setup** page, you will be prompted to enter your API key.
5. After entering the API key, click **Next** to complete the setup.
