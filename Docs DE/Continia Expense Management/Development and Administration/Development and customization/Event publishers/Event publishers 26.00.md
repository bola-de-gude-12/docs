---
title: Event Publisher für Expense Management (26.00)
date: 24-03-2025
description:
id: EM-303
lang: de
---

# Event Publisher für Expense Management (26.00)

Die folgenden Event Publisher sind in Continia Expense Management  (26.00) enthalten:

### Table 6086309 CEM Posting Setup


|   |   |
| --- | --- |
| Event name | **OnBeforeModifyExistingExpense** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | PostingSetup: `Record` "CEM Posting Setup"<br> External: `Boolean`<br> `var` Expense: `Record` "CEM Expense" |
| From version | 25.0.0.0 |


|   |   |
| --- | --- |
| Event name | **OnBeforeModifyExistingMileage** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | PostingSetup: `Record` "CEM Posting Setup"<br> External: `Boolean`<br> `var` Mileage: `Record` "CEM Mileage" |
| From version | 25.0.0.0 |

### Table 6086320 CEM Expense


|   |   |
| --- | --- |
| Event name | **OnExpenseTypeValidateBeforeExpValidation** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ExpPostingSetup: `Record` "CEM Posting Setup"<br> ValidPostingSetupFound: `Boolean`<br> `var` Expense: `Record` "CEM Expense" |
| From version | 25.0.0.0 |
| Obsolete | Use 6086311 "CEM Expense Bank Trans. Mgt." - OnBeforeSendExpenseToUser() instead |


|   |   |
| --- | --- |
| Event name | **OnAfterNewCalculatedAccount** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Expense: `Record` "CEM Expense"<br> `var` NewCalculatedAccount: `Code[20]`<br> ExpPostingSetup: `Record` "CEM Posting Setup" |
| From version | 25.0.0.0 |


|   |   |
| --- | --- |
| Event name | **OnAfterAddAttachment** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Expense: `Record` "CEM Expense"<br> `var` Attachment: `Record` "CEM Attachment" |
| From version | 25.0.0.0 |

### Table 6086330 CEM Bank Transaction


|   |   |
| --- | --- |
| Event name | **OnBeforeInsertExpense** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |

|   |   |
| --- | --- |
| Event name | **OnAfterNewCalculatedAccount** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Expense: `Record` "CEM Expense"<br> `var` NewCalculatedAccount: `Code[20]`<br> ExpPostingSetup: `Record` "CEM Posting Setup" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterAddAttachment** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Expense: `Record` "CEM Expense"<br> `var` Attachment: `Record` "CEM Attachment" |
| From version | 26.0.0.0 |

### Table 6086330 CEM Bank Transaction


|   |   |
| --- | --- |
| Event name | **OnBeforeInsertExpense** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Transaction: `Record` "CEM Bank Transaction"<br> `var` Expense: `Record` "CEM Expense" |
| From version | 26.0.0.0 |

### Table 6086333 CEM Exp. Posting Desc. Field


|   |   |
| --- | --- |
| Event name | **OnBeforeReplacePlaceholdersWithValues** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | TableID: `Integer`<br> DocumentType: `Integer`<br> DocumentNo: `Code[20]`<br> DocRefNo: `Integer`<br> `var` PostingDesc: `Text[1024]`<br> `var` IsHandled: `Boolean` |
| From version | 26.0.0.0 |

### Table 6086338 CEM Mileage


|   |   |
| --- | --- |
| Event name | **OnBeforeCalcMileageDetails** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Mileage: `Record` "CEM Mileage"<br> `var` IsHandled: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterCalcMileageDetails** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Mileage: `Record` "CEM Mileage" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnBeforeSetCalculationTolerance** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Tolerance: `Decimal`<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterAddAttachment** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Mileage: `Record` "CEM Mileage"<br> `var` Attachment: `Record` "CEM Attachment" |
| From version | 26.0.0.0 |

### Table 6086370 CEM Mileage Rate


|   |   |
| --- | --- |
| Event name | **OnBeforeRecalcMilRate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Company: `Record Company` |
| From version | 26.0.0.0 |

### Report 6086312 CEM Batch Post Expenses


|   |   |
| --- | --- |
| Event name | **OnBeforeOnOpenPage** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PostingDatePolicy: `Option` "First Document Date","Last Document Date","Specific Date"<br> `var` ReplacePostingDate: `Boolean`<br> `var` PostingDateReq: `Date`<br> `var` PostingDateEditable: `Boolean`<br> `var` PostingDatePolicyEditable: `Boolean`<br> `var` IsHandled: `Boolean` |
| From version | 26.0.0.0 |

### Report 6086313 CEM Batch Post Mileage


|   |   |
| --- | --- |
| Event name | **OnBeforeOnOpenPage** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PostingDatePolicy: `Option` "First Document Date","Last Document Date","Specific Date"<br> `var` ReplacePostingDate: `Boolean`<br> `var` PostingDateReq: `Date`<br> `var` PostingDateEditable: `Boolean`<br> `var` PostingDatePolicyEditable: `Boolean`<br> `var` IsHandled: `Boolean` |
| From version | 26.0.0.0 |

### Report 6086314 CEM Batch Post Settlements


|   |   |
| --- | --- |
| Event name | **OnBeforeOnOpenPage** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PostingDatePolicy: `Option` "First Document Date","Last Document Date","Specific Date"<br> `var` ReplacePostingDate: `Boolean`<br> `var` PostingDateReq: `Date`<br> `var` PostingDateEditable: `Boolean`<br> `var` PostingDatePolicyEditable: `Boolean`<br> `var` IsHandled: `Boolean` |
| From version | 26.0.0.0 |

### Report 6086315 CEM Batch Post Per Diems


