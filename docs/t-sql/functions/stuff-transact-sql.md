---
description: STUFF (Transact-SQL)
title: STUFF (Transact-SQL) | Microsoft-Dokumentation
ms.custom: ''
ms.date: 11/17/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.reviewer: ''
ms.technology: t-sql
ms.topic: language-reference
f1_keywords:
- STUFF
- STUFF_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- deleting characters
- STUFF function
- length characters
- removing characters
- replacing characters
- characters [SQL Server], replacing
- inserting data
ms.assetid: abb0afa9-44f6-42a2-a871-5f471dfb222b
author: julieMSFT
ms.author: jrasnick
monikerRange: '>=aps-pdw-2016||=azuresqldb-current||=azure-sqldw-latest||>=sql-server-2016||>=sql-server-linux-2017||=azuresqldb-mi-current'
ms.openlocfilehash: f3911e3856116dcf11e3688ab5819feebc49eaed
ms.sourcegitcommit: 1a544cf4dd2720b124c3697d1e62ae7741db757c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "97461211"
---
# <a name="stuff-transact-sql"></a>STUFF (Transact-SQL)
[!INCLUDE [sql-asdb-asdbmi-asa-pdw](../../includes/applies-to-version/sql-asdb-asdbmi-asa-pdw.md)]

  Die STUFF-Funktion fügt eine Zeichenfolge in eine andere Zeichenfolge ein. Sie löscht ab einer bestimmten Anfangsposition eine festgelegte Anzahl von Zeichen in der ersten Zeichenfolge und fügt dort die zweite Zeichenfolge ein.  
  
 ![Symbol für Themenlink](../../database-engine/configure-windows/media/topic-link.gif "Symbol für Themenlink") [Transact-SQL-Syntaxkonventionen](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Syntax  
  
```syntaxsql
STUFF ( character_expression , start , length , replaceWith_expression )  
```  
  
[!INCLUDE[sql-server-tsql-previous-offline-documentation](../../includes/sql-server-tsql-previous-offline-documentation.md)]

## <a name="arguments"></a>Argumente
 *character_expression*  
 Ein [Ausdruck](../../t-sql/language-elements/expressions-transact-sql.md) von Zeichendaten. *character_expression* kann eine Konstante, Variable oder Spalte mit Zeichen- oder Binärdaten darstellen.  
  
 *start*  
 Ein ganzzahliger Wert, der die Position angibt, ab der Zeichen gelöscht werden sollen und an der anschließend eine andere Zeichenfolge eingefügt werden soll. Falls *start* negativ oder 0 (null) ist, wird eine NULL-Zeichenfolge zurückgegeben. Wenn *start* länger als das erste *character_expression*-Element ist, wird eine NULL-Zeichenfolge zurückgegeben. *start* kann vom Typ **bigint** sein.  
  
 *length*  
 Eine ganze Zahl, die festlegt, wie viele Zeichen gelöscht werden sollen. Falls *length* negativ ist, wird eine NULL-Zeichenfolge zurückgegeben. Wenn *length* länger als das erste *character_expression*-Element ist, wird bis zum letzten Zeichen im letzten *character_expression*-Element alles gelöscht.  Wenn *length* null ist, erfolgt die Einfügung an der Position *start*, und es werden keine Zeichen gelöscht. *length* kann vom Datentyp **bigint** sein.

 *replaceWith_expression*  
 Ein [Ausdruck](../../t-sql/language-elements/expressions-transact-sql.md) von Zeichendaten. *character_expression* kann eine Konstante, Variable oder Spalte mit Zeichen- oder Binärdaten darstellen. Dieser Ausdruck ersetzt ab *start**length*-Zeichen durch *character_expression*. Wenn `NULL` als *replaceWith_expression* angegeben ist, werden die Zeichen entfernt, ohne zusätzliche Zeichen einzufügen.   
  
## <a name="return-types"></a>Rückgabetypen  
 Gibt Zeichendaten zurück, wenn *character_expression* einer der unterstützten Zeichendatentypen ist. Gibt Binärdaten zurück, wenn *character_expression* einer der unterstützten Binärdatentypen ist.  
  
## <a name="remarks"></a>Hinweise  
 Falls die Startposition oder die Länge negativ oder die Startposition größer als die Länge der ersten Zeichenfolge ist, wird eine Nullzeichenfolge zurückgegeben. Wenn die Startposition 0 ist, wird ein NULL-Wert zurückgegeben. Wenn es sich um mehr zu löschende Zeichen handelt als die erste Zeichenfolge aufweist, wird die erste Zeichenfolge bis auf das erste Zeichen gelöscht.  

Wenn der Ergebniswert größer als der vom Rückgabetyp unterstützte Höchstwert ist, wird ein Fehler ausgegeben.  
  
## <a name="supplementary-characters-surrogate-pairs"></a>Ergänzende Zeichen (Ersatzpaare)  
 Wenn SC-Sortierungen verwendet werden, kann sowohl *character_expression* als auch *replaceWith_expression* Ersatzzeichenpaare enthalten. Der Längenparameter betrachtet jedes Ersatzzeichen in *character_expression* als einzelnes Zeichen.  
  
## <a name="examples"></a>Beispiele  
 In diesem Beispiel wird eine neue Zeichenfolge zurückgegeben, indem zunächst drei Zeichen aus der ersten Zeichenfolge (`abcdef`) ab der Position `2`, (also bei `b`) gelöscht werden. Anschließend wird die zweite Zeichenfolge an der Löschposition eingefügt.  
  
```sql  
SELECT STUFF('abcdef', 2, 3, 'ijklmn');  
GO  
```  
  
 [!INCLUDE[ssResult](../../includes/ssresult-md.md)]  
  
```  
---------   
aijklmnef   
  
(1 row(s) affected)  
```  
  
## <a name="see-also"></a>Weitere Informationen  
 [CONCAT &#40;Transact-SQL&#41;](../../t-sql/functions/concat-transact-sql.md)  
 [CONCAT_WS &#40;Transact-SQL&#41;](../../t-sql/functions/concat-ws-transact-sql.md)  
 [FORMATMESSAGE &#40;Transact-SQL&#41;](../../t-sql/functions/formatmessage-transact-sql.md)  
 [QUOTENAME &#40;Transact-SQL&#41;](../../t-sql/functions/quotename-transact-sql.md)  
 [REPLACE &#40;Transact-SQL&#41;](../../t-sql/functions/replace-transact-sql.md)  
 [REVERSE &#40;Transact-SQL&#41;](../../t-sql/functions/reverse-transact-sql.md)  
 [STRING_AGG &#40;Transact-SQL&#41;](../../t-sql/functions/string-agg-transact-sql.md)  
 [STRING_ESCAPE &#40;Transact-SQL&#41;](../../t-sql/functions/string-escape-transact-sql.md)  
 [TRANSLATE &#40;Transact-SQL&#41;](../../t-sql/functions/translate-transact-sql.md)  
 [Datentypen &#40;Transact-SQL&#41;](../../t-sql/data-types/data-types-transact-sql.md)   
 [String Functions &#40;Transact-SQL&#41; (Zeichenfolgenfunktionen &#40;Transact-SQL&#41;)](../../t-sql/functions/string-functions-transact-sql.md)  
