---
title: Einkaufsverträge basierend auf der Rechnungshistorie in Document Capture erstellen
date: 23-07-2025
description: So erstellen Sie Einkaufsverträge auf Grundlage der Rechnungshistorie.
id: DC-163
lang: de
---

# Einkaufsverträge basierend auf der Rechnungshistorie erstellen

Mithilfe künstlicher Intelligenz (KI) kann das Einkaufsverträge-Modul Muster in Ihren Eingangsrechnungen erkennen und ermitteln, ob diese wiederkehrend sind und sich für die automatische Verwaltung mit einem Einkaufsvertrag eignen. Wenn dies der Fall ist, erhalten Sie oben in Ihrem Belegjournal eine Benachrichtigung, die Ihnen empfiehlt, diese und ähnliche Rechnungen in Zukunft automatisch vom Einkaufsverträge-Modul verwalten zu lassen.

Die Benachrichtigungen sind auf Ihre jeweilige Situation zugeschnitten und enthalten unterschiedliche Informationen, je nachdem, ob Sie das Einkaufsverträge-Modul bereits aktiviert haben. Dies gilt auch für die verschiedenen Benutzeraktionen, die Sie über die Benachrichtigung aufrufen können:

- [Verfügbare Aktionen, wenn das Einkaufsverträge-Modul aktiviert ist](#mit-aktiviertem-einkaufsvertrage-modul)
- [Verfügbare Aktionen, wenn das Einkaufsverträge-Modul nicht aktiviert ist](#mit-deaktiviertem-einkaufsvertrage-modul)

Wenn Sie eine der in der Benachrichtigung vorgeschlagenen Aktionen auswählen, werden Sie durch den Vorgang geführt – wie in den folgenden Abschnitten beschrieben.

Das Modul schlägt Ihnen automatisch einen oder mehrere Einkaufsverträge auf Basis der Daten in den identifizierten, wiederkehrenden Rechnungen vor. Sie können dann sofort einen Einkaufsvertrag anhand der Vorschläge des Moduls und der automatisch ausgefüllten Daten erstellen, sofern Sie das Modul bereits aktiviert haben. Alternativ können Sie eine Übersicht aller möglichen Einkaufsverträge öffnen, die vom Modul identifiziert wurden und diese überprüfen.

> [!NOTE]
> Diese Funktion ist derzeit nur für Online-Versionen von Continia Document Capture verfügbar.

## Mit aktiviertem Einkaufsverträge-Modul

Wenn Sie das Einkaufsverträge-Modul beim Erkennen möglicher wiederkehrender Rechnungen bereits aktiviert haben, wird oben im Belegjournal die folgende Benachrichtigung angezeigt:

![Module activated](/images/DC/PurchaseContracts/module-activated.png)

In dieser Benachrichtigung stehen Ihnen die folgenden Aktionen zur Verfügung:

<br>

| Aktion                           | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| -------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Erstelle Einkaufsvertrag**     | Öffnet [die Seite **Erstelle Einkaufsvertrag**](#die-seite-erstelle-einkaufsvertrag), auf der Sie einen Einkaufsvertrag erstellen können.                                                                                                                                                                                                                                                                                                                             |
| **Ähnliche Rechnungen anzeigen** | Öffnet [die Liste **Vorgeschlagene Einkaufsverträge**](#die-liste-vorgeschlagene-einkaufsvertrage).                                                                                                                                                                                                                                                                                                                                                                   |
| **Nicht mehr anzeigen**          | Zeigt eine Meldung an, in der Sie auswählen können, wie die Benachrichtigung deaktiviert werden kann: <ul><li>**Nicht mehr nach dieser Rechnung fragen**: Deaktiviert diese Benachrichtigung für den Benutzer und für diese bestimmte Belegvorlage.</li><li>**Diese Benachrichtigung nicht mehr anzeigen**: Deaktiviert diese Benachrichtigung für den Benutzer und für alle Belegvorlagen.</li></ul> |

### Die Seite „Erstelle Einkaufsvertrag“

Auf der Seite **Erstelle Einkaufsvertrag** können Sie einen Einkaufsvertrag erstellen. Wenn Sie die Seite aus der Benachrichtigung oben im Belegjournal oder von [der Seite **Vorgeschlagene Einkaufsverträge**](#die-liste-vorgeschlagene-einkaufsvertrage) öffnen, versucht das Einkaufsverträge-Modul so viele Felder wie möglich auszufüllen, zum Beispiel die Felder **Beschreibung**, **Einkäufercode** und **Abrechnungszeit-Code**. Dies basiert auf Daten von den Rechnungen, die [als wiederkehrend und zusammengehörig identifiziert wurden und entsprechend gruppiert sind](#funktionsweise-und-kriterien).

Um einen Einkaufsvertrag zu erstellen, aktualisieren Sie falls erforderlich den Text/die Werte der automatisch ausgefüllten Felder, füllen Sie alle verbleibenden Felder nach Bedarf aus und wählen Sie dann **OK**, wenn Sie fertig sind. Dadurch wird der neue Vertrag erstellt und der Liste der Verträge auf der Seite **Einkaufsverträge** hinzugefügt. Wenn Sie auf der Seite **Einkaufsvertrag erstellen** die Option **Einkaufsvertrag öffnen** aktiviert haben, wird der neue Vertrag geöffnet, sobald Sie **OK** auswählen.

## Mit deaktiviertem Einkaufsverträge-Modul

Wenn Sie das Einkaufsverträge-Modul beim Erkennen möglicher wiederkehrender Rechnungen nicht aktiviert haben, wird oben im Belegjournal die folgende Benachrichtigung angezeigt:

![Module not activated](/images/DC/PurchaseContracts/module-not-activated.png)

In dieser Benachrichtigung stehen Ihnen die folgenden Aktionen zur Verfügung:

<br>

| Aktion                           | Beschreibung                                                                                                                                                                                                                                   |
| -------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Mehr erfahren**                | Öffnet die [unterstützte Anleitung zum **Testen der Einkaufsverträge**](#the-try-purchase-contracts-assisted-setup-guide), die Ihnen einen Überblick gibt und Sie beim Starten einer Einkaufsverträge-Testversion unterstützt. |
| **Ähnliche Rechnungen anzeigen** | Öffnet [die Liste **Vorgeschlagene Einkaufsverträge**](#die-liste-vorgeschlagene-einkaufsvertrage).                                                                                                                            |
| **Nicht mehr anzeigen**          | Deaktiviert die Benachrichtigung für den Benutzer und für alle Belegvorlagen.                                                                                                                                                  |

> [!NOTE]
> Wenn das Einkaufsverträge-Modul nicht aktiviert ist, können Sie auch mit der Option **Testen Sie es** von der Seite **Continia Lösungsverwaltung** aus öffnen:
>
> 1. Suchen Sie ({{search}}) nach **Continia Lösungsverwaltung** und wählen Sie dann den entsprechenden Link aus.
> 2. Wählen Sie in der Infobox **Abonnementdetails** rechts unter **Abonnement Module** >**Testen Sie es**, um die unterstützte Anleitung [zum **Testen von Einkaufsverträgen**](#die-unterstutzte-anleitung-zum-testen-von-einkaufsvertragen) zu öffnen.

### Die unterstützte Anleitung zum Testen von Einkaufsverträgen

Die unterstützte Anleitung zum **Testen von Einkaufsverträgen** bietet einen Überblick über die Vorteile, die Sie mit dem Einkaufsverträge-Modul genießen können.

Im ersten Schritt der Anleitung finden Sie folgenden Link: **\{Anzahl} Ihrer Lieferanten sind perfekt, um das Modul zu testen**. Wenn Sie auf diesen Link klicken, wird [die Liste **Vorgeschlagene Einkaufsverträge**](#die-liste-vorgeschlagene-einkaufsvertrage) geöffnet. Damit erhalten Sie entweder einen Überblick über alle potenziellen Einkaufsverträge oder können einen neuen Vertrag erstellen, wenn Sie das Einkaufsverträge-Modul aktiviert haben.

Wenn Sie **Weiter** auswählen, gelangen Sie zum zweiten Schritt der unterstützten Anleitung. Hier können Sie **Test starten** auswählen, um eine kostenlose 30-Tage-Testversion des Einkaufsverträge-Moduls zu starten. Dadurch wird die Testversion aktiviert und folgendermaßen gestartet:

- Wenn Sie die Anleitung über die Benachrichtigung oben im Belegjournal geöffnet haben, gelangen Sie zurück zum Belegjournal und können dort wie gewohnt fortfahren.
- Wenn Sie die Anleitung von der **Continia Lösungsverwaltung** aus geöffnet haben, wird ein Dialogfeld angezeigt, in dem Sie gefragt werden, ob Sie sofort einen Einkaufsvertrag erstellen möchten. Klicken Sie auf **Ja**, um [die Liste **Vorgeschlagene Einkaufsverträge**](#die-liste-vorgeschlagene-einkaufsvertrage) zu öffnen.

## Die Liste „Vorgeschlagene Einkaufsverträge“

Die Liste **Vorgeschlagene Einkaufsverträge** ist eine Seite, auf der alle möglichen Einkaufsverträge aufgeführt werden, die durch eine [Analyse von Aufgabenwarteschlangen](#funktionsweise-und-kriterien) ermittelt werden.

In der Aktionsleiste können Sie **Details anzeigen** auswählen, um [die Seite **Vorgeschlagener Einkaufsvertrag**](#the-suggested-purchase-contract-page) für den Vertrag zu öffnen, den Sie in der Liste der möglichen Verträge ausgewählt haben. Auf dieser Seite erhalten Sie eine detailliertere Ansicht des vorgeschlagenen Einkaufsvertrags und können basierend darauf einen neuen Vertrag erstellen, wenn Sie das Einkaufsverträge-Modul aktiviert haben.

Wenn Sie das Einkaufsverträge-Modul aktiviert haben, stehen Ihnen in der Aktionsleiste außerdem folgende Aktionen zur Verfügung:

- **Erstelle Einkaufsvertrag**: Damit wird [die Seite **Erstelle Einkaufsvertrag**](#-die-seite-erstelle-einkaufsvertrag) geöffnet, auf der Sie dann auf Grundlage des Vertragsvorschlags einen Einkaufsvertrag erstellen können.
- **Einkaufsvertrag öffnen**: Damit wird die Karte **Einkaufsvertrag** eines bereits bestehenden Vertrags geöffnet, der der ausgewählten Rechnung ähnelt. Die Aktion ist nur verfügbar, wenn ein solcher Vertrag bereits im Einkaufsverträge-Modul erstellt wurde.

> [!NOTE]
> Diese beiden Aktionen sind nur auswählbar, wenn das Einkaufsverträge-Modul aktiviert wurde. Wenn es nicht aktiviert wurde, sind die Aktionen in der Aktionsleiste nicht verfügbar.

Die Liste enthält die folgenden Spalten:

<br>

| Spaltenüberschrift                                                      | Beschreibung                                                                                                                                                                                                                                                                                                                             |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Eink. von Kred.-Nr.** | Die Nummer des Kreditors, der die wiederkehrenden Rechnungen gesendet hat, auf denen der vorgeschlagene Vertrag basiert. Diese Nummer wird verwendet, um die Rechnungen zu gruppieren.                                                                                                                   |
| **Eink. von Name**                                      | Der Name des Kreditors, der die wiederkehrenden Rechnungen gesendet hat, auf denen der vorgeschlagene Vertrag basiert. Dieser Name wird verwendet, um die Rechnungen zu gruppieren.                                                                                                                      |
| **Abrechnungszeitraum**                                                 | Der Rechnungszeitraum, den das System anhand der Belegdaten der gruppierten Rechnungen vorgeschlagen hat.                                                                                                                                                                                                                |
| **Währung**                                                             | Die Währung des vorgeschlagenen Vertrags. Die Rechnungen, auf denen der vorgeschlagene Vertrag basiert, werden auch anhand dieses Werts gruppiert.                                                                                                                                                       |
| **Letzter Rechnungsbetrag**                                             | Der Betrag der letzten Rechnung in der Rechnungsgruppe, auf der der vorgeschlagene Vertrag basiert. Dieser Betrag enthält keine Mehrwertsteuer.                                                                                                                                                          |
| **Letztes Rechnungsdatum**                                              | Das Datum der letzten Rechnung in der Rechnungsgruppe, auf der der vorgeschlagene Vertrag basiert.                                                                                                                                                                                                                       |
| **Bestehender Vertrag**                                                 | Ein Hinweis darauf, ob bereits ein ähnlicher Einkaufsvertrag im System vorhanden ist. Diese Spalte ist nur sichtbar, wenn das Einkaufsverträge-Modul aktiviert wurde. Wenn das Kontrollkästchen aktiviert ist, ist die Aktion **Einkaufsvertrag öffnen** in der Aktionsleiste aktiviert. |
| **Anzahl Rechnungen**                                                   | Die Anzahl der Rechnungen, die zu einem möglichen Einkaufsvertrag zusammengefasst wurden.                                                                                                                                                                                                                                |

## Die Seite „Vorgeschlagener Einkaufsvertrag“

Die Seite **Vorgeschlagener Einkaufsvertrag** bietet einen Überblick über den Einkaufsvertrag, der aufgrund der erkannten, wiederkehrenden Rechnungen vorgeschlagen wurde. Auf der rechten Seite ist eine Dokumentenvorschau verfügbar, die den Beleg anzeigt, den Sie in der Liste unter **Wiederkehrende Rechnungen** ausgewählt haben (siehe unten).

Klicken Sie in der Aktionsleiste auf **Erstelle Einkaufsvertrag**, um [die Seite **Einkaufsvertrag erstellen**](#die-seite-erstelle-einkaufsvertrag) zu öffnen. Dort können Sie dann auf Grundlage des Vertragsvorschlags einen Einkaufsvertrag erstellen.

> [!NOTE]
> Dies ist nur möglich, wenn das Einkaufsverträge-Modul aktiviert wurde. Wenn dies nicht aktiviert ist, bietet die Seite **Vorgeschlagener Einkaufsvertrag** nur einen Überblick und in der Aktionsleiste sind keine Aktionen verfügbar.

Im Inforegister **Allgemein** finden Sie die grundlegenden Details des vorgeschlagenen Vertrags, zum Beispiel die folgenden Felder:

<br>

| Feld                                                                    | Beschreibung                                                                                                                                                                                                           |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Eink. von Name**                                      | Der Name des Kreditors, der die wiederkehrenden Rechnungen gesendet hat, auf denen der vorgeschlagene Vertrag basiert. Dieser Name wird verwendet, um die Rechnungen zu gruppieren.    |
| **Eink. von Kred.-Nr.** | Die Nummer des Kreditors, der die wiederkehrenden Rechnungen gesendet hat, auf denen der vorgeschlagene Vertrag basiert. Diese Nummer wird verwendet, um die Rechnungen zu gruppieren. |
| **Währung**                                                             | Die Währung des vorgeschlagenen Vertrags. Die Rechnungen, auf denen der vorgeschlagene Vertrag basiert, werden auch anhand dieses Werts gruppiert.                                     |
| **Abrechnungszeitraum**                                                 | Der Rechnungszeitraum, den das System anhand der Belegdaten der gruppierten Rechnungen vorgeschlagen hat.                                                                                              |

Im Inforegister **Wiederkehrende Rechnungen** werden die gebuchten Einkaufsrechnungen angezeigt, die als [wiederkehrend und zugehörig](#funktionsweise-und-kriterien) identifiziert wurden. Die Liste enthält nur die drei aktuellsten Rechnungen. Um alle zusammengefassten Rechnungen anzuzeigen, gehen Sie zur Titelleiste des Inforegisters und wählen **Alle Rechnungen** aus. In der Titelleiste des Inforegisters können Sie auch **Rechnung öffnen** auswählen, um eine beliebige Rechnung in der Liste als **Gebuchte Einkaufsrechnung** zu öffnen.

Die Liste enthält die folgenden Spalten:

<br>

| Spaltenüberschrift                                     | Beschreibung                                                                                                                                    |
| ------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| **Nr.**                                | Die Nummer der gebuchten Einkaufsrechnung, wie in Document Capture registriert.                                                 |
| **Kreditoren Rechnungsnummer**                         | Die Rechnungsnummer, wie sie vom Kreditor intern registriert wurde (in der Regel in der Rechnung angegeben). |
| **Einkäufercode**                                      | Der Einkäufercode, wie auf der Rechnung angegeben.                                                                              |
| **Belegdatum**                                         | Das Datum, an dem die Rechnung ausgestellt wurde, wie in der Rechnung angegeben.                                                |
| **Betrag**                                             | Der Gesamtbetrag der Rechnung ohne Mehrwertsteuer.                                                                              |
| **Betrag inkl. MwSt.** | Der Gesamtbetrag der Rechnung einschließlich Mehrwertsteuer.                                                                    |

## Funktionsweise und Kriterien

Diese Funktion schlägt mögliche Einkaufsverträge auf der Grundlage wiederkehrender Rechnungen vor, die im System identifiziert wurden. Wiederkehrende Rechnungen sind Rechnungen, die Sie in festgelegten Abständen (beispielsweise monatlich) erhalten und die im Wesentlichen identisch oder zumindest sehr ähnlich sind. Um solche wiederkehrenden Rechnungen zu identifizieren, werden alle 24 Stunden Aufgabenwarteschlangen ausgeführt. Diese Aufgabenwarteschlangen werden um Mitternacht ausgeführt und laufen nur 30 Minuten, um Systemunterbrechungen zu minimieren. Wenn eine Aufgabenwarteschlange innerhalb des 30-minütigen Zeitfensters keine vollständige Analyse durchführen kann, wird sie beim nächsten Mal an der Stelle fortgesetzt, an der sie beendet wurde.

Die Aufgabenwarteschlangen umfassen Folgendes:

- Analysiert werden alle Rechnungen, die innerhalb eines Zeitraums von drei Jahren eingegangen sind.
- Gebuchte Rechnungen werden berücksichtigt, aber keine stornierten Rechnungen.
- Rechnungen von gesperrten Kreditoren werden ausgeschlossen.
- Es werden Inflation und andere Änderungen berücksichtigt und der folgende maximale Preisunterschied ist zulässig:
  - 3 % bei Monatsverträgen.
  - 14% bei Jahresverträgen.

Wenn Aufgabenwarteschlangen Ihre empfangenen Rechnungen in diesem Umfang analysieren, gruppieren sie zusammengehörige Rechnungen anhand der folgenden Kriterien:

- Kreditoren müssen übereinstimmen.
- Währungscodes müssen übereinstimmen.
- Beträge müssen übereinstimmen (innerhalb der oben genannten akzeptablen Abweichungsprozentsätze).
- Belegdaten müssen übereinstimmen, das heißt, sie müssen innerhalb des angegebenen Rechnungszeitraums einem sequenziellen Muster folgen.
- Zeilen müssen übereinstimmen (hinsichtlich der Felder **Art**, **Nr.**, **Menge**, **Einstandspreis** und **Betrag**).
- Der Abrechnungszeitraum muss anhand der Rechnungsdaten erkennbar sein.
- Die Anzahl Rechnungen, die für den identifizierten Abrechnungszeitraum gruppiert wurden, muss ausreichend sein:
  - Bei Jahres-, Halbjahres- und Quartalsverträgen sind zwei Rechnungen erforderlich.
  - Bei Monatsverträgen sind drei Rechnungen erforderlich.
- Für die letzte Rechnungsperiode muss eine Rechnung vorliegen. <br> <div class="alarm alarm-note"><p class="alert-title"><i class="icon icon-warning-2"></i><span>Hinweis</span></p><p>Wenn beispielsweise für Juni, Juli und August zugehörige Rechnungen identifiziert werden, für September jedoch keine ähnliche Rechnung existiert, stellt das System fest, dass diese Rechnungen nicht mehr wiederkehrend sind und es wird auf ihrer Grundlage kein Vertrag mehr vorgeschlagen. </p></div>

Sind diese Kriterien bei mehreren Rechnungen erfüllt, werden diese Rechnungen gruppiert, als wiederkehrend und zusammengehörig gekennzeichnet und diese Rechnungsgruppe bildet dann die Grundlage eines möglichen Vertrags.

## Informationen zum Thema

[Einkaufsverträge erstellen](@DC-86)  
[Einkaufsverträge genehmigen](@DC-87)  
[Vertragsrechnungen erstellen](@DC-88)  
[Vertragsrechnungen genehmigen](@DC-89)  
[Das Einkaufsvertragsarchiv anzeigen](@DC-90)