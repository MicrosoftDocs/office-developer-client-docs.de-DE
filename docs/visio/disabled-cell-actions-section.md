---
title: Zelle "Disabled" (Abschnitt "Actions")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251337
localization_priority: Normal
ms.assetid: ebf66729-d794-a398-268a-84d761bf06b6
description: Gibt an, ob ein Element in einem Kontext- oder Aktionstagmenü deaktiviert ist.
ms.openlocfilehash: ddf55f40056d7df7a2403e500bb4bae335930433
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431351"
---
# <a name="disabled-cell-actions-section"></a>Zelle "Disabled" (Abschnitt "Actions")

Gibt an, ob ein Element in einem Kontext- oder Aktionstagmenü deaktiviert ist.
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Befehlsnamen deaktivieren (abblenden).  <br/> |
|FALSE  <br/> |Befehlsnamen aktivieren (Standardeinstellung).  <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden Sie zum Erhalten eines Verweises auf die Zelle Disabled anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Aktionen. *Name*  . Deaktiviert, wobei Aktionen. *Name*  ist der Name der Zeile Aktionen  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Deaktivierte Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionAction** <br/> |
|Zeilenindex:  <br/> |**visRowAction**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visActionDisabled** <br/> |
   

