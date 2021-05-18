---
title: NOT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251469
localization_priority: Normal
ms.assetid: 65873b32-2406-7c33-8e68-802461f467b2
description: Gibt TRUE (1) zurück, wenn logicalexpression false ist. Andernfalls wird FALSE (0) zurückgegeben.
ms.openlocfilehash: 3359e21654bcc318caf31405093f851eca064119
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413332"
---
# <a name="not-function"></a>NOT Function

Gibt TRUE (1) zurück,  _wenn logicalexpression_ false ist. Andernfalls wird FALSE (0) zurückgegeben. 
  
## <a name="syntax"></a>Syntax

NOT(** *logicalexpression* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _logicalexpression_ <br/> |Erforderlich  <br/> |**String** <br/> |Der logische Ausdruck, der ausgewertet werden soll.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Boolesch
  
## <a name="example"></a>Beispiel

NOT(Height \> 0.75 in) 
  
Gibt 1 zurück, wenn Höhe kleiner als oder gleich 2 cm ist. Gibt 0 zurück, wenn Höhe größer als 2 cm ist. 
  

