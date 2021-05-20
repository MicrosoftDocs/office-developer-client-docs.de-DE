---
title: Zelle "PagesY" (Abschnitt "Print Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033790
localization_priority: Normal
ms.assetid: 396a0f3e-dbbb-3f5b-3c5d-f7dd454a765f
description: Bestimmt die Anzahl der Druckseiten, auf denen das Zeichenblatt vertikal dargestellt werden soll.
ms.openlocfilehash: 43d4081439525c516d3da28b6c0e46e9273d85c4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429782"
---
# <a name="pagesy-cell-print-properties-section"></a>Zelle "PagesY" (Abschnitt "Print Properties")

Bestimmt die Anzahl der Druckseiten, auf denen das Zeichenblatt vertikal dargestellt werden soll. 
  
## <a name="remarks"></a>Hinweise

Dieser Wert wird nur dann verwendet, wenn die Zelle OnPage auf WAHR festgelegt ist. 
  
Um einen Verweis auf die Zelle PagesY anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | PagesY  <br/> |
   
Um einen Verweis auf die Zelle PagesY nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPrintProperties** <br/> |
| Zeilenindex:  <br/> |**visPrintPropertiesPagesY** <br/> |
   

