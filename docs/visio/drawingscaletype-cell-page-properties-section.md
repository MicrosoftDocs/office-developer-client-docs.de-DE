---
title: Zelle "DrawingScaleType" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm270
localization_priority: Normal
ms.assetid: 5d4f1cf8-bc1f-07b8-1da5-7253808e337e
description: Legt den im Dialogfeld Seite einrichten ausgewählten Zeichnungsmaßstab fest (klicken Sie auf der Registerkarte Start auf den Pfeil neben Seite einrichten).
ms.openlocfilehash: d1c1c00ffe025c566646a1f8b9fe034732ad86a8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428739"
---
# <a name="drawingscaletype-cell-page-properties-section"></a>Zelle "DrawingScaleType" (Abschnitt "Page Properties")

Legt den im Dialogfeld **Seite einrichten** ausgewählten Zeichnungsmaßstab fest (klicken Sie auf der Registerkarte **Start** auf den Pfeil neben **Seite einrichten**). 
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Kein Maßstab  <br/> |**visNoScale** <br/> |
| 1  <br/> | Architekturmaßstab  <br/> |**visArchitectural** <br/> |
| 2  <br/> | Tiefbaumaßstab  <br/> |**visEngineering** <br/> |
| 3  <br/> | Benutzerdefinierter Maßstab  <br/> |**visScaleCustom** <br/> |
| 4   <br/> | Metrik  <br/> |**visScaleMetric** <br/> |
| 5   <br/> | Maschinenbaumaßstab  <br/> |**visScaleChanal** <br/> |
   
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die Zelle DrawingScaleType anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | DrawingScaleType  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die DrawingScaleType-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPage** <br/> |
| Zellenindex:  <br/> |**visPageDrawScaleType** <br/> |
   

