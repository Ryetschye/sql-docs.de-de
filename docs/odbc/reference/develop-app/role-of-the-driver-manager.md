---
description: Rolle des Treiber-Managers
title: Rolle des Treiber-Managers | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
helpviewer_keywords:
- diagnostic information [ODBC], SqlGetDiagField
- diagnostic information [ODBC], driver manager error checking
- SQLGetDiagField function [ODBC], driver manager
- SQLGetDiagRec function [ODBC], driver manager
- ODBC driver manager [ODBC]
- diagnostic information [ODBC], SqlGetDiagRec
- driver manager [ODBC], error checking
ms.assetid: 7b861c82-357e-4590-8074-45136e9ed15e
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: f974fe6436173b55f39aced45cc38312221cffaa
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "88465657"
---
# <a name="role-of-the-driver-manager"></a>Rolle des Treiber-Managers
Der Treiber-Manager bestimmt die endgültige Reihenfolge, in der die von ihm generierten Statusdaten Sätze zurückgegeben werden. Insbesondere wird ermittelt, welcher Datensatz den höchsten Rang hat und zuerst zurückgegeben werden soll. Der Treiber ist für das Anordnen von Statusdaten Sätzen verantwortlich, die er generiert. Wenn die Statusdaten Sätze sowohl vom Treiber-Manager als auch vom Treiber gesendet werden, ist der Treiber-Manager für die Bestellung verantwortlich. Weitere Informationen finden Sie unter [Sequenz von Status Datensätzen](../../../odbc/reference/develop-app/sequence-of-status-records.md).  
  
 Der Treiber-Manager führt so viele Fehlerprüfungen wie möglich aus. Dadurch wird jeder Treiber daran bewahrt, die gleichen Fehler zu überprüfen. Wenn ein Funktions Argument z. b. eine diskrete Anzahl von Werten akzeptiert (z. b. *Vorgang* in **SQLSetPos**), überprüft der Treiber-Manager, ob der angegebene Wert gültig ist.  
  
 In den folgenden Abschnitten werden die Typen von Bedingungen beschrieben, die vom Treiber-Manager geprüft werden. Sie sollen nicht vollständig sein. eine komplette Liste der Sqlstates, die der Treiber-Manager zurückgibt, finden Sie im Abschnitt "Diagnose" der einzelnen Funktionen. die Beschreibung jeder vom Treiber-Manager vorgenommenen Überprüfung beginnt mit den Buchstaben "(DM)". Siehe auch die Status Übergangs Tabellen in [Anhang B: ODBC-Status Übergangs Tabellen](../../../odbc/reference/appendixes/appendix-b-odbc-state-transition-tables.md); Fehler, die in Klammern angezeigt werden, werden vom Treiber-Manager erkannt.  
  
 In diesem Abschnitt werden die folgenden Themen behandelt:  
  
-   [Überprüfungen des Argumentwerts](../../../odbc/reference/develop-app/argument-value-checks.md)  
  
-   [Überprüfungen des Statusübergangs](../../../odbc/reference/develop-app/state-transition-checks.md)  
  
-   [Überprüfungen auf allgemeine Fehler](../../../odbc/reference/develop-app/general-error-checks.md)  
  
-   [Fehler des Treiber-Managers und Überprüfungen der Warnung](../../../odbc/reference/develop-app/driver-manager-error-and-warning-checks.md)
