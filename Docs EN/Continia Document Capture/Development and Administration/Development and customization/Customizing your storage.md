---
title: Customizing storage in Document Capture
date: 16-06-2025
description:  How to customize your Document Capture storage by extending or overruling the way documents are stored and fetched.
id: DC-73
lang: en
---

# Customizing storage

Document Capture provides support for three different storage models: **File System**, **Database**, and **Azure Blob Storage**. But it's also possible for you to customize your storage by extending or overruling the way documents are stored and fetched in Document Capture. You can overrule or extend the existing behavior using four different publisher events that are provided in the codeunit **CDC Doc. File Events**:

* **OnSetFile** - invoked when a file is requested to be stored.
* **OnGetFile** - invoked when a file is requested.
* **OnHasFile** - invoked when the existence of a file is checked.
* **OnClearFile** - invoked when a file deletion is requested, for example when a document related to the relevant file is deleted or imported.

All of the above methods implement a *handled* pattern, which enables programmers to overrule or extend the behavior. If *Handled* is set to *true*, Document Capture won't do anything, as it expects the file operation to be handled by the extension code. If *Handled* isn't set, the code will carry out the file operation as implemented according to the storage model selected in the Document Capture setup. In this way, it's possible to extend and store a subset of files externally and still let Document Capture handle the file storage. 

All of the methods have the following arguments:

* *Filename*: The name of the file that's being stored or fetched. The file name is decided by Document Capture and is a unique file identifier within the current company.
* *Company*: The name of the company in which the file operation takes place. Together, *Filename* and *Company* uniquely identify a file within a given database.
* *DocumentNo*: The **No.** field of the **CDC Document** record for which the file operation is performed.
* *FileType*: Identifies the type of file being stored or fetched. This can be used if only certain file types should be handled by the user code. The possible types are listed in the codeunit **CDC Document File Interface** and are identified using the following procedures: *TiffFileType*, *PdfFileType*, *MiscFileType*, *PageFileType*, *EmailFileType*, *HtmlFileType*, *XmlOriginalFileType*, and *XmlTrimmedFileType*.
* *Result*: A Boolean value indicating if the operation was successful. This value is only propagated if the *Handled* value is also set to *true*.

**OnSetFile** and **OnGetFile** have one additional parameter, *TempFile*, which is a **CDC Temp File** record. The **CDC Temp File** record is to be considered a file object, as it contains file information and the content of the file. The **Data** field on the record contains the data of the file that's either stored or fetched. So when you subscribe to **OnSetFile**, the **Data** field will contain the content of the file that's to be stored, whereas for **OnGetFile**, the content of the file that's requested should appear in the **Data** field.

> [!NOTE]
> Because the procedures above are invoked by various routines in Document Capture, such as document import, there must be no errors in the executing code, as this would break or stop the existing functionality.

> [!IMPORTANT]
> Extending the storage of documents comes with a risk. Continia Software can't be held accountable for documents lost or missing when this part of Document Capture is extended.