---
title: Event Publishers for Continia Delivery Network 2021 R2 (2.00)
date: 05-10-2022
description:
id: DO-13
lang: en
---

# Event Publishers for Continia Delivery Network 2021 R2 (2.00)

The following event publishers are included in Continia Delivery Network 2021 R2 (2.00):

### Codeunit 6086225 CTS-CDN Document Output Mgt.


|   |   |
| --- | --- |
| Event name | **OnBeforePrePostValidate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesHeader: `Record` "Sales Header"<br> EDocSendCode: `Code[20]`<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePrePostValidateServ** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceHeader: `Record` "Service Header"<br> EDocSendCode: `Code[20]`<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |

### Codeunit 6086232 CTS-CDN PEPPOL Mgt.


|   |   |
| --- | --- |
| Event name | **OnBeforeGetIso4217CurrencyCode** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | CurrencyCode: `Code[10]`<br> `var` Handled: `Boolean`<br> `var` ReturnValue: `Code[3]` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetUNECERec20UOMCode** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | UOMCode: `Code[10]`<br> `var` Handled: `Boolean`<br> `var` ReturnValue: `Code[10]` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeAddPeppolCountrySpecifics** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | VATRegNo: `Text[20]`<br> CountryCode: `Code[10]`<br> Handled: `Boolean`<br> `var` ReturnValue: `Text[1024]` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetNamespaces** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Namespaces: `Record` "CTS-CDN XML Export Namespace" temporary<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSetNamespaces** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Namespaces: `Record` "CTS-CDN XML Export Namespace" temporary |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnGetTotalsOnBeforeInsertVATAmtLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesLine: `Record` "Sales Line"<br> `var` VATAmtLine: `Record` "VAT Amount Line" |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnCreateItemAttributes** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ItemNode: `Codeunit` "CSC XML Node"<br> ItemNo: `Code[20]`<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeTranslateForPartyID** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | VatRegNo: `Text[30]`<br> CountryCode: `Code[10]`<br> `var` ReturnValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeTranslateForTaxCompany** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | VatRegNo: `Text[30]`<br> CountryCode: `Code[10]`<br> `var` ReturnValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeTranslateForLegalCompany** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | VatRegNo: `Text[30]`<br> CountryCode: `Code[10]`<br> `var` ReturnValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |

### Codeunit 6086233 CTS-CDN ISO Code Mgt.


|   |   |
| --- | --- |
| Event name | **OnBeforeGetCountryCodeISO31661** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | CountryCode: `Code[10]`<br> `var` Handled: `Boolean`<br> `var` ReturnValue: `Code[3]` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetCurrencyCodeISO4217** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | CurrencyCode: `Code[10]`<br> `var` Handled: `Boolean`<br> `var` ReturnValue: `Code[3]` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetUOMCodeUNECERec20** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | UOMCode: `Code[10]`<br> `var` Handled: `Boolean`<br> `var` ReturnValue: `Code[10]` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeAddPeppolCountrySpecifics** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | VATRegNo: `Text[20]`<br> CountryCode: `Code[10]`<br> Handled: `Boolean`<br> `var` ReturnValue: `Text[1024]` |
| From version | 2.0.0.0 |

### Codeunit 6086234 CTS-CDN Export Mgt.


|   |   |
| --- | --- |
| Event name | **OnAfterGetReceiverInfo** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | FromRecord: `Variant`<br> CustomerNo: `Code[20]`<br> ForNetworkProfile: `Record` "CTS-CDN Network Profile"<br> `var` ReceiverIDType: `Record` "CTS-CDN Participation ID Type"<br> `var` ReceiverIDValue: `Text[250]` |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSkipDocumentLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | FromCodeunit: `Integer`<br> DocLineVariant: `Variant`<br> `var` SkipLine: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSkipDocumentLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | FromCodeunit: `Integer`<br> DocLineVariant: `Variant`<br> `var` SkipLine: `Boolean` |
| From version | 2.3.0.0 |

### Codeunit 6086235 CTS-CDN Localization Mgt.


