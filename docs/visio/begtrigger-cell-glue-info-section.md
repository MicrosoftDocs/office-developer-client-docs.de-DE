---
title: Zelle "BegTrigger" (Abschnitt "Glue Info")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm100
localization_priority: Normal
ms.assetid: 0b7ffe39-ee6c-71eb-355c-9bb4660260f1
description: Enthält eine von der Anwendung generierte Triggerformel, die festlegt, ob der Anfangspunkt eines 1D-Shapes zur Aufrechterhaltung seiner Verbindung zu einem anderen Shape verschoben werden soll.
ms.openlocfilehash: b401d349119337016a96b5fffbc26f7be2891864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437952"
---
# <a name="begtrigger-cell-glue-info-section"></a>Zelle "BegTrigger" (Abschnitt "Glue Info")

Enthält eine von der Anwendung generierte Triggerformel, die festlegt, ob der Anfangspunkt eines 1D-Shapes zur Aufrechterhaltung seiner Verbindung zu einem anderen Shape verschoben werden soll.
  
## <a name="remarks"></a>Hinweise

Wenn Sie ein 1D-Shape mit dynamischem Kleber an ein anderes Shape kleben, generiert die Anwendung eine Formel, die sich auf die Zelle EventXFMod eines anderen Shapes bezieht. Wenn das Shape geändert wird, berechnet Visio alle auf die Zelle EventXFMod bezogenen Formeln neu, einschließlich der Formel in der Zelle BegTrigger. Andere Formeln für das 1D-Shape beziehen sich auf die Zelle BegTrigger und verschieben den Anfangspunkt des 1D-Shape oder verändern ggf. das Shape entsprechend.
  
Um einen Verweis auf die Zelle "BegTrigger" anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | BegTrigger  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle "BegTrigger" nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowGroup** <br/> |
| Zellenindex:  <br/> |**visBegTrigger** <br/> |
   

