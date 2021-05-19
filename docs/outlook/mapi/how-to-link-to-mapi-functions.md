---
title: Verweisen auf MAPI-Funktionen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be72a893-a3bc-4dea-8234-47f3e1db4515
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 71108da8bb9914bb7ed0ad0b3adacc24e1d69e63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346883"
---
# <a name="link-to-mapi-functions"></a><span data-ttu-id="1d43e-103">Verweisen auf MAPI-Funktionen</span><span class="sxs-lookup"><span data-stu-id="1d43e-103">Link to MAPI functions</span></span>

<span data-ttu-id="1d43e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1d43e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1d43e-105">Es gibt drei Methoden zum Verknüpfen: implizite Verknüpfung, explizite Verknüpfung und ein neues Hybridmodell mithilfe der MAPI-Stubbibliothek.</span><span class="sxs-lookup"><span data-stu-id="1d43e-105">There are three methods of linking: implicit linking, explicit linking, and a new hybrid model using the MAPI Stub Library.</span></span>
  
## <a name="implicit-linking"></a><span data-ttu-id="1d43e-106">Implizite Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="1d43e-106">Implicit linking</span></span>

<span data-ttu-id="1d43e-107">In der Vergangenheit war beim Aufrufen von MAPI-Funktionen in einer Messaginganwendung immer die Verknüpfung mit der Mapi32.lib-Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1d43e-107">Historically, calling MAPI functions in a messaging application always involved linking to the Mapi32.lib library.</span></span> <span data-ttu-id="1d43e-108">Dazu gehörten Routing-MAPI-Aufrufe an die Windows-MAPI-Stubbibliothek Mapi32.dll, die die Aufrufe dann zur Laufzeit an die standardmäßige MAPI-Clientimplementierung weiterleitet.</span><span class="sxs-lookup"><span data-stu-id="1d43e-108">This included routing MAPI calls to the Windows MAPI stub library, Mapi32.dll, which then forwarded the calls to the default MAPI client implementation at run time.</span></span> <span data-ttu-id="1d43e-109">Dieser Aufrufprozess wird als implizite Verknüpfung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1d43e-109">This call process is known as implicit linking.</span></span> <span data-ttu-id="1d43e-110">Die linke Seite der folgenden Abbildung zeigt ein Beispiel für implizite Verknüpfungen, die in einem Aufrufprozess für MAPI-Funktionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1d43e-110">The left side of the following figure shows an example of implicit linking used in a MAPI function call process.</span></span> <span data-ttu-id="1d43e-111">Der Prozess wird von einer MAPI-Anwendung initiiert und umfasst die MAPI-Bibliothek (Mapi32.lib) und den Windows-MAPI-Stub (Mapi32.dll) und wird durch die Outlook-MAPI-Clientimplementierung des MAPI-Stubs (Msmapi32.dll) abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="1d43e-111">The process is initiated by a MAPI application and involves the MAPI library (Mapi32.lib) and the Windows MAPI stub (Mapi32.dll) and is completed by the Outlook MAPI client implementation of the MAPI stub (Msmapi32.dll).</span></span>
  
<span data-ttu-id="1d43e-112">**Vergleich der impliziten und expliziten Verknüpfung.**</span><span class="sxs-lookup"><span data-stu-id="1d43e-112">**Comparison of implicit and explicit linking.**</span></span>

<span data-ttu-id="1d43e-113">![Vergleich der impliziten und expliziten Verknüpfung](media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "Vergleich der impliziten und expliziten Verknüpfung")</span><span class="sxs-lookup"><span data-stu-id="1d43e-113">![Comparison of implicit and explicit linking](media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "Comparison of implicit and explicit linking")</span></span>
  
## <a name="explicit-linking"></a><span data-ttu-id="1d43e-114">Explizite Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="1d43e-114">Explicit linking</span></span>

