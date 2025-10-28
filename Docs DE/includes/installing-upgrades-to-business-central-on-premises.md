Wenn Sie Microsoft Dynamics 365 Business Central On-Premises, aber _nicht_ Continia {param1}aktualisieren möchten, müssen Sie alle Continia-Apps deinstallieren und deren Veröffentlichung aufheben, bevor Sie das Business Central-Upgrade installieren. Dies gilt sowohl für größere als auch für kleinere (kumulative) Upgrades.

Der Grund dafür ist, dass Continia-Apps als Runtime Packages verteilt werden und deren Funktion nur dann garantiert ist, wenn sie auf einer Plattform mit derselben Version veröffentlicht werden, auf der sie erstellt wurden. Continia gibt Apps als Runtime Packages heraus, da jede Erweiterung in einem Runtime Package – in diesem Fall die App Continia {param1} – auf Servern installiert werden kann, die nicht über eine Entwicklerlizenz verfügen. Weitere Informationen finden Sie in diesem [Microsoft-Artikel](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-creating-runtime-packages).

> [!NOTE] Wenn Sie Business Central und Continia {param1} gleichzeitig aktualisieren, können Sie die Apps in der von Ihnen bevorzugten Reihenfolge aktualisieren.

Beachten Sie, dass Continia Code für alle verfügbaren kumulativen Updates (CUs) für Business Central veröffentlicht, wenn eine Version von Continia {param1} veröffentlicht wird (gilt sowohl für Hauptversionen als auch für Service Packs). Jedes neu veröffentlichte CU von Microsoft wird erst ab dem nächsten von Continia veröffentlichten Service Pack unterstützt. Wenn Sie auf ein derzeit nicht unterstütztes Business Central CU aktualisieren müssen – beispielsweise auf das neueste – und nicht warten können, bis Continia ein Service Pack veröffentlicht, das dies unterstützt, wenden Sie sich bitte an das Continia-Supportteam, indem Sie ein Supportticket erstellen. Continia stellt Ihnen dann ein voll funktionsfähiges Paket bereit, das das entsprechende Business Central CU unterstützt.

## Erforderliche Schritte für Continia {param1} vor dem Business Central-Upgrade

Bevor Sie Business Central On-Premises aktualisieren, müssen Sie Continia {param1} deinstallieren und die Veröffentlichung aufheben. Dabei _müssen_ Sie darauf achten, dass dies in der in der folgenden Tabelle beschriebenen Reihenfolge durchgeführt wird.

Wenn Sie das Produkt deinstalliert und die Veröffentlichung aufgehoben und Business Central aktualisiert haben, müssen Sie es erneut veröffentlichen und neu installieren. Beides muss in der in der folgenden Tabelle beschriebenen Reihenfolge durchgeführt werden.

> [!IMPORTANT]
> Vermeiden Sie es, [Repair-NAVApp cmdlet](https://docs.microsoft.com/en-us/powershell/module/microsoft.dynamics.nav.apps.management/repair-navapp?view=businesscentral-ps-19) auszuführen. Die Continia-Apps sind vorkompiliert und das Ausführen dieses Cmdlets gibt einen Fehler zurück, da sie als Runtime Packages herausgegeben wurden.