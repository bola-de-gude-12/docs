---
title: Event Publishers for Continia Delivery Network  (6.00)
date: 07-03-2024
description:  
id: DO-134
lang: en
---

# Event Publishers for Continia Delivery Network (6.00)

The following event publishers are included in Continia Delivery Network (6.00):

### Codeunit 6086225 CTS-CDN Document Output Mgt.


|   |   |
| --- | --- |
| Event name | **OnBeforePrePostValidate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesHeader: `Record` "Sales Header"<br> EDocSendCode: `Code[20]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePrePostValidateServ** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceHeader: `Record` "Service Header"<br> EDocSendCode: `Code[20]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateEndPointID** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | IDType: `Record` "CTS-CDN Participation ID Type"<br> `var` IdValue: `Text`<br> CountryRegion: `Code[10]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetCustomerOutputProfile** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | CustomerNo: `Code[20]`<br> `var` OutputProfile: `Code[20]`<br> `var` Handled: `Boolean` |
| From version | 6.2.0.0 |

### Codeunit 6086227 CTS-CDN DC Proxy


|   |   |
| --- | --- |
| Event name | **OnDocCategoryLookup** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Text: `Text[1024]`<br> `var` DocCatCode: `Code[20]` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnInvalidCharsInNoSeriesByCode** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | NoSeriesCode: `Code[20]` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnGetCultureNameById** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | LanguageId: `Integer`<br> `var` ReturnLangCode: `Text[30]` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnGetSetupBaseUrl** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` SetupBaseUrl: `Text` |
| From version | 6.0.0.0 |

### Codeunit 6086229 CTS-CDN DO Proxy


|   |   |
| --- | --- |
| Event name | **OnSetExportResponse** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` FromRecordRef: `RecordRef`<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> Filename: `Text` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnSetDeliveryResponse** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | DeliveryOK: `Boolean`<br> ErrorMessage: `Text` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnGetEDocCode** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | RecordVariant: `Variant`<br> `var` EDocCode: `Code[20]` |
| From version | 6.0.0.0 |

### Codeunit 6086230 CTS-CDN Wizard Helper


|   |   |
| --- | --- |
| Event name | **OnBeforeIsNemHandelActive** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` SkipLocalizationCheck: `Boolean` |
| From version | 6.0.0.0 |

### Codeunit 6086232 CTS-CDN PEPPOL Mgt.


|   |   |
| --- | --- |
| Event name | **OnBeforeGetIso4217CurrencyCode** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | CurrencyCode: `Code[10]`<br> `var` Handled: `Boolean`<br> `var` ReturnValue: `Code[3]` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetUNECERec20UOMCode** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | UOMCode: `Code[10]`<br> `var` Handled: `Boolean`<br> `var` ReturnValue: `Code[10]` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeAddPeppolCountrySpecifics** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | VATRegNo: `Text[20]`<br> CountryCode: `Code[10]`<br> Handled: `Boolean`<br> `var` ReturnValue: `Text[1024]` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetNamespaces** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Namespaces: `Record` "CTS-CDN XML Export Namespace" temporary<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSetNamespaces** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Namespaces: `Record` "CTS-CDN XML Export Namespace" temporary |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnGetTotalsOnBeforeInsertVATAmtLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesLine: `Record` "Sales Line"<br> `var` VATAmtLine: `Record` "VAT Amount Line" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnCreateItemAttributes** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ItemNode: `Codeunit` "CSC XML Node"<br> ItemNo: `Code[20]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeTranslateForPartyID** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | VatRegNo: `Text[30]`<br> CountryCode: `Code[10]`<br> `var` ReturnValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeTranslateForTaxCompany** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | VatRegNo: `Text[30]`<br> CountryCode: `Code[10]`<br> `var` ReturnValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeTranslateForLegalCompany** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | VatRegNo: `Text[30]`<br> CountryCode: `Code[10]`<br> `var` ReturnValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSetPaymentMeansCode** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` PaymentMeansCode: `Code[2]` |
| From version | 6.0.0.0 |

### Codeunit 6086233 CTS-CDN ISO Code Mgt.


|   |   |
| --- | --- |
| Event name | **OnBeforeGetCountryCodeISO31661** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | CountryCode: `Code[10]`<br> `var` Handled: `Boolean`<br> `var` ReturnValue: `Code[3]` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetCurrencyCodeISO4217** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | CurrencyCode: `Code[10]`<br> `var` Handled: `Boolean`<br> `var` ReturnValue: `Code[3]` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetUOMCodeUNECERec20** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | UOMCode: `Code[10]`<br> `var` Handled: `Boolean`<br> `var` ReturnValue: `Code[10]` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeAddPeppolCountrySpecifics** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | VATRegNo: `Text[20]`<br> CountryCode: `Code[10]`<br> Handled: `Boolean`<br> `var` ReturnValue: `Text[1024]` |
| From version | 6.0.0.0 |

### Codeunit 6086234 CTS-CDN Export Mgt.


|   |   |
| --- | --- |
| Event name | **OnAfterGetReceiverInfo** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | FromRecord: `Variant`<br> CustomerNo: `Code[20]`<br> ForNetworkProfile: `Record` "CTS-CDN Network Profile"<br> `var` ReceiverIDType: `Record` "CTS-CDN Participation ID Type"<br> `var` ReceiverIDValue: `Text[250]` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSkipDocumentLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | FromCodeunit: `Integer`<br> DocLineVariant: `Variant`<br> `var` SkipLine: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSkipDocumentLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | FromCodeunit: `Integer`<br> DocLineVariant: `Variant`<br> `var` SkipLine: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetLatestNetworkProfile** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ForNetworkProfile: `Record` "CTS-CDN Network Profile"<br> Participation: `Record` "CTS-CDN Participation"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSelectLatestVersionOfProfile** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ParticipProfileRel: `Record` "CTS-CDN Particip. Profile Rel."<br> `var` ForNetworkProfile: `Record` "CTS-CDN Network Profile"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSelectLatestVersionOfProfile** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ParticipProfileRel: `Record` "CTS-CDN Particip. Profile Rel."<br> `var` ForNetworkProfile: `Record` "CTS-CDN Network Profile" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSelectMatchingProfileVersion** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ParticipProfileRel: `Record` "CTS-CDN Particip. Profile Rel."<br> `var` ForNetworkProfile: `Record` "CTS-CDN Network Profile"<br> `var` APNetworkProfiles: `Record` "CTS-CDN AP Network Profile" temporary<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSelectMatchingProfileVersion** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ParticipProfileRel: `Record` "CTS-CDN Particip. Profile Rel."<br> `var` ForNetworkProfile: `Record` "CTS-CDN Network Profile"<br> `var` APNetworkProfiles: `Record` "CTS-CDN AP Network Profile" temporary<br> `var` SelectedProfileID: `Integer` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetProfileIdentifier** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ForNetworkProfile: `Record` "CTS-CDN Network Profile"<br> `var` ProfileIdentifier: `Text`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |

