---
title: IFolderSupport IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IFolderSupport
api_type:
- COM
ms.assetid: a4b03a66-cf6d-cd20-f1df-b247d3ee87aa
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a4a1c78e65d9a515b2b42d7e0a2bc3a8b4bd8869
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792089"
---
# <a name="ifoldersupport--iunknown"></a><span data-ttu-id="39932-103">IFolderSupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="39932-103">IFolderSupport : IUnknown</span></span>

  
  
<span data-ttu-id="39932-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="39932-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="39932-105">Enthält Informationen zur Unterstützung für einen Ordner für die Freigabe.</span><span class="sxs-lookup"><span data-stu-id="39932-105">Provides information about a folder's support for sharing.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="39932-106">Bereitgestellt von:</span><span class="sxs-lookup"><span data-stu-id="39932-106">Provided by:</span></span>  <br/> |<span data-ttu-id="39932-107">Nachricht Speicheranbieter</span><span class="sxs-lookup"><span data-stu-id="39932-107">Message store provider</span></span>  <br/> |
|<span data-ttu-id="39932-108">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="39932-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="39932-109">IID_IFolderSupport</span><span class="sxs-lookup"><span data-stu-id="39932-109">IID_IFolderSupport</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="39932-110">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="39932-110">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="39932-111">**[GetSupportMask](ifoldersupport-getsupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="39932-111">**[GetSupportMask](ifoldersupport-getsupportmask.md)**</span></span> <br/> |<span data-ttu-id="39932-112">Ruft Informationen über die Unterstützung für einen Ordner für die Freigabe.</span><span class="sxs-lookup"><span data-stu-id="39932-112">Gets information about a folder's support for sharing.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="39932-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="39932-113">Remarks</span></span>

<span data-ttu-id="39932-114">Im Allgemeinen erfordert Microsoft Office Outlook MAPI-Speicheranbieter diese Schnittstelle implementieren, wenn der Anbieter einen Ordner freigeben möchte.</span><span class="sxs-lookup"><span data-stu-id="39932-114">Generally, Microsoft Office Outlook requires a MAPI store provider to implement this interface if the provider wants to share a folder.</span></span> <span data-ttu-id="39932-115">Die Ausnahme ist der Exchange-Server-Speicher-Anbieter, der Ordner freigeben kann, ohne dass diese Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="39932-115">The exception is the Exchange Server store provider, which can share folders without implementing this interface.</span></span>
  
<span data-ttu-id="39932-116">Ein Client kann ein **[IMAPIFolder](imapifolderimapicontainer.md)** **IFolderSupport**Abfragen.</span><span class="sxs-lookup"><span data-stu-id="39932-116">A client can query an **[IMAPIFolder](imapifolderimapicontainer.md)** for **IFolderSupport**.</span></span> <span data-ttu-id="39932-117">Wenn dies erfolgreich ist, rufen Sie **IFolderSupport::GetSupportMask** , und prüfen Sie, ob das Bit **FS_SUPPORTS_SHARING** festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="39932-117">If that succeeds, call **IFolderSupport::GetSupportMask** and check for the **FS_SUPPORTS_SHARING** bit to be set.</span></span> 
  
