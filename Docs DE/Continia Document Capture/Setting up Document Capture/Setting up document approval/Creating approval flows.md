---
title: Genehmigungsabläufe erstellen
date: 04-10-2024
description: So richten Sie Genehmigungsabläufe ein.
id: DC-30
lang: de
---

# Genehmigungsabläufe erstellen

Als Alternative zur [Standardeinkaufsgenehmigung](@DC-32) können Sie einen Genehmigungsablauf bzw. mehrere Genehmigungsabläufe einrichten. Dabei handelt es sich im Prinzip um benutzerdefinierte Listen von Genehmigern, die für die Genehmigung von Belegen erforderlich sind. Ein Beleg, dem ein Genehmigungsablauf zugewiesen wurde, kann erst gebucht werden, wenn er von allen Genehmigern im Ablauf (Standardeinstellung) bzw. von den Genehmigern, die gemäß den angegebenen Grenzwerten ausgewählt wurden, genehmigt wurde. Bei der Standardeinstellung müssen die Genehmiger den Beleg in der Reihenfolge genehmigen, die Sie beim Einrichten des Ablaufs festlegen.

Beim Erstellen eines Genehmigungsablaufs müssen Sie diesem einen Genehmigungsablaufcode zuweisen, der den Anforderungen Ihres Unternehmens entspricht. Der Code kann als Freitext eingegeben werden und sollte Ihren Genehmigungsprozess so gut wie möglich beschreiben, z. B. **KLEIN** (für kleine Einkäufe) oder **DEUTSCHLAND** (für in Deutschland beschaffte Lieferungen), je nach Ihren Präferenzen. Der eingegebene Code wird verwendet, wenn Sie den Genehmigungsablauf einem Beleg zuweisen.

Um Ihrem Genehmigungsablauf Genehmiger hinzufügen zu können, müssen Sie diese zunächst [einrichten](@DC-23). Nach der Einrichtung stehen die Genehmiger in der **Continia Benutzerliste** zur Auswahl zur Verfügung, wie unten beschrieben.

> [!NOTE]
> Bei der [Vier-Augen-Genehmigung](@DC-35) ist Folgendes zu beachten: Wenn Sie einen Genehmigungsablauf einrichten und [zuweisen](@DC-33), wird die Vier-Augen-Genehmigung nicht angewendet, selbst wenn sie aktiviert wurde.

## So richten Sie einen Genehmigungsablauf ein

