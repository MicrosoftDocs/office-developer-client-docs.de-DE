---
title: IMAPIMessageSiteNewMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.NewMessage
api_type:
- COM
ms.assetid: ce6b6e6c-7f22-43c2-8182-90cf6db93844
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7062e0b73d2d70be12fb9cead6813ef9c36fdd43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792224"
---
# <a name="imapimessagesitenewmessage"></a><span data-ttu-id="afa3d-103">IMAPIMessageSite::NewMessage</span><span class="sxs-lookup"><span data-stu-id="afa3d-103">IMAPIMessageSite::NewMessage</span></span>

  
  
<span data-ttu-id="afa3d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="afa3d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="afa3d-105">Erstellt eine neue Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="afa3d-105">Creates a new message.</span></span>
  
```cpp
HRESULT NewMessage(
  ULONG fComposeInFolder,
  LPMAPIFOLDER pFolderFocus,
  LPPERSISTMESSAGE pPersistMessage,
  LPMESSAGE FAR * ppMessage,
  LPMAPIMESSAGESITE FAR * ppMessageSite,
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a><span data-ttu-id="afa3d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="afa3d-106">Parameters</span></span>

 <span data-ttu-id="afa3d-107">_fComposeInFolder_</span><span class="sxs-lookup"><span data-stu-id="afa3d-107">_fComposeInFolder_</span></span>
  
> <span data-ttu-id="afa3d-108">[in] Gibt an, in welchem Ordner die Nachricht verfasst werden sollte.</span><span class="sxs-lookup"><span data-stu-id="afa3d-108">[in] Indicates in which folder the message should be composed.</span></span> <span data-ttu-id="afa3d-109">Wenn die Variable auf false festgelegt ist, der _pFolderFocus_ -Parameter wird ignoriert, und der Formular-Viewer kann Verfassen Sie die Nachricht in einem Ordner.</span><span class="sxs-lookup"><span data-stu-id="afa3d-109">If the variable is FALSE, the  _pFolderFocus_ parameter is ignored and the form viewer can compose the message in any folder.</span></span> <span data-ttu-id="afa3d-110">Wenn die Variable auf true festgelegt ist und NULL im _pFolderFocus_ -Parameter übergeben wird, besteht die Nachricht im aktuellen Ordner.</span><span class="sxs-lookup"><span data-stu-id="afa3d-110">If the variable is TRUE and NULL is passed in the  _pFolderFocus_ parameter, the message is composed in the current folder.</span></span> <span data-ttu-id="afa3d-111">Wenn die Variable TRUE ist und _pFolderFocus_ein NULL-Wert übergeben wird, besteht die Nachricht im Ordner auf _pFolderFocus_zeigt.</span><span class="sxs-lookup"><span data-stu-id="afa3d-111">If the variable is TRUE and a non-NULL value is passed in  _pFolderFocus_, the message is composed in the folder pointed to by  _pFolderFocus_.</span></span>
    
 <span data-ttu-id="afa3d-112">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="afa3d-112">_pFolderFocus_</span></span>
  
> <span data-ttu-id="afa3d-113">[in] Ein Zeiger auf den Ordner, in dem die neue Nachricht erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="afa3d-113">[in] A pointer to the folder where the new message is created.</span></span>
    
 <span data-ttu-id="afa3d-114">_pPersistMessage_</span><span class="sxs-lookup"><span data-stu-id="afa3d-114">_pPersistMessage_</span></span>
  
> <span data-ttu-id="afa3d-115">[in] Ein Zeiger auf das Form-Objekt für das neue Formular.</span><span class="sxs-lookup"><span data-stu-id="afa3d-115">[in] A pointer to the form object for the new form.</span></span>
    
 <span data-ttu-id="afa3d-116">_ppMessage_</span><span class="sxs-lookup"><span data-stu-id="afa3d-116">_ppMessage_</span></span>
  
> <span data-ttu-id="afa3d-117">[out] Ein Zeiger auf einen Zeiger auf die neue Nachricht.</span><span class="sxs-lookup"><span data-stu-id="afa3d-117">[out] A pointer to a pointer to the new message.</span></span>
    
 <span data-ttu-id="afa3d-118">_ppMessageSite_</span><span class="sxs-lookup"><span data-stu-id="afa3d-118">_ppMessageSite_</span></span>
  
> <span data-ttu-id="afa3d-119">[out] Ein Zeiger auf einen Zeiger auf ein Objekt "Message" Website für die neue Nachricht.</span><span class="sxs-lookup"><span data-stu-id="afa3d-119">[out] A pointer to a pointer to a message site object for the new message.</span></span>
    
 <span data-ttu-id="afa3d-120">_ppViewContext_</span><span class="sxs-lookup"><span data-stu-id="afa3d-120">_ppViewContext_</span></span>
  
> <span data-ttu-id="afa3d-121">[out] Ein Zeiger auf einen Zeiger auf ein Ansichtskontext, die für die Übergabe an ein neues Formular mit der neuen Nachricht geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="afa3d-121">[out] A pointer to a pointer to a view context that is appropriate for passing to a new form with the new message.</span></span> <span data-ttu-id="afa3d-122">Wenn das Formular eine eigene Ansichtskontext implementiert, kann der NULL im _PpViewContext_ -Parameter übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="afa3d-122">If the form implements its own view context, NULL can be passed in the  _ppViewContext_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="afa3d-123">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="afa3d-123">Return value</span></span>

<span data-ttu-id="afa3d-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="afa3d-124">S_OK</span></span> 
  
> <span data-ttu-id="afa3d-125">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="afa3d-125">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="afa3d-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="afa3d-126">Remarks</span></span>

<span data-ttu-id="afa3d-127">Formularobjekte Aufrufen die **IMAPIMessageSite::NewMessage** -Methode zum Erstellen einer neuen Nachricht.</span><span class="sxs-lookup"><span data-stu-id="afa3d-127">Form objects call the **IMAPIMessageSite::NewMessage** method to create a new message.</span></span> <span data-ttu-id="afa3d-128">Das Formular wird mit **NewMessage** eine neue Nachricht und die Website für die zugehörige Nachricht aus der Ansicht abgerufen.</span><span class="sxs-lookup"><span data-stu-id="afa3d-128">The form uses **NewMessage** to get a new message and the associated message site from its view.</span></span> <span data-ttu-id="afa3d-129">Sie können dann die neue Nachricht ändern.</span><span class="sxs-lookup"><span data-stu-id="afa3d-129">It can then modify the new message.</span></span> 
  
<span data-ttu-id="afa3d-130">Sie können auch einen Kontext für die zugeordnete Ansicht durch die Übergabe eines nicht-NULL-Werts im Parameter _PpViewContext_ abrufen.</span><span class="sxs-lookup"><span data-stu-id="afa3d-130">You can also obtain an associated view context by passing in a non-NULL value in the  _ppViewContext_ parameter.</span></span> <span data-ttu-id="afa3d-131">In diesem Ansichtskontext direkt verwendet werden kann, oder aggregiert und an die neue Nachricht übergeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="afa3d-131">This view context can be used directly, or it can be aggregated and passed to the new message.</span></span> <span data-ttu-id="afa3d-132">Wenn eine vollständige Implementierung erforderlich ist, übergeben Sie NULL _PpViewContext_.</span><span class="sxs-lookup"><span data-stu-id="afa3d-132">If a complete implementation is required, pass NULL in  _ppViewContext_.</span></span>
  
<span data-ttu-id="afa3d-133">Eine Liste der Schnittstellen im Zusammenhang mit der Formular-Servern finden Sie unter [MAPI-Formulars Schnittstellen](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="afa3d-133">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="afa3d-134">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="afa3d-134">MFCMAPI reference</span></span>

<span data-ttu-id="afa3d-135">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="afa3d-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="afa3d-136">**Datei**</span><span class="sxs-lookup"><span data-stu-id="afa3d-136">**File**</span></span>|<span data-ttu-id="afa3d-137">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="afa3d-137">**Function**</span></span>|<span data-ttu-id="afa3d-138">**Comment**</span><span class="sxs-lookup"><span data-stu-id="afa3d-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="afa3d-139">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="afa3d-139">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="afa3d-140">CMyMAPIFormViewer::NewMessage</span><span class="sxs-lookup"><span data-stu-id="afa3d-140">CMyMAPIFormViewer::NewMessage</span></span>  <br/> |<span data-ttu-id="afa3d-141">MFCMAPI (engl.) wird die **IMAPIMessageSite::NewMessage** -Methode verwendet, um eine neue Nachricht erstellen, instanziieren Sie einen neues Formular Viewer und Aufrufen von **SetPersist** , um die Nachricht auf dem Formular Viewer festzulegen.</span><span class="sxs-lookup"><span data-stu-id="afa3d-141">MFCMAPI uses the **IMAPIMessageSite::NewMessage** method to create a new message, instantiate a new form viewer, and call **SetPersist** to set the message on the form viewer.</span></span> <span data-ttu-id="afa3d-142">Schließlich gibt den Formular-Viewer als Website für die Nachricht zurück.</span><span class="sxs-lookup"><span data-stu-id="afa3d-142">Finally, it returns the form viewer as the message site.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="afa3d-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="afa3d-143">See also</span></span>



[<span data-ttu-id="afa3d-144">IMAPIViewContext: IUnknown</span><span class="sxs-lookup"><span data-stu-id="afa3d-144">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
  
[<span data-ttu-id="afa3d-145">IMAPIMessageSite: IUnknown</span><span class="sxs-lookup"><span data-stu-id="afa3d-145">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="afa3d-146">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="afa3d-146">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="afa3d-147">MAPI-Formulars Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="afa3d-147">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)
