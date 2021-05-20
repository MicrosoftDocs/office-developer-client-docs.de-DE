---
title: TRIM-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027318
localization_priority: Normal
ms.assetid: 6f2d84fd-27eb-4c2f-a2e1-43d20e0c78be
description: Entfernt alle Leerzeichen aus Text, mit Ausnahme einzelner Leerzeichen zwischen Wörtern.
ms.openlocfilehash: b947c9500012d0ceefe3e8044be387f7b810dda9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435719"
---
# <a name="trim-function"></a>TRIM Function

Entfernt alle Leerzeichen aus Text, mit Ausnahme einzelner Leerzeichen zwischen Wörtern. 
  
## <a name="syntax"></a>Syntax

TRIM (** *text* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Text, aus dem die Leerzeichen entfernt werden sollen.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeichenfolge
  
## <a name="remarks"></a>Hinweise

Sie können die Funktion TRIM bei Texten verwenden, die aus einer anderen Anwendung übernommen wurden und überzählige Leerzeichen aufweisen.
  
## <a name="example"></a>Beispiel

TRIM ("1. Januar 2003 ") 
  
Gibt "January 1, 2003" zurück. 
  