1. Wählen Sie das Symbol {{search}}, geben Sie **Genehmigungsabläufe** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie in der Aktionsleiste **Neu** aus, um einen Genehmigungsablauf hinzuzufügen.
3. Geben Sie in der Liste unter **Code** einen passenden Code für den Genehmigungsablauf ein.
4. **Optional**: Geben Sie unter **Beschreibung** eine Freitextbeschreibung des Genehmigungsablaufs ein.
5. Geben Sie unter **Auswahlmethode** an, wie Genehmiger für die Genehmigung von Belegen, auf die dieser Genehmigungsablaufcode angewendet wurde, ausgewählt werden. Weitere Informationen finden Sie unter [Genehmigungsabläufen Grenzbeträge hinzufügen](#genehmigungsablaufen-grenzbetrage-hinzufugen) weiter unten.
6. Unter **Anzahl von Genehmigern**, wählen Sie die Anzahl aus (**0** für neue Abläufe), um die Seite **Genehmiger** zu öffnen.
7. Wählen Sie in der Aktionsleiste **Neu** aus, um einen Genehmiger hinzuzufügen.
8. Wählen Sie in der Liste unter **Name** die drei Punkte rechts aus, um die **Continia Benutzerliste** zu öffnen. Wählen Sie einen Benutzer aus der Liste aus und klicken Sie dann auf **OK**, um die Seite zu schließen.
9. Fügen Sie unter **Genehmigungsgrenzwert** das Betragslimit hinzu, das für diesen Genehmiger angewendet werden soll. Dies gilt speziell für diesen Genehmigungsablauf und überschreibt alle anderen Genehmigungslimits, die an anderer Stelle für diesen Benutzer konfiguriert wurden. Beachten Sie, dass alle eingegebenen Grenzbeträge ignoriert werden, wenn Sie in Schritt 5 oben unter **Auswahlmethode** **Alle** auswählen.
10. Wiederholen Sie Schritte 7–9 für jeden weiteren Genehmiger, den Sie dem Ablauf hinzufügen möchten.

> [!NOTE]
> Wenn Sie in Schritt 5 unter **Auswahlmethode** die Option **Alle** auswählen, gilt Folgendes: Die Reihenfolge der Genehmiger auf der Seite **Genehmiger** stellt die Reihenfolge dar, in der Genehmiger alle Belege genehmigen müssen, denen dieser Ablauf zugewiesen wurde. Der oberste Genehmiger muss den Beleg zuerst genehmigen, und anschließend wird der Beleg an den zweiten Genehmiger in der Liste weitergeleitet (ggf. gefolgt vom dritten, vierten usw.).

## Genehmigungsabläufen Grenzbeträge hinzufügen

Wenn Sie einem Genehmigungsablauf Grenzbeträge hinzufügen, können Sie den Ablauf so einrichten, dass Belege immer dann freigegeben werden, wenn der Betrag innerhalb des angegebenen Grenzwerts liegt. Auf diese Weise müssen Belege nicht an alle Genehmiger im Ablauf weitergeleitet werden, wenn sie von einem Genehmiger mit dem entsprechenden Genehmigungslimit gleich zu Beginn genehmigt werden können. So wird nur die erforderliche Anzahl von Personen am Genehmigungsprozess beteiligt, wodurch eine schnellere Genehmigung von Belegen ermöglicht wird.

Um einem Genehmigungsablauf Grenzbeträge hinzuzufügen, folgen Sie der Anleitung [So richten Sie einen Genehmigungsablauf ein](#to-set-up-an-approval-flow) weiter oben. Die Grenzbeträge werden als numerische Werte für die einzelnen Genehmiger unter **Genehmigungsgrenzwert** in Schritt 9 der Anleitung hinzugefügt. In Schritt 5 der Anleitung können Sie entscheiden, ob und wie diese Grenzbeträge dann zur Auswahl von Genehmigern für die Genehmigung von Belegen mit diesem Genehmigungsablauf verwendet werden sollen. Die folgenden Auswahlmethoden stehen zur Verfügung:

<br>

| <span style="white-space: nowrap;">Auswahlmethode</span> | Beschreibung                                                                                                                                                                                                                                                                                                                                                            |
| -------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Alle**                                                 | Mit dieser Option wird für jeden Genehmiger im Ablauf ein Genehmigungsposten erstellt. Dies ist die Standardeinstellung, die genau der Funktionalität früherer Versionen von Continia Document Capture entspricht. Beachten Sie, dass alle eingegebenen Grenzbeträge ignoriert werden, wenn Sie diese Option auswählen. |
| **Erstqualifizierte**                                    | Mit dieser Option wählt Document Capture den ersten Genehmiger aus, dessen Grenzbetrag dem Gesamtwert des zur Genehmigung eingereichten Einkaufsbelegs entspricht oder diesen überschreitet.                                                                                                                                                            |
| **Alle bis Erstqualifizierte**                           | Mit dieser Option werden alle Genehmiger im Ablauf ausgewählt, beginnend bei dem Genehmiger mit dem niedrigsten Grenzbetrag bis zum erstqualifizierten Genehmiger (eine Definition hierzu finden Sie oben unter **Erstqualifizierte**).                                                                                              |
| **Initial und Erstqualifizierte**                        | Mit dieser Option wählt Document Capture den Genehmiger mit dem niedrigsten Grenzbetrag sowie den erstqualifizierten Genehmiger aus (eine Definition finden Sie unter **Erstqualifizierte** weiter oben).                                                                                                                            |

## Informationen zum Thema

[Genehmigungsabläufe verwenden](@DC-33)\
[Continia Benutzereinrichtung für Genehmigungen](@DC-23)