|   |   |
| --- | --- |
| Event name | **OnBeforeGetCompanyID** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` CompanyIdentifier: `Text[250]`<br> `var` Handled: `Boolean` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetCustomerID** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Customer: `Record Customer`<br> `var` CustomerIdentifier: `Text[250]`<br> `var` Handled: `Boolean` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterFindIDFieldCustomer** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Customer: `Record Customer`<br> `var` IdentifierFieldNo: `Integer` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterFindIDFieldCompany** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` IdentifierFiledNo: `Integer` |
| From version | 2.3.0.0 |

### Codeunit 6086240 CTS-CDN PEPPOL BIS3 Inv.


|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` LineNodeList: `Codeunit` "CSC XML NodeList" |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePaymentMeans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentType: `Option Bank,KID,FIK`<br> `var` PaymentID: `Integer`<br> `var` AccountID: `Code[50]`<br> `var` FinancialInstitutionBranchID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |
| Obsolete | Replaced by OnBeforeCreatePaymentMeans |



|   |   |
| --- | --- |
| Event name | **OnBeforePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentTermsText: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeaderDiscounts** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateTaxTotal** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLegalMonetary** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceLine: `Record` "Sales Invoice Line"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceLine: `Record` "Sales Invoice Line"<br> `var` InvoiceLineNode: `Codeunit` "CSC XML Node" |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` TempBlob: `Record` "CSC Temp Blob" temporary<br> `var` Filename: `Text[1024]`<br> `var` ID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreatePaymentMeans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentType: `Option Bank,KID,FIK`<br> `var` PaymentID: `Text[1024]`<br> `var` AccountID: `Code[50]`<br> `var` FinancialInstitutionBranchID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetBuyerReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` BuyerRefValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetOrderReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` OrderRefID: `Code[50]`<br> `var` OrderRefSalesOrderID: `Code[50]`<br> `var` Handled: `Boolean` |
| From version | 2.2.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateBuyerReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` BuyerRefValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.2.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetInvPeriodHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` InvoicePeriodStartDate: `Date`<br> `var` InvoicePeriodEndDate: `Date`<br> `var` InvoicePeriodDescriptionCode: `Code[50]` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetInvPeriodLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceLine: `Record` "Sales Invoice Line"<br> `var` InvoicePeriodStartDate: `Date`<br> `var` InvoicePeriodEndDate: `Date` |
| From version | 2.3.0.0 |

### Codeunit 6086241 CTS-CDN PEPPOL BIS3 Cr.M.


|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` LineNodeList: `Codeunit` "CSC XML NodeList" |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePaymentMeans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` PaymentType: `Option Bank,KID,FIK`<br> `var` PaymentID: `Integer`<br> `var` AccountID: `Code[50]`<br> `var` FinancialInstitutionBranchID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |
| Obsolete | Replaced by OnBeforeCreatePaymentMeans |



|   |   |
| --- | --- |
| Event name | **OnBeforePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentTermsText: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeaderDiscounts** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateTaxTotal** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLegalMonetary** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoLine: `Record` "Sales Cr.Memo Line"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoLine: `Record` "Sales Cr.Memo Line"<br> `var` InvoiceLineNode: `Codeunit` "CSC XML Node" |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` TempBlob: `Record` "CSC Temp Blob" temporary<br> `var` Filename: `Text[1024]`<br> `var` ID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreatePaymentMeans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentType: `Option Bank,KID,FIK`<br> `var` PaymentID: `Text[1024]`<br> `var` AccountID: `Code[50]`<br> `var` FinancialInstitutionBranchID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetBuyerReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` BuyerRefValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetOrderReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` OrderRefID: `Code[50]`<br> `var` OrderRefSalesOrderID: `Code[50]`<br> `var` Handled: `Boolean` |
| From version | 2.2.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateBuyerReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` BuyerRefValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.2.0.0 |

### Codeunit 6086242 CTS-CDN PEPPOL BIS3 Sv. Inv.