|   |   |
| --- | --- |
| Event name | **OnBeforeOnOpenPage** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PostingDatePolicy: `Option` "First Document Date","Last Document Date","Specific Date"<br> `var` ReplacePostingDate: `Boolean`<br> `var` PostingDateReq: `Date`<br> `var` PostingDateEditable: `Boolean`<br> `var` PostingDatePolicyEditable: `Boolean`<br> `var` IsHandled: `Boolean` |
| From version | 26.0.0.0 |

### Report 6086319 CEM Export Attachments


|   |   |
| --- | --- |
| Event name | **OnExportAttachmentsOnCreateFileName** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Expense: `Record` "CEM Expense"<br> TempFile: `Record` "CDC Temp File" temporary<br> `var` FileName: `Text`<br> `var` IsHandled: `Boolean` |
| From version | 26.0.0.0 |

### Page 6086402 CEM Client Addin - Settlement


|   |   |
| --- | --- |
| Event name | **OnHandleXmlCommandOnActiveRecordChanged** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ActiveTableID: `Integer`<br> `var` RecordRef: `RecordRef`<br> `var` IsHandled: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnLoadImageFromRecIDOnAfterSetRecRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | RecRef: `RecordRef`<br> `var` TableID: `Integer`<br> `var` DocRefNo: `Integer` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnLoadImageFromRecIDOnAfterFilterAttachment** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | RecRef: `RecordRef`<br> TableID: `Integer`<br> DocRefNo: `Integer`<br> `var` EMAttachment: `Record` "CEM Attachment" |
| From version | 26.0.0.0 |

### Codeunit 6086302 CEM Navigate Mileage - Find


|   |   |
| --- | --- |
| Event name | **OnBeforeNavigateMileage** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Mileage: `Record` "CEM Mileage"<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

### Codeunit 6086304 CEM Shortcut Field Functions


|   |   |
| --- | --- |
| Event name | **OnAfterValidateShortcutFieldValue** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | TableID: `Integer`<br> DocumentType: `Integer`<br> DocumentNo: `Code[20]`<br> DocRefNo: `Integer`<br> DimCode: `Code[20]`<br> FieldCode: `Code[20]`<br> `var` ShortcutFieldValue: `Text[250]` |
| From version | 26.0.0.0 |

### Codeunit 6086306 CEM About Expense Management


|   |   |
| --- | --- |
| Event name | **OnAfterFullProductName** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ProductName: `Text[50]`<br> `var` ProductVariant: `Text[20]` |
| From version | 26.0.0.0 |

### Codeunit 6086308 CEM Expense Inbox-Transfer


|   |   |
| --- | --- |
| Event name | **OnBeforeInsertEMDimensions** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Expense: `Record` "CEM Expense" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterInsertEMDimensions** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Expense: `Record` "CEM Expense" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterHandleAllocations** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Expense: `Record` "CEM Expense" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnBeforeExpenseAllocInsert** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ExpenseAllocation: `Record` "CEM Expense Allocation" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterExpenseInboxTransfer** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Expense: `Record` "CEM Expense" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterExpenseInboxTransfer2** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Expense: `Record` "CEM Expense"<br> ExpenseInbox: `Record` "CEM Expense Inbox" |
| From version | 26.0.0.0 |

### Codeunit 6086311 CEM Expense Bank Trans. Mgt.


|   |   |
| --- | --- |
| Event name | **OnBeforeSendExpenseToUser** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Expense: `Record` "CEM Expense"<br> `var` IsHandled: `Boolean` |
| From version | 26.0.0.0 |

### Codeunit 6086312 CEM Approval Management


|   |   |
| --- | --- |
| Event name | **OnAfterInitApproverID** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | TableID: `Integer`<br> DocumentNo: `Code[20]`<br> `var` InitialApproverID: `Code[50]` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnBeforeApprovalMgtCode** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | TableID: `Integer`<br> DocumentNo: `Code[20]`<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnBeforeAutoApproveExpense** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Expense: `Record` "CEM Expense" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnBeforeAutoApproveMileage** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Mileage: `Record` "CEM Mileage" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterInitializeApprovalEntry** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | TableID: `Integer`<br> DocumentNo: `Code[20]`<br> `var` ApprovalEntry: `Record` "Approval Entry"<br> `var` ApprovalAmount: `Decimal`<br> `var` ApprovalAmountLCY: `Decimal` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnBeforeGetNextApprover** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | TableID: `Integer`<br> DocumentNo: `Code[20]`<br> `var` ApproverID: `Code[50]`<br> `var` IsHandled: `Boolean` |
| From version | 26.0.0.0 |

### Codeunit 6086317 CEM Navigate Bnk Trans. - Find


|   |   |
| --- | --- |
| Event name | **OnBeforeNavigateBankTrans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | BankTransaction: `Record` "CEM Bank Transaction"<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

### Codeunit 6086318 CEM Dimension Mgt.


