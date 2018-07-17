---
title: IMAPIPropCopyProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.CopyProps
api_type:
- COM
ms.assetid: f65da1c8-d49b-44e8-8c66-9c53d088d334
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ff8f13a1dcf678e1d05b6e8e083597156422b83d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792291"
---
# <a name="imapipropcopyprops"></a><span data-ttu-id="e684f-103">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="e684f-103">IMAPIProp::CopyProps</span></span>

  
  
<span data-ttu-id="e684f-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e684f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e684f-105">Kopiert oder verschiebt ausgewählten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e684f-105">Copies or moves selected properties.</span></span> 
  
```cpp
HRESULT CopyProps(
  LPSPropTagArray lpIncludeProps,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  LPCIID lpInterface,
  LPVOID lpDestObj,
  ULONG ulFlags,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="e684f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e684f-106">Parameters</span></span>

 <span data-ttu-id="e684f-107">_lpIncludeProps_</span><span class="sxs-lookup"><span data-stu-id="e684f-107">_lpIncludeProps_</span></span>
  
> <span data-ttu-id="e684f-108">[in] Ein Zeiger auf ein Array-Eigenschaft Tag, der angibt, die Eigenschaften zum Kopieren oder verschieben.</span><span class="sxs-lookup"><span data-stu-id="e684f-108">[in] A pointer to a property tag array that specifies the properties to copy or move.</span></span> <span data-ttu-id="e684f-109">**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) kann nicht in das Array aufgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="e684f-109">**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) cannot be included in the array.</span></span> <span data-ttu-id="e684f-110">Der Parameter _LpIncludeProps_ darf nicht **null**sein.</span><span class="sxs-lookup"><span data-stu-id="e684f-110">The  _lpIncludeProps_ parameter cannot be **null**.</span></span>
    
 <span data-ttu-id="e684f-111">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="e684f-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="e684f-112">[in] Ein Handle für das übergeordnete Fenster der Statusanzeige.</span><span class="sxs-lookup"><span data-stu-id="e684f-112">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="e684f-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="e684f-113">_lpProgress_</span></span>
  
> <span data-ttu-id="e684f-114">[in] Ein Zeiger auf eine Implementierung der eine Statusanzeige.</span><span class="sxs-lookup"><span data-stu-id="e684f-114">[in] A pointer to an implementation of a progress indicator.</span></span> <span data-ttu-id="e684f-115">Wenn **null** in der _LpProgress_ -Parameter übergeben wird, wird die Statusanzeige mithilfe der MAPI-Implementierung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e684f-115">If **null** is passed in the  _lpProgress_ parameter, the progress indicator is displayed by using the MAPI implementation.</span></span> <span data-ttu-id="e684f-116">Der Parameter _LpProgress_ wird ignoriert, es sei denn, das Flag MAPI_DIALOG im _UlFlags_ -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e684f-116">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="e684f-117">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="e684f-117">_lpInterface_</span></span>
  
> <span data-ttu-id="e684f-118">[in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle darstellt, die Zugriff auf das Objekt, auf das durch den Parameter _LpDestObj_ verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="e684f-118">[in] A pointer to the interface identifier (IID) that represents the interface that must be used to access the object pointed to by the  _lpDestObj_ parameter.</span></span> <span data-ttu-id="e684f-119">Der Parameter _LpInterface_ darf nicht **null**sein.</span><span class="sxs-lookup"><span data-stu-id="e684f-119">The  _lpInterface_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="e684f-120">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="e684f-120">_lpDestObj_</span></span>
  
> <span data-ttu-id="e684f-121">[in] Ein Zeiger auf das Objekt, das die Eigenschaften kopierten oder verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="e684f-121">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="e684f-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e684f-122">_ulFlags_</span></span>
  
> <span data-ttu-id="e684f-123">[in] Eine Bitmaske aus Flags, die den Vorgang kopieren oder verschieben steuert.</span><span class="sxs-lookup"><span data-stu-id="e684f-123">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="e684f-124">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="e684f-124">The following flags can be set:</span></span>
    
<span data-ttu-id="e684f-125">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="e684f-125">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="e684f-126">Wenn **CopyProps** die [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) -Methode aufgerufen, um die Kopie zu behandeln oder verschoben wird, muss er stattdessen direkt mit den Fehlerwert MAPI_E_DECLINE_COPY zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e684f-126">If **CopyProps** calls the [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method to handle the copy or move operation, it should instead return immediately with the error value MAPI_E_DECLINE_COPY.</span></span> <span data-ttu-id="e684f-127">Das Flag MAPI_DECLINE_OK wird von MAPI festgelegt, um Rekursion zu begrenzen.</span><span class="sxs-lookup"><span data-stu-id="e684f-127">The MAPI_DECLINE_OK flag is set by MAPI to limit recursion.</span></span> <span data-ttu-id="e684f-128">Clients stellen Sie dieses Flag keine.</span><span class="sxs-lookup"><span data-stu-id="e684f-128">Clients do not set this flag.</span></span> 
    
<span data-ttu-id="e684f-129">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="e684f-129">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="e684f-130">Eine Statusanzeige angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e684f-130">Displays a progress indicator.</span></span>
    
<span data-ttu-id="e684f-131">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="e684f-131">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="e684f-132">**CopyProps** sollte einen Verschiebevorgang anstatt einen Kopiervorgang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e684f-132">**CopyProps** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="e684f-133">Wenn dieses Flag nicht festgelegt ist, führt **CopyProps** durch einen Kopiervorgang.</span><span class="sxs-lookup"><span data-stu-id="e684f-133">When this flag is not set, **CopyProps** performs a copy operation.</span></span> 
    
<span data-ttu-id="e684f-134">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="e684f-134">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="e684f-135">Vorhandene Eigenschaften im Zielobjekt sollte nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e684f-135">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="e684f-136">Wenn dieses Flag nicht festgelegt ist, überschreibt **CopyProps** vorhandene Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e684f-136">When this flag is not set, **CopyProps** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="e684f-137">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="e684f-137">_lppProblems_</span></span>
  
> <span data-ttu-id="e684f-138">[in, out] Bei Eingabe einen Zeiger auf einen Zeiger auf eine [SPropProblemArray](spropproblemarray.md) -Struktur. andernfalls **null**, was bedeutet, dass es keine Notwendigkeit Fehlerinformationen besteht.</span><span class="sxs-lookup"><span data-stu-id="e684f-138">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, **null**, indicating that there is no need for error information.</span></span> <span data-ttu-id="e684f-139">Wenn _LppProblems_ einen gültigen Zeiger für die Eingabe ist, gibt **CopyProps** detaillierte Informationen zu Fehlern in eine oder mehrere Eigenschaften kopieren.</span><span class="sxs-lookup"><span data-stu-id="e684f-139">If  _lppProblems_ is a valid pointer on input, **CopyProps** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e684f-140">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="e684f-140">Return value</span></span>

<span data-ttu-id="e684f-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="e684f-141">S_OK</span></span> 
  
> <span data-ttu-id="e684f-142">Eigenschaften wurden erfolgreich kopiert oder verschoben.</span><span class="sxs-lookup"><span data-stu-id="e684f-142">Properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="e684f-143">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="e684f-143">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="e684f-144">Ein Unterobjekt kann nicht kopiert werden, da ein Unterobjekt mit dem gleichen Anzeigenamen, durch die Eigenschaft **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) definiert im Zielobjekt bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e684f-144">A subobject cannot be copied because a subobject with the same display name, defined by the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, already exists in the destination object.</span></span> 
    
<span data-ttu-id="e684f-145">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="e684f-145">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="e684f-146">Der Dienstanbieter implementiert den Kopiervorgang nicht.</span><span class="sxs-lookup"><span data-stu-id="e684f-146">The service provider does not implement the copy operation.</span></span>
    
<span data-ttu-id="e684f-147">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="e684f-147">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="e684f-148">Ausführen des Vorgangs kopieren oder verschieben direkt oder indirekt Quellobjekt enthält Zielobjekt.</span><span class="sxs-lookup"><span data-stu-id="e684f-148">The source object performing the copy or move operation directly or indirectly contains the destination object.</span></span> <span data-ttu-id="e684f-149">Erhebliche Arbeit möglicherweise durchgeführt wurden, bevor diese Bedingung ermittelt wurde, damit die Quell- und Ziel-Objekte teilweise geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="e684f-149">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="e684f-150">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="e684f-150">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="e684f-151">Die Schnittstelle, die vom _LpInterface_ -Parameter wird durch das Zielobjekt nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e684f-151">The interface identified by the  _lpInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="e684f-152">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="e684f-152">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="e684f-153">Es wurde versucht, auf ein Objekt zuzugreifen, für den der Anrufer nicht über ausreichende Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="e684f-153">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="e684f-154">Dieser Fehler wird zurückgegeben, wenn Zielobjekt Quellobjekt identisch ist.</span><span class="sxs-lookup"><span data-stu-id="e684f-154">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="e684f-155">Die folgenden Werte können in der Struktur **SPropProblemArray** , aber nicht als Rückgabewerte für **CopyProps**zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="e684f-155">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **CopyProps**.</span></span> <span data-ttu-id="e684f-156">Diese Fehler gelten für eine einzelne Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e684f-156">These errors apply to a single property.</span></span>
  
<span data-ttu-id="e684f-157">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="e684f-157">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="e684f-158">Entweder die Option MAPI_UNICODE festgelegt wurde und **CopyProps** unterstützt keine Unicode oder Parameter MAPI_UNICODE wurde nicht festgelegt und **CopyProps** nur Unicode unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e684f-158">Either the MAPI_UNICODE flag was set and **CopyProps** does not support Unicode, or MAPI_UNICODE was not set and **CopyProps** supports only Unicode.</span></span> 
    
<span data-ttu-id="e684f-159">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="e684f-159">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="e684f-160">Die Eigenschaft kann nicht vom Anrufer geändert werden, da es eine schreibgeschützte Eigenschaft, mit der Besitzer des Zielobjekts berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="e684f-160">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="e684f-161">Dieser Fehler ist nicht schwerwiegend. der Aufrufer sollte den Kopiervorgang fortgesetzt zulassen.</span><span class="sxs-lookup"><span data-stu-id="e684f-161">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="e684f-162">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="e684f-162">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="e684f-163">Der Eigenschaftstyp ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="e684f-163">The property type is invalid.</span></span>
    
<span data-ttu-id="e684f-164">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="e684f-164">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="e684f-165">Der Eigenschaftentyp ist nicht vom Anrufer erwartet.</span><span class="sxs-lookup"><span data-stu-id="e684f-165">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e684f-166">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e684f-166">Remarks</span></span>

<span data-ttu-id="e684f-167">Die **IMAPIProp::CopyProps** -Methode kopiert oder verschiebt ausgewählte Eigenschaften aus dem aktuellen Objekt in ein Zielobjekt.</span><span class="sxs-lookup"><span data-stu-id="e684f-167">The **IMAPIProp::CopyProps** method copies or moves selected properties from the current object to a destination object.</span></span> <span data-ttu-id="e684f-168">**CopyProps** dient hauptsächlich zum Beantworten und Weiterleiten von Nachrichten, wobei nur einige der Eigenschaften aus der ursprünglichen Nachricht mit der Antwort Reisen oder Kopie weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="e684f-168">**CopyProps** is used mainly for replying to and forwarding messages, where only some of the properties from the original message travel with the reply or forwarded copy.</span></span> 
  
<span data-ttu-id="e684f-169">Alle Unterobjekte im Quellobjekt werden vollständig unabhängig von der Verwendung von Eigenschaften, die durch die Struktur [SPropTagArray](sproptagarray.md) angegeben automatisch bei der Konflikte enthalten und kopiert oder verschoben.</span><span class="sxs-lookup"><span data-stu-id="e684f-169">Any subobjects in the source object are automatically included in the operation and copied or moved in their entirety, regardless of the use of properties indicated by the [SPropTagArray](sproptagarray.md) structure.</span></span> <span data-ttu-id="e684f-170">Standardmäßig überschreibt **CopyProps** Eigenschaften im Zielobjekt, die Eigenschaften aus dem Quellobjekt entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e684f-170">By default, **CopyProps** overwrites any properties in the destination object that match properties from the source object.</span></span> <span data-ttu-id="e684f-171">Wenn die kopierte oder verschobenen Eigenschaften bereits im Zielobjekt vorhanden sind, werden die vorhandenen Eigenschaften von den Eigenschaften der neuen überschrieben, wenn das Flag MAPI_NOREPLACE im _UlFlags_ -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e684f-171">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="e684f-172">Vorhandene Informationen im Zielobjekt, das nicht überschrieben wird, bleibt unverändert.</span><span class="sxs-lookup"><span data-stu-id="e684f-172">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e684f-173">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="e684f-173">Notes to implementers</span></span>

<span data-ttu-id="e684f-174">Sie können eine vollständige Implementierung **CopyProps** bereit oder verlassen sich auf die Implementierung, die MAPI in dessen Support-Objekt bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="e684f-174">You can provide a full implementation of **CopyProps** or rely on the implementation that MAPI provides in its support object.</span></span> <span data-ttu-id="e684f-175">Wenn Sie die MAPI-Implementierung verwenden möchten, rufen Sie die **IMAPISupport::DoCopyProps** -Methode.</span><span class="sxs-lookup"><span data-stu-id="e684f-175">If you want to use the MAPI implementation, call the **IMAPISupport::DoCopyProps** method.</span></span> <span data-ttu-id="e684f-176">Wenn Sie führen Sie die Verarbeitung für **DoCopyProps** delegieren, und Sie das Flag MAPI_DECLINE_OK übergeben werden, vermeiden Sie den Anruf an den Support und zurückzugeben Sie MAPI_E_DECLINE_COPY stattdessen.</span><span class="sxs-lookup"><span data-stu-id="e684f-176">However, if you do delegate processing to **DoCopyProps** and you are passed the MAPI_DECLINE_OK flag, avoid the support call and return MAPI_E_DECLINE_COPY instead.</span></span> <span data-ttu-id="e684f-177">Sie können dieses Flag MAPI, um die möglichen Rekursion zu vermeiden, die auftreten können, wenn Sie den Ordner kopieren aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e684f-177">You will be called with this flag by MAPI to avoid the possible recursion that can occur when you copy folders.</span></span> 
  
<span data-ttu-id="e684f-178">Da der Kopiervorgang langen sein kann, sollte eine Statusanzeige angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e684f-178">Because the copy operation can be lengthy, you should display a progress indicator.</span></span> <span data-ttu-id="e684f-179">Verwenden Sie die [IMAPIProgress](imapiprogressiunknown.md) -Implementierung, die in den _LpProgress_ -Parameter übergeben wird, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e684f-179">Use the [IMAPIProgress](imapiprogressiunknown.md) implementation that is passed in the  _lpProgress_ parameter, if there is one.</span></span> <span data-ttu-id="e684f-180">Wenn _LpProgress_ **null**ist, rufen Sie die [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) -Methode, um die MAPI-Implementierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="e684f-180">If  _lpProgress_ is **null**, call the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to use the MAPI implementation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e684f-181">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="e684f-181">Notes to callers</span></span>

<span data-ttu-id="e684f-182">Legen Sie die Kennzeichen MAPI_DECLINE_OK nicht; Es wird in die Anrufe von MAPI verwendet, auf Speicher-Anbieter **CopyProps** Implementierungen message.</span><span class="sxs-lookup"><span data-stu-id="e684f-182">Do not set the MAPI_DECLINE_OK flag; it is used by MAPI in its calls to message store provider **CopyProps** implementations.</span></span> 
  
<span data-ttu-id="e684f-183">Da verschieben und kopieren können Zeit in Anspruch nehmen, es ist ratsam, die Anzeige einer Statusanzeige anfordern, indem Sie das MAPI_DIALOG-Flag.</span><span class="sxs-lookup"><span data-stu-id="e684f-183">Because copy and move operations can take time, it is wise to request the display of a progress indicator by setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="e684f-184">Sie können den Parameter _LpProgress_ festlegen, die Implementierung von **IMAPIProgress**, falls vorhanden, oder **null**.</span><span class="sxs-lookup"><span data-stu-id="e684f-184">You can set the  _lpProgress_ parameter to your implementation of **IMAPIProgress**, if you have one, or to **null**.</span></span> <span data-ttu-id="e684f-185">Wenn _LpProgress_ **null**ist, wird **CopyProps** die Standard-Statusanzeige bereitgestellt von MAPI verwendet.</span><span class="sxs-lookup"><span data-stu-id="e684f-185">If  _lpProgress_ is **null**, **CopyProps** will use the default progress indicator provided by MAPI.</span></span> 
  
<span data-ttu-id="e684f-186">Sie können die Anzeige einer Statusanzeige installieren, indem Sie das Flag MAPI_DIALOG nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e684f-186">You can suppress the display of a progress indicator by not setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="e684f-187">**CopyProps** die Parameter _UlUIParam_ und _LpProgress_ ignoriert und das Symbol anzeigen vermeiden.</span><span class="sxs-lookup"><span data-stu-id="e684f-187">**CopyProps** will ignore the  _ulUIParam_ and  _lpProgress_ parameters and avoid displaying the indicator.</span></span> 
  
 <span data-ttu-id="e684f-188">**CopyProps** können melden, globale und einzelne-Fehler oder einen oder mehrere der Eigenschaften auftretenden Fehler.</span><span class="sxs-lookup"><span data-stu-id="e684f-188">**CopyProps** can report global and individual errors, or errors that occur with one or more of the properties.</span></span> <span data-ttu-id="e684f-189">Diese einzelnen Fehler werden in einer **SPropProblemArray** eingefügt.</span><span class="sxs-lookup"><span data-stu-id="e684f-189">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="e684f-190">Sie können die Fehlerberichterstattung Ebene der Eigenschaft, indem Sie **null**, anstatt einen gültigen Zeiger, für den Parameter Property Problem Array Struktur übergeben unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="e684f-190">You can suppress error reporting at the property level by passing **null**, instead of a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="e684f-191">Wenn Sie Informationen zu Fehlern erhalten möchten, übergeben Sie einen gültigen **SPropProblemArray** Struktur Zeiger des _LppProblems_ -Parameters.</span><span class="sxs-lookup"><span data-stu-id="e684f-191">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="e684f-192">Wenn **CopyProps** S_OK zurückgegeben wird, überprüfen Sie auf mögliche Fehler mit einzelnen Eigenschaften in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="e684f-192">When **CopyProps** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="e684f-193">Wenn **CopyProps** einen Fehler zurückgibt, wird keine Informationen in der Struktur **SPropProblemArray** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e684f-193">When **CopyProps** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="e684f-194">Rufen Sie stattdessen die [IMAPIProp::GetLastError](imapiprop-getlasterror.md) -Methode, um ausführliche Fehlerinformationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e684f-194">Instead, call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="e684f-195">Wenn **CopyProps** S_OK zurückgibt, frei die zurückgegebene Struktur **SPropProblemArray** durch Aufrufen der [MAPIFreeBuffer](mapifreebuffer.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="e684f-195">If **CopyProps** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="e684f-196">Wenn Sie Eigenschaften, die für den Objekttyp Quelle eindeutig sind kopieren, müssen Sie sicherstellen, dass das Zielobjekt des gleichen Typs ist.</span><span class="sxs-lookup"><span data-stu-id="e684f-196">If you are copying properties that are unique to the source object type, you must make sure that the destination object is of the same type.</span></span> <span data-ttu-id="e684f-197">**CopyProps** verhindert nicht, dass Sie Eigenschaften, die um einen Objekttyp mit einem anderen Typ des Objekts in der Regel gehören, zuordnen.</span><span class="sxs-lookup"><span data-stu-id="e684f-197">**CopyProps** does not prevent you from associating properties that typically belong to one type of object with another type of object.</span></span> <span data-ttu-id="e684f-198">Zum Schluss kommen zum Kopieren von Eigenschaften, die für Zielobjekt sinnvoll ist.</span><span class="sxs-lookup"><span data-stu-id="e684f-198">It is up to you to copy properties that make sense for the destination object.</span></span> <span data-ttu-id="e684f-199">Beispielsweise sollten Sie eine Adressbuchcontainer nicht Nachrichteneigenschaften kopieren.</span><span class="sxs-lookup"><span data-stu-id="e684f-199">For example, you should not copy message properties to an address book container.</span></span> 
  
<span data-ttu-id="e684f-200">Um sicherzustellen, dass Sie zwischen Objekten des gleichen Typs kopieren möchten, prüfen Sie, ob das Quell- und Ziel-Objekt den gleichen Typ, entweder durch Vergleichen Objektzeigern oder die [QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e684f-200">To ensure that you are copying between objects of the same type, check that the source and destination object are the same type, either by comparing object pointers or calling the [IUnknown::QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) method.</span></span> <span data-ttu-id="e684f-201">Legen Sie die Schnittstelle-ID auf den _LpInterface_ der standard-Benutzeroberfläche für das Quellobjekt.</span><span class="sxs-lookup"><span data-stu-id="e684f-201">Set the interface identifier pointed to by  _lpInterface_ to the standard interface for the source object.</span></span> <span data-ttu-id="e684f-202">Stellen Sie außerdem sicher, dass der Objekttyp oder **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))-Eigenschaft für die beiden Objekte identisch ist.</span><span class="sxs-lookup"><span data-stu-id="e684f-202">Also, ensure that the object type or **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property is the same for the two objects.</span></span> <span data-ttu-id="e684f-203">Wenn Sie aus einer Nachricht kopieren möchten, legen Sie _LpInterface_ IID_IMessage und die **PR_OBJECT_TYPE** für beide Objekte MAPI_MESSAGE fest.</span><span class="sxs-lookup"><span data-stu-id="e684f-203">For example, if you are copying from a message, set  _lpInterface_ to IID_IMessage and the **PR_OBJECT_TYPE** for both objects to MAPI_MESSAGE.</span></span> 
  
<span data-ttu-id="e684f-204">Wenn ein ungültiger Zeiger im _LpDestObj_ -Parameter übergeben wird, sind die Ergebnisse unvorhersehbar.</span><span class="sxs-lookup"><span data-stu-id="e684f-204">If an invalid pointer is passed in the  _lpDestObj_ parameter, the results are unpredictable.</span></span> 
  
<span data-ttu-id="e684f-205">Um eine Nachricht Empfängerliste zu kopieren, rufen Sie die Nachricht **CopyProps** -Methode, und fügen Sie die **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))-Eigenschaft im Array Tag-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e684f-205">To copy a message's recipient list, call the message's **CopyProps** method and include the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in the property tag array.</span></span> <span data-ttu-id="e684f-206">Um die e-Mail-Anlagen zu kopieren, umfassen Sie die **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e684f-206">To copy the message's attachments, include the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="e684f-207">Um einen Ordner oder Adressbuchcontainer des Hierarchie oder Inhaltstabelle zu kopieren, unter anderem **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) oder **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) Eigenschaften in der Tag-Array-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e684f-207">To copy a folder or address book container's hierarchy or contents table, include the **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) properties in the property tag array.</span></span> <span data-ttu-id="e684f-208">Einen Ordner zugeordneten Inhaltstabelle aufnehmen möchten, fügen Sie die **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))-Eigenschaft im Array.</span><span class="sxs-lookup"><span data-stu-id="e684f-208">To include a folder's associated contents table, include the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property in the array.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e684f-209">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="e684f-209">MFCMAPI reference</span></span>

<span data-ttu-id="e684f-210">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e684f-210">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e684f-211">**Datei**</span><span class="sxs-lookup"><span data-stu-id="e684f-211">**File**</span></span>|<span data-ttu-id="e684f-212">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="e684f-212">**Function**</span></span>|<span data-ttu-id="e684f-213">**Comment**</span><span class="sxs-lookup"><span data-stu-id="e684f-213">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e684f-214">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="e684f-214">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="e684f-215">CopyNamedProps</span><span class="sxs-lookup"><span data-stu-id="e684f-215">CopyNamedProps</span></span>  <br/> |<span data-ttu-id="e684f-216">MFCMAPI (engl.) verwendet die **IMAPIProp::CopyProps** -Methode, um benannte Eigenschaften von einer Nachricht in eine andere kopiert.</span><span class="sxs-lookup"><span data-stu-id="e684f-216">MFCMAPI uses the **IMAPIProp::CopyProps** method to copy named properties from one message to another.</span></span>  <br/> |
|<span data-ttu-id="e684f-217">SingleMAPIPropListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="e684f-217">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="e684f-218">CSingleMAPIPropListCtrl::OnPasteProperty</span><span class="sxs-lookup"><span data-stu-id="e684f-218">CSingleMAPIPropListCtrl::OnPasteProperty</span></span>  <br/> |<span data-ttu-id="e684f-219">MFCMAPI (engl.) verwendet die **IMAPIProp::CopyProps** -Methode, um eine Eigenschaft einzufügen, die von einem anderen Objekt kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="e684f-219">MFCMAPI uses the **IMAPIProp::CopyProps** method to paste a property that has been copied from another object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e684f-220">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e684f-220">See also</span></span>



[<span data-ttu-id="e684f-221">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="e684f-221">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="e684f-222">IMAPIProgress: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e684f-222">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="e684f-223">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="e684f-223">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
[<span data-ttu-id="e684f-224">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="e684f-224">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="e684f-225">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="e684f-225">IMAPISupport::DoCopyProps</span></span>](imapisupport-docopyprops.md)
  
[<span data-ttu-id="e684f-226">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="e684f-226">IMAPISupport::DoProgressDialog</span></span>](imapisupport-doprogressdialog.md)
  
[<span data-ttu-id="e684f-227">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="e684f-227">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="e684f-228">Kanonische PidTagContainerContents-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e684f-228">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="e684f-229">Kanonische PidTagContainerHierarchy-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e684f-229">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="e684f-230">Kanonische PidTagDisplayName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e684f-230">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="e684f-231">Kanonische PidTagFolderAssociatedContents-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e684f-231">PidTagFolderAssociatedContents Canonical Property</span></span>](pidtagfolderassociatedcontents-canonical-property.md)
  
[<span data-ttu-id="e684f-232">Kanonische PidTagMessageAttachments-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e684f-232">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="e684f-233">Kanonische PidTagMessageRecipients-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e684f-233">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="e684f-234">Kanonische PidTagObjectType-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e684f-234">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="e684f-235">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="e684f-235">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="e684f-236">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="e684f-236">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="e684f-237">IMAPIProp: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e684f-237">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="e684f-238">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="e684f-238">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