### Codeunit 6086235 CTS-CDN Localization Mgt.


|   |   |
| --- | --- |
| Event name | **OnBeforeGetCompanyID** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` CompanyIdentifier: `Text[250]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetCustomerID** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Customer: `Record Customer`<br> `var` CustomerIdentifier: `Text[250]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetCompanyIDForIDType** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | IDType: `Record` "CTS-CDN Participation ID Type"<br> `var` CompanyIdentifier: `Text[250]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetCustomerIDForIDType** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | IDType: `Record` "CTS-CDN Participation ID Type"<br> Customer: `Record Customer`<br> `var` CustomerIdentifier: `Text[250]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterFindIDFieldCustomer** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Customer: `Record Customer`<br> `var` IdentifierFieldNo: `Integer` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterFindIDFieldCompany** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` IdentifierFiledNo: `Integer` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetCompanySIRETNo** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` SIRETNo: `Text`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetCustomerSIRETNo** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Customer: `Record Customer`<br> `var` SIRETNo: `Text`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetCustomerIDForIDType2** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` IDType: `Record` "CTS-CDN Participation ID Type"<br> Customer: `Record Customer`<br> `var` CustomerIdentifier: `Text[250]`<br> `var` UseIdType: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 6.2.0.0 |

### Codeunit 6086239 CTS-CDN DO Page Helpers


|   |   |
| --- | --- |
| Event name | **OnGetZugferdParameters** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | CustomerNo: `Code[20]`<br> `var` Conformance: `Text`<br> `var` Filename: `Text`<br> `var` DocType: `Text`<br> `var` DocVersion: `Text`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnGetZugferdDocTypeFromTable** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | TableNo: `Integer`<br> `var` DocumentType: `Text`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |

### Codeunit 6086240 CTS-CDN PEPPOL BIS3 Inv.


|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` LineNodeList: `Codeunit` "CSC XML NodeList" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentTermsText: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeaderDiscounts** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateTaxTotal** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLegalMonetary** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceLine: `Record` "Sales Invoice Line"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceLine: `Record` "Sales Invoice Line"<br> `var` InvoiceLineNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` TempBlob: `Record` "CSC Temp Blob" temporary<br> `var` Filename: `Text[1024]`<br> `var` ID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreatePaymentMeans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentType: `Option Bank,KID,FIK`<br> `var` PaymentID: `Text[1024]`<br> `var` AccountID: `Code[50]`<br> `var` FinancialInstitutionBranchID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetOrderReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` OrderRefID: `Code[50]`<br> `var` OrderRefSalesOrderID: `Code[50]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateBuyerReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` BuyerRefValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetInvPeriodHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` InvoicePeriodStartDate: `Date`<br> `var` InvoicePeriodEndDate: `Date`<br> `var` InvoicePeriodDescriptionCode: `Code[50]` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetInvPeriodLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceLine: `Record` "Sales Invoice Line"<br> `var` InvoicePeriodStartDate: `Date`<br> `var` InvoicePeriodEndDate: `Date` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnSetTaxCurrencyCode** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` TaxCurrencyCode: `Code[10]`<br> `var` TaxAmountInTaxCurrency: `Decimal` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetSalesPerson** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` SalespersonPurchaser: `Record` "Salesperson/Purchaser"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetHeaderNotes** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XMLNode: `Codeunit` "CSC XML Node"<br> `var` HeaderNotesHandled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetLineNotes** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceLine: `Record` "Sales Invoice Line"<br> `var` XMLNode: `Codeunit` "CSC XML Node"<br> `var` LineNotesHandled: `Boolean` |
| From version | 6.0.0.0 |

### Codeunit 6086241 CTS-CDN PEPPOL BIS3 Cr.M.


