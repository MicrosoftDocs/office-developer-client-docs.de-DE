---
title: Office für Android-Unterstützung für Android Storage Access Framework
manager: soliver
ms.date: 06/18/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9cfed295-f499-44dc-bac5-9e266df1b5b3
description: Office für Android lässt sich in Android Storage Access Framework integrieren, mit dem Office Dateien öffnen kann, die von einem anderen Dokumentanbieter gespeichert werden.
ms.openlocfilehash: 24d7e48106aeb5e58a668b94cbde00eaa9175230
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300350"
---
# <a name="office-for-android-support-for-the-android-storage-access-framework"></a><span data-ttu-id="5a7d6-103">Office für Android-Unterstützung für Android Storage Access Framework</span><span class="sxs-lookup"><span data-stu-id="5a7d6-103">Office for Android support for the Android Storage Access Framework</span></span>

<span data-ttu-id="5a7d6-104">Office für Android lässt sich in Android Storage Access Framework integrieren, mit dem Office Dateien öffnen kann, die von einem anderen Dokumentanbieter gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="5a7d6-104">Office for Android integrates with the Android Storage Access Framework, which enables Office to open files stored by another document provider.</span></span>
  
<span data-ttu-id="5a7d6-p101">In Android 4.4 (API Level 19) wird das Storage Access Framework (SAF) eingeführt. Mit SAF können Benutzer Dokumente, Bilder und andere Dateien durchsuchen und öffnen, die von den bevorzugten Dokumentspeicheranbieter gespeichert sind. Mit der Standard-Benutzeroberfläche können Benutzer Dateien auf konsistente Weise App- und Anbieter-übergreifend durchsuchen und auf diese zugreifen.</span><span class="sxs-lookup"><span data-stu-id="5a7d6-p101">Android 4.4 (API level 19) introduces the Storage Access Framework (SAF). The SAF enables users to browse and open documents, images, and other files across all their preferred document storage providers. A standard UI lets users browse files and access them in a consistent way across apps and providers.</span></span>
  
## <a name="implement-a-document-provider"></a><span data-ttu-id="5a7d6-108">Implementieren eines Dokumentanbieters</span><span class="sxs-lookup"><span data-stu-id="5a7d6-108">Implement a document provider</span></span>

