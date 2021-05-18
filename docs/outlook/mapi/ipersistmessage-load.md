---
title: IPersistMessageLoad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.Load
api_type:
- COM
ms.assetid: bd4646d2-8229-499d-91aa-3cbec72b9445
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5024c2f8b88b54051e4b8400f4b3f14374b10c23
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317129"
---
# <a name="ipersistmessageload"></a><span data-ttu-id="fc69a-103">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="fc69a-103">IPersistMessage::Load</span></span>

  
  
<span data-ttu-id="fc69a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc69a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc69a-105">Lädt das Formular für eine angegebene Nachricht.</span><span class="sxs-lookup"><span data-stu-id="fc69a-105">Loads the form for a specified message.</span></span>
  
```cpp
HRESULT Load(
  LPMESSAGESITE pMessageSite,
  LPMESSAGE pMessage,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags
);
```

## <a name="parameters"></a><span data-ttu-id="fc69a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc69a-106">Parameters</span></span>

 <span data-ttu-id="fc69a-107">_pMessageSite_</span><span class="sxs-lookup"><span data-stu-id="fc69a-107">_pMessageSite_</span></span>
  
> <span data-ttu-id="fc69a-108">[in] Ein Zeiger auf die Nachrichtenwebsite, damit das Formular geladen wird.</span><span class="sxs-lookup"><span data-stu-id="fc69a-108">[in] A pointer to the message site for the form to be loaded.</span></span>
    
 <span data-ttu-id="fc69a-109">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="fc69a-109">_pMessage_</span></span>
  
> <span data-ttu-id="fc69a-110">[in] Ein Zeiger auf die Nachricht, für die das Formular geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="fc69a-110">[in] A pointer to the message for which the form should be loaded.</span></span>
    
 <span data-ttu-id="fc69a-111">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="fc69a-111">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="fc69a-112">[in] Eine Bitmaske mit client- oder anbieterdefinierten Flags, die aus der **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))-Eigenschaft der Nachricht kopiert werden, die Informationen über den Status der Nachricht bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="fc69a-112">[in] A bitmask of client-defined or provider-defined flags, copied from the message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property, that provide information about the state of the message.</span></span>
    
 <span data-ttu-id="fc69a-113">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="fc69a-113">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="fc69a-114">[in] Eine Bitmaske mit Flags, die aus der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft der Nachricht kopiert wurde, die weitere Informationen zum Status der Nachricht bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="fc69a-114">[in] A bitmask of flags, copied from the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property, that provide further information about the state of the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fc69a-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fc69a-115">Return value</span></span>

<span data-ttu-id="fc69a-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="fc69a-116">S_OK</span></span> 
  
> <span data-ttu-id="fc69a-117">Das Formular wurde erfolgreich geladen.</span><span class="sxs-lookup"><span data-stu-id="fc69a-117">The form was successfully loaded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fc69a-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fc69a-118">Remarks</span></span>

<span data-ttu-id="fc69a-119">Formularbetrachter rufen die **IPersistMessage::Load-Methode** auf, um ein Formular für eine vorhandene Nachricht zu laden.</span><span class="sxs-lookup"><span data-stu-id="fc69a-119">Form viewers call the **IPersistMessage::Load** method to load a form for an existing message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="fc69a-120">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="fc69a-120">Notes to implementers</span></span>

 <span data-ttu-id="fc69a-121">**Load** wird nur aufgerufen, wenn sich ein Formular in einem der folgenden Zustände befindet:</span><span class="sxs-lookup"><span data-stu-id="fc69a-121">**Load** is called only when a form is in one of the following states:</span></span> 
  
- [<span data-ttu-id="fc69a-122">Nicht initialisiert</span><span class="sxs-lookup"><span data-stu-id="fc69a-122">Uninitialized</span></span>](uninitialized-state.md)
    
