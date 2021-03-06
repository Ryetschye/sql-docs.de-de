---
description: CopyRecordOptionsEnum
title: Copyrecordoptionsenum | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: conceptual
apitype: COM
f1_keywords:
- CopyRecordOptionsEnum
helpviewer_keywords:
- CopyRecordOptionsEnum enumeration [ADO]
ms.assetid: 2fa4eec5-d50b-4fd3-8ae7-40af441ba12b
author: rothja
ms.author: jroth
ms.openlocfilehash: 1570b0baa22b6d08db9b47d99f4d1e01595622d6
ms.sourcegitcommit: 18a98ea6a30d448aa6195e10ea2413be7e837e94
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2020
ms.locfileid: "88974541"
---
# <a name="copyrecordoptionsenum"></a>CopyRecordOptionsEnum
Gibt das Verhalten der [CopyRecord](./copyrecord-method-ado.md) -Methode an.  
  
|Konstante|Wert|Beschreibung|  
|--------------|-----------|-----------------|  
|**adcopyzuwemulations**|4|Gibt an, dass der *Quell* Anbieter versucht, die Kopie mithilfe von Download-und Uploadvorgängen zu simulieren, wenn diese Methode fehlschlägt, weil das *Ziel*auf einem anderen Server ausgeführt wird oder von einem anderen Anbieter als *Quelle*bedient wird. Beachten Sie, dass unterschiedliche Anbieter Funktionen die Leistung beeinträchtigen oder Daten verlieren können.|  
|**adCopyNonRecursive**|2|Kopiert das aktuelle Verzeichnis, aber keines seiner Unterverzeichnisse, in das Ziel. Der Kopiervorgang ist nicht rekursiv.|  
|**adCopyOverwrite**|1|Überschreibt die Datei oder das Verzeichnis, wenn das *Ziel* auf eine vorhandene Datei oder ein vorhandenes Verzeichnis verweist.|  
|**adcopyunspezifiziert**|-1|Standard. Führt den Standard Kopiervorgang aus: der Vorgang schlägt fehl, wenn die Zieldatei oder das Verzeichnis bereits vorhanden ist, und der Vorgang wird rekursiv kopiert.|  
  
## <a name="adowfc-equivalent"></a>ADO/WFC-Entsprechung  
 Diese Konstanten haben keine ADO/WFC-Entsprechungen.  
  
## <a name="applies-to"></a>Gilt für  
 [CopyRecord-Methode (ADO)](./copyrecord-method-ado.md)