---
title: Zelle "ImgHeight" (Abschnitt "Foreign Image Info")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm445
localization_priority: Normal
ms.assetid: decb86a4-b711-35e1-b9dc-744a84ee177c
description: 'Definiert die Höhe des Bilds des Objekts innerhalb seines Rahmens. Die Standardformel lautet:'
ms.openlocfilehash: 956bc478604fd19d8dfdbb7079e092e9e8a16e7b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411197"
---
# <a name="imgheight-cell-foreign-image-info-section"></a>Zelle "ImgHeight" (Abschnitt "Foreign Image Info")

Definiert die Höhe des Bilds des Objekts innerhalb seines Rahmens. Die Standardformel lautet:
  
= Höhe \* 1
  
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die Zelle ImgHeight anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ImgHeight  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die ImgHeight-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowForeign** <br/> |
| Zellenindex:  <br/> |**visFrgnImgHeight** <br/> |
   