|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` LineNodeList: `Codeunit` "CSC XML NodeList" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentTermsText: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeaderDiscounts** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateTaxTotal** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLegalMonetary** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoLine: `Record` "Sales Cr.Memo Line"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoLine: `Record` "Sales Cr.Memo Line"<br> `var` InvoiceLineNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` TempBlob: `Record` "CSC Temp Blob" temporary<br> `var` Filename: `Text[1024]`<br> `var` ID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreatePaymentMeans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentType: `Option Bank,KID,FIK`<br> `var` PaymentID: `Text[1024]`<br> `var` AccountID: `Code[50]`<br> `var` FinancialInstitutionBranchID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetOrderReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` OrderRefID: `Code[50]`<br> `var` OrderRefSalesOrderID: `Code[50]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateBuyerReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` BuyerRefValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnSetTaxCurrencyCode** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` TaxCurrencyCode: `Code[10]`<br> `var` TaxAmountInTaxCurrency: `Decimal` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetInvoiceDocumentReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` InvoiceDocumentReference: `Code[20]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |
| Obsolete | Replaced by OnBeforeSetInvDocumentReference |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetInvDocumentReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` InvoiceDocumentReference: `Code[35]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetSalesPerson** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` SalespersonPurchaser: `Record` "Salesperson/Purchaser"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetHeaderNotes** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XMLNode: `Codeunit` "CSC XML Node"<br> `var` HeaderNotesHandled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetLineNotes** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoLine: `Record` "Sales Cr.Memo Line"<br> `var` XMLNode: `Codeunit` "CSC XML Node"<br> `var` LineNotesHandled: `Boolean` |
| From version | 6.0.0.0 |

### Codeunit 6086242 CTS-CDN PEPPOL BIS3 Sv. Inv.


|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` LineNodeList: `Codeunit` "CSC XML NodeList" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentTermsText: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeaderDiscounts** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateTaxTotal** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLegalMonetary** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceLine: `Record` "Service Invoice Line"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceLine: `Record` "Service Invoice Line"<br> `var` InvoiceLineNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` TempBlob: `Record` "CSC Temp Blob" temporary<br> `var` Filename: `Text[1024]`<br> `var` ID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreatePaymentMeans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentType: `Option Bank,KID,FIK`<br> `var` PaymentID: `Text[1024]`<br> `var` AccountID: `Code[50]`<br> `var` FinancialInstitutionBranchID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetOrderReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` OrderRefID: `Code[50]`<br> `var` OrderRefSalesOrderID: `Code[50]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateBuyerReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` BuyerRefValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnSetTaxCurrencyCode** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` TaxCurrencyCode: `Code[10]`<br> `var` TaxAmountInTaxCurrency: `Decimal` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetSalesPerson** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` SalespersonPurchaser: `Record` "Salesperson/Purchaser"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetHeaderNotes** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` XMLNode: `Codeunit` "CSC XML Node"<br> `var` HeaderNotesHandled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetLineNotes** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceLine: `Record` "Service Invoice Line"<br> `var` XMLNode: `Codeunit` "CSC XML Node"<br> `var` LineNotesHandled: `Boolean` |
| From version | 6.0.0.0 |

### Codeunit 6086243 CTS-CDN XRechnung 2 Inv.


|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` LineNodeList: `Codeunit` "CSC XML NodeList" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentTermsText: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeaderDiscounts** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateTaxTotal** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLegalMonetary** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceLine: `Record` "Sales Invoice Line"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceLine: `Record` "Sales Invoice Line"<br> `var` InvoiceLineNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` TempBlob: `Record` "CSC Temp Blob" temporary<br> `var` Filename: `Text[1024]`<br> `var` ID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreatePaymentMeans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentType: `Option Bank,KID,FIK`<br> `var` PaymentID: `Text[1024]`<br> `var` AccountID: `Code[50]`<br> `var` FinancialInstitutionBranchID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetOrderReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` OrderRefID: `Code[50]`<br> `var` OrderRefSalesOrderID: `Code[50]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateBuyerReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` BuyerRefValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetInvPeriodHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` InvoicePeriodStartDate: `Date`<br> `var` InvoicePeriodEndDate: `Date`<br> `var` InvoicePeriodDescriptionCode: `Code[50]` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetInvPeriodLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceLine: `Record` "Sales Invoice Line"<br> `var` InvoicePeriodStartDate: `Date`<br> `var` InvoicePeriodEndDate: `Date` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnSetTaxCurrencyCode** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` TaxCurrencyCode: `Code[10]`<br> `var` TaxAmountInTaxCurrency: `Decimal` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetSalesPerson** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` SalespersonPurchaser: `Record` "Salesperson/Purchaser"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetHeaderNotes** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XMLNode: `Codeunit` "CSC XML Node"<br> `var` HeaderNotesHandled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetLineNotes** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceLine: `Record` "Sales Invoice Line"<br> `var` XMLNode: `Codeunit` "CSC XML Node"<br> `var` LineNotesHandled: `Boolean` |
| From version | 6.0.0.0 |

### Codeunit 6086244 CTS-CDN XRechnung 2 Cr.Memo


|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` LineNodeList: `Codeunit` "CSC XML NodeList" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentTermsText: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeaderDiscounts** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateTaxTotal** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLegalMonetary** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoLine: `Record` "Sales Cr.Memo Line"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoLine: `Record` "Sales Cr.Memo Line"<br> `var` InvoiceLineNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` TempBlob: `Record` "CSC Temp Blob" temporary<br> `var` Filename: `Text[1024]`<br> `var` ID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreatePaymentMeans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentType: `Option Bank,KID,FIK`<br> `var` PaymentID: `Text[1024]`<br> `var` AccountID: `Code[50]`<br> `var` FinancialInstitutionBranchID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetOrderReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` OrderRefID: `Code[50]`<br> `var` OrderRefSalesOrderID: `Code[50]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateBuyerReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` BuyerRefValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnSetTaxCurrencyCode** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` TaxCurrencyCode: `Code[10]`<br> `var` TaxAmountInTaxCurrency: `Decimal` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetSalesPerson** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` SalespersonPurchaser: `Record` "Salesperson/Purchaser"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetHeaderNotes** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XMLNode: `Codeunit` "CSC XML Node"<br> `var` HeaderNotesHandled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetLineNotes** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoLine: `Record` "Sales Cr.Memo Line"<br> `var` XMLNode: `Codeunit` "CSC XML Node"<br> `var` LineNotesHandled: `Boolean` |
| From version | 6.0.0.0 |

### Codeunit 6086245 CTS-CDN XRechnung 2 Sv. Inv.


|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` LineNodeList: `Codeunit` "CSC XML NodeList" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentTermsText: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeaderDiscounts** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateTaxTotal** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLegalMonetary** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceLine: `Record` "Service Invoice Line"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` TempBlob: `Record` "CSC Temp Blob" temporary<br> `var` Filename: `Text[1024]`<br> `var` ID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreatePaymentMeans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentType: `Option Bank,KID,FIK`<br> `var` PaymentID: `Text[1024]`<br> `var` AccountID: `Code[50]`<br> `var` FinancialInstitutionBranchID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceLine: `Record` "Service Invoice Line"<br> `var` InvoiceLineNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetOrderReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` OrderRefID: `Code[50]`<br> `var` OrderRefSalesOrderID: `Code[50]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateBuyerReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` BuyerRefValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnSetTaxCurrencyCode** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` TaxCurrencyCode: `Code[10]`<br> `var` TaxAmountInTaxCurrency: `Decimal` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetSalesPerson** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` SalespersonPurchaser: `Record` "Salesperson/Purchaser"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetHeaderNotes** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` XMLNode: `Codeunit` "CSC XML Node"<br> `var` HeaderNotesHandled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetLineNotes** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceLine: `Record` "Service Invoice Line"<br> `var` XMLNode: `Codeunit` "CSC XML Node"<br> `var` LineNotesHandled: `Boolean` |
| From version | 6.0.0.0 |

### Codeunit 6086246 CTS-CDN XRechnung 2 Sv.Cr.Memo


