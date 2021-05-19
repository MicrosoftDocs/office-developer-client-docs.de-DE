---
title: HrGetAutoDiscoverXML
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrGetAutoDiscoverXML
api_type:
- COM
ms.assetid: 03691187-7c65-620b-576f-6ebe62a80830
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 77f28654ffe0f6f459fde229bb7428f2c39e96c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347803"
---
# <a name="hrgetautodiscoverxml"></a><span data-ttu-id="2a412-103">HrGetAutoDiscoverXML</span><span class="sxs-lookup"><span data-stu-id="2a412-103">HrGetAutoDiscoverXML</span></span>

  
  
<span data-ttu-id="2a412-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a412-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a412-105">Gibt einen XML-Stream (Extensible Markup Language) zurück, der Informationen darstellt, die aus dem AutoErmittlungsdienst eines Microsoft Exchange 2007-Servers abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="2a412-105">Returns an Extensible Markup Language (XML) stream that represents information retrieved from the auto-discovery service of a Microsoft Exchange 2007 server.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2a412-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="2a412-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2a412-107">Exportiert von:</span><span class="sxs-lookup"><span data-stu-id="2a412-107">Exported by:</span></span>  <br/> |<span data-ttu-id="2a412-108">olmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="2a412-108">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="2a412-109">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="2a412-109">Called by:</span></span>  <br/> |<span data-ttu-id="2a412-110">Client</span><span class="sxs-lookup"><span data-stu-id="2a412-110">Client</span></span>  <br/> |
|<span data-ttu-id="2a412-111">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="2a412-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="2a412-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="2a412-112">Outlook</span></span>  <br/> |
   
```cpp
HRESULT HrGetAutoDiscoverXML( 
    __in_z const WCHAR *pwzAddress, 
    __in_opt_z const WCHAR *pwzPassword, 
    __in_opt HANDLE hCancelEvent, 
    __in_opt ULONG ulFlags, 
    __out IStream** ppXmlStream); 

```

## <a name="parameters"></a><span data-ttu-id="2a412-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="2a412-113">Parameters</span></span>

 <span data-ttu-id="2a412-114">_pwzAddress_</span><span class="sxs-lookup"><span data-stu-id="2a412-114">_pwzAddress_</span></span>
  
> <span data-ttu-id="2a412-115">[in] Eine SMTP-E-Mail-Adresse (Simple Mail Transfer Protocol, Simple Mail Transfer Protocol) des Kontos, für das Sie die Informationen zur automatischen Ermittlung abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="2a412-115">[in] A null-terminated Simple Mail Transfer Protocol (SMTP) email address of the account for which you want to retrieve the auto-discovery information.</span></span>
    
 <span data-ttu-id="2a412-116">_pwzPassword_</span><span class="sxs-lookup"><span data-stu-id="2a412-116">_pwzPassword_</span></span>
  
> <span data-ttu-id="2a412-117">[in] Ein optionales Kennwort für das von _pwzAddress angegebene Konto._</span><span class="sxs-lookup"><span data-stu-id="2a412-117">[in] An optional password for the account specified by  _pwzAddress_.</span></span> <span data-ttu-id="2a412-118">Beachten Sie, dass das Übergeben eines Kennworts keine Auswirkung hat, wenn für das von  _pwzAddress_ angegebene Konto kein Kennwort erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="2a412-118">Note that passing any password has no effect if the account specified by  _pwzAddress_ does not require a password.</span></span> 
    
 <span data-ttu-id="2a412-119">_hCancelEvent_</span><span class="sxs-lookup"><span data-stu-id="2a412-119">_hCancelEvent_</span></span>
  
> <span data-ttu-id="2a412-120">[in] Ein nicht verwendetes Win32-Ereignishandle, das optional ist und zum Abbrechen des Vorgangs verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2a412-120">[in] An unset Win32 event handle that is optional and can be used to cancel the operation.</span></span> <span data-ttu-id="2a412-121">Zum Abbrechen des Vorgangs legen Sie das Ereignis fest, und übergeben Sie das Ereignishandle als  _hCancelEvent_; übergeben **Sie null,** wenn Sie den Vorgang nicht abbrechen möchten.</span><span class="sxs-lookup"><span data-stu-id="2a412-121">To cancel the operation, set the event and pass the event handle as  _hCancelEvent_; pass **null** if you do not want to cancel the operation.</span></span> <span data-ttu-id="2a412-122">Beachten Sie, dass das Übergeben eines Werts, der kein Ereignishandle repräsentiert, keine Auswirkung hat und von der Funktion ignoriert wird.</span><span class="sxs-lookup"><span data-stu-id="2a412-122">Note that passing a value that does not represent an event handle has no effect and is ignored by the function.</span></span> 
    
 <span data-ttu-id="2a412-123">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2a412-123">_ulFlags_</span></span>
  
