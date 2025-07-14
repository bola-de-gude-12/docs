---
title: Document validation in the Continia Delivery Network
date: 10-12-2024
description: Comprehensive guide to e-document validation standards in the Continia Delivery Network, covering PEPPOLBIS3, XRECHNUNG2, and OIOUBL compliance
id: DO-213
lang: en
---

# Document validation in the Continia Delivery Network (CDN)

## Overview

The Continia Delivery Network (CDN) ensures that all e-documents processed through its Document Output feature comply with various validation requirements. These validations are performed by specific codeunits tailored to different document standards, including PEPPOLBIS3, XRECHNUNG2, and OIOUBL.

## Validation standards

### PEPPOLBIS3

PEPPOLBIS3 validation applies to the following document types:
- Sales Invoice
- Credit Memo
- Service Sales Invoice
- Service Credit Memo

Codeunits:
- 6086251: CTS-CDN PEPPOL Chk. Sales Inv.
- 6086252: CTS-CDN PEPPOL Chk. Sales Cr.M
- 6086267: CTS-CDN PEPPOL Chk. Serv. Inv.
- 6086268: CTS-CDN PEPPOL Chk. Serv. Cr.M

#### Key validation rules
1. Sales Invoice:
   - Payment Terms Code must not be empty.
   - External Document No. must not be empty.
   - Customer validations:
     - Sell-to Customer and Bill-to Customer must exist with valid Name and Country/Region Code.
   - Sales Invoice Lines:
     - No. and Description must not be empty.
     - Total amounts (lines and discounts) must not be negative.
   - Netherlands-specific validations:
     - Company and Customer addresses (Address, City, Post Code) must be filled.

2. Credit Memo, Service Sales Invoice, and Service Credit Memo:
   - Validation rules mirror those of the Sales Invoice.

### XRECHNUNG2

XRECHNUNG2 validation applies to the same document types as PEPPOLBIS3, with the following codeunits:
- 6086254: CTS-CDN XRech2 Chk. Sales Inv.
- 6086255: CTS-CDN XRech2 Chk. Sales Cr.M
- 6086259: CTS-CDN XRech2 Chk. Sv. Inv.
- 6086260: CTS-CDN XRech2 Chk. Sv. Cr.M

#### Key validation rules
1. Sales Invoice:
   - Company and Customer details (City, Post Code, Name, Country/Region Code) must not be empty.
   - Ship-to Address:
     - Must include valid City and Post Code.
   - Payment Terms Code must not be empty.
   - Sales Invoice Lines:
     - Total amounts (lines and discounts) must not be negative.

2. Credit Memo, Service Sales Invoice, and Service Credit Memo:
   - Ship-to Address validation is omitted.

### OIOUBL

OIOUBL validation uses the following codeunits:
- 6086275: CTS-CDN OIOUBL Chk. Sales Inv.
- 6086276: CTS-CDN OIOUBL Chk. Sales Cr.M
- 6086284: CTS-CDN OIOUBL Chk. Sv. Inv.
- 6086285: CTS-CDN OIOUBL Chk. Sv. Cr.M

#### Key validation rules
1. Sales Invoice:
   - Company Information:
     - VAT Registration No., Name, Address, City, Post Code, and Country/Region Code must not be empty.
   - Payment Terms Code must not be empty.
   - Sales Invoice Lines:
     - Total amounts (lines and discounts) must not be negative.
   - Bill-to Customer:
     - Name, Address, Post Code, City, and Country/Region Code must be valid.
   - Sell-to Contact must not be empty.

2. Credit Memo and Service Sales Invoice:
   - Validations mirror those of the Sales Invoice.

3. Service Credit Memo:
   - Matches Service Sales Invoice validation rules.

### CII (Cross Industry Invoice)

CII does not currently have specific validation codeunits.