---
title: MAPIOFFLINE_NOTIFY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e03c5a87-4513-2133-ae0a-11d242f80e4b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6c5480a8f5e008c01c7ab8141317f5f19547ab10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414767"
---
# <a name="mapioffline_notify"></a><span data-ttu-id="b7959-103">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="b7959-103">MAPIOFFLINE_NOTIFY</span></span>

<span data-ttu-id="b7959-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b7959-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b7959-105">Dies ist die Benachrichtigung für eine Änderung des Verbindungsstatus.</span><span class="sxs-lookup"><span data-stu-id="b7959-105">This is the notification for a change in the connection state.</span></span> <span data-ttu-id="b7959-106">Er gibt den Teil des geänderten Verbindungsstatus, den alten Verbindungsstatus und den neuen Verbindungsstatus an.</span><span class="sxs-lookup"><span data-stu-id="b7959-106">It indicates the part of the connection state that has changed, the old connection state, and the new connection state.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b7959-107">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="b7959-107">Quick info</span></span>

<span data-ttu-id="b7959-108">Weitere Informationen finden Sie unter **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="b7959-108">See **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
  
```cpp
typedef struct  
{ 
      ULONG ulSize; 
      MAPIOFFLINE_NOTIFY_TYPE NotifyType; 
      ULONG ulClientToken; 
      union { 
         struct 
           { 
           ULONG ulMask; 
           ULONG ulStateOld; 
           ULONG ulStateNew; 
           } StateChange; 
             } Info; 
} MAPIOFFLINE_NOTIFY;
```

## <a name="members"></a><span data-ttu-id="b7959-109">Elemente</span><span class="sxs-lookup"><span data-stu-id="b7959-109">Members</span></span>

 <span data-ttu-id="b7959-110">_ulSize_</span><span class="sxs-lookup"><span data-stu-id="b7959-110">_ulSize_</span></span>
  
> <span data-ttu-id="b7959-111">Größe der **MAPIOFFLINE_NOTIFY** Struktur.</span><span class="sxs-lookup"><span data-stu-id="b7959-111">Size of the **MAPIOFFLINE_NOTIFY** structure.</span></span> 
    
 <span data-ttu-id="b7959-112">_NotifyType_</span><span class="sxs-lookup"><span data-stu-id="b7959-112">_NotifyType_</span></span>
  
> <span data-ttu-id="b7959-113">Typ der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="b7959-113">Type of notification.</span></span> <span data-ttu-id="b7959-114">Beachten Sie, dass nur Benachrichtigungen über die Änderung des Verbindungsstatus unterstützt werden. Die einzigen unterstützten Werte sind:</span><span class="sxs-lookup"><span data-stu-id="b7959-114">Note that only notification on change of the connection state is supported; the only supported values are:</span></span>
    
   - <span data-ttu-id="b7959-115">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START</span><span class="sxs-lookup"><span data-stu-id="b7959-115">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START</span></span>
    
   - <span data-ttu-id="b7959-116">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE</span><span class="sxs-lookup"><span data-stu-id="b7959-116">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE</span></span>
    
   - <span data-ttu-id="b7959-117">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE</span><span class="sxs-lookup"><span data-stu-id="b7959-117">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE</span></span>
    
 <span data-ttu-id="b7959-118">_ulClientToken_</span><span class="sxs-lookup"><span data-stu-id="b7959-118">_ulClientToken_</span></span>
  
> <span data-ttu-id="b7959-119">Ein vom Client in **[](mapioffline_adviseinfo.md)** der MAPIOFFLINE_ADVISEINFO in **[IMAPIOfflineMgr::Advise definiertes Token.](imapiofflinemgr-advise.md)**</span><span class="sxs-lookup"><span data-stu-id="b7959-119">A token defined by the client in the **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** structure in **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> 
    
 <span data-ttu-id="b7959-120">_ulMask_</span><span class="sxs-lookup"><span data-stu-id="b7959-120">_ulMask_</span></span>
  
> <span data-ttu-id="b7959-121">Der Teil des Verbindungsstatus, der geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="b7959-121">The part of the connection state that has changed.</span></span> <span data-ttu-id="b7959-122">Der einzige unterstützte Wert ist MAPIOFFLINE_STATE_OFFLINE_MASK.</span><span class="sxs-lookup"><span data-stu-id="b7959-122">The only supported value is MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span>
    
 <span data-ttu-id="b7959-123">_ulStateOld_</span><span class="sxs-lookup"><span data-stu-id="b7959-123">_ulStateOld_</span></span>
  
