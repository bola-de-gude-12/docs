---
title: Zugriff auf den Quellcode in Document Capture
description:
date: 16-06-2025
id: DC-485
lang: de
---

# Zugriff auf den Quellcode

Continia ist bewusst, dass der Zugriff auf den Quellcode unserer Apps zu Test-, Integrations- oder Problemlösungszwecken erforderlich ist. Um auf den Quellcode zuzugreifen, gehen Sie folgendermaßen vor:

1. Gehen Sie zur [Continia PartnerZone](https://partnerzone.continia.com/) > **Downloads** und laden Sie das entsprechende Produktpaket herunter.
2. Extrahieren Sie das Produktpaket in einen Ordner auf Ihrem Computer.
3. Klicken Sie auf den Ordner **App** und dann auf den Ordner **Source**.
4. Wählen Sie die ZIP-Datei aus, die Ihrer Microsoft Dynamics 365 Business Central (BC)-Version entspricht, einschließlich des richtigen kumulativen Updates.
5. Extrahieren Sie die benötigten Dateien.

Beachten Sie, dass der Ordner **Source** zwei verschiedene Arten von ZIP-Dateien mit dem Document Capture-Quellcode enthält:

- Eine Datei für alle Basisfunktionen, mit dem Namen „DC [Versionsnummer] – [BC-Versionsnummer] (BC-Handelsname) Source.zip“ (zum Beispiel **DC 9.0.0.0 – 19 (BC 2021 Wave 2) Source.zip**)
- Eine Datei für On-Premises-Funktionalität mit dem Namen „DC on-premises [Versionsnummer] – [BC-Versionsnummer] (BC-Handelsname) Source.zip“ (zum Beispiel **DC on-premises 9.0.0.0 – 19 (BC 2021 Wave 2) Source.zip**)

Die Basis-App wird sowohl für Cloud- als auch für On-Premises-Bereitstellungen verwendet. Beachten Sie jedoch, dass Sie für On-Premises-Installationen sowohl die Basis-App als auch die On-Premises-App benötigen.

> [!NOTE]
> Wenn Sie nach den Quellcodedateien in einem älteren Produktpaket suchen, befinden sie sich möglicherweise in einem anderen Ordner: Ordner **App** > Ordner der entsprechenden Business Central-Version > Ordner **Document Capture**.