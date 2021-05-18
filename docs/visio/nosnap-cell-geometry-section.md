---
title: Zelle "NoSnap" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm740
localization_priority: Normal
ms.assetid: 0e6c8621-868c-9eac-926b-3049f18023b0
description: Definiert, ob andere Shapes an einem Pfad einrasten.
ms.openlocfilehash: 60a6532aee0f391eb38609f6ed87577e5558d5c2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408544"
---
# <a name="nosnap-cell-geometry-section"></a>Zelle "NoSnap" (Abschnitt "Geometry")

Definiert, ob andere Shapes an einem Pfad einrasten.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Andere Shapes können nicht an diesem Pfad einrasten.  <br/> |
| FALSE  <br/> | Andere Shapes können an diesem Pfad einrasten.  <br/> |
   
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die Zelle NoSnap anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometry  *i*  . NoSnap, wobei  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die NoSnap-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionFirstComponent**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visRowComponent** <br/> |
| Zeilenindex:  <br/> |**visCompNoSnap** <br/> |
   

