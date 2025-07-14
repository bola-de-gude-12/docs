---
title: Calculating due dates with payment days
date: 11-03-2025
description:
id: DC-229
lang: en
---

# Calculating due dates with Payment Days

This article describes the **Payment Days** feature, which can be used to calculate the due date of purchase and sales documents.

In Spain, the process around vendor payments often involves a fixed payment day which differs from the payment term stated in the transaction. These payment days can be configured on the company level or on the vendor card.

>[!NOTE]
>This feature is only available in the Spanish (ES) localization of Microsoft Dynamics 365 Business Central.

When configured, payments days are included in the calculation of the due date – along with the vendor's payment terms, if applicable. For example:

| Invoice date | Due date | Payment days | Without payment days configured | With payment days configured |
| ------------ | -------- | ------------ | ------------------------------- | ---------------------------- |
| 01/02/2025   | 60D      | 25D          | 01/04/2025                      | 25/04/2025                   |

>[!NOTE]
>For payment days to be taken into account when evaluating the recognized due date, you need to enable the **Show Default Field Value** setting on the **Document Category Card**. For more information, see [Capturing Header Fields in a Document](@DC-110).

## To configure Payment Days on the company level 

1. Choose the {{search}} icon, enter **Información Empresa**, and then choose the related link.
2. On the action bar, click **Relacionado** > **Pagos** > **Días pago**.
3. Enter a valid day of the month under the **Día del mes** column.
4. **Optional:** To add more than one payment day, select **Nuevo** and enter another valid day of the month under the **Día del mes** column.

## To configure Payment Days on the vendor level 

1. Choose the {{search}} icon, enter **Proveedores**, and then choose the related link.
2. Select the desired vendor.
3. On the action bar, click **Relacionado** > **Proveedor** > **Días pago**.
4. Enter a valid day of the month under the **Día del mes** column.
5. **Optional:** To add more than one payment day, select **Nuevo** and enter another valid day of the month under the **Día del mes** column.

>[!NOTE]
>Payment days configured on the vendor level override the same setting configured on the company level. For example, if you entered 25 on the company level and 18 on the vendor level, the value used in due date calculations for this vendor is 18.