---
title: IMsgServiceAdminMsgServiceTransportOrder
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.MsgServiceTransportOrder
api_type:
- COM
ms.assetid: c57ada0e-b9a1-496b-8548-75686d8cba4e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3d532e0eb46daa412711344421936a58da309b7b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420094"
---
# <a name="imsgserviceadminmsgservicetransportorder"></a><span data-ttu-id="8f8fa-103">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="8f8fa-103">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>

  
  
<span data-ttu-id="8f8fa-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f8fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8f8fa-105">Legt die Reihenfolge fest, in der Transportanbieter aufgerufen werden, um eine Nachricht zu senden.</span><span class="sxs-lookup"><span data-stu-id="8f8fa-105">Sets the order in which transport providers are called to deliver a message.</span></span>
  
```cpp
HRESULT MsgServiceTransportOrder(
  ULONG cUID,
  LPMAPIUID lpUIDList,
  ULONG ulFlags    
);
```

## <a name="parameters"></a><span data-ttu-id="8f8fa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f8fa-106">Parameters</span></span>

 <span data-ttu-id="8f8fa-107">_cUID_</span><span class="sxs-lookup"><span data-stu-id="8f8fa-107">_cUID_</span></span>
  
> <span data-ttu-id="8f8fa-108">[in] Die Anzahl eindeutiger Bezeichner im _lpUIDList-Parameter._</span><span class="sxs-lookup"><span data-stu-id="8f8fa-108">[in] The count of unique identifiers in the  _lpUIDList_ parameter.</span></span> 
    
 <span data-ttu-id="8f8fa-109">_lpUIDList_</span><span class="sxs-lookup"><span data-stu-id="8f8fa-109">_lpUIDList_</span></span>
  
> <span data-ttu-id="8f8fa-110">[in] Ein Zeiger auf ein Array eindeutiger Bezeichner, die Transportanbieter darstellen.</span><span class="sxs-lookup"><span data-stu-id="8f8fa-110">[in] A pointer to an array of unique identifiers that represent transport providers.</span></span> <span data-ttu-id="8f8fa-111">Das Array enthält einen Bezeichner für jeden Transportanbieter, der im aktuellen Profil konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="8f8fa-111">The array contains one identifier for each transport provider configured in the current profile.</span></span>
    
 <span data-ttu-id="8f8fa-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8f8fa-112">_ulFlags_</span></span>
  
> <span data-ttu-id="8f8fa-113">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="8f8fa-113">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8f8fa-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8f8fa-114">Return value</span></span>

<span data-ttu-id="8f8fa-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="8f8fa-115">S_OK</span></span> 
  
> <span data-ttu-id="8f8fa-116">Der Transportauftrag wurde erfolgreich festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8f8fa-116">The transport order was set successfully.</span></span>
    
<span data-ttu-id="8f8fa-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="8f8fa-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="8f8fa-118">Der Wert im  _cUID-Parameter_ unterscheidet sich von der Anzahl der Tatsächlichen Transportanbieter im Profil.</span><span class="sxs-lookup"><span data-stu-id="8f8fa-118">The value in the  _cUID_ parameter differs from the number of transport providers actually in the profile.</span></span> 
    
<span data-ttu-id="8f8fa-119">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="8f8fa-119">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="8f8fa-120">Mindestens eine der im _lpUIDList-Parameter übergebenen MAPIUID-Strukturen_ bezieht sich nicht auf einen Transportanbieter, der sich derzeit im Profil befindet. [](mapiuid.md)</span><span class="sxs-lookup"><span data-stu-id="8f8fa-120">One or more of the [MAPIUID](mapiuid.md) structures passed in the  _lpUIDList_ parameter do not refer to a transport provider currently in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8f8fa-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8f8fa-121">Remarks</span></span>

<span data-ttu-id="8f8fa-122">Die **IMsgServiceAdmin::MsgServiceTransportOrder-Methode** legt die Zustellungsreihenfolge von Transportanbietern in einem Profil fest.</span><span class="sxs-lookup"><span data-stu-id="8f8fa-122">The **IMsgServiceAdmin::MsgServiceTransportOrder** method sets the delivery order of transport providers in a profile.</span></span> <span data-ttu-id="8f8fa-123">Der  _lpUIDList-Parameter_ muss eine sortierte Liste der Transportanbieter-Eintragsbezeichner **enthalten,** die von der PR_PROVIDER_UID ([PidTagProviderUid](pidtagprovideruid-canonical-property.md))-Eigenschaft der Von der [IMsgServiceAdmin::GetProviderTable-Methode zurückgegebenen](imsgserviceadmin-getprovidertable.md) Tabelle erhalten werden.</span><span class="sxs-lookup"><span data-stu-id="8f8fa-123">The  _lpUIDList_ parameter must contain a sorted list of transport-provider entry identifiers obtained from the **PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) property of the table returned from the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method.</span></span> <span data-ttu-id="8f8fa-124">Eine Clientanwendung muss die vollständige Liste in _lpUIDList übergeben._</span><span class="sxs-lookup"><span data-stu-id="8f8fa-124">A client application must pass the complete list in  _lpUIDList_.</span></span>
  
 <span data-ttu-id="8f8fa-125">**SetTransportOrder** überschreibt Transportanbietereinstellungen, z. B. das STATUS_XP_PREFER_LAST, das in der **eigenschaft PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8f8fa-125">**SetTransportOrder** overrides transport provider preferences such as the STATUS_XP_PREFER_LAST flag set in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8f8fa-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8f8fa-126">See also</span></span>



[<span data-ttu-id="8f8fa-127">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="8f8fa-127">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="8f8fa-128">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8f8fa-128">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

