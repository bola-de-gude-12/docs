---
title: Assign per diems to projects by destination
date: 30-09-2025
description: Expense users can assign per diems to projects by destination
id: EM-331
lang: en
---

# Assign per diems to projects by destination

| Feature | General availability | Public preview |
| --- | :-: | :-: |
| Assign per diems to projects by destination | {{checkmark}} Oct 2025 | {{checkmark}} Sept 2025 |

## Business value
This feature enhances project cost management by allowing users to select project information for each individual destination within a per diem. Having a highly granular and accurate allocation of travel costs is particularly valuable for companies that manage complex, multi-leg trips and require precise budget tracking on a project-by-project basis. Overall, this capability ensures a smoother workflow and greater operational efficiency for the most detailed expense allocation scenarios.

## Feature details
This update introduces **Project** and **Task** fields to per diem destinations, allowing for a more detailed cost allocation.

- Project and Task fields - The two new fields for "Project" and "Task" have been added to the destination lines of a per diem. These fields are also available in the Expense Portal and the Expense Mobile App.
- Inheritance of project data - When you create a new per diem, the project and task details from the header are automatically inherited by the destination lines. However, you have the flexibility to change the project and task on individual destination lines.
- Posting logic:
  - If multiple destinations aren't enabled, the project and task specified in the per diem header will be used for posting.
  - If multiple destinations are used, the system will post expenses based on the project and task assigned to each specific leg of the trip.
  - For scenarios with two or more destinations on the same day with different projects, a separate job journal line will be created for each destination. Each line will be posted with the full daily rate, as the rate is determined by the final destination of that day.
- Configuration - You can add the new **Project** and **Task** fields to the view in Business Central using **Configured Fields**.
- Partner extensibility - An event has been included to allow partners to customize the posted amount for each project, offering greater flexibility.

For more information, see [Using projects and project task numbers](@EM-170)
