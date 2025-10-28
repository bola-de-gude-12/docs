---
title: Das Continia Delivery Network einrichten
date: 12-03-2025
description: Informationen zum Einrichten des Continia Delivery Networks.
id: DC-75
lang: de
---

# Das Continia Delivery Network einrichten

Bevor Sie mit der Nutzung des Continia Delivery Network beginnen können, müssen Sie von Continia freigeschaltet werden. Derzeit können Sie dem [Peppol eDelivery Network](#teilnahme-am-peppol-edelivery-network) oder dem [NemHandel-Netzwerk](#teilnahme-bei-nemhandel-nur-fur-danische-unternehmen) (nur für dänische Unternehmen) beitreten, wie unten beschrieben.

> [!NOTE]
> Das Continia Delivery Network ist in Sandbox-Umgebungen nicht verfügbar.

## Teilnahme einrichten

So verbinden Sie sich mit den NemHandel- und/oder Peppol-Netzwerken:

1. Um den Einrichtungsassistenten zu öffnen, wählen Sie einen der folgenden Schritte:
   - Wählen Sie das Symbol {{search}}, geben Sie **Continia Delivery Network Onboarding** ein, und wählen Sie dann den zugehörigen Link.
   - Wählen Sie das Symbol {{search}}, geben Sie **Continia Delivery Network Teilnahmen** ein, und wählen Sie dann den zugehörigen Link. Wählen Sie in der Aktionsleiste **Neu** und dann **Neue Teilnahme** aus.

2. Der **Onboarding-Assistent für das Continia Delivery Network** wird geöffnet. Wählen Sie **Weiter**.

3. Aktivieren Sie je nach Bedarf ein oder mehrere Netzwerke (wenn Sie beispielsweise nur in Dänemark geschäftlich tätig sind, aktivieren Sie **NemHandel**). Wählen Sie dann **Weiter**.

4. Füllen Sie alle Felder nach Bedarf aus. Einige der Felder sind möglicherweise vorausgefüllt basierend auf den Informationen Ihres Microsoft Dynamics 365 Business Central-Mandanten. Sie können jedoch bei Bedarf andere Informationen eingeben. <br>

   | **Feld**                  | **Beschreibung**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
   | ------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   | Kennungstyp ID            | Der Kennungstyp. Wenn Sie die Unternehmenskennung nicht kennen, suchen Sie im [NemHandelsregistret](https://registration.nemhandel.dk/NemHandelRegisterWeb/) (nur für NemHandel) oder im [Peppol-Verzeichnis](https://docs.peppol.eu/edelivery/codelists/) unter Participant Identifier Schemes (nur für Peppol) danach. Weitere Informationen finden Sie unter [Kennungstypen](#kennungstypen).                                                          |
   | Kennung Wert              | Der Wert der Kennung. Dies ist der Name, unter dem das Unternehmen registriert ist und unter dem andere es im Peppol-Netzwerk finden können. Zum Beispiel: DK77777777.                                                                                                                                                                                                                                                                                                          |
   | Mandantenname             | Der Name des Mandanten. Zum Beispiel: CRONUS UK Ltd.                                                                                                                                                                                                                                                                                                                                                                                                                                            |
   | USt-IdNr. | Der lokale Registrierungscode, der das Unternehmen identifiziert. Zum Beispiel: VAT, DK:CVR, NO:ORG, SE:ORG, usw.                                                                                                                                                                                                                                                                                                                               |
   | Adresse                   | Die Adresse des Unternehmens.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
   | PLZ-Code                  | Die Postleitzahl des Unternehmens.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
   | Länder-/Regionscode       | Der Code des Landes oder der Region, in der das Unternehmen seinen Sitz hat. Zum Beispiel: GB.                                                                                                                                                                                                                                                                                                                                                                                                  |
   | Ihr Name                  | Der Name der Person, die für die Einrichtung des Continia Delivery Network für das Unternehmen autorisiert ist, z. B. ein Partner oder Berater.                                                                                                                                                                                                                                                                                                                                                 |
   | Kontaktname               | Der Name des Ansprechpartners im Unternehmen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
   | Kontakt Telefonnummer     | Die Telefonnummer des Ansprechpartners im Unternehmen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
   | Kontakt-E-Mail            | Die E-Mail-Adresse des Ansprechpartners im Unternehmen. Beachten Sie, dass, wenn die Domäne dieser E-Mail-Adresse nicht mit dem **Mandantennamen** übereinstimmt, zusätzliche Fragen gestellt werden, um die Verbindung zwischen den beiden zu überprüfen. Zum Beispiel: Durch Eingabe von CRONUS UK Ltd. unter **Mandantenname** und benutzer@contoso.com unter **Kontakt E-Mail** ist eine zusätzliche Überprüfung erforderlich. |

5. Wenn Sie möchten, dass andere Personen und Organisationen Sie finden können und sehen, dass Sie Teil des Netzwerks sind, aktivieren Sie den Schalter **Im Verzeichnis veröffentlichen**.

6. Fügen Sie unter **Bitte wählen Sie die Profile aus, bei denen Sie registriert werden möchten** Ihr bevorzugtes Profil bzw. Ihre Profile hinzu. Ein Profil ist eine Belegart, die Sie senden und/oder empfangen können. Sie können mehrere Profile einzeln oder in Gruppen konfigurieren.
   > [!NOTE]
   > In der Spalte **Profilrichtung** können Sie die Richtung für jedes Profil auswählen, das heißt, ob Sie diese bestimmte Belegart senden und/oder empfangen möchten. Wenn Sie **Eingehend** oder **Beides** auswählen, müssen Sie in der Spalte **Belegkategorie** eine Document Capture-Kategorie eingeben, um festzulegen, in welche Kategorie das Continia Delivery Network eingehende Belege für dieses Profil importieren soll.

7. Wählen Sie **Weiter** > **Beenden**, um sich mit dem Continia Delivery Network zu verbinden.

Ihre Onboarding-Registrierung muss von Continia manuell genehmigt werden, bevor Sie dem Netzwerk offiziell beitreten können. Dies kann zwei bis vier Tage dauern und Sie müssen möglicherweise weitere Informationen bereitstellen, damit Continia Ihre Daten überprüfen kann.

## Liste der Teilnahmen

Wenn Sie den **Continia Delivery Network Onboarding-Assistenten** wie oben beschrieben abgeschlossen haben, haben Sie eine sogenannte Teilnahme erstellt. Eine Teilnahme ist im Grunde jede Organisation oder juristische Person, die dem Continia Delivery Network beigetreten ist bzw. dies beantragt hat und als solche registriert ist. Die Teilnahme ermöglicht es dieser Organisation oder juristischen Person auch, Belege über das Continia Delivery Network zu senden und zu empfangen.

Zwei der Felder, die Sie im Einrichtungsassistenten ausfüllen, werden zur eindeutigen Identifizierung jeder Teilnahme verwendet: **Kennungstyp ID** und **Kennung Wert**. Sie können zwar mehrere Teilnahmen erstellen (z. B. eine für jede juristische Person innerhalb einer Organisation), aber nicht mehrere Teilnahmen mit demselben Paar aus Kennung Typ-ID und Kennung Wert. Die Kennungstyp ID und der entsprechende Wert sind für die Teilnahme, mit der sie erstellt wurden, eindeutig und können daher nur einmal verwendet werden.

> [!NOTE]
> Es ist möglich, dieselbe GLN für Peppol und NemHandel zu verwenden.

> [!IMPORTANT]
> Wenn Sie dem Peppol- oder NemHandel-Netzwerk zuvor über einen anderen Dienstanbieter als Continia beigetreten sind, müssen Sie sich bei diesem Dienstanbieter abmelden, um dem Continia Delivery Network beitreten zu können. Wenn dies bei Ihnen der Fall ist, wenden Sie sich bitte an [Ihren Continia-Partner](@DC-15), um Unterstützung zu erhalten.

Alle von Ihnen erstellten Teilnahmen werden der Liste der Teilnahmen hinzugefügt. Wählen Sie das Symbol {{search}}, geben Sie **Continia Delivery Network Teilnahmen** ein, und wählen Sie dann den zugehörigen Link, um diese Liste zu öffnen. Die Liste bietet einen Überblick über Ihre Teilnahmen und deren jeweiligen Status:

- Genehmigung ausstehend: Alle neu erstellten Teilnahmen erhalten diesen Status sofort nach der Erstellung und behalten ihn, bis sie manuell von Continia genehmigt werden.
- Verbunden: Dies ist der Status aller von Continia genehmigten Teilnahmen. Mit diesem Status können Sie Belege über das Continia Delivery Network senden/empfangen.
- Abgelehnt: Teilnahmen, die Continia nicht genehmigen konnte, werden als abgelehnt markiert, normalerweise mit einem Hinweis auf den Grund der Ablehnung.

Die Angabe falscher Informationen in den Feldern **Kennung Typ-ID** und **Kennung Wert** führt zur sofortigen Ablehnung der Onboarding-Anfrage. Wenn Ihre Teilnahme jedoch abgelehnt wird, können Sie sie direkt in der List der Teilnahmen bearbeiten und erneut einreichen.

## Kennungstypen

### NemHandel

Dies sind die im NemHandel-Netzwerk verfügbaren Kennungstypen.

| **Kennung**            | **Beschreibung**                                                                                                                                                |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| DK:CVR | Det Centrale Virksomhedsregister (Central Business Register), das von Unternehmen in Dänemark verwendet wird.                |
| GLN                    | Global Location Number, die international zur Identifizierung physischer Standorte, juristischer Personen oder anderer Parteien verwendet wird. |

### Peppol

Dies sind einige der gängigsten Kennungstypen im Peppol-Netzwerk.

| Kennung                   | Beschreibung                                                                                                                                                                      |
| ------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BE:EN/VAT | Belgische Umsatzsteuer-Identifikationsnummer für Unternehmen.                                                                                                     |
| DE:VAT    | Deutsche Umsatzsteuer-Identifikationsnummer für Unternehmen.                                                                                                      |
| DK:DIGST  | Dänische Kennung für digitale Behördendienste.                                                                                                                    |
| FI:OVT2   | Finnische Umsatzsteuer-Identifikationsnummer für Unternehmen.                                                                                                     |
| GLN                       | Global Location Number. Diese wird international zur Identifizierung physischer Standorte, juristischer Personen oder anderer Parteien verwendet. |
| NL:VAT    | Niederländische Umsatzsteuer-Identifikationsnummer für Unternehmen.                                                                                               |
| NO:ORG    | Organisasjonsnummer (Norwegische Unternehmensnummer).                                                                                          |
| SE:ORGNR  | Organisationsnummer (Schwedische Unternehmensnummer).                                                                                          |

## Informationen zum Thema

[Finden eines Partners für Continia Document Capture](@DC-15)