---
title: IProfAdminGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.GetLastError
api_type:
- COM
ms.assetid: bb161d7b-ae5b-4f8e-a506-8346ac5e583d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b6964ecde3a78bd1e9ce0ae1dcab0342c5a21a03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430773"
---
# <a name="iprofadmingetlasterror"></a><span data-ttu-id="fba1b-103">IProfAdmin::GetLastError</span><span class="sxs-lookup"><span data-stu-id="fba1b-103">IProfAdmin::GetLastError</span></span>

  
  
<span data-ttu-id="fba1b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fba1b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fba1b-105">Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Fehler enthält, der für ein Profilverwaltungsobjekt aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="fba1b-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to a profile administration object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="fba1b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fba1b-106">Parameters</span></span>

 <span data-ttu-id="fba1b-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="fba1b-107">_hResult_</span></span>
  
> <span data-ttu-id="fba1b-108">[in] Ein HRESULT-Datentyp, der den im vorherigen Methodenaufruf generierten Fehlerwert enthält.</span><span class="sxs-lookup"><span data-stu-id="fba1b-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="fba1b-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fba1b-109">_ulFlags_</span></span>
  
> <span data-ttu-id="fba1b-110">[in] Eine Bitmaske mit Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="fba1b-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="fba1b-111">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="fba1b-111">The following flag can be set:</span></span>
    
<span data-ttu-id="fba1b-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fba1b-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="fba1b-113">Die Zeichenfolgen in der [MAPIERROR-Struktur,](mapierror.md) die im  _lppMAPIError-Parameter_ zurückgegeben wird, sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="fba1b-113">The strings in the [MAPIERROR](mapierror.md) structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="fba1b-114">Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="fba1b-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="fba1b-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="fba1b-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="fba1b-116">[out] Ein Zeiger auf einen Zeiger auf die **MAPIERROR-Struktur,** die Versions-, Komponenten- und Kontextinformationen für den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="fba1b-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="fba1b-117">Der  _Parameter lppMAPIError_ kann auf NULL festgelegt werden, wenn keine **MAPIERROR-Struktur** zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="fba1b-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fba1b-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fba1b-118">Return value</span></span>

<span data-ttu-id="fba1b-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="fba1b-119">S_OK</span></span> 
  
> <span data-ttu-id="fba1b-120">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="fba1b-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="fba1b-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="fba1b-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="fba1b-122">Entweder wurde MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="fba1b-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fba1b-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fba1b-123">Remarks</span></span>

<span data-ttu-id="fba1b-124">Die **IProfAdmin::GetLastError-Methode** ruft Informationen zum letzten Fehler ab, der von einem Methodenaufruf für das Profilverwaltungsobjekt zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="fba1b-124">The **IProfAdmin::GetLastError** method retrieves information about the last error returned from a method call for the profile administration object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="fba1b-125">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="fba1b-125">Notes to callers</span></span>

<span data-ttu-id="fba1b-126">Sie können die **MAPIERROR-Struktur** verwenden, wenn MAPI eine angibt, auf die der  _lppMAPIError-Parameter_ nur verweist, wenn **GetLastError** S_OK.</span><span class="sxs-lookup"><span data-stu-id="fba1b-126">You can use the **MAPIERROR** structure, if MAPI supplies one, pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="fba1b-127">Manchmal kann MAPI nicht ermitteln, was der letzte Fehler war oder hat nichts mehr über den Fehler zu melden.</span><span class="sxs-lookup"><span data-stu-id="fba1b-127">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="fba1b-128">In diesem Fall wird ein Zeiger auf NULL in _lppMAPIError zurückgegeben._</span><span class="sxs-lookup"><span data-stu-id="fba1b-128">In this situation, a pointer to NULL is returned in  _lppMAPIError_.</span></span> 
  
<span data-ttu-id="fba1b-129">Rufen Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) auf, um den von MAPI zugewiesenen Arbeitsspeicher für die **MAPIERROR-Struktur** frei zu geben.</span><span class="sxs-lookup"><span data-stu-id="fba1b-129">To release all the memory allocated by MAPI for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="fba1b-130">Weitere Informationen zur **GetLastError-Methode** finden Sie unter [Using Extended Errors](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="fba1b-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fba1b-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fba1b-131">See also</span></span>



[<span data-ttu-id="fba1b-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="fba1b-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="fba1b-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="fba1b-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="fba1b-134">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fba1b-134">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

