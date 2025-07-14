---
title: Event publishers for Document Capture 2023 R2 (12.00)
date: 14-04-2025
description: The full list of event publishers for Document Capture 2023 R2 (12.00).
id: DC-152
lang: en
---

# Event publishers for Document Capture 2023 R2 (12.00)

The following event publishers are included in Continia Document Capture 2023 R2 (12.00):

### Table 6085575 CDC Document Category


|   |   |
| --- | --- |
| Event name | **OnGetJournalTemplateTableIDOnAfterSetAllObjWithCaption** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` TempAllObjWithCaption: `Record AllObjWithCaption temporary` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterLookupJournalTemplateName** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | DocumentCategory: `Record` "CDC Document Category" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterLookupJournalBatchName** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | DocumentCategory: `Record` "CDC Document Category" |
| From version | 12.0.0.0 |

### Table 6085579 CDC Template


|   |   |
| --- | --- |
| Event name | **OnCloneCDCTemplate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` FromTemplate: `Record` "CDC Template"<br> `var` ToTemplate: `Record` "CDC Template" |
| From version | 12.0.0.0 |

### Table 6085580 CDC Template Field


|   |   |
| --- | --- |
| Event name | **OnBeforeClone** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | FromCompany: `Text[30]`<br> FromField: `Record` "CDC Template Field"<br> ToTemplate: `Record` "CDC Template"<br> CreatedFromMasterTemplate: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |

### Table 6085590 CDC Document


|   |   |
| --- | --- |
| Event name | **OnBeforeRegisterHideErrors** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` DocIsRegistered: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterTestStatus** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeFindTemplateInCompanies** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` FromCompany: `Text[30]`<br> `var` FromTemplate: `Record` "CDC Template"<br> SourceName: `Text[250]`<br> `var` Result: `Boolean`<br> `var` IsHandle: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnOpenPdfFile** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` TempFile: `Record` "CDC Temp File" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeRegisterYN** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeHasWarningComments** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` HandledHasWarningComments: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterBuildTempLinesTable2** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` TempDocumentLine: `Record` "CDC Temp. Document Line" |
| From version | 12.0.0.0 |

### Table 6085596 CDC Temp. Document Line


|   |   |
| --- | --- |
| Event name | **OnBeforeInsertMatchSpecification** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` DocumentLine: `Record` "CDC Temp. Document Line"<br> PurchDocMatch: `Record` "CDC Purch. Doc. Match"<br> `var` MatchSpec: `Record` "CDC Purch. Doc. Match Spec." |
| From version | 12.0.0.0 |

### Table 6085614 CDC Temp File


|   |   |
| --- | --- |
| Event name | **OnSaveFileWithDialog** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` TempFile: `Record` "CDC Temp File" temporary<br> WindowTitle: `Text[50]`<br> FilterString: `Text`<br> `var` Ok: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnCreateFromClientFilePath** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` TempFile: `Record` "CDC Temp File" temporary<br> ClientFilePath: `Text` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnCheckFilePathLength** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` TempFile: `Record` "CDC Temp File" temporary<br> ClientFilePath: `Text` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnSaveToClient** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` TempFile: `Record` "CDC Temp File" temporary<br> `var` ClientFilePath: `Text` |
| From version | 12.0.0.0 |

### Table 6085767 CDC Purchase Header Info.


|   |   |
| --- | --- |
| Event name | **OnBeforeUpdateApprvlFlowCode** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | PurchHeader: `Record` "Purchase Header"<br> NewCode: `Code[10]`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeIsApprovalFlowVisible** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeIsApprovalFlowVisiblePurchOrder** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Handled: `Boolean` |
| From version | 12.1.0.0 |

### Table 6225182 CDC Purch. Contract Header


|   |   |
| --- | --- |
| Event name | **OnAfterValidateShortcutDimCode** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchContractHeader: `Record` "CDC Purch. Contract Header"<br> xPurchContractHeader: `Record` "CDC Purch. Contract Header"<br> FieldNumber: `Integer`<br> `var` ShortcutDimCode: `Code[20]` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeUpdateAllLineDim** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchContractHeader: `Record` "CDC Purch. Contract Header"<br> NewParentDimSetID: `Integer`<br> OldParentDimSetID: `Integer`<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnUpdateAllLineDimOnBeforePurchContrLineModify** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchContractLine: `Record` "CDC Purch. Contract Line" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterConfirmPurchPrice** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchContractHeader: `Record` "CDC Purch. Contract Header"<br> `var` PurchContractLine: `Record` "CDC Purch. Contract Line"<br> `var` RecalculateLines: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnUpdatePurchContractLinesByChangedFieldName** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | PurchContractHeader: `Record` "CDC Purch. Contract Header"<br> `var` PurchContractLine: `Record` "CDC Purch. Contract Line"<br> ChangedFieldName: `Text[100]` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterChangePricesIncludingVAT** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchContractHeader: `Record` "CDC Purch. Contract Header" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterUpdateCurrencyFactor** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchContractHeader: `Record` "CDC Purch. Contract Header"<br> HideValidationDialog: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeUpdateCurrencyFactor** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchContractHeader: `Record` "CDC Purch. Contract Header"<br> `var` Updated: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateDimTableIDs** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchContractHeader: `Record` "CDC Purch. Contract Header"<br> CallingFieldNo: `Integer`<br> `var` TableID: `array[10] of Integer`<br> `var` No: `array[10] of Code[20]`<br> `var` DimPriorityCode: `Code[10]` |
| From version | 12.0.0.0 |

### Table 6225183 CDC Purch. Contract Line


|   |   |
| --- | --- |
| Event name | **OnAfterCreateDimTableIDs** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchContractLine: `Record` "CDC Purch. Contract Line"<br> CallingFieldNo: `Integer`<br> `var` TableID: `array[10] of Integer`<br> `var` No: `array[10] of Code[20]` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterGetPurchHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchContractLine: `Record` "CDC Purch. Contract Line"<br> `var` PurchContractHeader: `Record` "CDC Purch. Contract Header" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterUpdateAmounts** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchContractLine: `Record` "CDC Purch. Contract Line"<br> `var` xPurchContractLine: `Record` "CDC Purch. Contract Line"<br> CurrFieldNo: `Integer` |
| From version | 12.0.0.0 |

### Page 6085593 CDC Doc. Capture Client Addin


|   |   |
| --- | --- |
| Event name | **OnAfterLineUpdateFieldValue** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | "Page": `Record` "CDC Document Page"<br> `var` "Field": `Record` "CDC Template Field"<br> Top: `Integer`<br> Left: `Integer`<br> Bottom: `Integer`<br> Right: `Integer`<br> LineNo: `Integer`<br> Word: `Text[1024]` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCaptureEnded** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | PageNo: `Integer`<br> "Area": `Code[20]`<br> FieldName: `Text[1024]`<br> LineNo: `Integer`<br> IsValue: `Boolean`<br> Top: `Integer`<br> Left: `Integer`<br> Bottom: `Integer`<br> Right: `Integer`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeHandleXmlCommand** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> Command: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |

### Page 6085597 CDC Document Lines ListPart


|   |   |
| --- | --- |
| Event name | **OnBeforeUpdateFieldValue** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` TempDocumentLine: `Record` "CDC Temp. Document Line" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeAddLineFieldCaption** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | TemplateField: `Record` "CDC Template Field"<br> `var` AddField: `Boolean` |
| From version | 12.1.0.0 |

### Page 6085600 CDC Document List With Image


|   |   |
| --- | --- |
| Event name | **OnBeforeSetSourceNoNameVisibility** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | CurrentDocCategory: `Code[20]`<br> HasSourceTableNo: `Boolean`<br> `var` IsSourceNoNameVisible: `Boolean`<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetSourceVATRegistrationNoVisibility** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | CurrentDocCategory: `Code[20]`<br> HasSourceTableNo: `Boolean`<br> `var` IsSourceVATRegistrationNoVisible: `Boolean`<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnUpdateListOnBeforeCurrPageUpdate** |
| Event type | IntegrationEvent(IncludeSender : `true`, GlobalVarAccess : `false`) |
| Parameters | CurrentDocCategory: `Code[20]` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetEditableFromParent** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Rec: `Record` "CDC Document"<br> `var` AllowEdit: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterGetSource** |
| Event type | IntegrationEvent(IncludeSender : `true`, GlobalVarAccess : `false`) |
| Parameters | `var` Rec: `Record` "CDC Document"<br> `var` SourceID: `Text[250]`<br> `var` SourceName: `Text[1024]` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnPageFindRecord** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Rec: `Record` "CDC Document"<br> CurrentDocCategory: `Code[20]`<br> Which: `Text`<br> `var` Found: `Boolean`<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnPageNextRecord** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Rec: `Record` "CDC Document"<br> CurrentDocCategory: `Code[20]`<br> Steps: `Integer`<br> `var` NextStep: `Integer`<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |

### Page 6085612 CDC Continia Config. Subpage


|   |   |
| --- | --- |
| Event name | **OnModifyTempTableOnBeforeGetEntryNo** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Rec: `Record` "CDC Temp. Configuration Line"<br> `var` TempConfigLine: `Record` "CDC Temp. Configuration Line"<br> EntryNo: `Integer`<br> IsIncluded: `Boolean` |
| From version | 12.0.0.0 |

### Page 6085702 CDC Purch. Invoice Match


|   |   |
| --- | --- |
| Event name | **OnAfterSetFilterPurchRcptLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchRcptLine: `Record` "Purch. Rcpt. Line"<br> `var` Document: `record` "CDC Document" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSetFilterPurchLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchaseLine: `Record` "Purchase Line"<br> `var` Document: `record` "CDC Document" |
| From version | 12.0.0.0 |

### Page 6085759 CDC Document Files Factbox


|   |   |
| --- | --- |
| Event name | **FileCopyCompleted** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` TempFile: `Record` "CDC Temp File"<br> `var` Document: `Record` "CDC Document" |
| From version | 12.0.0.0 |