|   |   |
| --- | --- |
| Event name | **OnBeforeInsertDefaultDimOnExpense** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | TableID: `Integer`<br> AccountNo: `Code[20]`<br> `var` Expense: `Record` "CEM Expense" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterInsertDefaultDimOnExpense** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | TableID: `Integer`<br> AccountNo: `Code[20]`<br> `var` Expense: `Record` "CEM Expense" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnBeforeDeleteDefaultDimOnExpense** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | TableID: `Integer`<br> AccountNo: `Code[20]`<br> `var` Expense: `Record` "CEM Expense" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterDeleteDefaultDimOnExpense** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | TableID: `Integer`<br> AccountNo: `Code[20]`<br> `var` Expense: `Record` "CEM Expense" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnBeforeInsertDefaultDimOnMileage** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | TableID: `Integer`<br> AccountNo: `Code[20]`<br> `var` Mileage: `Record` "CEM Mileage" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterInsertDefaultDimOnMileage** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | TableID: `Integer`<br> AccountNo: `Code[20]`<br> `var` Mileage: `Record` "CEM Mileage" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnBeforeDeleteDefaultDimOnMileage** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | TableID: `Integer`<br> AccountNo: `Code[20]`<br> `var` Mileage: `Record` "CEM Mileage" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterDeleteDefaultDimOnMileage** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | TableID: `Integer`<br> AccountNo: `Code[20]`<br> `var` Mileage: `Record` "CEM Mileage" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnBeforeInsertDefaultDimOnExpHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | TableID: `Integer`<br> AccountNo: `Code[20]`<br> `var` ExpHeader: `Record` "CEM Expense Header" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterInsertDefaultDimOnExpHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | TableID: `Integer`<br> AccountNo: `Code[20]`<br> `var` ExpHeader: `Record` "CEM Expense Header" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnBeforeDeleteDefaultDimOnExpHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | TableID: `Integer`<br> AccountNo: `Code[20]`<br> `var` ExpHeader: `Record` "CEM Expense Header" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterDeleteDefaultDimOnExpHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | TableID: `Integer`<br> AccountNo: `Code[20]`<br> `var` ExpHeader: `Record` "CEM Expense Header" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnBeforeInsertDefaultDimOnPerDiem** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | TableID: `Integer`<br> AccountNo: `Code[20]`<br> `var` PerDiem: `Record` "CEM Per Diem" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterInsertDefaultDimOnPerDiem** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | TableID: `Integer`<br> AccountNo: `Code[20]`<br> `var` PerDiem: `Record` "CEM Per Diem" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnBeforeDeleteDefaultDimOnPerDiem** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | TableID: `Integer`<br> AccountNo: `Code[20]`<br> `var` PerDiem: `Record` "CEM Per Diem" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterDeleteDefaultDimOnPerDiem** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | TableID: `Integer`<br> AccountNo: `Code[20]`<br> `var` PerDiem: `Record` "CEM Per Diem" |
| From version | 26.0.0.0 |

### Codeunit 6086319 CEM NAV-version Mgt.


|   |   |
| --- | --- |
| Event name | **OnBeforePostGenJnlLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` GenJournalLine: `Record` "Gen. Journal Line" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnBeforePostJobJnlLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` JobJournalLine: `Record` "Job Journal Line" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterCreateJnlLineDefaultDim** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` GenJnlPostLine: `Codeunit` "Gen. Jnl.-Post Line"<br> `var` GenJnlLine: `Record` "Gen. Journal Line"<br> TableID: `Integer`<br> DocumentType: `Integer`<br> DocumentNo: `Code[20]`<br> DocRefNo: `Integer` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnBeforePostGenJnlLine2** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` GenJnlPostLine: `Codeunit` "Gen. Jnl.-Post Line"<br> `var` GenJnlLine: `Record` "Gen. Journal Line"<br> TableID: `Integer`<br> DocumentType: `Integer`<br> DocumentNo: `Code[20]`<br> DocRefNo: `Integer` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterPostGenJnlLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` GenJnlPostLine: `Codeunit` "Gen. Jnl.-Post Line"<br> `var` GenJnlLine: `Record` "Gen. Journal Line"<br> TableID: `Integer`<br> DocumentType: `Integer`<br> DocumentNo: `Code[20]`<br> DocRefNo: `Integer`<br> GLEntryNo: `Integer` |
| From version | 26.0.0.0 |

### Codeunit 6086321 CEM Expense-Validate


|   |   |
| --- | --- |
| Event name | **OnBeforeExpenseValidate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Rec: `Record` "CEM Expense" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterExpenseValidate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Rec: `Record` "CEM Expense" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnBeforeValidateAttachments** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Rec: `Record` "CEM Expense"<br> `var` IsHandled: `Boolean` |
| From version | 26.0.0.0 |

### Codeunit 6086322 CEM Navigate Expense - Find


|   |   |
| --- | --- |
| Event name | **OnBeforeNavigateExpense** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Expense: `Record` "CEM Expense"<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

### Codeunit 6086326 CEM Navigate Settlement - Find


|   |   |
| --- | --- |
| Event name | **OnBeforeNavigateSettlements** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Settlement: `Record` "CEM Expense Header"<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

### Codeunit 6086330 CEM Expense-Post


|   |   |
| --- | --- |
| Event name | **OnBeforePostExpense** |
| Event type | IntegrationEvent(IncludeSender : `TRUE`, GlobalVarAccess : `false`) |
| Parameters | `var` Expense: `Record` "CEM Expense"<br> `var` IsPosted: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterPostExpense** |
| Event type | IntegrationEvent(IncludeSender : `TRUE`, GlobalVarAccess : `false`) |
| Parameters | `var` Expense: `Record` "CEM Expense" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnBeforeValidatePricesInclVAT** |
| Event type | IntegrationEvent(IncludeSender : `TRUE`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchHeader: `Record` "Purchase Header"<br> `var` Expense: `Record` "CEM Expense"<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterEmployeePICreated** |
| Event type | IntegrationEvent(IncludeSender : `TRUE`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchHeader: `Record` "Purchase Header"<br> `var` Expense: `Record` "CEM Expense" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterEmployeeCrMemoCreated** |
| Event type | IntegrationEvent(IncludeSender : `TRUE`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchHeader: `Record` "Purchase Header"<br> `var` Expense: `Record` "CEM Expense" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterBankPICreated** |
| Event type | IntegrationEvent(IncludeSender : `TRUE`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchHeader: `Record` "Purchase Header"<br> `var` Expense: `Record` "CEM Expense" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterBusVendorPICreated** |
| Event type | IntegrationEvent(IncludeSender : `TRUE`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchHeader: `Record` "Purchase Header"<br> `var` Expense: `Record` "CEM Expense" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnShouldSkipPosting** |
| Event type | IntegrationEvent(IncludeSender : `TRUE`, GlobalVarAccess : `false`) |
| Parameters | ExpenseAllocation: `Record` "CEM Expense Allocation"<br> `var` SkipPosting: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterAddLineToInvoice** |
| Event type | IntegrationEvent(IncludeSender : `TRUE`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchLine: `Record` "Purchase Line"<br> Expense2: `Record` "CEM Expense" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAddLineToInvoiceOnBeforeValidateDirectUnitCost** |
| Event type | IntegrationEvent(IncludeSender : `TRUE`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchaseLine: `Record` "Purchase Line"<br> Expense: `Record` "CEM Expense"<br> `var` IsHandled: `Boolean` |
| From version | 26.0.0.0 |

### Codeunit 6086331 CEM Expense-Post (Yes/No)


|   |   |
| --- | --- |
| Event name | **OnBeforeConfirmAccMissmatch** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Expense: `Record` "CEM Expense"<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

### Codeunit 6086333 CEM Expense - Check


|   |   |
| --- | --- |
| Event name | **OnBeforeCheckExpense** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Expense: `Record` "CEM Expense" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterCheckExpense** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Expense: `Record` "CEM Expense" |
| From version | 26.0.0.0 |

### Codeunit 6086336 CEM Posting Functions


|   |   |
| --- | --- |
| Event name | **OnBeforeAddJobsToJnlLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` GenJnlLine: `Record` "Gen. Journal Line"<br> Jobno: `Code[20]`<br> JobTaskNo: `Code[20]`<br> JobLineType: `Option` " ",Schedule,Contract,"Both Schedule and Contract"<br> Billable: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterAddJobsToJnlLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` GenJnlLine: `Record` "Gen. Journal Line"<br> Jobno: `Code[20]`<br> JobTaskNo: `Code[20]`<br> JobLineType: `Option` " ",Schedule,Contract,"Both Schedule and Contract"<br> Billable: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnBeforeCreateJobJnlLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | GenJnlLine: `Record` "Gen. Journal Line"<br> `var` JobJnlLine: `Record` "Job Journal Line"<br> Jobno: `Code[20]`<br> TaskNo: `Code[20]`<br> JobLineType: `Option` " ",Schedule,Contract,"Both Schedule and Contract"<br> Billable: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterCreateJobJnlLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | GenJnlLine: `Record` "Gen. Journal Line"<br> `var` JobJnlLine: `Record` "Job Journal Line"<br> Jobno: `Code[20]`<br> TaskNo: `Code[20]`<br> JobLineType: `Option` " ",Schedule,Contract,"Both Schedule and Contract"<br> Billable: `Boolean` |
| From version | 26.0.0.0 |

### Codeunit 6086338 CEM Settlement-Post


|   |   |
| --- | --- |
| Event name | **OnBeforePostExpenseReport** |
| Event type | IntegrationEvent(IncludeSender : `TRUE`, GlobalVarAccess : `false`) |
| Parameters | `var` ExpenseReport: `Record` "CEM Expense Header"<br> `var` IsPosted: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterPostExpenseReport** |
| Event type | IntegrationEvent(IncludeSender : `TRUE`, GlobalVarAccess : `false`) |
| Parameters | `var` ExpenseReport: `Record` "CEM Expense Header" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnBeforeBalancePostGenJnlLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` GenJournalLine: `Record` "Gen. Journal Line"<br> TableID: `Integer`<br> DocumentType: `Integer`<br> DocumentNo: `Code[20]`<br> DocRefNo: `Integer` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterBalancePostGenJnlLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` GenJournalLine: `Record` "Gen. Journal Line"<br> TableID: `Integer`<br> DocumentType: `Integer`<br> DocumentNo: `Code[20]`<br> DocRefNo: `Integer` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnBeforeExpensePostGenJnlLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` GenJournalLine: `Record` "Gen. Journal Line"<br> Expense: `Record` "CEM Expense"<br> UseExpenseAllocation: `Boolean` |
| From version | 26.0.0.0 |
| Obsolete | Use OnBeforeExpensePostGenJnlLine2 |

