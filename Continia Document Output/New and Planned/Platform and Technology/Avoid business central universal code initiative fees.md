---
title: Document Output Support for the Business Central Universal Code Initiative
date: 01-10-2022
description: 
id: DO-81
lang: en
---

# Support for the Business Central Universal Code Initiative

| Feature | Public preview | General availability |
| --- | :-: | :-: |
| Support for the Business Central Universal Code Initiative | - | {{checkmark}} Oct 2022 |

## Business value
It will be possible to continue to use all Document Output on-premises features without paying Universal Code fees to Microsoft.

## Feature details
Microsoft has introduced a new program called Business Central Universal Code Initiative. The program introduces increasing fees for using non-cloud-ready code over the coming years. 
In short, end users must license a new module, “Implemented code is not cloud-optimized” if they use non-cloud-optimized extensions. The module is free to license in 2022 and 2023. 
You can read more about the program and the prices [here](http://aka.ms/BCUniversalcode).

Today, we have the Continia Document Output Service handling the download of files to local storage, when operating in a cloud solution. We will start using this service in the on-premise solutions as well. This also applies for use of printer services, where the same service downloads files for local printing.
For PDF file manipulation, such as merge, sign or inserting a background image, we will be using an existing service in Continia Online (already in use in cloud solutions).

We are now in the process of rewriting the Document Output app so you can continue to use all Document Output features without paying the Universal Code fees to Microsoft. If we meet a partner requirement for local installed services without use of Continia Document Output Service, we will develop a separate Document Output on-premise app, enabling these features locally, but with the consequence that the solution will be subject to the Microsoft Universal Code fees.
