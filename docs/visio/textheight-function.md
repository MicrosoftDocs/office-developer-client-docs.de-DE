---
title: TEXTHEIGHT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251504
localization_priority: Normal
ms.assetid: 5a10892f-c8fa-c127-2f5a-564009ce5411
description: Gibt die Höhe des zusammengesetzten Texts in einer Form zurück, in der keine Textzeile den maximalen Gesamtwert überschreitet.
ms.openlocfilehash: 7455f58f14f9a4a0ae1fcd5375dba5d5860d3852
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427409"
---
# <a name="textheight-function"></a>TEXTHÖHE-Funktion

Gibt die Höhe des zusammengesetzten Texts in einer Form zurück, in der keine Textzeile den _maximalen Wert überschreitet._ 
  
## <a name="syntax"></a>Syntax

TEXTHEIGHT(** *shapename! TheText* ** ** *[,maximumwidth]* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _shapename!theText_ <br/> |Erforderlich  <br/> |**String** <br/> |Ein Verweis auf die Zelle mit dem Namen TheText in der Zielform.  _shapename!_ ist der Name der Form, aus der Sie den Text abrufen möchten.  <br/> |
| _maximumwidth_ <br/> |Optional.  <br/> |**Numeric** <br/> |Die maximale Breite eines Textblocks.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeichenfolge
  
## <a name="remarks"></a>Hinweise

Der zurückgegebene Wert enthält die Höhe des Texts einschließlich der Abstände vor und hinter dem Text, des Zeilenabstands im Text und der oberen und unteren Textblockränder. Diese Funktion wird meistens verwendet, um die Höhe eines Shapes so anzupassen, dass der gesamte Text vollständig dargestellt wird.
  
## <a name="example"></a>Beispiel

TEXTHEIGHT(TheText,(Width - 0.5 in)) 
  
Gibt die Texthöhe zurück, wenn der Text auf die Breite des Shapes abzüglich 0,5 Zoll umgebrochen wird. 
  

