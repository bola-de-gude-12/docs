---
title: Zahlungsmittel in eDocuments verwenden
date: 15-10-2025
description: So konfigurieren Sie Zahlungsmittel auf Bankkonten-, Mandanten- und Debitorenebene.
id: DC-450
lang: de
---

# Zahlungsmittel in eDocuments verwenden

Mit der Zahlungsmittel-Funktion können Sie Zahlungsformen beim Senden von eDokumenten wie Rechnungen oder Gutschriften aus Microsoft Dynamics 365 Business Central definieren.

Dieser Artikel führt Sie durch den Prozess der Konfiguration von Zahlungsmitteln auf Bankkonten-, Mandanten- und Debitorenebene.

## Standardkonfiguration verwenden

Standardmäßig wird die Konfiguration der Zahlungsmittel von der Seite **Firmendaten** übernommen. Das heißt, sofern keine Änderungen an der **eDocuments Zahlungsmittel Einrichtung** vorgenommen werden (und diese auf der gewünschten Ebene, z. B. Debitor oder Bankkonto, angewendet werden), enthält der Abschnitt für Zahlungsmittel in Ihren elektronischen Dokumenten die folgenden Werte:

- **Zahlungsmittelcode**: 42, d. h. Zahlung auf Bankkonto.
- **Zahlungsart**: Bank.

In diesem Fall müssen zwei Werte angegeben werden: **Bankkontonummer** und **BLZ**. Wenn das Feld **Bankkontocode des Mandanten** auf der Rechnung oder Gutschrift leer ist, werden diese Werte aus den Firmendaten übernommen. Andernfalls werden sie vom angegebenen Bankkonto übernommen (z. B.: CHECKING).