|   |   |
| --- | --- |
| Event name | **OnBeforeExpensePostGenJnlLine2** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` GenJournalLine: `Record` "Gen. Journal Line"<br> Expense: `Record` "CEM Expense"<br> AllocationOnExpense: `Record` "CEM Expense"<br> ExpenseIsAllocated: `Boolean`<br> AllocationEntryNo: `Integer`<br> BalanceAccountType: `Option` "G/L Account",,Vendor,"Bank Account",,,Employee<br> BalanceAccountNo: `Code[20]` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterExpensePostGenJnlLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` GenJournalLine: `Record` "Gen. Journal Line"<br> Expense: `Record` "CEM Expense"<br> UseExpenseAllocation: `Boolean` |
| From version | 26.0.0.0 |
| Obsolete | Use OnAfterExpensePostGenJnlLine2 |

|   |   |
| --- | --- |
| Event name | **OnAfterTransferExpense** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Expense: `Record` "CEM Expense" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnBeforeMileagePostGenJnlLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` GenJournalLine: `Record` "Gen. Journal Line"<br> Mileage: `Record` "CEM Mileage" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterMileagePostGenJnlLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` GenJournalLine: `Record` "Gen. Journal Line"<br> Mileage: `Record` "CEM Mileage" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterTransferMileage** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Mileage: `Record` "CEM Mileage" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnBeforePerDiemPostGenJnlLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` GenJournalLine: `Record` "Gen. Journal Line"<br> PerDiem: `Record` "CEM Per Diem" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterPerDiemPostGenJnlLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` GenJournalLine: `Record` "Gen. Journal Line"<br> PerDiem: `Record` "CEM Per Diem" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterTransferPerDiem** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PerDiem: `Record` "CEM Per Diem"<br> PayTypeCode: `Code[20]`<br> PostingAmount: `Decimal` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterValidatePostBalanceAccountNo** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` GenJournalLine: `Record` "Gen. Journal Line"<br> TableID: `Integer`<br> DocType: `Integer`<br> DocNo: `Code[20]`<br> DocRefNo: `Integer` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnBeforeCreateJobJnlLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` GenJournalLine: `Record` "Gen. Journal Line"<br> Mileage: `Record` "CEM Mileage" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnBeforeMileagePostJobJnlLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` GenJournalLine: `Record` "Gen. Journal Line"<br> Mileage: `Record` "CEM Mileage" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterMileagePostJobJnlLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` GenJournalLine: `Record` "Gen. Journal Line"<br> Mileage: `Record` "CEM Mileage" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnBeforePostBusinessVendorPmtBalLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` BalGenJnlLine: `Record` "Gen. Journal Line" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnBeforeCreateGenJnlBalanceEntrySet** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PostBalanceOnNewJnlLine: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterExpensePostGenJnlLine2** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` GenJournalLine: `Record` "Gen. Journal Line"<br> Expense: `Record` "CEM Expense"<br> UseExpenseAllocation: `Boolean`<br> PreviewMode: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterPostExpenseReportOnBeforeStopPreviewAndCommit** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ExpenseReport: `Record` "CEM Expense Header"<br> PostedSettlementNo: `Code[20]` |
| From version | 26.0.0.0 |

