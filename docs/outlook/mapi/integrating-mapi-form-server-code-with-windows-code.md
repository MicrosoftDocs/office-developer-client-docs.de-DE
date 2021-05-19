---
title: Integrieren von MAPI-Formularservercode in Windows Code
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 47ec3e97-ad2b-43ea-842a-b2a0675eef48
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 33b205c0ac5caf5fc049a0732cd219aa2c321326
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332179"
---
# <a name="integrating-mapi-form-server-code-with-windows-code"></a><span data-ttu-id="76c9f-103">Integrieren von MAPI-Formularservercode in Windows Code</span><span class="sxs-lookup"><span data-stu-id="76c9f-103">Integrating MAPI Form Server Code with Windows Code</span></span>

  
  
<span data-ttu-id="76c9f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="76c9f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="76c9f-105">Denken Sie daran, dass ihr Formularserver eine Win32-Anwendung ist.</span><span class="sxs-lookup"><span data-stu-id="76c9f-105">Recall that your form server is a Win32 application.</span></span> <span data-ttu-id="76c9f-106">Es gibt also einige Aufgaben im Zusammenhang mit dem Laden des Formularservers in den Arbeitsspeicher und dem sauberen Beenden.</span><span class="sxs-lookup"><span data-stu-id="76c9f-106">As such, there are some tasks related to loading your form server into memory and exiting cleanly.</span></span> <span data-ttu-id="76c9f-107">Wie alle Windows ist der Einstiegspunkt für Ihren Formularserver die **WinMain-Funktion.**</span><span class="sxs-lookup"><span data-stu-id="76c9f-107">Like all Windows applications, the entry point for your form server is the **WinMain** function.</span></span> <span data-ttu-id="76c9f-108">Diese Funktion ist der geeignete Ort, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="76c9f-108">This function is the appropriate place to perform the following tasks:</span></span> 
  
- <span data-ttu-id="76c9f-109">Erstellen und Registrieren einer Fensterklasse, damit der Formularserver mit anderen OLE-Komponenten interagieren kann.</span><span class="sxs-lookup"><span data-stu-id="76c9f-109">Creating and registering a window class so that your form server can interact with other OLE components.</span></span>
    
- <span data-ttu-id="76c9f-110">Erstellen und Registrieren einer Fensterklasse oder -klassen für die Benutzeroberflächen ihrer Formularobjekte.</span><span class="sxs-lookup"><span data-stu-id="76c9f-110">Creating and registering a window class or classes for your form objects' user interfaces.</span></span>
    
- <span data-ttu-id="76c9f-111">Aufrufen der [MAPIInitialize-Funktion.](mapiinitialize.md)</span><span class="sxs-lookup"><span data-stu-id="76c9f-111">Calling the [MAPIInitialize](mapiinitialize.md) function.</span></span> <span data-ttu-id="76c9f-112">**MAPIInitialize** übernimmt auch die erforderliche OLE-Initialisierung für Sie.</span><span class="sxs-lookup"><span data-stu-id="76c9f-112">**MAPIInitialize** handles the required OLE initialization for you, as well.</span></span> <span data-ttu-id="76c9f-113">Dies muss einmal pro Instanz des Formularservers geschehen.</span><span class="sxs-lookup"><span data-stu-id="76c9f-113">This must be done once per instance of your form server.</span></span> 
    
- <span data-ttu-id="76c9f-114">Registrieren eines globalen Atoms mit einer Zeichenfolgendarstellung der Klassen-ID (CLSID) des Formularservers.</span><span class="sxs-lookup"><span data-stu-id="76c9f-114">Registering a global atom with a string representation of the form server's class identifier (CLSID).</span></span> <span data-ttu-id="76c9f-115">Dieses Atom sollte für die Lebensdauer des Formularservers vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="76c9f-115">This atom should exist for the lifetime of the form server.</span></span>
    
- <span data-ttu-id="76c9f-116">Aufrufen der [OLE-Funktion CoRegisterClassObject](https://msdn.microsoft.com/library/ms693407.aspx) zum Registrieren der Klassen factory ihres Formularservers bei OLE.</span><span class="sxs-lookup"><span data-stu-id="76c9f-116">Calling the OLE function [CoRegisterClassObject](https://msdn.microsoft.com/library/ms693407.aspx) to register your form server's class factory with OLE.</span></span> 
    
- <span data-ttu-id="76c9f-117">Erstellen eines Hauptfensters zum Empfangen von Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="76c9f-117">Creating a main window to receive messages.</span></span> <span data-ttu-id="76c9f-118">Dieses Fenster muss wahrscheinlich nicht angezeigt werden, da der Benutzer mit den spezifischen Fenstern interagiert, die einzelnen Formularobjekten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="76c9f-118">This window probably does not need to be visible because the user will be interacting with the specific windows associated with individual form objects.</span></span> <span data-ttu-id="76c9f-119">Während der Entwicklung kann das Hauptfenster jedoch ein bequemer Ort zum Debuggen der Ausgabe oder Steuerung des Formularservers sein.</span><span class="sxs-lookup"><span data-stu-id="76c9f-119">However, during development, the main window can be a convenient place for debugging output or control of your form server.</span></span>
    
- <span data-ttu-id="76c9f-120">Erstellen einer Nachrichtenschleife, die für die Lebensdauer des Formularservers ausgeführt wird, Übersetzen und Senden von Windows-Nachrichten an aktive Formularobjekte.</span><span class="sxs-lookup"><span data-stu-id="76c9f-120">Creating a message loop that runs for the lifetime of the form server, translating and dispatching windows messages to active form objects.</span></span>
    
<span data-ttu-id="76c9f-121">Wenn der Formularserver beendet wird, sollten die folgenden Aufgaben ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="76c9f-121">When your form server exits, it should perform the following tasks:</span></span>
  
- <span data-ttu-id="76c9f-122">Rufen Sie die OLE-Funktion [CoRevokeClassObject auf,](https://msdn.microsoft.com/library/ms688650%28VS.85%29.aspx) um die OLE-Registrierung Ihrer Nachrichtenklasse zu widerrufen.</span><span class="sxs-lookup"><span data-stu-id="76c9f-122">Call the OLE function [CoRevokeClassObject](https://msdn.microsoft.com/library/ms688650%28VS.85%29.aspx) to revoke your message class's OLE registration.</span></span> 
    
- <span data-ttu-id="76c9f-123">Rufen **Sie MAPIUninitialize auf,** um die Verbindung des Formularservers mit MAPI ordnungsgemäß zu schließen.</span><span class="sxs-lookup"><span data-stu-id="76c9f-123">Call **MAPIUninitialize** to properly close the form server's connection to MAPI.</span></span> 
    
- <span data-ttu-id="76c9f-124">Löschen Sie das globale Atom, das die Zeichenfolgendarstellung des Klassenbezeichners enthält.</span><span class="sxs-lookup"><span data-stu-id="76c9f-124">Delete the global atom that contains the string representation of the class identifier.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="76c9f-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76c9f-125">See also</span></span>



[<span data-ttu-id="76c9f-126">Schreiben von Formularservercode</span><span class="sxs-lookup"><span data-stu-id="76c9f-126">Writing Form Server Code</span></span>](writing-form-server-code.md)

