---
title: IProxyStoreObject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProxyStoreObject
api_type:
- COM
ms.assetid: 567bede4-39a3-bfb4-af85-ba678e2cf4a5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 485d3f3cd4b6be4748a2ebf2ba0d0b71f691478f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315519"
---
# <a name="iproxystoreobject"></a><span data-ttu-id="140c0-103">IProxyStoreObject</span><span class="sxs-lookup"><span data-stu-id="140c0-103">IProxyStoreObject</span></span>

  
  
<span data-ttu-id="140c0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="140c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="140c0-105">Stellt ein ImAP-Speicherobjekt (Internet Message Access Protocol) bereit, das entpackt wurde und den Zugriff auf Elemente in der Pst -Datei (Personal Folders) ermöglicht, ohne die Synchronisierung aufrufen und die Elemente herunterladen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="140c0-105">Provides an Internet Message Access Protocol (IMAP) store object that has been unwrapped and that allows access to items in the Personal Folders file (PST) without invoking synchronization and downloading the items.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="140c0-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="140c0-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="140c0-107">Geerbt von:</span><span class="sxs-lookup"><span data-stu-id="140c0-107">Inherited from:</span></span>  <br/> |[<span data-ttu-id="140c0-108">IUnknown</span><span class="sxs-lookup"><span data-stu-id="140c0-108">IUnknown</span></span>](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) <br/> |
|<span data-ttu-id="140c0-109">Bereitgestellt von:</span><span class="sxs-lookup"><span data-stu-id="140c0-109">Provided By:</span></span>  <br/> |<span data-ttu-id="140c0-110">Anbieter des Nachrichtenspeichers</span><span class="sxs-lookup"><span data-stu-id="140c0-110">Message store provider</span></span>  <br/> |
|<span data-ttu-id="140c0-111">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="140c0-111">Interface identifier:</span></span>  <br/> |<span data-ttu-id="140c0-112">**IID_IProxyStoreObject**</span><span class="sxs-lookup"><span data-stu-id="140c0-112">**IID_IProxyStoreObject**</span></span> <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="140c0-113">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="140c0-113">Vtable order</span></span>

|||
|:-----|:-----|
| <span data-ttu-id="140c0-114">*Platzhaltermitglied*</span><span class="sxs-lookup"><span data-stu-id="140c0-114">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="140c0-115">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="140c0-115">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="140c0-116">IProxyStoreObject::UnwrapNoRef</span><span class="sxs-lookup"><span data-stu-id="140c0-116">IProxyStoreObject::UnwrapNoRef</span></span>](iproxystoreobject-unwrapnoref.md) <br/> |<span data-ttu-id="140c0-117">Ruft einen Zeiger auf einen nicht ausgepackten IMAP-Speicher ab.</span><span class="sxs-lookup"><span data-stu-id="140c0-117">Gets a pointer to an unwrapped IMAP store.</span></span>  <br/> |
| <span data-ttu-id="140c0-118">*Platzhaltermitglied*</span><span class="sxs-lookup"><span data-stu-id="140c0-118">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="140c0-119">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="140c0-119">*Not supported or documented.*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="140c0-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="140c0-120">Remarks</span></span>

<span data-ttu-id="140c0-121">Rufen [Sie IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) im Quellnachrichtenspeicher auf, um die **IProxyStoreObject-Schnittstelle abzurufen.**</span><span class="sxs-lookup"><span data-stu-id="140c0-121">Call [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) on the source message store to obtain the **IProxyStoreObject** interface.</span></span> <span data-ttu-id="140c0-122">Rufen Sie **dann IProxyStoreObject::UnwrapNoRef auf,** um das entpackte Speicherobjekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="140c0-122">Then call **IProxyStoreObject::UnwrapNoRef** to obtain the unwrapped store object.</span></span> <span data-ttu-id="140c0-123">Wenn **QueryInterface** den Fehler **MAPI_E_INTERFACE_NOT_SUPPORTED** zurückgibt, wurde der Speicher nicht umschlossen.</span><span class="sxs-lookup"><span data-stu-id="140c0-123">If **QueryInterface** returns the error **MAPI_E_INTERFACE_NOT_SUPPORTED**, then the store has not been wrapped.</span></span> 
  
<span data-ttu-id="140c0-124">Da **UnwrapNoRef** die Referenzanzahl für diesen neuen Zeiger nicht auf das nicht mehr ausgepackte Speicherobjekt erhöht, sollten Sie nach dem erfolgreichen Aufruf von **UnwrapNoRef** [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) aufrufen, um die Referenzanzahl zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="140c0-124">Because **UnwrapNoRef** does not increment the reference count for this new pointer to the unwrapped store object, after successfully calling **UnwrapNoRef**, you should call [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) to maintain the reference count.</span></span> 
  