<span data-ttu-id="5a7d6-p102">Wenn Sie eine App entwickeln, die Speicherdienste für Dokumente bereitstellt, können Sie Ihre Dateien über SAF durch [Schreiben eines benutzerdefinierten Dokumentanbieters](https://developer.android.com/guide/topics/providers/document-provider.html) zur Verfügung stellen. Office-Apps können dann die [ACTION_OPEN_DOCUMENT ](https://developer.android.com/reference/android/content/Intent.html)- und/oder [ACTION_CREATE_DOCUMENT ](https://developer.android.com/reference/android/content/Intent.html)-Absicht zum Empfangen der Dateien aufrufen, die von Ihrem Dokumentanbieter zurückgegeben wurden. Beachten Sie, dass die Absicht Filter zum weiteren Verfeinern der Kriterien enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="5a7d6-p102">If you're developing an app that provides storage services for documents, you can make your files available through the SAF by [writing a custom document provider](https://developer.android.com/guide/topics/providers/document-provider.html). Office apps can then invoke the [ACTION_OPEN_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html) and/or [ACTION_CREATE_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html) intent to receive the files returned by your document provider. Note that the intent might include filters to further refine the criteria.</span></span> 
  
## <a name="enable-free-consumer-edits"></a><span data-ttu-id="5a7d6-112">Aktivieren der kostenlosen Bearbeitung</span><span class="sxs-lookup"><span data-stu-id="5a7d6-112">Enable free consumer edits</span></span>

<span data-ttu-id="5a7d6-p103">Benutzer können sich mit einem kostenlosen Microsoft-Konto bei Office-Apps anmelden, um Dokumente zu erstellen oder zu bearbeiten, die in einem benutzerorientierten Speicherdienst gespeichert sind. In der folgenden Tabelle werden die obligatorischen Eigenschaften aufgeführt, die Anbieter im Rahmen des Cursors bereitstellen müssen, um die kostenlose Bearbeitung der über das Storage Access Framework zugegriffenen Dokumenten zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="5a7d6-p103">Users can sign in to the Office apps with a free Microsoft account to create or edit docs that are stored in a consumer-oriented storage service. The following table lists the mandatory properties that providers must supply as part of the cursor, to enable free consumer edit for documents accessed via the Storage Access Framework.</span></span>
  
|<span data-ttu-id="5a7d6-115">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="5a7d6-115">**Property**</span></span>|<span data-ttu-id="5a7d6-116">**Index**</span><span class="sxs-lookup"><span data-stu-id="5a7d6-116">**Index**</span></span>|<span data-ttu-id="5a7d6-117">**Wert**</span><span class="sxs-lookup"><span data-stu-id="5a7d6-117">**Value**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5a7d6-118">Dokumenttyp</span><span class="sxs-lookup"><span data-stu-id="5a7d6-118">Document Type</span></span>  <br/> |<span data-ttu-id="5a7d6-119">com_microsoft_office_doctype</span><span class="sxs-lookup"><span data-stu-id="5a7d6-119">com_microsoft_office_doctype</span></span>  <br/> |<span data-ttu-id="5a7d6-120">\<Benutzer\></span><span class="sxs-lookup"><span data-stu-id="5a7d6-120">\<consumer\></span></span>  <br/> |
|<span data-ttu-id="5a7d6-121">Anzeigename des Dienstes</span><span class="sxs-lookup"><span data-stu-id="5a7d6-121">Service Friendly Name</span></span>  <br/> |<span data-ttu-id="5a7d6-122">com_microsoft_office_servicename</span><span class="sxs-lookup"><span data-stu-id="5a7d6-122">com_microsoft_office_servicename</span></span>  <br/> |<span data-ttu-id="5a7d6-p104">Ein beliebiger benutzerfreundlicher Name für den Dienst, der zum Identifizieren eines Dokuments in der Liste der zuletzt geöffneten Dokumente in Office-Apps verwendet wird. Beachten Sie, dass die Eigenschaft für Lizenzbedingungen angegeben werden muss, bevor der Anzeigename für den Dienst angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5a7d6-p104">Any user-friendly name for the service, used to identify a document in the Recent list in the Office apps. Note that the "Terms of Use Agreement" property must be supplied before the friendly name for the service can be displayed.</span></span>  <br/> |
|<span data-ttu-id="5a7d6-125">Nutzungsbedingungen</span><span class="sxs-lookup"><span data-stu-id="5a7d6-125">Terms of Use Agreement</span></span>  <br/> |<span data-ttu-id="5a7d6-126">com_microsoft_office_termsofuse</span><span class="sxs-lookup"><span data-stu-id="5a7d6-126">com_microsoft_office_termsofuse</span></span>  <br/> |<span data-ttu-id="5a7d6-127">\<Ich stimme den Nutzungsbedingungen unter https://go.microsoft.com/fwlink/p/?LinkId=528381\> zu.</span><span class="sxs-lookup"><span data-stu-id="5a7d6-127">\<I agree to the terms located at https://go.microsoft.com/fwlink/p/?LinkId=528381\></span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5a7d6-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a7d6-128">See also</span></span>
<span data-ttu-id="5a7d6-129"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="5a7d6-129"><a name="bk_addresources"> </a></span></span>

- [<span data-ttu-id="5a7d6-130">Integration in Office</span><span class="sxs-lookup"><span data-stu-id="5a7d6-130">Integrate with Office</span></span>](integrate-with-office.md)
    
- [<span data-ttu-id="5a7d6-131">Grundlagen für Inhaltsanbieter</span><span class="sxs-lookup"><span data-stu-id="5a7d6-131">Content Provider Basics</span></span>](hhttps://developer.android.com/guide/topics/providers/content-provider-basics.html)
    
- [<span data-ttu-id="5a7d6-132">Erstellen eines Inhaltsanbieters</span><span class="sxs-lookup"><span data-stu-id="5a7d6-132">Creating a Content Provider</span></span>](https://developer.android.com/guide/topics/providers/content-provider-creating.html)
    
- [<span data-ttu-id="5a7d6-133">Storage Access Framework - Entwicklerhandbuch</span><span class="sxs-lookup"><span data-stu-id="5a7d6-133">Storage Access Framework Developer Guide</span></span>](https://developer.android.com/guide/topics/providers/document-provider.html)
    

