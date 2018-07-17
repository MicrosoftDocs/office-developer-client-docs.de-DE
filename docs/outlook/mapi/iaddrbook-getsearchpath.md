---
title: IAddrBookGetSearchPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetSearchPath
api_type:
- COM
ms.assetid: 43b51a66-71fa-4e10-93e4-d533b48af4de
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c20cd7f82df2fb7f878db177fdc940022e1da351
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792005"
---
# <a name="iaddrbookgetsearchpath"></a><span data-ttu-id="c0881-103">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="c0881-103">IAddrBook::GetSearchPath</span></span>

  
  
<span data-ttu-id="c0881-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c0881-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c0881-105">Gibt eine geordnete Liste von Eintrags-IDs der Container in der [IAddrBook::ResolveName](iaddrbook-resolvename.md) -Methode initiiert Vorgang der Lösung enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="c0881-105">Returns an ordered list of entry identifiers of the containers to be included in the name resolution process initiated by the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> 
  
```cpp
HRESULT GetSearchPath(
  ULONG ulFlags,
  LPSRowSet FAR * lppSearchPath
);
```

## <a name="parameters"></a><span data-ttu-id="c0881-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0881-106">Parameters</span></span>

 <span data-ttu-id="c0881-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c0881-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c0881-108">[in] Eine Bitmaske aus Flags, die den Typ der Zeichenfolgen steuert, die in den Suchpfad zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c0881-108">[in] A bitmask of flags that controls the type of the strings returned in the search path.</span></span> <span data-ttu-id="c0881-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="c0881-109">The following flag can be set:</span></span>
    
<span data-ttu-id="c0881-110">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c0881-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c0881-111">Die zurückgegebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="c0881-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="c0881-112">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="c0881-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="c0881-113">_lppSearchPath_</span><span class="sxs-lookup"><span data-stu-id="c0881-113">_lppSearchPath_</span></span>
  
> <span data-ttu-id="c0881-114">[out] Ein Zeiger auf einen Zeiger auf eine sortierte Liste der Container-Eintragsbezeichner.</span><span class="sxs-lookup"><span data-stu-id="c0881-114">[out] A pointer to a pointer to an ordered list of container entry identifiers.</span></span> <span data-ttu-id="c0881-115">**GetSearchPath** speichert die sortierte Liste in eine [SRowSet](srowset.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="c0881-115">**GetSearchPath** stores the ordered list in an [SRowSet](srowset.md) structure.</span></span> <span data-ttu-id="c0881-116">Wenn keine Container in der Adressbuchhierarchie vorhanden sind, wird 0 (null) in der Struktur **SRowSet** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c0881-116">If there are no containers in the address book hierarchy, zero is returned in the **SRowSet** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c0881-117">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="c0881-117">Return value</span></span>

<span data-ttu-id="c0881-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="c0881-118">S_OK</span></span> 
  
> <span data-ttu-id="c0881-119">Der Suchpfad wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c0881-119">The search path was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c0881-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c0881-120">Remarks</span></span>

<span data-ttu-id="c0881-121">Clients und Dienstanbieter rufen Sie die **GetSearchPath-** Methode, um den Suchpfad abzurufen, der zum Auflösen von Namen mit der **ResolveName** -Methode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c0881-121">Clients and service providers call the **GetSearchPath** method to get the search path that is used to resolve names with the **ResolveName** method.</span></span> <span data-ttu-id="c0881-122">In der Regel rufen Clients die [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) -Methode, um einen Container Suchpfad im Profil herzustellen, vor dem Aufruf von **GetSearchPath** , um sie abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c0881-122">Typically, clients call the [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) method to establish a container search path in the profile before they call **GetSearchPath** to retrieve it.</span></span> <span data-ttu-id="c0881-123">Aufrufen von **SetSearchPath** ist jedoch optional.</span><span class="sxs-lookup"><span data-stu-id="c0881-123">However, calling **SetSearchPath** is optional.</span></span> 
  
<span data-ttu-id="c0881-124">Wenn **SetSearchPath** noch nie aufgerufen wurde, werden erstellt **GetSearchPath** einen Pfad durcharbeiten die Adresse des Buchs Hierarchietabellen.</span><span class="sxs-lookup"><span data-stu-id="c0881-124">If **SetSearchPath** has never been called, **GetSearchPath** builds a path by working through the address book's hierarchy tables.</span></span> <span data-ttu-id="c0881-125">Der Standardsuchpfad **GetSearchPath** eingesetzten umfasst die folgenden Container in der folgenden Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="c0881-125">The default search path established by **GetSearchPath** consists of the following containers in the following order:</span></span> 
  
1. <span data-ttu-id="c0881-126">Der erste Container mit Lese-/Schreibzugriff, normalerweise über das persönliche Adressbuch (PAB).</span><span class="sxs-lookup"><span data-stu-id="c0881-126">The first container with read/write permission, usually the personal address book (PAB).</span></span>
    
2. <span data-ttu-id="c0881-127">Jedes Container, dessen **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))-Eigenschaft auf DT_GLOBAL festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c0881-127">Every container that has its **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) property set to DT_GLOBAL.</span></span> <span data-ttu-id="c0881-128">Diese Einstellung gibt an, dass der Container Empfänger enthält.</span><span class="sxs-lookup"><span data-stu-id="c0881-128">This setting indicates that the container holds recipients.</span></span> 
    
3. <span data-ttu-id="c0881-129">Der Container als Standard, festgelegt werden, wenn es sind keine Container, die die in ihrer **PR_DISPLAY_TYPE** -Eigenschaft und der Standardcontainer DT_GLOBAL gekennzeichnet sind unterscheidet sich von den ersten Container mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="c0881-129">The container designated as the default, if there are no containers that have the DT_GLOBAL flag set in their **PR_DISPLAY_TYPE** property and the default container differs from the first container with read/write permission.</span></span> 
    
<span data-ttu-id="c0881-130">Wenn **SetSearchPath** aufgerufen wurde, erstellt **GetSearchPath** einen Pfad mit Address Book Container, die im Profil gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="c0881-130">If **SetSearchPath** has been called, **GetSearchPath** builds a path by using the address book containers that have been stored in the profile.</span></span> <span data-ttu-id="c0881-131">**GetSearchPath** überprüft dieser Pfad, bevor sie ihn an den Aufrufer zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="c0881-131">**GetSearchPath** validates this path before it returns it to the caller.</span></span> 
  
<span data-ttu-id="c0881-132">Nach dem ersten Aufruf von **SetSearchPath**müssen nachfolgende Aufrufe von **SetSearchPath** so ändern Sie den zurückgegebene **GetSearchPath**Suchpfad verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c0881-132">After the first call to **SetSearchPath**, subsequent calls to **SetSearchPath** must be used to modify the search path returned by **GetSearchPath**.</span></span> <span data-ttu-id="c0881-133">Anders ausgedrückt, erhält die aufrufende Client oder Anbieter den Standardpfad für die Suche nach dem ersten Aufruf von **SetSearchPath**keine.</span><span class="sxs-lookup"><span data-stu-id="c0881-133">In other words, the calling client or provider does not receive the default search path after the first call to **SetSearchPath**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c0881-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0881-134">See also</span></span>



[<span data-ttu-id="c0881-135">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="c0881-135">IAddrBook::SetSearchPath</span></span>](iaddrbook-setsearchpath.md)
  
[<span data-ttu-id="c0881-136">' Srowset '</span><span class="sxs-lookup"><span data-stu-id="c0881-136">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="c0881-137">IAddrBook: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c0881-137">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
