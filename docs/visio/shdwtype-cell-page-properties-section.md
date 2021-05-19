---
title: Zelle "ShdwType" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60084
localization_priority: Normal
ms.assetid: 551166d0-3aaa-0fd7-e742-cf3450ba90ed
description: Gibt den Standardschattentyp eines Zeichenblatts an.
ms.openlocfilehash: f1fc72484d94788ca2798760ca935c89c3e841ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424098"
---
# <a name="shdwtype-cell-page-properties-section"></a>Zelle "ShdwType" (Abschnitt "Page Properties")

Gibt den Standardschattentyp eines Zeichenblatts an.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 1  <br/> | Einfach  <br/> |**visFSTSimple** <br/> |
| 2  <br/> | Schräg  <br/> |**visFSTOblique** <br/> |
|3  <br/> |Inner  <br/> |**visFSTInner** <br/> |
   
## <a name="remarks"></a>Hinweise

 Der in dieser Zelle beschriebene Schattentyp wird immer dann verwendet, wenn die Zelle ShapeShdwType (der Schattentyp für eine einzelne Form auf der Seite) auf Page Default (**visFSTPageDefault** ) festgelegt ist. 
  
Einfache Schattentypen werden als Abstandsschatten auf der Benutzeroberfläche beschrieben. Ein einfacher Schatten gibt den Effekt, dass die Form auf eine parallele Ebene überschattet wird, die sich etwas hinter ihr befindet. Schräge Schatten werden als schräge Schatten auf der Benutzeroberfläche beschrieben und haben den Effekt, dass der Schatten auf einer zum Shape rechtwinkligen Ebene zu liegen scheint. 
  
Eine Liste vordefinierter einfacher und schräger Schattentypen finden Sie im Dialogfeld **Seite einrichten** auf der Registerkarte **Schatten** in der Liste **Formatvorlage** (klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**). 
  
Um einen Verweis auf die Zelle ShdwType anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ShdwType  <br/> |
   
Um einen Verweis auf die Zelle ShapeShdwOffsetX nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPage** <br/> |
| Zellenindex:  <br/> |**visPageShdwType** <br/> |
   

