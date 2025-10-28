Die folgenden Anforderungen und Empfehlungen gelten sowohl für die Online-Version als auch für die On-Premises-Version von Microsoft Dynamics 365 Business Central.

## Browser

Es wird empfohlen, einen der folgenden Webbrowser mit den neuesten Updates zu verwenden:

- Google Chrome
- Mozilla Firefox
- Apple Safari
- Microsoft Edge (Version 4.50 oder später)

Die Verwendung von Internet Explorer kann zu Fehlern und Problemen bei der Darstellung führen. Falls Internet Explorer die einzige Option ist, muss dieser auf die neueste Version aktualisiert werden.

## Bildschirmauflösung

Die Bildschirmauflösung muss mindestens 1440 × 900 Pixel betragen, da bei geringeren Auflösungen die Dokumentenvorschau von Document Capture nicht optimal funktioniert. Die empfohlene Bildschirmauflösung beträgt 1680 x 1050 Pixel oder höher.

Beachten Sie, dass das Vergrößern in Ihrem Browser oder Ändern der Skalierungs- und Layouteinstellungen Ihres Monitors nicht unterstützt wird und daher die Vorschau beeinträchtigen kann.

## Mobilgeräte

Die meisten Document Capture-Funktionen funktionieren auf Mobilgeräten, obwohl diese Funktionalität nicht offiziell unterstützt wird. Dies gilt für die Verwendung von Document Capture in verschiedenen Mobilversionen von Dynamics 365, einschließlich des Webclients für Mobilgeräte und der offiziellen Business Central-App.

> [!NOTE]
> Nicht alle Document Capture-Funktionen sind auf Mobilgeräten sichtbar oder zugänglich. Selbst wenn Funktionen auf mobilen Geräten verwendet werden können, sieht die Benutzeroberfläche auf Mobilgeräten möglicherweise deutlich anders aus als die entsprechende Oberfläche auf Ihrem Desktop-Computer. Der Zugriff auf bestimmte Funktionen kann auf mobilen Geräten ebenfalls anders sein. Beispielsweise wird die ursprüngliche PDF- oder XML-Datei auf Mobilgeräten nicht angezeigt. Sie können sie jedoch über das Menü **Dokument** in der Aktionsleiste herunterladen.

Das Continia Web Approval Portal wird nahezu vollständig auf Mobilgeräten unterstützt, insbesondere für die Genehmigung von Dokumenten. Eine besondere Ausnahme sind formatierte XML-Dateien, die im Portal im mobilen Modus nicht angezeigt werden. Wenn Sie eine XML-Datei auf einem mobilen Gerät anzeigen möchten, wird empfohlen, im Browser auf Ihrem Mobilgerät in den Desktop-Modus zu wechseln. Das Web Approval Portal ist ein separater Continia-Client, der außerhalb von Business Central verwendet wird. Weitere Informationen finden Sie unter [Mindestanforderungen für die Verwendung von Document Capture](@DC-453#continia-web-approval-portal) (Online) und [Anforderungen für die Verwendung des Continia Web Approval Portals On-Premises](@DC-454) (On-Premises).

## RemoteApps

Die meisten Document Capture-Funktionen funktionieren mit Windows Server RemoteApps, obwohl dies nicht offiziell unterstützt wird.

> [!NOTE]
> Bei Verwendung von Document Capture mit RemoteApps sind nicht alle Document Capture-Funktionen funktionsfähig. Beispielsweise funktioniert die Drag & Drop-Funktion von Document Capture nicht wie vorgesehen, da RemoteApps das Ziehen und Ablegen von Dateien im Ablagebereich nicht zulässt. Alternativ können Sie Dateien mit der Funktion zum Durchsuchen hinzufügen.

## Technische E-Mail-Anforderungen

Um ein Dokument in Document Capture zu importieren, müssen Sie es als PDF- oder XML-Datei an eine E-Mail anhängen und die E-Mail dann an eine vordefinierte Continia-E-Mail-Adresse senden. Die E-Mails für den Import von Dokumenten müssen eine Reihe technischer Anforderungen erfüllen, die im Folgenden aufgeführt sind:

- Es werden nur ungelesene E-Mails verarbeitet.
- Verschlüsselte E-Mails und das interne Microsoft Exchange-E-Mail-Format TNEF werden nicht unterstützt.
- Nur PDF- und XML-Dateien werden unterstützt. Es können keine anderen Dateien verarbeitet werden, einschließlich verschlüsselter, passwortgeschützter und komprimierter Dateien (z. B. ZIP-Dateien).
- Die PDF- oder XML-Dateien müssen direkt an die E-Mail angehängt sein. Nur Dateien, die direkt an die E-Mail angehängt sind, werden verarbeitet.
- Archivierte oder verschlüsselte Dateien, die PDF- oder XML-Dateien enthalten, werden nicht verarbeitet.
- PDF- oder XML-Dateien, die als Link im E-Mail-Text verfübar sind, werden ignoriert.
- PDF- oder XML-Dateien, die im E-Mail-Text eingebettet sind, werden ignoriert.
- Dateinamen dürfen 199 Zeichen nicht überschreiten.
- Die maximale E-Mail-Größe für Continia Online-OCR beträgt 20 MB.
- Die maximale Anzahl der Seiten, die bei PDF-Dateien verarbeitet werden können, beträgt 500.

Wenn Sie eine E-Mail mit einer Fehlerbeschreibung erhalten möchten, wenn eine Anforderung nicht erfüllt ist, wenden Sie sich bitte an das Continia-Supportteam. Wenn eine PDF- oder XML-Datei die Anforderungen erfüllt, aber trotzdem nicht mit OCR verarbeitet werden kann, wird sie in der Spalte **Fehlerhafte Belege** angezeigt, die Sie unter **Continia Document Capture Aktivitäten** > **Bereit zum Import** finden. Dies kommt jedoch selten vor.

> [!WARNING]
> Nur ungelesene E-Mails werden für den Dokumentenimport heruntergeladen und anschließend als gelesen markiert. Gelesene E-Mails müssen manuell als ungelesen markiert werden, damit sie heruntergeladen werden.

> [!IMPORTANT]
> Dateiformate wie EXE, XLS und JPG werden ignoriert, aber eine als PDF gespeicherte schädliche Datei würde jedoch dennoch von Document Capture verarbeitet. Daher müssen Sie sicherstellen, dass Ihr Antivirenprogramm, beispielsweise Microsoft Defender Antivirus, auf dem neuesten Stand ist, wenn Sie Dateien auf Ihre Server herunterladen. Wenn Sie eine Business Central-Cloudumgebung verwenden, wenden Sie sich an Microsoft, um zu erfahren, wie Ihre Umgebung geschützt ist.

## Business Central-Add-In für Outlook

Die meisten Document Capture-Funktionen funktionieren im Business Central-Add-In für Outlook, obwohl dies nicht offiziell unterstützt wird.

Zum Beispiel funktioniert der Dateidownload nicht für Versionen, die älter als Business Central 2022 Release Wave 1 (BC v20) sind. Dies wird jedoch für BC v20 und später unterstützt.

## Informationen zum Thema

[Mindestanforderungen für die Verwendung von Continia Document Capture](@DC-453)  
[Mindestanforderungen für die Verwendung von Continia Document Capture On-Premises](/Continia Document Capture/Development and Administration/On-Premises/Deployment/Minimum Requirements.md)  
[Mindestanforderungen für die Verwendung des Continia Web Approval Portals On-Premises](@DC-454)  
[Business Central-Website](https://dynamics.microsoft.com/business-central/overview/)