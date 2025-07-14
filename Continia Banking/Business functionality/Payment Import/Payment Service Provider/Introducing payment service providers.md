---
title: Introducing Payment Service Providers in Continia Banking
description: Learn more about including third-party payments in your administration.
date: 28-03-2025	
id: CB-128
lang: en
---

# Introducing Payment Service Providers

Using Continia Banking to establish integrated communication between Business Central and payment service providers (PSPs) is an efficient way to incorporate third-party payments into your administration.

Continia Banking supports file imports from third-party Payment Service Providers (PSPs) such as eCommerce marketplaces (e.g., bol.com) and payment services (e.g., PayPal and Klarna). You can directly import customer payment files from the PSP into the cash receipt journal.

> [!NOTE]
>
> You can enable the Payment Service Provider module from the Continia Feature Management Page. 

Continia Banking comes with preset PSPs for which you can add agreements. PSP agreements help you distinguish between different payment streams for a PSP. For example, if the same PSP uses different bank accounts or G/L accounts for posting fees.

>  [!TIP]
>
> We are continuously working on adding support for new payment service providers. If your preferred PSP is not listed, please reach out to us to learn more about the possibilities.

The following information is available for each PSP:
![Payment Service Provider](/images/CB/psp.png)

* **Code** - specifies the code that identifies the PSP.
* **Description** - provides a description of the PSP.
* **Transaction Port** - displays the appropriate file format to be imported. The options are XML, Excel, and Text.
* **PSP agreements** - displays the number of PSP agreements the payment service provider has. Select to view PSP agreements or to add one.
* **Rule template** - lists the external reference rules that are applied. 
  ![Agreement rule template](/images/CB/agreement-rule-template.png)

> [!NOTE]
>
> You can enable the Payment Service Provider module from the Continia Feature Management Page. 

