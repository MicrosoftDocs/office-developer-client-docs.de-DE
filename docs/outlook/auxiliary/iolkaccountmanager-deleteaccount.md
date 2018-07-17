---
title: IOlkAccountManagerDeleteAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: df210364-fe20-8e33-a455-9902f04ec739
description: Löscht das angegebene Konto.
ms.openlocfilehash: 1c0b246af10dac1af9c61f368d082a92c7b3616a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791093"
---
# <a name="iolkaccountmanagerdeleteaccount"></a><span data-ttu-id="dc906-103">IOlkAccountManager::DeleteAccount</span><span class="sxs-lookup"><span data-stu-id="dc906-103">IOlkAccountManager::DeleteAccount</span></span>

<span data-ttu-id="dc906-104">Löscht das angegebene Konto.</span><span class="sxs-lookup"><span data-stu-id="dc906-104">Deletes the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="dc906-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="dc906-105">Quick info</span></span>

<span data-ttu-id="dc906-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="dc906-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::DeleteAccount (  
    DWORD dwAcctID, 
);
```

## <a name="parameters"></a><span data-ttu-id="dc906-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc906-107">Parameters</span></span>

<span data-ttu-id="dc906-108">_dwAcctID_</span><span class="sxs-lookup"><span data-stu-id="dc906-108">_dwAcctID_</span></span>
  
> <span data-ttu-id="dc906-109">[in] Die Konto-ID des Kontos gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="dc906-109">[in] The account ID of the account to be deleted.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="dc906-110">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="dc906-110">Return values</span></span>

|<span data-ttu-id="dc906-111">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="dc906-111">**HRESULT**</span></span>|<span data-ttu-id="dc906-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dc906-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dc906-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="dc906-113">S_OK</span></span>  <br/> |<span data-ttu-id="dc906-114">Der Aufruf war erfolgreich</span><span class="sxs-lookup"><span data-stu-id="dc906-114">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="dc906-115">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="dc906-115">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="dc906-116">Das angegebene Konto kann nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="dc906-116">The specified account cannot be found.</span></span>  <br/> |
|<span data-ttu-id="dc906-117">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="dc906-117">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="dc906-118">Konto-Manager wurde nicht für die Verwendung initialisiert.</span><span class="sxs-lookup"><span data-stu-id="dc906-118">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dc906-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc906-119">See also</span></span>

- [<span data-ttu-id="dc906-120">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="dc906-120">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="dc906-121">IOlkAccountManager::FindAccount</span><span class="sxs-lookup"><span data-stu-id="dc906-121">IOlkAccountManager::FindAccount</span></span>](iolkaccountmanager-findaccount.md)
