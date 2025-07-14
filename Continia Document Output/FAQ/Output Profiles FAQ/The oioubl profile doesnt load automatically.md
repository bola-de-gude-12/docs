---
title: The OIOUBL Profile Doesn't Load Automatically, Why?
date: 05-12-2023
description: Document Output comes with all available templates from all regions. 
id: DO-155
lang: en
---

# The OIOUBL Profile Doesn't Load Automatically, Why?

## Question

After having run a full setup using the Document Output assisted setup guide, I go to the e-document setup menu and can see that the OIOUBL profile is missing. Why?		


## Answer

You can view it with the code displayed below. If it is not 'DK', then OIOUBL will not be automatically loaded.

```
0 references | 0% Coverage
Local procedure TestProcedure()
var
	EnvironmentInfo: Codeunit "Environment Information";
begin
	Message(EnvironmentInfo.GetApplicationFamily())
end;
```

Where to apply it?

If you use an on-premises installation, you can use powershell to set Application Family. See example 3 in this Microsoft article: [Set-NAVApplication](https://learn.microsoft.com/en-us/powershell/module/microsoft.dynamics.nav.management/set-navapplication?view=businesscentral-ps-22) (external link).
