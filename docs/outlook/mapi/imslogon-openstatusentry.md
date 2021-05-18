---
title: IMSLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 850e256b-6b50-428c-aede-287edaf7b005
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f50c0eb9e3af68e206eaa5bcc51cefa923c30f72
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413178"
---
# <a name="imslogonopenstatusentry"></a><span data-ttu-id="baf32-103">IMSLogon::OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="baf32-103">IMSLogon::OpenStatusEntry</span></span>

  
  
<span data-ttu-id="baf32-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="baf32-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="baf32-105">Öffnet ein Statusobjekt.</span><span class="sxs-lookup"><span data-stu-id="baf32-105">Opens a status object.</span></span>
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPVOID FAR * lppEntry
);
```

## <a name="parameters"></a><span data-ttu-id="baf32-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="baf32-106">Parameters</span></span>

 <span data-ttu-id="baf32-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="baf32-107">_lpInterface_</span></span>
  
> <span data-ttu-id="baf32-108">[in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), damit das Statusobjekt geöffnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="baf32-108">[in] A pointer to the interface identifier (IID) for the status object to open.</span></span> <span data-ttu-id="baf32-109">Das Übergeben von NULL gibt an, dass die Standardschnittstelle für das Objekt zurückgegeben wird (in diesem Fall die [IMAPIStatus-Schnittstelle).](imapistatusimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="baf32-109">Passing NULL indicates the standard interface for the object is returned (in this case, the [IMAPIStatus](imapistatusimapiprop.md) interface).</span></span> <span data-ttu-id="baf32-110">Der  _lpInterface-Parameter_ kann auch auf einen Bezeichner für eine geeignete Schnittstelle für das Objekt festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="baf32-110">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the object.</span></span> 
    
 <span data-ttu-id="baf32-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="baf32-111">_ulFlags_</span></span>
  
> <span data-ttu-id="baf32-112">[in] Eine Bitmaske mit Flags, die steuert, wie das Statusobjekt geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="baf32-112">[in] A bitmask of flags that controls how the status object is opened.</span></span> <span data-ttu-id="baf32-113">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="baf32-113">The following flag can be set:</span></span>
    
<span data-ttu-id="baf32-114">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="baf32-114">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="baf32-115">Fordert Lese-/Schreibberechtigungen an.</span><span class="sxs-lookup"><span data-stu-id="baf32-115">Requests read/write permission.</span></span> <span data-ttu-id="baf32-116">Standardmäßig werden Objekte mit schreibgeschützter Berechtigung erstellt, und Clientanwendungen sollten nicht unter der Annahme funktionieren, dass Lese-/Schreibberechtigungen erteilt wurden.</span><span class="sxs-lookup"><span data-stu-id="baf32-116">By default, objects are created with read-only permission, and client applications should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="baf32-117">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="baf32-117">_lpulObjType_</span></span>
  
> <span data-ttu-id="baf32-118">[out] Ein Zeiger auf den Typ des geöffneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="baf32-118">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="baf32-119">_lppEntry_</span><span class="sxs-lookup"><span data-stu-id="baf32-119">_lppEntry_</span></span>
  
> <span data-ttu-id="baf32-120">[out] Ein Zeiger auf den Zeiger auf das geöffnete Objekt.</span><span class="sxs-lookup"><span data-stu-id="baf32-120">[out] A pointer to the pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="baf32-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="baf32-121">Return value</span></span>

<span data-ttu-id="baf32-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="baf32-122">S_OK</span></span> 
  
> <span data-ttu-id="baf32-123">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="baf32-123">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="baf32-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="baf32-124">Remarks</span></span>

<span data-ttu-id="baf32-125">Nachrichtenspeicheranbieter implementieren die **IMSLogon::OpenStatusEntry-Methode,** um ein Statusobjekt zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="baf32-125">Message store providers implement the **IMSLogon::OpenStatusEntry** method to open a status object.</span></span> <span data-ttu-id="baf32-126">Dieses Statusobjekt wird dann verwendet, um Clients das Aufrufen von [IMAPIStatus-Methoden zu](imapistatusimapiprop.md) ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="baf32-126">This status object is then used to enable clients to call [IMAPIStatus](imapistatusimapiprop.md) methods.</span></span> <span data-ttu-id="baf32-127">Clients können beispielsweise die [IMAPIStatus::SettingsDialog-Methode](imapistatus-settingsdialog.md) verwenden, um die Anmeldesitzung des Nachrichtenspeichers oder die [IMAPIStatus::ValidateState-Methode](imapistatus-validatestate.md) neu zu konfigurieren, um den Status der Anmeldesitzung des Nachrichtenspeichers zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="baf32-127">For example, clients can use the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method to reconfigure the message store logon session or the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method to validate the state of the message store logon session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="baf32-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="baf32-128">See also</span></span>



[<span data-ttu-id="baf32-129">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="baf32-129">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
  
[<span data-ttu-id="baf32-130">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="baf32-130">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="baf32-131">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="baf32-131">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="baf32-132">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="baf32-132">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

