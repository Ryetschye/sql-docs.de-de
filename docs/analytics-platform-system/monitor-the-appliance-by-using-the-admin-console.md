---
title: Überwachen mit der Verwaltungskonsole
description: Für Analytics Platform System ist die Verwaltungskonsole eine Webanwendung, die den Status, die Integrität und die Leistungsinformationen des Geräts übersteigt. Benutzer stellen über einen Internetbrowser eine Verbindung mit der Verwaltungskonsole her.
author: mzaman1
ms.prod: sql
ms.technology: data-warehouse
ms.topic: conceptual
ms.date: 04/17/2018
ms.author: murshedz
ms.reviewer: martinle
ms.custom: seo-dt-2019
ms.openlocfilehash: 88e1619ce37de7c7a334ee7d915115f2deef47ef
ms.sourcegitcommit: 591bbf4c7e4e2092f8abda6a2ffed263cb61c585
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/22/2020
ms.locfileid: "86941072"
---
# <a name="monitor-the-appliance-with-the-admin-console---analytics-platform-system"></a>Überwachen der Appliance mit der Verwaltungskonsole: Analytics Platform System
Bei der Verwaltungskonsole handelt es sich um eine SQL Server PDW Webanwendung, die den Status, die Integrität und die Leistungsinformationen des Geräts. Benutzer stellen über Internet Explorer eine Verbindung mit der Verwaltungskonsole her.  
  
## <a name="about-the-admin-console"></a><a name="About"></a>Informationen zur Verwaltungskonsole  
![Anwendungskonsole, Home](./media/monitor-the-appliance-by-using-the-admin-console/SQL_Server_PDW_AdminConsol_ApplHome.png "SQL_Server_PDW_AdminConsol_ApplHome")  
  
**Appliance**  
Startseite  
Bietet eine kurze Zusammenfassung des Geräte Zustands.  
  
Gesundheitswesen  
Zeigt die Geräte Topologie mit Indikatoren an, die die Integrität der einzelnen überwachten Komponenten innerhalb der einzelnen Knoten anzeigen. Mit dieser Option können Sie den aktuellen Status einzelner Knoten und Eigenschaften der Knoten Komponenten anzeigen.  
  
Zeigt Hardware-und Software Warnungen an.  
  
Systemmonitor  
Zeigt System Monitor Diagramme an.  
  
**Parallel Data Warehouse**  
Startseite  
Bietet eine kurze Zusammenfassung des PDW-Zustands.  
  
Sitzungen  
Zeigt aktive PDW-Benutzersitzungen an. Dies kann bei der Überwachung von Ressourcenkonflikten helfen.  
  
Abfragen  
Zeigt eine Liste der ausgelaufenden Abfragen und kürzlich abgeschlossenen Abfragen an. Sie zeigt ggf. zugehörige Fehler an. Bietet außerdem die Möglichkeit, Details zum Abfrage Ausführungsplan und zu den Knoten Ausführungs Informationen anzuzeigen.  
  
Lädt  
Zeigt Lade Pläne, den aktuellen Status von PDW-Ladevorgängen und ggf. zugehörige Fehler an.  
  
Sicherungen/Wiederherstellungen  
Zeigt ein Protokoll von PDW-Sicherungs-und Wiederherstellungs Vorgängen an.  
  
Gesundheitswesen  
Zeigt die PDW-Topologie mit Indikatoren an, die die Integrität der einzelnen überwachten Komponenten innerhalb der einzelnen Knoten anzeigen. Mit dieser Option können Sie den aktuellen Status einzelner Knoten und Eigenschaften der Knoten Komponenten anzeigen.  
  
Zeigt Hardware-und Software Warnungen an.  
  
Ressourcen  
Zeigt eine Liste von PDW-Ressourcen sperren und deren aktuellen Status an.  
  
Storage  
Fasst die PDW-Speicherauslastung zusammen.  
  
Systemmonitor  
Zeigt die PDW-Leistungs Monitor Diagramme an.  
 
> [!NOTE]  
> Die Verwaltungskonsole weist eine Bildschirmauflösung von 1024 x 768 auf. Die Verwaltungskonsole wird am besten mit einer Bildschirmauflösung von 1280 X 1024 oder höher angezeigt.  
  
## <a name="connect-to-the-admin-console"></a><a name="Connect"></a>Herstellen einer Verbindung mit der Verwaltungskonsole  
Zum Herstellen einer Verbindung mit der Verwaltungskonsole ist Folgendes erforderlich:  
  
-   Mindestens Internet Explorer Version 10.  
  
-   Berechtigungen für den Zugriff auf die Verwaltungskonsole. <!-- MISSING LINKS See [Grant Permissions to Use the Admin Console &#40;SQL Server PDW&#41;](../sqlpdw/grant-permissions-to-use-the-admin-console-sql-server-pdw.md).  -->  
  
-   Die IP-Adresse des Steuerelement Knoten Clusters.  Erhalten Sie dies von Ihrem SQL Server PDW-Administrator.  
  
Zum Herstellen einer Verbindung mit der Verwaltungskonsole verwenden Sie Internet Explorer und HTTPS, um die IP-Adresse des Steuerelement Knoten Clusters zu suchen. Wenn z. b. die IP-Adresse des Steuerelement Knoten Clusters ist `10.192.63.102` , geben Sie `https://10.192.63.102` in die Adressleiste Ihres Browsers ein. Der erste Bildschirm fordert ihren **Anmelde** Namen und Ihr **Kennwort**an. Geben Sie entweder einen Anmelde Namen und ein Kennwort für die SQL Server-Authentifizierung oder einen Anmelde Namen für die Windows-Authentifizierung und Wenn Sie einen Anmelde Namen für die Windows-Authentifizierung verwenden, verwendet die Verwaltungskonsole den Identitätswechsel.  
  
## <a name="admin-console-tasks"></a><a name="RelatedTasks"></a>Aufgaben der Verwaltungskonsole  
Die Verwaltungskonsole bietet die Möglichkeit, Folgendes zu überwachen:  
  
|Informationstyp|Zugreifen auf die Verwaltungskonsole|
|-|-|
|Gesamtstatus des Geräts|Klicken Sie im Menü oben auf **Appliance State** ( **Startseite**).|  
|Warnungen|Klicken Sie auf **Warnungen**. Weitere Informationen finden Sie Untergrund Legendes zu Warnungen in der [Administrator Konsole &#40;Analytics Platform System&#41;](understanding-admin-console-alerts.md).|  
|Gerätekomponenten und deren Status|Klicken Sie im Menü oben auf **Appliance State** ( **Startseite**).|  
|Überwachen von Anforderungen (einschließlich Abfragen, Ladungen, Sicherungen und Wiederherstellungen)|Klicken Sie auf **Sitzungen** , um die derzeit aktiven oder letzten Sitzungen anzuzeigen.<br /><br />Klicken Sie auf **Abfragen** , um die derzeit aktiven oder aktuellen Abfragen anzuzeigen. Die für Abfragen angezeigten Informationen umfassen Ladungen, Sicherungen und Wiederherstellungen.<br /><br />Klicken Sie auf **Sperren** , um aktive Sperren anzuzeigen.|  
|Überwachen zusätzlicher Informationen zu Lasten, Sicherungen und Wiederherstellungen.|Klicken **Sie** auf Ladevorgänge oder **Sicherungen/** Wiederherstellungen.|  
|Leistungsinformationen|Klicken Sie auf System **Monitor**.|  
  
## <a name="see-also"></a>Weitere Informationen  
[Geräteüberwachung &#40;Analytics-Platt Form System&#41;](appliance-monitoring.md)  
  
