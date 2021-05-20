---
title: Zelle "Disabled" (Abschnitt "Action Tags")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60038
localization_priority: Normal
ms.assetid: bf0a80c9-0fdb-e2cf-3ab0-74cb6338fdce
description: Gibt an, ob das Aktionstag im Zeichnungsfenster angezeigt wird.
ms.openlocfilehash: 867d36e27cb890509b0687500caf719362a711fb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439667"
---
# <a name="disabled-cell-action-tags-section"></a>Zelle "Disabled" (Abschnitt "Action Tags")

Gibt an, ob das Aktionstag im Zeichnungsfenster angezeigt wird.
  
> [!NOTE]
> In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Das Aktionstag ist deaktiviert.  <br/> |
| FALSE  <br/> | Das Aktionstag ist aktiviert (Standardeinstellung).  <br/> |
   
## <a name="remarks"></a>Hinweise

Deaktivierte Aktionstags werden erst angezeigt, wenn sie wieder aktiviert werden. 
  
Verwenden Sie zum Erhalten eines Verweises auf die Zelle Disabled anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | SmartTags.  *Name*  . Deaktiviert, wobei SmartTags. *Name*  ist der Name der Aktionstagzeile  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Deaktivierte Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionSmartTag** <br/> |
| Zeilenindex:  <br/> |**visRowSmartTag**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visSmartTagDisabled** <br/> |
   

