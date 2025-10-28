---
title: Using Continia Solution Management (on premises)
date: 21-07-2025
description: How to manage your solutions in on-premises instances of Business Central. 
id: DC-151
lang: en
---

# Using Continia Solution Management (on premises)
This article deals with the general management of Continia solutions in on-premises deployments of Microsoft Dynamics 365 Business Central. For information on the management of Continia solutions in online deployments of Business Central, see [Using Continia Solution Management](@DC-107). 

For information on Continia license management, including how to buy or cancel solution licenses, manage modules, and add or remove companies, see [Managing licenses](@DC-488).

> [!IMPORTANT]
> All guides in this article are aimed at Continia partners, as only partners are able to carry out the steps mentioned. If any of the guides are applicable to you, please reach out to your [dedicated Continia partner](@DC-487) and ask them to complete the relevant guide(s) for you.

## To activate a solution
When you've [bought a license for a solution](/continia-document-capture/development-and-administration/on-premises/managing-solutions/managing-licenses#to-buy-a-license), you can activate the solution by following these steps:

1. Search ({{search}}) for and select **Continia Solution Management**. 
1. In the list of installed Continia solutions, select the solution you wish to activate.
1. On the action bar, click **Activate Solution**.
1. Follow the on-screen instructions of the assisted setup guide to complete the activation.

If this is the first solution you activate, the customer's company is also activated at the same time. In that case, you must enter the customer's credentials and select the company type (test or production) as you complete the setup guide.

## To deactivate a solution
To deactivate a Continia solution:

1. Search ({{search}}) for and select **Continia Solution Management**.
1. In the list of installed Continia solutions, select the solution you wish to deactivate.
1. On the action bar, click **Deactivate Solution**.

> [!NOTE]
> When a solution has been deactivated, certain core features will stop functioning for this solution. However, the solution will still be visible in the user interface, and you'll still be able to access its data.

Note that when you deactivate all solutions, the company you're currently signed in to is also deactivated.

## To change client credentials

> [!WARNING]
> Take caution when changing client credentials. You should only ever change client credentials when moving from a production to a demo environment. Otherwise you risk losing essential data in Continia Online.

> [!NOTE]
> Whenever you change a customer's credentials, all of the customer's companies and their respective solutions are automatically deactivated. Following the change, you must manually reactivate all solutions for each company.

To change client credentials:

