---
title: Belegarten einrichten
date: 02-06-2025
description: Erfahren Sie, wie Sie eine Belegart einreichen.
id: EM-41
lang: de
---

# Belegarten einrichten

Belegarten sind Codes, die es Expense-Benutzern ermöglichen, ihre Belege effizient zu kategorisieren. Beispielsweise können Benutzer schnell Belege für Verpflegung, Parken oder Unterkunft identifizieren.

Mit Expense Management können Sie spezifische Einstellungen für jede Belegart anpassen. Geben Sie beispielsweise an, ob für eine Belegart ein Anhang für die Validierung hochgeladen werden muss. Darüber hinaus können Sie bestimmte Belegarten für bestimmte Benutzer ausblenden und so die Einstellungen an individuelle Anforderungen und persönliche Präferenzen anpassen.

So richten Sie eine Belegart ein:

1. Suchen Sie {{search}} nach **Belegart**.
2. Klicken Sie in der Aktionsleiste auf **Neu**.
3. Füllen Sie die folgenden Felder aus:
   - **Code** – Geben Sie den mit der Belegart verknüpften Code ein.
   - **Beschreibung** – Geben Sie eine kurze Erklärung zum Zweck der Belegart an.
   - **Suchbegriff** – Geben Sie einen Suchbegriff an, um die Belegart einfach zu finden.
   - **Keine Erstattung** – Gibt an, ob die Erstattung durch das Unternehmen zulässig ist. Der Mitarbeiter muss für die Gebühren aufkommen, die durch die Nutzung der Firmenkreditkarte entstehen, sofern er nicht dazu berechtigt ist. Diese Einstellung wird auch verwendet, wenn der Benutzer mit der Firmenkreditkarte an einem Geldautomaten Bargeld abhebt.
   - **Anhang** – Mit dieser Einstellung können Sie festlegen, ob für eine bestimmte Belegart das Hochladen eines Anhangs erforderlich ist. Die Optionen sind:
      - _Empfohlen_ – Wählen Sie diese Option, wenn Sie den Benutzer warnen möchten, wenn er vergisst, eine Datei anzuhängen. Es hindert den Benutzer nicht daran, einen Beleg ohne Anhang zu senden, informiert ihn aber über den fehlenden Anhang.
      - _Obligatorisch_ – Wählen Sie diese Option, wenn für einen Beleg das Anhängen einer Datei erforderlich ist. Der Benutzer kann keinen Beleg senden, ohne einen Anhang beizufügen, und der Buchhalter kann die Belege auch nicht verarbeiten.
      - _Optional_ – Verwenden Sie diese Option, wenn für eine bestimmte Belegart keine Anhänge erwartet werden. Dies eignet sich zum Beispiel für Kreditkartengebühren, für die möglicherweise keine Quittung verfügbar ist. Der Benutzer erhält keine Warnungen oder Fehlermeldungen. Wenn der Benutzer dennoch eine Quittung anhängen möchte, wird diese vom System akzeptiert.
   - **Nicht auswählbar** – Wenn diese Einstellung aktiviert ist, wird die Belegart in der Continia Expense Mobile App oder im Expense Portal nicht mehr angezeigt. Dies kann beispielsweise bei gebührenpflichtigen Belegarten sinnvoll sein.
   - **Transaktion ausschließen** – Wählen Sie diese Einstellung aus, um Transaktionen von der sofortigen Buchung nach dem Import auszuschließen. Dies basiert auf Abstimmungsregeln, bei denen ein bestimmtes Schlüsselwort innerhalb der Transaktion die entsprechende Belegart identifiziert. Folglich verhindert Expense Management, dass diese Transaktionen gebucht werden. Weitere Informationen finden Sie unter [Bearbeitungsgebühren](@EM-163).
   - **Teilnehmer erforderlich** – In manchen Unternehmen kann ein höherer Aufwand entstehen, wenn mehrere Benutzer an der gleichen Veranstaltung teilnehmen, sofern die Namen der Teilnehmer angegeben werden. Zu diesem Zweck kann ein Beleg so konfiguriert werden, dass er das Pflichtfeld **Teilnehmer erforderlich** enthält. Sie müssen [Systemabhängigkeiten aktualisieren](/continia-expense-management/setting-up-expense-management/setting-up-general-business-functionality/setting-up-field-dependencies#so-aktualisieren-sie-systemabhangigkeiten), damit die Änderungen wirksam werden.
   - **Bild** – Das Bild, das in der Expense Mobile App und im Expense Portal für die Belegart angezeigt wird.
   - **Unternehmensrichtlinien** – gibt die Anzahl der Unternehmensrichtlinien an, die für diese Belegart gelten. Hier finden Sie weitere Informationen über die Konfiguration von Standarddimensionen und zum Festlegen spezieller [Unternehmensrichtlinien für Belege](@EM-39) und [Unternehmensrichtlinien für Fahrstrecken.](@EM-40)
   - **Einkaufsvertrag** – Gibt an, ob für die Belegart ein Einkaufsvertrag erforderlich ist.

## Eine Buchungseinrichtung hinzufügen

Sie müssen Ihrer Belegart außerdem eine Buchungseinrichtung hinzufügen.

1. Wählen Sie eine Belegart und klicken Sie dann in der Aktionsleiste auf **Einrichtung**.

2. Füllen Sie die folgenden Felder aus:
   - **Benutzer** – Dies ist der Mitarbeiter, für den das Buchungskonto verwendet wird. Wenn dieses Konto für mehrere Mitarbeiter verwendet werden soll, sollte dieser Wert leer sein.
   - **Expense Benutzergruppe** – Dies ist die Mitarbeitergruppe, für die das Buchungskonto verwendet wird. Wenn keine Anforderung für bestimmte Gruppen besteht, kann dieser Wert leer sein.
   - **Buchungskontoart** – Geben Sie den Kontotyp ein, der beim Buchen verwendet wird. Die gängigste Option ist Sachkonto.
   - **Buchungskonto Nr.** – Geben Sie eine Sachkontonummer (oder in seltenen Fällen die Artikelnummer) für die interne Buchung nicht in einem Lohn- und Gehaltsabrechnungssystem ein.
   - **Produktbuchungsgruppe** – Hier können Sie eine allgemeine Produktbuchungsgruppe hinzufügen, die beim Buchen verwendet wird. Dadurch werden die Standardwerte des Buchungskontos überschrieben.
   - **Geschäftsbuchungsgruppe** – Die Geschäftsbuchungsgruppe ist die Gruppe, die beim Buchen verwendet wird. Dadurch werden die Standardwerte des Buchungskontos überschrieben.
   - **MwSt.-Produktbuchungsgruppe** – Gibt die MwSt.-Produktbuchungsgruppe an, die beim Buchen verwendet wird. Dadurch werden die Standardwerte des Sachkontos überschrieben.
   - **MwSt.-Geschäftsbuchungsgruppe** – Gibt die MwSt.-Geschäftsbuchungsgruppe an, die beim Buchen verwendet wird. Dadurch werden die Standardwerte des Sachkontos überschrieben.

3. Sie können die Buchung der Belegart nach Expense-Benutzer, Expense-Benutzergruppe oder Land differenzieren, beispielsweise, wenn Sie für bestimmte Länder eine andere Mehrwertsteuer oder Umsatzsteuer anwenden möchten. [Personalisieren Sie dazu die Seite](https://docs.microsoft.com/de-de/dynamics365/business-central/ui-personalization-user), indem Sie die folgenden Schritte ausführen:
   1. Klicken Sie auf **Einstellungen** {{settings}} > **Personalisieren**.
   2. Klicken Sie in der oberen linken Ecke auf **+ Feld**, um den Bereich **Feld der Seite hinzufügen** zu öffnen.
   3. Ziehen Sie die relevanten Felder – in diesem Fall **Land/Region Code** und **Land/Region** – aus dem Bereich in die Tabellenüberschrift.
   4. Klicken Sie auf **Fertig**, um das Banner **Personalisierung** zu schließen.

4. Die neuen Spalten werden der Tabelle hinzugefügt. Wenn Sie eine Standard-Mehrwertsteuer oder Umsatzsteuer für alle Länder festlegen möchten:

   1. Gehen Sie zu **Land/Region** für die erste Zeile in der Tabelle.
   2. Klicken Sie auf **Länder/Regionen kopieren**.
   3. Füllen Sie die restlichen Felder nach Bedarf für diese Zeile aus.

5. Um eine Mehrwertsteuer oder Umsatzsteuer für ein bestimmtes Land festzulegen:

   1. Gehen Sie zu **Land/Region** für die zweite Zeile in der Tabelle.

   2. Klicken Sie auf **Land**.

   3. Klicken Sie in der Spalte **Land/Region Code** auf den Code des entsprechenden Landes und füllen Sie dann die restlichen Felder nach Bedarf für diese Zeile aus.

   > [!TIP]
   > Wählen Sie beispielsweise für **MwSt.-Produktbuchungsgruppe** > **Ohne MwSt.** aus, wenn der ausgewählte Ausgabentyp für das ausgewählte Land von der MwSt. befreit ist.

6. Suchen Sie {{search}} nach **Konfigurierte Felder**.

7. Gehen Sie in der Tabelle zur Spalte **Feldcode** für eine leere Zeile und klicken Sie auf **LAND/REGION** für diese Zeile.

8. Klicken Sie in der Aktionsleiste auf **Continia Online** > **Erzwinge Synchronisation mit Continia Online**.

In der Expense Mobile App und im Expense Portal ist das Feld **Land/Region Code** jetzt für Belege sichtbar, d. h. Sie können sehen oder angeben, in welchem Land eine bestimmte Ausgabe angefallen ist. Wenn Sie einen Beleg mit einer Buchungskonfiguration erstellen, die für ein bestimmtes Land angepasst wurde (wie in der Anleitung oben beschrieben) und dieses Land im Feld **Land/Region Code** angezeigt wird, wird die angepasste Buchungskonfiguration automatisch angewendet und der Beleg entsprechend gebucht.

> [!IMPORTANT]
> Wenn Sie eine Buchungseinrichtung für ein bestimmtes Land anpassen, ist es wichtig, dass alle anderen Länder auch über eine Buchungseinrichtung verfügen.

Hier ist ein Beispiel für eine Buchungseinrichtung:

1. Suchen Sie {{search}} nach **Expense Buchungseinrichtung**.
2. Gehen Sie zu **Land/Region** für die erste Zeile in der Tabelle.
3. Klicken Sie auf **Alle Länder/Regionen**, um eine Standard-Buchungseinrichtung vorzunehmen, die für alle Länder gilt.
4. Sie können dann für alle Länder, die von dieser Standardeinrichtung abweichen, benutzerdefinierte Buchungseinstellungen festlegen, indem Sie zusätzliche Tabellenzeilen hinzufügen: Klicken Sie unterr **Land/Region** auf **Land**.
5. Fügen Sie unter **Land/Region Code** den entsprechenden Ländercode hinzu.

Sie können sogar mehrere Länder mit derselben Buchungseinrichtung in einer Gruppe zusammenfassen – beispielsweise in einer Gruppe „Ausland“ – deren Code Sie unter **Land/Region Code** angeben. Dies spart Ihnen in Ihrem Arbeitsablauf Zeit, da Sie bei Verwendung dieser Methode nur eine zusätzliche Tabellenzeile erstellen müssen, anstatt eine Zeile pro Land erstellen zu müssen.
