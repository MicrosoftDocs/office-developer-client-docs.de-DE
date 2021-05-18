---
title: Month-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5df43594-a434-4fb7-8109-e5cf0401ae09
description: Gibt eine ganze Zahl zurück, die den Monat des angegebenen Datums darstellt.
ms.openlocfilehash: 0ca7059a2fd6dad1f9790ad6f4eafe7affa014dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411491"
---
# <a name="month-function-access-custom-web-app"></a>Month-Funktion (benutzerdefinierte Access-Web-App)

Gibt eine ganze Zahl zurück, die den Monat des angegebenen Datums darstellt.
  
> [!NOTE]
> Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

 **Month** (*Date*) 
  
Die **Month-Funktion** enthält das folgende Argument. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *Date*  <br/> |Ein Ausdruck, der in einen Datums-/Uhrzeitwert aufgelöst werden kann.  <br/> |
   
## <a name="remarks"></a>Hinweise

 **Month** gibt denselben Wert wie **DatePart** (Monat, Datum) zurück. 
  
Wenn  *Date*  nur einen Zeitteil enthält, ist der Rückgabewert 1, der Basismonat. 
  

