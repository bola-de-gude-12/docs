---
title: Expense Management Upgrading to Business Central April 2019 (v14)
date: 28-03-2025
description:  
lang: en
---

# Upgrading to Business Central April 2019 (v14, FOB-based)

The following table provides an overview of what you have to do if you have Continia Expense Management (EM) installed and want to update your old version of Microsoft Dynamics NAV/Business Central (BC) to Business Central April 2019 (v14, FOB-based). Follow the guidelines in the **Tasks** column below to ensure Expense Management remains fully functional and compatible with your updated version of Business Central.

| Scenario | Tasks |
| --- | --- |
| Full upgrade from one of the following versions: <ul><li>Microsoft Navision NAV 3.70</li><li>Microsoft Dynamics NAV 4.0</li><li>Microsoft Dynamics NAV 4.0 SP1</li><li>Microsoft Dynamics NAV 4.0 SP2</li><li>Microsoft Dynamics NAV 4.0 SP3</li><li>Microsoft Dynamics NAV 5.0</li><li>Microsoft Dynamics NAV 5.0 SP1</li><li>Microsoft Dynamics NAV 2009</li><li>Microsoft Dynamics NAV 2009 SP1</li><li>Microsoft Dynamics NAV 2009 R2</li></ul> | From these versions, you must do as follows to upgrade: <ol><li>Upgrade Expense Management to the latest version. Use <a href="/continia-expense-management/development-and-administration/on-premises/upgrade/expense-management-2021-r1">this table</a> to determine how to upgrade from your particular version of Expense Management.</li><li>Upgrade to NAV 2013 or NAV 2015 using <a href="https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/upgrade/upgrading-to-business-central-on-premises">this Microsoft guide</a> (see the third row in the table). We recommend upgrading to NAV 2015.</li><li>From NAV 2013 or NAV 2015, upgrade to Business Central v14 (FOB-based) using the approach described further below in the table under "Microsoft Dynamics NAV 2013, Microsoft Dynamics NAV 2013 R2, Microsoft Dynamics NAV 2015".</li></ol> |
| Full upgrade from one of the following versions: <ul><li>Microsoft Dynamics NAV 2013</li><li>Microsoft Dynamics NAV 2013 R2</li><li>Microsoft Dynamics NAV 2015</li></ul> | From these versions, you must do as follows to upgrade: <ol><li>Upgrade Expense Management to the latest version (unless you've already done so coming from an earlier Business Central version). Use <a href="/continia-expense-management/development-and-administration/on-premises/upgrade/expense-management-2021-r1">this table</a> to determine how to upgrade from your particular version of Expense Management.</li><li>Complete the tasks described in <a href="https://continia.zendesk.com/hc/en-us/articles/360000872980-Upgrading-NAV-2013-2013-R2-or-2015-to-NAV-2016-and-above-with-Expense-Management-5-00">this guide</a> to prepare to upgrade your pre-workflow version of NAV (2013, 2013 R2, or 2015) to a workflow-enabled version (NAV 2016 and later). Note that these tasks must be carried out after the technical upgrade of NAV but before running the data conversion.</li><li>Upgrade to BC v14 (FOB-based) using <a href="https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/upgrade/upgrading-to-business-central-on-premises">this Microsoft guide</a>.</li></ol> |
| Full upgrade from one of the following versions: <ul><li>Microsoft Dynamics NAV 2016</li><li>Microsoft Dynamics NAV 2017</li><li>Microsoft Dynamics NAV 2018</li><li>Business Central October 2018 (v13)</li></ul> | From these versions, you must do as follows to upgrade: <ol><li>Upgrade Expense Management to the latest version (unless you've already done so coming from an earlier Business Central version). Use <a href="/continia-expense-management/development-and-administration/on-premises/upgrade/expense-management-2021-r1">this table</a> to determine how to upgrade from your particular version of Expense Management.</li><li>Upgrade to BC v14 (FOB-based) using <a href="https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/upgrade/upgrading-to-business-central-on-premises">this Microsoft guide</a>.</li></ol> |

## Related information
[Upgrading to Continia Expense Management 2021 R1 (7.00)](/Continia Expense Management/Development and Administration/On-Premises/Upgrade/Expense Management 2021 R1.md)  



<style>
  .content table tr td:nth-child(1) {
    width: 230px;
  }
  .content table tr td:nth-child(2) {
    width: 500px;
  }  
</style>