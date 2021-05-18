---
title: Zelle "Initials" (Abschnitt "Reviewer")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60045
localization_priority: Normal
ms.assetid: 8f5d34f0-4c4b-5265-83c1-5b86b73d464f
description: Enthält die Initialen eines Dokumentbearbeiters.
ms.openlocfilehash: ddca3697dfcf1f422efacbe395c18f1a6b8ac48c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411505"
---
# <a name="initials-cell-reviewer-section"></a>Zelle "Initials" (Abschnitt "Reviewer")

Enthält die Initialen eines Dokumentbearbeiters.
  
## <a name="remarks"></a>Hinweise

Dieser Wert wird standardmäßig auf die Initialen  im Feld **Initialen** auf der  Registerkarte Allgemein im Dialogfeld **Visio-Optionen** festgelegt (klicken Sie auf die Registerkarte Datei, klicken Sie auf **Optionen** und dann auf **Allgemein** ). 
  
Verwenden Sie zum Erhalten eines Verweises auf die Zelle Initialen anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Reviewer.Initials [  *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Initialen nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionReviewer** <br/> |
| Zeilenindex:  <br/> |**visRowReviewer**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visReviewerInitials** <br/> |
   

