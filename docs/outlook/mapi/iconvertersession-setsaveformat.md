---
title: IConverterSessionSetSaveFormat
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetCharSet
api_type:
- COM
ms.assetid: e5308a94-5191-2109-a881-b4f4a7ff1c61
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b528d6ef45c02b27f8e07d151793fc338f9af7b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336638"
---
# <a name="iconvertersessionsetsaveformat"></a><span data-ttu-id="006a9-103">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="006a9-103">IConverterSession::SetSaveFormat</span></span>

<span data-ttu-id="006a9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="006a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="006a9-105">Legt das Format fest, in dem der Konverter einen MIME-Stream in [IConverterSession::MAPIToMIMEStm zurück gibt.](iconvertersession-mapitomimestm.md)</span><span class="sxs-lookup"><span data-stu-id="006a9-105">Sets the format in which the converter will return a MIME stream in [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span></span>
  
```cpp
HRESULT IConverterSession::SetSaveFormat ( 
     MIMESAVETYPE mstSaveFormat 
);
```

## <a name="parameters"></a><span data-ttu-id="006a9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="006a9-106">Parameters</span></span>

<span data-ttu-id="006a9-107">_mstSaveFormat_</span><span class="sxs-lookup"><span data-stu-id="006a9-107">_mstSaveFormat_</span></span>
  
> <span data-ttu-id="006a9-108">[in] Das Speicherformat, das für einen MIME-Stream verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="006a9-108">[in] The save format to be used for a MIME stream.</span></span> <span data-ttu-id="006a9-109">Weitere Informationen finden Sie im Enumerationstyp [MIMESAVETYPE](https://msdn.microsoft.com/library/ms715128%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="006a9-109">For more information, see the enum type [MIMESAVETYPE](https://msdn.microsoft.com/library/ms715128%28VS.85%29.aspx).</span></span>
    
  - <span data-ttu-id="006a9-110">**SAVE_RFC1521**: Verwenden Sie MIME, was die Standardeinstellung ist.</span><span class="sxs-lookup"><span data-stu-id="006a9-110">**SAVE_RFC1521**: Use MIME, which is the default.</span></span>      
  - <span data-ttu-id="006a9-111">**SAVE_RFC822**: Verwenden Sie uuencode.</span><span class="sxs-lookup"><span data-stu-id="006a9-111">**SAVE_RFC822**: Use uuencode.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="006a9-112">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="006a9-112">Return values</span></span>

<span data-ttu-id="006a9-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="006a9-113">S_OK</span></span>
  
> <span data-ttu-id="006a9-114">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="006a9-114">The call was successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="006a9-115">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="006a9-115">MFCMAPI reference</span></span>

<span data-ttu-id="006a9-116">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="006a9-116">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="006a9-117">**Datei**</span><span class="sxs-lookup"><span data-stu-id="006a9-117">**File**</span></span>|<span data-ttu-id="006a9-118">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="006a9-118">**Function**</span></span>|<span data-ttu-id="006a9-119">**Comment**</span><span class="sxs-lookup"><span data-stu-id="006a9-119">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="006a9-120">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="006a9-120">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="006a9-121">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="006a9-121">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="006a9-122">MFCMAPI verwendet MimeToMAPI, um eine EML-Datei in eine MAPI-Nachricht zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="006a9-122">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="006a9-123">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="006a9-123">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="006a9-124">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="006a9-124">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="006a9-125">MFCMAPI verwendet MAPIToMIMEStm, um eine MAPI-Nachricht in eine EML-Datei zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="006a9-125">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="006a9-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="006a9-126">See also</span></span>

- [<span data-ttu-id="006a9-127">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="006a9-127">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
- [<span data-ttu-id="006a9-128">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="006a9-128">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
- [<span data-ttu-id="006a9-129">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="006a9-129">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
- [<span data-ttu-id="006a9-130">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="006a9-130">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
- [<span data-ttu-id="006a9-131">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="006a9-131">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
- [<span data-ttu-id="006a9-132">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="006a9-132">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
- [<span data-ttu-id="006a9-133">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="006a9-133">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
- [<span data-ttu-id="006a9-134">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="006a9-134">MAPI Constants</span></span>](mapi-constants.md)

