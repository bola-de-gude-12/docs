---
title: Frequently Asked Questions Document Output
date: 21-06-2024
description: Frequently asked questions about Continia Document Output
id: DO-103
lang: en
---

# General FAQ
In this section, you can find answers to some of the most frequently asked questions about Continia Document Output. The answers provide information on anything from availability to zero-cost trials and also include multiple links to other sites with more information.

## Is Document Output available in my country?
Document Output is available in a range of countries and languages. To access the full lists, use the links below:

* [Country/Regional Availability and Supported Languages](@DO-1) (app)
* [Country/Regional Availability and Supported Languages for FOB](@DO-2) (FOB)

## How do I get Document Output?
Continia works through a network of specialized partners who are also Microsoft Dynamics 365 Business Central experts. Contact your Continia partner to get started quickly.

See also: [Finding a reseller of Continia Document Output](/Continia Document Output/Getting Started/Resellers and Partners/Find a Reseller.md).

You can also start with a free 30-day trial or set up a sandbox environment. For more information, see [Continia Document Output Trials and Subscriptions](/Continia Document Output/Getting Started/Trials and Subscriptions.md).

## Where do I go if I have questions?

If you have any questions about Document Output that you can't find answers to in this documentation, you’re more than welcome to ask your Continia partner.

Find more information here [Help and Support](/Continia Document Output/Getting Started/Help and Support.md) and here [Resellers and Partners](/Continia Document Output/Getting Started/Resellers and Partners/Overview.md).

## What does it cost to use Document Output?

The cost of using Document Output for Microsoft Dynamics 365 Business Central online depends on how many modules you choose and how many posted transaction lines you send to and receive from your bank. For Business Central on-premises, the cost is based on other parameters, which you can find in the link below.

You can find detailed information on pricing for both online and on-premises usage [here](https://www.continia.com/pricing/).

## Why is my Document Output not activated after I moved NAV to a new server?

There are two possible solutions: 

### Solution 1
1. If it is a FOB installation, run the page **6192837** and mark the **Exclude DB info.from activa.** field. 
2. Restart the NAV client. 

### Solution 2

1. Open Continia Solution Management and update the database/server.

## Can I use the print service on the demo portal?

The print service is specifically designed for Business Central cloud solutions. It doesn't work in the demo portal since the portal is a virtual environment without the capability to connect to local printers. As a contained system, it lacks the connection to enable printing functionalities.

## Where can I update many or all of my customers?

In case you want to update your customers, but more than just one at the time, you can do it in the following menu: **Document Output Customer Setup List**.
In the action bar, select **Update Customers**. In this menu, you can update a certain group of customers or all customers. You select the customers by using filters.

Currently, you can change the following aspects of customers:

- Automatic statement
- Manual/Automatic
- Send Statement Code
- First statement start date
- Output Profile

The last thing to remember is to enable the toggle **Change Existing setup** to have your changes take effect.

## Why is the Resend button grayed out?

This issue may occur in production environments, for instance in BC v22.5, and also sandboxes based on BC v23.1. When it happens, the **Resend** button is grayed out on Document Output Email, and it can affect all users, including users with the SUPER permission set.

Here's how to fix it:

Open the email, and then click on the message part.
Now resending the email will be possible.

Explanation: From a code perspective, the email editor must have been initialized as it contains the email, and modifications to the html (with reply/resend information in the top) are displayed in it. You can minimize/close it again after it has been initialized, as there's still access to it afterwards.

## See also
[Country/Regional Availability and Supported Languages](/Continia Document Output/Development and Administration/Countries and Languages.md)  
[Finding a reseller of Continia Document Output](/Continia Document Output/Getting Started/Resellers and Partners/Find a Reseller.md)  
[Trials and Subscriptions](/Continia Document Output/Getting Started/Trials and Subscriptions.md)  
[Resources for Help and Support](/Continia Document Output/Getting Started/Help and Support.md)  
[Resellers and Partners](/Continia Document Output/Getting Started/Resellers and Partners/Overview.md)  