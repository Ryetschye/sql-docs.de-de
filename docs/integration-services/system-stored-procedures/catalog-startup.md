---
description: catalog.startup
title: catalog.Startup | Microsoft-Dokumentation
ms.custom: ''
ms.date: 03/04/2017
ms.prod: sql
ms.prod_service: integration-services
ms.reviewer: ''
ms.technology: integration-services
ms.topic: language-reference
ms.assetid: 271fd405-246a-4852-bfbe-f557241ce6ea
author: chugugrace
ms.author: chugu
ms.openlocfilehash: d3ad08806328cbeb1e99ff997db9dc6593ce9430
ms.sourcegitcommit: 192f6a99e19e66f0f817fdb1977f564b2aaa133b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/25/2020
ms.locfileid: "96129601"
---
# <a name="catalogstartup"></a>catalog.startup 

[!INCLUDE[sqlserver-ssis](../../includes/applies-to-version/sqlserver-ssis.md)]


[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  Führt eine Wartung des Status von Vorgängen für den SSISDB-Katalog aus.  
  
 Durch die gespeicherte Prozedur wird der Status aller Pakete korrigiert, die während des Ausfalls (falls zutreffend) der [!INCLUDE[ssIS](../../includes/ssis-md.md)]-Serverinstanz ausgeführt wurden.  
  
 Sie haben die Möglichkeit, die gespeicherte Prozedur automatisch ausführen zu lassen, sobald die [!INCLUDE[ssIS](../../includes/ssis-md.md)]-Serverinstanz neu gestartet wird. Dazu wählen Sie im Dialogfeld **Katalog erstellen** die Option **Automatische Ausführung gespeicherter Integration Services-Prozeduren beim Starten von SQL Server aktivieren** aus.  
  
## <a name="syntax"></a>Syntax  
  
```sql  
catalog.startup  
```  
  
## <a name="return-code-value"></a>Rückgabecodewert  
 0 (Erfolg)  
  
## <a name="result-sets"></a>Resultsets  
 Keine  
  
## <a name="permissions"></a>Berechtigungen  
 Diese gespeicherte Prozedur erfordert eine der folgenden Berechtigungen:  
  
-   READ-Berechtigung und MODIFY-Berechtigung für die Instanz der Ausführung, READ-Berechtigung und EXECUTE-Berechtigung für das Projekt und ggf. READ-Berechtigungen für die Umgebung, auf die verwiesen wird  
  
-   Mitgliedschaft in der Datenbankrolle **ssis_admin**  
  
-   Mitgliedschaft in der Serverrolle **sysadmin**  
  
  
