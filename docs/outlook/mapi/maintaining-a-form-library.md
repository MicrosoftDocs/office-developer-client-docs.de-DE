---
title: Verwalten einer Formularbibliothek
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8488f7ec-e44b-4d1a-ba42-baea8c71d350
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5ccb5a2881d3cef3ff21a106e7e9ea33e0aedd9e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792915"
---
# <a name="maintaining-a-form-library"></a><span data-ttu-id="1e92a-103">Verwalten einer Formularbibliothek</span><span class="sxs-lookup"><span data-stu-id="1e92a-103">Maintaining a Form Library</span></span>

  
  
<span data-ttu-id="1e92a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1e92a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1e92a-105">Eine Formularbibliothek enthält alle wichtigen Informationen zu einem Formular: seine Eigenschaften, seiner Verben und ausführbare Dateien des Servers.</span><span class="sxs-lookup"><span data-stu-id="1e92a-105">A form library holds all of the important information about a form: its properties, its verbs, and its server's executable files.</span></span> <span data-ttu-id="1e92a-106">Einige Clients können ihre Benutzer verwalten, installieren oder Entfernen von Servern Formular.</span><span class="sxs-lookup"><span data-stu-id="1e92a-106">Some clients allow their users to maintain, install, or remove form servers.</span></span> <span data-ttu-id="1e92a-107">Wenn Sie dieses Feature Ihren Benutzern anbieten möchten, benötigen Sie Zugriff auf:</span><span class="sxs-lookup"><span data-stu-id="1e92a-107">If you want to offer this feature to your users, you must have access to:</span></span>
  
- <span data-ttu-id="1e92a-108">Der Formular-Server-Konfigurationsdatei, eine Datei mit der. Erweiterung CFG.</span><span class="sxs-lookup"><span data-stu-id="1e92a-108">The form server's configuration file, a file with the .CFG extension.</span></span>
    
- <span data-ttu-id="1e92a-109">Der Formularbibliothek Container-Objekt, ein Objekt, das implementiert die [IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md) Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="1e92a-109">The form library's container object, an object that implements the [IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) interface.</span></span> 
    
<span data-ttu-id="1e92a-110">Zugriff auf die Konfigurationsdatei oder einen Pfadnamen zu verwenden sind beliebige Weise praktisch.</span><span class="sxs-lookup"><span data-stu-id="1e92a-110">To access the configuration file or a pathname to it, use whatever means are convenient.</span></span> <span data-ttu-id="1e92a-111">Clients stehen in der Regel dem Benutzer ein Dialogfeld zum Installieren und Entfernen von Servern Formular, die auch verwendet werden können, um den Benutzer für den Speicherort der Konfigurationsdatei aufzufordern.</span><span class="sxs-lookup"><span data-stu-id="1e92a-111">Usually, clients present the user with a dialog box for installing and removing form servers that can also be used to prompt the user for the location of the configuration file.</span></span>
  
<span data-ttu-id="1e92a-112">Rufen Sie den Formular-Manager [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) -Methode, um für den Zugriff auf die Formularbibliothek Container.</span><span class="sxs-lookup"><span data-stu-id="1e92a-112">To access the form library's container, call the form manager's [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) method.</span></span> <span data-ttu-id="1e92a-113">Übergeben Sie eine Enumerationswert an, welche Formularbibliothek zu öffnen, und Sie bei Bedarf einen Zeiger auf das Objekt, das der Formular-Manager zum Öffnen der Formularbibliothek verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1e92a-113">Pass in an enumeration value to specify which form library to open, and if necessary, a pointer to the object that the form manager should use to open the form library.</span></span> <span data-ttu-id="1e92a-114">Wenn Sie einen [Ordner von Formularbibliotheken](folder-form-libraries.md)öffnen, beispielsweise übergeben ein [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) Zeiger.</span><span class="sxs-lookup"><span data-stu-id="1e92a-114">For example, if you are opening a [Folder Form Libraries](folder-form-libraries.md), pass an [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) pointer.</span></span> 
  
<span data-ttu-id="1e92a-115">Nach dem **OpenFormContainer** den **IMAPIFormContainer** Zeiger zurückgegeben wird, rufen Sie [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) oder [IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md), je nach der Wartung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1e92a-115">After **OpenFormContainer** returns the **IMAPIFormContainer** pointer, call either [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) or [IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md), depending on the maintenance to be performed.</span></span> <span data-ttu-id="1e92a-116">**InstallForm** hinzugefügt der Bibliothek einen Formular Server; **RemoveForm** Löscht einen Formular Server aus der Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="1e92a-116">**InstallForm** adds a form server to the library; **RemoveForm** deletes a form server from the library.</span></span> 
  
