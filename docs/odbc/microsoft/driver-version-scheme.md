---
description: Treiberversionsschema
title: Treiber Versions Schema | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
helpviewer_keywords:
- ODBC driver for Oracle [ODBC], versions
ms.assetid: e4a8d9d7-8aba-48ab-8be6-1a6129adfb8f
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 0414da00ffc5a220e3bf6b13837880b1116f58eb
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "88412726"
---
# <a name="driver-version-scheme"></a>Treiberversionsschema
> [!IMPORTANT]  
>  Diese Funktion wird in einer zukünftigen Version von Windows entfernt. Nutzen Sie diese Funktionen bei Neuentwicklungen nicht mehr, und planen Sie die Änderung von Anwendungen, die diese Funktion zurzeit verwenden. Verwenden Sie stattdessen den von Oracle bereitgestellten ODBC-Treiber.  
  
 In der folgenden Tabelle sind alle veröffentlichten Versionen des Microsoft ODBC-Treibers für Oracle aufgeführt.  
  
|Treiberversion|Buildnummer|Verfügbarkeitsverlauf|  
|--------------------|------------------|--------------------------|  
|1.0|2.00.6235|Visual C++ 4,2 und Visual Basic 5,0, Enterprise Edition|  
|2.0|2.73.7269|Visual Studio 97 und MDAC 1.5 a|  
|2,0 aktualisiert|2.73.7283.01|IIS 4,0|  
|2,0 aktualisiert|2.73.7283.03|MDAC 1.5 b und 1.5 c|  
|2,0 aktualisiert|2.73.7356|ODBC 3,5 SDK|  
|2.5|2.573.2927|Visual Studio 6,0 und MDAC 2,0|  
|2,5 aktualisiert|2.573.3513|SQL Server 7,0<br /><br /> SQL Server 6,5 SP5|  
  
 Build 2.00.6235 (Version 1) war die erste Version von Microsoft ODBC Driver for Oracle. Nach der Veröffentlichung der ersten Version wurde eine neue Benennungs Konvention angenommen.  
  
 Beispielsweise kann 2.73.7283.03 in die folgenden unterschiedlichen Komponenten unterteilt werden:  
  
-   2 = die Versionsnummer.  
  
-   73 = die Version des Oracle-Servers, für den der Treiber entworfen wurde.  
  
-   7283,03 = die Buildnummer des Treibers.  
  
> [!NOTE]  
>  Mit Release 2.573.2973 hat die Benennungs Konvention zu Verwirrung geführt, dass 2,573 eine frühere Version als 2,73 ist, aber jeder Abschnitt der Buildnummer sollte einzeln betrachtet werden. Die Zahl 573 ist größer als 73, sodass es sich um eine neuere Version handelt. Außerdem gibt "2,5" die Versionsnummer des Treibers an.
