---
title: IOlkAccountHelperGetMapiSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a431787c-6e9a-9be1-165f-98c778d12e3e
description: Öffnet eine MAPI-Sitzung und verwaltet einen Verweis auf die Sitzung für den Konto-Manager.
ms.openlocfilehash: 5886ac1ae1bb8f3b43e09f49e48434d9a73656ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322176"
---
# <a name="iolkaccounthelpergetmapisession"></a><span data-ttu-id="fa7f1-103">IOlkAccountHelper::GetMapiSession</span><span class="sxs-lookup"><span data-stu-id="fa7f1-103">IOlkAccountHelper::GetMapiSession</span></span>

<span data-ttu-id="fa7f1-104">Öffnet eine MAPI-Sitzung und verwaltet einen Verweis auf die Sitzung für den Konto-Manager.</span><span class="sxs-lookup"><span data-stu-id="fa7f1-104">Opens a MAPI session and maintains a reference to the session for the account manager.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="fa7f1-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="fa7f1-105">Quick info</span></span>

<span data-ttu-id="fa7f1-106">Siehe [IOlkAccountHelper](iolkaccounthelper.md).</span><span class="sxs-lookup"><span data-stu-id="fa7f1-106">See [IOlkAccountHelper](iolkaccounthelper.md).</span></span>
  
```cpp
HRESULT IOlkAccountHelper::GetMapiSession(  
    LPUNKNOWN *ppmsess 
);
```

## <a name="parameters"></a><span data-ttu-id="fa7f1-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa7f1-107">Parameters</span></span>

<span data-ttu-id="fa7f1-108">_ppmsess_</span><span class="sxs-lookup"><span data-stu-id="fa7f1-108">_ppmsess_</span></span>
  
> <span data-ttu-id="fa7f1-109">[out] Die aktuelle MAPI-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="fa7f1-109">[out] The current MAPI session.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="fa7f1-110">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="fa7f1-110">Return values</span></span>

<span data-ttu-id="fa7f1-111">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="fa7f1-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fa7f1-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fa7f1-112">Remarks</span></span>

<span data-ttu-id="fa7f1-113">Aufgrund von Zirkelverweisproblemen kann der Kontomanager selbst den Verweis für die MAPI-Sitzung nicht verwalten.</span><span class="sxs-lookup"><span data-stu-id="fa7f1-113">Because of circular reference problems, the account manager itself cannot maintain the reference for the MAPI session.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fa7f1-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa7f1-114">See also</span></span>

- [<span data-ttu-id="fa7f1-115">IOlkAccountHelper::HandsOffSession</span><span class="sxs-lookup"><span data-stu-id="fa7f1-115">IOlkAccountHelper::HandsOffSession</span></span>](iolkaccounthelper-handsoffsession.md)
- [<span data-ttu-id="fa7f1-116">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fa7f1-116">IMAPISession : IUnknown</span></span>](https://msdn.microsoft.com/library/5650fa2a-6e62-451c-964e-363f7bee2344%28Office.15%29.aspx)

