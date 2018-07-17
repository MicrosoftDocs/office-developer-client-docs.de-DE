---
title: IMAPIViewContext IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext
api_type:
- COM
ms.assetid: d566ff39-92c1-4a14-85e5-1c406825f805
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a7d62253baaaae7955e722874a15d05ed16e566e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792504"
---
# <a name="imapiviewcontext--iunknown"></a><span data-ttu-id="554b6-103">IMAPIViewContext: IUnknown</span><span class="sxs-lookup"><span data-stu-id="554b6-103">IMAPIViewContext : IUnknown</span></span>

  
  
<span data-ttu-id="554b6-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="554b6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="554b6-105">Ein Formular in einer Clientanwendung Formular Viewer verwaltet.</span><span class="sxs-lookup"><span data-stu-id="554b6-105">Manages a form in a client application's form viewer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="554b6-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="554b6-106">Header file:</span></span>  <br/> |<span data-ttu-id="554b6-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="554b6-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="554b6-108">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="554b6-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="554b6-109">Kontext-Objekte anzeigen</span><span class="sxs-lookup"><span data-stu-id="554b6-109">View context objects</span></span>  <br/> |
|<span data-ttu-id="554b6-110">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="554b6-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="554b6-111">Formular-Viewer</span><span class="sxs-lookup"><span data-stu-id="554b6-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="554b6-112">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="554b6-112">Called by:</span></span>  <br/> |<span data-ttu-id="554b6-113">Formular-Objekte</span><span class="sxs-lookup"><span data-stu-id="554b6-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="554b6-114">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="554b6-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="554b6-115">IID_IMAPIViewContext</span><span class="sxs-lookup"><span data-stu-id="554b6-115">IID_IMAPIViewContext</span></span>  <br/> |
|<span data-ttu-id="554b6-116">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="554b6-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="554b6-117">LPMAPIVIEWCONTEXT</span><span class="sxs-lookup"><span data-stu-id="554b6-117">LPMAPIVIEWCONTEXT</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="554b6-118">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="554b6-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="554b6-119">SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="554b6-119">SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md) <br/> |<span data-ttu-id="554b6-120">Verwaltet ein Formular Registrierung Erhalt von Benachrichtigungen zu Änderungen im Viewer.</span><span class="sxs-lookup"><span data-stu-id="554b6-120">Manages a form's registration to receive notifications about changes in the viewer.</span></span>  <br/> |
|[<span data-ttu-id="554b6-121">ActivateNext</span><span class="sxs-lookup"><span data-stu-id="554b6-121">ActivateNext</span></span>](imapiviewcontext-activatenext.md) <br/> |<span data-ttu-id="554b6-122">Die nächste oder vorherige Nachricht im Formular-Viewer aktiviert.</span><span class="sxs-lookup"><span data-stu-id="554b6-122">Activates the next or previous message in the form viewer.</span></span>  <br/> |
|[<span data-ttu-id="554b6-123">GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="554b6-123">GetPrintSetup</span></span>](imapiviewcontext-getprintsetup.md) <br/> |<span data-ttu-id="554b6-124">Ruft die aktuellen Drucken von Informationen.</span><span class="sxs-lookup"><span data-stu-id="554b6-124">Retrieves current printing information.</span></span>  <br/> |
|[<span data-ttu-id="554b6-125">GetSaveStream</span><span class="sxs-lookup"><span data-stu-id="554b6-125">GetSaveStream</span></span>](imapiviewcontext-getsavestream.md) <br/> |<span data-ttu-id="554b6-126">Ruft einen Datenstrom zum Speichern der aktuellen Nachricht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="554b6-126">Retrieves a stream to be used for saving the current message.</span></span>  <br/> |
|[<span data-ttu-id="554b6-127">GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="554b6-127">GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md) <br/> |<span data-ttu-id="554b6-128">Ruft den aktuellen Status der Viewer ab.</span><span class="sxs-lookup"><span data-stu-id="554b6-128">Retrieves the current viewer status.</span></span>  <br/> |
|[<span data-ttu-id="554b6-129">GetLastError</span><span class="sxs-lookup"><span data-stu-id="554b6-129">GetLastError</span></span>](imapiviewcontext-getlasterror.md) <br/> |<span data-ttu-id="554b6-130">Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über den vorherigen Fehler auftritt, in der Ansicht Context-Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="554b6-130">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring in the view context object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="554b6-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="554b6-131">See also</span></span>



[<span data-ttu-id="554b6-132">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="554b6-132">MAPI Interfaces</span></span>](mapi-interfaces.md)
