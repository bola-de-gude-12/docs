---
title: Expense Management Customizing Storage
date: 22-08-2022
description:  How to customize your Expense Management storage by extending or overruling the way documents are stored and fetched.
id: EM-92
lang: en
---

# Customizing your Storage

Expense Management provides support for three different storage models: **File System**, **Database**, and **Azure Blob Storage**. But it's also possible for you to customize your storage by extending or overruling the way documents are stored and fetched in Expense Management. You can overrule or extend the existing behavior using four different publisher events that are provided in the codeunit **CEM Doc. File Events**:

* **SetAttachment**: Invoked when a file is requested to be stored.
* **GetAttachment**: Invoked when a file is requested.
* **HasAttachment**: Invoked when the existence of a file is checked.
* **ClearAttachment**: Invoked when a file deletion is requested, for example when a document related to the relevant file is deleted or imported.

PDF documents are split into pages that are displayed in the addin. You can interact with the images by using the following events:

* **SetPage**: Invoked when a file is requested to be stored.
* **GetPage**: Invoked when a file is requested.
* **HasPage**: Invoked when the existence of a file is checked.
* **ClearPage**: Invoked when a file deletion is requested, for example when a document related to the relevant file is deleted or imported.

In several localizations, document signing is a necessity. In these cases, the following events can be used for interaction with digitally-signed PDF documents:

* **SetPDF**: Invoked when a file is requested to be stored.
* **GetPDF**: Invoked when a file is requested.
* **HasPDF**: Invoked when the existence of a file is checked.
* **ClearPDF**: Invoked when a file deletion is requested, for example when a document related to the relevant file is deleted or imported.

In Expense Management, all files are initially downloaded from Continia Online in a buffer called Attachment Inbox. This is why all events are also available for inbox processes as well. These are:

* **SetInboxAttachment**: Invoked when a file is requested to be stored.
* **GetInboxAttachment**: Invoked when a file is requested.
* **HasInboxAttachment**: Invoked when the existence of a file is checked.
* **ClearInboxAttachment**: Invoked when a file deletion is requested, for example when a document related to the relevant file is deleted or imported.
* **SetInboxPage**: Invoked when a PDF page is requested to be stored.
* **GetInboxPage**: Invoked when a PDF page is requested.
* **HasInboxPage**: Invoked when the existence of a PDF page is checked.
* **ClearInboxPage**: Invoked when a PDF page deletion is requested, for example when a document related to the relevant file is deleted or imported.
* **SetInboxPDF**: Invoked when a digitally signed PDF is requested to be stored.
* **GetInboxPDF**: Invoked when a digitally signed PDF is requested.
* **HasInboxPDF**: Invoked when the existence of a digitally signed PDF  is checked.
* **ClearInboxPDF**: Invoked when a digitally signed PDF  deletion is requested, for example when a document related to the relevant file is deleted or imported.

All of the above methods implement a *handled* pattern, which enables programmers to overrule or extend the behavior. If *Handled* is set to *true*, Expense Management won't do anything, as it expects the file operation to be handled by the extension code. If *Handled* isn't set, the code will carry out the file operation as implemented according to the storage model selected in the Expense Management setup. In this way, it's possible to extend and store a subset of files externally and still let Expense Management handle the file storage. 

All of the methods have the following arguments:

* EMAttachment: A reference to the attachment record that has all the information about the attachment.

* Success: A Boolean value indicating if the operation was successful. This value is only propagated if the *Handled* value is also set to *true*.

  

**OnSet()** and **OnGet()** have one additional parameter, *TempFile*, which is a **CDC Temp File** record. The **CDC Temp File** record is to be considered a file object, as it contains file information and the content of the file. The **Data** field on the record contains the data of the file that's either stored or fetched. So when you subscribe to **OnSet()**, the **Data** field will contain the content of the file that's to be stored, whereas for **OnGet()**, the content of the file that's requested should appear in the **Data** field.

> [!NOTE]
> Because the procedures above are invoked by various routines in Expense Management, such as document import, there must be no errors in the executing code, as this would break or stop the existing functionality.

> [!IMPORTANT]
> Extending the storage of documents comes with a risk. Continia Software can't be held accountable for documents lost or missing when this part of Expense Management is extended.