### Codeunit 6086342 CEM Mileage Inbox-Transfer


|   |   |
| --- | --- |
| Event name | **OnBeforeInsertEMDimensions** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Mileage: `Record` "CEM Mileage" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterInsertEMDimensions** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Mileage: `Record` "CEM Mileage" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterMileageInboxTransfer** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Mileage: `Record` "CEM Mileage"<br> MileageInbox: `Record` "CEM Mileage Inbox" |
| From version | 26.0.0.0 |

### Codeunit 6086344 CEM Mileage - Check


|   |   |
| --- | --- |
| Event name | **OnBeforeCheckMileage** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Mileage: `Record` "CEM Mileage" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterCheckMileage** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Mileage: `Record` "CEM Mileage" |
| From version | 26.0.0.0 |

### Codeunit 6086345 CEM Mileage-Validate


|   |   |
| --- | --- |
| Event name | **OnBeforeMileageValidate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Rec: `Record` "CEM Mileage" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterMileageValidate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Rec: `Record` "CEM Mileage" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnBeforeSetTolerance** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Tolerance: `Decimal`<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |
| Obsolete | Moved to CEM Mileage Table |

### Codeunit 6086346 CEM Mileage-Reimburse


|   |   |
| --- | --- |
| Event name | **OnMileageReimburseOnAfterSetReimbursed** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Mileage: `Record` "CEM Mileage" |
| From version | 26.0.0.0 |

### Codeunit 6086349 CEM Settlement - Check


|   |   |
| --- | --- |
| Event name | **OnBeforeCheckSettlement** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Settlement: `Record` "CEM Expense Header" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterCheckSettlement** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Settlement: `Record` "CEM Expense Header" |
| From version | 26.0.0.0 |

### Codeunit 6086350 CEM Mileage-Post


|   |   |
| --- | --- |
| Event name | **OnBeforePostMileage** |
| Event type | IntegrationEvent(IncludeSender : `TRUE`, GlobalVarAccess : `false`) |
| Parameters | `var` Mileage: `Record` "CEM Mileage"<br> `var` IsPosted: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterPostMileage** |
| Event type | IntegrationEvent(IncludeSender : `TRUE`, GlobalVarAccess : `false`) |
| Parameters | `var` Mileage: `Record` "CEM Mileage" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterAddLineToInvoice** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchLine: `Record` "Purchase Line"<br> Mileage: `Record` "CEM Mileage" |
| From version | 26.0.0.0 |

### Codeunit 6086351 CEM Mileage-Post (Yes/No)


|   |   |
| --- | --- |
| Event name | **OnBeforeConfirmAccMissmatch** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Mileage: `Record` "CEM Mileage"<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

### Codeunit 6086356 CEM Approval Functions (WS)


|   |   |
| --- | --- |
| Event name | **OnBeforeForwardApprovalEntryWS** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ApproverId: `Code[50]`<br> DelegateToUserId: `Code[50]`<br> DelegateAction: `Integer` |
| From version | 26.0.0.0 |

### Codeunit 6086369 CEM Approvals Bridge


|   |   |
| --- | --- |
| Event name | **OnSendExpenseForApproval** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Expense: `Record` "CEM Expense" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnExpenseForceApproveApprovalRequest** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Expense: `Record` "CEM Expense" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnExpenseForceRejectApprovalRequest** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Expense: `Record` "CEM Expense" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnCancelExpenseApprovalRequest** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Expense: `Record` "CEM Expense" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnApproveAndDelegateRequested** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ApprovalEntry: `Record` "Approval Entry" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnDelegateWithoutApprovalRequested** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ApprovalEntry: `Record` "Approval Entry" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnDelegateAndSendBackRequested** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ApprovalEntry: `Record` "Approval Entry" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnSendMileageForApproval** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Mileage: `Record` "CEM Mileage" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnMileageForceApproveApprovalRequest** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Mileage: `Record` "CEM Mileage" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnMileageForceRejectApprovalRequest** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Mileage: `Record` "CEM Mileage" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnCancelMileageApprovalRequest** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Mileage: `Record` "CEM Mileage" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnSendPerDiemForApproval** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PerDiem: `Record` "CEM Per Diem" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnPerDiemForceApproveApprovalRequest** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PerDiem: `Record` "CEM Per Diem" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnPerDiemForceRejectApprovalRequest** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PerDiem: `Record` "CEM Per Diem" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnCancelPerDiemApprovalRequest** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PerDiem: `Record` "CEM Per Diem" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnSendSettlementForApproval** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ExpHeader: `Record` "CEM Expense Header" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnSettlementForceApproveApprovalRequest** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ExpHeader: `Record` "CEM Expense Header" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnSettlementeForceRejectApprovalRequest** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ExpHeader: `Record` "CEM Expense Header" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnCancelSettlementApprovalRequest** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ExpHeader: `Record` "CEM Expense Header" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnBeforeSendExpenseForApproval** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | DocumentNo: `Code[20]` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnBeforeExpenseForceApproveApprovalRequest** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | DocumentNo: `Code[20]` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnBeforeAutoApproveExpenseWithPurchContract** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Expense: `Record` "CEM Expense" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnBeforeSendExpenseHeaderForApproval** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | DocumentNo: `Code[20]` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnBeforeSettlementForceApproveApprovalRequest** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | DocumentNo: `Code[20]` |
| From version | 26.0.0.0 |