### Page 6085813 CDC Document File Viewer


|   |   |
| --- | --- |
| Event name | **OnBeforeHandleXmlCommand** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> Command: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |

### Page 6085999 CDC Change Document Amount 2


|   |   |
| --- | --- |
| Event name | **OnAfterSetSourceRecord** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` RecordVariant: `Variant`<br> `var` DocumentType: `Text`<br> `var` DocumentNo: `Text`<br> `var` PayToName: `Text`<br> `var` CurrencyCode: `Code[10]` |
| From version | 12.0.0.0 |

### Page 6086002 CDC Purch. Doc. (WS)


|   |   |
| --- | --- |
| Event name | **OnGetDocHeaderAmounts** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchHeader: `Record` "Purchase Header"<br> `var` ImportedAmountExclVAT: `Decimal`<br> `var` ImportedAmountInclVAT: `Decimal`<br> `var` IsHandled: `Boolean`<br> `var` AssignedAmountExclVAT: `Decimal`<br> `var` AssignedAmountInclVAT: `Decimal` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetDocFilename** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchHeader: `Record` "Purchase Header"<br> `var` ReturnValue: `Text[1024]`<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterGetDocFilename** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchHeader: `Record` "Purchase Header"<br> `var` ReturnValue: `Text[1024]`<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |

### Page 6086019 CDC Purch. Posted Inv. (WS)


|   |   |
| --- | --- |
| Event name | **OnBeforeGetDocFilename** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchInvHeader: `Record` "Purch. Inv. Header"<br> `var` ReturnValue: `Text[1024]`<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterGetDocFilename** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchInvHeader: `Record` "Purch. Inv. Header"<br> `var` ReturnValue: `Text[1024]`<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |

### Page 6086021 CDC Purch. Posted Cr.Memo (WS)


|   |   |
| --- | --- |
| Event name | **OnBeforeGetDocFilename** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchCrMemoHdr: `Record` "Purch. Cr. Memo Hdr."<br> `var` ReturnValue: `Text[1024]`<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterGetDocFilename** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchCrMemoHdr: `Record` "Purch. Cr. Memo Hdr."<br> `var` ReturnValue: `Text[1024]`<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |

### Page 6086038 CDC Document Files (WS)


|   |   |
| --- | --- |
| Event name | **OnBeforeOnFindRecord** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Which: `Text[1024]`<br> `var` Rec: `Record` "CDC Document"<br> `var` RecordFound: `Boolean`<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeOnNextRecord** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Steps: `Integer`<br> `var` Rec: `Record` "CDC Document"<br> `var` CurrentSteps: `Integer`<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |

### Page 6225250 CDC Contr. Line Exp. FactBox


|   |   |
| --- | --- |
| Event name | **OnPageAfterGetRecord** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchContractLine: `Record` "CDC Purch. Contract Line"<br> `var` NoOfOpenExpenses: `Integer`<br> `var` NoOfPostedExpenses: `Integer` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnOpenExpensesDrillDown** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchContractLine: `Record` "CDC Purch. Contract Line" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnPostedExpensesDrillDown** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchContractLine: `Record` "CDC Purch. Contract Line" |
| From version | 12.0.0.0 |

### Codeunit 6085575 CDC Capture Engine


|   |   |
| --- | --- |
| Event name | **OnBeforeRunLineCaptureCodeunit** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCaptureField2** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> PageNo: `Integer`<br> `var` "Field": `Record` "CDC Template Field"<br> UpdateFieldCaption: `Boolean`<br> `var` FieldCaption: `Record` "CDC Template Field Caption"<br> `var` Handled: `Boolean`<br> `var` Word: `Text[1024]` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCaptureField2** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> PageNo: `Integer`<br> `var` "Field": `Record` "CDC Template Field"<br> UpdateFieldCaption: `Boolean`<br> `var` FieldCaption: `Record` "CDC Template Field Caption"<br> `var` Handled: `Boolean`<br> `var` Word: `Text[1024]` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeBufferWords** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | DocumentNo: `Code[20]`<br> PageNo: `Integer`<br> `var` Words: `Record` "CDC Document Word"<br> `var` GlobalWords: `Record` "CDC Document Word"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeFindDocumentSource** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterFindDocumentSource** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeAfterCapture** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateDocument** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeAutoDelegateDocument** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeModifyDocumentWhenCaptureDocument** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> Template: `Record` "CDC Template" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnGetFieldCaptionOnBeforeSetPosition** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | FieldCaption: `Record` "CDC Template Field Caption"<br> DocumentNo: `Code[20]`<br> `var` Margin: `Decimal` |
| From version | 12.0.0.0 |

### Codeunit 6085576 CDC Capture Management


|   |   |
| --- | --- |
| Event name | **OnBeforeUpdateFieldValueCapture** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | DocumentNo: `Code[20]`<br> PageNo: `Integer`<br> LineNo: `Integer`<br> `var` "Field": `Record` "CDC Template Field"<br> `var` Word: `Text[1024]`<br> Manual: `Boolean`<br> UpdatedByUser: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterUpdateFieldValue** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | DocumentNo: `Code[20]`<br> PageNo: `Integer`<br> LineNo: `Integer`<br> `var` "Field": `Record` "CDC Template Field"<br> Word: `Text[1024]`<br> Manual: `Boolean`<br> UpdatedByUser: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeApplyTranslationToWord** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` "Field": `Record` "CDC Template Field"<br> Word: `Text[1024]`<br> `var` Handled: `Boolean`<br> `var` ResultWord: `Text[1024]` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterApplyTranslationToWord** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` "Field": `Record` "CDC Template Field"<br> `var` Word: `Text[1024]` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnCaseElseTransferDestFields** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Value: `Record` "CDC Document Value"<br> FieldRef: `FieldRef`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateXmlAttachment** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` AttachmentXmlNode: `Codeunit` "CSC XML Node"<br> `var` AttachmentFilename: `Text[1024]` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeUpdateFieldCaption** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` "Field": `Record` "CDC Template Field"<br> PageNo: `Integer`<br> Top: `Integer`<br> Left: `Integer`<br> DPI: `Integer`<br> Word: `Text[1024]`<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateXmlUriAttachment** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` AttachmentXmlNode: `Codeunit` "CSC XML Node"<br> `var` AttachmentFilename: `Text[1024]` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSetDocumentWordFilters** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` Template: `Record` "CDC Template"<br> PageNo: `Integer`<br> `var` DocumentWord: `Record` "CDC Document Word" |
| From version | 12.0.0.0 |

### Codeunit 6085577 CDC Document Importer


|   |   |
| --- | --- |
| Event name | **OnAfterImportDocument2** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> DocCatCode: `Code[20]`<br> Path: `Text[1024]`<br> Filename: `Text[199]` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnCheckDocAutoReg** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` Handle: `Boolean` |
| From version | 12.0.0.0 |

### Codeunit 6085579 CDC Doc. - Search Word Ident.


|   |   |
| --- | --- |
| Event name | **OnBeforeOnRun** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeExcludeSource** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | CategoryCode: `Code[10]`<br> SourceRecordIdTreeId: `Integer`<br> `var` ExcludeSource: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |

### Codeunit 6085583 CDC Navigate Document Capture


|   |   |
| --- | --- |
| Event name | **OnAfterFilterDocuments** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Doc2: `Record` "CDC Document" temporary<br> DocNoFilter: `Code[250]`<br> PostingDateFilter: `Text[250]` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeFilterDoc** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Doc2: `Record` "CDC Document"<br> TableNo: `Integer`<br> DocIDFilter: `Code[250]`<br> `var` IsHandled: `Boolean` |
| From version | 12.4.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeFilterDocAndTable** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Doc2: `Record` "CDC Document"<br> TableNo: `Integer`<br> Fld1: `Integer`<br> Fld2: `Integer`<br> Val1: `Text[250]`<br> Val2: `Text[250]`<br> DocType: `Integer`<br> SubType: `Integer`<br> DocIDFieldNo: `Integer`<br> `var` IsHandled: `Boolean` |
| From version | 12.4.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeAddAllDocuments** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Doc2: `Record` "CDC Document"<br> RecIDTreeID: `Integer`<br> DocType: `Integer`<br> DocSubType: `Integer`<br> DocIDFilter: `Text[250]`<br> ExtDocNo: `Code[35]`<br> `var` DocumentExcluded: `Boolean` |
| From version | 12.4.0.0 |

### Codeunit 6085598 CDC SmtpMail Management


|   |   |
| --- | --- |
| Event name | **OnBeforeIsValidEmail** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | EmailAddress: `Text[1024]`<br> `var` IsValidEmailAddress: `Boolean`<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |

### Codeunit 6085602 CDC Document Attachment Mgt.