Darüber hinaus generiert das Standardzahlungsmittel keine Zahlungs-ID. Wenn dies erforderlich ist oder andere Werte als die Werte auf der Seite **Firmendaten** verwendet werden sollen, konfigurieren Sie die Zahlungsmittel wie unter [Benutzerdefinierte Zahlungsmitteleinrichtungen konfigurieren](#benutzerdefinierte-zahlungsmitteleinrichtungen-konfigurieren) beschrieben.

> [!IMPORTANT]
> Wenn bei einem Zahlungsmittel die **Zahlungsart** auf **Bank** eingestellt ist, können die **Bankkontonummer** und die **BLZ** in der **Zahlungsmittel Einrichtung** nicht angepasst werden.

## Benutzerdefinierte Zahlungsmitteleinrichtungen konfigurieren

Es ist möglich, benutzerdefinierte Zahlungsmitteleinrichtungen für Bankkonten, Mandanten und Debitoren zu konfigurieren. Beginnen Sie dazu mit der Erstellung einer Standardeinrichtung.

1. Suchen Sie ({{search}}) nach **eDocuments Zahlungsmittel Einrichtung** und wählen Sie dann den entsprechenden Link aus.
2. Klicken Sie auf der Seite **eDocuments Zahlungsmittel Einrichtung** in der Aktionsleiste auf **Neu**.
3. Geben Sie auf dem Inforegister **Allgemein** die folgenden Details ein:
   - **Code**: der Code, der das eingerichtete Zahlungsmittel identifiziert. Zum Beispiel: FIK73.
   - **Beschreibung**: der Text, der die Einrichtung der Zahlungsform beschreibt. Zum Beispiel: FIK 73.
   - **Zahlungsmittel**: das gewünschte Zahlungsmittel, ausgewählt aus der Tabelle **eDocuments Zahlungsmittel**. Abhängig vom gewählten Zahlungsmittel müssen Sie möglicherweise weitere Felder ausfüllen. Weitere Informationen finden Sie unter [Zahlungsmittel verwalten und erstellen](#zahlungsmittel-verwalten-und-erstellen).

Dadurch wird eine Konfiguration in der **eDocuments Zahlungsmittel Einrichtung** erstellt. Wie die Standardkonfiguration verwenden auch neue Konfigurationen die **Bankkontonummer** und **BLZ** von der Seite **Firmendaten**.

## Benutzerdefinierte Zahlungsmitteleinrichtungen anwenden

Benutzerdefinierte Zahlungsmitteleinrichtungen können auf Mandanten-, Bankkonten- oder Debitorenebene vorgenommen werden.

> [!NOTE]
> Wenn für Ihren Mandanten, Ihr Bankkonto und Ihren Debitor eine Zahlungsmitteleinrichtung konfiguriert ist, wird die detaillierteste Einrichtung verwendet. Das heißt, das Zahlungsmittel für den Debitor hat Vorrang vor dem Zahlungsmittel für das Bankkonto, welches wiederum Vorrang vor dem Zahlungsmittel für den Mandanten hat.

### Mandant

So wenden Sie eine benutzerdefinierte Zahlungsmitteleinrichtung auf einen Mandanten an:

1. Suchen Sie {{search}} nach **Firmendaten** und wählen Sie dann den entsprechenden Link aus.

2. Klicken Sie auf der Seite **Firmendaten** im Inforegister **Zahlungen** auf die drei Punkte neben dem Feld **Zahlungsmittel Einrichtung**.

3. Wählen Sie die gewünschte Zahlungsmitteleinrichtung aus.

Das ausgewählte Zahlungsmittel wird jetzt als Standard verwendet, wenn das Feld **Bankkontocode des Mandanten** auf der Rechnung oder Gutschrift leer ist.

> [!NOTE]
> Pro Mandant kann nur eine Konfiguration erstellt werden.

### Bankkonto

So wenden Sie eine benutzerdefinierte Zahlungsmitteleinrichtung auf ein Bankkonto an:

1. Suchen Sie {{search}} nach **Bankkonten** und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie auf der Seite **Bankkonten** das gewünschte Bankkonto aus.
3. Klicken Sie auf der **Bankkontokarte** im Inforegister **Allgemein** auf die drei Punkte neben dem Feld **Zahlungsmittel Einrichtung**.
4. Wählen Sie die gewünschte Zahlungsmitteleinrichtung aus.

Wenn Sie im Feld **Bankkontocode des Mandanten** einer elektronischen Rechnung oder Gutschrift dieses Bankkonto auswählen, wird das damit verknüpfte Zahlungsmittel verwendet.

> [!NOTE]
> Pro Bankkonto kann nur eine Konfiguration erstellt werden.

### Debitor

So wenden Sie eine benutzerdefinierte Zahlungsmitteleinrichtung auf einen Debitor an:

1. Suchen Sie ({{search}}) nach **Debitoren** und wählen Sie den entsprechenden Link aus.
2. Wählen Sie auf der Seite **Debitoren** den gewünschten Debitor aus. Beachten Sie, dass dieser Debitor eDokumente empfangen können muss.
3. Klicken Sie auf der **Debitorenkarte** im Inforegister **eDokumente** auf die drei Punkte neben dem Feld **Zahlungsmittel Einrichtung**.
4. Wählen Sie die gewünschte Zahlungsmitteleinrichtung aus.

Beim Versand von Rechnungen und Gutschriften an diesen Debitor wird das ihm zugeordnete Zahlungsmittel verwendet.

> [!NOTE]
> Pro Debitor kann nur eine Konfiguration erstellt werden.

## Zahlungsmittel verwalten und erstellen

Wenn Sie Konfigurationsdateien von Continia Online importieren, stehen mehrere Zahlungsmittel zur Verfügung. Diese Zahlungsmittel sind vorkonfiguriert und sofort einsatzbereit und decken die gängigsten Optionen ab.

Es besteht jedoch auch die Möglichkeit, ein Zahlungsmittel zu erstellen. Gehen Sie dazu wie folgt vor:

1. Suchen Sie ({{search}}) nach **eDocuments Zahlungsmittel** und wählen Sie dann den entsprechenden Link aus.
2. Klicken Sie auf der Seite **eDocuments Zahlungsmittel** in der Aktionsleiste **Neu** aus.
3. Geben Sie die folgenden Details ein:
   - **Code**: der Code, der das eingerichtete Zahlungsmittel identifiziert.
   - **Beschreibung**: der Text, der die Zahlungsmethode beschreibt.
   - **Typ**: die Art des Zahlungsmittels, ausgewählt aus der Dropdown-Liste.
   - **Zahlungsmittelcode**: der Zahlungsmittelcode, der dem UNCL4461-Standard entspricht. Weitere Informationen finden Sie unter [Payment Means Code (UNCL4461)](https://docs.peppol.eu/poacc/billing/3.0/codelist/UNCL4461/) (Peppol-Liste).