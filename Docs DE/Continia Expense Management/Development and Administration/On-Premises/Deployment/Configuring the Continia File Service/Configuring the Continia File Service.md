---
title: Expense Management Den Continia File Service konfigurieren
date: 28-03-2023
description:
id: EM-139
lang: de
---

# Den Continia File Service konfigurieren

Nachdem Sie den [Continia File Service installiert](@EM-140) haben, müssen Sie ein Repository und einen Autorisierungsschlüssel dafür einrichten. Für diesen Vorgang müssen Sie das Continia File Service Konfigurationstool  – Continia File Service Configuration – verwenden, das als Teil des Installationsvorgangs auf demselben Server wie der Continia File Service installiert wird.

> [!IMPORTANT]
> Die Details, die Sie im Konfigurationstool beim Ausführen der Anleitung unten eingeben, werden später benötigt, wenn Sie [den Continia File Service in Business Central einrichten](@EM-142). Daher ist es wichtig, dass Sie dieselben verwenden, die Sie sie während dieses Einrichtungsvorgangs eingeben. Sie können unten jedes gewünschte Repository und jeden gewünschten Autorisierungsschlüssel als Freitext eingeben, solange Sie diese notieren und später genau so wiederverwenden.

Um ein Repository und einen Autorisierungsschlüssel für den Continia File Service einzurichten, gehen Sie folgendermaßen vor:

1. Öffnen Sie die Continia File Service-Konfiguration.
2. Wählen Sie je nach den Richtlinien Ihrer IT-Infrastruktur **Enable HTTP**, **Enable HTTPS** oder beides aus.
3. Geben Sie für die Option(en), die Sie oben in Schritt 2 aktiviert haben, die Portnummer(n) ein. Der Standardport für HTTP ist **5000**.
4. Fügen Sie unter **Repositories** die Einträge hinzu, die Sie verwenden möchten. Achten Sie darauf, den/die richtigen Pfad(e) einzugeben und notieren Sie sich Ihre Einträge, da Sie diese später noch benötigen.
   > [!NOTE]
   > Nachfolgend sehen Sie ein Beispiel für eine mögliche Konfiguration. Beachten Sie, dass alle Einträge nach der Eingabe in die Tabelle automatisch in Kleinbuchstaben umgewandelt werden:
   >
   > | Repository                | Autorisierungsschlüssel | Dateipfad             |
   > | ------------------------- | ----------------------- | --------------------- |
   > | documentcapture           | d93msbx52oem            | c:\dc |
   > | continiaexpensemanagement | 398dhjf4kkm67owly       | c:\em |
5. Wählen Sie im Abschnitt **Service** unter **Service user** einen Dienstbenutzer mit Zugriff auf das Verzeichnis aus.
6. Wählen Sie unter der Tabelle **Repositories** > **Save** aus, um Ihre Änderungen zu speichern.
7. Wählen Sie im Abschnitt **Service** unter **Service status** die Option **Starten** aus, um den Dienst zu starten.
8. Wenn Sie fertig sind, wählen Sie zum Beenden **Schließen**.

Jetzt können Sie die endgültige Konfiguration des Continia File Service durchführen. Informationen hierzu finden Sie unter [Den Continia File Service in Business Central einrichten](@EM-142).

<style>
  .content table tr td:nth-child(1) {
    width: 150px;
  }
  .content table tr td:nth-child(2) {
    width: 130px;
  }
  .content table tr td:nth-child(3) {
    width: 250px;
  }  
</style>