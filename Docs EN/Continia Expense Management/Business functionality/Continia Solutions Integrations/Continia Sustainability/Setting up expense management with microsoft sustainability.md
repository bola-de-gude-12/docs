---
title: Setting up Continia Expense Management with Microsoft Sustainability
date: 02-10-2024
description:  
id: EM-
lang: en
---
# Setting up Continia Expense Management with Microsoft Sustainability

**--DRAFT--**

This integration enables your organization to track emissions related to various expense categories. You can then collect and report on the environmental impact of expenses directly within your Business Central system using the Microsoft Sustainability platform.  

## Pre-requisites

Before you start, ensure everything is configured correctly by consulting a certified Continia partner. You must also have the following:

* A Microsoft Dynamics 365 Business Central environment that has an active license for the Microsoft Sustainability app

## Install the Microsoft Sustainability app

To set up Expense Management  with Microsoft Sustainability, you need to:

1. **Install Microsoft Sustainability App:** Install the Microsoft Sustainability app in your [Business Central](https://www.google.com/search?q=Business+Central&sca_esv=ec29702a6463f262&ei=5ZbbaKSGLYGGxc8P9ZTjqQw&ved=2ahUKEwib0uDnioCQAxUVA9sEHQ2iG0YQgK4QegQIBRAB&uact=5&oq=what+is+the+set+up+for+Continia+Expense+Management+with+MS+Sustainability&gs_lp=Egxnd3Mtd2l6LXNlcnAiSXdoYXQgaXMgdGhlIHNldCB1cCBmb3IgQ29udGluaWEgRXhwZW5zZSBNYW5hZ2VtZW50IHdpdGggTVMgU3VzdGFpbmFiaWxpdHlIj3pQrQpYjE9wAXgBkAEBmAGrAqAB7xKqAQYxNy43LjG4AQPIAQD4AQGYAhCgAr0LwgIKEAAYsAMY1gQYR8ICBRAAGO8FwgIIEAAYgAQYogTCAggQABiiBBiJBcICBBAhGAqYAwCIBgGQBgiSBwQxMS41oAfbV7IHBDEwLjW4B7cLwgcGNS4xMC4xyAcW&sclient=gws-wiz-serp&mstk=AUtExfDDRm4StHJ0BhXnU7KCMUO9suOBnbCuOQ-MAfnK0QX2aCl3pPIaI9zbl2QQGobpj6m1dINGfFfNlzYF3lbceJqo-V2LRgJMvCMIZ8iihGhCFW46VJOYhe-xQf50Y5tUTec&csui=3) environment.

**For Existing Data**

You will need to update all existing expenses to use the new sustainability accounts from Microsoft. 

## Configure your Expense Management setup

First you must update your Expense setup, then configure fields for emissions data, and finally map emissions to accounts.

To update your Expense setup:

1. Search for **Expense Management Setup** in Business Central.

2. Update the setup for each expense type to reflect the new Microsoft Sustainability accounts.

3. Synchronize Expense Management with the new Microsoft Sustainability app.

To configure fields for emissions data:
1. Add new field types for capturing sustainability information to your expense types. 

To map emissions to accounts:
1. For each relevant expense type, link the new field types to their corresponding sustainability account types and numbers.
1. To enforce data capture during the expense submission process, set these fields to "Mandatory" or "Recommended". 


## Related information