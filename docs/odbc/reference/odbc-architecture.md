---
description: ODBC-Architektur
title: ODBC-Architektur | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
helpviewer_keywords:
- ODBC architecture [ODBC], components
- ODBC architecture [ODBC]
ms.assetid: 2604f492-587b-4a51-9876-59a7870b3ef2
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 3afeb698d7eff9d09161a091e3de0194fea93ec2
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "88429002"
---
# <a name="odbc-architecture"></a>ODBC-Architektur
Die ODBC-Architektur verfügt über vier Komponenten:  
  
-   **Anwendung** Führt die Verarbeitung durch und ruft ODBC-Funktionen auf, um SQL-Anweisungen zu senden und Ergebnisse abzurufen.  
  
-   **Treiber-Manager** Lädt Treiber im Namen einer Anwendung und entlädt Sie. Verarbeitet ODBC-Funktionsaufrufe oder übergibt sie an einen Treiber.  
  
-   **Treiber** Verarbeitet ODBC-Funktionsaufrufe, übermittelt SQL-Anforderungen an eine bestimmte Datenquelle und gibt Ergebnisse an die Anwendung zurück. Bei Bedarf ändert der Treiber die Anforderung einer Anwendung so, dass die Anforderung der vom zugeordneten DBMS unterstützten Syntax entspricht.  
  
-   **Datenquelle** Besteht aus den Daten, auf die der Benutzer zugreifen möchte, und dem zugeordneten Betriebssystem, DBMS und der Netzwerkplattform (sofern vorhanden), die für den Zugriff auf das DBMS verwendet werden.  
  
 Beachten Sie die folgenden Punkte zur ODBC-Architektur. Zuerst können mehrere Treiber und Datenquellen vorhanden sein, sodass die Anwendung gleichzeitig auf Daten aus mehreren Datenquellen zugreifen kann. Zweitens wird die ODBC-API an zwei Stellen verwendet: zwischen der Anwendung und dem Treiber-Manager und zwischen dem Treiber-Manager und den einzelnen Treibern. Die Schnittstelle zwischen dem Treiber-Manager und den Treibern wird manchmal als *Dienstanbieter Schnittstelle* oder *SPI*bezeichnet. Für ODBC sind die Anwendungsprogrammierschnittstelle (Application Programming Interface, API) und die Dienstanbieter Schnittstelle (SPI) identisch. Das heißt, der Treiber-Manager und jeder Treiber verfügen über dieselbe Schnittstelle wie die gleichen Funktionen.  
  
 In diesem Abschnitt werden die folgenden Themen behandelt:  
  
-   [Anwendungen](../../odbc/reference/applications.md)  
  
-   [Der Treiber-Manager](../../odbc/reference/the-driver-manager.md)  
  
-   [Treiber](../../odbc/reference/drivers.md)  
  
-   [Data Sources](../../odbc/reference/data-sources.md) (Datenquellen)
