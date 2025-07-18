From the Continia Solution Management page, you can efficiently manage all Continia solutions and modules. This includes starting or stopping a subscription, managing installed modules, and updating your invoicing and partner details. It is a central hub for controlling various aspects of your Continia products, ensuring smooth and straightforward management.

To access Continia Solution Management:

* Search ({{search}}) for and select **Continia Solution Management**.

## To activate Continia {param1} (from trial to subscription)
When you activate the solution for the first time, you need help from a Continia partner. They will guide you through the setup process effectively. During the initial activation guide run, the partner will log in using their Continia credentials to provide hands-on assistance. 

To activate a new subscription or change from trial to subscription:
1. Search ({{search}}) for and select **Continia Solution Management**. 
1. In the list of installed Continia solutions, select the solution you wish to activate or update from trial to subscription.
1. On the action bar, click **Manage Subscription**.
1. In the assisted setup guide, in the field **Activation mode**, click **Start Subscription**.
1. Follow the on-screen instructions to complete the guide.

> [!NOTE] 
> When you change the activation mode from trial to subscription, all modules in the subscription will be selected by default. In the guide, under **Select modules**, you must manually turn off any modules you don't want to subscribe to.

## To deactivate Continia {param1} in a single company

 You can deactivate Continia {param1} for a company without affecting the overall subscription or other companies in the environment. This is useful when a solution is no longer needed in a specific company, but should remain active elsewhere.

 To deactivate Continia {param1} in just one company:

1. Search ({{search}}) for and select **Continia Solution Management**.
2. Select Continia {param1} from the list of installed solutions.
3. On the action bar, click **Actions > Advanced > Deactivate App**.



## To cancel your subscription

When you decide to cancel your subscription, there are a few important things to keep in mind:

* **Billing for usage** - after canceling a subscription, you will still be billed for your usage during the month of cancellation, or you may be charged the minimum fee for that month. This applies to the services you used until the cancellation date.
* **Database-wide cancellation** - when you cancel a subscription, the cancellation will apply to all companies in the database. Keep in mind that this action will affect all relevant entities using the subscription services.
* **Continued access to processed data** - despite the cancellation, you can still access data that was already processed in your imported documents. This includes images and PDF files, which will remain accessible for your reference even after the subscription has been canceled.

To cancel your subscription:

1. Search ({{search}}) for and select **Continia Solution Management**. 
1. Select the solution you wish to cancel from the list of installed Continia solutions.
1. On the action bar, click **Cancel Subscription**.
1. Follow the instructions in the assisted setup guide to cancel your subscription.

## To enable or disable modules
To enable or disable a module:
1. Search ({{search}}) for and select **Continia Solution Management**. 
1. In the list of installed Continia solutions, select the solution for which you want to enable or disable modules.
1. On the action bar, click **Manage Modules**.
1. Follow the instructions in the assisted setup guide to turn modules on or off.

> [!NOTE]
> If you enable new modules, you’ll be charged for these modules on your next invoice.

## To activate a trial module

When you have an active subscription for one or more modules, you can try out another module in your production environment completely free of charge for 30 days. This option is currently only available for a limited number of specific modules, but it may be applied to more modules in the future.

To activate a free 30-day trial of a module, follow these steps:

1. Search ({{search}}) for and select **Continia Solution Management**. 
1. In the **Subscription Modules** FactBox on the right side of the page, locate the relevant module.
1. Select {{vertical-dots}} to open a dropdown menu for the module, and then click **Start Trial** to activate the module in trial mode.

If you want, you can stop the trial at any time within the 30-day trial period. To do so, follow the guide above but select **Stop Trial** instead in the dropdown menu.

> [!NOTE]
> By the end of the trial period, the trial will be automatically converted to a paid subscription, unless you actively cancel it as described above.

## To update invoicing information
To update your invoicing details:
1. Search ({{search}}) for and select **Continia Solution Management**. 
1. In the list of installed Continia solutions, select the solution for which you want to update invoicing details.
1. On the action bar, click **Update Company Information**.
1. Update your company details in all relevant fields, and select **Update** when you're done.

## To update partner information
When you enable **Update all Continia Solutions**, the entered partner details will be updated for all installed Continia solutions. This applies even if some solutions have partner details that differ from the selected solution.

If you want to switch to a new Continia partner for your organization, the new partner must follow these steps:

1. From within the organization's environment, choose the {{search}} icon, enter **Continia Solution Management**, and then choose the related link. 
1. In the list of installed Continia solutions, select the solution for which you want to update partner details.
1. On the action bar, select **Update Partner Information**.
1. Enter your Continia PartnerZone credentials. 
1. Select **Update**.

## To copy a company

The following instructions apply only to cloud instances. For instructions on how to copy a company on-premises, see [Managing Solutions](@dc-151#to-copy-a-company-for-use-as-a-test-company).

To safely create a company based on another company in a production or sandbox environment: 

1. Copy the company, and give it a new name. For details on how to do this, see [Copy a company](https://learn.microsoft.com/en-us/dynamics365/business-central/about-new-company#copy-a-company) (Microsoft article). 
1. When you're done copying the company, choose the company switcher icon and select your new company. 
1. Search ({{search}}) for and select **Continia Solution Management**. 
1. In the list of installed Continia solutions, select the solution you wish to activate. 
1. On the action bar, click **Activate Solution** and go through the setup – making sure to either activate as Trial in a Sandbox or as Trial or Subscription as required in Production. 
1. Search ({{search}}) for and select **Set Up [Name of the Solution]**.
1. Go through the steps in the assisted setup.
1. **Document Capture only** - search ({{search}}) for and select **Export OCR Configuration Files**.
1. **Expense Management only** - search ({{search}}) and select **Synchronize with Expense Management**.
