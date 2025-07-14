---
title: Enabling the reimport of bank statement files in Continia Banking
description: Learn how to enable reimporting of bank statement files
date: 12-02-2025
id: CB-183
lang: en
---

# Enabling the reimport of bank statement files

In Continia Banking, imported bank statement files are initially moved to the File Archive. They are then sent to Continia Online for conversion into the Continia Banking transaction format. This process ensures that the files are correctly formatted for use in the system. However, there may be cases where a reimport is necessary—for example, if critical information is missing or the file conversion did not process correctly.

To enable reimporting bank statement files, a setting in the **Continia Banking Setup** allows you to overwrite existing transactions. When this setting is activated, previously imported lines will be deleted and reimported if the Message ID matches, ensuring it is the same file. Additionally, the Bank Transaction Header and its lines will only be reimported if the **Imported To Company** field is blank on both the header and at least one of the related lines.

> [!NOTE]
>
> Currently, this feature is available for CAMT.053 and CAMT.054 files only. 

To allow reimporting of bank statements:
1. Search ({{search}}) for and select **Continia Banking Setup**.
2. On the action bar, select **Actions** > **Troubleshooting**.
3. On the **Troubleshooting** page, enable **Allow Files Reimport**. During reimport, the existing Bank Transaction Header and all associated lines are deleted before the file is imported again.

> [!IMPORTANT]
> Bank statement lines will only be overwritten if the **Imported To Company** field is not set. If this field is populated, the lines will remain unchanged.