---
title: Zelle "ShapePermeableY" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251666
localization_priority: Normal
ms.assetid: 90701ecf-3d34-2eac-9ee9-7965e16c0f7c
description: Legt fest, ob ein Verbinder vertikal durch ein Shape geleitet werden kann.
ms.openlocfilehash: 62f8bfa0fdfb5c483836f344e8b784dc9092fded
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417518"
---
# <a name="shapepermeabley-cell-shape-layout-section"></a>Zelle "ShapePermeableY" (Abschnitt "Shape Layout")

Legt fest, ob ein Verbinder vertikal durch ein Shape geleitet werden kann.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Verbinder können vertikal durch ein Shape geleitet werden.  <br/> |
|FALSE  <br/> |Verbinder können nicht vertikal durch ein Shape geleitet werden.  <br/> |
   
## <a name="remarks"></a>Hinweise

Sie können den Wert dieser Zelle auch auf der Registerkarte Platzierung im Dialogfeld [](run-in-developer-mode-display-the-developer-tab.md) Verhalten festlegen (wenn eine Form ausgewählt ist, klicken  Sie auf der Registerkarte Entwickler in der Gruppe **Shape-Entwurf** auf **Verhalten,** und klicken Sie dann auf die Registerkarte Platzierung).   
  
In Versionen vor Visio 2000 wird dieses Verhalten in der Zelle ObjInterakt im Abschnitt Miscellaneous festgelegt.
  
Um einen Verweis auf die Zelle ShapePermeableY anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ShapePermeableY  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ShapePermeableY nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
|Zellenindex:  <br/> |**visSLOPermY** <br/> |
   

