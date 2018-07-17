---
title: IMAPISupportWrapStoreEntryID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.WrapStoreEntryID
api_type:
- COM
ms.assetid: 923fb879-5f32-4fe2-8920-2ec17002256c
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 25c04f8dee012f4985db98df7d1b3ae5536ef6b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792425"
---
# <a name="imapisupportwrapstoreentryid"></a><span data-ttu-id="86fce-103">IMAPISupport::WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="86fce-103">IMAPISupport::WrapStoreEntryID</span></span>

  
  
<span data-ttu-id="86fce-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="86fce-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="86fce-105">Konvertiert einen Nachrichtenspeicher interne Eintrags-ID auf einen Eintrag Bezeichner MAPI-Standardformat.</span><span class="sxs-lookup"><span data-stu-id="86fce-105">Converts a message store's internal entry identifier to an entry identifier in the MAPI standard format.</span></span>
  
```cpp
HRESULT WrapStoreEntryID(
ULONG cbOrigEntry,
LPENTRYID lpOrigEntry,
ULONG FAR * lpcbWrappedEntry,
LPENTRYID FAR * lppWrappedEntry
);
```

## <a name="parameters"></a><span data-ttu-id="86fce-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="86fce-106">Parameters</span></span>

 <span data-ttu-id="86fce-107">_cbOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="86fce-107">_cbOrigEntry_</span></span>
  
> <span data-ttu-id="86fce-108">[in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpOrigEntry_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="86fce-108">[in] The byte count in the entry identifier pointed to by the  _lpOrigEntry_ parameter.</span></span> 
    
 <span data-ttu-id="86fce-109">_lpOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="86fce-109">_lpOrigEntry_</span></span>
  
> <span data-ttu-id="86fce-110">[in] Ein Zeiger auf die private Eintrags-ID für den Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="86fce-110">[in] A pointer to the private entry identifier for the message store.</span></span>
    
 <span data-ttu-id="86fce-111">_lpcbWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="86fce-111">_lpcbWrappedEntry_</span></span>
  
> <span data-ttu-id="86fce-112">[out] Ein Zeiger auf die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LppWrappedEntry_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="86fce-112">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppWrappedEntry_ parameter.</span></span> 
    
 <span data-ttu-id="86fce-113">_lppWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="86fce-113">_lppWrappedEntry_</span></span>
  
> <span data-ttu-id="86fce-114">[out] Ein Zeiger auf einen Zeiger auf den Eintrag gepackten Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="86fce-114">[out] A pointer to a pointer to the wrapped entry identifier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="86fce-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="86fce-115">Return value</span></span>

<span data-ttu-id="86fce-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="86fce-116">S_OK</span></span> 
  
> <span data-ttu-id="86fce-117">Die Eintrags-ID wurde erfolgreich umbrochen.</span><span class="sxs-lookup"><span data-stu-id="86fce-117">The entry identifier was successfully wrapped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="86fce-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="86fce-118">Remarks</span></span>

<span data-ttu-id="86fce-119">Die **IMAPISupport::WrapStoreEntryID** -Methode wird für alle dienstanbieterobjekten Unterstützung implementiert.</span><span class="sxs-lookup"><span data-stu-id="86fce-119">The **IMAPISupport::WrapStoreEntryID** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="86fce-120">Dienstanbieter verwenden **WrapStoreEntryID** MAPI einen Eintrag Bezeichner für einen Nachrichtenspeicher zu erstellen, der den Speicher interne Eintrags-ID umbrochen wird.</span><span class="sxs-lookup"><span data-stu-id="86fce-120">Service providers use **WrapStoreEntryID** to have MAPI generate an entry identifier for a message store that wraps the store's internal entry identifier.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="86fce-121">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="86fce-121">Notes to callers</span></span>

<span data-ttu-id="86fce-122">Wenn ein Client den Nachrichtenspeicher [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode aufruft, um die **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))-Eigenschaft und Nachrichtenspeichers abzurufen verwendet eine Eintrags-ID in einem privaten Format, rufen Sie **WrapStoreEntryID **und die Eintrags-ID auf das durch den Parameter _LppWrappedEntry_ zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="86fce-122">When a client calls your message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property, and your message store uses an entry identifier in a private format, call **WrapStoreEntryID** and return the entry identifier pointed to by the  _lppWrappedEntry_ parameter.</span></span> 
  
<span data-ttu-id="86fce-123">Aufrufe der Methoden [IMSProvider::Logon](imsprovider-logon.md) und [IMSLogon::CompareEntryIDs](imslogon-compareentryids.md) abrufen immer private Eintrags-ID für den Speicher. Die gepackten Version wird nur zwischen Clientanwendungen und MAPI verwendet.</span><span class="sxs-lookup"><span data-stu-id="86fce-123">Calls to the [IMSProvider::Logon](imsprovider-logon.md) and [IMSLogon::CompareEntryIDs](imslogon-compareentryids.md) methods always obtain the store's private entry identifier; the wrapped version is used only between client applications and MAPI.</span></span> 
  
<span data-ttu-id="86fce-124">Freigeben des Speichers für die Eintrags-ID mithilfe der Funktion [MAPIFreeBuffer](mapifreebuffer.md) Sie abschließend mithilfe der Eintrags-ID auf durch den Parameter _LppWrappedEntry_ zeigt.</span><span class="sxs-lookup"><span data-stu-id="86fce-124">Free the memory for the entry identifier pointed to by the  _lppWrappedEntry_ parameter by using the [MAPIFreeBuffer](mapifreebuffer.md) function when you are finished using the entry identifier.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="86fce-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86fce-125">See also</span></span>



[<span data-ttu-id="86fce-126">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="86fce-126">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="86fce-127">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="86fce-127">IMAPISupport::CompareEntryIDs</span></span>](imapisupport-compareentryids.md)
  
[<span data-ttu-id="86fce-128">IMSLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="86fce-128">IMSLogon::CompareEntryIDs</span></span>](imslogon-compareentryids.md)
  
[<span data-ttu-id="86fce-129">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="86fce-129">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="86fce-130">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="86fce-130">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="86fce-131">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="86fce-131">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
