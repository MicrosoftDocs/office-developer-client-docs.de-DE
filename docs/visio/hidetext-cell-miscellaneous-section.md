---
title: Zelle "HideText" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251323
localization_priority: Normal
ms.assetid: 3d23647a-e567-da71-50df-336a0f2f4071
description: Blendet den Text für ein Shape aus. Sie können Text anzeigen, Eigenschaften ändern und Formatvorlagen auf den Text im Textblock anwenden. Die Änderungen werden jedoch erst übernommen, wenn Sie HideText auf FALSE (0) zurücksetzen.
ms.openlocfilehash: 3e1be814984ed15247c451f5cd86d0f7a6dba71a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425484"
---
# <a name="hidetext-cell-miscellaneous-section"></a>Zelle "HideText" (Abschnitt "Miscellaneous")

Blendet den Text für ein Shape aus. Sie können Text anzeigen, Eigenschaften ändern und Formatvorlagen auf den Text im Textblock anwenden. Die Änderungen werden jedoch erst übernommen, wenn Sie HideText auf FALSE (0) zurücksetzen.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Text ist verborgen und wird nicht ausgedruckt.  <br/> |
| FALSE  <br/> | Text ist nicht verborgen.  <br/> |
   
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die Zelle HideText anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | HideText  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die HideText-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowMisc** <br/> |
| Zellenindex:  <br/> |**visHideText** <br/> |
   