### Codeunit 6086371 CEM Workflow Response Handling


|   |   |
| --- | --- |
| Event name | **OnBeforeExecuteResponseStepInstance** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` NewWorkflowStepInstance: `Record` "Workflow Step Instance" |
| From version | 26.0.0.0 |

### Codeunit 6086373 CEM Proxy Response Handling


|   |   |
| --- | --- |
| Event name | **OnBeforeConfirmOnDeleteUserSetup** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` HideConfirmationDialog: `Boolean` |
| From version | 26.0.0.0 |

### Codeunit 6086381 CEM Settlement - Validate


|   |   |
| --- | --- |
| Event name | **OnBeforeSettlementValidate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Rec: `Record` "CEM Expense Header" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterSettlementValidate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Rec: `Record` "CEM Expense Header" |
| From version | 26.0.0.0 |

### Codeunit 6086384 CEM Settlement Inbox-Transfer


|   |   |
| --- | --- |
| Event name | **OnBeforeInsertEMDimensions** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ExpenseHeader: `Record` "CEM Expense Header" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterInsertEMDimensions** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ExpenseHeader: `Record` "CEM Expense Header" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterExpHeaderInboxTransfer** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ExpHeader: `Record` "CEM Expense Header"<br> ExpHeaderInbox: `Record` "CEM Expense Header Inbox" |
| From version | 26.0.0.0 |

### Codeunit 6086401 CEM NAV Client URL Mgt.


|   |   |
| --- | --- |
| Event name | **OnBeforeGetApprovalHyperlink** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ApprovalHyperLink: `Text[1024]`<br> `var` IsHandled: `Boolean` |
| From version | 26.0.0.0 |

### Codeunit 6086409 CEM Digital Voucher Mgt.


|   |   |
| --- | --- |
| Event name | **OnBeforeCreateDigitalVoucher** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | DestinationRecID: `RecordID`<br> DocumentRecID: `RecordID`<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnCopyDocumentAsDigitalVoucherPostedDocument** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | RecRef: `RecordRef`<br> Attachment: `Record` "CEM Attachment"<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

### Codeunit 6086505 CEM Module License


|   |   |
| --- | --- |
| Event name | **OnGetActivationState** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ModuleCode: `Code[20]`<br> `var` Activated: `Boolean`<br> `var` TestValue: `Text` |
| From version | 26.0.0.0 |

### Codeunit 6086513 CEM Per Diem Calc. Engine


|   |   |
| --- | --- |
| Event name | **OnBeforeFindRateAndUpdateAmtOnDetail** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PerDiemDetails: `Record` "CEM Per Diem Detail"<br> `var` IsHandled: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterFindRateAndUpdateAmtOnDetail** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PerDiemDetails: `Record` "CEM Per Diem Detail" |
| From version | 26.0.0.0 |

### Codeunit 6086515 CEM Settlement Online Mgt.


|   |   |
| --- | --- |
| Event name | **OnAfterReadSettlementDims** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ExpHeaderNode: `Codeunit` "CSC XML Node"<br> Pos: `Integer`<br> FieldNameCode: `Code[20]`<br> FieldValue: `Text[1024]`<br> `var` ExpHeaderInbox: `Record` "CEM Expense Header Inbox"<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

### Codeunit 6086516 CEM Expense Online Mgt.


|   |   |
| --- | --- |
| Event name | **OnAfterReadExpDimensions** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` XMLNodeList: `Codeunit` "CSC XML NodeList"<br> Pos: `Integer`<br> FieldNameCode: `Code[20]`<br> FieldValue: `Text[1024]`<br> `var` ExpenseInbox: `Record` "CEM Expense Inbox"<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterReadExpAllocDimensions** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` XMLNodeList: `Codeunit` "CSC XML NodeList"<br> Pos: `Integer`<br> FieldNameCode: `Code[20]`<br> FieldValue: `Text[1024]`<br> `var` ExpAllocInbox: `Record` "CEM Expense Allocation Inbox"<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterAddExpenseDimensionsToXmlNode** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Expense: `Record` "CEM Expense"<br> `var` DimsNode: `Codeunit` "CSC XML Node"<br> Handled: `Boolean` |
| From version | 26.0.0.0 |

### Codeunit 6086517 CEM Mileage Online Mgt.


|   |   |
| --- | --- |
| Event name | **OnAfterReadMilDimensions** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` XMLNodeList: `Codeunit` "CSC XML NodeList"<br> Pos: `Integer`<br> FieldNameCode: `Code[20]`<br> FieldValue: `Text[1024]`<br> `var` MileageInbox: `Record` "CEM Mileage Inbox"<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

### Codeunit 6086518 CEM Per Diem Online Mgt.


|   |   |
| --- | --- |
| Event name | **OnAfterReadPerDiemDimensions** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` XMLNodeList: `Codeunit` "CSC XML NodeList"<br> Pos: `Integer`<br> FieldNameCode: `Code[20]`<br> FieldValue: `Text[1024]`<br> `var` PerDiemInbox: `Record` "CEM Per Diem Inbox"<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

### Codeunit 6086525 CEM Per Diem Inb.-Transfer


