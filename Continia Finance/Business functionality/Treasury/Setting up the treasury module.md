---

title: Treasury in Continia Finance
date: 18-10-2024
description:  Learn more about setting up the Treasury module.
id: CF-129
lang: en

---

# Setting up the Treasury Module

Continia Finance Treasury offers a cross-company view of key data, including bank balances and  open customer/vendor items. These views, which can display G/L accounts, customers, vendors, and bank accounts for selected companies, are accessible based on user permissions. Available permission sets are:

* CTS-CFI TRE, READ
* CTS-CFI TRE, SETUP
* CTS-CFI TRE, USE

> [!NOTE]
> Permission to view Treasury lists also depends on the user's permissions to view a company (group).

## Setting up Treasury Company Groups
Treasury Groups enable you to consolidate multiple Treasury companies into a single group to make it easier to track related companies. You can set up user permissions to restrict access, ensuring that only authorized users can view specific group data. For example, User A may be granted access to Group One, while User B can only access Group Two. Users with the necessary permissions will have full visibility of the Treasury data for the groups they are assigned to, ensuring both data security and efficient management.

To set up a Treasury Company Group:

1. Use the {{search}} icon, search for Treasury Company Groups, and select the related link. 
2. On the action bar, select **New**.
3. Add a Company Group Code and Name. 
4. Use the {{search}} icon, search for Treasury Companies, and navigate to the company that you want to add to the group.
5. In the **Company Group** column, select the Company Group you just created. 

## Setting up the Treasury module

To set up the module, configure the **Treasury Setup** page by selecting which companies' data to display, along with the relevant accounts and open items.

To set up the Treasury module using the assisted setup:

1. Use the {{search}} icon, enter **Assisted Setup**, and select the related link. Alternatively, select the cogwheel  icon (Settings), and then select **Assisted Setup**.
2. In the **Continia Finance** section, select **Set up Treasury**.
3. The wizard will now let you decide what companies and accounts to include.

To set up the Treasury module:

1. Use the {{search}} icon, enter Treasury Setup, and select the related link.

2. On the **Treasury Setup** page header, select the plus icon to create a new entry.

3. Enter information for the following fields:

   > [!IMPORTANT]
   >
   > To set up the Treasury module for the first time, make sure that you first select the **plus icon** located in the header of the page.

   | Field                     | Description                                                  |
   | ------------------------- | ------------------------------------------------------------ |
   | Companies                 | In the **Companies** field, you can choose:<br />**All** - the data for all companies is displayed.<br />or<br />**Selection** - if selected, you must define the companies that must be considered. On the action bar, go to **Selection** > **Company Selection** to enter the companies. Select the **Name** option in the **Type** field to enter companies individually. For a group of companies, select **Filter**. When you select the **Filter** type, you must select the criteria in the **Filter Field** field and the filter itself in the **Filter** field. For example, to select all companies that have "Eco" in the name, add \*Eco\*. |
   | G/L Accounts              | To display the balances of selected companies in the treasury list, you need to determine whether and for which G/L accounts the balances will be shown. Note that you cannot select all G/L accounts at once; you must define a specific selection. The options are: <ul><li>**Blank** - no accounts will be synchronized.</li><li>**Selection** - select the accounts using an appropriate filter.</li></ul> |
   | Bank Accounts             | Define whether and for which bank accounts the balances of the selected companies are displayed in the treasury list. You can select specific bank accounts or select all bank accounts.<br />If you chose **Selection**, go to the action bar and select **Actions** > **Account Selection** to select the bank accounts that you want to include. |
   | Customers                 | Specify if the balances of the selected companies are displayed in the treasury list and for which customer(s). The options are: <ul><li>**Blank** - no customer balances will be displayed.</li><li>**All** - displays balances for all customers.</li><li>**All Open** - displays all customers with open entries.</li><li>**Selection** - select specific customers using a filter.</li></ul> |
   | Vendors                   | Specify if the balances of the selected companies are displayed in the treasury list and for which vendor(s). The options are: <ul><li>**Blank** - no vendor balances will be displayed.</li><li>**All** - displays balances for all vendors.</li><li>**All Open** - displays only open items.</li><li>**Selection** - select specific vendors using a filter.</li></ul> |
   | Open Customer Entries     | To manage customer entries, the Treasury can display either all open items from individual customers or only the open items of specific selected accounts. Transaction data updates automatically, ensuring that any new open items are immediately reflected in the Treasury. If the **All Open** option is selected, all items are displayed without filtering; if **Selection Customer** is chosen, only items from specific accounts will be shown. |
   | Open Vendor Entries       | To manage vendor entries, the Treasury can display either all open items from individual vendors or only the open items of specific selected accounts. Transaction data updates automatically, ensuring that any new open items are immediately reflected in the Treasury. If the **All Open** option is selected, all items are displayed without filtering; if **Selection Customer** is chosen, only items from specific accounts will be shown. |
   | G/L Entries               | Determines if the G/L entries of the selected G/L accounts will be displayed in the treasury list. |
   | Starting Date G/L Entries | When you choose to add G/L entries in the Treasury list for the selected accounts, it's important to define a Starting Date for the G/L entries. If you do not select a starting date, this will cause the system to process all historical data, potentially leading to significant delays and a heavy workload. For instance, if your system begins operations in October 2000, setting the starting date at that point prevents unnecessary synchronization of older, irrelevant data.<br/><br/>**Recommendation**: set a Starting Date to avoid processing all historical entries, which can impact system performance. This targeted approach helps focus the synchronization process on only relevant, recent G/L entries. |
   | Activate Treasury         | Once you have entered all the required information on the Treasury Setup page, enable the **Activate Treasury** option to begin processing ongoing movements and updates across your Treasury companies. |
   | Display in Treasury Lists | Controls whether only the selected companies will be shown in the treasury lists. For a company's data to be included in the Treasury list, the **Display in Treasury Lists** checkbox must be selected on the **Treasury Companies** page. |
   | Activate G/L Entries      | Enabling this option ensures that Treasury items are kept up to date with continuous synchronization of General Ledger (G/L) entries. However, you must be aware that this process can take significant time, especially when there are a large number of booked entries. <br /><br />**Recommendation**: It's generally not advised to activate this option, as it can place a heavy load on system resources. However, if you are working with a smaller volume of G/L entries, activating this feature may be manageable and less likely to impact performance. |

4. After selecting the companies and setting the configurations, select **Home** > **Initialize** to initialize the selected companies for the Treasury and to transfer all master and transaction data according to the setup from the companies belonging to the Treasury network into the cross-company views. Any further movement or change on the assigned accounts will be automatically displayed in the Treasury views from this point onwards. Please note that this one-time initialization can affect the database performance during the execution of the job, depending on the extent of the booking history.

5. Go to **Lists** > **Treasury Bank Account List, Treasury G/L Account List, Treasury Account List, Treasury Open Entries, Treasury Companies** for your cross-company view of key data.