|   |   |
| --- | --- |
| Event name | **OnBeforeCreateTempDocumentList** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` TempDoc: `Record` "CDC Temp. Document"<br> RecID: `RecordID`<br> CreatedDocTableNo: `Integer`<br> CreatedDocSubtype: `Integer`<br> CreatedDocNo: `Code[20]`<br> CreatedDocRefNo: `Integer`<br> ShowAllDocs: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateTempDocumentList** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` TempDoc: `Record` "CDC Temp. Document"<br> RecID: `RecordID`<br> CreatedDocTableNo: `Integer`<br> CreatedDocSubtype: `Integer`<br> CreatedDocNo: `Code[20]`<br> CreatedDocRefNo: `Integer`<br> ShowAllDocs: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateTempDocListFromNavigate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` TempDoc: `Record` "CDC Temp. Document"<br> PostingDate: `Date`<br> DocNo: `Code[250]`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateTempDocListFromNavigate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` TempDoc: `Record` "CDC Temp. Document"<br> PostingDate: `Date`<br> DocNo: `Code[250]` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeEditDocumentFile** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | TempDoc: `Record` "CDC Temp. Document"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterEditDocumentFile** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | TempDoc: `Record` "CDC Temp. Document" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeDeleteDocumentFile** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | TempDoc: `Record` "CDC Temp. Document"<br> `var` ReturnValue: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterDeleteDocumentFile** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | TempDoc: `Record` "CDC Temp. Document" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeModifyDocumentFile** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | TempDoc: `Record` "CDC Temp. Document"<br> `var` ReturnValue: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterModifyDocumentFile** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | TempDoc: `Record` "CDC Temp. Document" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeShowDocumentCard** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | TempDoc: `Record` "CDC Temp. Document"<br> `var` ReturnValue: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterShowDocumentCard** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | TempDoc: `Record` "CDC Temp. Document" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateDocument** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> RecID: `RecordID`<br> CreatedDocTableNo: `Integer`<br> CreatedDocSubtype: `Integer`<br> CreatedDocNo: `Code[20]`<br> CreatedDocRefNo: `Integer`<br> DocCat: `Code[20]`<br> NewDescription: `Text[1024]`<br> NewExtension: `Text[20]`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateDocument** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> RecID: `RecordID`<br> CreatedDocTableNo: `Integer`<br> CreatedDocSubtype: `Integer`<br> CreatedDocNo: `Code[20]`<br> CreatedDocRefNo: `Integer`<br> DocCat: `Code[20]`<br> NewDescription: `Text[1024]`<br> NewExtension: `Text[20]` |
| From version | 12.0.0.0 |

### Codeunit 6085610 CDC Document Search Mgnt.


|   |   |
| --- | --- |
| Event name | **OnBeforeSearchResultInsert** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` SearchResult: `Record` "CDC Document Search Result" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSetDocumentWordFilter** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` DocumentWord: `Record` "CDC Document Word" |
| From version | 12.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSetDocumentValueFilter** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` DocumentValue: `Record` "CDC Document Value" |
| From version | 12.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSetXMLDocumentSearchFilter** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document2: `Record` "CDC Document" |
| From version | 12.1.0.0 |

### Codeunit 6085619 CDC Export Continia Users


|   |   |
| --- | --- |
| Event name | **OnBeforeAppendUser** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` SmtpMailMgt: `Codeunit` "CDC SmtpMail Management"<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |

### Codeunit 6085640 CDC Doc. File Events


|   |   |
| --- | --- |
| Event name | **OnHasFile** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | FileName: `Text[1024]`<br> Company: `Text[50]`<br> DocumentNo: `Code[20]`<br> FileType: `Integer`<br> `var` Result: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnClearFile** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | FileName: `Text[1024]`<br> Company: `Text[50]`<br> DocumentNo: `Code[20]`<br> FileType: `Integer`<br> `var` Result: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnGetFile** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | FileName: `Text[1024]`<br> Company: `Text[50]`<br> DocumentNo: `Code[20]`<br> FileType: `Integer`<br> `var` TempFile: `Record` "CDC Temp File" temporary<br> `var` Result: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnSetFile** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | FileName: `Text[1024]`<br> Company: `Text[50]`<br> DocumentNo: `Code[20]`<br> FileType: `Integer`<br> `var` TempFile: `Record` "CDC Temp File" temporary<br> `var` Result: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |

### Codeunit 6085699 CDC URL Management


|   |   |
| --- | --- |
| Event name | **OnBeforeGetApprovalHyperlink** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ApprovalHyperlink: `Text[1024]`<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |

### Codeunit 6085702 CDC Purch. Doc. - Identificat.


|   |   |
| --- | --- |
| Event name | **OnAfterFindVendorBeforeModify** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` "Field": `Record` "CDC Template Field"<br> `var` FieldCaption: `Record` "CDC Template Field Caption"<br> `var` VatRegNo: `Code[20]`<br> `var` FoundVendor: `Record Vendor`<br> `var` Found: `Boolean` |
| From version | 12.0.0.0 |

### Codeunit 6085703 CDC Purch. - Full Capture


|   |   |
| --- | --- |
| Event name | **OnAfterFullCapture** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCalculateDueDate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeAdjustMissingQty** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeAdjustMissingFields** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |

### Codeunit 6085704 CDC Purch. - Line Validation


|   |   |
| --- | --- |
| Event name | **OnBeforeLineValidation** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` TempDocumentLine: `Record` "CDC Temp. Document Line"<br> Document: `Record` "CDC Document"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |

### Codeunit 6085705 CDC Purch. - Validation


|   |   |
| --- | --- |
| Event name | **OnBeforeBuildTempLinesTable** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` DocumentLines: `Record` "CDC Temp. Document Line" temporary<br> `var` IsValid: `Boolean`<br> `var` LinesHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeMatchValidation** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` DocumentLine: `Record` "CDC Temp. Document Line" temporary<br> `var` IsValid: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetDocumentDate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` DueDate: `Date`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeTotalAmountNegCheck** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` IsValid: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckExternalDocNo** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> ExtDocNo: `Code[250]`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateAmtAccounts** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` Template: `Record` "CDC Template"<br> `var` IsInvalid: `Boolean`<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterValidateDocument** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` IsInvalid: `Boolean` |
| From version | 12.0.0.0 |

### Codeunit 6085706 CDC Purch. - Register


