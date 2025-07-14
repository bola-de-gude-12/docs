---
title: Installing Document Output Service
date: 04-11-2024
description:
id: DO-203
lang: en
---

# Installing Document Output Service

This guide provides step-by-step instructions to install, configure, and use the Continia Document Output Service for Microsoft Dynamics 365 Business Central (BC) On-Premises. Continia Document Output Service allows Business Central users to print documents through a local print service, ensuring efficient document handling and output.

## Prerequisites

* Access to Business Central on-premises
* Local administrator rights to install software
* Domain user credentials with "Log on as a Service" permissions

## To install Document Output Service

1. Sign into Business Central.
2. In the search field, type and select **Local Print Service Status and Setup**.
3. Download and Run the Setup File:
   - Select the download link and open the setup file (`setup.exe`).
   - If prompted, click **More Info** and then **Run Anyway** to allow installation.
4. Run the Setup Wizard and select **Next** to proceed through the setup steps.
5. When prompted to choose an installation folder, accept the default location (`C:\Program Files\Continia\Continia Document Output Service`) or specify a different folder, then select **Next**.
6. Select **Yes** to allow the app to make changes.
7. After installation, select **Close** to exit.

## To enable and configure the Continia Local Print Service

1. Open Continia Document Output Service.
2. Navigate to the installation folder (`C:\Program Files\Continia\Continia Document Output Service`) and open **Manager.exe**.
3. Select **Yes** if prompted to allow changes.
4. To enable Local Printing, check the **Enable local printing** box in the Manager application.

The default port is **9225**; ensure it remains set to **9225** unless instructed otherwise by your network administrator.

## To install the service and assign user rights

1. In the Manager application, select **Install Service**.
2. Enter your **Domain/Username** and **Password**
3. To assign **Log on as a Service** rights (if not already assigned), open **Control Panel > Administrative Tools > Local Security Policy**.
4. In the left pane, navigate to **Security Settings > Local Policies > User Rights Assignment**.
5. In the right pane, locate **Log on as a Service**, right-click, and select **Properties**.
6. Add the domain user account, then select **OK**.
7. After installation, the service will start automatically. Click **OK** to confirm.

## To start the service

1. To start Document Output Service, select **Start Service** in the Manager application.
2. Once the service starts, click **OK** to confirm.

## To configure printer settings in Business Central

1. Sign into Business Central.
2. In the search field, type and select **Printer Selection**.
3. In the **Printer Selection** window, enter the **User ID** and select a **Printer Name** for each user.
4. Optional: Set up specific printers based on **Report ID** or **Machine Name (PC)** if different printers are required for specific tasks.

## To use Document Output Service for printing

1. In Business Central, select an **Unhandled Document Task**, and choose one of the following options:<br><ol><li><b>Send All to Queue</b>, which sends all selected documents to the print queue.</li><li><b>Print PDF</b>, which prints a single document immediately.</li></ol>
2. If you selected **Send All to Queue**, navigate to **Document Queue** in the **Role Center** to manage print tasks.
3. When you use **Print PDF**, select the desired printer in the dialog box that appears and confirm to print.

## To use the “BC Print Server” service for batch printing

1. Documents sent to the print queue via **Send All to Queue** are processed by the **BC Print Server** service.

The **BC Print Server** manages batch print jobs, ensuring that queued documents print in sequence on the designated printers.

## Troubleshooting and support

If you encounter any issues:
* Confirm that the user account has "Log on as a Service" rights.
* Ensure the local print service is enabled and the default port is set to **9225**.
* For further assistance, contact your network administrator or Continia support.