|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` LineNodeList: `Codeunit` "CSC XML NodeList" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentTermsText: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeaderDiscounts** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateTaxTotal** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLegalMonetary** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoLine: `Record` "Service Cr.Memo Line"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoLine: `Record` "Service Cr.Memo Line"<br> `var` InvoiceLineNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` TempBlob: `Record` "CSC Temp Blob" temporary<br> `var` Filename: `Text[1024]`<br> `var` ID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetOrderReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` OrderRefID: `Code[50]`<br> `var` OrderRefSalesOrderID: `Code[50]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateBuyerReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` BuyerRefValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreatePaymentMeans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentType: `Option Bank,KID,FIK`<br> `var` PaymentID: `Text[1024]`<br> `var` AccountID: `Code[50]`<br> `var` FinancialInstitutionBranchID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnSetTaxCurrencyCode** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` TaxCurrencyCode: `Code[10]`<br> `var` TaxAmountInTaxCurrency: `Decimal` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetSalesPerson** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` SalespersonPurchaser: `Record` "Salesperson/Purchaser"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetHeaderNotes** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XMLNode: `Codeunit` "CSC XML Node"<br> `var` HeaderNotesHandled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetLineNotes** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoLine: `Record` "Service Cr.Memo Line"<br> `var` XMLNode: `Codeunit` "CSC XML Node"<br> `var` LineNotesHandled: `Boolean` |
| From version | 6.0.0.0 |

### Codeunit 6086247 CTS-CDN PEPPOL BIS3 Sv. Cr.M.


|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` LineNodeList: `Codeunit` "CSC XML NodeList" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentTermsText: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeaderDiscounts** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateTaxTotal** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLegalMonetary** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoLine: `Record` "Service Cr.Memo Line"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoLine: `Record` "Service Cr.Memo Line"<br> `var` InvoiceLineNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` TempBlob: `Record` "CSC Temp Blob" temporary<br> `var` Filename: `Text[1024]`<br> `var` ID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreatePaymentMeans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentType: `Option Bank,KID,FIK`<br> `var` PaymentID: `Text[1024]`<br> `var` AccountID: `Code[50]`<br> `var` FinancialInstitutionBranchID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetOrderReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` OrderRefID: `Code[50]`<br> `var` OrderRefSalesOrderID: `Code[50]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateBuyerReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` BuyerRefValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnSetTaxCurrencyCode** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` TaxCurrencyCode: `Code[10]`<br> `var` TaxAmountInTaxCurrency: `Decimal` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetInvoiceDocumentReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` InvoiceDocumentReference: `Code[20]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |
| Obsolete | Replaced by OnBeforeSetInvDocumentReference |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetInvDocumentReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` InvoiceDocumentReference: `Code[35]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetSalesPerson** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` SalespersonPurchaser: `Record` "Salesperson/Purchaser"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetHeaderNotes** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XMLNode: `Codeunit` "CSC XML Node"<br> `var` HeaderNotesHandled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetLineNotes** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoLine: `Record` "Service Cr.Memo Line"<br> `var` XMLNode: `Codeunit` "CSC XML Node"<br> `var` LineNotesHandled: `Boolean` |
| From version | 6.0.0.0 |

### Codeunit 6086250 CTS-CDN PEPPOL Chk. Sales Hdr.


|   |   |
| --- | --- |
| Event name | **OnBeforeCheckLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesHeader: `Record` "Sales Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckPricesExclVAT** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesHeader: `Record` "Sales Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidatePaymentTermsCode** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesHeader: `Record` "Sales Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateExternalDocumentNo** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesHeader: `Record` "Sales Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateBillToCustomer** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesHeader: `Record` "Sales Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateSellToCustomer** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesHeader: `Record` "Sales Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckNLSpecifics** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesHeader: `Record` "Sales Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |

### Codeunit 6086251 CTS-CDN PEPPOL Chk. Sales Inv.


|   |   |
| --- | --- |
| Event name | **OnAfterValidate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckPricesExclVAT** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidatePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateExternalDocumentNo** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateSellToCustomer** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateBillToCustomer** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckNLSpecifics** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |

### Codeunit 6086252 CTS-CDN PEPPOL Chk. Sales Cr.M


|   |   |
| --- | --- |
| Event name | **OnAfterValidate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckPricesExclVAT** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidatePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateExternalDocumentNo** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateSellToCustomer** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateBillToCustomer** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckNLSpecifics** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |

### Codeunit 6086253 CTS-CDN XRech2 Chk. Sales Hdr.


|   |   |
| --- | --- |
| Event name | **OnAfterCheck** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesHeader: `Record` "Sales Header" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSetFiltersCheckLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` SalesLine: `Record` "Sales Line" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesHeader: `Record` "Sales Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesHeader: `Record` "Sales Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckPricesExclVAT** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesHeader: `Record` "Sales Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidatePaymentTermsCode** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesHeader: `Record` "Sales Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateBillToCustomer** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesHeader: `Record` "Sales Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |

### Codeunit 6086254 CTS-CDN XRech2 Chk. Sales Inv.


|   |   |
| --- | --- |
| Event name | **OnAfterCheck** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSetFiltersCheckLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` SalesInvoiceLine: `Record` "Sales Invoice Line" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckPricesExclVAT** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidatePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateBillToCustomer** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |

### Codeunit 6086255 CTS-CDN XRech2 Chk. Sales Cr.M


|   |   |
| --- | --- |
| Event name | **OnAfterCheck** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSetFiltersCheckLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` SalesCrMemoLine: `Record` "Sales Cr.Memo Line" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckPricesExclVAT** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidatePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateBillToCustomer** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |

### Codeunit 6086258 CTS-CDN XRech2 Chk. Sv. Hdr.


|   |   |
| --- | --- |
| Event name | **OnBeforeValidate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceHeader: `Record` "Service Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCheck** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceHeader: `Record` "Service Header" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSetFiltersCheckLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ServiceLine: `Record` "Service Line" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceHeader: `Record` "Service Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckPricesExclVAT** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceHeader: `Record` "Service Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidatePaymentTermsCode** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceHeader: `Record` "Service Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateBillToCustomer** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceHeader: `Record` "Service Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |

### Codeunit 6086259 CTS-CDN XRech2 Chk. Sv. Inv.


|   |   |
| --- | --- |
| Event name | **OnAfterCheck** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSetFiltersCheckLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ServiceInvoiceLine: `Record` "Service Invoice Line" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckPricesExclVAT** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidatePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateBillToCustomer** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |

### Codeunit 6086260 CTS-CDN XRech2 Chk. Sv. Cr.M


|   |   |
| --- | --- |
| Event name | **OnAfterCheck** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Service Cr.Memo Header" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSetFiltersCheckLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ServiceCrMemoLine: `Record` "Service Cr.Memo Line" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckPricesExclVAT** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidatePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateBillToCustomer** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |

### Codeunit 6086266 CTS-CDN PEPPOL Chk.Sv.ServHdr.


|   |   |
| --- | --- |
| Event name | **OnBeforeCheckLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceHeader: `Record` "Service Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckPricesExclVAT** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceHeader: `Record` "Service Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidatePaymentTermsCode** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceHeader: `Record` "Service Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateBillToCustomer** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceHeader: `Record` "Service Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateSellToCustomer** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceHeader: `Record` "Service Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |

### Codeunit 6086267 CTS-CDN PEPPOL Chk. Serv. Inv.


|   |   |
| --- | --- |
| Event name | **OnAfterValidate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckPricesExclVAT** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidatePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateBillToCustomer** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateSellToCustomer** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |

### Codeunit 6086268 CTS-CDN PEPPOL Chk. Serv. Cr.M


|   |   |
| --- | --- |
| Event name | **OnAfterValidate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidate** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckPricesExclVAT** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidatePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateBillToCustomer** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateSellToCustomer** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |

### Codeunit 6086270 CTS-CDN OIOUBL Mgt.


|   |   |
| --- | --- |
| Event name | **OnGetTotalsOnBeforeInsertVATAmtLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesLine: `Record` "Sales Line"<br> `var` VATAmtLine: `Record` "VAT Amount Line" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetNamespaces** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Namespaces: `Record` "CTS-CDN XML Export Namespace" temporary<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSetNamespaces** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Namespaces: `Record` "CTS-CDN XML Export Namespace" temporary |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeTranslateForPartyID** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | VatRegNo: `Text[30]`<br> CountryCode: `Code[10]`<br> `var` ReturnValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeTranslateForTaxCompany** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | VatRegNo: `Text[30]`<br> CountryCode: `Code[10]`<br> `var` ReturnValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeTranslateForLegalCompany** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | VatRegNo: `Text[30]`<br> CountryCode: `Code[10]`<br> `var` ReturnValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnCreateItemAttributes** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ItemNode: `Codeunit` "CSC XML Node"<br> ItemNo: `Code[20]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeAddPeppolCountrySpecifics** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | VATRegNo: `Text[20]`<br> CountryCode: `Code[10]`<br> `var` Handled: `Boolean`<br> `var` ReturnValue: `Text[1024]` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSupplierPartyPostalAddress** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | CompInfo: `Record` "Company Information"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Party: `Codeunit` "CSC XML Node"<br> `var` AddressFormatCode: `Text[250]`<br> `var` ListId: `Text[250]`<br> `var` ListAgencyID: `Text[250]`<br> `var` PostalAddressHandled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCustomerPartyPostalAddress** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | Customer: `Record Customer`<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Party: `Codeunit` "CSC XML Node"<br> `var` AddressFormatCode: `Text[250]`<br> `var` ListId: `Text[250]`<br> `var` ListAgencyID: `Text[250]`<br> `var` PostalAddressHandled: `Boolean` |
| From version | 6.0.0.0 |