|   |   |
| --- | --- |
| Event name | **OnBeforeGetOrderNoUpdateOrderWithMatch** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | PurchDocMatch: `Record` "CDC Purch. Doc. Match"<br> Template: `Record` "CDC Template"<br> `var` OrderNo: `Code[100]`<br> IsInvoice: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |
| Obsolete | Replaced by OnBeforeGetOrderNoUpdateOrderWithMatch2 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetOrderNoUpdateOrderWithMatch2** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | PurchDocMatch: `Record` "CDC Purch. Doc. Match"<br> Template: `Record` "CDC Template"<br> `var` OrderNo: `Code[100]`<br> DocumentType: `Integer`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreatePurchHeaderCopyHeaderDim** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | PurchDocMatch: `Record` "CDC Purch. Doc. Match"<br> `var` PurchHeader: `Record` "Purchase Header"<br> PurchaserCode: `Code[20]`<br> IsInvoice: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |
| Obsolete | Replaced by OnBeforeCreatePurchHeaderCopyHeaderDim2 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreatePurchHeaderCopyHeaderDim2** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | PurchDocMatch: `Record` "CDC Purch. Doc. Match"<br> `var` PurchHeader: `Record` "Purchase Header"<br> PurchaserCode: `Code[20]`<br> DocumentType: `Integer`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateWithoutMatchModifyPurchLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` PurchLine: `Record` "Purchase Line"<br> DocumentLineNo: `Integer` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateWithoutMatchLineTrans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchLine: `Record` "Purchase Line"<br> LineTrans: `Record` "CDC Data Translation" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateWithMatchCreatePurchLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` PurchDocMatch: `Record` "CDC Purch. Doc. Match"<br> PurchHeader: `Record` "Purchase Header"<br> `var` PurchLine: `Record` "Purchase Line"<br> `var` NextLineNo: `Integer`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterModifyPurchLineCreatePurchLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` PurchLine: `Record` "Purchase Line" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterModifyPurchLineCreatePurchLineAmountDistribution** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` PurchLine: `Record` "Purchase Line"<br> IsHeadingLine: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreatePurchLineLineTrans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchLine: `Record` "Purchase Line"<br> DataTransl: `Record` "CDC Data Translation" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterTransferPurchHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchHeader: `Record` "Purchase Header"<br> `var` Document: `Record` "CDC Document" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePurchHeaderInsert** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` PurchHeader: `Record` "Purchase Header" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterRegister** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterPerformStep1** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` PurchaseHeader: `Record` "Purchase Header" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePerformStep2** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` Template: `Record` "CDC Template"<br> `var` PurchHeader: `Record` "Purchase Header"<br> IsInvoice: `Boolean`<br> `var` SkipNextStep: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |
| Obsolete | Replaced by OnBeforePerformStep2DocType |



|   |   |
| --- | --- |
| Event name | **OnBeforePerformStep2DocType** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` Template: `Record` "CDC Template"<br> `var` PurchHeader: `Record` "Purchase Header"<br> DocumentType: `Integer`<br> `var` SkipNextStep: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeShowAfterRegister** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterTransferPurchLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchLine: `Record` "Purchase Line"<br> Document: `Record` "CDC Document"<br> DocumentLineNo: `Integer` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateWithoutMatchSetAccountRequired** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` DocumentLine: `Record` "CDC Temp. Document Line" temporary<br> `var` AccountRequired: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateWithMatchGetPurchLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | PurchDocMatch: `Record` "CDC Purch. Doc. Match"<br> `var` PurchaseLine: `Record` "Purchase Line"<br> `var` NextLineNo: `Integer`<br> `var` PurchLineGetHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreatePurchHeaderWithoutMatch** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` PurchHeader: `Record` "Purchase Header"<br> IsInvoice: `Boolean` |
| From version | 12.0.0.0 |
| Obsolete | Replaced by OnAfterCreatePurchHeaderWithoutMatch2 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreatePurchHeaderWithoutMatch2** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` PurchHeader: `Record` "Purchase Header"<br> DocumentType: `Integer` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreatePurchHeaderWithMatch** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` PurchHeader: `Record` "Purchase Header"<br> IsInvoice: `Boolean` |
| From version | 12.0.0.0 |
| Obsolete | Replaced by OnAfterCreatePurchHeaderWithMatch2 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreatePurchHeaderWithMatch2** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` PurchHeader: `Record` "Purchase Header"<br> DocumentType: `Integer` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateJournalInsert** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` GenJournalLine: `Record` "Gen. Journal Line"<br> DocumentLineNo: `Integer` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateJournalModify** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` GenJournalLine: `Record` "Gen. Journal Line"<br> DocumentLineNo: `Integer` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateVendorGenJnlLineInsert** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` GenJournalLine: `Record` "Gen. Journal Line" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreatingVendorGenJnlLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` GenJournalLine: `Record` "Gen. Journal Line" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeTransferLineDim** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> LineNo: `Integer`<br> `var` PurchLine: `Record` "Purchase Line"<br> `var` LineTrans: `Record` "CDC Data Translation"<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeModifyPurchLineCreateMatchVarianceLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | PurchaseHeader: `Record` "Purchase Header"<br> `var` PurchaseLine: `Record` "Purchase Line" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateWithoutMatchCreateLinesByHeaderAmounts** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` PurchaseHeader: `Record` "Purchase Header"<br> PurchaserCode: `Code[20]`<br> IsInvoice: `Boolean`<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |
| Obsolete | Replaced by OnBeforeCreateWithoutMatchCreateLinesByHeaderAmounts2 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateWithoutMatchCreateLinesByHeaderAmounts2** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` PurchaseHeader: `Record` "Purchase Header"<br> PurchaserCode: `Code[20]`<br> DocumentType: `Integer`<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeRegisterDocument** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeaderAmounts** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` PurchHeader: `Record` "Purchase Header"<br> `var` "Field": `Record` "CDC Template Field"<br> `var` Template: `Record` "CDC Template"<br> LinesRecognised: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeaderAmountsWithTextLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` PurchHeader: `Record` "Purchase Header"<br> `var` "Field": `Record` "CDC Template Field"<br> `var` Template: `Record` "CDC Template"<br> LinesRecognised: `Boolean`<br> TextLineArray: `array[50] of Text[1024]`<br> NoOfTextLines: `Integer`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePerformStep1** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> ActionToPerform: `Option CreateWithoutMatch,CreateWithMatch,UpdateOrderWithMatch,CreateJournal` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeProcessDocumentLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` TempDocumentLine: `Record` "CDC Temp. Document Line" temporary<br> PurchaseHeader: `Record` "Purchase Header" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckWMS** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | PurchLine: `Record` "Purchase Line"<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePostPrepayment** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` PurchHeader: `Record` "Purchase Header"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeModifyPurchHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchaseHeader: `Record` "Purchase Header"<br> `var` Document: `Record` "CDC Document" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckDuplicateNumber** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | PurchaseHeader: `Record` "Purchase Header"<br> CDCDocument: `Record` "CDC Document"<br> OrderNo: `Code[100]` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterValidateDocument** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeTransferPurchHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchHeader: `Record` "Purchase Header"<br> `var` Document: `Record` "CDC Document" |
| From version | 12.0.0.0 |

### Codeunit 6085709 CDC Purch. Doc. - Management


|   |   |
| --- | --- |
| Event name | **OnBeforeAutoMatchSetDocumentMatchStatusWithOrderNoFilter** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> OrderNoFilter: `Code[1024]`<br> `var` Matched: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeAutoMatchNoLinesTryMatchAmounts** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> Template: `Record` "CDC Template"<br> PurchDocType: `Option Receipt` "Return Shipment","Order","Return Order"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeIsDocMatched** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` IsDocMatched: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetDocMatchedAmount** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` MatchedAmount: `Decimal`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetLineAmount** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> LineNo: `Integer`<br> `var` ReturnValue: `Decimal`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetLineTranslAccountNo** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Template: `Record` "CDC Template"<br> `var` Document: `Record` "CDC Document"<br> LineNo: `Integer`<br> `var` DataTrans: `Record` "CDC Data Translation"<br> TranslateFrom: `Code[150]`<br> `var` Handled: `Boolean`<br> `var` FoundTranslation: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckMatchToWithTrack** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | PurchOrderLine: `Record` "Purchase Line"<br> MatchedToDocType: `Option Receipt` "Return Shipment","Order","Return Order"<br> ShowError: `Boolean`<br> `var` Handled: `Boolean`<br> `var` ReturnValue: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterGetIsInvoice** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` "Field": `Record` "CDC Template Field"<br> `var` IsInvoice: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnGetDocumentTypeOnBeforeGetDocType** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` "Field": `Record` "CDC Template Field"<br> `var` FieldRule: `Record` "CDC Template Field Rule"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSplitPurchOrderLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchaseLine: `Record` "Purchase Line"<br> `var` AmountOnNewLine: `Decimal`<br> `var` DescriptionOnNewLine: `Text[50]`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeInsertPurchDocMatch** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchDocMatch: `Record` "CDC Purch. Doc. Match"<br> DocNo: `Code[20]`<br> DocLineNo: `Integer`<br> PurchDocType: `Option Receipt` "Return Shipment","Order","Return Order"<br> PurchDocNo: `Code[20]`<br> PurchLineNo: `Integer`<br> `var` AvailMatchQty: `Decimal`<br> `var` DirectUnitCost: `Decimal`<br> `var` LineDiscountPct: `Decimal`<br> UpdateMatchTracking: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetDocLineMatchedQty** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` DocumentLine: `Record` "CDC Temp. Document Line"<br> `var` MatchQty: `Decimal`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSetFiltersAutoMatchOpenPurchDocument** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> DocumentLine: `Record` "CDC Temp. Document Line" temporary<br> Template: `Record` "CDC Template"<br> OrderNoFilter: `Code[1024]`<br> PurchDocType: `Option Receipt` "Return Shipment","Order","Return Order"<br> `var` PurchLine: `Record` "Purchase Line"<br> `var` Stop: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCalcAvailMatchQtyAutoMatchOpenPurchDoc** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> DocumentLine: `Record` "CDC Temp. Document Line" temporary<br> Template: `Record` "CDC Template"<br> PurchLine: `Record` "Purchase Line"<br> `var` AvailableMatchQty: `Decimal` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSetFiltersAutoMatchReceipt** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> DocumentLine: `Record` "CDC Temp. Document Line" temporary<br> Template: `Record` "CDC Template"<br> OrderNoFilter: `Code[1024]`<br> `var` PurchRcptLine: `Record` "Purch. Rcpt. Line"<br> `var` Stop: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCalcAvailMatchQtyAutoMatchReceipt** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> DocumentLine: `Record` "CDC Temp. Document Line" temporary<br> Template: `Record` "CDC Template"<br> PurchRcptLine: `Record` "Purch. Rcpt. Line"<br> `var` AvailableMatchQty: `Decimal` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSetFilterAutoMatchReturnShipment** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> DocumentLine: `Record` "CDC Temp. Document Line" temporary<br> Template: `Record` "CDC Template"<br> OrderNoFilter: `Code[1024]`<br> `var` ReturnShptLine: `Record` "Return Shipment Line"<br> `var` Stop: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCalcAvailMatchQtyAutoMatchReturnShpt** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> DocumentLine: `Record` "CDC Temp. Document Line" temporary<br> Template: `Record` "CDC Template"<br> ReturnShptLine: `Record` "Return Shipment Line"<br> `var` AvailableMatchQty: `Decimal` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeInsertMatchSpecByPurchDocMatchShowMatchedSpec** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | PurchDocType: `Option Receipt` "Return Shipment","Order","Return Order"<br> PurchDocNo: `Code[20]`<br> PurchLineNo: `Integer`<br> PurchDocMatch: `Record` "CDC Purch. Doc. Match"<br> `var` MatchSpec: `Record` "CDC Purch. Doc. Match Spec." |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSetPurchHeaderFilters** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` PurchHeader: `Record` "Purchase Header"<br> PurchDocType: `Option Receipt` "Return Shipment","Order","Return Order" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSetPurchLineFilters** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` PurchLine: `Record` "Purchase Line"<br> PurchDocType: `Option Receipt` "Return Shipment","Order","Return Order" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSetPurchRcptLineFilters** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` PurchRcptLine: `Record` "Purch. Rcpt. Line" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSetReturnShptLineFilters** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` ReturnShptLine: `Record` "Return Shipment Line" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterAutoMatchGetOurDocumentNo** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` OurDocumentNo: `Code[250]` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterAutoMatchSetOrderNoFilter** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` OrderNoFilter: `Code[1024]` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckWhseRequirement** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> PurchLine: `Record` "Purchase Line"<br> `var` WhseRequirementDialogHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckAgainstImportedAmounts** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | PurchHeader: `Record` "Purchase Header"<br> Template: `Record` "CDC Template"<br> `var` ImportedAmountExclVAT: `Decimal`<br> `var` ImportedAmountInclVAT: `Decimal`<br> `var` AssignedAmountExclVAT: `Decimal`<br> `var` AssignedAmountInclVAT: `Decimal`<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeAutoMatchEnabled** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` Result: `Boolean`<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeUpdateMatchedQuantity** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> PurchLine: `Record` "Purchase Line"<br> Currency: `Record Currency`<br> MatchedToDocType: `Option Receipt` "Return Shipment","Order","Return Order"<br> MatchedToDocNo: `Code[20]`<br> MatchedToLineNo: `Integer`<br> MatchedToQuantity: `Decimal`<br> QtyAvailableOnMatchedToLine: `Decimal`<br> `var` MatchedQuantity: `Decimal`<br> AutoCalcQtyCostsDiscount: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetWhseRequirementDialogType** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | PurchLine: `Record` "Purchase Line"<br> `var` DialogType: `Option` "None",ShipError,ReciveError,Shipwarning,ReceiveWarning<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnCalculateMatchedQtyOnAfterSetFilter** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | DCDocumentNo: `Code[20]`<br> MatchedToDocType: `Option Receipt` "Return Shipment","Order","Return Order"<br> MatchedToDocNo: `Code[20]`<br> MatchedToLineNo: `Integer`<br> ForDCDocOnly: `Boolean`<br> `var` PurchDocMatch: `Record` "CDC Purch. Doc. Match" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeShowMessages** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> Template: `Record` "CDC Template"<br> `var` ShowTelerenceMsg: `Boolean`<br> `var` ShowRequireReceiveMsg: `Boolean`<br> `var` ShowPOFullyReceivedMsg: `Boolean`<br> `var` ShowNoReceiptExistMsg: `Boolean`<br> `var` ShowReturnShptExistMsg: `Boolean`<br> `var` ShowPOFullyReceivedAndInvoiMsg: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterAutoMatch** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeFindOpenPurchLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchDocMatchTmp: `Record` "CDC Purch. Doc. Match" temporary<br> `var` PurchLine: `Record` "Purchase Line"<br> DocumentNo: `Code[20]`<br> PurchDocType: `Option Receipt` "Return Shipment","Order","Return Order"<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCalculateMatchedQuantity** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> PurchLine: `Record` "Purchase Line"<br> `var` MatchedQuantity: `Decimal`<br> MatchedToQuantity: `Decimal`<br> QtyAvailableOnMatchedToLine: `Decimal`<br> TotalMatchedQty: `Decimal`<br> PrevMatchedQty: `Decimal` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckWhseReqAMOpenPurchDoc** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> PurchLine: `Record` "Purchase Line"<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeAutoMatch** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | CDCDocument: `Record` "CDC Document"<br> OurDocumentNo: `Code[250]`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckQtyToInvoice** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchaseHeader: `Record` "Purchase Header"<br> `var` PurchaseLine: `Record` "Purchase Line"<br> `var` IsHandled: `Boolean` |
| From version | 12.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeMatchUnitCost** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | PurchLine: `Record` "Purchase Line"<br> PurchRcptLine: `Record` "Purch. Rcpt. Line"<br> Template: `Record` "CDC Template"<br> Document: `Record` "CDC Document"<br> DocumentLine: `Record` "CDC Temp. Document Line"<br> TemplField: `Record` "CDC Template Field"<br> `var` UnitCost: `Decimal`<br> `var` Include: `Boolean`<br> `var` RemMatchQty: `Decimal`<br> `var` Matched: `Boolean`<br> `var` MatchUnitCostHandled: `Boolean` |
| From version | 12.1.0.0 |

### Codeunit 6085712 CDC Purch. Approval E-Mail


|   |   |
| --- | --- |
| Event name | **OnAfterApplyApprEntryFilters** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ApprEntry: `Record` "Approval Entry" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeIsNewEventEntry** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | EventEntryCmt: `Record` "CDC Event Entry Comment"<br> ApprovalEntry: `Record` "Approval Entry"<br> `var` IsHandled: `Boolean`<br> `var` Result: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSendReminderEmails** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateTableHeaderRow** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` BigString: `Codeunit` "CDC BigString Management"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnCreateTableHeaderRowOnBeforeAppendRow** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` BigString: `Codeunit` "CDC BigString Management" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateTableRow** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | PurchHeader: `Record` "Purchase Header"<br> ApprEntry: `Record` "Approval Entry"<br> `var` BigString: `Codeunit` "CDC BigString Management"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnCreateTableRowOnBeforeAppendRow** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | PurchHeader: `Record` "Purchase Header"<br> ApprEntry: `Record` "Approval Entry"<br> `var` BigString: `Codeunit` "CDC BigString Management" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateDocumentHTML** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` DocumentHTML: `Codeunit` "CDC BigString Management" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetApprovalHTMLBody** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` HTML: `Codeunit` "CDC BigString Management"<br> ContiniaUserSetup: `Record` "CDC Continia User Setup" |
| From version | 12.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetReminderHTMLBody** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` HTML: `Codeunit` "CDC BigString Management"<br> ApprovalEntry: `Record` "Approval Entry" |
| From version | 12.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetSharedReminderHTMLBody** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` HTML: `Codeunit` "CDC BigString Management"<br> ApprovalSharing: `Record` "CDC Approval Sharing"<br> ApprovalEntry: `Record` "Approval Entry" |
| From version | 12.1.0.0 |

### Codeunit 6085716 CDC Purch./Sales - Line Capt.


|   |   |
| --- | --- |
| Event name | **OnBeforeCaptureTablePageFind** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` DocumentPage: `Record` "CDC Document Page"<br> Document: `Record` "CDC Document" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCaptureTableCell** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Template: `Record` "CDC Template"<br> `var` Document: `Record` "CDC Document"<br> `var` "Page": `Record` "CDC Document Page"<br> `var` "Field": `Record` "CDC Template Field"<br> LineNo: `Integer`<br> Top: `Integer`<br> Left: `Integer`<br> Bottom: `Integer`<br> Right: `Integer`<br> NewBottom: `Integer` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnNotIsLineFieldsValid** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> LineNo: `Integer`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnCaptureTableOnAfterSetCaptionMarginPercent** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | FieldCaption: `Record` "CDC Template Field Caption"<br> "Field": `Record` "CDC Template Field"<br> "Page": `Record` "CDC Document Page"<br> CaptionStartWord: `array[100] of Record` "CDC Document Word"<br> CaptionEndWord: `array[100] of Record` "CDC Document Word"<br> `var` CaptionMarginPercent: `Decimal` |
| From version | 12.0.0.0 |

