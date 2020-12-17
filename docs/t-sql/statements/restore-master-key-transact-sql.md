---
description: RESTORE MASTER KEY (Transact-SQL)
title: RESTORE MASTER KEY (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: sql-database
ms.reviewer: ''
ms.technology: t-sql
ms.topic: language-reference
f1_keywords:
- RESTORE_MASTER_KEY_TSQL
- RESTORE MASTER KEY
- LOAD_MASTER_KEY_TSQL
- LOAD MASTER KEY
dev_langs:
- TSQL
helpviewer_keywords:
- database master key [SQL Server], importing
- encryption [SQL Server], Database Master Key
- copying Database Master Keys
- importing Database Master Keys
- cryptography [SQL Server], Database Master Key
- transferring Database Master Keys
- RESTORE MASTER KEY statement
ms.assetid: 70ceb951-31a2-4fc4-a0c1-e6c18eeb3ae7
author: VanMSFT
ms.author: vanto
ms.openlocfilehash: f5a15c5ac7a401e4f5359cff34693a6131ce1391
ms.sourcegitcommit: c5078791a07330a87a92abb19b791e950672e198
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "91497797"
---
# <a name="restore-master-key-transact-sql"></a>RESTORE MASTER KEY (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  Importiert einen Datenbank-Hauptschlüssel aus einer Sicherungsdatei.  
  
 ![Symbol für Themenlink](../../database-engine/configure-windows/media/topic-link.gif "Symbol für Themenlink") [Transact-SQL-Syntaxkonventionen](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Syntax  
  
```syntaxsql
RESTORE MASTER KEY FROM FILE = 'path_to_file'   
    DECRYPTION BY PASSWORD = 'password'  
    ENCRYPTION BY PASSWORD = 'password'  
    [ FORCE ]  
```  
  
[!INCLUDE[sql-server-tsql-previous-offline-documentation](../../includes/sql-server-tsql-previous-offline-documentation.md)]

## <a name="arguments"></a>Argumente
 FILE ='*path_to_file*'  
 Gibt den vollständigen Pfad, einschließlich des Dateinamens, zum gespeicherten Datenbank-Hauptschlüssel an. *path_to_file* kann ein lokaler Pfad oder ein UNC-Pfad zu einem Netzwerkspeicherort sein.  
  
 DECRYPTION BY PASSWORD ='*password*'  
 Gibt das Kennwort an, das zum Entschlüsseln des aus einer Datei importierten Datenbank-Hauptschlüssels erforderlich ist.  
  
 ENCRYPTION BY PASSWORD ='*password*'  
 Gibt das Kennwort an, das nach dem Laden in die Datenbank zum Verschlüsseln des Datenbank-Hauptschlüssels verwendet wird.  
  
 FORCE  
 Gibt an, dass der RESTORE-Prozess auch dann fortgesetzt werden soll, wenn der aktuelle Datenbank-Hauptschlüssel nicht geöffnet ist oder wenn einige der privaten Schlüssel, die mit ihm verschlüsselt sind, von [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] nicht entschlüsselt werden können.  
  
## <a name="remarks"></a>Bemerkungen  
 Bei der Wiederherstellung des Hauptschlüssels werden alle Schlüssel von [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] entschlüsselt, die mit dem aktuell aktiven Hauptschlüssel verschlüsselt sind. Diese Schlüssel werden dann mit dem wiederhergestellten Hauptschlüssel verschlüsselt. Die Ausführung dieses ressourcenintensiven Vorgangs sollte außerhalb der Hauptzeiten geplant werden. Falls der aktuelle Datenbank-Hauptschlüssel nicht geöffnet ist oder nicht geöffnet werden kann oder falls einer der Schlüssel, die mit ihm verschlüsselt sind, nicht entschlüsselt werden kann, kann der Wiederherstellungsvorgang nicht erfolgreich ausgeführt werden.  
  
 Die FORCE-Option sollte nur verwendet werden, wenn der Hauptschlüssel nicht abgerufen werden kann oder wenn bei der Entschlüsselung ein Fehler aufgetreten ist. Informationen, die nur mit dem nicht abrufbaren Schlüssel verschlüsselt sind, gehen verloren.  
  
 Wurde der Hauptschlüssel mit dem Diensthauptschlüssel verschlüsselt, wird auch der wiederhergestellte Hauptschlüssel mit dem Diensthauptschlüssel verschlüsselt.  
  
 Falls in der aktuellen Datenbank kein Hauptschlüssel vorhanden ist, wird von RESTORE MASTER KEY ein Hauptschlüssel erstellt. Der neue Hauptschlüssel wird nicht automatisch mit dem Diensthauptschlüssel verschlüsselt.  
  
## <a name="permissions"></a>Berechtigungen  
 Erfordert die CONTROL-Berechtigung für die Datenbank.  
  
## <a name="examples"></a>Beispiele  
 Im folgenden Beispiel wird der Datenbank-Hauptschlüssel für die `AdventureWorks2012`-Datenbank wiederhergestellt.  
  
```sql  
USE AdventureWorks2012;  
RESTORE MASTER KEY   
    FROM FILE = 'c:\backups\keys\AdventureWorks2012_master_key'   
    DECRYPTION BY PASSWORD = '3dH85Hhk003#GHkf02597gheij04'   
    ENCRYPTION BY PASSWORD = '259087M#MyjkFkjhywiyedfgGDFD';  
GO  
```  
  
## <a name="see-also"></a>Weitere Informationen  
 [CREATE MASTER KEY &#40;Transact-SQL&#41;](../../t-sql/statements/create-master-key-transact-sql.md)   
 [ALTER MASTER KEY (Transact-SQL)](../../t-sql/statements/alter-master-key-transact-sql.md)   
 [Verschlüsselungshierarchie](../../relational-databases/security/encryption/encryption-hierarchy.md)  
  
  