### Codeunit 6086271 CTS-CDN OIOUBL Export Inv.


|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` LineNodeList: `Codeunit` "CSC XML NodeList" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` TempBlob: `Record` "CSC Temp Blob" temporary<br> `var` Filename: `Text[1024]`<br> `var` ID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentTermsText: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeaderDiscounts** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateTaxTotal** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLegalMonetary** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetOrderReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` OrderRefID: `Code[50]`<br> `var` OrderRefSalesOrderID: `Code[50]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSetOrderReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceLine: `Record` "Sales Invoice Line"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceLine: `Record` "Sales Invoice Line"<br> `var` InvoiceLineNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeaderNotes** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> XMLNode: `Codeunit` "CSC XML Node"<br> `var` HeaderNotesHandled: `Boolean` |
| From version | 6.0.0.0 |
| Obsolete | Replaced by OnBeforeSetHeaderNotes |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetHeaderNotes** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XMLNode: `Codeunit` "CSC XML Node"<br> `var` HeaderNotesHandled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetInvoiceLineDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` InvoiceLine: `Codeunit` "CSC XML Node"<br> SalesInvoiceLine: `Record` "Sales Invoice Line"<br> `var` DeliveryQuantity: `Decimal`<br> `var` DeliveryMinQuantity: `Decimal`<br> `var` DeliveryMaxQuantity: `Decimal`<br> `var` DeliveryActualDeliveryDate: `Date`<br> `var` DeliveryActualDeliveryTime: `Time`<br> `var` DeliveryTrackingID: `Text[250]`<br> `var` DeliveryHandled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetLineItemPrice** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceLine: `Record` "Sales Invoice Line"<br> `var` InvoiceLineNode: `Codeunit` "CSC XML Node"<br> `var` PriceAmount: `Decimal`<br> `var` BaseQuantity: `Decimal`<br> `var` UOMCode: `Code[10]`<br> `var` DiscountAmount: `Decimal`<br> `var` DiscountBaseAmount: `Decimal`<br> `var` CurrencyCode: `Code[10]`<br> `var` FieldsCalculated: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnSetPaymentMeans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentType: `Option Bank,KID,FIK`<br> `var` PaymentID: `Text[1024]`<br> `var` AccountID: `Code[50]`<br> `var` FinancialInstitutionBranchID: `Text[1024]`<br> `var` InstructionID: `Text[1024]`<br> `var` PaymentDueDate: `Date`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetSalesPerson** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` SalespersonPurchaser: `Record` "Salesperson/Purchaser"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |

### Codeunit 6086272 CTS-CDN OIOUBL Export Cr.


|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` LineNodeList: `Codeunit` "CSC XML NodeList" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` TempBlob: `Record` "CSC Temp Blob" temporary<br> `var` Filename: `Text[1024]`<br> `var` ID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePaymentMeans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentType: `Option Bank,KID,FIK`<br> `var` PaymentID: `Text[1024]`<br> `var` AccountID: `Code[50]`<br> `var` FinancialInstitutionBranchID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |
| Obsolete | Not used |



|   |   |
| --- | --- |
| Event name | **OnBeforePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentTermsText: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |
| Obsolete | Not used |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeaderDiscounts** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateTaxTotal** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLegalMonetary** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetOrderReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` OrderRefID: `Code[50]`<br> `var` OrderRefSalesOrderID: `Code[50]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSetOrderReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoLine: `Record` "Sales Cr.Memo Line"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoLine: `Record` "Sales Cr.Memo Line"<br> `var` InvoiceLineNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeaderNotes** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> XMLNode: `Codeunit` "CSC XML Node"<br> `var` HeaderNotesHandled: `Boolean` |
| From version | 6.0.0.0 |
| Obsolete | Replaced by OnBeforeSetHeaderNotes |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetHeaderNotes** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XMLNode: `Codeunit` "CSC XML Node"<br> `var` HeaderNotesHandled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetCreditMemoLineDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` InvoiceLine: `Codeunit` "CSC XML Node"<br> SalesCrMemoLine: `Record` "Sales Cr.Memo Line"<br> `var` DeliveryQuantity: `Decimal`<br> `var` DeliveryMinQuantity: `Decimal`<br> `var` DeliveryMaxQuantity: `Decimal`<br> `var` DeliveryActualDeliveryDate: `Date`<br> `var` DeliveryActualDeliveryTime: `Time`<br> `var` DeliveryTrackingID: `Text[250]`<br> `var` DeliveryHandled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetLineItemPrice** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoLine: `Record` "Sales Cr.Memo Line"<br> `var` InvoiceLineNode: `Codeunit` "CSC XML Node"<br> `var` PriceAmount: `Decimal`<br> `var` BaseQuantity: `Decimal`<br> `var` UOMCode: `Code[10]`<br> `var` DiscountAmount: `Decimal`<br> `var` DiscountBaseAmount: `Decimal`<br> `var` CurrencyCode: `Code[10]`<br> `var` FieldsCalculated: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetSalesPerson** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` SalespersonPurchaser: `Record` "Salesperson/Purchaser"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |

### Codeunit 6086273 CTS-CDN OIOUBL Reminder