### Codeunit 6085720 CDC Purch. Alloc.-Post


|   |   |
| --- | --- |
| Event name | **OnAfterDateNoAllowed** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | PostingDate: `Date`<br> `var` DateIsNotAllowed: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePostGenJnlLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` GenJnlLine: `Record` "Gen. Journal Line"<br> `var` PurchAllocHeader: `Record` "CDC Purch. Allocation Header"<br> `var` PurchAllocLine: `Record` "CDC Purch. Allocation Line" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePostGenJnlBalAcc** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` GenJnlLine: `Record` "Gen. Journal Line"<br> `var` PurchAllocHeader: `Record` "CDC Purch. Allocation Header" |
| From version | 12.0.0.0 |

### Codeunit 6085722 CDC Approval Management


|   |   |
| --- | --- |
| Event name | **OnAfterCreateFlowApprovalEntriesMakeApprovalEntry** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ApprovalEntryArgument: `Record` "Approval Entry"<br> AppvlFlowLine: `Record` "CDC Approval Flow Line" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreatePurchApprovalRequest** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | PurchHeader: `Record` "Purchase Header"<br> WorkflowStepInstanceID: `Guid`<br> `var` Handled: `Boolean`<br> `var` ReturnValue: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeOnAfterApprovalRequest** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ApprovalEntry: `Record` "Approval Entry"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetDelegateToAndMethod** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ApprovalEntry: `Record` "Approval Entry"<br> `var` Selection: `Option Cancel,ApproveAndDelegate,DelegateWithoutApproval,DelegateAndSendBack`<br> `var` NewUserID: `Code[50]`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeAddApproverAfter** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ApprovalEntry: `Record` "Approval Entry"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeForceApproval** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchHeader: `Record` "Purchase Header"<br> IsManual: `Boolean`<br> `var` Handled: `Boolean`<br> `var` ReturnValue: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeBuildApprvlEntryFindSharedApprvlEntry** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ApprovalEntry: `Record` "Approval Entry" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeUpdateApprvlEntryByApproverFindApprvlEntry** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ApprovalEntry: `Record` "Approval Entry" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeUpdateApprovalEntry** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ApprovalEntry: `Record` "Approval Entry"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeUpdateApprvlEntryIfCanAppEntry** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ApprovalEntry: `Record` "Approval Entry"<br> `var` Handled: `Boolean`<br> `var` ReturnValue: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePurchDocSubmittingForApproval** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchHeader: `Record` "Purchase Header"<br> `var` Handled: `Boolean`<br> `var` ReturnValue: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckPurchApprovalRequest** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ApprovalEntry: `Record` "Approval Entry"<br> `var` PurchHeader: `Record` "Purchase Header"<br> ShowConfirmation: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeAutoApproveOrdersNotFullyApproved** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchHeader: `Record` "Purchase Header"<br> `var` Document: `Record` "CDC Document"<br> `var` Handled: `Boolean`<br> `var` ReturnValue: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckCanChangeImportedAmount** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | PurchHeader: `Record` "Purchase Header"<br> ShowError: `Boolean`<br> `var` Handled: `Boolean`<br> `var` ReturnValue: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckCanChangeImportedAmountGenJnlLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | GenJnlLine: `Record` "Gen. Journal Line"<br> ShowError: `Boolean`<br> `var` Handled: `Boolean`<br> `var` ReturnValue: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeFilterPurchHeaderForApprover** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | DocType: `Integer`<br> ApproverID: `Code[50]`<br> `var` PurchHeader: `Record` "Purchase Header"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePutOnHold** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchHeader: `Record` "Purchase Header"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeShowPurchDocFromApprEntry** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ApprovalEntry: `Record` "Approval Entry"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePurchDocSubmittedForApproval** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchHeader: `Record` "Purchase Header"<br> `var` ReturnValue: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateFourEyeApp** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | PurchHeader: `Record` "Purchase Header"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeAutoArchive** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ApprovalEntry: `Record` "Approval Entry"<br> `var` SuspendAutoArchive: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSendApprovalEmails** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterMakeApprovalEntry** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ApprovalEntry: `Record` "Approval Entry" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeRaiseErrorIfInvAdvApprFlowCode** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchHeader: `Record` "Purchase Header"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePurchDocSubmitApprovalConfirmAmounts** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | PurchHeader: `Record` "Purchase Header"<br> `var` SkipConfirm: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSendBackOrRejectApprovalReq** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ApprovalEntry: `Record` "Approval Entry"<br> `var` Answer: `Option` "Dialog Cancelled","Send Back",Reject<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeInsertPurchAllocHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | PurchaseHeader: `Record` "Purchase Header"<br> `var` PurchAllocationHeader: `Record` "CDC Purch. Allocation Header" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateFlowApprovalEntries** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | PurchaseHeader: `Record` "Purchase Header"<br> ApprovalEntry: `Record` "Approval Entry"<br> `var` Handled: `Boolean`<br> `var` Result: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckPurchDocAmtAgainstImpAmt** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` IsHandled: `Boolean`<br> PurchHeader: `Record` "Purchase Header"<br> ImportedAmountExclVAT: `Decimal`<br> ImportedAmountInclVAT: `Decimal`<br> `var` MessageText: `Text[1024]` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeDelegateWithoutApproval** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ApprovalEntry: `Record` "Approval Entry"<br> DelegateToUserID: `Code[50]`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |

### Codeunit 6085730 CDC Purch. - Val. Purch. Ord.


|   |   |
| --- | --- |
| Event name | **OnBeforeValidatePurchaseOrder** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterValidatePurchaseOrder** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document" |
| From version | 12.0.0.0 |

### Codeunit 6085746 CDC Advanced Appvl. Management


|   |   |
| --- | --- |
| Event name | **OnBeforeRaiseErrorIfNextApprIDBlank2** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchHeader: `Record` "Purchase Header"<br> `var` WorkflowStepInstanceID: `Guid`<br> `var` ApprovalEntry: `Record` "Approval Entry"<br> `var` NextApproverID: `Code[50]`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterUpdateDtldApprEntries** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ApprovalEntry: `Record` "Approval Entry"<br> `var` PurchHeader: `Record` "Purchase Header"<br> `var` AppvlGroup: `Record` "CDC Approval Group"<br> `var` ApprovalGroupUserID: `Code[50]`<br> `var` CurrentUser: `Code[50]`<br> `var` NextApproverID: `Code[50]`<br> `var` ActionToPerform: `Option Approve,FindNextApprover` |
| From version | 12.0.0.0 |

### Codeunit 6085749 CDC Purch. Doc. - Reopen


|   |   |
| --- | --- |
| Event name | **OnBeforeConfirmDocAlreadyLinked** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> PurchaseHeader: `Record` "Purchase Header" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterConfirmDocAlreadyLinked** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> PurchaseHeader: `Record` "Purchase Header" |
| From version | 12.2.0.0 |

### Codeunit 6085758 CDC Doc. - Move to Company


|   |   |
| --- | --- |
| Event name | **OnBeforeIdentifyTargetCompany** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` DocCat: `Record` "CDC Document Category"<br> `var` IdentifiedCompanyName: `Text[250]`<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterMoveDocument** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | OldDocument: `Record` "CDC Document"<br> NewDocument: `Record` "CDC Document"<br> SourceCompanyName: `Text[30]`<br> TargetCompanyName: `Text[30]` |
| From version | 12.0.0.0 |

