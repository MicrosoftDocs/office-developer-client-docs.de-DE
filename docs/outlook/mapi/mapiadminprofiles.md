---
title: "\"MAPIAdminProfiles\""
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAdminProfiles
api_type:
- HeaderDef
ms.assetid: 82a9e379-39e4-4257-8cba-a6758f431cdc
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3cd1a19b23a3c4d3ff8a297881eb2b959585eb17
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793119"
---
# <a name="mapiadminprofiles"></a><span data-ttu-id="3d344-103">"MAPIAdminProfiles"</span><span class="sxs-lookup"><span data-stu-id="3d344-103">MAPIAdminProfiles</span></span>

  
  
<span data-ttu-id="3d344-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3d344-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3d344-105">Erstellt ein Profil Administration-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3d344-105">Creates a profile administration object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3d344-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="3d344-106">Header file:</span></span>  <br/> |<span data-ttu-id="3d344-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="3d344-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="3d344-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="3d344-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3d344-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3d344-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3d344-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="3d344-110">Called by:</span></span>  <br/> |<span data-ttu-id="3d344-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="3d344-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPIAdminProfiles(
  ULONG ulFlags,
  LPPROFADMIN FAR * lppProfAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="3d344-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d344-112">Parameters</span></span>

 <span data-ttu-id="3d344-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3d344-113">_ulFlags_</span></span>
  
> <span data-ttu-id="3d344-114">[in] Bitmaske aus Flags, die Optionen für die Funktion Eintrag angibt.</span><span class="sxs-lookup"><span data-stu-id="3d344-114">[in] Bitmask of flags indicating options for the service entry function.</span></span> 
    
 <span data-ttu-id="3d344-115">_lppProfAdmin_</span><span class="sxs-lookup"><span data-stu-id="3d344-115">_lppProfAdmin_</span></span>
  
> <span data-ttu-id="3d344-116">[out] Zeiger auf einen Zeiger auf das neue Profil Administration-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3d344-116">[out] Pointer to a pointer to the new profile administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3d344-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="3d344-117">Return value</span></span>

<span data-ttu-id="3d344-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="3d344-118">S_OK</span></span> 
  
> <span data-ttu-id="3d344-119">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="3d344-119">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="3d344-120">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="3d344-120">MFCMAPI reference</span></span>

<span data-ttu-id="3d344-121">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="3d344-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3d344-122">**Datei**</span><span class="sxs-lookup"><span data-stu-id="3d344-122">**File**</span></span>|<span data-ttu-id="3d344-123">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="3d344-123">**Function**</span></span>|<span data-ttu-id="3d344-124">**Comment**</span><span class="sxs-lookup"><span data-stu-id="3d344-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3d344-125">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="3d344-125">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="3d344-126">CMapiObjects::GetProfAdmin</span><span class="sxs-lookup"><span data-stu-id="3d344-126">CMapiObjects::GetProfAdmin</span></span>  <br/> |<span data-ttu-id="3d344-127">MFCMAPI (engl.) verwendet die **"MAPIAdminProfiles"** -Methode, um das Profil Administration-Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3d344-127">MFCMAPI uses the **MAPIAdminProfiles** method to get the profile administration object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3d344-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d344-128">See also</span></span>



[<span data-ttu-id="3d344-129">IProfAdmin::CreateProfile</span><span class="sxs-lookup"><span data-stu-id="3d344-129">IProfAdmin::CreateProfile</span></span>](iprofadmin-createprofile.md)


[<span data-ttu-id="3d344-130">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="3d344-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