|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` LineNodeList: `Codeunit` "CSC XML NodeList" |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePaymentMeans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentType: `Option Bank,KID,FIK`<br> `var` PaymentID: `Integer`<br> `var` AccountID: `Code[50]`<br> `var` FinancialInstitutionBranchID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |
| Obsolete | Replaced by OnBeforeCreatePaymentMeans |



|   |   |
| --- | --- |
| Event name | **OnBeforePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentTermsText: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeaderDiscounts** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateTaxTotal** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLegalMonetary** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceLine: `Record` "Service Invoice Line"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceLine: `Record` "Service Invoice Line"<br> `var` InvoiceLineNode: `Codeunit` "CSC XML Node" |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` TempBlob: `Record` "CSC Temp Blob" temporary<br> `var` Filename: `Text[1024]`<br> `var` ID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreatePaymentMeans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentType: `Option Bank,KID,FIK`<br> `var` PaymentID: `Text[1024]`<br> `var` AccountID: `Code[50]`<br> `var` FinancialInstitutionBranchID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetBuyerReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` BuyerRefValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetOrderReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` OrderRefID: `Code[50]`<br> `var` OrderRefSalesOrderID: `Code[50]`<br> `var` Handled: `Boolean` |
| From version | 2.2.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateBuyerReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` BuyerRefValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.2.0.0 |

### Codeunit 6086243 CTS-CDN XRechnung 2 Inv.


|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` LineNodeList: `Codeunit` "CSC XML NodeList" |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePaymentMeans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentType: `Option Bank,KID,FIK`<br> `var` PaymentID: `Integer`<br> `var` AccountID: `Code[50]`<br> `var` FinancialInstitutionBranchID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |
| Obsolete | Replaced by OnBeforeCreatePaymentMeans |



|   |   |
| --- | --- |
| Event name | **OnBeforePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentTermsText: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeaderDiscounts** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateTaxTotal** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLegalMonetary** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceLine: `Record` "Sales Invoice Line"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceLine: `Record` "Sales Invoice Line"<br> `var` InvoiceLineNode: `Codeunit` "CSC XML Node" |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetBuyerReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` BuyerRefValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` TempBlob: `Record` "CSC Temp Blob" temporary<br> `var` Filename: `Text[1024]`<br> `var` ID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreatePaymentMeans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentType: `Option Bank,KID,FIK`<br> `var` PaymentID: `Text[1024]`<br> `var` AccountID: `Code[50]`<br> `var` FinancialInstitutionBranchID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetOrderReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` OrderRefID: `Code[50]`<br> `var` OrderRefSalesOrderID: `Code[50]`<br> `var` Handled: `Boolean` |
| From version | 2.2.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateBuyerReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` BuyerRefValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.2.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetInvPeriodHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` InvoicePeriodStartDate: `Date`<br> `var` InvoicePeriodEndDate: `Date`<br> `var` InvoicePeriodDescriptionCode: `Code[50]` |
| From version | 2.4.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetInvPeriodLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceLine: `Record` "Sales Invoice Line"<br> `var` InvoicePeriodStartDate: `Date`<br> `var` InvoicePeriodEndDate: `Date` |
| From version | 2.4.0.0 |

### Codeunit 6086244 CTS-CDN XRechnung 2 Cr.Memo


|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` LineNodeList: `Codeunit` "CSC XML NodeList" |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePaymentMeans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` PaymentType: `Option Bank,KID,FIK`<br> `var` PaymentID: `Integer`<br> `var` AccountID: `Code[50]`<br> `var` FinancialInstitutionBranchID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |
| Obsolete | Replaced by OnBeforeCreatePaymentMeans |



|   |   |
| --- | --- |
| Event name | **OnBeforePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentTermsText: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeaderDiscounts** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateTaxTotal** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLegalMonetary** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoLine: `Record` "Sales Cr.Memo Line"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoLine: `Record` "Sales Cr.Memo Line"<br> `var` InvoiceLineNode: `Codeunit` "CSC XML Node" |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetBuyerReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` BuyerRefValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` TempBlob: `Record` "CSC Temp Blob" temporary<br> `var` Filename: `Text[1024]`<br> `var` ID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreatePaymentMeans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentType: `Option Bank,KID,FIK`<br> `var` PaymentID: `Text[1024]`<br> `var` AccountID: `Code[50]`<br> `var` FinancialInstitutionBranchID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetOrderReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` OrderRefID: `Code[50]`<br> `var` OrderRefSalesOrderID: `Code[50]`<br> `var` Handled: `Boolean` |
| From version | 2.2.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateBuyerReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` BuyerRefValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.2.0.0 |

### Codeunit 6086245 CTS-CDN XRechnung 2 Sv. Inv.


|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` LineNodeList: `Codeunit` "CSC XML NodeList" |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePaymentMeans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentType: `Option Bank,KID,FIK`<br> `var` PaymentID: `Integer`<br> `var` AccountID: `Code[50]`<br> `var` FinancialInstitutionBranchID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentTermsText: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeaderDiscounts** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateTaxTotal** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLegalMonetary** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceLine: `Record` "Service Invoice Line"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceLine: `Record` "Service Invoice Line"<br> `var` InvoiceLineNode: `Codeunit` "CSC XML Node" |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetBuyerReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` BuyerRefValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` TempBlob: `Record` "CSC Temp Blob" temporary<br> `var` Filename: `Text[1024]`<br> `var` ID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.2.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetOrderReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` OrderRefID: `Code[50]`<br> `var` OrderRefSalesOrderID: `Code[50]`<br> `var` Handled: `Boolean` |
| From version | 2.2.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateBuyerReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` BuyerRefValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.2.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreatePaymentMeans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentType: `Option Bank,KID,FIK`<br> `var` PaymentID: `Text[1024]`<br> `var` AccountID: `Code[50]`<br> `var` FinancialInstitutionBranchID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.4.0.0 |

