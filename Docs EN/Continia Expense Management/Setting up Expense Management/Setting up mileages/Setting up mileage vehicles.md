---
title: Setting up Mileage Vehicles
date: 31-03-2025
description: 
id: EM-27
lang: en
---
# Setting up Mileage Vehicles

Vehicles are used for identifying different mileage rates and distinguishing between different posting setups. Some countries, for example, have different rates for electric vehicles and vehicles running on fossil fuel.

Vehicles are linked to a Microsoft Dynamics 365 Business Central G/L account, posting groups and VAT posting groups, and you can also specify [company policies for mileage expenses](@EM-40).



## Setting up a vehicle

It's possible to define a default vehicle that will be selected automatically when you create mileage expenses, based on either an expense user or an expense user group. You can use both existing expense users and expense user groups, or you can create new ones. See how to set up expense users [here](@EM-36) and expense user groups [here](@EM-35).

### Posting

After you've created a new vehicle, you need to define where mileages for this vehicle are posted. You can set a different posting account for each vehicle type if you want to, or you can choose the same account. 

To add a posting account to a vehicle type, follow the steps below.

1. Search {{search}} for **Vehicle List**, then choose the related link.
2. Select the vehicle you want to add a posting account for, then, on the action bar, select **Setup**.
3. Under **Posting Account Type**, choose an account type.
4. Under **Posting Account No.**, choose the account that mileages will be posted to.

When you're done setting up vehicles, you need to [define mileage rates](Setting up mileage rates.md) for these vehicles before you can start processing mileage expenses.

## Advanced vehicle setup

You can assign default vehicles (for example a company car), to both individual users or user groups. 

### Setting up a vehicle for an expense user group

To set up a default vehicle for an expense user group, follow these steps:

1. Search {{search}} for **Continia Users Default Setup**, then choose the related link.
2. On the action bar, select **New**.
3. On the new line, under **Setup Type**, choose **Group**.
4. Under **Code**, choose an expense user group.
5. Under **Vehicle Code**, choose the vehicle you want to set as the default vehicle for the expense user group.
6. Fill out the rest of the fields as necessary.

### Setting up a vehicle for an expense user

To set up a default vehicle for an expense user, follow these steps:

1. Search {{search}} for **Continia Users Default Setup**, then choose the related link.
2. On the action bar, select **New**.
3. On the new line, under **Setup Type**, choose **User**.
4. Under **Code**, choose an expense user.
5. Under **Vehicle Code**, choose the vehicle you want to set as the default vehicle for the expense user.
6. Fill out the rest of the fields as necessary.

## Related information
[Setting up the Continia Users Default Setup](/Continia Expense Management/Setting up Expense Management/Setting up General Business Functionality/Setting up the Continia Users Default Setup.md)  
[Expense User Setup for Expense Management](@EM-36)  
[Expense User Group Setup for Expense Management](@EM-35)  

