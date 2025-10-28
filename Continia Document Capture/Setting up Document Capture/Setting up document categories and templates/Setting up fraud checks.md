---
title: Setting up fraud checks in Document Capture
date: 12-09-2025
description:  
id: DC-213
lang: en
---

# Setting up fraud checks

To minimize fraud, you can configure Continia Document Capture to check if certain data captured in incoming documents actually exists for the vendors who sent the documents. Document Capture can perform such checks for the following data:

* Bank account numbers
* VAT numbers
* Phone numbers

For example, if you set Document Capture up to check for bank account numbers and it captures a bank account number in an imported document, it then validates that number against the following fields on the **Vendor Bank Account Card** (accessed from the vendor card):

* **IBAN**
* **Bank Sort Code** (bank branch) + **Bank Account No.**
* **Bank Account No.** + **Bank Sort Code** (bank branch)

If the values of any of these fields match the captured value, no fraud is suspected. But if there's no match, an error-type comment is displayed in the **Comments** section of the document journal to indicate that the document may be fraudulent.

Similarly, any captured VAT numbers are validated against the **VAT Registration No.** field on the vendor card, whereas any captured phone numbers are validated against the **Phone No.** field on the vendor card. If the captured values don't exist or are different from the corresponding values on the vendor card, an error-type comment is displayed in the document journal to indicate fraud.

> [!NOTE]
> For all of the above, the feature validates digits only. All other characters are ignored in the fraud checks (even though the characters are in fact captured and added to the relevant template fields in the **Document Header** section).

## To set up fraud checks on a vendor template

In order to set up fraud checks for bank account numbers, VAT numbers, or phone numbers in incoming documents from a certain vendor, follow these steps:

1. Search ({{search}}) for and select **Document Categories**.
1. Click the code of the relevant document category – in this case **PURCHASE** – to open the document journal.
1. If Document Capture has automatically identified a vendor for the document, the number of the identified vendor is displayed in the **Vendor** field of the document list. If no vendor has been identified, assign a vendor manually as described under [Changing a document’s associated vendor](@DC-71#changing-a-documents-associated-vendor).
1. On the action bar, click **Template** > **Add Template Field** to open the **Template Fields** page.
1. In the list of fields, scroll to the **Header Fields** section, and then find and select the field(s) you want to use for fraud checking. You can choose between the following fields for this purpose:
   * **Vendor Bank Account No.**
   * **VAT No.**
   * **Vendor Phone No.**
1. Click **OK** to add the field(s) and return to the document journal.
1. The selected fields are added to the **Document Header** section of the document journal. Select the field you want to set up first.
1. Use your mouse to select exactly what text in the document should be captured for the chosen template field: To set the caption, right-click and hold to draw an orange box around the relevant text in the document viewer.
1. Similarly, to set the corresponding value for the chosen template field, left-click and hold to draw a blue box around the relevant text in the document viewer.
1. The selected text is added to the template field in the **Document Header** section. Verify that it has been captured correctly.
1. Repeat steps 7-10 for any additional fields you added in step 5 above.

For all incoming documents from this vendor, Document Capture will now validate any captured values for the added template fields against the corresponding values on the vendor card in order to prevent fraud.