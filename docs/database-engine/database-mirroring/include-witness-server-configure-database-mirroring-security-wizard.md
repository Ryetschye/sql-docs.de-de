---
title: Zeugenserver einschließen (Assistent zum Konfigurieren der Sicherheit für die Datenbankspiegelung)
description: In diesem Artikel wird die Seite „Zeugenserver einschließen“ des Assistenten zum Konfigurieren der Sicherheit für die Datenbankspiegelung in der SQL Server Management Studio-GUI (SSMS) beschrieben.
ms.custom: seo-lt-2019
ms.date: 03/07/2017
ms.prod: sql
ms.prod_service: high-availability
ms.reviewer: ''
ms.technology: high-availability
ms.topic: conceptual
f1_keywords:
- sql13.swb.configdbmsecurwiz.inclwitness.f1
ms.assetid: f04b38a4-f4e2-4d4c-bdac-7cc70e5a5684
author: MikeRayMSFT
ms.author: mikeray
ms.openlocfilehash: a8b787f59da14c1414e66f158f8001e05cca6006
ms.sourcegitcommit: da88320c474c1c9124574f90d549c50ee3387b4c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2020
ms.locfileid: "85754645"
---
# <a name="include-witness-server-configure-database-mirroring-security-wizard"></a>Zeugenserver einschließen (Assistent zum Konfigurieren der Sicherheit für die Datenbankspiegelung)
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]
  Verwenden Sie diese Seite, um festzulegen, ob Sie einen Zeugenserver in diese Sicherheitskonfiguration für die Datenbankspiegelung einschließen möchten.  
  
 **So konfigurieren Sie die Datenbankspiegelung mithilfe von SQL Server Management Studio**  
  
-   [Einrichten einer Datenbank-Spiegelungssitzung mithilfe der Windows-Authentifizierung &#40;SQL Server Management Studio&#41;](../../database-engine/database-mirroring/establish-database-mirroring-session-windows-authentication.md)  
  
-   [Starten des Assistenten zum Konfigurieren der Sicherheit für die Datenbankspiegelung &#40;SQL Server Management Studio&#41;](../../database-engine/database-mirroring/start-the-configuring-database-mirroring-security-wizard.md)  
  
## <a name="options"></a>Tastatur  
 **Ja**  
 Klicken Sie hier, um eine Zeugenserverinstanz in die Sicherheitskonfiguration einzubeziehen. Der Zeuge ist erforderlich für den Modus für hohe Sicherheit mit automatischem Failover, der ein automatisches Failover zur Spiegelserverinstanz unterstützt, wenn die Prinzipalserverinstanz einen Fehler erzeugt.  
  
 **Nein**  
 Klicken Sie hier, um die Sicherheit ohne einen Zeugen zu konfigurieren.  
  
## <a name="see-also"></a>Weitere Informationen  
 [Datenbankeigenschaften &#40;Seite Wird gespiegelt&#41;](../../relational-databases/databases/database-properties-mirroring-page.md)   
 [Datenbankspiegelung &#40;SQL Server&#41;](../../database-engine/database-mirroring/database-mirroring-sql-server.md)   
 [Datenbank-Spiegelungszeuge](../../database-engine/database-mirroring/database-mirroring-witness.md)  
  
  
