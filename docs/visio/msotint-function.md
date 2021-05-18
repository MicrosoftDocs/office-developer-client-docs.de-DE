---
title: MSOTINT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bae0af9-229d-e114-4feb-bf6d7a7d8b08
description: Ändert die Farbe, indem deren Helligkeit um den angegebenen Prozentsatz erhöht  wird.
ms.openlocfilehash: d63b90d0cd6fcb35e23a8efa4ca9e13e2838bc21
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406423"
---
# <a name="msotint-function"></a>MSOTINT Function

Ändert die Farbe, indem deren Helligkeit um den angegebenen Prozentsatz erhöht  wird.
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2010
 
  
## <a name="syntax"></a>Syntax

MSOTINT(** *color* **, ** *deltaLum* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Erforderlich  <br/> |**RGB** <br/> |Der standardmäßige RGB-Farbwert (Rot, Grün, Blau) oder eine Referenz auf eine Farbe.  <br/> |
| _deltaLum_ <br/> |Erforderlich  <br/> |**Integer** <br/> |Die prozentuale Änderung in Richtung Weiß (-100 %) oder schwarz (100 %) aus dem _Farbwert._  <br/> |
   
## <a name="remarks"></a>Hinweise

Je näher der  _Farbwert_ weiß oder schwarz ist, desto kleiner ist die Änderung des Farbtons, der durch einen bestimmten  _deltaLum-Wert erzeugt_ wird. 
  

