---
description: Ergänzendes Oracle-Protokollierungsskript
title: Ergänzendes Oracle-Protokollierungsskript | Microsoft-Dokumentation
ms.custom: ''
ms.date: 03/01/2017
ms.prod: sql
ms.prod_service: integration-services
ms.reviewer: ''
ms.technology: integration-services
ms.topic: conceptual
ms.assetid: 5e6ee618-b89b-46c7-92ad-4fc5ef7b777a
author: chugugrace
ms.author: chugu
ms.openlocfilehash: ec1835467ed0fb3ac23d570d26d8416cd83521b5
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "88425992"
---
# <a name="oracle-supplemental-logging-script"></a>Ergänzendes Oracle-Protokollierungsskript

[!INCLUDE[sqlserver-ssis](../../includes/applies-to-version/sqlserver-ssis.md)]


  In diesem Dialogfeld wird das ergänzende Oracle-Protokollierungsskript angezeigt.  
  
 Wenn Sie eine CDC-Instanz für die Verwendung vorbereiten, erstellt der CDC Designer ein Oracle SQL-Skript, mit dem die ergänzende Protokollierung für die aufzuzeichnenden Tabellen eingerichtet wird. Das ergänzende Protokollierungsskript weist Oracle an, dass beim Aktualisieren einer bestimmten Tabelle die Änderungsdatensätze, die in das Transaktionsprotokoll geschrieben werden, die Daten aller wichtigen Spalten enthalten sollen, nicht nur die Spalten, die sich geändert haben.  
  
 Je nach den Oracle DBA-Richtlinien in Ihrer Organisation kann es erforderlich sein, dass beim Ausführen des ergänzenden Protokollierungsskripts eine Überprüfung und Genehmigung durch einen Oracle-Datenbankadministrator erfolgt.  
  
## <a name="options"></a>Optionen  
 Sie können die folgenden Optionen verwenden, um festzulegen, wie das Skript ausgeführt wird.  
  
 **Skript ausführen**  
 Führt das ergänzende Protokollierungsskript für die Tabellen aus, die für die CDC-Instanz definiert wurden. Zum Ausführen dieses Skripts muss der Oracle-Benutzer über die ALTER TABLE-Berechtigung für alle zu erfassenden Tabellen und die SELECT-Berechtigung für die DBA_LOG_GROUPS-Sicht verfügen. Außerdem muss der Oracle-Benutzer die Anmeldeinformationen für eine Oracle-Datenbankverwendung mit den erforderlichen Berechtigungen besitzen. Sie können auf die Aufforderung des Programms zur Eingabe der Oracle-Anmeldeinformationen warten, und dann die Ausführung des Skripts folgen lassen.  
  
 **Speichern unter**  
 Speichert das Skript als Textdatei. Diese Option wird verwendet, wenn ein Oracle-Datenbankadministrator das ergänzende Protokollierungsskript untersuchen und ausführen muss und wenn das Programm das Speichern des Skripts in einer Textdatei zulässt, die Sie später per E-Mail an den Oracle-Datenbankadministrator senden oder auf andere Art für die spätere Ausführung bereitstellen können (mithilfe des SQL*Plus Oracle-Hilfsprogramms oder eines anderen Tools zum Ausführen von Skripts für eine Oracle-Datenbank).  
  
 **Kopieren**  
 Kopiert das Skript in die Zwischenablage. Nach Abschluss des Vorgangs können Sie das Skript an jedem erforderlichen Speicherort einfügen, falls ein Oracle-Datenbankadministrator das ergänzende Protokollierungsskript untersuchen und ausführen muss.  
  
## <a name="see-also"></a>Siehe auch  
 [How to Manage a CDC Instance](../../integration-services/change-data-capture/how-to-manage-a-cdc-instance.md)   
 [Verwalten einer CDC-Instanz](../../integration-services/change-data-capture/manage-a-cdc-instance.md)  
  
  
