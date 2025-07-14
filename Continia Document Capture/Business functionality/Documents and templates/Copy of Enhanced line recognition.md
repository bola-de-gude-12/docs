---
title: Enhanced line recognition in Document Capture
date: 30-05-2025
id: null
lang: en
description: A description of the enhanced line recognition in Document Capture.
---

# Enhanced line recognition

Building on top of line data captured by artificial intelligence (AI), Continia Document Capture is capable of capturing more data in the lines of incoming documents, and the captured data is considerably more accurate than before.

> \[!IMPORTANT] The functionality described in this article is only available if you use the **CDC Line Capture 2.0** line capture codeunit. To check this, open the template card of the relevant template, go to the **Codeunits** FastTab, and check the codeunit displayed under **Line Capture**. As of Document Capture 2024 R1, all newly created templates use this codeunit by default, while existing templates retain the older codeunit.
>
> You can assign the new codeunit to existing templates on your own responsibility. This should work well in the vast majority of cases, but it may affect the results and quality of the line capture under certain circumstances. If so, you can reapply the older codeunit to restore previous functionality.

The below video outlines the most important features of enhanced line recognition:

\


## To apply suggested improvements

To make these features readily available to you and assist you in applying them, Document Capture features an AI-based assistant that automatically identifies a number of line recognition areas for improvement – and then notifies you about them. If you select the notification, you're presented with a list of suggestions for how to update the assigned template in order to accurately capture more line details. You can then freely choose whether to apply these suggestions.

> \[!NOTE] If you use AI to recognize lines on the document card, suggestions to improve recognition will continue to appear – as long as the document values prompt a suggestion and the specific suggestion hasn't been disabled.

All suggestions are setup shortcuts intended to make Document Capture do what you want in terms of line recognition. This means that each suggested improvement can also be configured in the traditional way in the setup, as described in some of the other sections below.

