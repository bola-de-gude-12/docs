---
title: Understanding the CBIC and CBCC components
description: How Payment Management uses the CBIC to manage payment data communicated with the bank
date: 04-11-2021
id: PM-61
lang: en
---

# Understanding the CBIC and CBCC Components

When communicating payment information between Business Central and the bank, Payment Management uses external bank service components to manage the data conversion and transfer. The two external bank components concern the CBIC (Continia Bank Integration Component) and the CBCC (Continia Bank Communication Components), installed on Continia Online. The transfer of data between Business Central and Continia Online is processed by API calls.

The main concepts of the two service components are:

- The CBIC converts in-house formatted payment files (created in Business Central) into files that are formatted and structured after the specifications outlined by the individual banks. Vice versa, the CBIC converts the files received from the bank into in-house formatted files, making it possible to import and create the bank data in Business Central.
- When using direct communication, the CBCC sends the formatted payment files to the bank, following the specifications outlined by the individual banks. Vice versa, when a status file, a cash receipt file, or a bank account statement is available in the bank, the CBCC retrieves the file from the bank and transfers the data to Continia Online, where the CBIC will then convert the data into the in-house supported format.  



## Component maintenance

The service components (normally one component per bank) are developed with Microsoft Visual Studio against the specifications outlined by the individual banks. Any use of a component can be scaled based on the usage (monitored), and new instances can be started in case there is a change in the demand for more resources, servers, memory, etc. Using external components, Continia can at any time stop, update, or replace the component, for any reason such as changes in a bank's specifications, changes in the in-house format, and legal changes that require an update.

All Continia projects are saved in secure versioned servers with multiple backups. A full changelog of changes to the component is accessible for Continia personnel and auditors.



## Security and compliance

To ensure the highest level of security, the CBIC and CBCC components are installed on Continia Online, and can't be installed locally. In the Payment Management app edition, the connection is automatically established to the components on Continia Online, thus no installation is required (as is the case with the Payment Management FOB edition).

Data used to establish the connection between Continia Online and Business Central is logged on the Continia owned Azure SQL servers for Continia to monitor the service. The components are deployed and monitored behind secure firewalls. A built-in error-handling routine ensures that the component always handles errors and exceptions, without compromising this or other connections. Each connection is established in a complete and neutral instance, without any usage of disk or memory from other instances. Any use of the components is monitored, logged, and supervised by Continia personnel, who also have the ability to deactivate the components if this is considered necessary in the rare event that an incident is returned.

Any communication to and from the components is conducted in a safe and secure way, using encrypted data transfer, without the possibility of interference from external parties.

All data transfer that can be linked to the Business Central tenant, concerning payments, statuses, account statements, and certificates exchanged between the bank and Business Central, expire immediately after the data has been sent from Continia Online. However, data, such as the number of transactions, is collected and held anonymously (no identifying values can link the information to the participant) on Continia's Azure SQL server for Continia to monitor the service. Even though no data with direct reference to the Business Central tenant is saved in Continia Online, auditing by external companies or institutions can be made from outside Continia's network and Active Directory, if requested.



