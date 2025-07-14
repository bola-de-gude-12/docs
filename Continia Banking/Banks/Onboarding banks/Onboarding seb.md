---
title: SEB and Continia Banking
description: Learn how to set up integration through SEB.
date: 12-06-2025
id: CB-148
lang: en
---

# Onboarding SEB

SEB (Skandinaviska Enskilda Banken) is one of the leading banks in the Nordic region, offering a wide range of financial services to businesses and individuals. This article guides you through the process of setting up direct communication between SEB and Business Central, ensuring efficient and secure data exchange for smoother banking operations.

## To prepare for direct communication through SEB

Before you can establish a connection with SEB, you must first establish an agreement with SEB to enable connectivity. Once the agreement is in place, SEB will provide you with the necessary login credentials to authenticate the connection and ensure secure communication.

To create an agreement in the SEB Business Arena:
1. Log in to SEB Business Arena and navigate to **Products and Services**.
2. Select **Automatic bookkeeping – payments in ISO format** and select **Fill in and order**.
3. From the list of providers, choose **Continia Software**, select the **Only on C&I Online** checkbox and select **Next**.
4. In the **Before you connect** dialog box, read the information and select **Next**.
5. Select the accounts to connect by selecting **Add account**. 
6. Choose the accounts you want to connect and click **Done**. Repeat this step for each account, one at a time. Once all accounts are connected, select **Next**.
7. Enter the **Contact information** and select **Next**.
8. Review the details and select **Apply**.
9. Sign with your **Digipass**. After signing, select **Close**. A message saying *We have received your order* will appear. It will now take up to 2 bank days for the agreement to be ready. 
10. Once SEB approves the agreement, the necessary information will be available in SEB Business Arena for you to complete the sign-up process in Continia Banking.

Before connecting to SEB, you must sign an additional agreement to access the File Handling Service (FHS) in C&I Online. This agreement is essential for viewing and authorizing payments in ISO format, as well as for uploading payment, salary, and direct debit files in various formats while allowing the download of comprehensive reporting files.

To authorize FHS file signing in C&I Online:

1. Log in to C&I Online.

2. On the action bar, navigate to **Authorizations** > **Authorizations**.

3. Select **Create new authorization**. 

4. On the **Agreement** tab, in the Agreement field select **FHS file signing**.

5. Assign a name to the authorization (for example, *Signing of Payments*) and select **Continue**.

6. On the **Services** tab, select the services for the payments you want to sign and select **Continue**.

7. On the **Delimitation** tab, we recommend selecting **All present and future accounts** and then select **Continue**.

8. On the **Users** tab, select the condition (solely, two jointly, groupwise) and select **Continue**. 

9. Once the condition has been chosen, it is possible to add users. Select **Add Users**, select the users and select **Continue**. 

10. Review the information and select **Save**.

11. Select **Edit and Sign** and put a checkmark on the agreement that needs signing. 

12. For single-user signing, select **Sign** and authenticate with Digipass. For multiple users, go to **Authorizations** > **Edit and Sign**.

     Once the agreement is signed, the new menu **Sign Payments** will appear under **Payments**.

## To set up direct communication through SEB

Once you set up the agreement and have access to the necessary information in SEB Business Arena, you are ready to complete the sign-up process in Continia Banking.

To set up direct communication through SEB:

1. Search ({{search}}) for and select **Bank Account Setup**.
2. On the **Bank Account Setup** page, choose an existing bank account or create a new one.
3. To enable direct communication through SEB, select **Direct Communication** in the **Communication** column, then click **Next**.
4. On the **SEB Assisted Setup** page, you will be prompted to enter:
   * The company name stated on the bank agreement
   * The VAT number stated on the bank agreement
   * The email address - this must match the email address originally entered in the agreement within the Business Arena at the time of its creation.
   
     > [!IMPORTANT]
     >
     > The email address must be exactly the same as the address entered in the agreement. If it differs in any way, the connection will not be established.
   * The bank agreement number - [the 14 digit CIN number](#to-find-the-cin-number-in-seb).
5. After entering the sign-in information, click **Next** to complete the setup.

### To find the CIN number in SEB

To integrate with Continia Banking, you must provide a 14-digit CIN number. Follow the steps below to locate the CIN number in SEB.

To find the CIN number in SEB:

1.	Login to SEB's Business Arena (Netbank) using an admin account.
2.	Navigate to **C&I Online** and select **Authorizations** > **Users**
3.	Use the **Search** to find the Admin name and select it.
4.	Under **Company with right to order digipass**, you will see the Company Name and the 14-digit CIN number. This number is required to establish the connection with Continia Banking.

