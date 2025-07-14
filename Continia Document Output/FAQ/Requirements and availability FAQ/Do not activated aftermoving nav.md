---
title: Why Is my Document Output not Activated after I Moved NAV to a New Server?
date: 24-10-2023
description: Learn more about the requirements to run DO online. 
id: DO-142
lang: en
---

# Why Is my Document Output not Activated after I Moved NAV to a New Server?
## **Question**

I moved my NAV installation to a new server, and now I get a message in Document Output saying that DO is not activated. What can I do?

## Answer

There are two possible solutions: 

### Solution 1
1. If it is a FOB installation, run the page **6192837** and mark the **Exclude DB info.from activa.** field. 
2. Restart the NAV client. 

### Solution 2

1. Open Continia Solution Management and update the database/server.

