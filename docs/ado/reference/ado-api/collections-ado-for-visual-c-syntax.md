---
description: Collections (ADO für Visual C++-Syntax)
title: Auflistungen (ADO für Visual C++-Syntax) | Microsoft-Dokumentation
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: conceptual
apitype: COM
dev_langs:
- C++
helpviewer_keywords:
- ADO for Visual C++ syntax [ADO]
- syntax indexes [ADO], ADO for Visual C++ syntax
- collections [ADO], ADO for Visual C++ syntax
ms.assetid: 6a0109a0-f2d9-4f7c-8e1e-42763f9acaea
author: rothja
ms.author: jroth
ms.openlocfilehash: b4bc59facd753bf6d36c3a79d06a4efe29e7c235
ms.sourcegitcommit: 18a98ea6a30d448aa6195e10ea2413be7e837e94
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2020
ms.locfileid: "88975381"
---
# <a name="collections-ado-for-visual-c-syntax"></a>Collections (ADO für Visual C++-Syntax)
## <a name="parameters"></a>Parameter  
  
### <a name="methods"></a>Methoden  
  
```  
Append(IDispatch *Object);  
Delete(VARIANT Index);  
Refresh(void);  
```  
  
 Weitere Informationen finden Sie unter  
  
-   [Append-Methode (ADO)](./append-method-ado.md)  
  
-   [Delete-Methode (ADO-Parameters-Collection)](./delete-method-ado-parameters-collection.md)  
  
-   [Refresh-Methode (ADO)](./refresh-method-ado.md)  
  
### <a name="properties"></a>Eigenschaften  
  
```  
get_Count(long *c);  
get_Item(VARIANT Index, _ADOParameter **ppvObject);  
```  
  
 Weitere Informationen finden Sie unter  
  
-   [Count-Eigenschaft (ADO)](./count-property-ado.md)  
  
-   [Item-Eigenschaft (ADO)](./item-property-ado.md)  
  
## <a name="fields"></a>Felder  
  
### <a name="methods"></a>Methoden  
  
```  
Append(BSTR bstrName, DataTypeEnum Type, long DefinedSize, FieldAttributeEnum Attrib);  
Delete(VARIANT Index);  
Refresh(void);  
```  
  
 Weitere Informationen finden Sie unter  
  
-   [Append-Methode (ADO)](./append-method-ado.md)  
  
-   [Delete-Methode (ADO-Parameters-Collection)](./delete-method-ado-parameters-collection.md)  
  
-   [Refresh-Methode (ADO)](./refresh-method-ado.md)  
  
### <a name="properties"></a>Eigenschaften  
  
```  
get_Count(long *c);  
get_Item(VARIANT Index, ADOField **ppvObject);  
```  
  
 Weitere Informationen finden Sie unter  
  
-   [Count-Eigenschaft (ADO)](./count-property-ado.md)  
  
-   [Item-Eigenschaft (ADO)](./item-property-ado.md)  
  
## <a name="errors"></a>Errors  
  
### <a name="methods"></a>Methoden  
  
```  
Clear(void);  
Refresh(void);  
```  
  
 Weitere Informationen finden Sie unter  
  
-   [Clear-Methode (ADO)](./clear-method-ado.md)  
  
-   [Refresh-Methode (ADO)](./refresh-method-ado.md)  
  
### <a name="properties"></a>Eigenschaften  
  
```  
get_Count(long *c);  
get_Item(VARIANT Index, ADOError **ppvObject);  
```  
  
 Weitere Informationen finden Sie unter  
  
-   [Count-Eigenschaft (ADO)](./count-property-ado.md)  
  
-   [Item-Eigenschaft (ADO)](./item-property-ado.md)  
  
## <a name="properties"></a>Eigenschaften  
  
### <a name="methods"></a>Methoden  
  
```  
Refresh(void);  
```  
  
 Weitere Informationen finden Sie unter  
  
-   [Refresh-Methode (ADO)](./refresh-method-ado.md)  
  
### <a name="properties"></a>Eigenschaften  
  
```  
get_Count(long *c);  
get_Item(VARIANT Index, ADOProperty **ppvObject);  
```  
  
 Weitere Informationen finden Sie unter  
  
-   [Count-Eigenschaft (ADO)](./count-property-ado.md)  
  
-   [Item-Eigenschaft (ADO)](./item-property-ado.md)  
  
## <a name="see-also"></a>Weitere Informationen  
 [Fehlersammlung (ADO)](./errors-collection-ado.md)   
 [Fields-Auflistung (ADO)](./fields-collection-ado.md)   
 [Parameter Auflistung (ADO)](./parameters-collection-ado.md)   
 [Properties-Collection (ADO)](./properties-collection-ado.md)