<span data-ttu-id="1d43e-115">Da der standardmäßige MAPI-Client die On-Demand-Installation mithilfe des Windows Installer (MSI) unterstützt, können Sie Messaginganwendungen direkt im Outlook-MAPI-Stub entwickeln, anstatt die MAPI-Bibliothek und den Windows zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1d43e-115">Because the default MAPI client supports on-demand installation using the Windows Installer (MSI), you can develop messaging applications directly on the Outlook MAPI stub instead of using the MAPI library and Windows MAPI stub.</span></span> <span data-ttu-id="1d43e-116">Die rechte Seite der vorherigen Abbildung zeigt ein Beispiel für einen AUFRUFprozess der MAPI-Funktion, beginnend mit einer MAPI-Anwendung, die nach dem Pfad und dem DLL-Namen für den Outlook-MAPI-Stub sucht (Schritt 2 im folgenden Abschnitt), und das Aufrufen von Funktionsaufrufen in den Outlook-MAPI-Stub (Schritt 3 im folgenden Abschnitt).</span><span class="sxs-lookup"><span data-stu-id="1d43e-116">The right side of the previous figure shows an example of a MAPI function call process, starting with a MAPI application looking for the path and DLL name for the Outlook MAPI stub (step 2 in the following section), and making function calls into the Outlook MAPI stub (step 3 in the following section).</span></span> <span data-ttu-id="1d43e-117">Im folgenden Verfahren wird gezeigt, wie Sie MAPI-Funktionen mithilfe expliziter Verknüpfungen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1d43e-117">The following procedure shows how to call MAPI functions by using explicit linking.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1d43e-118">Diese Informationen zur expliziten Verknüpfung sind möglicherweise überflüssig für Ihre Anforderungen mit der Einführung der MAPIStubLibrary.lib, die im folgenden Abschnitt erläutert wird.</span><span class="sxs-lookup"><span data-stu-id="1d43e-118">This information about explicit linking may be superfluous to your needs with the introduction of the MAPIStubLibrary.lib discussed in the following section.</span></span> <span data-ttu-id="1d43e-119">Wie das implizite Modell verwaltet die neue Bibliothek alles und implementiert die explizite Verknüpfungslogik, die Outlook MAPI direkt lädt.</span><span class="sxs-lookup"><span data-stu-id="1d43e-119">Like the implicit model, the new library manages everything and implements the explicit linking logic that loads Outlook's MAPI directly.</span></span> 
  
<span data-ttu-id="1d43e-120">Weitere Informationen zu expliziten Verknüpfungen finden Sie unter Linking Explicitly.</span><span class="sxs-lookup"><span data-stu-id="1d43e-120">For more information about explicit linking, see Linking Explicitly.</span></span>
  
### <a name="to-call-mapi-api-elements-without-the-mapi-library-and-the-windows-mapi-stub"></a><span data-ttu-id="1d43e-121">So rufen Sie MAPI-API-Elemente ohne die MAPI-Bibliothek und den Windows-MAPI-Stub auf</span><span class="sxs-lookup"><span data-stu-id="1d43e-121">To call MAPI API elements without the MAPI library and the Windows MAPI stub</span></span>

1. <span data-ttu-id="1d43e-122">Erstellen Sie in Ihrer Programmdatei eine globale Liste von Funktionszeigern für jedes von Ihnen verwendete MAPI-API-Element.</span><span class="sxs-lookup"><span data-stu-id="1d43e-122">In your program file, create a global list of function pointers for each MAPI API element that you are using.</span></span> 
    
   <span data-ttu-id="1d43e-123">Das folgende Beispiel zeigt diesen Schritt.</span><span class="sxs-lookup"><span data-stu-id="1d43e-123">The following example shows this step.</span></span>
    
   ```cpp
    //Global MAPI function pointers
    LPMAPIINITIALIZE pfnMAPIInitialize = NULL;
    LPMAPIUNINITIALIZE pfnMAPIUninitialize = NULL;
   ```

