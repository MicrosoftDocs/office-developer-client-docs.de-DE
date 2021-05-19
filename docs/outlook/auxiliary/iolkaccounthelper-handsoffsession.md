---
title: IOlkAccountHelperHandsOffSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9f71fdef-5df5-0892-b64c-293a2f22f5c3
description: Gibt das MAPI-Sitzungsobjekt frei, das von IOlkAccountHelper::GetMapiSession zurückgegeben wurde.
ms.openlocfilehash: c481cee1ecb8c2bd3997cdee8ae86c9c3b5a712e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418631"
---
# <a name="iolkaccounthelperhandsoffsession"></a><span data-ttu-id="78c5f-103">IOlkAccountHelper::HandsOffSession</span><span class="sxs-lookup"><span data-stu-id="78c5f-103">IOlkAccountHelper::HandsOffSession</span></span>

<span data-ttu-id="78c5f-104">Gibt das MAPI-Sitzungsobjekt frei, das von - [IOlkAccountHelper::GetMapiSession zurückgegeben wurde.](iolkaccounthelper-getmapisession.md)</span><span class="sxs-lookup"><span data-stu-id="78c5f-104">Releases the MAPI session object that was returned by - [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="78c5f-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="78c5f-105">Quick info</span></span>

<span data-ttu-id="78c5f-106">Siehe [IOlkAccountHelper](iolkaccounthelper.md).</span><span class="sxs-lookup"><span data-stu-id="78c5f-106">See [IOlkAccountHelper](iolkaccounthelper.md).</span></span>
  
```cpp
HRESULT IOlkAccountHelper::HandsOffSession( );
```

## <a name="return-values"></a><span data-ttu-id="78c5f-107">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="78c5f-107">Return values</span></span>

|<span data-ttu-id="78c5f-108">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="78c5f-108">**HRESULT**</span></span>|<span data-ttu-id="78c5f-109">**Description**</span><span class="sxs-lookup"><span data-stu-id="78c5f-109">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="78c5f-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="78c5f-110">S_OK</span></span>  <br/> |<span data-ttu-id="78c5f-111">Wenn Ihre Implementierung von **IOlkAccountHelper** eine eigene MAPI-Sitzung erstellt, die in **IOlkAccountHelper::GetMapiSession** zurückgegeben wird, müssen Sie die Sitzung hier veröffentlichen und S_OK.</span><span class="sxs-lookup"><span data-stu-id="78c5f-111">If your implementation of **IOlkAccountHelper** creates its own MAPI session that is returned in **IOlkAccountHelper::GetMapiSession**, you must release the session here and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="78c5f-112">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="78c5f-112">E_NOTIMPL</span></span>  <br/> |<span data-ttu-id="78c5f-113">Wenn Ihre Implementierung von **IOlkAccountHelper** keine eigene MAPI-Sitzung erstellt hat, müssen Sie nur eine E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="78c5f-113">If your implementation of **IOlkAccountHelper** did not create its own MAPI session, you must return only E_NOTIMPL.</span></span> <span data-ttu-id="78c5f-114">In diesem Fall ist dies der einzige unterstützte Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="78c5f-114">In this case, this is the only supported return value.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="78c5f-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78c5f-115">See also</span></span>

- [<span data-ttu-id="78c5f-116">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="78c5f-116">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="78c5f-117">IOlkAccountHelper::GetMapiSession</span><span class="sxs-lookup"><span data-stu-id="78c5f-117">IOlkAccountHelper::GetMapiSession</span></span>](iolkaccounthelper-getmapisession.md)

