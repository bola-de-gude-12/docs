---
title: Expense Management Requesting Events and External Functions
date: 28-03-2022
description: How to request external functionality and new events that are currently missing
id: EM-169
lang: en
---

# Requesting Events and External Functions

Continia Expense Management offers customization options through event publishers and external function invocation. While most functions are internal, they can be made external upon request. Users can ask for additional events or external functions, which, if accepted, will be included in future service packs, typically within two months. This approach balances cloud update ease and Business Central's sensitivity to breaking changes, ensuring flexibility and faster app updates. 

## To request a new event

Before contacting the Continia support team regarding new events, please check the list of published events to see if there is an event that fulfills your requirements. If an appropriate event exists, you can utilize that event without needing to reach out for support.

However, if the event you need is not listed, please [contact us](/Continia Expense Management/Getting Started/Help and Support.md) with the following information for our evaluation:

* Event name
* Event purpose
* Location in the code where the event should be raised (preferably with a screen dump or code snippet)
* Relevant event-publisher parameters
* Parameter description

> [!NOTE]
>
> For any new event publisher created and added to Expense Management, Continia will use the same naming structure as the one used by Microsoft.

## To request an external function

Before requesting to make a function external, please ensure that the function is currently internal by downloading the latest service pack and compiling your Expense Management extension against it. If the function is confirmed to be unavailable, request your partner to create a Zendesk ticket. 

To request making a function external in Expense Management:

* Request your partner to create a Zendesk ticket with the following information:
  * The function's name, object type, and number.
  * The reason for wanting to make it external.

Continia will review your request, and if approved, the function will be made external in an upcoming Expense Management service pack.

## See also

[Overview of Event Publishers](@DC-91)  
[Resources for Help and Support](@DC-14)  
[Accessing the Source Code](Accessing the source code.md)  