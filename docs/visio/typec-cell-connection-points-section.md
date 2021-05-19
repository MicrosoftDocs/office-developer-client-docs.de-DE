---
title: Zelle "Type / C" (Abschnitt "Connection Points")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251723
localization_priority: Normal
ms.assetid: 2264d026-2041-3855-2b23-553ce67ae69d
description: Legt den Verbindungspunkttyp fest.
ms.openlocfilehash: a73554d9f3a3bce6a039689d2c0b192a1c5b69aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415236"
---
# <a name="type--c-cell-connection-points-section"></a>Zelle "Type / C" (Abschnitt "Connection Points")

Legt den Verbindungspunkttyp fest.
  
|**Wert**|**Typ**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Nach innen  <br/> |**visCnnctTypeInward** <br/> |
|1  <br/> |Nach außen  <br/> |**visCnnctTypeOutward** <br/> |
|2  <br/> |Nach innen &amp; nach außen  <br/> |**visCnnctTypeInwardOutward** <br/> |
   
## <a name="remarks"></a>Hinweise

Sie können den Verbindungspunkttyp auch festlegen, indem Sie das Tool **Automatischer Verbinder** sowie ein Shape auswählen und anschließend mit der rechten Maustaste auf einen Verbindungspunkt klicken. Dazu müssen Sie in den [Entwicklermodus](run-in-developer-mode-display-the-developer-tab.md) wechseln. 
  
Verwenden Sie zum Erhalten eines Verweises auf die Zelle Type /C anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Connections.Type[  *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Type /C nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionConnectionPts** <br/> |
|Zeilenindex:  <br/> |**visRowConnectionPts**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visCnnctType** (nicht erweiterte Zeilen) **visCnnctC** (erweiterte Zeilen)  <br/> |
   
Informationen zu erweiterten und nicht erweiterten Zeilen finden Sie in der Zeile Connections Points.
  

