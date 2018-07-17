---
title: ISocialProviderGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f40d5405-12e3-475b-b731-d2223ab70c1d
description: Ruft eine Zeichenfolge, die vom Anbieterfunktionen beschreibt.
ms.openlocfilehash: 54e28f22f2dc8fdbe19821d8188087b78c327518
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795975"
---
# <a name="isocialprovidergetcapabilities"></a><span data-ttu-id="73bf2-103">ISocialProvider::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="73bf2-103">ISocialProvider::GetCapabilities</span></span>

<span data-ttu-id="73bf2-104">Ruft eine Zeichenfolge, die vom Anbieterfunktionen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="73bf2-104">Gets a string that describes provider capabilities.</span></span>
  
```cpp
HRESULT _stdcall GetCapabilities([out, retval] BSTR* result);
```

## <a name="parameters"></a><span data-ttu-id="73bf2-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="73bf2-105">Parameters</span></span>

<span data-ttu-id="73bf2-106">_Ergebnis_</span><span class="sxs-lookup"><span data-stu-id="73bf2-106">_result_</span></span>
  
> <span data-ttu-id="73bf2-107">[out] Eine XML-Zeichenfolge, die die Funktionen von einem Anbieter Outlook Social Connector (OSC) darstellt.</span><span class="sxs-lookup"><span data-stu-id="73bf2-107">[out] An XML string that represents the capabilities of an Outlook Social Connector (OSC) provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="73bf2-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="73bf2-108">Remarks</span></span>

<span data-ttu-id="73bf2-109">Die zurückgegebene _Ergebnis_ -XML-Zeichenfolge muss die Schemadefinition für das **Capabilities** -Element gemäß Definition im XML-Schema für die Erweiterbarkeit des OSC-Providers entsprechen.</span><span class="sxs-lookup"><span data-stu-id="73bf2-109">The returned  _result_ XML string must comply with the schema definition for the **capabilities** element, as defined in the XML schema for OSC provider extensibility.</span></span> 
  
<span data-ttu-id="73bf2-110">Der Anbieter muss eine Zeichenfolge _Ergebnis_ , um nachfolgende Aufrufe aus der OSC an den Anbieter ordnungsgemäß ermöglichen zurück.</span><span class="sxs-lookup"><span data-stu-id="73bf2-110">The provider must return a  _result_ string to enable subsequent calls from the OSC to the provider to operate correctly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="73bf2-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73bf2-111">See also</span></span>

- [<span data-ttu-id="73bf2-112">ISocialProvider: IUnknown</span><span class="sxs-lookup"><span data-stu-id="73bf2-112">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)