2. <span data-ttu-id="1d43e-124">Erstellen Sie eine Funktion, die MAPI-Funktionen initialisiert, um eine Verknüpfung mit der MAPI-DLL des standardmäßigen MAPI-Clients (z. B. Msmapi32.dll von Microsoft Outlook).</span><span class="sxs-lookup"><span data-stu-id="1d43e-124">Create a function that initializes MAPI functions to link to the MAPI DLL of the default MAPI client (for example, Msmapi32.dll of Microsoft Outlook).</span></span> <span data-ttu-id="1d43e-125">Gehen Sie in dieser Funktion wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="1d43e-125">In this function, do the following:</span></span> 
    
    1. <span data-ttu-id="1d43e-126">Laden mapi32.dll aus dem entsprechenden Systemverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="1d43e-126">Load mapi32.dll from the appropriate system directory.</span></span> 
        
       |||
       |:-----|:-----|
       |<span data-ttu-id="1d43e-127">x64 oder x86 nativ</span><span class="sxs-lookup"><span data-stu-id="1d43e-127">x64 or x86 natively</span></span>  <br/> |<span data-ttu-id="1d43e-128">**%windir%\system32\mapi32.dll**</span><span class="sxs-lookup"><span data-stu-id="1d43e-128">**%windir%\system32\mapi32.dll**</span></span> <br/> |
       |<span data-ttu-id="1d43e-129">x86 im WoW-Modus</span><span class="sxs-lookup"><span data-stu-id="1d43e-129">x86 on WoW mode</span></span>  <br/> |<span data-ttu-id="1d43e-130">**%windir%\syswow64\mapi32.dll**</span><span class="sxs-lookup"><span data-stu-id="1d43e-130">**%windir%\syswow64\mapi32.dll**</span></span> <br/> |
    
    2. <span data-ttu-id="1d43e-131">Rufen Sie [die FGetComponentPath-Funktion auf,](fgetcomponentpath.md) um den Pfad und den DLL-Namen zu erhalten, der das MAPI-Subsystem implementiert.</span><span class="sxs-lookup"><span data-stu-id="1d43e-131">Call the [FGetComponentPath](fgetcomponentpath.md) function to get the path and DLL name that implements the MAPI subsystem.</span></span> <span data-ttu-id="1d43e-132">Weitere Informationen finden Sie unter [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md).</span><span class="sxs-lookup"><span data-stu-id="1d43e-132">For more information, see [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md).</span></span>
        
    3. <span data-ttu-id="1d43e-133">Laden Sie die DLL, indem Sie die LoadLibrary-Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1d43e-133">Load the DLL by calling the LoadLibrary function.</span></span> 
        
    4. <span data-ttu-id="1d43e-134">Initialisieren Sie das MAPI-Funktionszeigerarray, indem Sie die GetProcAddress-Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1d43e-134">Initialize the MAPI function pointer array by calling the GetProcAddress function.</span></span> 
        
    <span data-ttu-id="1d43e-135">Das folgende Beispiel zeigt die vorherigen Schritte:</span><span class="sxs-lookup"><span data-stu-id="1d43e-135">The following example shows the previous steps:</span></span>
        
   ```cpp
    void InitializeMapiFunctions()
    {
    {
        // Get the DLL path and name of the actual MAPI implementation.
        FGetComponentPath(g_szMapiComponentGUID, NULL, szMAPIDLL, MAX_PATH);
        // Load the DLL.
        hMod = LoadLibrary(szMAPIDLL);
        // Initialize MAPI functions.
        pfnMAPIInitialize = GetProcAddress(hMod, "MAPIInitialize");
        pfnMAPIUninitialize = GetProcAddress(hMod, "MAPIUninitialize");
    }
   ```

