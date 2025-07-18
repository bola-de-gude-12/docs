You can request the addition of event publishers or have specific functions made external to support your customizations. To minimize the risk of breaking changes and ensure smoother updates in Microsoft Dynamics 365 Business Central online, most functions are internal by default.

Before submitting a request, check whether your needs are already met by existing event publishers or external functions. To do this, use the [Event Recorder tool in Business Central](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-events-discoverability) – which allows you to record and review all events published during your business processes. This helps you identify available events without manually searching through code.

If your requirements aren't covered, you may [submit a request](/Continia {param1}/Getting Started/Help and Support.md). If your request is accepted, the changes are typically included in an upcoming service pack (usually within two months).

## To request a new event

When requesting a new event, provide the following details:

- Event name
- Purpose of the event
- Exact location in the code where the event should be added (include screenshots or code snippets)
- Required parameters, along with a description of each parameter

All new events will follow Microsoft’s naming conventions.

## To request an external function

To request a function to be made external:

1. Confirm the function is currently internal by compiling your extension against the latest Continia {param1} service pack, or by reviewing the source code.
2. If the function is unavailable, submit a [submit a support ticket](/Continia {param1}/Getting Started/Help and Support.md) (or ask your partner to do so) with the following information:
   - Function name
   - Object type and number
   - Justification for making the function external