|   |   |
| --- | --- |
| Event name | **OnBeforeInsertEMDimensions** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PerDiem: `Record` "CEM Per Diem" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterInsertEMDimensions** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PerDiem: `Record` "CEM Per Diem" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterPerDiemInboxTransfer** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PerDiem: `Record` "CEM Per Diem"<br> PerDiemInbox: `Record` "CEM Per Diem Inbox" |
| From version | 26.0.0.0 |

### Codeunit 6086526 CEM Per Diem-Validate


|   |   |
| --- | --- |
| Event name | **OnBeforePerDiemValidate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Rec: `Record` "CEM Per Diem" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterPerDiemValidate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Rec: `Record` "CEM Per Diem" |
| From version | 26.0.0.0 |

### Codeunit 6086530 CEM Per Diem-Post


|   |   |
| --- | --- |
| Event name | **OnBeforePostPerDiem** |
| Event type | IntegrationEvent(IncludeSender : `TRUE`, GlobalVarAccess : `false`) |
| Parameters | `var` PerDiem: `Record` "CEM Per Diem"<br> `var` IsPosted: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterPostPerDiem** |
| Event type | IntegrationEvent(IncludeSender : `TRUE`, GlobalVarAccess : `false`) |
| Parameters | `var` PerDiem: `Record` "CEM Per Diem" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterAddLineToInvoice** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PurchLine: `Record` "Purchase Line"<br> PerDiem: `Record` "CEM Per Diem" |
| From version | 26.0.0.0 |

### Codeunit 6086532 CEM Per Diem - Check


|   |   |
| --- | --- |
| Event name | **OnBeforePerDiemCheck** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PerDiem: `Record` "CEM Per Diem" |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterPerDiemCheck** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PerDiem: `Record` "CEM Per Diem" |
| From version | 26.0.0.0 |

### Codeunit 6086535 CEM Navigate Per Diem - Find


|   |   |
| --- | --- |
| Event name | **OnBeforeNavigatePerDiem** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | PerDiem: `Record` "CEM Per Diem"<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

### Codeunit 6086537 CEM Field Type Code Mgt.


