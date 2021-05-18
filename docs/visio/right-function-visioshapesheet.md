---
title: RIGHT-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027314
localization_priority: Normal
ms.assetid: 910f0297-d588-2048-f308-03f3c2389bba
description: Gibt das letzte Zeichen oder die letzten Zeichen in einer Textzeichenfolge basierend auf der angegebenen Anzahl von Zeichen zurück.
ms.openlocfilehash: faf14ef55b34e51bac11129d6857e381d07357c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411456"
---
# <a name="right-function-visioshapesheet"></a>RIGHT-Funktion (VisioShapeSheet)

Gibt das letzte Zeichen oder die letzten Zeichen in einer Textzeichenfolge basierend auf der angegebenen Anzahl von Zeichen zurück.
  
## <a name="syntax"></a>Syntax

RIGHT(** *text* ** [, ** *num_chars_opt* ** ]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Erforderlich  <br/> |**String** <br/> | Die Textzeichenfolge mit den zu extrahierenden Zeichen.  <br/> |
| _num_chars_opt_ <br/> |Optional.  <br/> |**Number** <br/> |Die Anzahl der Zeichen, die extrahiert werden sollen. Standardwert ist 1.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeichenfolge
  
## <a name="remarks"></a>Hinweise

Der Wert der  _num_chars_opt_ muss größer oder gleich Null (0) sein. 
  
Wenn  _num_chars_opt_ die Länge des Texts überwieg, gibt RIGHT den ganzen Text zurück. Wenn  _num_chars_opt_ nicht angegeben wird, wird angenommen, dass es 1 ist. 
  
## <a name="example"></a>Beispiel

RIGHT ("Januar 1, 2004", 4) 
  
Gibt den Wert 2004 zurück. 
  

