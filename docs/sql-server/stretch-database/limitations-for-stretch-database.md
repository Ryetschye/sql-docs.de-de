---
description: Einschränkungen für Stretch Database
title: Einschränkungen für Stretch Database
ms.date: 06/14/2016
ms.service: sql-server-stretch-database
ms.reviewer: ''
ms.topic: conceptual
helpviewer_keywords:
- Stretch Database, limitations
- Stretch Database, blocking issues
- limitations (Stretch Database)
- blocking issues (Stretch Database)
ms.assetid: 2b1fbec1-7859-44fc-8417-724fc57a59c0
author: rothja
ms.author: jroth
ms.custom: seo-dt-2019
ms.openlocfilehash: c53fe235850dbb932e5773c82cc22cc19d62e749
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "88454353"
---
# <a name="limitations-for-stretch-database"></a>Einschränkungen für Stretch Database
[!INCLUDE [sqlserver2016-windows-only](../../includes/applies-to-version/sqlserver2016-windows-only.md)]


  Erfahren Sie mehr zu Einschränkungen für Stretch-aktivierten Tabellen und zu Einschränkungen, die derzeit verhindern, Stretch für eine Tabelle zu aktivieren.  
  
##  <a name="limitations-for-stretch-enabled-tables"></a><a name="Caveats"></a> Einschränkungen für Tabellen, für die Stretch aktiviert ist  
  
Die folgenden Einschränkungen für Stretch-aktivierte Tabellen sind zu beachten.  
  
### <a name="constraints"></a>Einschränkungen  
-   Für UNIQUE-Einschränkungen und PRIMARY KEY-Einschränkungen wird in der Azure-Tabelle,die die migrierten Daten enthält, keine Eindeutigkeit erzwungen.  
  
### <a name="dml-operations"></a>DML-Vorgänge  
-   Sie können Zeilen, die für die Migration geeignet sind, mit der UPDATE- oder DELETE-Anweisung in einer Stretch-aktivierten Tabelle oder einer Sicht, die Stretch-aktivierte Tabellen enthält, aktualisieren oder löschen.  
  
-   In eine Stretch-aktivierte Tabelle auf einem Verbindungsserver können Zeilen nicht mit INSERT eingefügt werden.  
  
### <a name="indexes"></a>Indizes  
-   Für eine Sicht, die Stretch-aktivierte Tabellen enthält, kann kein Index erstellt werden.  
  
-   Filter für [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] -Indizes werden nicht an die Remotetabelle weitergegeben.  
  
##  <a name="limitations-that-currently-prevent-you-from-enabling-stretch-for-a-table"></a><a name="Limitations"></a> Einschränkungen, die Sie derzeit vom Aktivieren von Stretch für eine Tabelle abhalten  
   
 Die folgenden Elemente verhindern derzeit die Aktivierung von Stretch für eine Tabelle.  
  
 ### <a name="table-properties"></a>Tabelleneigenschaften  
-   Tabellen, die mehr als 1.023 Spalten oder mehr als 998 Indizes enthalten  
  
-   FileTables, die FILESTREAM-Daten enthalten  
  
-   Tabellen, die repliziert sind oder die Änderungsnachverfolgung oder Change Data Capture aktiv verwenden  
  
-   Speicheroptimierte Tabellen  
  
### <a name="data-types"></a>Datentypen  
-   text, ntext und image  
  
-   timestamp  
  
-   sql_variant  
  
-   XML  
  
-   CLR-Datentypen, einschließlich „geometry“, „geography“, „hierarchyid“ sowie benutzerdefinierte CLR-Typen  
  
 ### <a name="column-types"></a>Spaltentypen  
 -   COLUMN_SET  
  
-   Berechnete Spalten  
  
### <a name="constraints"></a>Einschränkungen  
-   Default- und CHECK-Einschränkungen  
  
-   FOREIGN KEY-Einschränkungen, die auf die Tabelle verweisen. In einer Über-/Unterordnungsbeziehung (z.B. Order und Order_Detail) können Sie Stretch für die untergeordnete Tabelle (Order-Detail) aktivieren, jedoch nicht für die übergeordnete Tabelle (Order).  
  
### <a name="indexes"></a>Indizes  
-   Volltextindizes  
  
-   XML-Indizes  
  
-   Räumlichkeitsindizes  
  
-   Indizierte Sichten, die auf die Tabelle verweisen  
  
## <a name="see-also"></a>Weitere Informationen  
 [Identifizieren von Datenbanken und Tabellen für Stretch Database durch Ausführen des Ratgebers für Stretch Database](../../sql-server/stretch-database/stretch-database-databases-and-tables-stretch-database-advisor.md)   
 [Aktivieren von Stretch Database für eine Datenbank](../../sql-server/stretch-database/enable-stretch-database-for-a-database.md)   
 [Aktivieren von Stretch Database für eine Tabelle](../../sql-server/stretch-database/enable-stretch-database-for-a-table.md)  
  
  