> <span data-ttu-id="b7959-124">Der alte Verbindungsstatus.</span><span class="sxs-lookup"><span data-stu-id="b7959-124">The old connection state.</span></span> <span data-ttu-id="b7959-125">Die einzigen unterstützten Werte sind:</span><span class="sxs-lookup"><span data-stu-id="b7959-125">The only supported values are:</span></span>
    
   - <span data-ttu-id="b7959-126">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="b7959-126">MAPIOFFLINE_STATE_OFFLINE</span></span>
    
   - <span data-ttu-id="b7959-127">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="b7959-127">MAPIOFFLINE_STATE_ONLINE</span></span>
    
 <span data-ttu-id="b7959-128">_ulStateNew_</span><span class="sxs-lookup"><span data-stu-id="b7959-128">_ulStateNew_</span></span>
  
> <span data-ttu-id="b7959-129">Der neue Verbindungsstatus.</span><span class="sxs-lookup"><span data-stu-id="b7959-129">The new connection state.</span></span> <span data-ttu-id="b7959-130">Die einzigen unterstützten Werte sind:</span><span class="sxs-lookup"><span data-stu-id="b7959-130">The only supported values are:</span></span>
    
   - <span data-ttu-id="b7959-131">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="b7959-131">MAPIOFFLINE_STATE_OFFLINE</span></span>
    
   - <span data-ttu-id="b7959-132">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="b7959-132">MAPIOFFLINE_STATE_ONLINE</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b7959-133">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b7959-133">Remarks</span></span>

<span data-ttu-id="b7959-134">Die Offlinestatus-API unterstützt nur Benachrichtigungen für Online-/Offlineänderungen.</span><span class="sxs-lookup"><span data-stu-id="b7959-134">The Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="b7959-135">Ein Client muss überprüfen, Outlook die folgenden Werte zurückgibt, bevor die tatsächliche Änderung untersucht wird:</span><span class="sxs-lookup"><span data-stu-id="b7959-135">A client must check that Outlook returns the following values before examining the actual change:</span></span>
  
1.  <span data-ttu-id="b7959-136">*NotifyType*  hat den Wert MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START, MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE oder MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE.</span><span class="sxs-lookup"><span data-stu-id="b7959-136">*NotifyType*  has the value MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START, MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE, or MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE.</span></span> <span data-ttu-id="b7959-137">In diesem Fall kann der Client davon ausgehen, dass es sich bei der Änderung um eine Verbindungsstatusänderung handelt, und  *Info*  hat die Struktur  *StateChange*  .</span><span class="sxs-lookup"><span data-stu-id="b7959-137">In this case, the client can assume that the change is a connection state change, and  *Info*  is of the structure  *StateChange*  .</span></span> 
    
2.  <span data-ttu-id="b7959-138">*ulMask*  hat den Wert MAPIOFFLINE_STATE_OFFLINE_MASK.</span><span class="sxs-lookup"><span data-stu-id="b7959-138">*ulMask*  has the value MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span> <span data-ttu-id="b7959-139">In diesem Fall kann der Client davon ausgehen, dass es sich bei der Änderung um eine Änderung des Online-/Offlineverbindungsstatus handelt, und er kann mit der Prüfung *von ulStateOld* und *ulStateNew fortfahren.*</span><span class="sxs-lookup"><span data-stu-id="b7959-139">In this case, the client can assume that the change is an online/offline connection state change, and can proceed with examining  *ulStateOld*  and  *ulStateNew*  .</span></span> 
    
<span data-ttu-id="b7959-140">Es ist möglich, Outlook einen Client über andere Änderungen benachrichtigt, die nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b7959-140">It is possible that Outlook notifies a client of other changes that are not supported.</span></span> <span data-ttu-id="b7959-141">In solchen Fällen wäre *NotifyType* keiner der drei zuvor angegebenen Werte, oder *ulMask* wäre nicht MAPIOFFLINE_STATE_OFFLINE_MASK, und der Client muss die restlichen Daten in *Info ignorieren.*</span><span class="sxs-lookup"><span data-stu-id="b7959-141">In such cases,  *NotifyType*  would not be any one of the three values stated previously, or  *ulMask*  would not be MAPIOFFLINE_STATE_OFFLINE_MASK, and the client must ignore the rest of the data in  *Info*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b7959-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7959-142">See also</span></span>

- [<span data-ttu-id="b7959-143">Informationen zur Offlinestatus-API</span><span class="sxs-lookup"><span data-stu-id="b7959-143">About the Offline State API</span></span>](about-the-offline-state-api.md)  
- [<span data-ttu-id="b7959-144">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="b7959-144">MAPI Constants</span></span>](mapi-constants.md)  
- [<span data-ttu-id="b7959-145">MAPIOFFLINE_NOTIFY_TYPE</span><span class="sxs-lookup"><span data-stu-id="b7959-145">MAPIOFFLINE_NOTIFY_TYPE</span></span>](mapioffline_notify_type.md)

