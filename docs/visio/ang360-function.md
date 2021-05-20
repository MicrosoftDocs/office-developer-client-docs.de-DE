---
title: ANG360-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251392
localization_priority: Normal
ms.assetid: 23e6899d-0a94-a7d8-8de2-091e0531f163
description: Normalisiert den Winkelbereich.
ms.openlocfilehash: 6916e50daad735843bf0a2a6361fb5b1b833e2ce
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160300"
---
# <a name="ang360-function"></a>ANG360 Function

Normalisiert den Winkelbereich auf 0 = Ergebnis \< \< 2PI-Bogenmaß (0 = Ergebnis \< \< 360 Grad).
  
## <a name="syntax"></a>Syntax

ANG360(***angle*** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _angle_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Der zu normalisierende Winkel.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn  *winkel*  nicht mithilfe von Winkeleinheiten angegeben wird, wird er als Bogenmaß interpretiert. Wenn  *winkel*  nicht in einen Wert konvertiert werden kann, wird #VALUE! zurückgegeben. 
  
## <a name="example-1"></a>Beispiel 1

ANG360(395 deg)
  
Gibt 35 deg zurück.
  
## <a name="example-2"></a>Beispiel 2

ANG360(-9,8 rad.)
  
Gibt 2,7664 Rad zurück.
  
## <a name="example-3"></a>Beispiel 3

ANG360(45)
  
Gibt 58,31 deg (1,0177 Rad) zurück.
  