|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | IssuedReminderHeader: `Record` "Issued Reminder Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | IssuedReminderHeader: `Record` "Issued Reminder Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | IssuedReminderHeader: `Record` "Issued Reminder Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | IssuedReminderHeader: `Record` "Issued Reminder Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` LineNodeList: `Codeunit` "CSC XML NodeList" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeaderNotes** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | IssuedReminderHeader: `Record` "Issued Reminder Header"<br> XMLNode: `Codeunit` "CSC XML Node"<br> `var` HeaderNotesHandled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | IssuedReminderHeader: `Record` "Issued Reminder Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | IssuedReminderHeader: `Record` "Issued Reminder Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePaymentMeans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | IssuedReminderHeader: `Record` "Issued Reminder Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentType: `Option Bank,KID,FIK`<br> `var` PaymentID: `Text[1024]`<br> `var` AccountID: `Code[50]`<br> `var` FinancialInstitutionBranchID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Issued Reminder Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateTaxTotal** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | IssuedReminderHeader: `Record` "Issued Reminder Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLegalMonetary** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | IssuedReminderHeader: `Record` "Issued Reminder Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | IssuedReminderLine: `Record` "Issued Reminder Line"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | IssuedReminderLine: `Record` "Issued Reminder Line"<br> `var` InvoiceLineNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |

### Codeunit 6086274 CTS-CDN OIOUBL Chk. Reminder


|   |   |
| --- | --- |
| Event name | **OnBeforeCheck** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | IssuedReminderHeader: `Record` "Issued Reminder Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCheck** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | IssuedReminderHeader: `Record` "Issued Reminder Header" |
| From version | 6.0.0.0 |

### Codeunit 6086275 CTS-CDN OIOUBL Chk. Sales Inv.


|   |   |
| --- | --- |
| Event name | **OnBeforeCheck** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCheck** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateCompanyInformation** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | CompanyInformation: `Record` "Company Information"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidatePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateExternalDocumentNo** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateBillToCustomer** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |

### Codeunit 6086276 CTS-CDN OIOUBL Chk. Sales Cr.M


|   |   |
| --- | --- |
| Event name | **OnBeforeCheck** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCheck** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateCompanyInformation** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | CompanyInformation: `Record` "Company Information"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidatePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateExternalDocumentNo** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateBillToCustomer** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |

### Codeunit 6086277 CTS-CDN OIOUBL Chk. Sales Hdr.


|   |   |
| --- | --- |
| Event name | **OnBeforeCheck** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesHeader: `Record` "Sales Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCheck** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesHeader: `Record` "Sales Header" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesHeader: `Record` "Sales Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateCompanyInformation** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | CompanyInformation: `Record` "Company Information"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidatePaymentTermsCode** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesHeader: `Record` "Sales Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateExternalDocumentNo** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesHeader: `Record` "Sales Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateBillToCustomer** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesHeader: `Record` "Sales Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |

### Codeunit 6086278 CTS-CDN OIOUBL Sv. Inv.


|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` LineNodeList: `Codeunit` "CSC XML NodeList" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` TempBlob: `Record` "CSC Temp Blob" temporary<br> `var` Filename: `Text[1024]`<br> `var` ID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentTermsText: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeaderDiscounts** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateTaxTotal** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLegalMonetary** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetOrderReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` OrderRefID: `Code[50]`<br> `var` OrderRefSalesOrderID: `Code[50]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSetOrderReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvLine: `Record` "Service Invoice Line"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvLine: `Record` "Service Invoice Line"<br> `var` InvoiceLineNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetHeaderNotes** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` XMLNode: `Codeunit` "CSC XML Node"<br> `var` HeaderNotesHandled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetInvoiceLineDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` InvoiceLine: `Codeunit` "CSC XML Node"<br> ServiceInvLine: `Record` "Service Invoice Line"<br> `var` DeliveryQuantity: `Decimal`<br> `var` DeliveryMinQuantity: `Decimal`<br> `var` DeliveryMaxQuantity: `Decimal`<br> `var` DeliveryActualDeliveryDate: `Date`<br> `var` DeliveryActualDeliveryTime: `Time`<br> `var` DeliveryTrackingID: `Text[250]`<br> `var` DeliveryHandled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetLineItemPrice** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvLine: `Record` "Service Invoice Line"<br> `var` InvoiceLineNode: `Codeunit` "CSC XML Node"<br> `var` PriceAmount: `Decimal`<br> `var` BaseQuantity: `Decimal`<br> `var` UOMCode: `Code[10]`<br> `var` DiscountAmount: `Decimal`<br> `var` DiscountBaseAmount: `Decimal`<br> `var` CurrencyCode: `Code[10]`<br> `var` FieldsCalculated: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnSetPaymentMeans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentType: `Option Bank,KID,FIK`<br> `var` PaymentID: `Text[1024]`<br> `var` AccountID: `Code[50]`<br> `var` FinancialInstitutionBranchID: `Text[1024]`<br> `var` InstructionID: `Text[1024]`<br> `var` PaymentDueDate: `Date`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetSalesPerson** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` SalespersonPurchaser: `Record` "Salesperson/Purchaser"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |

### Codeunit 6086279 CTS-CDN OIOUBL Sv. Cr.Memo


|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateHeader** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` LineNodeList: `Codeunit` "CSC XML NodeList" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateParties** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnCreateAdditionalDocRef** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` TempBlob: `Record` "CSC Temp Blob" temporary<br> `var` Filename: `Text[1024]`<br> `var` ID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentTermsText: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateHeaderDiscounts** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateTaxTotal** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLegalMonetary** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetOrderReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` OrderRefID: `Code[50]`<br> `var` OrderRefSalesOrderID: `Code[50]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSetOrderReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoLine: `Record` "Service Cr.Memo Line"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateLineLoop** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoLine: `Record` "Service Cr.Memo Line"<br> `var` InvoiceLineNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetHeaderNotes** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XMLNode: `Codeunit` "CSC XML Node"<br> `var` HeaderNotesHandled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetInvoiceLineDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` InvoiceLine: `Codeunit` "CSC XML Node"<br> ServiceCrMemoLine: `Record` "Service Cr.Memo Line"<br> `var` DeliveryQuantity: `Decimal`<br> `var` DeliveryMinQuantity: `Decimal`<br> `var` DeliveryMaxQuantity: `Decimal`<br> `var` DeliveryActualDeliveryDate: `Date`<br> `var` DeliveryActualDeliveryTime: `Time`<br> `var` DeliveryTrackingID: `Text[250]`<br> `var` DeliveryHandled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetLineItemPrice** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoLine: `Record` "Service Cr.Memo Line"<br> `var` InvoiceLineNode: `Codeunit` "CSC XML Node"<br> `var` PriceAmount: `Decimal`<br> `var` BaseQuantity: `Decimal`<br> `var` UOMCode: `Code[10]`<br> `var` DiscountAmount: `Decimal`<br> `var` DiscountBaseAmount: `Decimal`<br> `var` CurrencyCode: `Code[10]`<br> `var` FieldsCalculated: `Boolean`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnSetPaymentMeans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentType: `Option Bank,KID,FIK`<br> `var` PaymentID: `Text[1024]`<br> `var` AccountID: `Code[50]`<br> `var` FinancialInstitutionBranchID: `Text[1024]`<br> `var` InstructionID: `Text[1024]`<br> `var` PaymentDueDate: `Date`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetSalesPerson** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` SalespersonPurchaser: `Record` "Salesperson/Purchaser"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |

### Codeunit 6086280 CTS-CDN CII Inv.


|   |   |
| --- | --- |
| Event name | **OnBeforeCreateExchangedDocumentContext** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateExchangedDocumentContext** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateExchangedDocument** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateExchangedDocument** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateSupplyChainTradeTransaction** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateSupplyChainTradeTransaction** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateIncludedSupplyChainTradeLineItems** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateIncludedSupplyChainTradeLineItems** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateIncludedSupplyChainTradeLineItem** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> SalesInvoiceLine: `Record` "Sales Invoice Line"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateIncludedSupplyChainTradeLineItem** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> SalesInvoiceLine: `Record` "Sales Invoice Line"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSpecifiedTradeProduct** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> SalesInvoiceLine: `Record` "Sales Invoice Line"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSpecifiedLineTradeDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> SalesInvoiceLine: `Record` "Sales Invoice Line"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSpecifiedLineTradeSettlement** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> SalesInvoiceLine: `Record` "Sales Invoice Line"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeApplicableHeaderTradeAgreement** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> CDNParticipation: `Record` "CTS-CDN Participation" temporary<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterApplicableHeaderTradeAgreement** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> CDNParticipation: `Record` "CTS-CDN Participation" temporary<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeApplicableHeaderTradeDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterApplicableHeaderTradeDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeApplicableHeaderTradeSettlement** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterApplicableHeaderTradeSettlement** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreatePaymentMeans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentType: `Option Bank,KID,FIK`<br> `var` PaymentID: `Text[1024]`<br> `var` AccountID: `Code[50]`<br> `var` FinancialInstitutionBranchID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeApplicableTradeTax** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSpecifiedTradeAllowanceCharge** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSpecifiedTradePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentTermsText: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSpecifiedTradeSettlementHeaderMonetarySummation** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnGetOtherDocumentID** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvHeader: `Record` "Sales Invoice Header"<br> `var` VersionCode: `Text`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateAdditionalReferencedDocument** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnGetFilesToEmbed** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` CSCTempFile: `Record` "CSC Temp. File" temporary |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateApplicableHeaderTradeSettlement** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` CreditorReferenceID: `Text[100]`<br> `var` PaymentReference: `Text[100]` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSetEmbeddedFilename** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvoiceHeader: `Record` "Sales Invoice Header"<br> `var` Filename: `Text` |
| From version | 6.0.0.0 |

### Codeunit 6086281 CTS-CDN CII Cr.M.


|   |   |
| --- | --- |
| Event name | **OnBeforeCreateExchangedDocumentContext** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateExchangedDocumentContext** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateExchangedDocument** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateExchangedDocument** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateSupplyChainTradeTransaction** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateSupplyChainTradeTransaction** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateIncludedSupplyChainTradeLineItems** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateIncludedSupplyChainTradeLineItems** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateIncludedSupplyChainTradeLineItem** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> SalesCrMemoLine: `Record` "Sales Cr.Memo Line"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateIncludedSupplyChainTradeLineItem** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> SalesCrMemoLine: `Record` "Sales Cr.Memo Line"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSpecifiedTradeProduct** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> SalesCrMemoLine: `Record` "Sales Cr.Memo Line"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSpecifiedLineTradeDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> SalesCrMemoLine: `Record` "Sales Cr.Memo Line"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSpecifiedLineTradeSettlement** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> SalesCrMemoLine: `Record` "Sales Cr.Memo Line"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeApplicableHeaderTradeAgreement** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> CDNParticipation: `Record` "CTS-CDN Participation" temporary<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterApplicableHeaderTradeAgreement** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> CDNParticipation: `Record` "CTS-CDN Participation" temporary<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeApplicableHeaderTradeDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterApplicableHeaderTradeDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeApplicableHeaderTradeSettlement** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterApplicableHeaderTradeSettlement** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreatePaymentMeans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentType: `Option Bank,KID,FIK`<br> `var` PaymentID: `Text[1024]`<br> `var` AccountID: `Code[50]`<br> `var` FinancialInstitutionBranchID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeApplicableTradeTax** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSpecifiedTradeAllowanceCharge** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSpecifiedTradePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentTermsText: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSpecifiedTradeSettlementHeaderMonetarySummation** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnGetOtherDocumentID** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvHeader: `Record` "Sales Cr.Memo Header"<br> `var` VersionCode: `Text`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateAdditionalReferencedDocument** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnGetFilesToEmbed** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` CSCTempFile: `Record` "CSC Temp. File" temporary |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateApplicableHeaderTradeSettlement** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` CreditorReferenceID: `Text[100]`<br> `var` PaymentReference: `Text[100]` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSetEmbeddedFilename** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesCrMemoHeader: `Record` "Sales Cr.Memo Header"<br> `var` Filename: `Text` |
| From version | 6.0.0.0 |

### Codeunit 6086282 CTS-CDN CII Sv. Inv.