3. <span data-ttu-id="1d43e-136">Rufen Sie schließlich die Funktion auf, die Sie in Schritt 2 in Ihrer Messaginganwendung erstellt haben, bevor Sie Aufrufe von MAPI-API-Elementen starten.</span><span class="sxs-lookup"><span data-stu-id="1d43e-136">Finally, call the function that you created in step 2 in your messaging application before you make calls to MAPI API elements.</span></span> 
    
   > [!CAUTION]
   > <span data-ttu-id="1d43e-137">Sie müssen die Initialisierung des MAPI-Subsystems vor dem Schließen der Anwendung uninitialisieren.</span><span class="sxs-lookup"><span data-stu-id="1d43e-137">You must uninitialize the MAPI subsystem before closing your application.</span></span> 
  
   <span data-ttu-id="1d43e-138">Das folgende Beispiel zeigt diesen Schritt:</span><span class="sxs-lookup"><span data-stu-id="1d43e-138">The following example shows this step:</span></span> 
    
   ```cpp
    int main()
    {
        HRESULT hr;
        InitializeMapiFunctions();
        // Initialize the MAPI subsystem.
        hr = (*pfnMAPIInitialize)(NULL);
        if (hr!= S_OK)
        {
            // Handle the error case.
        }
        // Here is where you make calls to other MAPI interfaces.
        // Uninitialize the MAPI subsystem.
        (*pfnMAPIUninitialize)();
    return (0);
    }
   ```

## <a name="mapistublibrarylib"></a><span data-ttu-id="1d43e-139">MAPIStubLibrary.lib</span><span class="sxs-lookup"><span data-stu-id="1d43e-139">MAPIStubLibrary.lib</span></span>

<span data-ttu-id="1d43e-140">Die Einführung Microsoft Outlook 2010 und 64-Bit-MAPI, die nun auf die Microsoft Outlook 2013 erweitert wird, erfordert mehr als die herkömmliche 32-Bit-API für die vollständige Implementierung.</span><span class="sxs-lookup"><span data-stu-id="1d43e-140">The advent of Microsoft Outlook 2010 and 64-bit MAPI, now extending to the Microsoft Outlook 2013, requires more than the traditional 32-bit API for full implementation.</span></span> <span data-ttu-id="1d43e-141">Ein neues Projekt, die MAPI-Stubbibliothek, das auf der CodePlex-Website veröffentlicht wird, bietet einen Drop-In-Ersatz für Mapi32.lib, das das Erstellen von 32-Bit- und 64-Bit-MAPI-Anwendungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1d43e-141">A new project, the MAPI Stub Library, posted on the CodePlex website provides a drop-in replacement for Mapi32.lib that supports building both 32-bit and 64-bit MAPI applications.</span></span> <span data-ttu-id="1d43e-142">MAPIStubLibrary.lib entfällt die Notwendigkeit, explizit mit MAPI zu verknüpfen, und nachdem Sie sie erstellt haben, können Sie Mapi32.lib aus Ihren Linkereinstellungen entfernen und durch MAPIStubLibrary.lib ersetzen. Es sollten keine weiteren Änderungen am Code erforderlich sein.</span><span class="sxs-lookup"><span data-stu-id="1d43e-142">MAPIStubLibrary.lib eliminates the need to explicitly link to MAPI, and having built it, you can remove Mapi32.lib from your linker settings, replacing it with MAPIStubLibrary.lib; no further modifications to your code should be needed.</span></span> <span data-ttu-id="1d43e-143">Außerdem ist es nicht **erforderlich, LoadLibrary-,** **GetProcAddress-** und **FreeLibrary-Code** zu schreiben, um neuere Exporte zu verarbeiten, die in dieser Bibliotheksdatei enthalten sind, jedoch nicht in Mapi32.lib, was bei Verwendung expliziter Verknüpfungen erforderlich wäre.</span><span class="sxs-lookup"><span data-stu-id="1d43e-143">It also eliminates the need to write **LoadLibrary**, **GetProcAddress**, and **FreeLibrary** code to handle newer exports included in this library file but not in Mapi32.lib, which would be needed if you used explicit linking.</span></span> 
  
<span data-ttu-id="1d43e-144">Einige der neuen Funktionen, die mit dieser Bibliothek verknüpft sind, die in Mapi32.lib nicht verfügbar sind, umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="1d43e-144">Some of the new functions linked from this library that are not available in Mapi32.lib include the following:</span></span>
  
