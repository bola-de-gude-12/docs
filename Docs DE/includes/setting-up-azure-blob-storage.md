Continia {param1} bietet leistungsstarke Funktionen zur Archivierung von Belegdateien mit einfacher Integration in Azure Blob Storage. Um Azure Blob Storage zu verwenden, befolgen Sie die hier beschriebenen Prozesse in der angegebenen Reihenfolge.

## So richten Sie ein Speicherkonto und einen Container ein

Informationen zum Erstellen eines Azure Blob Storage-Kontos und eines Containers finden Sie unter [Erstellen eines Azure-Speicherkontos](https://learn.microsoft.com/de-de/azure/storage/common/storage-account-create) und [Autorisieren des Zugriffs auf Daten in Azure Storage](https://learn.microsoft.com/de-de/azure/storage/common/authorize-data-access) (Microsoft-Artikel).

> [!IMPORTANT]
> Achten Sie beim Einrichten Ihres Azure Blob Storage-Kontos darauf, dass die Eigenschaft **AllowBlobPublicAccess** auf **False** gesetzt ist. Dadurch wird ein bekanntes Sicherheitsrisiko vermieden, bei dem die Authentifizierung aller Blob-Datenanforderungen erzwungen wird. Weitere Informationen finden Sie unter [Overview: Remediating anonymous read access for blob data](https://learn.microsoft.com/en-us/azure/storage/blobs/anonymous-read-access-overview) (Microsoft-Artikel).

{param1} unterstützt keine Shared Access Signatures (SAS) in Azure Blob Storage. Daher müssen Sie im Feld **Speicherkontoschlüssel** einen Speicherkontozugriffsschlüssel eingeben.

## So richten Sie {param1} ein

So richten Sie die Lösung für Azure Blob Storage ein:

1. Suchen Sie {{search}} nach **{param1} Einrichtung** und wählen Sie dann den entsprechenden Link aus.
2. Klicken Sie unter **Allgemein** > **Dokumentspeicherart** auf **Azure Blob Storage**, um die Gruppe mit Einstellungen für **Azure Blob Storage** zu öffnen.
3. Geben Sie in den Feldern **Speicherkontoname**, **Speicherkontoschlüssel** und **Name des Blob-Containers** die entsprechenden Werte ein, die Sie beim Einrichten des Speicherkontos und Containers erhalten haben.