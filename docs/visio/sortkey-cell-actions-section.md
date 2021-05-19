---
title: Zelle "SortKey" (Abschnitt "Actions")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027286
localization_priority: Normal
ms.assetid: c0c4b668-f31b-336f-4434-e94a4804ff7c
description: Eine Zahl, mit der die Reihenfolge von Aktionen bestimmt wird, die in einem Kontext- oder Aktionstagmenü angezeigt werden.
ms.openlocfilehash: d4eb98055f199f603003b068dca9fa7b4e377e52
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419660"
---
# <a name="sortkey-cell-actions-section"></a>Zelle "SortKey" (Abschnitt "Actions")

Eine Zahl, mit der die Reihenfolge von Aktionen bestimmt wird, die in einem Kontext- oder Aktionstagmenü angezeigt werden.
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
## <a name="remarks"></a>Hinweise

Die Aktionen in einem Aktionstag- oder Kontextmenü werden im Menü mit der niedrigsten Nummer ganz oben in aufsteigender Reihenfolge angezeigt. Wenn zwei Aktionszeilen den gleichen Wert in der Zelle SortKey aufweisen, wird die Reihenfolge durch die Reihenfolge der Zeilen bestimmt. Der Standardwert ist 0.
  
Verwenden Sie zum Erhalten eines Verweises auf die Zelle SortKey anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Aktionen. *Name*  . SortKeywhere-Aktionen.  *Name*  ist der Name der Zeile Aktionen  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle SortKey nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionAction** <br/> |
|Zeilenindex:  <br/> |**visRowAction**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visActionSortKey** <br/> |
   