- [<span data-ttu-id="fc69a-123">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="fc69a-123">HandsOffAfterSave</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="fc69a-124">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="fc69a-124">HandsOffFromNormal</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="fc69a-125">Wenn ein **Formularanzeiger Load aufruft,** während sich das Formular in einem anderen Zustand befindet, gibt die Methode E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="fc69a-125">If a form viewer calls **Load** while the form is in any other state, the method returns E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="fc69a-126">Wenn Ihr Formular einen Verweis auf eine andere aktive Nachrichtenwebsite als die an **Load** übergebene enthält, geben Sie die ursprüngliche Website frei, da sie nicht mehr verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fc69a-126">If your form has a reference to an active message site other than the one that is passed into **Load**, release the original site because it will no longer be used.</span></span> <span data-ttu-id="fc69a-127">Store die Zeiger auf die Nachrichtenwebsite und -nachricht von den _Parametern pMessageSite_ und _pMessage_ aus und rufen die [IUnknown::AddRef-Methoden](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) beider Objekte auf, um ihre Referenzanzahl zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="fc69a-127">Store the pointers to the message site and message from the  _pMessageSite_ and  _pMessage_ parameters and call both objects' [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) methods to increment their reference counts.</span></span> 
  
<span data-ttu-id="fc69a-128">Speichern Sie nach Abschluss von **AddRef** die Eigenschaften aus den  _Parametern ulMessageStatus_ und  _ulMessageFlags_ im Formular.</span><span class="sxs-lookup"><span data-stu-id="fc69a-128">After **AddRef** has completed, store the properties from the  _ulMessageStatus_ and  _ulMessageFlags_ parameters into the form.</span></span> <span data-ttu-id="fc69a-129">Überwechseln Sie das Formular in den [Status Normal,](normal-state.md) bevor es angezeigt wird, und benachrichtigen Sie registrierte Viewer, indem Sie ihre [IMAPIViewAdviseSink::OnNewMessage-Methoden](imapiviewadvisesink-onnewmessage.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="fc69a-129">Transition the form to its [Normal](normal-state.md) state before displaying it, and notify registered viewers by calling their [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) methods.</span></span> 
  
<span data-ttu-id="fc69a-130">Wenn keine Fehler auftreten, geben Sie S_OK.</span><span class="sxs-lookup"><span data-stu-id="fc69a-130">If no errors occur, return S_OK.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fc69a-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc69a-131">See also</span></span>



[<span data-ttu-id="fc69a-132">PidTagMessageFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="fc69a-132">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="fc69a-133">PidTagMessageStatus (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="fc69a-133">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="fc69a-134">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fc69a-134">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="fc69a-135">Nicht initialisierter Status</span><span class="sxs-lookup"><span data-stu-id="fc69a-135">Uninitialized State</span></span>](uninitialized-state.md)
  
[<span data-ttu-id="fc69a-136">HandsOffAfterSave-Status</span><span class="sxs-lookup"><span data-stu-id="fc69a-136">HandsOffAfterSave State</span></span>](handsoffaftersave-state.md)
  
[<span data-ttu-id="fc69a-137">HandsOffFromNormal-Status</span><span class="sxs-lookup"><span data-stu-id="fc69a-137">HandsOffFromNormal State</span></span>](handsofffromnormal-state.md)
  
[<span data-ttu-id="fc69a-138">Formularzustände</span><span class="sxs-lookup"><span data-stu-id="fc69a-138">Form States</span></span>](form-states.md)


[<span data-ttu-id="fc69a-139">IPersistStorage::Load</span><span class="sxs-lookup"><span data-stu-id="fc69a-139">IPersistStorage::Load</span></span>](https://msdn.microsoft.com/library/34379b8d-4e00-49cd-9fd1-65f88746c61a.aspx)
  
[<span data-ttu-id="fc69a-140">IPersistStream::Load</span><span class="sxs-lookup"><span data-stu-id="fc69a-140">IPersistStream::Load</span></span>](https://msdn.microsoft.com/library/351e1187-9959-4542-8778-925457c3b8e3.aspx)
  
[<span data-ttu-id="fc69a-141">IPersistFile::Load</span><span class="sxs-lookup"><span data-stu-id="fc69a-141">IPersistFile::Load</span></span>](https://msdn.microsoft.com/library/8391aa5c-fe6e-4b03-9eef-7958f75910a5.aspx)

