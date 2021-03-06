---
description: Ermitteln der Ziel-DBMS und Zieltreiber
title: Ermitteln der Ziel-DBMSs und-Treiber | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
helpviewer_keywords:
- target DBMSs and drivers in interoperability [ODBC]
- interoperability [ODBC], target dbmss and drivers
ms.assetid: 23bee0f6-e12a-4598-b34e-df11a8086829
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 8dfbc11e96577e9027d1cc6e17701a82b89061be
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "88429322"
---
# <a name="determining-the-target-dbmss-and-drivers"></a>Ermitteln der Ziel-DBMS und Zieltreiber
Die nächste Frage, die Sie beachten sollten, ist die Ziel-DBMSs für die Anwendung und welche Treiber verfügbar sind, die diese DBMSs unterstützen? Da generische Anwendungen tendenziell hochgradig interoperabel sind, ist die Frage der Ziel-DBMSs am meisten auf benutzerdefinierte und vertikale Anwendungen anwendbar. Die Frage der Ziel Treiber gilt jedoch für alle Anwendungen, da die Treiber stark von der Geschwindigkeit, Qualität, Featureunterstützung und Verfügbarkeit abweichen. Außerdem müssen die Kosten und die Verfügbarkeit von Lizenzierungs Plänen berücksichtigt werden, wenn die Treiber erneut mit der Anwendung verteilt werden müssen.  
  
 Bei vielen benutzerdefinierten Anwendungen sind die Ziel-DBMSs offensichtlich: Sie sind vorhanden, auf die die Anwendung zugreifen kann. DBMSs, zu dem die zukünftige Migration geplant ist, sollte ebenfalls berücksichtigt werden. Die Hauptfrage für diese Anwendungen ist jedoch, welche Treiber oder Treiber für Sie verwendet werden sollen. Für andere benutzerdefinierte Anwendungen, die nicht für den Zugriff auf ein vorhandenes DBMS konzipiert sind, können die Ziel-DBMSs basierend auf der Funktions Unterstützung, der gleichzeitigen Benutzerunterstützung, der Verfügbarkeit von Treibern und der Verfügbarkeit ausgewählt werden.  
  
 Bei vertikalen Anwendungen werden die Ziel-DBMSs in der Regel basierend auf der Funktions Unterstützung, der Treiber Verfügbarkeit und dem Markt ausgewählt. Beispielsweise muss eine vertikale Anwendung, die für kleine Unternehmen entwickelt wurde, auf DBMSs abzielen, die für diese Unternehmen bezahlbar sind. eine vertikale Anwendung, die als Add-on für vorhandenes DBMSs konzipiert ist, muss auf häufig verwendete DBMSs abzielen.  
  
 Bei der Auswahl von Ziel-DBMSs sollten die Unterschiede zwischen Desktop-und Server Datenbanken berücksichtigt werden. Desktop Datenbanken wie dBase, Paradox und Btrieve sind weniger leistungsfähig als Server Datenbanken. Da auf Sie in der Regel über die weniger leistungsfähigen SQL-Engines zugegriffen wird, die in den meisten dateibasierten Treibern gefunden werden, fehlen Ihnen häufig volle Transaktionsunterstützung, unterstützen weniger gleichzeitige Benutzer und haben nur begrenzte SQL Sie sind jedoch preiswert und verfügen über eine große installierte Basis.  
  
 Server Datenbanken wie Oracle, DB2 und SQL Server bieten vollständige Transaktionsunterstützung, unterstützen viele gleichzeitige Benutzer und verfügen über umfangreiche SQL-Funktionen. Sie sind viel teurer und verfügen über eine kleinere installierte Basis. Auf der anderen Seite sind die Softwarepreise tendenziell höher, was zu einem kleineren potenziellen Markt verlagert.  
  
 Folglich kann das Ziel-DBMSs in manchen Fällen basierend auf den Funktionen ausgewählt werden, die für die Anwendung und den Zielmarkt der Anwendung erforderlich sind. Beispielsweise kann ein Bestell Eintrags System für große Unternehmen nicht auf Desktop Datenbanken abzielen, da diese keine angemessene Transaktionsunterstützung benötigen. Ein ähnliches System, das für kleine Unternehmen entwickelt wurde, kann die meisten Server Datenbanken auf Grundlage der Kosten ausschließen. Und Entwickler von generischen Anwendungen könnten beide als Ziel verwenden, aber die erweiterten Funktionen von Server Datenbanken vermeiden.
