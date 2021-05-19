---
title: MAPI-Suchordner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 36c14d91-77f7-43a3-8d87-d50bcc21fad7
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c1d7f67458852319587d98831d031b2c3a131871
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357673"
---
# <a name="mapi-search-folders"></a><span data-ttu-id="9fa01-103">MAPI-Suchordner</span><span class="sxs-lookup"><span data-stu-id="9fa01-103">MAPI Search Folders</span></span>

  
  
<span data-ttu-id="9fa01-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9fa01-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9fa01-p101">A search-results folder holds links to messages in generic folders rather than the actual messages. Clients create a search-results folder by calling the [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) method with FOLDER_SEARCH as the  _ulFolderType_ parameter. Clients fill a search-results folder by setting up and applying search criteria�� rules that filter out messages with particular characteristics. Search criteria are set up with the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method. Clients build one or more [SRestriction](srestriction.md) structures to represent the search criteria to be applied and pass them to **SetSearchCriteria**. **SetSearchCriteria** also specifies a list of folders that indicate the search domain and a set of flags that control how the search is performed.</span><span class="sxs-lookup"><span data-stu-id="9fa01-p101">A search-results folder holds links to messages in generic folders rather than the actual messages. Clients create a search-results folder by calling the [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) method with FOLDER_SEARCH as the  _ulFolderType_ parameter. Clients fill a search-results folder by setting up and applying search criteria — rules that filter out messages with particular characteristics. Search criteria are set up with the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method. Clients build one or more [SRestriction](srestriction.md) structures to represent the search criteria to be applied and pass them to **SetSearchCriteria**. **SetSearchCriteria** also specifies a list of folders that indicate the search domain and a set of flags that control how the search is performed.</span></span> 
  
 <span data-ttu-id="9fa01-111">**SetSearchCriteria** identifies the messages that match the specified restriction.</span><span class="sxs-lookup"><span data-stu-id="9fa01-111">**SetSearchCriteria** identifies the messages that match the specified restriction.</span></span> <span data-ttu-id="9fa01-112">The selected messages (the ones that satisfy the criteria) are displayed as links in the search-results folder.</span><span class="sxs-lookup"><span data-stu-id="9fa01-112">The selected messages (the ones that satisfy the criteria) are displayed as links in the search-results folder.</span></span> <span data-ttu-id="9fa01-113">When the client calls the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to access the contents table of the search-results folder, the selected messages are displayed in the table.</span><span class="sxs-lookup"><span data-stu-id="9fa01-113">When the client calls the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to access the contents table of the search-results folder, the selected messages are displayed in the table.</span></span> <span data-ttu-id="9fa01-114">Contents tables for search-results folders contain the same columns as contents tables for generic folders.</span><span class="sxs-lookup"><span data-stu-id="9fa01-114">Contents tables for search-results folders contain the same columns as contents tables for generic folders.</span></span> <span data-ttu-id="9fa01-115">Bei Suchergebnisordnern gibt die **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) den Eintragsbezeichner des Ordners an, in dem sich die verknüpfte Nachricht befindet.</span><span class="sxs-lookup"><span data-stu-id="9fa01-115">However, for search-results folders, the **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) property specifies the entry identifier of the folder where the linked message resides.</span></span> <span data-ttu-id="9fa01-116">Search-results folders are not considered parent folders.</span><span class="sxs-lookup"><span data-stu-id="9fa01-116">Search-results folders are not considered parent folders.</span></span>
  
<span data-ttu-id="9fa01-117">Suchergebnisse Ordner haben die folgenden Einschr�nkungen:</span><span class="sxs-lookup"><span data-stu-id="9fa01-117">Search-results folders have the following limits:</span></span>
  
- <span data-ttu-id="9fa01-p103">Durch einen Aufruf von **SetSearchCriteria** ist die einzige M�glichkeit, den Inhalt eines Ordners-Ergebnisse ge�ndert werden k�nnen. Weitere Informationen zur Implementierung von **SetSearchCriteria** finden Sie unter Knowledge Base-Artikel [260322: wie auf Suchordner mit der Methode SetSearchCriteria](https://go.microsoft.com/fwlink/?LinkId=123603).</span><span class="sxs-lookup"><span data-stu-id="9fa01-p103">The only way that the contents of a search-results folder can be modified is through a call to **SetSearchCriteria**. For more information about the implementation of **SetSearchCriteria**, see Knowledge Base article [260322: How To Search Folders with the SetSearchCriteria Method](https://go.microsoft.com/fwlink/?LinkId=123603).</span></span>
    
- <span data-ttu-id="9fa01-120">Nachrichten werden nicht in Suchergebnissen Ordner kopiert oder verschoben.</span><span class="sxs-lookup"><span data-stu-id="9fa01-120">Messages cannot be moved or copied into search-results folders.</span></span>
    
- <span data-ttu-id="9fa01-121">Suchergebnisse Ordner k�nnen keine Unterordner enthalten.</span><span class="sxs-lookup"><span data-stu-id="9fa01-121">Search-results folders cannot contain subfolders.</span></span> 
    
- <span data-ttu-id="9fa01-122">Clients einem Suchergebnisse Ordner des Betreffs einer Suche nicht m�glich.</span><span class="sxs-lookup"><span data-stu-id="9fa01-122">Clients cannot make a search-results folder the subject of a search.</span></span>
    
<span data-ttu-id="9fa01-p104">Es ist jedoch m�glich, zum �ndern der Eigenschaften eines Ordners Suchergebnisse und verwenden, um eine Nachricht zu l�schen. Wenn eine Nachricht aus einem Suchergebnisse Ordner gel�scht wird, wird es aus dem Ordner realen tats�chlich gel�scht. L�schen den Suchergebnisse Ordner selbst haben jedoch keine Auswirkungen auf die Nachrichten innerhalb; bleiben sie in ihren generischen Ordnern.</span><span class="sxs-lookup"><span data-stu-id="9fa01-p104">It is possible, however, to modify the properties of a search-results folder and use it to delete a message. When a message is deleted from a search-results folder, it is actually deleted from the real folder. However, deleting the search-results folder itself has no impact on the messages inside; they remain in their generic folders.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9fa01-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9fa01-126">See also</span></span>



[<span data-ttu-id="9fa01-127">MAPI-Ordner</span><span class="sxs-lookup"><span data-stu-id="9fa01-127">MAPI Folders</span></span>](mapi-folders.md)

