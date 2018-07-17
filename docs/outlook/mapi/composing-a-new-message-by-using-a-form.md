---
title: Verfassen einer neuen Nachricht mithilfe eines Formulars
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c92181c4-79ca-4310-8bf1-2bc335c8e0cd
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f4b9cb00512838e6b54c0cc910b8f7279120db3c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791425"
---
# <a name="composing-a-new-message-by-using-a-form"></a><span data-ttu-id="9d440-103">Verfassen einer neuen Nachricht mithilfe eines Formulars</span><span class="sxs-lookup"><span data-stu-id="9d440-103">Composing a New Message by Using a Form</span></span>

  
  
<span data-ttu-id="9d440-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9d440-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9d440-105">Um ein Formular zum Verfassen einer neuen Nachricht verwenden, müssen Sie zuerst erstellen Sie ein neue benutzerdefinierte Message-Objekt.</span><span class="sxs-lookup"><span data-stu-id="9d440-105">To use a form to compose a new message, first create a new custom message object.</span></span>
  
 <span data-ttu-id="9d440-106">**Um eine neue Nachricht mit einem Formular zum Verfassen**</span><span class="sxs-lookup"><span data-stu-id="9d440-106">**To compose a new message using a form**</span></span>
  
1. <span data-ttu-id="9d440-107">Rufen Sie den Formular-Manager [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) -Methode, um einen Zeiger auf ein Form-Informationsobjekt abzurufen – ein Objekt, das implementiert die [IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md) Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="9d440-107">Call the form manager's [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method to retrieve a pointer to a form information object — an object that implements the [IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md) interface.</span></span> 
    
2. <span data-ttu-id="9d440-108">Übergeben Sie den Zeiger auf das Formular Informationen-Objekt in einem Aufruf von [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md).</span><span class="sxs-lookup"><span data-stu-id="9d440-108">Pass the pointer to the form information object in a call to [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md).</span></span> <span data-ttu-id="9d440-109">**CreateForm** lädt den entsprechende Formular Server.</span><span class="sxs-lookup"><span data-stu-id="9d440-109">**CreateForm** loads the appropriate form server.</span></span> <span data-ttu-id="9d440-110">Übergeben Sie darüber hinaus Interface Identifier an **CreateForm** an, das die Schnittstelle für die neue Nachricht Zugriff auf verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9d440-110">In addition, pass an interface identifier to **CreateForm** to specify the interface to be used to access the new message.</span></span> <span data-ttu-id="9d440-111">In der Regel, die Sie anfordern [IPersistMessage: IUnknown](ipersistmessageiunknown.md) , indem Sie auf **CreateForm**IID_IPersistMessage übergeben.</span><span class="sxs-lookup"><span data-stu-id="9d440-111">Typically, you request [IPersistMessage : IUnknown](ipersistmessageiunknown.md) by passing IID_IPersistMessage to **CreateForm**.</span></span>
    
3. <span data-ttu-id="9d440-112">Speichern Sie die neue Nachricht durch seine [IPersistMessage::Save](ipersistmessage-save.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9d440-112">Save the new message by calling its [IPersistMessage::Save](ipersistmessage-save.md) method.</span></span> <span data-ttu-id="9d440-113">Der Formular-Server sollte Werte für die Nachricht erforderlichen Eigenschaften festgelegt, wenn die Nachricht erstellt.</span><span class="sxs-lookup"><span data-stu-id="9d440-113">The form server should set values for the message's required properties when it creates the message.</span></span> 
    
4. <span data-ttu-id="9d440-114">Laden Sie die Nachricht mithilfe einer der beiden folgenden Strategien: [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) oder [IMAPISession::PrepareForm](imapisession-prepareform.md) gefolgt von [IMAPISession::ShowForm](imapisession-showform.md).</span><span class="sxs-lookup"><span data-stu-id="9d440-114">Load the message by using one of two strategies: [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) or [IMAPISession::PrepareForm](imapisession-prepareform.md) followed by [IMAPISession::ShowForm](imapisession-showform.md).</span></span> <span data-ttu-id="9d440-115">Weitere Informationen zu diesen Strategien finden Sie unter [Laden einer Nachricht in ein Formular](loading-a-message-into-a-form.md).</span><span class="sxs-lookup"><span data-stu-id="9d440-115">For more information about these strategies, see [Loading a Message Into a Form](loading-a-message-into-a-form.md).</span></span>
    
> [!NOTE]
> <span data-ttu-id="9d440-116">Möglichkeiten zur Leistungssteigerung vorhanden sind, eine neue benutzerdefinierte Meldung in einem Formular Server zu laden, da Sie bereits Gelegenheit, einige Informationen über die Meldung erhalten kommuniziert haben, werden – wie deren Nachrichtenklasse – während der Verarbeitung für die **erforderlich ResolveMessageClass** und **CreateForm** Anrufe.</span><span class="sxs-lookup"><span data-stu-id="9d440-116">There are opportunities for performance gains when loading a new custom message into a form server because you will already have had an opportunity to get some information about the message — such as its message class — during the processing required for the **ResolveMessageClass** and **CreateForm** calls.</span></span> <span data-ttu-id="9d440-117">Aus diesem Grund werden Sie vereinfachen die Verarbeitung vor dem Aufruf von **LoadForm** , die in den in der [Nachricht in ein Formular geladen](loading-a-message-into-a-form.md)Thema beschriebenen erforderlich sein.</span><span class="sxs-lookup"><span data-stu-id="9d440-117">Because of this, you will be able to simplify the processing required before calling **LoadForm** over that described in the topic [Loading a Message Into a Form](loading-a-message-into-a-form.md).</span></span> 
  
