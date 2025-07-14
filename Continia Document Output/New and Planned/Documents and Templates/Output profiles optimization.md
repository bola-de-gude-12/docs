---
title: Output Profiles Optimization
date: 22-09-2023
description: 
id: DO-85
lang: en
---

# Output Profiles Optimization

| Feature | Public preview | General availability |
| --- | :-: | :-: |
| Output Profiles optimization | - | {{checkmark}} Sep 2023 |

## Business value

Document Output supports both email distribution and electronic transmission in compatible formats. All of this is easily managed through Output profiles attached to individual customer cards. With an expanded range of prebuilt output profiles, we are committed to delivering complete empowerment for efficient document distribution.

## Feature details

We have introduced an Output Profile entity for every document type that is supported, as well as a default type. This will allow emails to be sent when an e-document is not possible or not supported by the XML format.
Additionally, we are implementing a standard Document Output setup field that will enable an Output profile to be configured on a customer, for documents to be sent also as emails. The upgraded Document Output will continue to function as before unless this new feature is enabled. This will eliminate the need for a SKIP profile to be set on customers.

You can read more about Output Profiles in the business functionality article [Output Profiles](@DO-74).