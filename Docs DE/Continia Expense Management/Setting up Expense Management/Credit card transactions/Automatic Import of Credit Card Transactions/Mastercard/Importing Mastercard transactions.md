---
title: Mastercard-Transaktionen importieren
date: 12-11-2020
description: Details zum Importieren von Mastercard-Transaktionen in Continia Expense Management
id: EM-279
lang: de
---

# Mastercard-Transaktionen importieren

Continia unterstützt den automatischen Import von Mastercard-Transaktionen direkt in Continia Expense Management. Dies kann auf zwei Arten erfolgen:

- [Direkt von Mastercard](#transaktionen-direkt-von-mastercard-importieren) mit Mastercard Smart Data (nur für Mastercard-Firmenkarten) – die empfohlene Option
- [Von Ihrer Bank](#transaktionen-von-ihrer-bank-importieren) – für andere Kartentypen oder wenn Mastercard Smart Data nicht unterstützt wird

Weitere Informationen zu den einzelnen Optionen und zu den Voraussetzungen für die Einrichtung des automatischen Imports finden Sie in den entsprechenden Abschnitten.

## Transaktionen direkt von Mastercard importieren

Bei Mastercard-Firmenkarten können Sie Ihre Kreditkartentransaktionen mithilfe von Mastercard Smart Data direkt von Mastercard in Expense Management importieren, sofern dies verfügbar ist (siehe Hinweis unten). Hierzu muss zunächst ein Transaktions-Feed zu Expense Management eingerichtet werden. Dies wird von Ihrer Bank durchgeführt. Wenden Sie sich daher bitte an Ihren Bankberater, um dies einzurichten.

> [!TIP]
> Ihr Bankberater wird diese [Anleitung zur Einrichtung eines Mastercard-Feeds](@EM-280) wahrscheinlich nützlich finden. Wir empfehlen Ihnen dringend, diese Anleitung an Ihren Bankberater weiterzuleiten, um den Vorgang zu vereinfachen.

> [!NOTE]
> Mastercard Smart Data wird von Continia vollständig unterstützt, aber nicht von allen Banken. Um herauszufinden, ob Ihre Bank dies unterstützt, wenden Sie sich bitte an Ihren Bankberater.

## Transaktionen von Ihrer Bank importieren

Wenn Ihre Bank Mastercard Smart Data nicht unterstützt oder Ihr Unternehmen andere Kartentypen als Mastercard-Firmenkarten verwendet, können Ihre Kreditkartentransaktionen von Ihrer Bank in Expense Management importiert werden, vorausgesetzt, die Bank ist bereit und in der Lage, Transaktionen an Expense Management zu senden. Für die große Mehrheit der Banken ist dies kein Problem, aber einige Banken haben technische Einrichtungen, die gewisse Herausforderungen mit sich bringen können.

> [!IMPORTANT]
> Continia unterstützt Tausende von Szenarien und zahlreiche Banken auf der ganzen Welt. Wenn Sie sich nicht sicher sind, ob Ihre Bank Transaktionen an Expense Management senden kann, wenden Sie sich bitte an Ihre Bank und bitten Sie sie, sich an [Ihren Continia-Partner](/Continia Expense Management/Getting Started/Resellers and Partners/Find a Reseller.md) zu wenden. Ihr Continia-Partner wird dann mit Continia zusammenarbeiten, um die bestmögliche Lösung für Ihr Unternehmen zu finden.

Um Mastercard-Transaktionen von Ihrer Bank in Expense Management zu importieren, muss eine Importvereinbarung mit der Bank getroffen werden. Sobald eine Vereinbarung besteht, werden Mastercard-Transaktionen täglich automatisch in Microsoft Dynamics 365 Business Central importiert.

Der Transaktionsaustausch zwischen Ihrer Bank und Continia erfolgt über SFTP, ein weit verbreitetes Netzwerkprotokoll für die Übertragung von Dateien zwischen Clients und Servern.

## Informationen zum Thema

[Automatischer Import von Kreditkartentransaktionen](/Continia Expense Management/Setting up Expense Management/Credit card transactions/Automatic Import of Credit Card Transactions/Overview.md)  
[Finden eines Partners für Continia Expense Management](/Continia Expense Management/Getting Started/Resellers and Partners/Find a Reseller.md)  
[American Express-Transaktionen importieren](/Continia Expense Management/Setting up Expense Management/Credit card transactions/Automatic Import of Credit Card Transactions/Importing American Express transactions.md)  
[Visa-Transaktionen importieren](@EM-281)  
[Transaktionen von anderen Karten importieren](/Continia Expense Management/Setting up Expense Management/Credit card transactions/Automatic Import of Credit Card Transactions/Importing transactions from other cards.md)  
[Manueller Dateiimport](/Continia Expense Management/Setting up Expense Management/Credit card transactions/Automatic Import of Credit Card Transactions/Manual file import.md)