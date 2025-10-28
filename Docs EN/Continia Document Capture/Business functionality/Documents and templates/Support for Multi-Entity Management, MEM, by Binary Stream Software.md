---
title: Support for Multi-Entity Management (MEM) by Binary Stream Software
date: 03-05-2024
description:  
id: DC-218
lang: en
---

# Support for Multi-Entity Management (MEM) by Binary Stream Software

> [!IMPORTANT]
> This article only applies to Microsoft Dynamics 365 Business Central 2024 release wave 1 (BC v24) and later.

Continia Document Capture supports [Multi-Entity Management](https://binarystream.com/products/D365BC-MEM/) (MEM) by Binary Stream Software. MEM is a popular extension that allows you to consolidate multiple legal entities into a single company within Business Central. The entities exist as dimensions in this single company, and these entity dimensions must be validated first when transactions are entered in Business Central.

To streamline your workflow, you can let Document Capture automatically transfer any dimension values captured in incoming documents to MEM as entity dimensions. This is possible for both purchase and sales documents and happens when you register the documents in your document journal, as described below.

> [!NOTE]
> This functionality replaces the "DC+MEM Dimension Helper" app, which was previously required in order for Document Capture and MEM to work together. To maintain seamless integration between the two and optimize the performance of the new feature introduced in Document Capture 2024 R1, you may have to uninstall this helper app and any other custom MEM extensions.

## Overall functionality

The integration between Document Capture and MEM means that whenever you use the document journal to register a purchase or sales document for which an entity dimension has been defined (on the **MEM Multi-Entity Management Setup** page, under **Entity Dimension**), the value of the template field that corresponds to the defined entity dimension will be auto-populated to MEM. For example, if:

1. **Entity Dimension** on the **MEM Multi-Entity Management Setup** page has been defined as **Global Dimension 1 Code**
1. **Global Dimension 1 Code** on the **Dimensions** FastTab of the **General Ledger Setup** has been configured as **Department**
1. The **Department** field has been added to the relevant template (appearing in the **Document Header** section of the document journal) and the value **ADM** has been captured for this field

– then the value **ADM** will be automatically populated to MEM as an entity dimension when you register a document with that template in the document journal. This means that you don't have to manually specify the entity dimension in a MEM dialog, resulting in a smoother workflow and easier document registration.

## Behavior in case of missing entity dimension values

The above functionality applies to the **PURCHASE** and **SALES** categories, and the functionality is identical for both categories as long as dimension values are captured. But when no such values are detected, there are certain differences between the categories in terms of how Document Capture behaves:

If an entity dimension value is missing for a document in the **PURCHASE** category, a dialog appears when you register the document, allowing you to specify the entity dimension manually. However, due to certain limitations in the MEM extension, this dialog isn't displayed when entity dimension values are missing for documents in the **SALES** category. Instead, Document Capture displays the following non-configurable error comment in the **Comments** section of the document journal, in order to prevent you from registering a sales document without an entity dimension, which would cause MEM to malfunction:

* *Multi Entity Company is missing.*