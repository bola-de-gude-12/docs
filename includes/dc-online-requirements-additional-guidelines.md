The following requirements and recommendations apply to both the online and on-premises versions of Microsoft Dynamics 365 Business Central.

## Browsers
It's recommended that you use one of the following web browsers with the latest updates applied:

* Google Chrome 
* Mozilla Firefox 
* Apple Safari 
* Microsoft Edge (version 4.50 or later)

Using Internet Explorer can cause errors and rendering issues. If Internet Explorer is the only option, it must be updated to the latest version.

## Screen resolution
The screen resolution must be at least 1,440×900 pixels, as lower resolutions make it difficult to use the Document Capture document viewer properly. The recommended screen resolution is 1,680×1,050 pixels or higher.

Note that zooming in your browser or changing your display’s scale and layout settings may disturb the viewing experience, as this isn’t fully supported.

## Mobile devices
Most Document Capture features work on mobile devices, although this functionality isn’t officially supported. This goes for the use of Document Capture in various mobile versions of Dynamics 365, including the mobile web client and the official Business Central app.

> [!NOTE]
> Not all Document Capture features are visible or accessible on mobile devices. Even for features that work on mobile devices, the mobile user interface (UI) may look noticeably different from the corresponding computer UI, and certain features may also be accessed differently on mobile devices. For example, the original PDF or XML file is not displayed on mobile devices – but you can download it using the **Document** menu on the action bar instead.

As for document approval in particular, the Continia Web Approval Portal is almost fully supported on mobile devices. One notable exception is that styled XML files aren't displayed in the portal in mobile mode. To view an XML file on a mobile device, it's recommended that you switch to desktop mode in your mobile browser. Note that the Web Approval Portal is a dedicated Continia client, so its use lies outside of Business Central. For more information, see [Minimum requirements for using Document Capture](@DC-453#continia-web-approval-portal) (online) and [Requirements for using the Continia Web Approval Portal on premises](@DC-454) (on-premises).

## RemoteApps
Most Document Capture features work with Windows Server RemoteApps, although this isn’t officially supported.

> [!NOTE]
> Not all Document Capture features are functional when you run Document Capture using RemoteApps. For example, the Document Capture drag-and-drop feature doesn't work as intended, as RemoteApps won't allow you to drag and drop files into the drop zone. As an alternative, you can use the browse function to link your files, which should work as expected.

## Technical email requirements
To import a document into Document Capture, you must attach it to an email as a PDF or XML file and then send the email to a predefined Continia email address. Such document-import emails must meet a number of technical requirements, which are listed below:

* Only unread emails are processed.
* Encrypted emails aren't supported, and neither is the internal Microsoft Exchange email format TNEF.
* Only PDF and XML files are supported. No other files are processed, including encrypted, password-protected, and compressed files (such as ZIP files).
* The PDF or XML files must be directly attached to the email. Only files that are directly attached to the email are processed. 
* Archived or encrypted files containing the PDF or XML files won’t be processed.
* PDF or XML files that are available as a link in the email body are ignored.
* PDF or XML files that are embedded in the email body are ignored. 
* The filename must not exceed 199 characters.
* For Continia Online OCR, the maximum email size is 20 MB.
* The maximum number of pages that can be processed for PDF files is 500.

If you'd like to receive an email with an error description whenever a requirement isn’t met, please reach out to the Continia support team. Note that if a PDF or XML file does in fact meet the requirements but somehow can’t be OCR-processed anyway, it's included in the **Documents with Error** column, which you can find under **Continia Document Capture Activities** > **Ready to import**. This rarely happens though.

> [!WARNING]
> Only unread document-import emails are downloaded and subsequently marked as read. If you or anyone else reads any such emails, those emails are only downloaded if they're manually marked as unread once they've been read by the user.

>[!IMPORTANT]
>File formats such as EXE, XLS, and JPG are ignored – but a malicious file saved as a PDF would still be handled by Document Capture. Therefore, you must make sure that your antivirus, such as Microsoft Defender Antivirus, is up to date when downloading files to your servers. If you're making use of a Business Central cloud environment, contact Microsoft to learn how your environment is protected.

## Business Central add-in for Outlook

Most Document Capture features work in the Business Central add-in for Outlook, although this isn’t officially supported.

Specifically, file download doesn't work for versions older than Business Central 2022 release wave 1 (BC v20). This is supported for BC v20 and later, though.

## Related information
[Minimum requirements for using Continia Document Capture](@DC-453)  
[Minimum requirements for using Continia Document Capture on premises](/Continia Document Capture/Development and Administration/On-Premises/Deployment/Minimum Requirements.md)  
[Requirements for using Continia Web Approval Portal on premises](@DC-454)  
[Business Central website](https://dynamics.microsoft.com/business-central/overview/)  