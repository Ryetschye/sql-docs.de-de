---
description: MSmerge_identity_range_allocations (Transact-SQL)
title: MSmerge_identity_range_allocations (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 03/04/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: replication
ms.topic: language-reference
f1_keywords:
- MSmerge_identity_range_allocations
- MSmerge_identity_range_allocations_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- MSmerge_identity_range_allocations system table
ms.assetid: 6362e35e-0ab3-4638-855b-1ce013f5fd6d
author: markingmyname
ms.author: maghan
ms.openlocfilehash: aba2d603c53827f63ceb39fdfdaae7819e4e1bff
ms.sourcegitcommit: dd36d1cbe32cd5a65c6638e8f252b0bd8145e165
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "89545641"
---
# <a name="msmerge_identity_range_allocations-transact-sql"></a>MSmerge_identity_range_allocations (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  Die **MSmerge_identity_range_allocations** Tabelle dient zum Nachverfolgen des Verlaufs der Identitäts Bereichs Zuweisungen für Verleger und Abonnenten für veröffentlichte Artikel. Diese Tabelle wird in der Verteilungsdatenbank gespeichert.  
  
|Spaltenname|Datentyp|BESCHREIBUNG|  
|-----------------|---------------|-----------------|  
|**publisher_id**|**smallint**|Die ID des Verlegers|  
|**publisher_db**|**nvarchar(128)**|Der Name der Veröffentlichungs Datenbank.|  
|**ung**|**nvarchar(128)**|Der Name der Veröffentlichung.|  
|**Artikel**|**nvarchar(128)**|Der Name des Artikels.|  
|**Abonnenten**|**nvarchar(128)**|Den Namen des Abonnenten.|  
|**subscriber_db**|**nvarchar(128)**|Der Name der Abonnement Datenbank.|  
|**is_pub_range**|**bit**|Zeigt an, ob der Identitätsbereich einem Verleger zugewiesen ist.|  
|**ranges_allocated**|**tinyint**|Die Anzahl zugewiesener Identitätsbereiche.|  
|**range_begin**|**numerisch (38)**|Der Anfangswert des Bereichs.|  
|**range_end**|**numerisch (38)**|Der letzte Wert des Bereichs.|  
|**next_range_begin**|**numerisch (38)**|Der Anfangswert des nächsten zuzuweisenden Bereichs.|  
|**next_range_end**|**numerisch (38)**|Der letzte Wert des nächsten zuzuweisenden Bereichs.|  
|**max_used**|**numerisch (38)**|Der höchste verwendete Identitätswert.|  
|**time_of_allocation**|**datetime**|Der Zeitpunkt, zu dem die Zuweisung erfolgte.|  
  
## <a name="see-also"></a>Weitere Informationen  
 [Replikations Tabellen &#40;Transact-SQL-&#41;](../../relational-databases/system-tables/replication-tables-transact-sql.md)   
 [Replikationssichten &#40;Transact-SQL&#41;](../../relational-databases/system-views/replication-views-transact-sql.md)  
  
  