### Codeunit 6085761 CDC Purch. - Line Rel. Mgt.


|   |   |
| --- | --- |
| Event name | **OnAfterSetReceiptLineInfo** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchLine: `Record` "Purchase Line"<br> `var` PurchRcptLine: `Record` "Purch. Rcpt. Line" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterPostPreviousDocument** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | RelPurchHeader: `Record` "Purchase Header"<br> PurchLineRel: `Record` "CDC Purchase Line Relationship"<br> PrevDocNo: `Code[20]` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterModifyRelatedDocument** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | PurchLineRel: `Record` "CDC Purchase Line Relationship"<br> `var` RelPurchLine: `Record` "Purchase Line" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterPostRelOrderLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | RelPurchHeader: `Record` "Purchase Header"<br> PurchLineRel: `Record` "CDC Purchase Line Relationship" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeUpdateRelatedHeaderDimensions** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` RelatedHeader: `Record` "Purchase Header"<br> PurchHeader: `Record` "Purchase Header"<br> `var` Handled: `Boolean` |
| From version | 12.2.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeUpdateRelatedLineDimensions** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` RelatedPurchLine: `Record` "Purchase Line"<br> PurchLine: `Record` "Purchase Line"<br> `var` Handled: `Boolean` |
| From version | 12.2.0.0 |

### Codeunit 6085762 CDC Purch.-Get Order


|   |   |
| --- | --- |
| Event name | **OnAfterInsertInvLineFromOrderLineValidateQuantity** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchInvLine: `Record` "Purchase Line"<br> `var` PurchOrderLine: `Record` "Purchase Line"<br> MatchedQuantity: `Decimal` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSetFilterPurchOrderLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchOrderLine: `Record` "Purchase Line" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | PurchHeader: `Record` "Purchase Header"<br> `var` IsHandled: `Boolean` |
| From version | 12.2.0.0 |

### Codeunit 6085770 CDC Sales - Management


|   |   |
| --- | --- |
| Event name | **OnBeforeGetDocType** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` DocType: `Integer`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetTranslLineInfo** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | TemplNo: `Code[20]`<br> CustItemNo: `Code[150]`<br> UseCustItemNos: `Boolean`<br> `var` LineTransl: `Record` "CDC Data Translation"<br> `var` IsHandled: `Boolean`<br> `var` ReturnValue: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetLineTranslAccountNo** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Template: `Record` "CDC Template"<br> `var` Document: `Record` "CDC Document"<br> LineNo: `Integer`<br> `var` DataTrans: `Record` "CDC Data Translation"<br> TranslateFrom: `Code[150]`<br> `var` Handled: `Boolean`<br> `var` FoundTranslation: `Boolean` |
| From version | 12.0.0.0 |

### Codeunit 6085773 CDC Sales - Full Capture


|   |   |
| --- | --- |
| Event name | **OnAfterFullCapture** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeAdjustMissingFields** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |

### Codeunit 6085774 CDC Sales - Line Validation


|   |   |
| --- | --- |
| Event name | **OnAfterRun** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` TempDocumentLine: `Record` "CDC Temp. Document Line" |
| From version | 12.0.0.0 |

### Codeunit 6085775 CDC Sales - Validation


|   |   |
| --- | --- |
| Event name | **OnBeforeCheckDifferentDateFormatsUsed** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> Template: `Record` "CDC Template"<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterValidateDocument** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> Template: `Record` "CDC Template"<br> `var` IsValid: `Boolean` |
| From version | 12.0.0.0 |

### Codeunit 6085776 CDC Sales - Register


|   |   |
| --- | --- |
| Event name | **OnBeforeCreateSalesHeaderInsert** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` SalesHeader: `Record` "Sales Header" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateSalesHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> SalesHeader: `Record` "Sales Header" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterTransferSalesLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` SalesLine: `Record` "Sales Line"<br> Document: `Record` "CDC Document"<br> LineNo: `Integer` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateSalesHeader2** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` SalesHeader: `Record` "Sales Header" |
| From version | 12.3.0.0 |

### Codeunit 6085778 CDC Sales - Show Reg. Doc.


|   |   |
| --- | --- |
| Event name | **OnRunOnSalesDocumentTypeCaseElse** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` DocNo: `Code[20]`<br> `var` DocDate: `Date` |
| From version | 12.0.0.0 |

