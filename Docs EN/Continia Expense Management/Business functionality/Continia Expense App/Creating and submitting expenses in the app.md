---
title: Creating and submitting expenses in the Expense Mobile App
date: 12-08-2025
description: Learn to submit an expense using the Expense Mobile app
id: EM-167
lang: en
---

# Creating and submitting expenses in the Expense Mobile App

Create and manage expenses with the Continia Expense Mobile App which automatically synchronizes with Continia Online using [job queues](@EM-65). When you submit an expense. it transfers through Continia Online, with the next synchronization to Business Central. The app's AI-powered receipt scanner increases efficiency by automatically extracting and filling-in essential details from receipts, such as the Amount, Currency, Document Date, Merchant, and VAT or GST amount. This automation significantly reduces manual data entry and lowers the risk of errors. Additionally, an auto-fill feature reuses recognized information across similar expenses, further reducing repetitive entries and saving time.

For a quick overview of how the autofill feature can improve the speed and accuracy of submitting expenses, watch the video below or enroll in the [Expense Management learning path](https://learn.continia.com/get-started-using-expense-management).


<iframe src=https://player.vimeo.com/video/878028363?h=4b82cbc83a&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479 width="560" height="315" frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write; encrypted-media" title="Autofill Expense Details with Continia Copilot"></iframe>

To create and submit an expense in the Expense Mobile App:

1. Open the Expense Mobile App, and select **New Expense** or **Create**.

    > [!NOTE]
     > If your account is set up with private and company cards, you are prompted to select the expense payment type.

1. Upload an image of the receipt or invoice. The AI-powered receipt scanner automatically identifies and populate key details, saving time and minimizing manual entry errors. You can review and adjust any details entered by the AI scanner or auto-fill feature and add information to any other relevant fields. To add an image of the receipt:
   - Capture a picture of your receipt by tapping the camera icon. Take a photo of the receipt to attach it to the expense.
   - Alternatively, you can attach an image from your camera roll by tapping the paperclip icon and selecting the receipt image.

1. The fields that are visible in the app vary depending on your setup. To enter or change information, use the following fields:


| Field<a href="#footnote-1"><sup>1</sup></a> | Required field | Description                                                  |
| ------------------------------------------- | ---------------------------------------------------- | ------------------------------------------------------------ |
| Amount                                      | {{checkmark}}                                        | Enter the amount and select the currency from the drop-down list. The list contains all the currencies available in Business Central. To access your commonly used currencies, mark them as favorites by selecting the star next to each currency. These marked currencies appear at the top of the list whenever you submit a new expense.<br />To enable an automatic currency selection, based on your current location, you must grant the expense app access to your location. After you give the app access to your location, it automatically chooses the currency associated with your current location. |
| Registration Date                           | {{cross}}                                            | Enter the date. By default, the date is set to the current date. |
| Payment Type                                | {{checkmark}}                                        | If your Expense Mobile App is set up with credit card specifications, the app prompts you to choose whether the expense is Cash/Private Card or a Corporate credit card expense. |
| Expense Type                                | {{checkmark}}                                        | Expense Types are pre-set in Business Central, and each type has a designated posting definition. Choose the appropriate code to categorize your expenses, the code associates it with the corresponding posting setup. The expense types that are available in the app depend on your setup. For more information, see [Setting up expense types](@EM-41).<br/>Similar to currencies, you can mark frequently used expense types as favorites by tapping the star icon. These favorite types appear at the top of the screen when selecting an expense type for a new expense. |
| Description                                 | {{checkmark}}                                        | Enter a description of the expense. After you've assigned a description to an expense, you cannot overwrite it later. |
| Merchant | {{cross}} | If you add an expense document, such as a receipt or an invoice, the merchant name is automatically added. This field is only visible if you've added an expense document. |
| Project                                     | {{cross}}                                            | Projects are pre-set in Business Central. Choose the appropriate code to assign your expenses to a specific project. Whether this field is visible or not depends on the setup of your Expense Mobile App. |
| Admin Comment                               | {{cross}}                                            | View communication comments between the expenses user, admin, and approvers. |
| Job No.                                     | {{cross}}                                            | You can assign expenses to a specific job. For more details, see [Using Jobs and Job Tasks](@EM-170). Whether this field is visible or not depends on the setup of your Expense Mobile App. |
| Job Task No.                                | {{cross}}                                            | You can assign expenses to a specific job task. For more details, see [Using Jobs and Job Tasks](@EM-170). Whether this field is visible or not depends on the setup of your Expense Mobile App. |
| Add allocation lines                       | {{cross}}                                            | You can split expenses into different lines. Tap **Plus** (+), to split the expense, slide the toggle to add the amount or percentage, and specific details, such as department and project, for each part of the expense separately. Using Allocation allows you to precisely allocate expenses and maintain accurate records for better financial tracking and reporting. Whether the Department and Project fields are visible or not depends on the setup of your Expense Mobile App. |
| Add to report             | {{cross}}                                            | Use this option to include the expense within a group of documents. An expense report typically consists of multiple related financial documents, such as invoices, receipts, or other expense items. By adding your expense to an expense report, you are grouping it with these other documents for a specific purpose or transaction. |

   <small style>
      <div class="footnotes">
      <hr />
    <ol>
    <li id="footnote-1">The available fields depends on your setup.</li>
    </ol>
   </div>
   </small>

4. Submit the expense. After you complete all of the required information, swipe the **Submit** slider to finalize. Your expense is now ready for the approval process. 

To return to an expense that has not yet been submitted, go to the app’s home page and tap **Open**. 

## Related information

For further information relating to this article, see:

[Setting up job queues](@EM-65)  
[Setting up expense types](@EM-41)  
[Using jobs and job tasks](@EM-170)  