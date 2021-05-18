---
title: Verfassen einer neuen Nachricht mithilfe eines Formulars
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c92181c4-79ca-4310-8bf1-2bc335c8e0cd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1c5ba8631ba39309b7131440f04564f80b5dbb57
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412800"
---
# <a name="composing-a-new-message-by-using-a-form"></a><span data-ttu-id="7de5a-103">Verfassen einer neuen Nachricht mithilfe eines Formulars</span><span class="sxs-lookup"><span data-stu-id="7de5a-103">Composing a New Message by Using a Form</span></span>

  
  
<span data-ttu-id="7de5a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7de5a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7de5a-105">Um ein Formular zum Verfassen einer neuen Nachricht zu verwenden, erstellen Sie zunächst ein neues benutzerdefiniertes Nachrichtenobjekt.</span><span class="sxs-lookup"><span data-stu-id="7de5a-105">To use a form to compose a new message, first create a new custom message object.</span></span>
  
 <span data-ttu-id="7de5a-106">**So verfassen Sie eine neue Nachricht mithilfe eines Formulars**</span><span class="sxs-lookup"><span data-stu-id="7de5a-106">**To compose a new message using a form**</span></span>
  
1. <span data-ttu-id="7de5a-107">Rufen Sie die [IMAPIFormMgr::ResolveMessageClass-Methode](imapiformmgr-resolvemessageclass.md) des Formular-Managers auf, um einen Zeiger auf ein Formularinformationsobjekt abzurufen – ein Objekt, das die [IMAPIFormInfo : IMAPIProp-Schnittstelle](imapiforminfoimapiprop.md) implementiert.</span><span class="sxs-lookup"><span data-stu-id="7de5a-107">Call the form manager's [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method to retrieve a pointer to a form information object — an object that implements the [IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md) interface.</span></span> 
    
2. <span data-ttu-id="7de5a-108">Übergeben Sie den Zeiger an das Formularinformationsobjekt in einem Aufruf von [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md).</span><span class="sxs-lookup"><span data-stu-id="7de5a-108">Pass the pointer to the form information object in a call to [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md).</span></span> <span data-ttu-id="7de5a-109">**CreateForm** lädt den entsprechenden Formularserver.</span><span class="sxs-lookup"><span data-stu-id="7de5a-109">**CreateForm** loads the appropriate form server.</span></span> <span data-ttu-id="7de5a-110">Übergeben Sie außerdem eine Schnittstellen-ID an **CreateForm,** um die Schnittstelle anzugeben, die für den Zugriff auf die neue Nachricht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7de5a-110">In addition, pass an interface identifier to **CreateForm** to specify the interface to be used to access the new message.</span></span> <span data-ttu-id="7de5a-111">In der Regel fordern Sie [IPersistMessage : IUnknown](ipersistmessageiunknown.md) an, indem Sie IID_IPersistMessage **CreateForm übergeben.**</span><span class="sxs-lookup"><span data-stu-id="7de5a-111">Typically, you request [IPersistMessage : IUnknown](ipersistmessageiunknown.md) by passing IID_IPersistMessage to **CreateForm**.</span></span>
    
3. <span data-ttu-id="7de5a-112">Speichern Sie die neue Nachricht, indem Sie die [IPersistMessage::Save-Methode](ipersistmessage-save.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7de5a-112">Save the new message by calling its [IPersistMessage::Save](ipersistmessage-save.md) method.</span></span> <span data-ttu-id="7de5a-113">Der Formularserver sollte beim Erstellen der Nachricht Werte für die erforderlichen Eigenschaften der Nachricht festlegen.</span><span class="sxs-lookup"><span data-stu-id="7de5a-113">The form server should set values for the message's required properties when it creates the message.</span></span> 
    
4. <span data-ttu-id="7de5a-114">Laden Sie die Nachricht mithilfe einer von zwei Strategien: [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) oder [IMAPISession::P repareForm](imapisession-prepareform.md) gefolgt von [IMAPISession::ShowForm](imapisession-showform.md).</span><span class="sxs-lookup"><span data-stu-id="7de5a-114">Load the message by using one of two strategies: [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) or [IMAPISession::PrepareForm](imapisession-prepareform.md) followed by [IMAPISession::ShowForm](imapisession-showform.md).</span></span> <span data-ttu-id="7de5a-115">Weitere Informationen zu diesen Strategien finden Sie unter [Laden einer Nachricht in ein Formular](loading-a-message-into-a-form.md).</span><span class="sxs-lookup"><span data-stu-id="7de5a-115">For more information about these strategies, see [Loading a Message Into a Form](loading-a-message-into-a-form.md).</span></span>
    
> [!NOTE]
> <span data-ttu-id="7de5a-116">Es gibt Möglichkeiten für Leistungsgewinne beim Laden einer neuen benutzerdefinierten Nachricht auf einem Formularserver, da Sie bereits während der Verarbeitung, die für die **ResolveMessageClass-** und **CreateForm-Aufrufe** erforderlich ist, die Möglichkeit hatten, Informationen zur Nachricht – z. B. der Nachrichtenklasse – zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7de5a-116">There are opportunities for performance gains when loading a new custom message into a form server because you will already have had an opportunity to get some information about the message — such as its message class — during the processing required for the **ResolveMessageClass** and **CreateForm** calls.</span></span> <span data-ttu-id="7de5a-117">Aus diesem Grund können Sie die Verarbeitung vereinfachen, bevor **Sie LoadForm über** das im Thema Laden einer Nachricht in ein Formular beschriebene Aufrufen [aufrufen.](loading-a-message-into-a-form.md)</span><span class="sxs-lookup"><span data-stu-id="7de5a-117">Because of this, you will be able to simplify the processing required before calling **LoadForm** over that described in the topic [Loading a Message Into a Form](loading-a-message-into-a-form.md).</span></span> 
  

