---
title: Using CSV Ports
date: 07-11-2024
description: Learn how to use CSV ports.
id: CF-55
lang: en
---

# Using CSV Ports

Using CSV ports in Microsoft Business Central is advantageous due to their simplicity, universal compatibility, and ability to handle large data volumes efficiently. They allow flexible data mapping and transformation, reducing the need for developer support and enabling quicker setup for regular data tasks. CSV ports also facilitate compliance and auditing by providing an easy way to export records. Finally, CSV files are ideal for integration with other systems, enhancing Business Central's interoperability across different platforms.

## To create a CSV port for data import or export

To set up a CSV port, follow these steps:

1. Choose the {{search}} icon, search for **CSV Ports**, and choose the related link. 
2. On the action bar, select **New**. 
3. In the **General** FastTab, enter a code and a description for your new CSV port. The **Code** field is mandatory. 
4. In **Direction**, choose whether this is a port for data import or export.
5. In the following fields, you can enter or change a value to define how the data is structured. Not all fields need to have a value. 

| Field                     | Description                                                  |
| ------------------------- | ------------------------------------------------------------ |
| Table                     | Select the table in Business Central that the CSV port will interact with. This determines where data is imported to or exported from. |
| Table Caption             | Enter a descriptive caption for the selected table to help identify the data purpose and context within the port. |
| Text Format external File | Choose the text format for the external file. The options are: MSDos, Windows, UTF8, and UTF16 |
| Fixed Column Position     | Specify if columns in the CSV file have fixed positions. This setting allows the CSV port to treat each column consistently based on its exact position rather than by name or type. |
| Length of Line            | Define the maximum character length per line. This helps manage large data rows and avoid errors in CSV files with varying line lengths. |
| Separator                 | Enter the separator type used in your CSV (Comma-Separated Values) files. The role of a separator is to demarcate two distinct entities so that they can be distinguished. These characters separate fields of data within each line. |
| Delimiter                 | Delimiters are used when files contain both commas as separators and descriptions with embedded commas. |

From here on, the fields you need to fill in depend on whether you're creating a CSV port for import or export.

### To create a CSV port for import

If you chose **Import** in **Direction** in the **General** FastTab, the CSV Port Card will display the **Import** FastTab.

Fill in the following fields where needed:

| Field                             | Description                                                  |
| --------------------------------- | ------------------------------------------------------------ |
| Date Format                       | Enter the date format used in your CSV file. This setting is used during file import to ensure the correct formatting of the posting date. The date format is based on the [.NET DateTime format](https://learn.microsoft.com/en-us/dotnet/standard/base-types/custom-date-and-time-format-strings). For example, ddMMyyyy. |
| Decimal Separator                 | Specify the character used as a decimal point. For example, period or comma. |
| With direct Gen. Journal Import   | Enables direct import into the General Journal.              |
| Check if Gen. Jnl. Batch is empty | Verifies that the General Journal Batch is empty before import to prevent accidental overwrites of existing data. |
| Open Gen. Journal Batch           | Automatically opens the General Journal Batch after import, allowing immediate review and editing of the imported data. |
| Skip Header Lines                 | Enter the number of header lines to skip in the CSV file, typically to avoid importing column headers or metadata rows. |
| Skip Footer Lines                 | Enter the number of footer lines to skip in the CSV file, useful if there are additional notes or metadata at the end of the file. |
| Run OnModify / OnInsert triggers  | Enables data triggers that run actions when records are modified or inserted during import, such as validating or recalculating values. |
| Execute OnValidate triggers       | Triggers field-level validation logic during import, ensuring imported data adheres to Business Central’s data integrity rules. |
| Amounts                           | Specifies a setting for amounts: As saved, Absolute, or Change Sign. |
| Filter string                     | Enter criteria to filter rows during import, allowing only data that matches the specified criteria to be imported. |
| Use Filter to exclude             | Specify if data is to be excluded during import based on a filter, preventing rows that match certain values from being included in the data import. |

### To create a CSV port for export

If you chose **Export** in **Direction** in the **General** FastTab, the CSV Port Card will display the **Export** FastTab.

Fill in the following fields where needed:

| Field                    | Description                                                  |
| ------------------------ | ------------------------------------------------------------ |
| Date Format              | Enter the date format used in your CSV file. This setting is used during file import to ensure the correct formatting of the posting date. The date format is based on the [.NET DateTime format](https://learn.microsoft.com/en-us/dotnet/standard/base-types/custom-date-and-time-format-strings). For example, ddMMyyyy. |
| Decimals Format          | Define the format for decimal numbers in your CSV file, specifying how many decimal places to include. This setting helps maintain consistency in number precision across data exports. |
| Decimal Separator        | Specify the character used as a decimal point. For example, period or comma. |
| Thousands Separator      | Specify the character to use as a thousands separator in exported numbers. |
| Format of boolean fields | Choose the format for exporting boolean fields, "True/False," "Yes/No," or "1/0". |
| Format Option Values     | Set how option values should be formatted in the export, either as values or as text. |
| Export Field Names       | Select whether to include field names as headers in the exported file. This is useful when the CSV file requires column headers for easy identification or compatibility with other systems. |

### To import data using a CSV port

To use a CSV port to import data to Business Central, carry out the following steps:

1. Choose the {{search}} icon, search for **CSV Ports**, and choose the related link. 
2. Select the CSV port you want to use. 
3. In the action bar, select **CSV Port** > **Import/Export**.
4. Select **Click here to browse** to select the file you want to import.

### To export data using a CSV port

To use a CSV port to export data from Business Central, carry out the following steps:

1. Choose the {{search}} icon, search for **CSV Ports**, and choose the related link. 
2. Select the CSV port you want to use. 
3. In the action bar, select **CSV Port** > **Import/Export**.
4. Select **Yes** to download the created file.

<style>

 .content table tr td:nth-child(1) {

 width: 200px;

 }

 .content table tr td:nth-child(2) {

 width: 600px;

 }

</style>
