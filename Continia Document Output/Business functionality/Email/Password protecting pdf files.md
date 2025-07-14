---
title: Password Protecting PDF Files
date: 10-01-2025
description:  
id: DO-35
lang: en
---

# Password Protecting PDF Files

Sending emails with unprotected PDF file attachments can expose a vulnerability in your data security. To address this issue, one effective solution is to enhance the security of PDF files by protecting them with passwords. By sharing the password with the intended recipient, you can add an extra layer of protection to safeguard the information.

You can specify PDF passwords for both templates and customers.
<br>
<br>
<iframe src="https://player.vimeo.com/video/902199660?h=0574e7500a&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" width="560" height="315" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" title="DO Learn_3d PDF passwords and signatures"></iframe>  

This video is part of the course [Get started using Document Output](https://learn.continia.com/get-started-using-document-output) on Continia Learn.

### Password hierarchy

Passwords on customer/vendor cards take precedence over both passwords on individual template lines and the template itself, and passwords on individual template lines take presedence over passwords on the templates themselves. 

- Passwords on customer/vendor cards > 
	- Passwords on template lines > 
		- Passwords on the templates themselves.

### To specify a template-specific password

To apply a PDF password that is specific to a particular email template:

1. Select the {{search}} icon, enter **Email Templates**, and then select the related link.
1. Select the email template for which you want to enable a PDF password.
1. On the **Email attachments** FastTab, in **PDF Password**, specify a PDF password. Specify a PDF password in the provided field. When you set a PDF password for an email template, this password will be required to access any attached PDF files. This setup will protect all PDF files attached to emails sent using this template with the same password.

### To specify a customer-specific password

To apply a PDF password that is specific to a particular customer:

1. Select the {{search}} icon, enter **Customers**, and select the related link.
1. Select the customer for which you want to use a PDF password.
1. On the **Document Output** FactBox, select the three dots to the right of **Output Profile**.
1. On the **General** FastTab, specify the PDF password that will be used for all templates when documents are sent to this customer.

   > [!NOTE]
   > This feature does not include functionality for sharing passwords with customers. 

### To specify a line-specific password

To apply a PDF password for a particular email template line:

1. Select the {{search}} icon, enter **Email Templates**, and then select the related link.
1. Select the email template in which you want to enable a PDF password for one or more email template lines.
1. Select the line for which you want to set a PDF password.
2. In **PDF Password**, specify a password.

Setting a password for a specific email template line will *override* the template-specific password for that line.
