---
title: Managing licenses
date: 15-09-2025
description: How to manage Continia licenses for on-premises Business Central.
id: DC-488
lang: en
---

# Managing licenses

This article provides information on how to manage Continia licenses for Microsoft Dynamics 365 Business Central on premises. For additional information about on-premises solution management, see [Using Continia Solution Management (on premises)](@DC-151). For solution management relating to Business Central online, see [Using Continia Solution Management (online)](@DC-107).

Using the guides below, you can buy or cancel solution licenses, manage modules (also referred to as granules), and add or remove companies.

> [!IMPORTANT]
> All guides in this article are aimed at Continia partners, as only partners are able to carry out the steps mentioned. If any of the guides are applicable to you, please reach out to your [dedicated Continia partner](@DC-487) and ask them to complete the relevant guide(s) for you.

## To buy a license
If you as a partner want to buy a license for one or more Continia solutions for a customer, follow these steps:

1. Go to the [Continia PartnerZone](https://partnerzone.continia.com/partnerzone/dashboard/).
1. In the menu at the top, click **License Manager**. Note that you must have admin rights to access this.
1. Do one of the following:
   * In the list of customers, find the customer that you want to buy a license for, and click **Manage** on the right to open the **Solutions manager** page.
   * If the customer isn't on the list, set up a new customer: In the upper-right corner, click **Create new customer**, and add all relevant details. You should be able to find all of these in the [Microsoft PartnerSource Business Center](https://businesscenter.mbs.microsoft.com/). Note that **MS Voice ID** is the customer's Microsoft license number. Click **Next** to open the **Solutions manager** page.
1. On the **Solutions manager** page, select the solution for which you want to buy a license.
1. Select the preferred license type and the number of users. The displayed options are based on the number of users you entered when you set up the customer, meaning that some of the options may have been grayed out.
   > [!NOTE]
   > When you select **Document Capture** in step 4 above, you also have to select which OCR technology you prefer once you've selected the license type and number of users.
1. Under **Companies**, enter the name of the customer's company, and click **Add company** to add any additional companies. Note that you're charged extra for additional companies, as they aren't covered by the basic license.
1. Click **Add license** when you're done.
1. Repeat steps 4-7 above for any additional solution(s) you want to buy a license for.
1. In the blue box on the right, click **Complete order** to open the order confirmation page. Enter any extra information in the displayed fields (all optional), and select **Submit order** when you're done.

The placed order is now sent to Continia, and you – the partner – receive an order confirmation by email. Once the order has been processed, another email is sent to you with the credentials you must use when you [activate the licensed solutions](/continia-document-capture/development-and-administration/on-premises/managing-solutions/managing-solutions#to-activate-a-solution). Note that it may take up to two days to process your order, as all orders are processed manually by Continia personnel. Finally, a third email containing an invoice is sent to you at a later point in time.

## Canceling a license
If, for some reason, you decide that you want to cancel a license, you can do so by sending a cancelation email to <accounting@continia.com> – including the customer's name and license number. Note that this email must be received by Continia no later than 30 days before the license renewal date.

All licenses are renewed automatically at the end of the license period, so you must actively cancel any license that you wish to discontinue in order for it to end.

## To add modules

> [!NOTE]
> You can't add modules until there's an active license for them to be added to, so be sure to [buy a license](/continia-document-capture/development-and-administration/on-premises/managing-solutions/managing-licenses#to-buy-a-license) before you carry out any of the steps below.

As a partner, you can add modules to a customer license by following these steps:

1. Sign in to [Microsoft PartnerSource Business Center](https://businesscenter.mbs.microsoft.com/).
1. Look up the relevant customer using the costumer's Microsoft account number.
1. Click **Registered ISV Modules**.
1. Click **Add ISV Module**.
1. In the list of ISV providers, select **Continia**.
1. Select the module(s) that you want to add to the license. For a list of all Continia modules, see [ISV modules to add to NAV/Business Central license](https://partnerzone.continia.com/partnerzone/my-continia/isv-modules/).
1. Click **Register** to add the selected module(s) to the license.
1. Download an updated license for the costumer.
1. Upload the updated license to your customer's Business Central environment, and ask the customer to restart Business Central.

## To remove modules
As a partner, you can remove modules from a customer license by following these steps:

1. Send an email to <accounting@continia.com> with information on what modules should be removed.
1. Sign in to [Microsoft PartnerSource Business Center](https://businesscenter.mbs.microsoft.com/).
1. Look up the relevant customer using the costumer's Microsoft account number.
1. Click **Registered ISV Modules**.
1. Deselect each of the modules that you want to remove to deactivate them.
1. Click **Register** to remove the deactivated module(s) from the license.
1. Download an updated license for the costumer.
1. Upload the updated license to your customer's Business Central environment, and ask the customer to restart Business Central.

## To add companies
To add one or more companies to a customer's Continia solution, follow these steps:

1. Go to the [Continia PartnerZone](https://partnerzone.continia.com/partnerzone/dashboard/).
1. In the menu at the top, click **License Manager**. Note that you must have admin rights to access this.
1. In the list of customers, find the customer that you want to buy a license for, and click **Manage** on the right to open the **Solutions manager** page.
1. On the **Solutions manager** page, select the solution to which you want to add a company.
1. Under **Additional companies**, click **Add additional company** and enter the name of the company you're adding. Note that you'll be charged extra for additional companies, as they aren't covered by the basic license.
1. Click **Add license** when you're done.
1. Repeat steps 4-6 above for any additional solution(s) you want to add companies to.
1. In the blue box on the right, click **Complete order** to open the order confirmation page. Enter any extra information in the displayed fields (all optional), and click **Submit order** when you're done.

## Removing companies
As a partner, you can remove one or more companies from your customer's license by sending an email to <accounting@continia.com> with information on what companies should be removed. This email should also include the customer's name and/or voice ID.

## Related information
[Managing solutions](@DC-151)  
[Continia Document Capture resellers and partners](@DC-487)  
[Continia PartnerZone](https://partnerzone.continia.com/partnerzone/dashboard/)  
[Microsoft PartnerSource Business Center](https://businesscenter.mbs.microsoft.com/)