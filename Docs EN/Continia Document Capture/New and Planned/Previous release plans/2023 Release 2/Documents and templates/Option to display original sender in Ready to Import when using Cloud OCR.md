---
title: Option to Display Original Sender in Ready to Import When Using Cloud OCR
date: 29-11-2024
description:
id: DC-302
lang: en
---

# Option to Display Original Sender in Ready to Import When Using Cloud OCR

| Feature | Public preview | General availability online |
| --- | :-: | :-: |
| Option to display original sender in **Ready to Import** when using Cloud OCR | - | {{checkmark}} Oct 2023 |

## Business value

This feature will provide more transparency by enabling you to display the email address of the original sender of documents in Continia Document Capture (typically a vendor), rather than that of an intermediary mailbox or similar.

## Feature details

For all documents that you want to import into Document Capture using Continia Cloud OCR, Continia recommends that you first send them to a separate mailbox which then forwards them to the system-generated Continia email address that imports them into Document Capture. While this approach enables you to create a catchier email address to share with vendors for document import, it also has the side effect that the email address of the mailbox – rather than that of the original sender – is displayed on the **View - Display Documents** page (which is accessible from the **Ready to Import** page).

If you'd rather want this page to display the original sender's email address, this new feature will enable you to do just that. The feature will also work for other scenarios than the one outlined above – that is, for any situation in which documents are sent via some kind of intermediate link rather than directly from the original sender.

> [!NOTE]
> An article describing the Document Capture section in the Business Central Role Center including information about the above feature will be published as soon as possible following the release of Continia Document Capture 2023 R2.

## Related information

[Configuring Cloud OCR](@DC-141)  