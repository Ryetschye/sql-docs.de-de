---
description: MSmerge_subscriptions (Transact-SQL)
title: MSmerge_subscriptions (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 03/03/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: replication
ms.topic: language-reference
f1_keywords:
- MSmerge_subscriptions
- MSmerge_subscriptions_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- MSmerge_subscriptions system table
ms.assetid: cafd954a-92f8-44cb-a5d0-dce9aafa5ee1
author: markingmyname
ms.author: maghan
ms.openlocfilehash: c6e522b60af93e74980c0465e771ddd820ac9149
ms.sourcegitcommit: dd36d1cbe32cd5a65c6638e8f252b0bd8145e165
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "89545570"
---
# <a name="msmerge_subscriptions-transact-sql"></a>MSmerge_subscriptions (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  Die **MSmerge_subscriptions** Tabelle enthält eine Zeile für jedes Abonnement, das von der Merge-Agent auf dem Abonnenten gewartet wird. Diese Tabelle wird in der Verteilungsdatenbank gespeichert.  
  
|Spaltenname|Datentyp|BESCHREIBUNG|  
|-----------------|---------------|-----------------|  
|**publisher_id**|**smallint**|Die ID des Verlegers|  
|**publisher_db**|**sysname**|Der Name der Verlegerdatenbank.|  
|**publication_id**|**int**|Die ID der Veröffentlichung.|  
|**subscriber_id**|**smallint**|Die ID des Abonnenten.|  
|**subscriber_db**|**sysname**|Der Name der Abonnement Datenbank.|  
|**subscription_type**|**int**|Der Typ des Abonnements:<br /><br /> 0 = Push.<br /><br /> 1 = Pull.<br /><br /> 2 = Anonym.|  
|**sync_type**|**tinyint**|Typ der Synchronisierung:<br /><br /> 1 = Automatisch.<br /><br /> 2 = Keine Synchronisierung|  
|**status**|**tinyint**|Status des Abonnements.|  
|**subscription_time**|**datetime**|Zeitpunkt, zu dem das Abonnement hinzugefügt wurde.|  
  
## <a name="see-also"></a>Weitere Informationen  
 [Replikations Tabellen &#40;Transact-SQL-&#41;](../../relational-databases/system-tables/replication-tables-transact-sql.md)   
 [Replikationssichten &#40;Transact-SQL&#41;](../../relational-databases/system-views/replication-views-transact-sql.md)  
  
  
