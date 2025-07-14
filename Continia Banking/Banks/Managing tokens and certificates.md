---
title: Managing tokens and certificates in Continia Banking
description: How to manage certificates and tokens used to authenticate direct bank communication.
date: 27-05-2025
id: CB-248
lang: en

---

# Managing tokens and certificates

When using direct communication with banks, it is often necessary to authenticate the web service connection between Business Central and the bank using a bank certificate or token. If your bank requires this authentication, you must follow the instructions in the [assisted Bank Account Setup guide](@CB-37). 

## To share authentication access keys between companies

If you have already authenticated the connection, you can share the authentication access key between companies or banks within Business Central without exporting the certificate or token.

> [!WARNING]
>
> You can only share certificates between companies within the same database. For multiple databases, each must have its own unique certificate. This prevents files from being processed by the wrong database. Sharing the same certificate across data bases can lead to data conflicts, operational issues, and potential data loss.

To share the authentication key:

1. Search ({{search}}) for and select **Banks - Continia Banking**.

   > [!IMPORTANT]
   >
   > This section only explains how to share an authentication key. If you want to set up authentication for a bank for the first time, it is important to follow the steps of the assisted Bank Account Setup guide.

1. In the **Banks - Continia Banking** overview, choose the bank from which you want to share an authentication key.

   > [!TIP]
   >
   > You can share an authentication key from any bank or company that shares the authentication. 

1. On the action bar, click **Actions** > **Authentication Keys**.

1. In the **Authentication Keys** overview, on the action bar, click **Related Companies**. This will open companies that share the authentication key. 

1. Add the relevant companies to the list. When you add a new company, select the correct bank code that the authentication key should be connected to. Then run the assisted Bank Account Setup guide for the companies you added. In addition, please double-check the following:

   - For all the banks set up in the newly added company, ensure the information specified on the bank card (in the **Communication Agreement** Section) is the same as those specified for the banks in the company from where you shared the authentication. This information can be different depending on the bank.
   - If there are variations of the bank codes used across the companies that share the authentication, ensure that the correct bank codes and company are connected in the **Related Company/Company Authentications** list.



## To renew an authentication

Bank certificates and tokens have an expiration period determined by your bank. Approximately three months before the authentication expires, Continia Banking automatically sends a renewal request to the bank on your behalf. This renewal process occurs in the background, ensuring that the authentication is automatically renewed without any manual intervention required. If automatic renewal encounters issues, you can [manually renew the authentication](#to-renew-an-authentication-manually). 

## To renew an authentication manually

If automatic renewal encounters issues, you can manually renew the authentication.

To manually renew the authentication:

1. Delete the existing authentication.
2. Search ({{search}}) for and select **Bank Account Setup**.
3. In the **Bank Account Overview**, choose the bank account you wish to set up with Continia Banking and select **Next**.
4. Complete the fields in each step of the guide. Once the bank account is fully set up, its status in the **Bank Accounts Overview** will display as *Ready*. 
5. Repeat the steps above for any additional bank accounts you need to set up.

## To delete an authentication

Before deleting an authentication, check if the authentication is shared between companies or banks, as the authentication will be deleted in all companies and banks to which the authentication is shared. 

To delete an authentication:

1. Search ({{search}}) for and select **Banks - Continia Banking**. 
1. On the **Banks - Continia Banking** overview, choose the bank you want to delete an authentication for.
1. On the bank card, choose **Actions** > **Authentication Keys**.
1. On the **Authentication Keys** page, select the authentication key that you want to delete.
1. In the action bar, select **Related** > **Delete**.
1. Now run the Bank Account assisted setup guide for the companies that used the deleted authentication. 