### Codeunit 6086246 CTS-CDN XRechnung 2 Sv.Cr.Memo


|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` LineNodeList: `Codeunit` "CSC XML NodeList" |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePaymentMeans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` PaymentType: `Option Bank,KID,FIK`<br> `var` PaymentID: `Integer`<br> `var` AccountID: `Code[50]`<br> `var` FinancialInstitutionBranchID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentTermsText: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeaderDiscounts** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateTaxTotal** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLegalMonetary** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoLine: `Record` "Service Cr.Memo Line"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoLine: `Record` "Service Cr.Memo Line"<br> `var` InvoiceLineNode: `Codeunit` "CSC XML Node" |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetBuyerReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` BuyerRefValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` TempBlob: `Record` "CSC Temp Blob" temporary<br> `var` Filename: `Text[1024]`<br> `var` ID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.2.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetOrderReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` OrderRefID: `Code[50]`<br> `var` OrderRefSalesOrderID: `Code[50]`<br> `var` Handled: `Boolean` |
| From version | 2.2.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateBuyerReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` BuyerRefValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.2.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreatePaymentMeans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentType: `Option Bank,KID,FIK`<br> `var` PaymentID: `Text[1024]`<br> `var` AccountID: `Code[50]`<br> `var` FinancialInstitutionBranchID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.4.0.0 |

### Codeunit 6086247 CTS-CDN PEPPOL BIS3 Sv. Cr.M.


|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` LineNodeList: `Codeunit` "CSC XML NodeList" |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePaymentMeans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` PaymentType: `Option Bank,KID,FIK`<br> `var` PaymentID: `Integer`<br> `var` AccountID: `Code[50]`<br> `var` FinancialInstitutionBranchID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |
| Obsolete | Replaced by OnBeforeCreatePaymentMeans |



