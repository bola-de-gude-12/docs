Es besteht ein erheblicher Unterschied darin, ob Sie Document Capture in der On-Premises-Version von Microsoft Dynamics 365 Business Central oder in der Online-Version ausführen. In diesem Artikel werden die Mindestanforderungen und Aspekte beschrieben, die bei der Nutzung von Document Capture in Business Central Online zu beachten sind. Die On-Premises-Anforderungen finden Sie unter [Mindestanforderungen für die Verwendung von Continia Document Capture On-Premises](@DC-135).

> [!IMPORTANT]
> Da Document Capture ein integrierter Bestandteil von Business Central ist, gelten die [Mindestanforderungen für Business Central](https://learn.microsoft.com/de-de/dynamics365/business-central/product-requirements) (Microsoft-Artikel) auch für Document Capture.

## Anforderungen für lokale Scanner

Document Capture unterstützt das Scannen von Dokumenten mit einem lokalen Desktopscanner, der an einen Computer angeschlossen ist. Hierzu ist die Installation einer separaten Continia-Anwendung sowie die Verwendung eines TWAIN-kompatiblen Scanners erforderlich. Wenn Sie den Business Central-Webclient verwenden, werden sowohl 32- als auch 64-Bit-Versionen des TWAIN-Scannertreibers unterstützt. Beachten Sie jedoch, dass 32-Bit-TWAIN-Scannertreiber nur in Document Capture 2021 R1 Service Pack 2 und spätere Versionen unterstützt werden. Weitere Informationen, wie Sie den Document Capture Scanner Service als eine 32-Bit-Anwendung ausführen können, finden Sie unter [How to alter the Document Capture Scanner Service to run as 32-bit application](https://continia.zendesk.com/hc/en-us/articles/360022114180-How-to-alter-the-Document-Capture-Scanner-Service-to-run-as-32-bit-application).

> [!NOTE]
> Wenn Sie mehrere Dokumente auf einmal scannen, müssen Sie jedes Dokument durch eine leere Seite trennen.

## E-Mail-Anforderungen

Sie können Dokumente (bzw. Belege) in Document Capture importieren, indem Sie sie einfach per E-Mail an eine von Continia vorgegebene E-Mail-Adresse senden. Informationen zu den technischen Anforderungen und wichtige Hinweise finden Sie unter [Zusätzliche Richtlinien für die Verwendung von Continia Document Capture](@DC-452).

## PDF-Anforderungen

Wenn Sie PDF-Dokumente in Document Capture importieren, wird empfohlen, jedes Dokument als separate PDF-Datei zu senden. Es ist jedoch möglich, eine aus mehreren Dokumenten bestehende [PDF-Datei automatisch aufzuteilen](/Continia Document Capture/Business functionality/Documents and templates/Splitting and merging documents.md), basierend auf verschiedenen Kriterien, wie zum Beispiel Barcode oder Rechnungsnummer.

Die PDF-Datei muss der Version PDF 1.7 oder früher sowie dem PDF/A-Standard entsprechen. Handschriftlicher Text wird nicht unterstützt und wahrscheinlich nicht gut erkannt.

Darüber hinaus gelten folgende Einschränkungen:

- Verschlüsselte/passwortgeschützte PDF-Dateien werden nicht unterstützt.
- PDF-Dateien mit elektronischen Signaturen werden möglicherweise erfolgreich verarbeitet, werden jedoch im Allgemeinen nicht unterstützt.
- PDF-Dateien im XFA-Format von Adobe (XML Forms Architecture) werden nicht unterstützt.
- Die maximale Anzahl der Seiten, die bei PDF-Dateien verarbeitet werden können, beträgt 500.

Um Dateien mit diesen Eigenschaften verarbeiten zu können, müssen Sie sie als neue PDF-Dateien erstellen. Dies ist beispielsweise mit der Option Microsoft Print to PDF möglich, die in Windows kostenlos verfügbar ist. Wenn Sie neue PDFs erstellen, werden zusätzliche Funktionen entfernt und „einfache“ PDF-Dateien ohne interaktive Elemente erstellt.

## Continia Web Approval Portal

Dokumente können entweder über den Business Central-Webclient oder das Continia Web Approval Portal genehmigt werden. Das Web Approval Portal basiert auf der standardmäßigen Genehmigungsfunktionalität von Business Central. Es handelt sich jedoch um einen separaten Service, auf den lizenzierte Benutzer von allen unterstützten Webbrowsern aus zugreifen können. [Die Webbrowser, die für Continia Document Capture unterstützt werden](/continia-document-capture/getting-started/frequently-asked-questions/minimum-requirements/additional-guidelines#browsers), werden auch für das Web Approval Portal unterstützt.

Das Web Approval Portal wird bis auf wenige Ausnahmen auf Mobilgeräten unterstützt. Eine besondere Ausnahme sind formatierte XML-Dateien, die im Portal im mobilen Modus nicht angezeigt werden. Wenn Sie eine XML-Datei auf einem mobilen Gerät anzeigen möchten, wechseln Sie im Browser auf Ihrem Mobilgerät in den Desktop-Modus.

> [!NOTE]
> Das Web Approval Portal kann entweder von Continia (continiaonline.com) oder auf einem lokalen Server gehostet werden. Der Zugriff erfolgt in beiden Fällen über einen Webbrowser; der Unterschied besteht also nur beim Hosting. Sie können die auf einem lokalen Server gehostete Version des Web Approval Portals nicht in Kombination mit Business Central Online verwenden; nur die von Continia gehostete Version des Web Approval Portals kann in Verbindung mit Business Central Online verwendet werden.

Um auf das Web Approval Portal zugreifen zu können, müssen Sie ein authentifizierter Business Central-Benutzer sein und über eine Lizenz für benannte Benutzer für Business Central verfügen. Eine „Named-User-License“ ist eine separate Abonnementlizenz (Subscription License, SL), die an einen bestimmten Benutzer gebunden ist und nicht mit anderen geteilt werden kann, im Gegensatz zu [Concurrent-User-Lizenzen](https://de.wikipedia.org/wiki/Concurrent_user). Benutzer-SLs sind der primäre Lizenztyp für Business Central.

Für Genehmigungsbenutzer, die nur Dokumente genehmigen und Einkaufszeilen ändern, sind Team Member-Lizenzen ausreichend, vorbehaltlich der Microsoft-Lizenzbedingungen (siehe unten). In allen anderen Fällen unterstützt Continia nur Benutzer mit Essentials- oder Premium-Lizenzen. Informationen zu Team Member-Lizenzen und wie sich Add-Ons auf deren Nutzung auswirken können, finden Sie im Microsoft Dynamics 365 Business Central Licensing Guide. Sie können dieses Handbuch auf der [Business Central](https://dynamics.microsoft.com/business-central/overview/)-Website herunterladen.

Benutzer des Web Approval Portals können auch automatisch auf Business Central zugreifen, sobald ihnen eine Team Member-Lizenz zugewiesen wurde. Das Web Approval Portal ist auf der Standardfunktionalität von Business Central aufgebaut, wodurch sich der Zugriff auf Business Central ergibt.

> [!IMPORTANT]
> Konsultieren Sie immer die Microsoft-Lizenzbedingungen, um sich mit den rechtlichen Anforderungen vertraut zu machen, unabhängig davon, wie diese in Continia Docs oder in einer anderen Continia-Dokumentation interpretiert werden. Dabei möchten wir insbesondere auf den Abschnitt **Team Members** im Business Central Licensing Guide hinweisen, der auf der [Business Central](https://dynamics.microsoft.com/business-central/overview/)-Website zum Download verfügbar ist.

Ab Version 1.16.0 kann das Web Approval Portal gleichzeitig eine Verbindung zu mehreren NAV- und/oder Business Central-Datenbanken herstellen, sodass sich Benutzer aus verschiedenen Datenbanken zur gleichen Zeit anmelden können.

Keine der früheren Versionen des Web Approval Portals unterstützen jedoch die gleichzeitige Anmeldung von Benutzern aus verschiedenen Datenbanken. Wenn Ihre Organisation über mehr als eine Datenbank in Business Central verfügt und Benutzer aus einer dieser Datenbanken in das Web Approval Portal exportiert, können sich nur diese neu exportierten Benutzer beim Web Approval Portal anmelden. Alle vorhandenen Benutzer, die zuvor aus einer anderen Datenbank exportiert wurden, werden aus dem Web Approval Portal gelöscht und können sich nicht anmelden.

> [!NOTE]
> Sicherheitsfilter werden derzeit im Web Approval Portal nicht unterstützt. Um festzulegen, welcher Inhalt für Benutzer im Portal sichtbar und zugänglich ist, verwenden Sie stattdessen Berechtigungen für Konten und Dimensionen. Diese können für [individuelle Benutzer](/continia-document-capture/setting-up-document-capture/setting-up-document-approval/continia-user-setup-for-approvals#konten--und-dimensionsberechtigungen-konfigurieren) oder für [Benutzergruppen](/continia-document-capture/setting-up-document-capture/setting-up-document-approval/approval-user-groups#so-konfigurieren-sie-konten--und-dimensionsberechtigungen-fur-eine-gruppe) konfiguriert werden.

## Azure Blob Storage

Für neuere Versionen von Microsoft Dynamics NAV/Business Central (NAV 2013 oder später) unterstützt Document Capture die Archivierung von Dokumentdateien mit Azure Blob Storage. Weitere Informationen zu Azure Blob Storage, einschließlich Informationen zu Preisen und Konfiguration, finden Sie unter [Azure Blob Storage](https://azure.microsoft.com/de-de/services/storage/blobs/) (Microsoft-Artikel).

Damit Azure Blob Storage funktioniert, muss die Dynamics NAV/Business Central-Dienstebene für die Verwendung des TLS 1.2-Sicherheitsprotokolls konfiguriert sein. Weitere Informationen finden Sie unter [Azure Blob Storage einrichten](/Continia Document Capture/Development and Administration/Setting up Azure Blob storage.md).

> [!IMPORTANT]
> Es wird dringend empfohlen, dass Sie für Ihre Azure Blob Storage-Konten [vorläufiges Löschen für Blobs](https://docs.microsoft.com/de-de/azure/storage/blobs/soft-delete-blob-overview) aktivieren, da Sie so alle Dokumente oder Dateien wiederherstellen können, die versehentlich gelöscht oder überschrieben wurden.

> [!CAUTION]
> Es ist wichtig, dass Document Capture vollständigen Lese-/Schreib-/Löschzugriff auf den entsprechenden Blob-Container hat. So wird zum Beispiel die Konfiguration von Zugriffsrichtlinien mit zeitbasierter Aufbewahrung nicht unterstützt, ebenso wenig wie Unveränderlichkeit und die Aufbewahrung für juristische Zwecke.

Continia hat keine weiteren Mindestanforderungen für die Verwendung von Azure Blob Storage zum Speichern von Document Capture-Dateien. Wenn Sie Fragen oder Anforderungen hinsichtlich Azure haben, zum Beispiel in Bezug auf Einrichtung, Abonnementtypen und die allgemeine Architektur, wenden Sie sich bitte an Microsoft.

## Zusätzliche Richtlinien

Es gibt noch eine Reihe weiterer Anforderungen und Empfehlungen, die sich auf die Leistung von Document Capture und die Verwendung der App auswirken. Weitere Informationen finden Sie unter [Zusätzliche Richtlinien für die Verwendung von Continia Document Capture](../additional-guidelines).

## Informationen zum Thema

[Zusätzliche Richtlinien für die Verwendung von Continia Document Capture](../additional-guidelines)  
[Funktionsüberblick](/Continia Document Capture/Getting Started/Business Functionality.md)  
[Nicht unterstützte Standardfunktionen](@DC-134)  
[Business Central-Website](https://dynamics.microsoft.com/business-central/overview/)