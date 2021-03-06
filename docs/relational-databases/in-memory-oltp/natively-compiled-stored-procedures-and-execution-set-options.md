---
title: Nativ kompilierte gespeicherte Prozeduren und SET-Optionen
description: Die SET-Optionen einer Sitzung wirken sich nicht auf die Ausführung einer gespeicherten Prozedur aus, es sei den, bestimmte SET-Optionen sorgen dafür, dass gespeicherte Prozeduren nicht ausgeführt werden.
ms.custom: seo-dt-2019
ms.date: 10/26/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database
ms.reviewer: ''
ms.technology: in-memory-oltp
ms.topic: conceptual
ms.assetid: c1869cf7-9030-4d18-85d6-0e419a4e9af7
author: markingmyname
ms.author: maghan
monikerRange: =azuresqldb-current||>=sql-server-2016||>=sql-server-linux-2017||=azuresqldb-mi-current
ms.openlocfilehash: e86ab52348e4e51a2b060bab50aecf2d3c453fc3
ms.sourcegitcommit: 1a544cf4dd2720b124c3697d1e62ae7741db757c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "97485282"
---
# <a name="natively-compiled-stored-procedures-and-execution-set-options"></a>Systemintern kompilierte gespeicherte Prozeduren und deren Ausführung mit SET-Optionen
[!INCLUDE [SQL Server Azure SQL Database](../../includes/applies-to-version/sql-asdb.md)]

Sitzungsoptionen sind in ATOMIC-Blöcken fixiert, wie in [Atomic Blocks (ATOMIC-Blöcken)](atomic-blocks-in-native-procedures.md) beschrieben. Die Ausführung einer gespeicherten Prozedur wird durch die SET-Optionen einer Sitzung nicht beeinflusst, da ATOMIC-Blöcke benötigt werden. Bestimmte SET-Optionen, wie SET NOEXEC und SET SHOWPLAN_XML, bewirken jedoch, dass gespeicherte Prozeduren (einschließlich systemintern kompilierter gespeicherter Prozeduren) nicht ausgeführt werden.   
  
 Wenn eine systemintern kompilierte gespeicherte Prozedur mit einer aktivierten STATISTICS-Option ausgeführt wird, werden Statistiken für die Prozedur als Ganzes und nicht pro Anweisung erfasst. Weitere Informationen finden Sie unter [SET STATISTICS IO &#40;Transact-SQL&#41;](../../t-sql/statements/set-statistics-io-transact-sql.md), [SET STATISTICS PROFILE &#40;Transact-SQL&#41;](../../t-sql/statements/set-statistics-profile-transact-sql.md), [SET STATISTICS TIME &#40;Transact-SQL&#41;](../../t-sql/statements/set-statistics-time-transact-sql.md) und [SET STATISTICS XML &#40;Transact-SQL&#41;](../../t-sql/statements/set-statistics-xml-transact-sql.md). Um für systemintern gespeicherte Prozeduren eine Ausführungsstatistik pro Anweisung abzurufen, verwenden Sie für das sp_statement_completed-Ereignis eine Sitzung für erweiterte Ereignisse. Diese startet, nachdem alle Abfragen in der Ausführung einer gespeicherten Prozedur abgeschlossen sind. Weitere Informationen zum Erstellen einer Sitzung für erweiterte Ereignisse finden Sie unter [CREATE EVENT SESSION &#40;Transact-SQL&#41;](../../t-sql/statements/create-event-session-transact-sql.md).  
  
 **SHOWPLAN_XML** wird für nativ kompilierte gespeicherte Prozeduren unterstützt. **SHOWPLAN_ALL** und **SHOWPLAN_TEXT** werden bei nativ kompilierten gespeicherten Prozeduren nicht unterstützt.  
  
 **SET FMTONLY** wird bei systemintern kompilierten gespeicherten Prozeduren nicht unterstützt. Verwenden Sie stattdessen [sp_describe_first_result_set &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/sp-describe-first-result-set-transact-sql.md).  
  
## <a name="see-also"></a>Weitere Informationen  
 [Nativ kompilierte gespeicherte Prozeduren](./a-guide-to-query-processing-for-memory-optimized-tables.md)  
  