|   |   |
| --- | --- |
| Event name | **OnBeforeCreateExchangedDocumentContext** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateExchangedDocumentContext** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateExchangedDocument** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateExchangedDocument** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateSupplyChainTradeTransaction** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateSupplyChainTradeTransaction** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateIncludedSupplyChainTradeLineItems** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateIncludedSupplyChainTradeLineItems** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateIncludedSupplyChainTradeLineItem** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> ServiceInvoiceLine: `Record` "Service Invoice Line"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateIncludedSupplyChainTradeLineItem** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> ServiceInvoiceLine: `Record` "Service Invoice Line"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSpecifiedTradeProduct** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> ServiceInvoiceLine: `Record` "Service Invoice Line"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSpecifiedLineTradeDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> ServiceInvoiceLine: `Record` "Service Invoice Line"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSpecifiedLineTradeSettlement** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> ServiceInvoiceLine: `Record` "Service Invoice Line"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeApplicableHeaderTradeAgreement** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> CDNParticipation: `Record` "CTS-CDN Participation" temporary<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterApplicableHeaderTradeAgreement** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> CDNParticipation: `Record` "CTS-CDN Participation" temporary<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeApplicableHeaderTradeDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterApplicableHeaderTradeDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeApplicableHeaderTradeSettlement** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterApplicableHeaderTradeSettlement** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreatePaymentMeans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentType: `Option Bank,KID,FIK`<br> `var` PaymentID: `Text[1024]`<br> `var` AccountID: `Code[50]`<br> `var` FinancialInstitutionBranchID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeApplicableTradeTax** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSpecifiedTradeAllowanceCharge** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSpecifiedTradePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentTermsText: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSpecifiedTradeSettlementHeaderMonetarySummation** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnGetOtherDocumentID** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvHeader: `Record` "Service Invoice Header"<br> `var` VersionCode: `Text`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateAdditionalReferencedDocument** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnGetFilesToEmbed** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` CSCTempFile: `Record` "CSC Temp. File" temporary |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateApplicableHeaderTradeSettlement** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` CreditorReferenceID: `Text[100]`<br> `var` PaymentReference: `Text[100]` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSetEmbeddedFilename** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvHeader: `Record` "Service Invoice Header"<br> `var` Filename: `Text` |
| From version | 6.0.0.0 |

### Codeunit 6086283 CTS-CDN CII Sv. Cr.M.


|   |   |
| --- | --- |
| Event name | **OnBeforeCreateExchangedDocumentContext** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateExchangedDocumentContext** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateExchangedDocument** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateExchangedDocument** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateSupplyChainTradeTransaction** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateSupplyChainTradeTransaction** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateIncludedSupplyChainTradeLineItems** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateIncludedSupplyChainTradeLineItems** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateIncludedSupplyChainTradeLineItem** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> ServiceCrMemoLine: `Record` "Service Cr.Memo Line"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCreateIncludedSupplyChainTradeLineItem** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> ServiceCrMemoLine: `Record` "Service Cr.Memo Line"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSpecifiedTradeProduct** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> ServiceCrMemoLine: `Record` "Service Cr.Memo Line"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSpecifiedLineTradeDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> ServiceCrMemoLine: `Record` "Service Cr.Memo Line"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSpecifiedLineTradeSettlement** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> ServiceCrMemoLine: `Record` "Service Cr.Memo Line"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeApplicableHeaderTradeAgreement** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> CDNParticipation: `Record` "CTS-CDN Participation" temporary<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterApplicableHeaderTradeAgreement** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> CDNParticipation: `Record` "CTS-CDN Participation" temporary<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeApplicableHeaderTradeDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterApplicableHeaderTradeDelivery** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeApplicableHeaderTradeSettlement** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterApplicableHeaderTradeSettlement** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` SupplyChainTradeTransactionNode: `Codeunit` "CSC XML Node" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreatePaymentMeans** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentType: `Option Bank,KID,FIK`<br> `var` PaymentID: `Text[1024]`<br> `var` AccountID: `Code[50]`<br> `var` FinancialInstitutionBranchID: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeApplicableTradeTax** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSpecifiedTradeAllowanceCharge** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSpecifiedTradePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` PaymentTermsText: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSpecifiedTradeSettlementHeaderMonetarySummation** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnGetOtherDocumentID** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesInvHeader: `Record` "Service Cr.Memo Header"<br> `var` VersionCode: `Text`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateAdditionalReferencedDocument** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnGetFilesToEmbed** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` CSCTempFile: `Record` "CSC Temp. File" temporary |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCreateApplicableHeaderTradeSettlement** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` XmlDoc: `Codeunit` "CSC XML Document"<br> `var` RootNode: `Codeunit` "CSC XML Node"<br> `var` CreditorReferenceID: `Text[100]`<br> `var` PaymentReference: `Text[100]` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSetEmbeddedFilename** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` Filename: `Text` |
| From version | 6.0.0.0 |

### Codeunit 6086284 CTS-CDN OIOUBL Chk. Sv. Inv.


|   |   |
| --- | --- |
| Event name | **OnBeforeCheck** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCheck** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateCompanyInformation** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | CompanyInformation: `Record` "Company Information"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidatePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateYourReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateBillToCustomer** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceInvoiceHeader: `Record` "Service Invoice Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |

### Codeunit 6086285 CTS-CDN OIOUBL Chk. Sv.Cr.Memo


|   |   |
| --- | --- |
| Event name | **OnBeforeCheck** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterCheck** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeCheckLines** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateCompanyInformation** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | CompanyInformation: `Record` "Company Information"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidatePaymentTerms** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateYourReference** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeValidateBillToCustomer** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | ServiceCrMemoHeader: `Record` "Service Cr.Memo Header"<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |

### Codeunit 6086290 CTS-CDN CII Mgt.


|   |   |
| --- | --- |
| Event name | **OnBeforeGetIso4217CurrencyCode** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | CurrencyCode: `Code[10]`<br> `var` Handled: `Boolean`<br> `var` ReturnValue: `Code[3]` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetUNECERec20UOMCode** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | UOMCode: `Code[10]`<br> `var` Handled: `Boolean`<br> `var` ReturnValue: `Code[10]` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeAddPeppolCountrySpecifics** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | VATRegNo: `Text[20]`<br> CountryCode: `Code[10]`<br> Handled: `Boolean`<br> `var` ReturnValue: `Text[1024]` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeSetNamespaces** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Namespaces: `Record` "CTS-CDN XML Export Namespace" temporary<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnAfterSetNamespaces** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` Namespaces: `Record` "CTS-CDN XML Export Namespace" temporary |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnGetTotalsOnBeforeInsertVATAmtLine** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | SalesLine: `Record` "Sales Line"<br> `var` VATAmtLine: `Record` "VAT Amount Line" |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnCreateItemAttributes** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var` ItemNode: `Codeunit` "CSC XML Node"<br> ItemNo: `Code[20]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeTranslateForPartyID** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | VatRegNo: `Text[30]`<br> CountryCode: `Code[10]`<br> `var` ReturnValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeTranslateForTaxCompany** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | VatRegNo: `Text[30]`<br> CountryCode: `Code[10]`<br> `var` ReturnValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeTranslateForLegalCompany** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | VatRegNo: `Text[30]`<br> CountryCode: `Code[10]`<br> `var` ReturnValue: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



|   |   |
| --- | --- |
| Event name | **OnBeforeGetTaxExemptionReason** |
| Event type | IntegrationEvent(IncludeSender : `false`, GlobalVarAccess : `false`) |
| Parameters | `var`iant: `Variant`<br> TempVATAmtLine: `Record` "VAT Amount Line" temporary<br> `var` TaxExtemptionReason: `Text[1024]`<br> `var` Handled: `Boolean` |
| From version | 6.0.0.0 |



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
