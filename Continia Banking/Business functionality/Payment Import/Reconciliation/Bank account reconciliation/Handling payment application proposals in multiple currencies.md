# Handling payment application proposals in multiple currencies 

Multi-currency payments enable businesses to accept and manage transactions in various currencies. This feature is particularly beneficial for companies with international customers. For instance, if your business sells software online, a customer in Germany can pay in euros, while a customer in Australia can pay in Australian dollars, making the purchasing process more convenient for both parties. 

The posting of a payment to a bank account is directly tied to the bank account's designated currency code.

## Payments to LCY bank accounts

Payments to an LCY bank account can be made in any currency. You can transfer funds to a local currency (LCY) bank account in any currency. The bank will convert the incoming foreign currency to the account's local currency based on the current exchange rate. So, you can send USD to a Euro-denominated account, and it will convert to euros.

When it comes to applying payments to invoices, the process is a bit more regulated. The ability to apply currencies to invoices is controlled by the settings of the **Application between Currencies** field in the **Sales & Receivables Setup** and **Purchases & Payables Setup**. 

The **Application between Currencies** field determines which currencies are allowed when matching payments to invoices:  

- **None** - all entries involved in one application must be in the same currency.
- **EMU** - you can apply entries in euro and one of the old national currencies (currencies of the countries that are part of the European Union).
- **All** - the entries can be in any currency.

Continia Banking considers the limitations to the postings, but can match and apply invoices in different currencies from every kind of bank account.

## FCY bank accounts

A payment to a FCY bank account can only be made in the currency linked to the bank account. If the payment is to apply to an invoice, the invoice currencies are limited to the set up in the **Sales & Receivables** field. **Application between currencies** field as well.

## Handling multiple currencies in Continia Banking

In Banking, handling multiple currencies is straightforward and requires no extra setup. The system uses standard settings from **Sales & Receivables Setup** and **Purchases & Payables Setup**.

When handling entries, the currency of the bank account is used. Payments to an LCY account can be in any currency, while entries in both LCY and FCY can be processed. For FCY bank accounts, entries in LCY, the same FCY, or different FCY can be processed.

When reconciling, if there's a rounding difference, an additional journal line is created using the appropriate G/L account from the customer's or vendor's posting group.

For example, if you have a GBP bank account (local currency) and receive a payment for a EUR invoice, the system matches the payment to the invoice and handles any rounding differences by creating necessary journal lines.

All payments to bank account ledger entries are posted in the currency of the bank account.