### Codeunit 6085781 CDC Continia User Mgt.


|   |   |
| --- | --- |
| Event name | **OnAfterRenameRecord** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` RecRef: `RecordRef`<br> TableNo: `Integer`<br> NumberOfPrimaryKeyFields: `Integer`<br> UserName: `Code[50]`<br> Company: `Text[30]` |
| From version | 12.0.0.0 |
| Obsolete | Not used with Universal Code |



|   |   |
| --- | --- |
| Event name | **OnBeforeRenameContiniaUser** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | OldUserName: `Code[50]`<br> NewUserName: `Code[50]` |
| From version | 12.0.0.0 |

### Codeunit 6085786 CDC Workflow Response Handling


|   |   |
| --- | --- |
| Event name | **OnBeforeExecuteResponseStepInstance** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` NewWorkflowStepInstance: `Record` "Workflow Step Instance" |
| From version | 12.0.0.0 |

### Codeunit 6085789 CDC Single Instance Storage


|   |   |
| --- | --- |
| Event name | **OnPurchaseOrderCategoryInUse** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` SkipCheck: `Boolean` |
| From version | 12.1.0.0 |

### Codeunit 6085790 CDC Approvals Bridge


|   |   |
| --- | --- |
| Event name | **OnAfterApproveAdvancedApprovalRequested** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ApprovalEntry: `Record` "Approval Entry" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnApproveAndDelegateRequested** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ApprovalEntry: `Record` "Approval Entry" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnDelegateWithoutApprovalRequested** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ApprovalEntry: `Record` "Approval Entry" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnDelegateAndSendBackRequested** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ApprovalEntry: `Record` "Approval Entry" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnSendBackApprovalRequested** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ApprovalEntry: `Record` "Approval Entry" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnSendPurchDocForForceApproval** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchaseHeader: `Record` "Purchase Header" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSendPurchDocApprovalRequest** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchHeader: `Record` "Purchase Header"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeForward** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchHeader: `Record` "Purchase Header"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterRejectApprovalRequests** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ApprovalEntry: `Record` "Approval Entry"<br> `var` PurchHeader: `Record` "Purchase Header" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCancelApprovalRequest** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchHeader: `Record` "Purchase Header"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeFilterPurchAppWorkflows** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | DocType: `Integer`<br> `var` Workflow: `Record Workflow`<br> FilterType: `Option` "Only DC","Only Standard",All<br> `var` FilterString: `Text[1024]`<br> `var` ReturnValue: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeIsPurchForceApprEnabledDocType** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | DocType: `Integer`<br> `var` Handled: `Boolean`<br> `var` ReturnValue: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSetApprovalButtons** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | PurchHeader: `Record` "Purchase Header"<br> `var` EnableForceAppr: `Boolean`<br> `var` EnableSendAppr: `Boolean`<br> `var` EnableCancelApprov: `Boolean`<br> `var` EnableApprove: `Boolean`<br> `var` EnableReject: `Boolean`<br> `var` EnableForward: `Boolean`<br> `var` EnableOnHold: `Boolean`<br> `var` ShowApprFactBox: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnSendDocumentForApproval** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeApproveApprovalRequest** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ApprovalEntry: `Record` "Approval Entry"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeDeleteTempPurchLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchaseHeader: `Record` "Purchase Header" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeRejectedApprovalEntryModify** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ApprovalEntry: `Record` "Approval Entry" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeNewWorkflowStepInstance** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` NewWorkflowStepInstance: `Record` "Workflow Step Instance"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterInitializeApprovalEntry** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ApprovalEntry: `Record` "Approval Entry"<br> RecRef: `RecordRef` |
| From version | 12.0.0.0 |

### Codeunit 6085808 CDC Document No. Series Mgt.


|   |   |
| --- | --- |
| Event name | **OnBeforeGetMainNoseriesCode** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` MainNoseriesCode: `Code[20]`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |

### Codeunit 6085813 CDC Open Document E-Mail


|   |   |
| --- | --- |
| Event name | **OnBeforeSendReminderEmails** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateTableHeaderRow** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` BigString: `Codeunit` "CDC BigString Management"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnCreateTableHeaderRowOnBeforeAppendRow** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` BigString: `Codeunit` "CDC BigString Management" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateTableRow** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` BigString: `Codeunit` "CDC BigString Management"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnCreateTableRowOnBeforeAppendRow** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` BigString: `Codeunit` "CDC BigString Management" |
| From version | 12.0.0.0 |

### Codeunit 6085830 CDC Match Tracking Mgt.


|   |   |
| --- | --- |
| Event name | **OnBeforeTransferMatchTracking** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ToPurchLine: `Record` "Purchase Line"<br> PurchDocMatch: `Record` "CDC Purch. Doc. Match"<br> DeleteExistingTracking: `Boolean`<br> UpdateExistingTracking: `Boolean`<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |

### Codeunit 6085871 CDC Business Setup Management


|   |   |
| --- | --- |
| Event name | **OnAfterInsertPurchContractManualSetup** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | AlreadyInserted: `Boolean`<br> `var` sender: `Codeunit` "Guided Experience" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnSkipInsertManualSetup** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` sender: `Codeunit` "Guided Experience" |
| From version | 12.0.0.0 |

### Codeunit 6085921 CDC Purchase Line Subscr.


|   |   |
| --- | --- |
| Event name | **OnBeforeResetUnitCostOnAfterValidateNo** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchaseLine: `Record` "Purchase Line"<br> `var` xPurchaseLine: `Record` "Purchase Line"<br> `var` Suspend: `Boolean` |
| From version | 12.0.0.0 |

### Codeunit 6086001 CDC Approval Functions (WS)


|   |   |
| --- | --- |
| Event name | **OnBeforeCopyDocumentLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | LCID: `Integer`<br> DocumentType: `Integer`<br> DocumentNo: `Code[20]`<br> LineNo: `Integer`<br> `var` NewLineNo: `Integer`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeReject** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | LCID: `Integer`<br> MenuCode: `Code[20]`<br> SubMenuCode: `Code[20]`<br> TableID: `Integer`<br> DocumentType: `Integer`<br> DocumentNo: `Code[20]`<br> ApproverId: `Code[50]`<br> ReasonCode: `Code[10]`<br> `var` NextTableID: `Integer`<br> `var` NextDocumentType: `Integer`<br> `var` NextDocumentNo: `Code[20]`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeForward** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | LCID: `Integer`<br> MenuCode: `Code[20]`<br> SubMenuCode: `Code[20]`<br> TableID: `Integer`<br> DocumentType: `Integer`<br> DocumentNo: `Code[20]`<br> ApproverId: `Code[50]`<br> DelegateToUserId: `Code[50]`<br> DelegateAction: `Integer`<br> `var` NextTableID: `Integer`<br> `var` NextDocumentType: `Integer`<br> `var` NextDocumentNo: `Code[20]`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePutOnHoldHandled** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | LCID: `Integer`<br> TableID: `Integer`<br> DocumentType: `Integer`<br> DocumentNo: `Code[20]`<br> ApproverId: `Code[50]`<br> ReasonCode: `Code[10]`<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeAddDocumentLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | LCID: `Integer`<br> DocumentType: `Integer`<br> DocumentNo: `Code[20]`<br> `var` NewLineNo: `Integer`<br> Type: `Integer`<br> AmountExclVAT: `Decimal`<br> AmountInclVAT: `Decimal` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeDeleteDocumentLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | LCID: `Integer`<br> DocumentType: `Integer`<br> DocumentNo: `Code[20]`<br> LineNo: `Integer` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnGetDocumentFile** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | DocNo: `Code[20]`<br> `var` TempFile: `Record` "CDC Temp File"<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnGetHtmlFile** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | DocNo: `Code[20]`<br> `var` TempFile: `Record` "CDC Temp File"<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnGetApprovalPDFDocumentTypeCaseElse** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | TableID: `Integer`<br> FileName: `Text[1024]`<br> DocumentType: `Integer`<br> DocumentNo: `Code[20]`<br> PDFReportID: `Integer`<br> `var` TempFile: `Record` "CDC Temp File" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSetPreDefinedDocumentPermissions** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | LCID: `Integer`<br> TableID: `Integer`<br> DocumentType: `Integer`<br> DocumentNo: `Code[20]`<br> ApproverId: `Code[50]`<br> `var` AllowView: `Boolean`<br> `var` AllowAddComment: `Boolean`<br> `var` AllowAttachFiles: `Boolean`<br> `var` AllowApprove: `Boolean`<br> `var` AllowReject: `Boolean`<br> `var` AllowForward: `Boolean`<br> `var` AllowPutOnHold: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetPathandFilename** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ToURL: `Text[1024]`<br> DocomentNo: `Code[20]`<br> `var` Path: `Text[1024]`<br> `var` Filename: `Text[1024]`<br> NSTLanguageID: `Integer`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |

### Codeunit 6086004 CDC Web Job and Dim. Mgnt.


