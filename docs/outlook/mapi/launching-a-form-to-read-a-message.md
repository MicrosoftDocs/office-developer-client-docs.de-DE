---
title: Starten eines Formulars zum Lesen einer Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 54a4b805-2ab7-4fb7-b0ea-4a33ead27451
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 439927dc78941f086c025d77c76236497d3f4a15
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425932"
---
# <a name="launching-a-form-to-read-a-message"></a><span data-ttu-id="a873e-103">Starten eines Formulars zum Lesen einer Nachricht</span><span class="sxs-lookup"><span data-stu-id="a873e-103">Launching a Form to Read a Message</span></span>

  
  
<span data-ttu-id="a873e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a873e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a873e-105">Die Implementierung von Formularservern sollte die folgende Abfolge von Methodenaufrufen an ihren Formularserver und Formularobjekte erwarten, wenn eine Clientanwendung eine Nachricht lädt:</span><span class="sxs-lookup"><span data-stu-id="a873e-105">Form server implementers should expect the following sequence of method calls to their form server and form objects when a client application loads a message:</span></span>
  
1. <span data-ttu-id="a873e-106">Die Clientanwendung öffnet den Formular-Manager mit einem Aufruf der [MAPIOpenFormMgr-Funktion.](mapiopenformmgr.md)</span><span class="sxs-lookup"><span data-stu-id="a873e-106">The client application opens the form manager with a call to the [MAPIOpenFormMgr](mapiopenformmgr.md) function.</span></span> 
    
2. <span data-ttu-id="a873e-107">Die Clientanwendung ruft die [IMAPIFormMgr::LoadForm-Methode](imapiformmgr-loadform.md) auf, die ein Objekt mit [IMAPIForm zurückgibt.](imapiformiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="a873e-107">The client application calls the [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) method, which returns an object with [IMAPIForm](imapiformiunknown.md).</span></span> <span data-ttu-id="a873e-108">Der Formular-Manager kann jetzt freigegeben werden, wenn er nicht für weitere Formularaktivierungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a873e-108">The form manager may be released now if it will not be used for further form activations.</span></span> <span data-ttu-id="a873e-109">Beachten Sie, dass ein Aufruf von **LoadForm** einige Zeit dauern kann, da der Formular-Manager möglicherweise die ausführbaren Dateien des Formularservers installieren muss, bevor er fortfahren kann.</span><span class="sxs-lookup"><span data-stu-id="a873e-109">Note that a call to **LoadForm** may take some time because the form manager may have to install the form server's executable files before proceeding.</span></span> 
    
3. <span data-ttu-id="a873e-110">Optional kann die Clientanwendung [IMAPIViewContext](imapiviewcontextiunknown.md) vorbereiten, um Vorgänge zu steuern, die dazu führen können, dass das Formularobjekt die vorherige oder nächste Nachricht in den Ordner laden kann.</span><span class="sxs-lookup"><span data-stu-id="a873e-110">Optionally, the client application can prepare [IMAPIViewContext](imapiviewcontextiunknown.md) to control operations that may cause the form object to load the previous or next message in the folder.</span></span> <span data-ttu-id="a873e-111">Die Clientanwendung kann die [IMAPIForm::SetViewContext-Methode](imapiform-setviewcontext.md) verwenden, um den Standardansichtskontext zu ändern, der im **LoadForm-Aufruf festgelegt** wurde.</span><span class="sxs-lookup"><span data-stu-id="a873e-111">The client application can use the [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method to change the default view context that was set in the **LoadForm** call.</span></span> 
    
4. <span data-ttu-id="a873e-112">Die Clientanwendung ruft die [IPersistMessage::Load-Methode](ipersistmessage-load.md) auf, um Nachrichtendaten in das Formularobjekt zu laden.</span><span class="sxs-lookup"><span data-stu-id="a873e-112">The client application calls the [IPersistMessage::Load](ipersistmessage-load.md) method to load message data into the form object.</span></span> 
    
5. <span data-ttu-id="a873e-113">Die Clientanwendung ruft [IMAPIForm::D oVerb](imapiform-doverb.md) auf, um das geöffnete Verb auf aufruft, und übergeben dabei den optionalen [IMAPIViewContext-Schnittstellenzeiger.](imapiviewcontextiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="a873e-113">The client application calls [IMAPIForm::DoVerb](imapiform-doverb.md) to invoke the open verb, passing the optional [IMAPIViewContext](imapiviewcontextiunknown.md) interface pointer.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="a873e-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a873e-114">See also</span></span>



[<span data-ttu-id="a873e-115">Formularserverinteraktionen</span><span class="sxs-lookup"><span data-stu-id="a873e-115">Form Server Interactions</span></span>](form-server-interactions.md)

