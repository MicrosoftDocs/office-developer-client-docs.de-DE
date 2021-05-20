---
title: IConverterSessionMIMEToMAPI
manager: soliver
ms.date: 09/06/2019
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.MIMEToMAPI
api_type:
- COM
ms.assetid: ee190ba7-9e71-97e4-7bf1-7b97adc73eed
description: 'Letzte Änderung: 06. September 2019'
ms.openlocfilehash: c9fcffa8ad4dc982e869f4ccd449e1377fb1ea57
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160286"
---
# <a name="iconvertersessionmimetomapi"></a><span data-ttu-id="5e00d-103">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="5e00d-103">IConverterSession::MIMEToMAPI</span></span>

  
  
<span data-ttu-id="5e00d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e00d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e00d-105">Konvertiert einen MIME-Stream in eine MAPI-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="5e00d-105">Converts a MIME stream to a MAPI message.</span></span>
  
```cpp
HRESULT IConverterSession:: MIMEToMAPI ( 
     LPSTREAM pstm, 
     LPMESSAGE pmsg, 
     LPCSTR pszSrcSrv, 
     ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="5e00d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e00d-106">Parameters</span></span>

 <span data-ttu-id="5e00d-107">_pstm_</span><span class="sxs-lookup"><span data-stu-id="5e00d-107">_pstm_</span></span>
  
> <span data-ttu-id="5e00d-108">[in] [IStream-Schnittstelle](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) zu einem MIME-Stream.</span><span class="sxs-lookup"><span data-stu-id="5e00d-108">[in] [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface to a MIME stream.</span></span> 
    
 <span data-ttu-id="5e00d-109">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="5e00d-109">_pmsg_</span></span>
  
> <span data-ttu-id="5e00d-110">[in] Zeiger auf die zu ladende Nachricht.</span><span class="sxs-lookup"><span data-stu-id="5e00d-110">[in] Pointer to the message to load.</span></span> <span data-ttu-id="5e00d-111">Der Aufrufer muss eine Meldung zum Ausfüllen der API liefern, damit das Objekt [in] wechseln muss.</span><span class="sxs-lookup"><span data-stu-id="5e00d-111">The caller must supply a message for the API to fill out, so the object must go [in].</span></span> <span data-ttu-id="5e00d-112">Die Typdefinition von **LPMESSAGE** finden Sie unter mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="5e00d-112">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span>
    
 <span data-ttu-id="5e00d-113">_pszSrcSrv_</span><span class="sxs-lookup"><span data-stu-id="5e00d-113">_pszSrcSrv_</span></span>
  
> <span data-ttu-id="5e00d-114">[in] Dieser Wert muss **null sein.**</span><span class="sxs-lookup"><span data-stu-id="5e00d-114">[in] This value must be **null**.</span></span>
    
 <span data-ttu-id="5e00d-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5e00d-115">_ulFlags_</span></span>
  
> <span data-ttu-id="5e00d-116">[in] Dieser Parameter identifiziert alle besonderen Aktionen, die während der Konvertierung ergriffen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5e00d-116">[in] This parameter identifies any special action to be taken during the conversion.</span></span> <span data-ttu-id="5e00d-117">Es muss null (0) sein, wenn keine bestimmte Aktion oder eine Kombination der folgenden Werte ergriffen werden soll:</span><span class="sxs-lookup"><span data-stu-id="5e00d-117">It must be zero (0) if no specific action is to be taken, or a combination of the following values:</span></span>
    
<span data-ttu-id="5e00d-118">CCSF_EMBEDDED_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="5e00d-118">CCSF_EMBEDDED_MESSAGE</span></span>
  
> <span data-ttu-id="5e00d-119">Gesendete/nicht gesendete Informationen werden in X-Unsent beibehalten.</span><span class="sxs-lookup"><span data-stu-id="5e00d-119">Sent/unsent information is persisted in X-Unsent.</span></span>
    
<span data-ttu-id="5e00d-120">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="5e00d-120">CCSF_SMTP</span></span>
  
> <span data-ttu-id="5e00d-121">Der MIME-Stream ist für eine SIMPLE Mail Transfer Protocol (SMTP)-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="5e00d-121">The MIME stream is for a Simple Mail Transfer Protocol (SMTP) message.</span></span>
    
<span data-ttu-id="5e00d-122">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="5e00d-122">CCSF_INCLUDE_BCC</span></span>
  
> <span data-ttu-id="5e00d-123">BCC-Empfänger des MIME-Datenstroms sollten in der MAPI-Nachricht enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="5e00d-123">BCC recipients of the MIME stream should be included in the MAPI message.</span></span>
    
<span data-ttu-id="5e00d-124">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="5e00d-124">CCSF_USE_RTF</span></span>
  
> <span data-ttu-id="5e00d-125">Der HTML-Textkörper des MIME-Datenstroms sollte in der MAPI-Nachricht in das Rich Text Format (RTF) konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="5e00d-125">The HTML body of the MIME stream should be converted to Rich Text Format (RTF) in the MAPI message.</span></span>

<span data-ttu-id="5e00d-126">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="5e00d-126">CCSF_GLOBAL_MESSAGE</span></span>
> <span data-ttu-id="5e00d-127">Der Konverter sollte den MIME-Stream als internationale Nachricht behandeln (EAI/RFC6530).</span><span class="sxs-lookup"><span data-stu-id="5e00d-127">The converter should handle the MIME stream as an international message (EAI/RFC6530).</span></span> <span data-ttu-id="5e00d-128">Wird in Outlook 2013 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5e00d-128">Not supported on Outlook 2013.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5e00d-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5e00d-129">Return value</span></span>

<span data-ttu-id="5e00d-130">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="5e00d-130">E_INVALIDARG</span></span>
  
> <span data-ttu-id="5e00d-131">Gibt an,  _dass pstm_ **null** ist,  _pmsg_ **null** oder  _ulFlags_ ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="5e00d-131">Indicates that  _pstm_ is **null**,  _pmsg_ is **null**, or  _ulFlags_ is invalid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5e00d-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5e00d-132">Remarks</span></span>

<span data-ttu-id="5e00d-133">Wenn Sie  CCSF_USE_RTF als Teil von _ulFlags_ angegeben haben und der Zielnachrichtenspeicher HTML und RTF unterstützt, wird die MAPI-Nachricht in HTML oder RTF konvertiert.</span><span class="sxs-lookup"><span data-stu-id="5e00d-133">If you have specified **CCSF_USE_RTF** as part of  _ulFlags_ and the destination message store supports both HTML and RTF, the MAPI message will be converted to either HTML or RTF.</span></span> <span data-ttu-id="5e00d-134">Wenn die Nachricht in RTF konvertiert wird, wird das konvertierte Format rtF komprimiert, alle #A0 in die komprimierte #A1 eingebettet, und die Zeichenfolge ist in der [kanonischen Eigenschaft PidTagRtfCompressed enthalten.](pidtagrtfcompressed-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="5e00d-134">If the message is converted to RTF, the converted format will be compressed RTF, any HTML will be embedded in the compressed RTF string, and the string will be contained in the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5e00d-135">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="5e00d-135">MFCMAPI reference</span></span>

<span data-ttu-id="5e00d-136">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="5e00d-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5e00d-137">**Datei**</span><span class="sxs-lookup"><span data-stu-id="5e00d-137">**File**</span></span>|<span data-ttu-id="5e00d-138">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="5e00d-138">**Function**</span></span>|<span data-ttu-id="5e00d-139">**Comment**</span><span class="sxs-lookup"><span data-stu-id="5e00d-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5e00d-140">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="5e00d-140">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="5e00d-141">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="5e00d-141">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="5e00d-142">MFCMAPI verwendet MimeToMAPI, um eine EML-Datei in eine MAPI-Nachricht zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="5e00d-142">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="5e00d-143">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="5e00d-143">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="5e00d-144">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="5e00d-144">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="5e00d-145">MFCMAPI verwendet MAPIToMIMEStm, um eine MAPI-Nachricht in eine EML-Datei zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="5e00d-145">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5e00d-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e00d-146">See also</span></span>



[<span data-ttu-id="5e00d-147">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5e00d-147">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="5e00d-148">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="5e00d-148">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="5e00d-149">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="5e00d-149">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="5e00d-150">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="5e00d-150">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="5e00d-151">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="5e00d-151">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="5e00d-152">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="5e00d-152">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="5e00d-153">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="5e00d-153">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)


[<span data-ttu-id="5e00d-154">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="5e00d-154">MAPI Constants</span></span>](mapi-constants.md)

