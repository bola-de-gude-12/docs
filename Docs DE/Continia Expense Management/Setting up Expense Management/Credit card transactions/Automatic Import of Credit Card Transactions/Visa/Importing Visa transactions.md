---
title: Visa-Transaktionen importieren
date: 23-03-2021
description: Details zum Importieren von Visa-Transaktionen in Continia Expense Management
id: EM-281
lang: de
---

# Visa-Transaktionen importieren

Continia unterstützt den automatischen Import von Visa-Transaktionen direkt in Continia Expense Management. Dies kann auf zwei Arten erfolgen:

- [Direkt von Visa](#transaktionen-direkt-von-visa-importieren) (für Visa-Firmenkarten) – die empfohlene Option
- [Von Ihrer Bank](#transaktionen-von-ihrer-bank-importieren) – für andere Kartentypen oder wenn direkter Import von Visa nicht unterstützt wird

Weitere Informationen zu den einzelnen Optionen und zu den Voraussetzungen für die Einrichtung des automatischen Imports finden Sie in den entsprechenden Abschnitten.

## Transaktionen direkt von Visa importieren

Bei Visa-Firmenkarten können Sie Ihre Kreditkartentransaktionen direkt von Visa in Expense Management importieren. Hierzu muss zunächst ein Transaktions-Feed zu Expense Management eingerichtet werden. Dies wird von Ihrer Bank durchgeführt. Wenden Sie sich daher bitte an Ihren Bankberater, um dies einzurichten.

> [!TIP]
> Ihr Bankberater wird diese [Anleitung zur Einrichtung eines Visa-Feeds](@EM-282) wahrscheinlich nützlich finden. Wir empfehlen Ihnen dringend, diese Anleitung an Ihren Bankberater weiterzuleiten, um den Vorgang zu vereinfachen.

## Transaktionen von Ihrer Bank importieren

Wenn es nicht möglich ist, Transaktionen direkt von Visa zu importieren, oder wenn Ihr Unternehmen andere Kartentypen als Visa-Firmenkarten verwendet, können Ihre Kreditkartentransaktionen von Ihrer Bank in Expense Management importiert werden, vorausgesetzt, die Bank ist bereit und in der Lage, Transaktionen an Expense Management zu senden. Für die große Mehrheit der Banken ist dies kein Problem, aber einige Banken haben technische Einrichtungen, die gewisse Herausforderungen mit sich bringen können.

> [!IMPORTANT]
> Continia unterstützt Tausende von Szenarien und zahlreiche Banken auf der ganzen Welt. Wenn Sie sich nicht sicher sind, ob Ihre Bank Transaktionen an Expense Management senden kann, wenden Sie sich bitte an Ihre Bank und bitten Sie sie, sich an [Ihren Continia-Partner](/Continia Expense Management/Getting Started/Resellers and Partners/Find a Reseller.md) zu wenden. Ihr Continia-Partner wird dann mit Continia zusammenarbeiten, um die bestmögliche Lösung für Ihr Unternehmen zu finden.

Um Visa-Transaktionen von Ihrer Bank in Expense Management zu importieren, muss eine Importvereinbarung mit der Bank getroffen werden. Sobald eine Vereinbarung besteht, werden Visa-Transaktionen täglich automatisch in Microsoft Dynamics 365 Business Central importiert.

Der Transaktionsaustausch zwischen Ihrer Bank und Continia erfolgt über SFTP, ein weit verbreitetes Netzwerkprotokoll für die Übertragung von Dateien zwischen Clients und Servern.

## Informationen zum Thema

[Automatischer Import von Kreditkartentransaktionen](/Continia Expense Management/Setting up Expense Management/Credit card transactions/Automatic Import of Credit Card Transactions/Overview.md)\
[Finden eines Partners für Continia Expense Management](/Continia Expense Management/Getting Started/Resellers and Partners/Find a Reseller.md)\
[American Express-Transaktionen importieren](/Continia Expense Management/Setting up Expense Management/Credit card transactions/Automatic Import of Credit Card Transactions/Importing American Express transactions.md)\
[Mastercard-Transakionen importieren](@EM-279)\
[Transaktion von anderen Karten importieren](/Continia Expense Management/Setting up Expense Management/Credit card transactions/Automatic Import of Credit Card Transactions/Importing transactions from other cards.md)\
[Manueller Dateiimport](/Continia Expense Management/Setting up Expense Management/Credit card transactions/Automatic Import of Credit Card Transactions/Manual file import.md)
