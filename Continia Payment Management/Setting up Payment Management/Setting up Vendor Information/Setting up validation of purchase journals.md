---
title: Setting up validation on purchase journals
description: How to set up validation on purchase journals
date: 02-11-2023
id: PM-253
lang: en
---

# Setting up Purchase Journal validation

Payment Management automatically validates payment information entered in purchase journals. This default validation alerts you to any incorrect or missing details. It operates in the background as you work on the purchase journal. The validation occurs when you reopen, reload, and manually validate using the Validate Journal action or preview/post the journal from the action bar.

To set up purchase journal validation:

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Payment Management Setup**, then select the related link. 
2. In the **Purchase and Payments** FastTab, you can enable the validation settings:
   - **Validate Purchase Journal** - when enabled, validation occurs when you manually select the action **Validate Journal** on the purchase journal or when you post the journal.  
   - **Use Dynamic Journal** - when enabled, validation runs in the background dynamically while you work on the purchase journal, and any validation errors will be displayed in the **Validation** FactBox when you reload or reopen the journal. To enable this setting, the **Validate Purchase Journal** setting must be enabled. 

>  [!TIP]
>
> On the purchase journal, enable the **Validation** FactBox to see potential validation errors for the journal. If you disable the **Use Dynamic Validation** setting, you must manually run the action **Validate Journal** to see the validation errors before posting the purchase journal.  

## Related information

[Setting up purchase documents](@PM-177)