> \[!NOTE] This guide doesn't describe all possible suggestions in any detail – only the process of applying them. Examples of possible suggestions include the following:
>
> * **Use AI as line recognition method** - see [To use AI line recognition](<Copy of Enhanced line recognition.md#to-use-ai-line-recognition>) below.
> * **Enable line capture to span multiple lines** - see [To capture lines spanning multiple rows](<Copy of Enhanced line recognition.md#to-capture-lines-spanning-multiple-rows>) below.
> * **Add rule to match item numbers** - this can, for example, be used to create a template field rule that only matches **No.** values containing capital letters and possibly digits, and with a minimum length of seven characters.
> * **Add rule to match decimal values** - this can, for example, be used to create a template field rule that only matches numbers using comma as the decimal separator, for the fields **Discount Amount**, **Line Amount**, and **Unit Cost**.

To use one or more suggestions made by the line recognition assistant:

1. Carry out steps 1-5 of the [guide for traditional line recognition](../../../Continia%20Document%20Capture/Business%20functionality/Documents%20and%20templates/@DC-147/#to-capture-line-fields) to open the document card.
2. If the feature identifies anything that it can improve in terms of line recognition, a notification appears at the top with a number of suggestions. Select **Show Suggestions** to open the **Template Suggestions** page.
3.  In the list of suggestions, locate the one(s) you want to apply, and then select the corresponding box(es) in the **Apply** column.

    > \[!TIP] To know more about a suggestion before you apply it, select **Show Details** in the rightmost column for that suggestion to open a dialog with more information. Select **OK** to close the dialog and return to the **Template Suggestions** page.
4. To close the page and apply the settings when you're done, select **Finish**.

The selected improvements suggested by the AI-based assistant are then applied. For an overview of all the suggestions you've applied, go to the action bar and select **Actions** > **Functions** > **Show Applied Suggestions**. This opens the **Template Suggestions** page, which provides a complete overview.

## To use AI line recognition

If Document Capture identifies a number of amounts that match the document total, it suggests that you use AI line recognition to expedite the process. The AI line recognition functionality is entirely optional, though, and it can be used in combination with [the traditional method](../../../Continia%20Document%20Capture/Business%20functionality/Documents%20and%20templates/@DC-147/). This means that you can manually capture any captions and values that the AI-driven line recognition feature has failed to identify, as well as override values that were captured incorrectly by the AI.

> \[!NOTE] This feature is available to all customers using the Continia Cloud OCR engine.

To capture the fields of a document using AI line recognition:

1. Carry out steps 1-5 of the [guide for traditional line recognition](../../../Continia%20Document%20Capture/Business%20functionality/Documents%20and%20templates/@DC-147/#to-capture-line-fields) to open the document card.
2. In the notification at the top of the page, select **Show Suggestions** to open the **Template Suggestions** page.
3.  In the list of suggestions, locate **Use AI as line recognition method**, and then select the corresponding box in the **Apply** column.

    > \[!TIP] You can also enable AI line recognition directly on the **General** FastTab: Go to **Recognize Lines**, and select **AI** in the dropdown menu.
4. Select **Finish** when you're done to close the page and apply the setting.
5. If the AI line recognition feature failed to recognize some of the line data, you can select the data manually yourself by following steps 6-9 of the [guide for traditional line recognition](../../../Continia%20Document%20Capture/Business%20functionality/Documents%20and%20templates/@DC-147/#to-capture-line-fields).

When all line data has been captured accurately by the AI feature and/or manually by you, the document is ready for further processing.

To override values captured incorrectly by the AI:

1. On the **Lines** FastTab, select the line field whose value you would like to override.
2. Left-click the area in the document that contains the correct value.
3.  Once you've manually selected a new value, you can also capture a different line caption.

    > \[!NOTE] Capturing a different line caption or overriding all line fields with manually selected values disables the AI-driven line recognition for the entire document.

## To capture lines spanning multiple rows

Some lines in purchase documents contain multiple rows of text. For example, the item number may be placed on a higher row than the item amount. Such layouts have proven difficult to capture using traditional line recognition, but they usually pose no problem for enhanced line recognition. If Document Capture detects a possible line-span issue, it suggests that you enable this feature to address the issue.

To capture lines that span multiple rows:

1. Follow the [guide for traditional line recognition](../../../Continia%20Document%20Capture/Business%20functionality/Documents%20and%20templates/@DC-147/#to-capture-line-fields) to open the document card, draw orange boxes around headers, and carry out line recognition.
2. If Document Capture determines that one or more lines in the document may span multiple rows, a notification appears at the top of the page with suggestions for line recognition improvements. In this notification, select **Show Suggestions** to open the **Template Suggestions** page.
3. In the list of suggestions, locate **Enable line capture to span multiple lines**, and then select the corresponding box in the **Apply** column.
4.  Select **Finish** when you're done to close the page and apply the setting.

    > \[!NOTE] This will enable the **Line Values Span Multiple Lines** field on the template card. You can also enable this directly yourself without using the notification provided by the assistant: On the document card, on the action bar, click **Template** > **Template Card** to open the template card. On the **General** FastTab, enable the **Line Values Span Multiple Lines** toggle.

The relevant values below each of the orange-boxed column headers are then automatically transferred to their corresponding fields on the **Lines** FastTab, for each line in the document. Also, the same values are enclosed in blue boxes in the document viewer. Note that you may have to apply additional suggestions in step 3 above (such as one or more rules) for Document Capture to determine exactly what values are relevant to capture.

## To use relative line capture

If an incoming document has a somewhat unusual layout – for example, one in which the lines span multiple rows – some line details are often not captured while others are. The line data that's not captured in the first attempt may now be captured using relative line capture.

Once you've defined where the lines are located in the document by capturing their most important details (for instance, by using the line-span feature described above), you can manually capture the remaining line details for one of the lines to let Document Capture know where to look for them in the other lines. Document Capture will then know how to capture the corresponding details in the other lines by searching in the same locations relative to the previously captured data.

You can also now define field captions and capture values at row level for each line, instead of at column level. This provides more flexibility than traditional column-based line capture and, in some cases, allows you to specify more accurately what you want to capture.

To capture a value using relative line capture:

1. Follow the [guide for traditional line recognition](../../../Continia%20Document%20Capture/Business%20functionality/Documents%20and%20templates/@DC-147/#to-capture-line-fields) to open the document card, draw orange boxes around headers, and carry out line recognition.
2. If some line details aren't captured due to an unusual document layout, you can capture them using relative line capture: On the **Lines** FastTab, in the list of lines, select the field whose value you want to capture, such as **Description**.
3.  In the document viewer, locate the corresponding text that you want to capture, and then left-click and hold the button to draw a blue box around the text.

    > \[!NOTE] For relative line capture to work, no column header caption must be defined for the value that you draw your blue box around. To clear the related caption, select the desired line field and right click an empty area in the document.

    > \[!TIP] If the field you want to capture a value for isn't available in the **Document Header** or **Lines** sections, you can add it by selecting the desired value in the document viewer.
    >
    > 1. Select a header or line field. Header fields can be selected from the document card or the document journal, while line fields can only be selected from the document card.
    > 2. Press **Ctrl** and select the desired value in the document viewer to open the **Assisted Template Field Setup Guide**. Note that values must be recognized with **Ctrl** and the left mouse button, and captions with **Ctrl** and the right mouse button.
    > 3. Select **Next > Template Field** to open the **Template Field List** and choose an existing field from the master template, or **Next > Create New** to create a custom field.
    > 4. When you're done, select **Finish** to return to the document card.
4. On the action bar, click **Home** > **Recognize Fields**. Document Capture takes note of the location of your blue-boxed value in relation to other previously captured values and then look for corresponding values in the same relative positions for other lines. The identified values are enclosed in blue boxes in the document viewer and automatically transferred to the corresponding field in the **Lines** FastTab, for each line in the document.
5. If some of the identified values are incorrect, you may be able to correct them using the newly introduced capability to define field captions at row level:
   1. On the **Lines** FastTab, locate the relevant field and select the three dots on the right side of the field to open the template field card.
   2. In **Line Caption Type**, select **Row** to identify field captions at row level, and then select **Close** to return to the document card.
   3. In the document viewer, locate the caption whose value you want to capture, and then right-click and hold the button to draw an orange box around the text.
   4. In the document viewer, locate the corresponding value that you want to capture, and then left-click and hold the button to draw a blue box around the text.
   5. On the action bar, click **Home** > **Recognize Fields**.

Document Capture takes note of the location of your blue-boxed value in relation to the orange-boxed caption and then look for corresponding values in the same relative positions for other lines. The identified values are enclosed in blue boxes in the document viewer and automatically transferred to the corresponding field on the **Lines** FastTab, for each line in the document.

## To fill empty fields based on formulas or other fields

In some business documents, certain values are implied, and their fields are therefore left empty for some of the document lines. For example, the first line in an invoice may refer to a related order number, but in the second invoice line referring to the same order number, this order number reference is then left out, because it can be inferred from the reference in the first invoice line. Such empty fields can now be autopopulated based on other fields (in this case, the corresponding field in the previous invoice line) or formulas.

To autopopulate empty fields based on fields or formulas:

1. Follow the [guide for traditional line recognition](../../../Continia%20Document%20Capture/Business%20functionality/Documents%20and%20templates/@DC-147/#to-capture-line-fields) to open the document card, draw orange boxes around headers, and carry out line recognition.
2. If a field is empty but its value could be inferred from other document data, go to the **Lines** FastTab and locate the empty field.
3. Select the three dots on the right side of the field to open the template field card.
4.  On the **General** FastTab, under **Advanced Recognition Settings**, go to **When Value is Empty** and then select one of the following options:

    | Option                            | Description                                                                                   |
    | --------------------------------- | --------------------------------------------------------------------------------------------- |
    | **Copy value from previous line** | Copies the value from the corresponding field in the previous document line.                  |
    | **Copy value from header field**  | Copies the value from a header field that you specify in the **Copy Value From Field** field. |
    | **Copy value from line field**    | Copies the value from a line field that you specify in the **Copy Value From Field** field.   |
    | **Use formula**                   | Calculates the value based on a formula that you specify in the **Formula** field.            |
5. If you selected **Copy value from header field** or **Copy value from line field** in step 4 above, the **Copy Value From Field** field appears. In this field, from the dropdown menu, select the field that you want to copy the value from.
6. If you selected **Use formula** in step 4 above, the **Formula** field appears. Select the three dots on the right side of this field to open the **Template Field List**, and then select the formula you prefer. Select **OK** to return to the template field card.
7. Select **Close** to return to the document card.
8. On the action bar, click **Home** > **Recognize Fields**.

Document Capture fills the empty field for all lines according to your setup.

## To capture only the parts of values that match a specific rule

To capture a specific type of values for a field, set up a rule for that field. Traditionally, such a rule might lead Document Capture to deem some of the captured values invalid, because they contain characters that don't match the rule. But with the addition of the **Capture Only Match** feature, you can filter out any such unwanted characters by specifying that Document Capture must capture only the part of the value that matches the rule.

For example, if you set up a rule to capture only digits, any captured values that contain digits but are enclosed in parentheses are dismissed as invalid if the **Capture Only Match** feature is disabled. When you enable this feature, Document Capture is able to filter out the parentheses and focus only on the digits that match the rule, resulting in the successful capture of the desired values.

To enable **Capture Only Match**:

1. Carry out steps 1-5 of the [guide for traditional line recognition](../../../Continia%20Document%20Capture/Business%20functionality/Documents%20and%20templates/@DC-147/#to-capture-line-fields) to open the document card.
2. On the **Lines** FastTab, locate the field that you want to set up a rule for, and then select the three dots on the right side of the field to open the template field card.
3. On the **General** FastTab, go to **Rule** and select the three dots on the right side of the field to open the **Field Rules** page.
4. Set up a rule, or use an existing one.
5. In the **Capture Only Match** column, select the box to enable the feature.

For the selected field, Document Capture only captures the part of each value that matches the rule you've set up.

## See also

[Working with paper and PDF documents](../../../Continia%20Document%20Capture/Business%20functionality/Documents%20and%20templates/@DC-71/)\
[Capturing header fields in a document](../../../Continia%20Document%20Capture/Business%20functionality/Documents%20and%20templates/@DC-110/)