|   |   |
| --- | --- |
| Event name | **OnBeforePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentTermsText: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeaderDiscounts** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateTaxTotal** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLegalMonetary** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoLine: `Record` "Service Cr.Memo Line"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoLine: `Record` "Service Cr.Memo Line"<br> `var` InvoiceLineNode: `Codeunit` "CSC XML Node" |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` TempBlob: `Record` "CSC Temp Blob" temporary<br> `var` Filename: `Text[1024]`<br> `var` ID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreatePaymentMeans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentType: `Option Bank,KID,FIK`<br> `var` PaymentID: `Text[1024]`<br> `var` AccountID: `Code[50]`<br> `var` FinancialInstitutionBranchID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetBuyerReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` BuyerRefValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetOrderReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` OrderRefID: `Code[50]`<br> `var` OrderRefSalesOrderID: `Code[50]`<br> `var` Handled: `Boolean` |
| From version | 2.2.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateBuyerReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` BuyerRefValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.2.0.0 |

### Codeunit 6086251 CTS-CDN PEPPOL Chk. Sales Inv.


|   |   |
| --- | --- |
| Event name | **OnAfterValidate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header" |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |

### Codeunit 6086252 CTS-CDN PEPPOL Chk. Sales Cr.M


|   |   |
| --- | --- |
| Event name | **OnAfterValidate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header" |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |

### Codeunit 6086253 CTS-CDN XRech2 Chk. Sales Hdr.


|   |   |
| --- | --- |
| Event name | **OnAfterCheck** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesHeader: `Record` "Sales Header" |
| From version | 2.0.0.0 |

### Codeunit 6086254 CTS-CDN XRech2 Chk. Sales Inv.


|   |   |
| --- | --- |
| Event name | **OnAfterCheck** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header" |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |

### Codeunit 6086255 CTS-CDN XRech2 Chk. Sales Cr.M


|   |   |
| --- | --- |
| Event name | **OnAfterCheck** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header" |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |

### Codeunit 6086258 CTS-CDN XRech2 Chk. Sv. Hdr.


|   |   |
| --- | --- |
| Event name | **OnAfterCheck** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceHeader: `Record` "Service Header" |
| From version | 2.0.0.0 |

### Codeunit 6086259 CTS-CDN XRech2 Chk. Sv. Inv.


|   |   |
| --- | --- |
| Event name | **OnAfterCheck** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header" |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |

### Codeunit 6086260 CTS-CDN XRech2 Chk. Sv. Cr.M


|   |   |
| --- | --- |
| Event name | **OnAfterCheck** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Service Cr.Memo Header" |
| From version | 2.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |

### Codeunit 6086267 CTS-CDN PEPPOL Chk. Serv. Inv.


|   |   |
| --- | --- |
| Event name | **OnAfterValidate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header" |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |

### Codeunit 6086268 CTS-CDN PEPPOL Chk. Serv. Cr.M


|   |   |
| --- | --- |
| Event name | **OnAfterValidate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header" |
| From version | 2.1.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 2.1.0.0 |

### Codeunit 6086270 CTS-CDN OIOUBL Mgt.


|   |   |
| --- | --- |
| Event name | **OnGetTotalsOnBeforeInsertVATAmtLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesLine: `Record` "Sales Line"<br> `var` VATAmtLine: `Record` "VAT Amount Line" |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetNamespaces** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Namespaces: `Record` "CTS-CDN XML Export Namespace" temporary<br> `var` Handled: `Boolean` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSetNamespaces** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Namespaces: `Record` "CTS-CDN XML Export Namespace" temporary |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeTranslateForPartyID** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | VatRegNo: `Text[30]`<br> CountryCode: `Code[10]`<br> `var` ReturnValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeTranslateForTaxCompany** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | VatRegNo: `Text[30]`<br> CountryCode: `Code[10]`<br> `var` ReturnValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeTranslateForLegalCompany** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | VatRegNo: `Text[30]`<br> CountryCode: `Code[10]`<br> `var` ReturnValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnCreateItemAttributes** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ItemNode: `Codeunit` "CSC XML Node"<br> ItemNo: `Code[20]`<br> `var` Handled: `Boolean` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeAddPeppolCountrySpecifics** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | VATRegNo: `Text[20]`<br> CountryCode: `Code[10]`<br> `var` Handled: `Boolean`<br> `var` ReturnValue: `Text[1024]` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSupplierPartyPostalAddress** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | CompInfo: `Record` "Company Information"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Party: `Codeunit` "CSC XML Node"<br> `var` AddressFormatCode: `Text[250]`<br> `var` ListId: `Text[250]`<br> `var` ListAgencyID: `Text[250]`<br> `var` PostalAddressHandled: `Boolean` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCustomerPartyPostalAddress** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Customer: `Record Customer`<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Party: `Codeunit` "CSC XML Node"<br> `var` AddressFormatCode: `Text[250]`<br> `var` ListId: `Text[250]`<br> `var` ListAgencyID: `Text[250]`<br> `var` PostalAddressHandled: `Boolean` |
| From version | 2.3.0.0 |

