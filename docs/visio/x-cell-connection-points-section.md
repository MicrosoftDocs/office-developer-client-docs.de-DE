---
title: Zelle "X" (Abschnitt "Connection Points")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251746
localization_priority: Normal
ms.assetid: 11c69600-4e1f-4c52-ff35-b6a7cc6c734c
description: Stellt die x-Koordinate für einen Verbindungspunkt in lokalen Koordinaten dar.
ms.openlocfilehash: 496e5af6ea5b7ba99730b23dcbb510db6af9b23b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436783"
---
# <a name="x-cell-connection-points-section"></a>Zelle "X" (Abschnitt "Connection Points")

Stellt  die x-Koordinate für einen Verbindungspunkt in lokalen Koordinaten dar. 
  
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die Zelle X anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Connections.X  *i*            where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die X-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionConnectionPts** <br/> |
| Zeilenindex:  <br/> |**visRowConnectionPts**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visX** <br/> |
   