- [<span data-ttu-id="1d43e-145">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="1d43e-145">GetDefCachedMode</span></span>](getdefcachedmode.md)    
- [<span data-ttu-id="1d43e-146">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="1d43e-146">HrGetGALFromEmsmdbUID</span></span>](hrgetgalfromemsmdbuid.md)   
- [<span data-ttu-id="1d43e-147">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="1d43e-147">HrOpenOfflineObj</span></span>](hropenofflineobj.md)    
- [<span data-ttu-id="1d43e-148">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="1d43e-148">MAPICrashRecovery</span></span>](mapicrashrecovery.md)   
- [<span data-ttu-id="1d43e-149">OpenStreamOnFileW</span><span class="sxs-lookup"><span data-stu-id="1d43e-149">OpenStreamOnFileW</span></span>](openstreamonfilew.md)    
- [<span data-ttu-id="1d43e-150">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="1d43e-150">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)
    
<span data-ttu-id="1d43e-151">Eine alternative Methode zum Integrieren der MAPI-Stubbibliothek besteht im Kopieren der Quelldateien MapiStubLibrary.cpp und StubUtils.cpp direkt in Ihr Projekt, und entfernen Sie alle Verknüpfungen mit Mapi32.lib und code, der explizit mit MAPI verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="1d43e-151">An alternate method of incorporating the MAPI Stub Library is to copy the source files, MapiStubLibrary.cpp and StubUtils.cpp, directly into your project and remove any linkage to Mapi32.lib and any code that explicitly links to MAPI.</span></span>
  
<span data-ttu-id="1d43e-152">Informationen zum Zugriff auf die MAPI-Stubbibliotheksdateien und Informationen zum Erstellen und Integrieren in Ihr Projekt sowie Fragen zu dieser Bibliothek, z. B. wann und warum sie verwendet werden sollen, finden Sie in der [MAPI-Stubbibliothek](https://mapistublibrary.codeplex.com/documentation) auf der CodePlex-Website.</span><span class="sxs-lookup"><span data-stu-id="1d43e-152">To access the MAPI Stub Library files and for information about how to build and integrate it into your project, as well as questions about this library such as when and why to use it, see the [MAPI Stub Library](https://mapistublibrary.codeplex.com/documentation) on the CodePlex site.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1d43e-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d43e-153">See also</span></span>

- [<span data-ttu-id="1d43e-154">Übersicht über die MAPI-Programmierung</span><span class="sxs-lookup"><span data-stu-id="1d43e-154">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
- [<span data-ttu-id="1d43e-155">Installieren des MAPI-Subsystems</span><span class="sxs-lookup"><span data-stu-id="1d43e-155">Installing the MAPI Subsystem</span></span>](installing-the-mapi-subsystem.md)
- [<span data-ttu-id="1d43e-156">Installieren von MAPI-Headerdateien</span><span class="sxs-lookup"><span data-stu-id="1d43e-156">Install MAPI Header Files</span></span>](how-to-install-mapi-header-files.md)
- [<span data-ttu-id="1d43e-157">Auswählen einer bestimmten Version der zu ladende MAPI</span><span class="sxs-lookup"><span data-stu-id="1d43e-157">Choose a Specific Version of MAPI to Load</span></span>](how-to-choose-a-specific-version-of-mapi-to-load.md)
- [<span data-ttu-id="1d43e-158">Bestimmen der zu verwendenden Verknüpfungsmethode</span><span class="sxs-lookup"><span data-stu-id="1d43e-158">Determining Which Linking Method to Use</span></span>](https://msdn.microsoft.com/library/253b8k2c.aspx)
- [<span data-ttu-id="1d43e-159">Verknüpfen einer ausführbaren Datei mit einer DLL</span><span class="sxs-lookup"><span data-stu-id="1d43e-159">Linking an Executable to a DLL</span></span>](https://msdn.microsoft.com/library/9yd93633.aspx)
- [<span data-ttu-id="1d43e-160">Einrichten der MSI-Schlüssel für Ihre MAPI-DLL</span><span class="sxs-lookup"><span data-stu-id="1d43e-160">Setting Up the MSI Keys for Your MAPI DLL</span></span>](https://msdn.microsoft.com/library/ee909494%28v=VS.85%29.aspx)

