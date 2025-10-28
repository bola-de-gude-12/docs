---
title: Einen Mastercard-Transaktions-Feed einrichten
date: 22-10-2024
description: Details zum Einrichten eines Mastercard-Transaktions-Feeds in Continia Expense Management
id: EM-280
lang: de
---

# Einen Mastercard-Transaktions-Feed einrichten

In diesem Artikel wird beschrieben, wie Sie einen Transaktions-Feed zu Continia Expense Management einrichten, damit Ihre Mastercard-Transaktionen direkt in Expense Management importiert werden können.

> [!NOTE]
> Der Transaktions-Feed muss von Ihrer Bank mithilfe der folgenden Anleitung eingerichtet werden, die einen externen Prozess von Continia beschreibt. Es ist daher möglich, dass die Anleitung nicht immer auf dem aktuellsten Stand ist, obwohl Continia grundsätzlich bestrebt ist, dies sicherzustellen.

## So richten Sie einen Transaktions-Feed für Expense Management ein

Als Benutzer von Expense Management müssen Sie sich an Ihren Bankberater wenden und anfordern, dass Ihr CDF-Feed direkt an Continia Software im Mastercard SmartData Portal gesendet wird. Weisen Sie Ihren Bankberater auf diese Anleitung hin.

Der Bankberater, der einen Mastercard-Transaktions-Feed zu Expense Management für das Unternehmen des Benutzers einrichten soll, muss die folgenden Schritte ausführen:

1. Öffnen Sie das Mastercard SmartData Portal.
2. Treffen Sie auf der Seite **Format** die folgende Auswahl:
   - Wählen Sie unter **Vendor Name** die Option **Continia Software** aus.
   - Wählen Sie unter **Application Name** die Option **Continia Expense Management** aus.

     ![Mastercard SmartData Portal interface](/images/EM/mastercard-smartdata-portal-interface.png)
3. Treffen Sie auf der Seite **Frequency** die folgende Auswahl:

   ![Frequency](/images/EM/frequency.png)
4. Treffen Sie auf der Seite **Record Selection** die folgende Auswahl:

   ![Record Selection](/images/EM/record-selection.png)
5. Wählen Sie auf der Seite **Filtering** die Option **No** aus.
6. Wählen Sie auf der Seite **Masking** aus, ob Daten wie Kreditkarten-IDs maskiert werden sollen oder nicht.
   > [!NOTE]
   > Wenn die Organisation des Benutzers die Kreditkarten-IDs maskiert, stellen Sie sicher, dass alle in der Organisation verwendeten Kreditkarten-IDs nach der Maskierung eindeutig sind.
7. Wählen Sie auf der Seite **Notifications** die Option **No** aus.
8. Führen Sie auf der Seite **Data Initialization** einen der folgenden Schritte aus:
   - Wenn historische Daten _nicht_ einbezogen werden sollen, treffen Sie die folgende Auswahl:

     ![Data Initialization, no historical data](/images/EM/data-initialization-no-historical-data.png)
   - Wenn historische Daten _einbezogen_ werden _sollen_, treffen Sie die folgende Auswahl und geben Sie das Datum der frühesten Transaktionen an, die Sie einbeziehen möchten:

     ![Data Initialization, historical data](/images/EM/data-initialization-historical-data.png)

Ihre Bank leitet die Bereitstellung des Feeds über Continia Software im Smart Data Portal von Mastercard. Sobald dies erledigt ist, sendet Ihnen die Bank eine E-Mail mit der Dateiübermittlungs-ID, zum Beispiel G0123456. Dies ist Ihre Bestätigung, dass die Einrichtung abgeschlossen wurde.

Jetzt können Sie in Expense Management eine Bankvereinbarung einrichten, um Mastercard-Transaktionen automatisch zu empfangen. Informationen hierzu finden Sie unter [Kreditkartenvereinbarungen aktivieren](@EM-32).

## Informationen zum Thema

[Mastercard-Transaktionen importieren](@EM-279)