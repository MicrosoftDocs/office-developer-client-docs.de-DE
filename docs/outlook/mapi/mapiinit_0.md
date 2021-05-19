---
title: MAPIINIT_0
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIINIT_0
api_type:
- COM
ms.assetid: 70739711-ff43-407d-bc8b-6baf7a476fef
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: de31fe7d472b143ed8f3c108dca84a019b5ce103
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357295"
---
# <a name="mapiinit_0"></a><span data-ttu-id="be082-103">MAPIINIT_0</span><span class="sxs-lookup"><span data-stu-id="be082-103">MAPIINIT_0</span></span>

  
  
<span data-ttu-id="be082-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be082-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be082-105">Übermittelt Optionen an die [MAPIInitialize-Funktion.](mapiinitialize.md)</span><span class="sxs-lookup"><span data-stu-id="be082-105">Conveys options to the [MAPIInitialize](mapiinitialize.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="be082-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="be082-106">Header file:</span></span>  <br/> |<span data-ttu-id="be082-107">MAPIX. H</span><span class="sxs-lookup"><span data-stu-id="be082-107">MAPIX.H</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG ulVersion;
  ULONG ulFlags;
} MAPIINIT_0, FAR *LPMAPIINIT_0;

```

## <a name="members"></a><span data-ttu-id="be082-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="be082-108">Members</span></span>

 <span data-ttu-id="be082-109">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="be082-109">**ulVersion**</span></span>
  
> <span data-ttu-id="be082-110">Ein ganzzahliger Wert, der die Versionsnummer der MAPIINIT_0 **darstellt.**</span><span class="sxs-lookup"><span data-stu-id="be082-110">An integer value that represents the version number of the **MAPIINIT_0** structure.</span></span> <span data-ttu-id="be082-111">Das **ulVersion-Element** ist für die zukünftige Erweiterung und stellt nicht die Version der MAPI-Schnittstelle dar.</span><span class="sxs-lookup"><span data-stu-id="be082-111">The **ulVersion** member is for future expansion and does not represent the version of the MAPI interface.</span></span> <span data-ttu-id="be082-112">Derzeit muss **ulVersion** auf "MAPI_INIT_VERSION.</span><span class="sxs-lookup"><span data-stu-id="be082-112">Currently, **ulVersion** must be set to MAPI_INIT_VERSION.</span></span> 
    
 <span data-ttu-id="be082-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="be082-113">**ulFlags**</span></span>
  
> <span data-ttu-id="be082-114">Die Bitmaske von Flags, die zum Steuern der Initialisierung der MAPI-Sitzung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="be082-114">The bitmask of flags used to control the initialization of the MAPI session.</span></span> <span data-ttu-id="be082-115">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="be082-115">The following flags can be set:</span></span>
    
<span data-ttu-id="be082-116">MAPI_MULTITHREAD_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="be082-116">MAPI_MULTITHREAD_NOTIFICATIONS</span></span> 
  
> <span data-ttu-id="be082-117">MAPI sollte Benachrichtigungen mithilfe eines Threads generieren, der für die Benachrichtigungsverarbeitung und nicht für den ersten Thread zum Aufrufen von **MAPIInitialize verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="be082-117">MAPI should generate notifications using a thread dedicated to notification handling instead of the first thread used to call **MAPIInitialize**.</span></span>
    
<span data-ttu-id="be082-118">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="be082-118">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="be082-119">Der Anrufer wird als Dienst Windows ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="be082-119">The caller is running as a Windows service.</span></span> <span data-ttu-id="be082-120">Anrufer, die nicht als Dienst Windows, sollten dieses Flag nicht festlegen. Anrufer, die als Dienst ausgeführt werden, müssen dieses Flag festlegen.</span><span class="sxs-lookup"><span data-stu-id="be082-120">Callers that are not running as a Windows service should not set this flag; callers that are running as a service must set this flag.</span></span>
    
<span data-ttu-id="be082-121">MAPI_NO_COINIT</span><span class="sxs-lookup"><span data-stu-id="be082-121">MAPI_NO_COINIT</span></span>
  
> <span data-ttu-id="be082-122">Legen Sie MAPI_NO_COINT-Flag fest, damit **MAPIInitialize** nicht versucht, COM mit einem Aufruf von [CoInitialize zu initialisieren.](https://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="be082-122">Set the MAPI_NO_COINT flag so that **MAPIInitialize** does not try to initialize COM with a call to [CoInitialize](https://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx).</span></span> <span data-ttu-id="be082-123">Wenn eine **MAPIINIT_0** an **MAPIInitialize** übergeben wird und _ulFlags_ auf MAPI_NO_COINIT festgelegt ist, geht MAPI davon aus, dass COM bereits initialisiert wurde und den Aufruf von **CoInitialize umgangen wird.**</span><span class="sxs-lookup"><span data-stu-id="be082-123">If a **MAPIINIT_0** structure is passed into **MAPIInitialize** with  _ulFlags_ set to MAPI_NO_COINIT, MAPI will assume that COM has already been initialized and will bypass the call to **CoInitialize**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="be082-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="be082-124">Remarks</span></span>

<span data-ttu-id="be082-125">Multithreadclients sollten das MAPI_MULTITHREAD_NOTIFICATIONS festlegen.</span><span class="sxs-lookup"><span data-stu-id="be082-125">Multithreaded clients should set the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> <span data-ttu-id="be082-126">Wenn das Flag nicht festgelegt ist, werden Benachrichtigungen für den Thread generiert, der zum ersten Aufruf von **MAPIInitialize verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="be082-126">If the flag is not set, notifications are generated on the thread used to make the first call to **MAPIInitialize**.</span></span> 
  
<span data-ttu-id="be082-127">Weitere Informationen zum Festlegen dieses Kennzeichens und zum Implementieren der Threadsicherheit in einem Client finden Sie unter [Threading in MAPI](threading-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="be082-127">For more information about when to set this flag and how to implement thread safety in a client, see [Threading in MAPI](threading-in-mapi.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="be082-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be082-128">See also</span></span>



[<span data-ttu-id="be082-129">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="be082-129">MAPIInitialize</span></span>](mapiinitialize.md)


[<span data-ttu-id="be082-130">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="be082-130">MAPI Structures</span></span>](mapi-structures.md)

