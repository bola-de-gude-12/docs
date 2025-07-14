---
title: Manage Tokens and Certificates
description: How to manage certificates and tokens used to authenticate direct bank communication.
date: 06-01-2025
id: PM-175
lang: en
---

# Manage Tokens and Certificates

When using direct communication with banks, it is often necessary to authenticate the web service connection between Business Central and the bank using a bank certificate or token. If your bank requires this authentication, you must follow the instructions in the [assisted Bank Account Setup guide](@PM-3). 

## To share authentication access keys between companies

If you have already authenticated the connection, you can easily share the authentication access key between companies or banks without exporting the certificate or token from Business Central.

> [!WARNING]
>
> You can only share certificates for companies within the same database. For multiple databases, each must have its own unique certificate to prevent files from being processed by the wrong database. Sharing the same certificate can lead to data conflicts, operational issues, and potential data loss.

To share the authentication key:

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Banks**, and then select the related link. 

   > [!IMPORTANT]
   >
   > This section only explains how to share an authentication key. If you want to set up authentication for a bank for the first time, it is important to follow the steps of the [assisted Bank Account Setup guide](@PM-3).

1. In the **Banks** overview, choose the bank from which you want to share an authentication key.

   > [!TIP]
   >
   > You can share an authentication key from any bank or company that shares the authentication. 

1. On the action bar, select **Connection** > **Authentication Access Key**.

1. In the **Authentication Access Key** overview, on the action bar, select either **Related Banks** or **Related Companies**. Depending on your selection, this will open a list of banks or companies that share the authentication. 

1. Add the relevant banks or companies to the list. When you add a new company, [run the assisted Bank Account Setup guide](@PM-2#to-set-up-bank-accounts) for the companies you added. In addition, please double-check the following:

   - For all the banks set up in the newly added company, ensure the information specified on the bank card (in the **Communication Agreement** FastTab) is the same as those specified for the banks in the company from where you shared the authentication. 
   - If there are variations of the bank codes used across the companies that share the authentication, ensure that the bank codes on the **Bank Authentication Access Key Setup** page of the newly added company, are also added to the other companies that share the authentication.



## To renew an authentication

Bank certificates and tokens have an expiration period determined by your bank. Approximately three months before the authentication expires, Payment Management automatically sends a renewal request to the bank on your behalf. This renewal process occurs in the background, ensuring that the authentication is automatically renewed without any manual intervention required. If automatic renewal encounters issues, you can [manually renew the authentication](#to-renew-an-authentication-manually). 

## To renew an authentication manually

If automatic renewal encounters issues, you can manually renew the authentication.

To manually renew the authentication:

1. Delete the existing authentication.
2. Use the {{search}} icon and search for **Bank Account Setup**, then select the related link.
3. In the **Bank Account Overview**, choose the bank account you wish to set up with Payment Management and select **Next**.
4. Complete the fields in each step of the guide. Hover over a field to read a short description for assistance. Once the bank account is fully set up, its status in the **Bank Accounts Overview** will display as **Ready** if it’s ready for use. 
5. Repeat the steps above for any additional bank accounts you need to set up.

## To delete an authentication

Before deleting an authentication, you should control if the authentication is shared between companies or banks, as the authentication will be deleted in all companies and banks to which the authentication is shared. If you wish to remove the authentication for a single company or bank, see the section [To manage authentications shared between companies](#to-manage-authentications-shared-between-companies).

To delete an authentication

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Banks**, and then select the related link. 
1. On the **Banks** overview, choose the bank you want to delete an authentication for.
1. On the bank card, choose **Connection** > **Authentication**.
1. On the **Authentication** page, select the authentication key that you want to delete.
1. In the action bar, select **Delete**.
1. Now [run the Bank Account assisted setup guide](@PM-2#to-set-up-bank-accounts) for the companies that used the deleted authentication. 

## To import or export an authentication

To import or export an authentication:

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Banks**, then select the related link. 
1. Open the bank card for which the authentication must be exported or imported.
1. On the bank card, select **Connection** > **Import Authentication** action to import an authentication into the bank card, or select **Connection** > **Export Authentication** action to export an authentication from the bank card to a local folder.

> [!IMPORTANT]
>
> We strongly recommend that you do not export certificates from Microsoft NAV for use in Business Central Cloud. Instead, please contact your bank to order a new pin code, ensuring that your old certificate is securely closed and the new files are imported correctly. Certificates can only be exported with prior approval from our support team. Please reach out to us for assistance before proceeding with any exports.