### Codeunit 6086271 CTS-CDN OIOUBL Export Inv.


|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` LineNodeList: `Codeunit` "CSC XML NodeList" |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` TempBlob: `Record` "CSC Temp Blob" temporary<br> `var` Filename: `Text[1024]`<br> `var` ID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePaymentMeans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentType: `Option Bank,KID,FIK`<br> `var` PaymentID: `Text[1024]`<br> `var` AccountID: `Code[50]`<br> `var` FinancialInstitutionBranchID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentTermsText: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeaderDiscounts** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateTaxTotal** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLegalMonetary** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetOrderReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` OrderRefID: `Code[50]`<br> `var` OrderRefSalesOrderID: `Code[50]`<br> `var` Handled: `Boolean` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSetOrderReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceLine: `Record` "Sales Invoice Line"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceLine: `Record` "Sales Invoice Line"<br> `var` InvoiceLineNode: `Codeunit` "CSC XML Node" |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeaderNotes** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> XMLNode: `Codeunit` "CSC XML Node"<br> `var` HeaderNotesHandled: `Boolean` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetInvoiceLineDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` InvoiceLine: `Codeunit` "CSC XML Node"<br> SalesInvoiceLine: `Record` "Sales Invoice Line"<br> `var` DeliveryQuantity: `Decimal`<br> `var` DeliveryMinQuantity: `Decimal`<br> `var` DeliveryMaxQuantity: `Decimal`<br> `var` DeliveryActualDeliveryDate: `Date`<br> `var` DeliveryActualDeliveryTime: `Time`<br> `var` DeliveryTrackingID: `Text[250]`<br> `var` DeliveryHandled: `Boolean` |
| From version | 2.4.0.0 |

### Codeunit 6086272 CTS-CDN OIOUBL Export Cr.


|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` LineNodeList: `Codeunit` "CSC XML NodeList" |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` TempBlob: `Record` "CSC Temp Blob" temporary<br> `var` Filename: `Text[1024]`<br> `var` ID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePaymentMeans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentType: `Option Bank,KID,FIK`<br> `var` PaymentID: `Text[1024]`<br> `var` AccountID: `Code[50]`<br> `var` FinancialInstitutionBranchID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentTermsText: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeaderDiscounts** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateTaxTotal** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLegalMonetary** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetOrderReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` OrderRefID: `Code[50]`<br> `var` OrderRefSalesOrderID: `Code[50]`<br> `var` Handled: `Boolean` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSetOrderReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoLine: `Record` "Sales Cr.Memo Line"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoLine: `Record` "Sales Cr.Memo Line"<br> `var` InvoiceLineNode: `Codeunit` "CSC XML Node" |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeaderNotes** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> XMLNode: `Codeunit` "CSC XML Node"<br> `var` HeaderNotesHandled: `Boolean` |
| From version | 2.3.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetCreditMemoLineDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` InvoiceLine: `Codeunit` "CSC XML Node"<br> SalesCrMemoLine: `Record` "Sales Cr.Memo Line"<br> `var` DeliveryQuantity: `Decimal`<br> `var` DeliveryMinQuantity: `Decimal`<br> `var` DeliveryMaxQuantity: `Decimal`<br> `var` DeliveryActualDeliveryDate: `Date`<br> `var` DeliveryActualDeliveryTime: `Time`<br> `var` DeliveryTrackingID: `Text[250]`<br> `var` DeliveryHandled: `Boolean` |
| From version | 2.4.0.0 |



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
