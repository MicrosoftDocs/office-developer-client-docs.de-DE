---
title: Zelle "ButtonFace" (Abschnitt "Actions")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60025
localization_priority: Normal
ms.assetid: cf15b879-a47e-a5a5-bfdd-1d7ea423742f
description: Bestimmt das Symbol, das neben einem Element in einem Kontext- oder Aktionstagmenü angezeigt wird.
ms.openlocfilehash: 7ee9c4e7e857acb34ce75429aa0aaf679320b0e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407375"
---
# <a name="buttonface-cell-actions-section"></a>Zelle "ButtonFace" (Abschnitt "Actions")

Bestimmt das Symbol, das neben einem Element in einem Kontext- oder Aktionstagmenü angezeigt wird.
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
## <a name="remarks"></a>Hinweise

Die Zeichenfolge in einer ButtonFace-Zelle stellt die ID einer Microsoft Office-Schaltflächenoberseite dar. Der Wert Null (0) oder ein Leerzeichen bedeutet, dass kein Symbol angezeigt wird. 
  
Die IDs, die in der Zelle ButtonFace verwendet werden können, sind identisch mit den IDs, die mit der **FaceID-Eigenschaft** eines **CommandBarButton-Objekts verwendet** werden. Weitere Informationen zu diesen IDs finden Sie unter "Arbeiten mit Befehlsleistenschaltflächebildern" auf MSDN. 
  
Verwenden Sie zum Erhalten eines Verweises auf die Zelle ButtonFace anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |**Aktionen**:  *Name*  . **ButtonFace,**         wobei **Aktionen**.  *Name*  ist der Name der Aktionszeile  <br/> |
   
Um einen Verweis auf die ButtonFace-Zelle nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionAction** <br/> |
|Zeilenindex:  <br/> |**visRowAction**  +   *i,* **wobei i** = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visActionButtonFace** <br/> |
   

