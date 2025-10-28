---
title: Upgrade Notes Concerning a Possible Add-in Conflict
date: 24-11-2021
description:  
lang: en
---

# Upgrade Notes Concerning a Possible Add-in Conflict

There is a possible add-in conflict when using Continia Document Output and Continia Document Capture – and by extension Continia Expense Management – and only upgrading one of the products.

The GdPicture14 add-in has been used in Document Capture from version 5.00 and onwards and in Document Output from the beginning.

Since Document Capture version 6.00 and Document Output version 3.00, GdPicture14 versions have been aligned in both solutions, but conflicts may occur if you're running an old version of Document Output while running an newer version of Document Capture, or vice versa.

| **Document Capture version** | **Document Output version** | **Possible conflict?** |
| --- | --- | --- |
| Before DC 5.00 | All versions | No conflict |
| DC 5.00 or DC 5.50 | All versions | Possible conflict |
| DC 6.00 or later| DO versions 3.00 or later | No conflict |
| DC 6.00 or later | DO versions before 3.00 | Possible conflict |

Since this potential conflict was discovered in January 2020, it's been ensured that releases from this point on use the same version of the GdPicture14 add-in. 

The best solution to avoid any issues is to run versions of both solutions released after January 2020, but preferably the latest releases.

In cases where only one of the solutions is upgraded, and there is a conflict, an error message will be displayed in Business Central prompting you to update a specific dll file to the latest version.

## A hotfix if you decide not to upgrade one of the solutions

To implement the hotfix, follow these steps:

1. Stop the service tier(s).
2. Delete all temp assemblies on the server (normally found here: C:\Users\[SERVICETIERUSER]\AppData\Local\Temp\Microsoft Dynamics NAV\Add-Ins\14.0.29530.0).
3. Install DC server components (if not already done).
4. Copy the following files from the Document Output add-in folder (C:\Program Files\Microsoft Dynamics 365 Business Central\140\Service\Add-ins\Document Output).
- GdPicture.NET.14.dll
- GdPicture.NET.14.filters.64.dll
- GdPicture.NET.14.image.gdimgplug.64.dll
- GdPicture.NET.14.filters.dll
- GdPicture.NET.14.image.gdimgplug.dll
5. Paste the files into the Document Capture add-in folder (C:\Program Files\Microsoft Dynamics 365 Business Central\140\Service\Add-ins\Document Capture), replacing the existing files with the same name. 
6. Start the service tier(s).

