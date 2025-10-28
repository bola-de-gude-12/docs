---
title: Setting Up Field Dependencies
date: 04-04-2025
description:  
id: EM-250
lang: en
---

# Setting up Field Dependencies

To ensure a seamless and meaningful user experience, the Continia Expense App and the Continia Expense Portal allow for setting up constraints between different fields. These constraints, known as field dependencies, consist of conditions and expectations. 

By defining specific conditions, corresponding expectations are enforced. For example, if the dimension 'DEPARTMENT' is set to the condition 'SALES', the user will be prompted to specify a value for the expectation, which is the 'PROJECT' dimension.

> [!IMPORTANT]
>
> Field dependencies apply across all document types: expense reports, expenses, mileages, and per diems.

There are two types of field dependencies:

- **System field dependencies** - Expense Management automatically calculates these based on your setup. For example, if you set a dimension as mandatory for a specific expense type, this generates a corresponding system field dependency that makes this dimension mandatory if that expense type is used.
- **User-defined field dependencies** -  these are dependencies that you can freely configure to enforce rules and expectations when you create expense documents.

<iframe src="https://player.vimeo.com/video/969169181?h=d28a2efaa6&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" width="560" height="315" frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write" title="8 Manage daily admin_Field dependencies"></iframe>

## Adding a field dependency

You can choose field types from the following Field types table to create a system field dependency or a user-defined field dependency that you create yourself.

To set up field dependencies:

1. Select the {{search}} icon, enter **Field Type Dependencies**, then select the related link.
2. On the action bar, select **New**.
3. Fill out all the required fields:

   | Field                     | Description                                                  |
   | ------------------------- | ------------------------------------------------------------ |
   | Field type code           | Specify the expense type. You can select one from the list or select **New** to [add a custom type](@EM-80). |
   | Condition                 | The options are:<ul><li>Has a specific value: you can only use this option for the Field type codes of the data type *Option* or *Code*.</li><li>Has any value</li></ul> |
   | Value                     | Specify the value if the condition is set to *Has a specific value*. For example, if the Field type code is set to *Expense type*, and the condition is set to *Has a specific value*, in the **Value** column, you can select *Hardware*. |
   | Reference field type code | Specify the field type by selecting from a list.             |
   | Expectation               | The options are:<br /><ul><li>Must have value</li><li>Must have a specific value: you can only use this option for Field type codes of the data type *Code* or *Text*.</li><li>Must have no value</li></ul> |
   | Expected value            | If the dependency entails a possible value outcome; it will be posted here. |
   | System created            | Selected when the dependency was created automatically.      |
   | Disabled                  | Specifies whether the dependency is disabled. This happens automatically when a conflict is detected. |
   | Detected conflicts        | If the dependency is disabled, this field states the reason why. |


4. On the action bar, select **Consistency Check** to enable this rule.
5. On the action bar, select **Force Synchronization with Continia Online** and the rule will be pushed to associated mobile devices.

> [!NOTE]
> The field dependency is only active if the field type and reference field type codes are **Configured Fields**.

## Updating system dependencies

System field dependencies are determined whenever you select **Update System Dependencies**. All resulting rules will be added to the Field Type Dependencies page. If any conflicts are detected in a field, a message displays, and the conflicting rules are disabled. When you select **Update System Dependencies**, a consistency check performs automatically, which reevaluates conditions.

The list of system field dependencies is calculated and updated periodically but you can also update it manually to reflect the latest setup changes in your company. When you update system field dependencies, they're created automatically on the Field Type Dependencies page, but you will always have to activate them manually, giving you complete control.

To calculate and update system field dependencies:
1. Choose the {{search}} icon, enter **Field Dependencies**, then choose the related link.
2. On the action bar, select **Update System Dependencies**.

Expense Management determines the system field dependencies based on the following:
- Expense type with attendees required
- Default dimensions

> [!NOTE]
> If you upgrade from versions older than Expense Management 7.0 and you’re used to Expense Management calculating field dependencies automatically, this no longer takes place as conflicts may occur. All conflicts must be resolved. 

## Running a consistency check

When adding a new field dependency, you’ll notice that the dependency is disabled, and there's a message displayed, “Run the Consistency Check action to enable this dependency.”

The consistency check helps you configure dependencies correctly, detect if rules have no use or are in conflict with one another, check for rule consistency and potential conflicts, and provide suggestions for solving any issues.

To run a consistency check:

* On the action bar, select **Consistency Check** and Update System Dependencies to start the consistency check automatically.