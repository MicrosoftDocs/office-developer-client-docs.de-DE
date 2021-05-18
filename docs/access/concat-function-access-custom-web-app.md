---
title: Verkettungsfunktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 38ad6365-79df-4342-9b76-ca27b8ab8952
description: Gibt eine Zeichenfolge zurück, die das Ergebnis der Kombination von zwei oder mehr Zeichenfolgenwerte ist.
ms.openlocfilehash: b8f52c292e64939f9464bc666ecc4bc341580f94
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423272"
---
# <a name="concat-function-access-custom-web-app"></a>Verkettungsfunktion (benutzerdefinierte Access-Web-App)

Gibt eine Zeichenfolge zurück, die das Ergebnis der Kombination von zwei oder mehr Zeichenfolgenwerte ist.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

**Concat** (*Value1*, *Value2*, ... [*ValueN*]) 
  
Die Funktion **Verketten** enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
|Wert  <br/> |Ein Zeichenfolgenwert, der mit den anderen Werten verkettet werden soll.  <br/> |
   
## <a name="remarks"></a>Hinweise

**Verketten** verwendet eine unterschiedliche Anzahl von Zeichenfolgenargumenten und verkettet diese zu einer einzigen Zeichenfolge. Mindestens zwei Zeichenfolgenargumente sind erforderlich. Andernfalls wird ein Fehler ausgelöst. 
  
Alle Argumente werden implizit in Zeichenfolgen-Datentypen konvertiert und dann verkettet.
  
## <a name="example"></a>Beispiel

Der folgende Ausdruck kann verwendet werden, um den vollständigen Namen einer Person anzuzeigen, für welche die Tabelle die Felder "LastName", "FirstName" und "MiddleInitial" enthält. Wenn das Feld MiddleInitial leer ist, werden nur die Felder FirstName und LastName kombiniert, um den vollständigen Namen anzeigen zu können.
  
```vb
IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))
```


