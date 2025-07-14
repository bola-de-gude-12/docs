---
title: Onboarding ABN AMRO for Continia Banking
description: Information about ABN AMRO and how to set up direct communication.
date: 11-07-2025
id: CB-251
lang: en
---

# Onboarding ABN AMRO

This walkthrough explains how to establish direct communication with ABN AMRO. It includes the requirements and instructions on preparing and establishing the connection. 

For more information about connecting to ABN AMRO through Bizcuit, refer to the [Onboarding through Bizcuit](@CB-250) article.

ABN AMRO has two kinds of online banking services, and they both have some payment limitations related to international payments:

* **Internet Banking Business** - cross-border payments can only be done through a manual file upload or manually entered in the banking environment.
* **Access Online** - supports cross-border payments through direct communication, but only as single payments.

## Requirements

To use direct communication for ABN AMRO, you require:

* **A TLS certificate, certificate password, and private key** - see the [To obtain a TLS certificate](#to-obtain-a-tls-certificate) section for more information about how to get a TLS certificate.

* **ABN AMRO API client ID and API key** - see the [To request production access](#to-request-production-access) section for more information on how to set up an ABN AMRO account and request access to production. 

  

## To prepare to connect to ABN AMRO

To establish direct communication between Continia Banking and ABN AMRO, you must register at ABN AMRO, set up the banking API agreement, and obtain a TLS certificate. 

> [!NOTE]
>
> The certification process with ABN AMRO may take up to 14 days, so it is important to start well in advance.

### To obtain a TLS certificate

To connect to ABN AMRO using direct communication, you require a Transport Layer Security (TLS) certificate accepted by ABN AMRO bank. TLS certificates secure internet connections by encrypting data sent between your browser, the website you’re visiting, and the website server to ensure that data is transmitted privately without modifications, loss, or theft. Upon purchasing the certificate, you will receive a private key, which is essential for the onboarding process.

The TLS certificate requirements:

* A TLS certificate of the type Organisation Validation (OV) or Extended Validation (EV) issued by one of the following trusted Certificate Authorities. It is necessary to choose a TLS certificate from one of the following authorities, as mandated by ABN AMRO: 

  * DigiCert + QuoVadis
  * Sectigo
  * Entrust
  
  > [!NOTE]
  >
  > Please note that these requirements may change. For more information, go to the [ABN AMRO Developer Portal](https://developer.abnamro.com/) and select **API Products** > **Business Account Payments Overview** > **Requirements.**
  
* No wildcard or character.

* The organization name on the certificate must be the same as the name of the API contract holder.

* The certificate format must be .crt.

  > [!NOTE]
  >
  > If you receive a .pfx file from a certificate provider that contains both the certificate and private key, it is recommended to contact the certificate provider and request the certificate and private key separately as .crt and .txt files. Next, you must assign a password to the certificate. 

Acquiring a TLS certificate can vary depending on the certificate provider. To ensure you acquire the private key, certificate, and certificate password correctly, contact your certificate provider. Typically, the private key is generated before the certificate is issued. Once the certificate is ready, you will receive a download link to obtain it. 

Once you have completed these steps, you will have access to the following:

-	TLS certificate
-	TLS private key 
-	TLS certificate password

### To create an ABN AMRO developer account

To use an ABN AMRO API product, you must create an account and request access to production.

To create an ABN AMRO developer account:

1. Go to the [ABN AMRO Developer Portal](https://developer.abnamro.com/) and select **Sign up**.
2. Enter your details, and select **Create new account**. 

3. ABN AMRO sends you an email that contains an activation link. Select the link from the email to proceed with the activation process.

### To request production access
To establish direct communication between Continia Banking and ABN AMRO, you must set up a banking API agreement on the services **Business Account Payment API** and **Business Account Insight API**. 

To request production access:
1. Log in and select the stack icon on the top right side of the webpage.
   ![Stack icon ABN AMRO developer portal](/images/CB/ABN-production-access.png)
2. Select **Request production access** > **Account APIs**. 
3. Select the **Business Account Insights** and **Business Account Payments**.
   
   ![Account APIs](/images/CB/ABN-production-access-selection.png)
4. Depending on your setup, select the banking service **Internet Business Banking** (*Internet Bankieren*) or **Access Online**.
5. Select **Next**.
6. Enter the following details:

   * Chamber of Commerce number
   * All the IBANs that you want to connect to the APIs
   * Contact information
   * Indicate whether you want to allow digital signing.
7. Upload the certificate in .CRT format and select **Next**. 
8. Under **API Usage**, enter the following information:
   * **Business account insights** - estimate the number of API calls and the total amount of monthly transactions. These estimations are provided as indications and do not need to be exact. They are meant to give ABN AMRO a general idea and will not affect costs.
   * **Business account payments** – estimate the number of API calls and the total amount of monthly single or batch payments initiated. These estimations are provided as indications and do not need to be exact. They are meant to give ABN AMRO a general idea and will not affect costs.
   * **Use case** - enter *Continia Software – Continia Banking*. 
9. Click **Preview**, verify all the info is correct, and select **Submit**. Once you have submitted the request for production access, the ABN AMRO support team will send a contract to the contact person listed on the form. After signing the contract, it will take ABN AMRO approximately a week to establish the connection. 

   Once the connection is established, you have access to:

   * **Client ID** - sent in an email by ABN AMRO.
   * **API key** - go to the [ABN AMRO Developer Portal](https://developer.abnamro.com/) and select the stack icon. Navigate to the **Operations** section and select **View**. Go to **Credentials** and the **API key** field. This key is required for setting up the connection in Continia Banking. 
     ![ABN API key](/images/CB/ABN-api-key.png)


## To establish the connection with ABN AMRO

After completing the [necessary preparations](#to-prepare-to-connect-to-abn-amro) and obtaining the [TLS certificate](#to-obtain-a-tls-certificate), you should have the following information available for the onboarding process:

| Item                 | Description                                                  | Location                                                     |
| -------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| TLS certificate      | .crt file that contains the TLS certificate. This file contains the public key and other information about the certificate. | After purchasing a [TLS certificate](#to-obtain-a-tls-certificate), you will receive a file from the provider. |
| Private key          | .txt file that contains the private key. This file contains the private key that matches the public key in the certificate. The private key is kept secret and is used to decrypt data encrypted with the public key. It is a crucial TLS  setup component and must be kept secure. | After purchasing a [TLS certificate](#to-obtain-a-tls-certificate), you will receive the private key from the provider. |
| Certificate password | The password for the TLS certificate. Some certificate authorities may provide a password to protect the private key file. This password adds an extra layer of security. | After purchasing a [TLS certificate](#to-obtain-a-tls-certificate), you will receive the password from the provider. |
| Client ID            | Your username for the ABN AMRO API. This ID is required for setting up the connection in Continia Banking. | Sent to you in an email by ABN AMRO. See [To request production access](#to-request-production-access) for more details. |
| API key              | The key for the ABN AMRO API. This key is required for setting up the connection in Continia Banking. | You can find the **API key** by selecting the stack icon. Navigate to the **Operations** section and select **View**. Go to **Credentials** > **API Key**. See [To request production access](#to-request-production-access) for more details. |

To set up direct communication with ABN AMRO:

1. Search ({{search}}) for and select **Bank Account Setup**.
1. Select **Next** to start the assisted setup.
1. On the **Bank System** field, select ABN AMRO and click **OK**.
1. Click **Next** to continue.
1. Upload the certificate and the private key and enter the certificate password, Client ID, and API key. Once the setup is completed, the connection to the bank will be successfully established.
1. Click **Next**. Now, you can make payments and download account statements.