|   |   |
| --- | --- |
| Event name | **OnAfterGetExpSystemFieldNo** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | FieldCode: `Code[20]`<br> `var` FieldNo: `Integer` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterGetExpenseFieldTypeCode** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | FieldNo: `Integer`<br> `var` FieldCode: `Code[20]` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterGetExpAllocSystFieldNo** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | FieldCode: `Code[20]`<br> `var` FieldNo: `Integer` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterGetMilSystemFieldNo** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | FieldCode: `Code[20]`<br> `var` FieldNo: `Integer` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterGetMileageFieldTypeCode** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | FieldNo: `Integer`<br> `var` FieldCode: `Code[20]` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterGetPerDiemSystFieldNo** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | FieldCode: `Code[20]`<br> `var` FieldNo: `Integer` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterGetPerDiemFieldTypeCode** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | FieldNo: `Integer`<br> `var` FieldCode: `Code[20]` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterGetDetailSystemFieldNo** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | FieldCode: `Code[20]`<br> `var` FieldNo: `Integer` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterGetPerDiemDetailFieldTypeCode** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | FieldNo: `Integer`<br> `var` FieldCode: `Code[20]` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterGetSettlSystemFieldNo** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | FieldCode: `Code[20]`<br> `var` FieldNo: `Integer` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterGetSettlementFieldTypeCode** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | FieldNo: `Integer`<br> `var` FieldCode: `Code[20]` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterFieldIsActivatedBySetup** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | FieldTypeCode: `Code[20]`<br> `var` FieldIsActivatedBySetup: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterSetDefaultSettings** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters |  |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterCreateFieldTableFilter** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` FieldType: `Record` "CEM Field Type" |
| From version | 26.0.0.0 |

### Codeunit 6086548 CEM Sales Tax Interface


|   |   |
| --- | --- |
| Event name | **OnIsEMCanadaAppInstalled** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` CAAppIsInstalled: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnShouldHandleCASalesTax** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ShouldHandle: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnShouldHandleCASalesTaxOnExp** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Expense: `Record` "CEM Expense"<br> `var` ShouldHandle: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnIsAllocationSalesTaxLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ExpenseAllocation: `Record` "CEM Expense Allocation"<br> `var` IsSalesTaxLine: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnHasCASalesTax** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | GenJnlLine: `Record` "Gen. Journal Line"<br> Expense: `Record` "CEM Expense"<br> `var` CASalesTaxExists: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnSplitJnlLineIntoTaxLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` GenJnlPostLine: `Codeunit` "Gen. Jnl.-Post Line"<br> Expense: `Record` "CEM Expense"<br> GenJnlLine: `Record` "Gen. Journal Line"<br> AllocationEntryNo: `Integer`<br> PreviewMode: `Boolean` |
| From version | 26.0.0.0 |

### Codeunit 6086557 CEM Doc. File Events


|   |   |
| --- | --- |
| Event name | **GetAttachmentFile** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` EMAttachment: `Record` "CEM Attachment"<br> `var` TempFile: `Record` "CDC Temp File" temporary<br> `var` Success: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **GetPage** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` AttachmentPages: `Record` "CEM Attachment Pages"<br> `var` TempFile: `Record` "CDC Temp File" temporary<br> `var` Success: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **GetPDFFile** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` EMAttachment: `Record` "CEM Attachment"<br> `var` TempFile: `Record` "CDC Temp File" temporary<br> `var` Success: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **SetAttachment** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` EMAttachment: `Record` "CEM Attachment"<br> `var` TempFile: `Record` "CDC Temp File" temporary<br> `var` Success: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **SetPage** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` AttachmentPages: `Record` "CEM Attachment Pages"<br> `var` TempFile: `Record` "CDC Temp File" temporary<br> `var` Success: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **SetPDF** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` EMAttachment: `Record` "CEM Attachment"<br> `var` TempFile: `Record` "CDC Temp File" temporary<br> `var` Success: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **HasAttachment** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` EMAttachment: `Record` "CEM Attachment"<br> `var` HasAttachment: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **HasPage** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` AttachmentPages: `Record` "CEM Attachment Pages"<br> `var` HasPage: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **HasPDF** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` EMAttachment: `Record` "CEM Attachment"<br> `var` HasSignedPDF: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **ClearAttachment** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` EMAttachment: `Record` "CEM Attachment"<br> `var` Success: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **ClearPage** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` AttachmentPages: `Record` "CEM Attachment Pages"<br> `var` Success: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **ClearPDF** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` EMAttachment: `Record` "CEM Attachment"<br> `var` Success: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **GetInboxAttachmentFile** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` EMAttachmentInbox: `Record` "CEM Attachment Inbox"<br> `var` TempFile: `Record` "CDC Temp File" temporary<br> `var` Success: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **GetInboxPage** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` AttachmentPagesInbox: `Record` "CEM Attachment Pages Inbox"<br> `var` TempFile: `Record` "CDC Temp File" temporary<br> `var` Success: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **GetInboxPDFFile** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` EMAttachmentInbox: `Record` "CEM Attachment Inbox"<br> `var` TempFile: `Record` "CDC Temp File" temporary<br> `var` Success: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **SetInboxAttachment** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` EMAttachmentInbox: `Record` "CEM Attachment Inbox"<br> `var` TempFile: `Record` "CDC Temp File" temporary<br> `var` Success: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **SetInboxPage** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` AttachmentPagesInbox: `Record` "CEM Attachment Pages Inbox"<br> `var` TempFile: `Record` "CDC Temp File" temporary<br> `var` Success: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **SetInboxPDF** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` EMAttachmentInbox: `Record` "CEM Attachment Inbox"<br> `var` TempFile: `Record` "CDC Temp File" temporary<br> `var` Success: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **HasInboxAttachment** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` EMAttachmentInbox: `Record` "CEM Attachment Inbox"<br> `var` HasAttachment: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **HasInboxPage** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` AttachmentPagesInbox: `Record` "CEM Attachment Pages Inbox"<br> `var` HasPage: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **HasInboxPDF** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` EMAttachmentInbox: `Record` "CEM Attachment Inbox"<br> `var` HasPDF: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **ClearInboxAttachment** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` EMAttachmentInbox: `Record` "CEM Attachment Inbox"<br> `var` Success: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **ClearInboxPage** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` AttachmentPagesInbox: `Record` "CEM Attachment Pages Inbox"<br> `var` Success: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **ClearInboxPDF** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` EMAttachmentInbox: `Record` "CEM Attachment Inbox"<br> `var` Success: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

### Codeunit 6086559 CEM Transaction Import CSV


|   |   |
| --- | --- |
| Event name | **OnBeforeInitGlobalVars** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters |  |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterInitGlobalVars** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters |  |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnBeforeParseValue** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | FieldMapping: `Record` "CEM Transaction Field Mapping"<br> FieldType: `FieldRef`<br> `var` ValueAsDataType: `Variant`<br> `var` ValueAsText: `Text[250]`<br> `var` Handled: `Boolean` |
| From version | 26.0.0.0 |

### Codeunit 6086565 CEM Export Expense Reimb.


|   |   |
| --- | --- |
| Event name | **OnAfterCreateRowWithColumnsCaptions** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` CurrentTempExcelBuffer: `Record` "Excel Buffer" temporary<br> `var` LastColumnNo: `Integer` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterCreateDataSheetLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` CurrentTempExcelBuffer: `Record` "Excel Buffer" temporary<br> ContiniaUserSetup: `Record` "CDC Continia User Setup"<br> `var` LastColumnNo: `Integer`<br> UserFilter: `Text[1024]`<br> QtyType: `Option Quantity,Amount`<br> PostingType: `Option` "Awaiting Posting","Ready to Reimburse","Posted and Reimbursed",Everything<br> PeriodFilter: `Text[250]` |
| From version | 26.0.0.0 |

### Codeunit 6086566 CEM Export Mileage Reimb.


|   |   |
| --- | --- |
| Event name | **OnAfterCreateRowWithColumnsCaptions** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` CurrentTempExcelBuffer: `Record` "Excel Buffer" temporary<br> `var` LastColumnNo: `Integer` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterCreateDataSheetLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` CurrentTempExcelBuffer: `Record` "Excel Buffer" temporary<br> ContiniaUserSetup: `Record` "CDC Continia User Setup"<br> `var` LastColumnNo: `Integer`<br> UserFilter: `Text[1024]`<br> VehicleFilter: `Text[250]`<br> QtyType: `Option Quantity,Amount`<br> PostingType: `Option` "Awaiting Posting","Ready to Reimburse","Posted and Reimbursed",Everything<br> PeriodFilter: `Text[250]` |
| From version | 26.0.0.0 |

### Codeunit 6086567 CEM Export Per Diem Reimb.


|   |   |
| --- | --- |
| Event name | **OnAfterCreateRowWithColumnsCaptions** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` CurrentTempExcelBuffer: `Record` "Excel Buffer" temporary<br> IncludeTaxable: `Boolean`<br> `var` LastColumnNo: `Integer` |
| From version | 26.0.0.0 |

|   |   |
| --- | --- |
| Event name | **OnAfterCreateDataSheetLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` CurrentTempExcelBuffer: `Record` "Excel Buffer" temporary<br> ContiniaUserSetup: `Record` "CDC Continia User Setup"<br> `var` LastColumnNo: `Integer`<br> UserFilter: `Text[1024]`<br> QtyType: `Option Quantity,Amount`<br> PostingType: `Option` "Awaiting Posting","Ready to Reimburse","Posted and Reimbursed",Everything<br> PeriodFilter: `Text[250]` |
| From version | 26.0.0.0 |



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
