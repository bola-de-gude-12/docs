If you want to upgrade Microsoft Dynamics 365 Business Central on-premises but *not* Continia {param1}, you must uninstall and unpublish all Continia apps before you install the Business Central upgrade. This applies to both major and minor (cumulative) upgrades. 

The reason is that Continia apps are distributed as runtime packages, which are guaranteed to work only if they're published to a platform with the same version as the one they were created on. Continia distributes apps as runtime packages because any extension in a runtime package – in this case the Continia {param1} app – can be installed on servers that don't have a developer license. For more information, see [this Microsoft article](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-creating-runtime-packages).

> [!NOTE] If you upgrade Business Central and Continia {param1} at the same time, you can upgrade the apps in the order you prefer.

Note that Continia releases code for all available cumulative updates (CUs) for Business Central whenever a version of Continia {param1} is released (applies to both major versions and service packs). Each newly released CU from Microsoft is only supported as of the next service pack released by Continia. If you need to upgrade to a currently unsupported Business Central CU – the latest one, for example – and can't wait until Continia has released a service pack that supports this, please reach out to the Continia support team by creating a support ticket. Continia will then provide you with a fully functional package that supports the relevant Business Central CU.

## Manage Continia {param1} before upgrading Business Central

Before you upgrade Business Central on-premises, you must uninstall Continia {param1} and unpublish it, and you *must* do it in the order described in the table below.

When you've uninstalled and unpublished the product and upgraded Business Central, you must republish and reinstall it – both in the order described in the table below.

> [!IMPORTANT] 
> Avoid running the [Repair-NAVApp cmdlet](https://docs.microsoft.com/en-us/powershell/module/microsoft.dynamics.nav.apps.management/repair-navapp?view=businesscentral-ps-19). The Continia apps are precompiled, and running this cmdlet will return an error due to their distribution as runtime packages.