1. Search ({{search}}) for and select **Continia Solution Management**.
1. On the action bar, click **Client Credentials** to open the **Continia Client Credentials** page.
1. Enter the new client ID and the corresponding client password, and select **Save** to save the changes and close the page.
1. Reactivate all solutions manually using [the usual procedure](/continia-document-capture/development-and-administration/on-premises/managing-solutions/managing-solutions#to-activate-a-solution).
1. Repeat all above steps for any additional companies.

## Activating companies
Once a [company has been added](/continia-document-capture/development-and-administration/on-premises/managing-solutions/managing-licenses#to-add-companies), it must be activated. You do this by activating all relevant solutions (you must activate at least one solution per company in order to activate the company), which you can do using [the usual procedure](/continia-document-capture/development-and-administration/on-premises/managing-solutions/managing-solutions#to-activate-a-solution).

## Deactivating companies
You can deactivate a company directly in the user interface by [deactivating all active solutions](/continia-document-capture/development-and-administration/on-premises/managing-solutions/managing-solutions#to-deactivate-a-solution) for the company you're currently signed in to. When all active solutions have been deactivated, the company is also deactivated.

> [!NOTE]
> When a company has been deactivated, certain core features will stop functioning for this company. However, the company will still be visible in the user interface, and you'll still be able to access its data.

## Registering a company as a test company
In general, companies can be registered as either test companies or production companies, and it's generally possible to change the company type after the initial activation of a solution. However, your options depend on whether you use demo or production credentials, as described below:

**Using production credentials**  
When you [activate the first solution](/continia-document-capture/development-and-administration/on-premises/managing-solutions/managing-solutions#to-activate-a-solution) for a customer's company, you must define it as either a test company or a production company. If production credentials are used, there's no technical difference between these two company types, as they both point to production environments. The only difference is that you don't have to buy a license for a test company.

You can always change the company type at a later stage, if necessary. To do this:

1. Search ({{search}}) for and select **Continia Solution Management**.
1. Under **Company Status**, select the company type (test or production).

**Using demo credentials**  
When you activate the first solution for a customer's company, the company is always registered as a test company, and this can't be changed.

## To activate a company after database changes
Sometimes you may have to make changes to your database, for instance if you need to move it to a new server or would like to back up your system in order to test new functionality. In such cases, you must reactivate all companies following the change.

To avoid any accidental import of production data into a test environment, the system automatically detects if the database has been restored or moved to another server. Whenever the system detects changes to the database information, all companies and their respective solutions are deactivated – and a warning is displayed on the Continia Solution Management page. To reactivate the deactivated companies and solutions:

1. Search ({{search}}) for and select **Continia Solution Management**.
1. Click the warning that's displayed (as mentioned above) to open the **Continia Client Credentials** page.
1. Do one of the following, depending on your situation:
   * If the database is a copy of another database (whether a production or a test database), change the client credentials and click **Save**. Then activate all solutions manually using [the usual procedure](/continia-document-capture/development-and-administration/on-premises/managing-solutions/managing-solutions#to-activate-a-solution).
   * If the database has been moved or restored, click **Update Database Info** to continue with your existing credentials. This automatically reactivates all solutions.
1. Repeat all above steps for any additional companies associated with the database that's been changed.

## To reactivate a renamed company
When a company has been renamed, you must reactivate it. You can do this either from the role center or from the **Continia Solution Management** page. Both methods are described below.

To reactivate from the role center:

1. In the role center, the notification "\<Solution name\> has been installed. Would you like to activate it now?" is displayed. Click this notification to start the **Solution Activation** setup guide.
1. Complete the guide by following the on-screen instructions to reactivate the solution.

To reactivate via **Continia Solution Management**:

1. Search ({{search}}) for and select **Continia Solution Management**.
1. On the **Continia Solution Management** page, a red label with the text "The company has not been activated correctly" is displayed. Click this label to reactivate the company, including all previously activated solutions. The red label disappears upon activation.

## To copy a company for use as a test company

> [!NOTE]
> Only one set of client credentials is stored in each database. For example, in a production database, the customer's production credentials are stored – and from here they point to the production environments of Continia Online, the Continia Web Approval Portal, and the Continia Cloud OCR services. If you want complete separation of your test and production environments, you must create a database and use demo credentials for this.

To create a test company in a production database by copying a production company in the same database:

1. Copy the company, and give it a new name. For details on how to do this, see [this Microsoft article](https://docs.microsoft.com/en-us/dynamics-nav/how-to--create-companies).
1. Open the company that you've just created as a copy.
1. Search ({{search}}) for and select **Continia Company Setup**. 
1. Under **General**, enter a new company code, and click **OK** when you're done.
1. Activate the company by activating all relevant solutions using [the usual procedure](/continia-document-capture/development-and-administration/on-premises/managing-solutions/managing-solutions#to-activate-a-solution). When you complete the setup guide, select **Test Company** as the company type.
1. To send the new company code to Continia Online, search ({{search}}) for and select **Export OCR Configuration Files**. A dialog box confirms that a number of configuration files have been exported. Click **OK** to close it.

## To copy a company for use as an active company
To create an active company in a production database by copying a production company in the same database:

1. Copy the company, and give it a new name. For details on how to do this, see [Creating companies in Dynamics NAV](https://docs.microsoft.com/en-us/dynamics-nav/how-to--create-companies) (Microsoft article).
1. Deactivate the original company:
   1. Open the original company (unless you're already signed in to this).
   1. Using Continia Solution Management, deactivate the original company by [deactivating all active solutions](/continia-document-capture/development-and-administration/on-premises/managing-solutions/managing-solutions#to-deactivate-a-solution). When all active solutions have been deactivated, the company is also deactivated.
1. Activate the new company:
   1. Open the new company.
   1. Using Continia Solution Management, activate the new company by activating at least one solution. You do this using [the usual procedure](/continia-document-capture/development-and-administration/on-premises/managing-solutions/managing-solutions#to-activate-a-solution).

## To copy a production database for use as a test database
When you copy a production database to use as a test database, you must separate the test database from the production details in Continia Online (that is, details regarding activation status, the Continia Web Approval Portal, and Continia Cloud OCR services). To do this, you must specify a new set of demo client credentials and then activate all relevant solutions.

> [!IMPORTANT]
> **You can't use the same client credentials in multiple databases simultaneously.**
> 
> The activation status of a company is stored in Continia Online. When the system checks if a company is activated, it does so based on the client credentials, the company name, and the company GUID that are stored for the company in the database. If you don't change the client credentials, the new test database will be activated as the production database, thereby taking over the existing production database's activation status. Also, the test database will be linked to production details in Continia Online (regarding the Continia Web Approval Portal and Continia Cloud OCR services).

To copy a production database for use as a test database:

1. Restore the new database.
1. Using Continia Solution Management, [change client credentials](/continia-document-capture/development-and-administration/on-premises/managing-solutions/managing-solutions#to-change-client-credentials) to demo client credentials.
1. Search ({{search}}) for and select **Continia Company Setup**.
1. Under **General**, enter a new company code, and click **OK** when you're done.
1. Activate the company by activating all relevant solutions using [the usual procedure](/continia-document-capture/development-and-administration/on-premises/managing-solutions/managing-solutions#to-activate-a-solution). As you're using demo client credentials, the company is registered by default as a test company.
1. If you use on-premises OCR and have email addresses specified in your document categories, either remove these email addresses or assign different ones. To do this, search ({{search}}) for and select **Document Categories**, select a category (not its code), and click **Edit** on the action bar. Under the **General** FastTab, change the value of the **Email** field.
1. To send the new company code to Continia Online, search ({{search}}) for and select **Export OCR Configuration Files**. A dialog box confirms that a number of configuration files have been exported. Click **OK** to close it.

## Copying a production database to a new server
When you copy a production database to a new server, you must [update the client credentials](/continia-document-capture/development-and-administration/on-premises/managing-solutions/managing-solutions#to-change-client-credentials) in one of the databases or delete the client credentials from one of the databases. To delete the client credentials, run the table and delete the relevant record in the table.

## Importing data into a company using import tools
When importing data from one company to another using import tools such as Rapid Start, you must make sure that Continia Core tables are skipped, as they store the current company's activation data. If the Continia Core tables aren't omitted, you could corrupt the data and invalidate the company's activation state.

Therefore, you must skip importing data stored in objects in the following range: 6192810 to 6192868.
