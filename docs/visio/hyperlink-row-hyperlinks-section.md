---
title: Zeile "Hyperlink" (Abschnitt "Hyperlinks")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3065
localization_priority: Normal
ms.assetid: e3c7ae27-2e54-a174-4fb3-d16093faf759
description: Enthält die Informationen für einen einzelnen Hyperlink, der einem Shape zugeordnet ist. Ein Shape enthält für jeden Hyperlink eine Hyperlink-Zeile.
ms.openlocfilehash: 36b9b62f248e4f5b9407156a79fa674dc2e8f14d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329904"
---
# <a name="hyperlink-row-hyperlinks-section"></a>Zeile "Hyperlink" (Abschnitt "Hyperlinks")

Enthält die Informationen für einen einzelnen Hyperlink, der einem Shape zugeordnet ist. Ein Shape enthält für jeden Hyperlink eine Hyperlink-Zeile.
  
Hyperlinkzeilen heißen Hyperlink. *namen*  und die folgenden Zellen enthalten. Weitere Informationen finden Sie in den spezifischen Zellthemen. 
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[Beschreibung](description-cell-hyperlinks-section.md) <br/> |Ein beschreibender Text als Zeichenfolge für einen Hyperlink.  <br/> |
|[Adresse](address-cell-hyperlinks-section.md) <br/> |URL-Adresse (Uniform Resource Locator), MS-DOS-Dateiname oder UNC-Pfad (Universal Naming Convention), zu der bzw. zu dem gewechselt werden soll.  <br/> |
|[SubAddress](subaddress-cell-hyperlinks-section.md) <br/> |Eine Stelle im Zieldokument für die Verknüpfung.  <br/> |
|[ExtraInfo](extrainfo-cell-hyperlinks-section.md) <br/> |Eine Zeichenfolge, die Informationen für die Auflösung der URL übergibt.  <br/> |
|[Frame](frame-cell-hyperlinks-section.md) <br/> |Der Name eines Rahmens, der als Ziel dienen soll, wenn Microsoft Office Visio als ActiveX-Dokument in einem ActiveX-Container geöffnet ist. Der Standardwert ist eine leere Zeichenfolge.  <br/> |
|[SortKey](sortkey-cell-hyperlinks-section.md) <br/> |Bestimmt die Reihenfolge der Hyperlinks, in der sie im Kontextmenü angezeigt werden.  <br/> |
|[NewWindow](newwindow-cell-hyperlinks-section.md) <br/> |Gibt an, ob der Hyperlink in einem neuen Fenster geöffnet werden soll. Wenn TRUE, öffnet die verknüpfte Seite, das Dokument oder die Website in einem neuen Fenster. Die Standardeinstellung ist FALSE.  <br/> |
|[Default](default-cell-hyperlinks-section.md) <br/> |Der Standardhyperlink für ein Shape oder ein Zeichenblatt.  <br/> |
|[Invisible](invisible-cell-hyperlinks-section.md) <br/> |Gibt an, ob der Hyperlink im Kontextmenü angezeigt wird.  <br/> |
   
## <a name="remarks"></a>Hinweise

 Sie können so viele Hyperlinks hinzufügen.  *name*  rows as you need, assign meaningful names to the rows, and set cell values. Klicken Sie zum Hinzufügen von Hyperlinks zu einem vorhandenen Abschnitt Hyperlinks mit der rechten Maustaste auf eine Zeile, und klicken Sie im Kontextmenü **auf** Zeile einfügen. 
  
Sie können auf diese Zellen durch ihren Zeilennamen verweisen, der in einem ShapeSheet-Fenster in rotem Text angezeigt wird. So weisen Sie Hyperlink aussagekräftige Namen zu. *Namenzeilen,*  klicken Sie auf die Zeile, und geben Sie dann einen Namen wie  *z.*  B. Marketing ein, um den Zeilennamen Hyperlink.Marketing zu erstellen. Anschließend können Sie mithilfe von Hyperlink.Marketing.Description auf die Zelle Description verweisen. 
  
Der eingegebene Zeilenname muss innerhalb des Abschnitts eindeutig sein.
  

