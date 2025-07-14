---
title: Customizing the Sender of Outgoing Emails
date: 17-11-2020
description:  New functionality that enables users to customize the sender of outgoing emails in Continia Document Output
lang: en
---

# Customizing the Sender of Outgoing Emails

| Feature | General availability on-premises | General availability online | Public preview |
| --- | :-: | :-: | :-: |
| Customizing the sender of outgoing emails |    {{checkmark}} Feb 15, 2021 | {{checkmark}} Feb 15, 2021  | - |

##Business value
Three new **From E-Mail** fields have been added to the email template card. These fields enable you to decide who should appear as the sender of the emails you send using Continia Document Output. This is useful if, for example, you'd like all replies to go to someone else than yourself.

##Feature details
The following fields will be added to the email template card:
* **From E-Mail**
* **From E-Mail Address**
* **From E-Mail Name** (only editable in the on-premises version)

In the **From E-Mail** field, you can determine where the displayed sender should be sourced from. You can choose between the following three options:
* **Fixed**: Selecting this option enables you to enter a fixed name and/or a fixed email address to be displayed as the sender of outgoing emails. The name and email address can be entered in the two template fields mentioned further below or in the SMTP setup.
* **User Setup**: When you select this option, the email address that's displayed as the sender in outgoing emails will be based on the user setup.
* **Salesperson from User Setup**: When this option is selected, the email address that appears as the sender will be that of a salesperson, and it will be found using the salesperson code in the user setup.

The following two related fields enable you to specify the exact name and email address of the displayed sender. Note that these fields only apply if you've selected **Fixed** under **From E-Mail** (see above):
* **From E-Mail Address**: In this field, you can enter the email address that should be displayed as the sender of outgoing emails.
* **From E-Mail Name**: Here you can enter the name of the person that should appear as the sender of outgoing emails. The entered name will be displayed in all sent emails together with the email address entered under **From E-Mail Address**, like this: *Name Nameson \<namenameson<span>@</span>company.com\>*