---
title: Extended Fixed Assets - Demo
date: 21-12-23
description: Use the Continia Demo Scenario to explain Extended Fixed Assets.
id: CF-49
lang: en
---

# Extended Fixed Assets Demo

The start a demo scenario for Extended Fixed Assets:

1. Select the search icon, enter **Continia Demo Scenarios**, and select the related link.
2. For the Ext. Fixed Assets module, there are two demo scenarios available:
   * **Ext. Fixed Assets: FA Templates** - generates different asset templates that are used in the context of a purchase invoice to create capitalized assets by purchasing the assets.
   * **Associations: Application with Customer/Vendor linking** -  allows you to present the topic Inventory managed Assets". This means that you can show the customer an acquisition of assets with a quantity deposit.
3. Select the scenario, and on the action bar, select **Run Scenario**.

## FA Templates

If you select the base scenario for FA templates, it will generate asset templates. 

To demonstrate FA templates:

1. Show how you can speed up the process of purchasing a new asset by using the templates and how various standard fields and depreciation books can be preset. 
   ![Fixed Asset Template](/images/CFI/fa-template-depreciation.png)
2. Go to the Fixed Asset Template Card, and navigate to the Continia Finance FastTab, to show **With Quantity** that is used to create the prerequisites for acquiring quantitatively managed assets.
   ![With Quantity](/images/CFI/fa-template-quantity.png)
3. Call up the Asset Templates from the Gen.-Journals, the Purchase Invoices and Purchase Orders, and the Asset Card.
4. Show how to select the function **Create FA from template** to let the asset create automatically after filling out the necessary fields (e.g. start date normal depreciation) over the menu option **Create Asset**.
5. Via the purchasing lines **Create Assets/Create FA from templates**, the card for selecting the asset templates opens, from which you can choose the asset to be purchased. As a result of the selection, you will receive a purchase line for the purchase of the selected asset from the respective creditor.
6. After posting the purchase invoice, you can view the purchased asset in the asset overview with the parameters preset from the template.

## To insert multiple Fixed Assets

The asset templates enable users to create multiple assets in a purchase document and link each asset to a new purchasing line immediately.

To insert multiple assets:

1. On the Purchase Invoice, select **Create FA from Template**.
2. Enter the general data, navigate to the **Insert Multiple Fixed Assets**, and in the **Quantity** field, enter a value.
3. After you then post the invoice the desired number of similar fixed assets has been created.



## Fixed Assets with quantities

If you choose to use the Fixed Assets with Quantity scenario, the Fixed Asset G/L Journals will open. Here, you will find the depreciation entry for an inventory-managed asset in the journal lines. 

The setup for managing assets in inventory can be saved in the asset template and can be accessed in the asset card of the created inventory-managed asset in the Continia Finance register. 

Once you have posted depreciation for the inventory-managed asset, you can navigate to the corresponding asset entries through the asset card. This will help you understand or demonstrate the results of the depreciation process for an inventory-managed asset.
