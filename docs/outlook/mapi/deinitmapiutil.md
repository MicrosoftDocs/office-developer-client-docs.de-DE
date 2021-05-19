---
title: DeinitMapiUtil
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeinitMapiUtil
api_type:
- HeaderDef
ms.assetid: e0b8dc9c-cc46-4d27-9497-7a55a0bfdff5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a9654efc34280941cdbc727bce9912a0a39d0fb9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427346"
---
# <a name="deinitmapiutil"></a><span data-ttu-id="6236c-103">DeinitMapiUtil</span><span class="sxs-lookup"><span data-stu-id="6236c-103">DeinitMapiUtil</span></span>

  
  
<span data-ttu-id="6236c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6236c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6236c-105">Gibt Hilfsfunktionen frei, die explizit von der [ScInitMapiUtil-Funktion](scinitmapiutil.md) oder implizit von der [MAPIInitialize-Funktion aufgerufen](mapiinitialize.md) werden.</span><span class="sxs-lookup"><span data-stu-id="6236c-105">Releases utility functions called explicitly by the [ScInitMapiUtil](scinitmapiutil.md) function or implicitly by the [MAPIInitialize](mapiinitialize.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6236c-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="6236c-106">Header file:</span></span>  <br/> |<span data-ttu-id="6236c-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="6236c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="6236c-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="6236c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6236c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6236c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6236c-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="6236c-110">Called by:</span></span>  <br/> |<span data-ttu-id="6236c-111">Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="6236c-111">Client applications</span></span>  <br/> |
   
```cpp
VOID DeinitMapiUtil( void );
```

## <a name="parameters"></a><span data-ttu-id="6236c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6236c-112">Parameters</span></span>

<span data-ttu-id="6236c-113">Keine</span><span class="sxs-lookup"><span data-stu-id="6236c-113">None</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="6236c-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6236c-114">Return value</span></span>

<span data-ttu-id="6236c-115">Keine</span><span class="sxs-lookup"><span data-stu-id="6236c-115">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6236c-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6236c-116">Remarks</span></span>

<span data-ttu-id="6236c-117">Die **Funktionen der DeinitMapiUtil-Funktionsfreigabe** werden mit [ScInitMapiUtil](scinitmapiutil.md) oder [MAPIInitialize initialisiert.](mapiinitialize.md)</span><span class="sxs-lookup"><span data-stu-id="6236c-117">The **DeinitMapiUtil** function release functions initialized with [ScInitMapiUtil](scinitmapiutil.md) or [MAPIInitialize](mapiinitialize.md).</span></span> 
  
<span data-ttu-id="6236c-118">Wenn die Verwendung der von **ScInitMapiUtil** aufgerufenen Funktionen abgeschlossen ist, muss **DeinitMapiUtil** explizit aufgerufen werden, um sie frei zu geben.</span><span class="sxs-lookup"><span data-stu-id="6236c-118">When use of the functions called by **ScInitMapiUtil** is complete, **DeinitMapiUtil** must be explicitly called to release them.</span></span> <span data-ttu-id="6236c-119">Im Gegensatz dazu ruft [MAPIUninitialize](mapiuninitialize.md) **implizit DeinitMapiUtil auf.**</span><span class="sxs-lookup"><span data-stu-id="6236c-119">In contrast, [MAPIUninitialize](mapiuninitialize.md) implicitly calls **DeinitMapiUtil**.</span></span> 
  