> <span data-ttu-id="2a412-124">[in] Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2a412-124">[in] This parameter is not used.</span></span> <span data-ttu-id="2a412-125">Es muss 0 sein.</span><span class="sxs-lookup"><span data-stu-id="2a412-125">It must be 0.</span></span>
    
 <span data-ttu-id="2a412-126">_ppXmlStream_</span><span class="sxs-lookup"><span data-stu-id="2a412-126">_ppXmlStream_</span></span>
  
> <span data-ttu-id="2a412-127">[out] Ein Zeiger auf ein [IStream-Objekt,](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) das die AutoErmittlungs-XML enthält.</span><span class="sxs-lookup"><span data-stu-id="2a412-127">[out] A pointer to an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object that contains the autodiscovery XML.</span></span> <span data-ttu-id="2a412-128">Gibt **null zurück,** wenn der AutoErmittlungsvorgang fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="2a412-128">Returns **null** if the autodiscovery operation fails.</span></span> <span data-ttu-id="2a412-129">Sie müssen das [IStream-Objekt](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) los, wenn Sie damit fertig sind.</span><span class="sxs-lookup"><span data-stu-id="2a412-129">You must release the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object when you are finished with it.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="2a412-130">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="2a412-130">Return values</span></span>

<span data-ttu-id="2a412-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="2a412-131">S_OK</span></span> 
  
- <span data-ttu-id="2a412-132">Der Funktionsaufruf ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="2a412-132">The function call is successful.</span></span>
    
<span data-ttu-id="2a412-133">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="2a412-133">E_INVALIDARG</span></span> 
  
-  <span data-ttu-id="2a412-134">_pwzAddress_ ist **null** oder ist keine gültige SMTP-Adresse, oder _ppXmlStream_ ist ein **Nullzeiger** auf ein [IStream-Objekt.](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a412-134">_pwzAddress_ is **null** or is not a valid SMTP address, or  _ppXmlStream_ is a **null** pointer to an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object.</span></span> 
    
<span data-ttu-id="2a412-135">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="2a412-135">MAPI_E_NOT_FOUND</span></span> 
  
- <span data-ttu-id="2a412-136">Der Clientcomputer ist nicht mit dem Netzwerk verbunden, der Clientcomputer ist nicht mit einem Microsoft Exchange 2007-Server verbunden, _pwzAddress_ ist kein Konto auf einem Exchange 2007-Server, oder _pwzAddress_ ist ein Konto, das Exchange auto-discovery service nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2a412-136">Client computer is not connected to the network, client computer is not connected to a Microsoft Exchange 2007 server,  _pwzAddress_ is not an account on an Exchange 2007 server, or  _pwzAddress_ is an account that does not support Exchange auto-discovery service.</span></span> 
    
<span data-ttu-id="2a412-137">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="2a412-137">MAPI_E_USER_CANCEL</span></span> 
  
- <span data-ttu-id="2a412-138">Ein Ereignishandle wurde an  _hCancelEvent übergeben,_ um den Vorgang abbricht.</span><span class="sxs-lookup"><span data-stu-id="2a412-138">An event handle has been passed to  _hCancelEvent_ to cancel the operation.</span></span> 
    
<span data-ttu-id="2a412-139">STRSAFE_E_INSUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="2a412-139">STRSAFE_E_INSUFFICIENT_BUFFER</span></span>
  
- <span data-ttu-id="2a412-140">Der an  _pwzAddress_ oder  _pwzPassword_ übergebene Wert ist zu lang, so dass er den internen Puffer der Größe 256 Byte überschreitet.</span><span class="sxs-lookup"><span data-stu-id="2a412-140">The value passed to  _pwzAddress_ or  _pwzPassword_ is too long, such that it overflows the internal buffer of size 256 bytes.</span></span> 
    