|   |   |
| --- | --- |
| Event name | **OnBeforeGetPurchLineTaskInfo** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | PurchLine: `Record` "Purchase Line"<br> `var` JobTaskNo: `Code[20]`<br> `var` JobTaskDesc: `Text[100]`<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateJobTaskNo** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | JobTaskNo: `Code[20]`<br> `var` PurchLine: `Record` "Purchase Line"<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterValidateJobTaskNo** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | JobTaskNo: `Code[20]`<br> `var` PurchLine: `Record` "Purchase Line" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeUpdateWebDim** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchLine: `Record` "Purchase Line"<br> "Code": `Code[20]`<br> ValueCode: `Code[20]`<br> CurrUserId: `Code[50]` |
| From version | 12.0.0.0 |

### Codeunit 6086026 CDC Item Reference Mgt.


|   |   |
| --- | --- |
| Event name | **OnBeforeUpdateItemRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ReferenceTypeNo: `Code[50]`<br> LineNo: `Integer`<br> ToType: `Integer`<br> ToNo: `Code[20]`<br> `var` LineTransl: `Record` "CDC Data Translation"<br> VendItemNo: `Code[250]`<br> `var` Item: `Record Item`<br> ReferenceType: `Integer`<br> `var` IsHandled: `Boolean` |
| From version | 12.2.0.0 |

### Codeunit 6086029 CDC Message Center Setup Mgt.


|   |   |
| --- | --- |
| Event name | **OnAfterCreateMessageCenterSetup** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | DocumentComment: `Record` "CDC Document Comment" |
| From version | 12.0.0.0 |

### Codeunit 6086035 CDC Gen. Jnl. Mgt.


|   |   |
| --- | --- |
| Event name | **OnBeforeCheckAmountOnPost** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` GenJournalLine: `Record` "Gen. Journal Line"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |

### Codeunit 6086044 CDC Text Management


|   |   |
| --- | --- |
| Event name | **OnBeforeGetDocumentID** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` DocumentID: `Text`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |

### Codeunit 6086055 CDC Purch. Order - Validation


|   |   |
| --- | --- |
| Event name | **OnBeforeBuildTempLinesTable** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` DocumentLines: `Record` "CDC Temp. Document Line" temporary<br> `var` IsValid: `Boolean`<br> `var` LinesHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetDocumentDate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` DueDate: `Date`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeTotalAmountNegCheck** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` IsValid: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckExternalDocNo** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> ExtDocNo: `Code[250]`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateAmtAccounts** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` Template: `Record` "CDC Template"<br> `var` IsInvalid: `Boolean`<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |

### Codeunit 6086056 CDC Purchase Order - Register


|   |   |
| --- | --- |
| Event name | **OnBeforeCreatePurchHeaderCopyHeaderDim** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | PurchDocMatch: `Record` "CDC Purch. Doc. Match"<br> `var` PurchHeader: `Record` "Purchase Header"<br> PurchaserCode: `Code[20]`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateWithoutMatchModifyPurchLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` PurchLine: `Record` "Purchase Line"<br> DocumentLineNo: `Integer` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateWithoutMatchLineTrans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchLine: `Record` "Purchase Line"<br> LineTrans: `Record` "CDC Data Translation" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterModifyPurchLineCreatePurchLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` PurchLine: `Record` "Purchase Line" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterModifyPurchLineCreatePurchLineAmountDistribution** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` PurchLine: `Record` "Purchase Line"<br> IsHeadingLine: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreatePurchLineLineTrans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchLine: `Record` "Purchase Line"<br> DataTransl: `Record` "CDC Data Translation" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterTransferPurchHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchHeader: `Record` "Purchase Header"<br> `var` Document: `Record` "CDC Document" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePurchHeaderInsert** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` PurchHeader: `Record` "Purchase Header" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterRegister** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterPerformStep1** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` PurchaseHeader: `Record` "Purchase Header" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePerformStep2** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` Template: `Record` "CDC Template"<br> `var` PurchHeader: `Record` "Purchase Header"<br> `var` SkipNextStep: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeShowAfterRegister** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterTransferPurchLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchLine: `Record` "Purchase Line"<br> Document: `Record` "CDC Document"<br> DocumentLineNo: `Integer` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateWithoutMatchSetAccountRequired** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` DocumentLine: `Record` "CDC Temp. Document Line" temporary<br> `var` AccountRequired: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateWithMatchGetPurchLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | PurchDocMatch: `Record` "CDC Purch. Doc. Match"<br> `var` PurchaseLine: `Record` "Purchase Line"<br> `var` NextLineNo: `Integer`<br> `var` PurchLineGetHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreatePurchHeaderWithoutMatch** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` PurchHeader: `Record` "Purchase Header" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeTransferLineDim** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> LineNo: `Integer`<br> `var` PurchLine: `Record` "Purchase Line"<br> `var` LineTrans: `Record` "CDC Data Translation"<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateWithoutMatchCreateLinesByHeaderAmounts** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` PurchaseHeader: `Record` "Purchase Header"<br> PurchaserCode: `Code[20]`<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeRegisterDocument** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeaderAmounts** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` PurchHeader: `Record` "Purchase Header"<br> `var` "Field": `Record` "CDC Template Field"<br> `var` Template: `Record` "CDC Template"<br> LinesRecognised: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeaderAmountsWithTextLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` PurchHeader: `Record` "Purchase Header"<br> `var` "Field": `Record` "CDC Template Field"<br> `var` Template: `Record` "CDC Template"<br> LinesRecognised: `Boolean`<br> TextLineArray: `array[50] of Text[1024]`<br> NoOfTextLines: `Integer`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeUpdateHeaderAmounts** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` PurchHeader: `Record` "Purchase Header"<br> `var` "Field": `Record` "CDC Template Field"<br> `var` Template: `Record` "CDC Template"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePerformStep1** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeProcessDocumentLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` TempDocumentLine: `Record` "CDC Temp. Document Line" temporary<br> PurchaseHeader: `Record` "Purchase Header" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckWMS** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | PurchLine: `Record` "Purchase Line"<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePostPrepayment** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` PurchHeader: `Record` "Purchase Header"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeModifyPurchHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchaseHeader: `Record` "Purchase Header"<br> `var` Document: `Record` "CDC Document" |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckDuplicateNumber** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | PurchaseHeader: `Record` "Purchase Header"<br> CDCDocument: `Record` "CDC Document"<br> OrderNo: `Code[100]` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeUpdatePurchLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> PurchHeader: `Record` "Purchase Header"<br> `var` PurchLine: `Record` "Purchase Line"<br> DocumentLine: `Record` "CDC Temp. Document Line"<br> DataTranslation: `Record` "CDC Data Translation" temporary<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |

### Codeunit 6086061 CDC Master Data Mgt. Subsc.


|   |   |
| --- | --- |
| Event name | **OnBeforeErrorMasterDataTableInsert** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SynchTableID: `Integer`<br> `var` OverrideError: `Boolean` |
| From version | 12.0.0.0 |

### Codeunit 6086073 CDC Secure Archive Subsc.


|   |   |
| --- | --- |
| Event name | **OnBeforeDeleteExclFromViews** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` SkipExcludeFromView: `Boolean` |
| From version | 12.0.0.0 |

### Codeunit 6086079 CDC Digital Voucher Mgt.


|   |   |
| --- | --- |
| Event name | **OnBeforeCreateDigitalVoucher** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | DestinationRecID: `RecordID`<br> Document: `Record` "CDC Document"<br> `var` Handled: `Boolean` |
| From version | 12.2.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateDigitalVoucherOnPostedDoc** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | DestinationRecID: `RecordID`<br> Document: `Record` "CDC Document"<br> `var` Handled: `Boolean` |
| From version | 12.2.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeAppendDnDToIncomingDoc** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> `var` Handled: `Boolean` |
| From version | 12.2.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateDigitalVoucherForEDocument** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | DestinationRecID: `RecordID`<br> eDocument: `Record` "CTS-CDN Document"<br> `var` Handled: `Boolean` |
| From version | 12.2.0.0 |

### Codeunit 6086202 CDC XML Line Capt.


|   |   |
| --- | --- |
| Event name | **OnNotIsLineFieldsValid** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Document: `Record` "CDC Document"<br> LineNo: `Integer`<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |

### Codeunit 6086217 CDC UTS Validation


|   |   |
| --- | --- |
| Event name | **OnBeforeFindRelatedDocument** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` RelatedDocument: `Record` "CDC Document"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |

### Codeunit 6086218 CDC UTS - Register


|   |   |
| --- | --- |
| Event name | **OnBeforeFindRelatedDocument** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` RelatedDocument: `Record` "CDC Document"<br> `var` Handled: `Boolean` |
| From version | 12.0.0.0 |

### Codeunit 6225181 CDC Review Mgt.


|   |   |
| --- | --- |
| Event name | **OnBeforeSendReviewEmails** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | IsHandled: `Boolean` |
| From version | 12.0.0.0 |

### Codeunit 6225201 CDC Purch. Contr. Creation


|   |   |
| --- | --- |
| Event name | **OnAfterInsertContractHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchContractHeader: `Record` "CDC Purch. Contract Header"<br> DocRecRef: `RecordRef` |
| From version | 12.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreatePurchaseContractFromDocument** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Document: `Record` "CDC Document"<br> `var` IsHandled: `Boolean` |
| From version | 12.0.0.0 |



<style>
  .content table tr td:nth-child(1) {
    width: 130px;
  }
  .content table tr td:nth-child(2) {
    width: 600px;
  }  
  .content table {
    margin: 0rem 0 2rem 0;
  }
</style>
