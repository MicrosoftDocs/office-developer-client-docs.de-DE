---
title: ASIN-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251395
localization_priority: Normal
ms.assetid: 7d917be4-65b1-002f-48cc-6d81916a1157
description: Gibt den Bogensinus einer Zahl zurück, z. B. den Winkel, dessen Sinus Zahl ist.
ms.openlocfilehash: e66ed9ab3d01ac79bceb18f5c793afc928e5e4b4
ms.sourcegitcommit: 939bd9686ba41a8f94b82e004ed84b9054d9c7cf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2020
ms.locfileid: "48293506"
---
# <a name="asin-function"></a>ASIN Function

Gibt den Bogensinus einer Zahl zurück, z. B. den Winkel, dessen Sinus Zahl *ist.* 
  
## <a name="syntax"></a>Syntax

ASIN(***number*** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Anzahl_ <br/> |Erforderlich  <br/> |**Numeric** <br/> |Der Sinus des Winkels.  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Eingabewert muss sich im Bereich -1 <=  *Zahl*  <= 1 oder einer #NUM! zurückgegeben. Der resultierende Winkel liegt im Bereich -PI/2 < *=*  Winkel <= PI/2 Bogenmaß (-90 < *=*  Winkel <= 90 Grad). 
  
## <a name="example"></a>Beispiel

ASIN(1)
  
Gibt 90 deg zurück.
  

