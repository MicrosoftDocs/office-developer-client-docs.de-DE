---
title: Entwickeln einer Project Online-Anwendung mit dem clientseitigen Objektmodell
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5740d0b2-5d36-40e4-9e83-577cb186359f
description: In diesem Artikel wird beschrieben, Microsoft Project Online Anwendungsentwicklung für desktopanwendungen mit .NET Framework 4.0. Die Anwendung, die in diesem Artikel beschriebenen Ruft Informationen aus dem Hostserver.
ms.openlocfilehash: a0a2b4042d4db127c56c5ba873ebe25418344571
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796187"
---
# <a name="developing-a-project-online-application-using-the-client-side-object-model"></a><span data-ttu-id="b8b5e-104">Entwickeln einer Project Online-Anwendung mit dem clientseitigen Objektmodell</span><span class="sxs-lookup"><span data-stu-id="b8b5e-104">Developing a Project Online application using the client-side object model</span></span>

<span data-ttu-id="b8b5e-105">In diesem Artikel wird beschrieben, Microsoft Project Online Anwendungsentwicklung für desktopanwendungen mit .NET Framework 4.0.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-105">This article describes Microsoft Project Online application development for desktop applications using the .NET Framework 4.0.</span></span> <span data-ttu-id="b8b5e-106">Die Anwendung, die in diesem Artikel beschriebenen Ruft Informationen aus dem Hostserver.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-106">The application described in this article retrieves information from the hosting server.</span></span> 
  
## <a name="background"></a><span data-ttu-id="b8b5e-107">Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b8b5e-107">Background</span></span>

<span data-ttu-id="b8b5e-108">Microsoft Project als desktop-Anwendung in der frühen 1990er gestartet.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-108">Microsoft Project started as desktop application in the early 1990's.</span></span> <span data-ttu-id="b8b5e-109">Heute ist Project vieles Weitere abschließen, die mehrere Varianten:</span><span class="sxs-lookup"><span data-stu-id="b8b5e-109">Today, Project is much more, as its several varieties attest:</span></span>
  
- <span data-ttu-id="b8b5e-110">Project standard Edition ist eine desktop-Anwendung, die als eigenständige Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-110">Project standard edition is a desktop application that runs as a stand-alone application.</span></span>
    
- <span data-ttu-id="b8b5e-111">Project professional Edition ist eine desktop-Anwendung, die kann interagieren und Daten gemeinsam mit einem Server in einem größeren Ausmaß als auch die Funktionalität in Project standard Edition ausführen.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-111">Project professional edition is a desktop application that can interact and share data with a server on a larger scale, as well as perform the functionality found in Project standard edition.</span></span>
    
- <span data-ttu-id="b8b5e-112">Project Online ist ein Microsoft-gehosteten Dienst, der bietet Unternehmen eine Lösung auf Dokumentebene PMO koordinieren und Verwalten von Projekten, Programme und Portfolios.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-112">Project Online is a Microsoft-hosted service that provides companies with a PMO-level solution to coordinate and manage projects, programs, and portfolios.</span></span> <span data-ttu-id="b8b5e-113">Eine andere besser als desktop-Editionen, Project Online warten und Nachverfolgen von Projektdetails im Lebenszyklus eines Projekts kann.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-113">A different offering than the desktop editions, Project Online can maintain and track project details throughout the life of a project.</span></span> 
    
- <span data-ttu-id="b8b5e-114">Projektserver ist eine Enterprise-gehosteten Dienst in dem Unternehmen verwaltet und sichert den Server, Project, Anwendung und Portfolio Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-114">Project Server is an enterprise-hosted service in which the enterprise manages and secures the server containing project, program, and portfolio information.</span></span> <span data-ttu-id="b8b5e-115">Projektserver nach der Sicherung des Servers internes bietet Projekt-, Anwendung und Portfolio orientierten Features von extern gehosteten Project Online mit eine höhere Kapazität für die Anpassung.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-115">Project Server, by virtue of securing the server in-house, offers the project, program, and portfolio oriented features of externally-hosted Project Online with a greater capacity for customization.</span></span>
    
<span data-ttu-id="b8b5e-116">Project Online hat drei online API-Sätze: mithilfe der clientseitigen Objekt Objektmodell (CSOM), JavaScript-Objektmodell (JSOM) und Representational State Transfer (REST).</span><span class="sxs-lookup"><span data-stu-id="b8b5e-116">Project Online has three online API sets: Client-side Object Model (CSOM), JavaScript Object Model (JSOM), and Representational State Transfer (REST).</span></span> 
  
- <span data-ttu-id="b8b5e-117">Die .NET CSOM-Implementierung ist die bevorzugte Schnittstelle beim Entwickeln von Windows-Anwendungen, die interagieren mit Project Online-Mandanten.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-117">The .NET CSOM implementation is the preferred interface when developing Windows applications that interact with Project Online tenants.</span></span> <span data-ttu-id="b8b5e-118">Typische Umgebung für die Benutzer-centric Applications gehören Desktops unter Windows und Microsoft Surface Geräte.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-118">Typical environments for user-centric applications include Windows desktops and Microsoft Surface devices.</span></span> <span data-ttu-id="b8b5e-119">Back-End-Clientanwendungen mit .NET CSOM geschrieben können mit anderen Servern für Business Logic und Datenquellen eine Verbindung herstellen, die externe mit Project Online sind.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-119">Back-end applications written with .NET CSOM can connect to other servers for business logic and data sources that are external to Project Online.</span></span> <span data-ttu-id="b8b5e-120">Abruf Anfragen zu Project Online verwenden Sie ein LINQ-ähnliche Abfrage, die mehrere Verbesserungen über grundlegende Retrieval Funktionen bietet.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-120">Retrieval requests to Project Online use a LINQ-like query system that offers several enhancements over basic retrieval functions.</span></span>
    
- <span data-ttu-id="b8b5e-121">Die JavaScript-Objektmodell (JSOM)-Schnittstelle bietet Browserübergreifende Unterstützung für Project Online-Add-ins. Ein Add-in ist eine Anwendung, die in Project Online-Mandanten gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-121">The JavaScript Object Model (JSOM) interface provides cross-browser support for Project Online Add-ins. An add-in is a web application that is stored in the Project Online tenant.</span></span> <span data-ttu-id="b8b5e-122">Wenn ein Benutzer ein Add-in ausführen möchte, wird der Code für das Add-in-downloads und im Browser auf dem Computer des Benutzers ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-122">When a user wants to run an add-in, the code for the add-in downloads and runs in the browser on the user machine.</span></span> 
    
- <span data-ttu-id="b8b5e-123">Details des Modells REST/Odata-HTTP-basierte Kommunikation bereitstellt, wird diese Schnittstelle für Applikationen in nicht-Windows-Umgebungen empfohlen.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-123">The REST/Odata model provides HTTP-based communication, This interface is recommended for applications in non-Windows environments.</span></span> <span data-ttu-id="b8b5e-124">Kommunikationsendpunkten sind die Objekte in der Website für die Project Web Application (PWA).</span><span class="sxs-lookup"><span data-stu-id="b8b5e-124">Communication endpoints are the objects in the Project Web Application (PWA) site.</span></span> <span data-ttu-id="b8b5e-125">Ergebnisse liefern normalen HTTP-Statuscodes.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-125">Results provide normal HTTP status codes.</span></span>
    
<span data-ttu-id="b8b5e-126">Dieser Artikel befasst sich eine Anwendung, die die .NET CSOM-Schnittstelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-126">This article focuses on an application that uses the .NET CSOM interface.</span></span>
  
## <a name="prerequisites"></a><span data-ttu-id="b8b5e-127">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="b8b5e-127">Prerequisites</span></span>

<span data-ttu-id="b8b5e-128">Starten Sie mit einem Basis-System mit Windows 10, und fügen Sie die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="b8b5e-128">Start with a base system running Windows 10, and add the following items:</span></span>
  
- <span data-ttu-id="b8b5e-129">.NET Framework 4.0 oder höher – verwenden Sie das vollständige Framework.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-129">.Net Framework 4.0 or later -- Use the complete framework.</span></span> <span data-ttu-id="b8b5e-130">Die Download-Website ist https://msdn.microsoft.com/en-us/vstudio/aa496123.aspx.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-130">The download site is https://msdn.microsoft.com/en-us/vstudio/aa496123.aspx.</span></span>
    
- <span data-ttu-id="b8b5e-131">Visual Studio 2013 oder höher--Edition ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-131">Visual Studio 2013 or later -- Any edition is acceptable.</span></span> <span data-ttu-id="b8b5e-132">Die Community-Edition von Visual Studio 2015 wurde verwendet, um die beispielanwendung aus zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-132">The community edition of Visual Studio 2015 was used to develop the sample application.</span></span> <span data-ttu-id="b8b5e-133">Die Community Edition steht unter https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-133">The community edition is available at https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.</span></span>
    
- <span data-ttu-id="b8b5e-134">SharePoint-Clientkomponenten SDK – Project Online und Project Server sit auf der Basis SharePoint und SharePoint-Assemblys.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-134">SharePoint Client Components SDK -- Project Online and Project Server sit on top of SharePoint, and SharePoint assemblies.</span></span> <span data-ttu-id="b8b5e-135">Die SharePoint-Clientkomponenten sind in Visual Studio Professional und Enterprise Edition enthalten.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-135">The SharePoint Client Components are included in Visual Studio Professional and Enterprise editions.</span></span> <span data-ttu-id="b8b5e-136">Wenn Sie Visual Studio-Community Edition verwenden, die neueste Version des Office Developer Tools SDK steht auf der folgenden Website: https://www.microsoft.com/en-us/download/details.aspx?id=35585.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-136">If you use Visual Studio Community edition, the latest version of the Office Developer Tools SDK is available at the following site: https://www.microsoft.com/en-us/download/details.aspx?id=35585.</span></span>
    
- <span data-ttu-id="b8b5e-137">Ein Konto Project Online – bietet dies Zugriff auf die Website gehostet.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-137">A Project Online account -- This provides access to the hosting site.</span></span> <span data-ttu-id="b8b5e-138">Weitere Informationen dazu, wie Sie ein Konto mit Project Online erhalten, finden Sie unter https://products.office.com/en-us/Project/project-online-portfolio-management.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-138">For more information about obtaining a Project Online account, see https://products.office.com/en-us/Project/project-online-portfolio-management.</span></span>
    
- <span data-ttu-id="b8b5e-139">Projekte auf der hosting-Website, die mit Daten aufgefüllt werden</span><span class="sxs-lookup"><span data-stu-id="b8b5e-139">Projects on the hosting site that are populated with information</span></span>
    
> [!NOTE]
> <span data-ttu-id="b8b5e-140">Der Standard ist .NET Framework (4.0 oder höher) die richtigen Framework verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-140">The standard .NET Framework (4.0 or later) is the correct framework to use.</span></span> <span data-ttu-id="b8b5e-141">Verwenden Sie die .NET Framework 4 Client Profile nicht.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-141">Do not use the .NET Framework 4 Client Profile.</span></span> 
  
## <a name="develop-the-application"></a><span data-ttu-id="b8b5e-142">Entwickeln der Anwendung</span><span class="sxs-lookup"><span data-stu-id="b8b5e-142">Develop the application</span></span>

<span data-ttu-id="b8b5e-143">Bei der Entwicklung von einer desktop-Anwendung für SharePoint, ist die bevorzugte Schnittstelle des Project-Seite-Clientobjektmodells (CSOM).</span><span class="sxs-lookup"><span data-stu-id="b8b5e-143">In developing a desktop application for SharePoint, the preferred interface is the Project client side object model (CSOM).</span></span> 
  
<span data-ttu-id="b8b5e-144">Sie können das vollständige Beispiel unter herunterladen https://github.com/OfficeDev/Project-CSOM-List-Projects-Tasks.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-144">You can download the complete sample at https://github.com/OfficeDev/Project-CSOM-List-Projects-Tasks.</span></span>
  
<span data-ttu-id="b8b5e-145">Die ersten beiden Themen enthalten grundlegende Probleme: Erstellen eines Visual Studio-Projekts mit den entsprechenden Namespaces und Assemblys und den Zugriff auf den Hostserver.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-145">The first two topics cover basic issues: creating a Visual Studio project with appropriate namespaces and assemblies, and accessing the hosting server.</span></span> <span data-ttu-id="b8b5e-146">Abrufen von Informationen über die CSOM aus einem und viele Objekte dienen in den übrigen Themen.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-146">The remaining topics deal with retrieving information through the CSOM, from one and many objects.</span></span> 
  
<span data-ttu-id="b8b5e-147">Abrufen von Informationen aus der Host ist ein Vorgang zwei-Aktion von Clientanwendungen.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-147">Retrieving information from the host is a two-action process from client applications.</span></span> <span data-ttu-id="b8b5e-148">Zunächst wird die Anwendung gibt an, und sendet eine oder mehrere Retrieval Anforderungen an den Server.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-148">First, the application specifies and sends one or more retrieval requests to the server.</span></span> <span data-ttu-id="b8b5e-149">Zweitens gibt die Anwendung eine Benachrichtigung an den Server die übermittelten Abfragen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-149">Second, the application issues a notification to the server to execute the submitted queries.</span></span> <span data-ttu-id="b8b5e-150">Der Server antwortet, indem die Ergebnisse der Abfrage an den Client gesendet.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-150">The server responds by sending the query results to the client.</span></span>
  
### <a name="set-up-the-visual-studio-project"></a><span data-ttu-id="b8b5e-151">Einrichten des Visual Studio-Projekts</span><span class="sxs-lookup"><span data-stu-id="b8b5e-151">Set up the Visual Studio project</span></span>

<span data-ttu-id="b8b5e-152">Erstellen eines neuen Projekts, verknüpfen die entsprechenden Assemblys und die erforderlichen Namespaces deklarieren besteht der Installation der Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-152">The application setup consists of creating a new project, linking the appropriate assemblies and declaring the needed namespaces.</span></span> <span data-ttu-id="b8b5e-153">Visual Studio stellt verschiedene Arten von Entwicklungsprojekten.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-153">Visual Studio presents several types of development projects.</span></span> 
  
#### <a name="select-a-visual-studio-project"></a><span data-ttu-id="b8b5e-154">Wählen Sie ein Visual Studio-Projekt</span><span class="sxs-lookup"><span data-stu-id="b8b5e-154">Select a Visual Studio project</span></span>

1. <span data-ttu-id="b8b5e-155">Starten Sie Visual Studio, und wählen Sie **Neues Projekt starten Sie** auf der Startseite.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-155">Launch Visual Studio and select **Start A New Project** on the Start Page.</span></span> 
    
   <span data-ttu-id="b8b5e-156">Das Dialogfeld Neues Projekt verfügbar Anwendungsvorlagen und Datenfelder für jede ausgewählte Vorlage angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-156">The New Project dialog displays available application templates, and data fields for any selected template.</span></span> 
    
2. <span data-ttu-id="b8b5e-157">Geben Sie für diese Anwendung die folgenden Elemente an.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-157">For this application, specify the following items.</span></span> <span data-ttu-id="b8b5e-158">Schlüsselwörter aufgetreten ist, auf dem Bildschirm aufweisen eine fett Attribut:</span><span class="sxs-lookup"><span data-stu-id="b8b5e-158">Keywords encountered on the screen have a bold attribute:</span></span>
    
   1. <span data-ttu-id="b8b5e-159">Wählen Sie im linken Bereich die installierte Vorlagen ein **C#-** => **Windows** => **klassischen Desktop**.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-159">From the Installed templates in the left pane, select **C#** => **Windows** => **Classic desktop**.</span></span> 
    
   2. <span data-ttu-id="b8b5e-160">Wählen Sie am oberen Rand der mittleren Bereich **.NET Framework 4**.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-160">At the top of the central pane, select **.NET Framework 4**.</span></span> 
    
   3. <span data-ttu-id="b8b5e-161">Wählen Sie im mittleren Bereich Anwendungstypen **Konsolenanwendung**aus.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-161">From the application types in the central pane, choose **Console Application**.</span></span> 
    
   4. <span data-ttu-id="b8b5e-162">Geben Sie im unteren Bereich einen Namen und Speicherort für das Projekt, und einen Lösungsnamen.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-162">In the bottom section, specify a name and location for the project, and a solution name.</span></span> 
    
   5. <span data-ttu-id="b8b5e-163">Auch im unteren Bereich das Kontrollkästchen Sie **Projektmappenverzeichnis erstellen** .</span><span class="sxs-lookup"><span data-stu-id="b8b5e-163">Also in the bottom section, check the **Create directory for solution** box.</span></span> 
    
3. <span data-ttu-id="b8b5e-164">Klicken Sie auf **OK** , um das ursprüngliche Projekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-164">Click **OK** to create the initial project.</span></span> 
    
#### <a name="add-assemblies"></a><span data-ttu-id="b8b5e-165">Hinzufügen von Assemblys</span><span class="sxs-lookup"><span data-stu-id="b8b5e-165">Add assemblies</span></span>

<span data-ttu-id="b8b5e-166">Die VS-Lösung benötigt die Assembly ProjectServerClient aus Project 2103 SDK, eine Reihe von Assemblys aus dem SharePoint-SDK und die System.Security für .NET Framework-Assembly.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-166">The VS solution needs the ProjectServerClient assembly from the Project 2103 SDK, a couple of assemblies from the SharePoint SDK, and the .NET Framework System.Security assembly.</span></span>
  
1. <span data-ttu-id="b8b5e-167">In VS Projektmappen-Explorer mit der rechten Maustaste in des Eintrags Verweise, und wählen Sie **Verweis hinzufügen**</span><span class="sxs-lookup"><span data-stu-id="b8b5e-167">In the VS Solution Explorer, right-click the References entry, and select **Add Reference…**</span></span> <span data-ttu-id="b8b5e-168">Klicken Sie im Kontextmenü.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-168">from the shortcut menu.</span></span> 
    
2. <span data-ttu-id="b8b5e-169">Überprüfen Sie die **Microsoft.ProjectServer.Client.dll**.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-169">Check the **Microsoft.ProjectServer.Client.dll**.</span></span> 
    
   <span data-ttu-id="b8b5e-170">Falls erforderlich, klicken Sie auf die **Durchsuchen...**</span><span class="sxs-lookup"><span data-stu-id="b8b5e-170">If needed, click the **Browse…**</span></span> <span data-ttu-id="b8b5e-171">Navigieren Sie zu dem Installationsverzeichnis Project 2013-SDK zum Suchen der Assembly, und klicken Sie unten im Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-171">button at the bottom of the dialog and navigate to the Project 2013 SDK installation directory to locate the assembly.</span></span> 
    
3. <span data-ttu-id="b8b5e-172">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-172">Click **OK**.</span></span> 
    
4. <span data-ttu-id="b8b5e-173">Fügen Sie den Namespace PrjoctServer Client, um die CS-Datei.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-173">Add the PrjoctServer Client namespace to the .cs file.</span></span>
    
   ```cs
    using Microsoft.ProjectServer.Client;
   ```

<span data-ttu-id="b8b5e-174">Fügen Sie die SharePoint 2013 SDK-Assemblys, die mit der NuGet Package Manager-Konsole hinzu.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-174">Add the SharePoint 2013 SDK assemblies using the NuGet Package Manager Console.</span></span> 
  
1. <span data-ttu-id="b8b5e-175">Klicken Sie im Menü Extras VS auf die folgenden Menüs: **Tools =\> NuGet Package Manager =\> Paket-Manager-Konsole**.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-175">From the VS Tools menu, click the following menus: **Tools =\> NuGet Package Manager =\> Package Manager Console**.</span></span> 
    
2. <span data-ttu-id="b8b5e-176">Geben Sie in der Paket-Manager-Konsole den folgenden Befehl und drücken Sie \<EINGABETASTE\>:</span><span class="sxs-lookup"><span data-stu-id="b8b5e-176">In the Package Manager Console, enter the following command and press \<ENTER\>:</span></span>
    
   ```cs
    Install-Package Microsoft.SharePointOnline.CSOM
   ```

   <span data-ttu-id="b8b5e-177">Die **Paket-Manager-Konsole** enthält eine Beschreibung der Befehlsergebnisse; und VS Projektmappen-Explorer angezeigt, die SharePoint-Assemblys in den Projektverweisen.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-177">The **Package Manager Console** provides a description of the command results; and, the VS Solution Explorer displays the SharePoint assemblies in the project references.</span></span> 
    
3. <span data-ttu-id="b8b5e-178">Fügen Sie die Namespaces in die CS-Datei:</span><span class="sxs-lookup"><span data-stu-id="b8b5e-178">Add the namespaces to the .cs file:</span></span>
    
   ```cs
    using Microsoft.SharePoint.Client;
   ```

<span data-ttu-id="b8b5e-179">Die System.Security Assembly ist Teil von .NET Framework und mit Framework installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-179">The System.Security assembly is part of .NET Framework and was installed with the framework.</span></span> <span data-ttu-id="b8b5e-180">Die beispielanwendung benötigt eine weitere Namespace, der eine verschlüsselte Zeichenfolge, die das Hostsystem für die Authentifizierung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-180">The sample application needs one more namespace that provides an encrypted string to the hosting system for authentication.</span></span> <span data-ttu-id="b8b5e-181">Nach der Authentifizierung kann die Anwendung auf das Hostsystem Projekte zugreifen.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-181">Once authenticated, the application can access projects on the hosting system.</span></span> <span data-ttu-id="b8b5e-182">CS-Datei auf diese Weise System.Security-Namespace hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="b8b5e-182">Add the System.Security namespace to the .cs file in this way:</span></span>
  
1. <span data-ttu-id="b8b5e-183">In VS Projektmappen-Explorer mit der rechten Maustaste in des Eintrags Verweise, und wählen Sie **Verweis hinzufügen**</span><span class="sxs-lookup"><span data-stu-id="b8b5e-183">In the VS Solution Explorer, right-click the References entry, and select **Add Reference…**</span></span> <span data-ttu-id="b8b5e-184">Klicken Sie im Kontextmenü.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-184">from the shortcut menu.</span></span> 
    
2. <span data-ttu-id="b8b5e-185">Wählen Sie **Assemblys =\> Framework** im linken Bereich des Dialogfelds Verweise Manager **System.Security**überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-185">Select **Assemblies =\> Framework** in the left pane of the References Manager dialog, then check **System.Security**.</span></span> 
    
3. <span data-ttu-id="b8b5e-186">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-186">Click **OK**.</span></span> 
    
4. <span data-ttu-id="b8b5e-187">CS-Datei System.Security-Namespace hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="b8b5e-187">Add the System.Security namespace to the .cs file:</span></span>
    
   ```cs
    using System.Security;
   ```

<span data-ttu-id="b8b5e-188">Der Anfang des CS-Datei sollte die folgenden Namespaces enthalten:</span><span class="sxs-lookup"><span data-stu-id="b8b5e-188">The start of the .cs file should contain the following namespaces:</span></span>
  
- <span data-ttu-id="b8b5e-189">System</span><span class="sxs-lookup"><span data-stu-id="b8b5e-189">System</span></span>
    
- <span data-ttu-id="b8b5e-190">System.Collections.Generic</span><span class="sxs-lookup"><span data-stu-id="b8b5e-190">System.Collections.Generic</span></span>
    
- <span data-ttu-id="b8b5e-191">System.Linq</span><span class="sxs-lookup"><span data-stu-id="b8b5e-191">System.Linq</span></span>
    
- <span data-ttu-id="b8b5e-192">System.Test</span><span class="sxs-lookup"><span data-stu-id="b8b5e-192">System.Test</span></span>
    
- <span data-ttu-id="b8b5e-193">Microsoft.ProjectServer.Client</span><span class="sxs-lookup"><span data-stu-id="b8b5e-193">Microsoft.ProjectServer.Client</span></span>
    
- <span data-ttu-id="b8b5e-194">Microsoft.SharePoint.Client</span><span class="sxs-lookup"><span data-stu-id="b8b5e-194">Microsoft.SharePoint.Client</span></span>
    
- <span data-ttu-id="b8b5e-195">System.Security</span><span class="sxs-lookup"><span data-stu-id="b8b5e-195">System.Security</span></span>
    
### <a name="connect-to-the-host-system"></a><span data-ttu-id="b8b5e-196">Verbinden Sie mit dem Hostsystem</span><span class="sxs-lookup"><span data-stu-id="b8b5e-196">Connect to the host system</span></span>

<span data-ttu-id="b8b5e-197">Project Online ist eine SharePoint-Anwendung mithilfe der SharePoint-Authentifizierung die richtige Vorgehensweise.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-197">Project Online is a SharePoint application, so using SharePoint authentication is the correct approach.</span></span> <span data-ttu-id="b8b5e-198">Im folgenden Codefragment bereitet gehostete Umgebung zugreifen.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-198">The following code fragment prepares to access the hosted environment.</span></span>
  
```cs
    class Program
    {
        private static ProjectContext projContext;
        static void Main (string[] args)
        {
            using (ProjectContext projContext = new ProjectContext("https://Contoso.sharepoint.com/sites/pwa"))
            {
                SecureString password - new SecureString();
                foreach (char c in "password".ToCharArray()) password.AppendChar(c);
                //Using SharePoint method to load Credentials
                projContext.Credentials = new SharePointOnlineCredentials("sarad@Contoso.onmicrosoft.com", password);

```

<span data-ttu-id="b8b5e-199">Vorbereitung die gehostete Umgebung Zugriff auf gehören die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="b8b5e-199">Preparations to access the hosted environment include the following items:</span></span>
  
1. <span data-ttu-id="b8b5e-200">Ein Context-Objekt für die Projekte erstellen – dies in den folgenden Code, der im vorherigen Codefragment enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-200">Create a context object for the projects -- this is contained in the following code of the preceding code fragment.</span></span> 
    
   ```cs
    private static ProjectContext projContext;
    
   ```

   <span data-ttu-id="b8b5e-201">Im Kontext wird von anderen Komponenten, die das System im Kontext des Project-Objektmodell verwalten geerbt.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-201">The context is inherited by other components, allowing the system to manage the context of the Project object model.</span></span>
    
2. <span data-ttu-id="b8b5e-202">Identifizieren der Hostwebsite – dies geschieht in den folgenden Code aus dem vorherigen Codefragment.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-202">Identify the host site -- this is done in the following code from the preceding code fragment.</span></span>
    
   ```cs
    using (ProjectContext projContext = new ProjectContext("https://Contoso.sharepoint.com/sites/pwa"))
   ```

   <span data-ttu-id="b8b5e-203">Wenn Projekte Kontext zu instanziieren, muss die Anwendung den Stamm der Websitesammlung Projekte bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-203">When instantiating the projects context, the application needs to provide the root of the Projects site collection.</span></span> <span data-ttu-id="b8b5e-204">Die Anwendung verwendet eine Teilzeichenfolge der URL des Stammverzeichnisses der Projekte.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-204">The application uses a substring of the URL of the root of the Projects.</span></span> <span data-ttu-id="b8b5e-205">Ein rotes Rechteck in der folgenden Abbildung ist eine Momentaufnahme der von diesem Speicherort hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-205">A snapshot of this location is highlighted with a red rectangle in the following illustration.</span></span> <span data-ttu-id="b8b5e-206">Die Authentifizierung benötigt die Zeichenfolge aus dem Start über die Teilzeichenfolge "pwa".</span><span class="sxs-lookup"><span data-stu-id="b8b5e-206">The authentication needs the string from its start through the substring "pwa".</span></span> <span data-ttu-id="b8b5e-207">Im Codebeispiel, die Anwendung verwendet die Zeichenfolge "https://XXXXXXXX.sharepoint.com/sites/pwa".</span><span class="sxs-lookup"><span data-stu-id="b8b5e-207">In the code listing, the application uses the string "https://XXXXXXXX.sharepoint.com/sites/pwa".</span></span>
        
   <span data-ttu-id="b8b5e-208">![Screenshot der URL der Websitesammlung Projekte innerhalb einer rote Rahmenlinie.] (media/d48c4894-5dba-46b6-886a-3c59bfb83c4d.png "Screenshot der URL der Projekte Websitesammlung innerhalb einer rote Rahmenlinie")</span><span class="sxs-lookup"><span data-stu-id="b8b5e-208">![Screen shot of the URL of the Projects site collection within a red border.](media/d48c4894-5dba-46b6-886a-3c59bfb83c4d.png "Screen shot of the URL of the Projects site collection within a red border")</span></span>
  
3. <span data-ttu-id="b8b5e-209">Setzen Sie das Kennwort in eine sichere Zeichenfolge – Dies geschieht in den folgenden Code aus dem vorherigen Codefragment.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-209">Place the password in a secure string -- this is done in the following code from the preceding code fragment.</span></span>
    
   ```cs
    SecureString password - new SecureString();
    foreach (char c in "password".ToCharArray()) password.AppendChar(c);
    
   ```

   <span data-ttu-id="b8b5e-210">Das Kennwort und die Benutzer sind die Anmeldeinformationen zum Zugriff auf die Hostwebsite.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-210">The password and user account are the credentials to access the host site.</span></span> 
    
4. <span data-ttu-id="b8b5e-211">Fügen Sie das Benutzerkonto und das Kennwort zum Bereich Anmeldeinformationen des Kontextobjekts – dies geschieht in den folgenden Code aus dem vorherigen Codefragment.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-211">Add the user account and password to the credentials portion of the context object -- this is done in the following code from the preceding code fragment.</span></span>
    
   ```cs
    projContext.Credentials = new SharePointOnlineCredentials("sarad@Contoso.onmicrosoft.com", password);
   ```

<span data-ttu-id="b8b5e-212">Der Projektkontext instanziierte ist einsatzbereit.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-212">The instantiated project context is ready to use.</span></span>
  
### <a name="list-all-published-projects"></a><span data-ttu-id="b8b5e-213">Listen Sie alle veröffentlichten Projekte</span><span class="sxs-lookup"><span data-stu-id="b8b5e-213">List all published projects</span></span>

<span data-ttu-id="b8b5e-214">Project Online und ProjectServer verwenden Proxys für die Kommunikation mit dem Server zu erstellen, Bericht, Update und delete-Operationen (CRUD).</span><span class="sxs-lookup"><span data-stu-id="b8b5e-214">Project Online and ProjectServer use proxies to communicate with the server for create, report, update, and delete (CRUD) operations.</span></span> <span data-ttu-id="b8b5e-215">Der Hostserver behandelt Anforderungen effizient und hat der Client die folgenden Aktionen ausführen, bei der Kommunikation mit dem Server:</span><span class="sxs-lookup"><span data-stu-id="b8b5e-215">The host/server handles requests in an efficient manner and has the client perform the following actions in communicating with the server:</span></span>
  
1. <span data-ttu-id="b8b5e-216">Richten Sie einen Kontext für die Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-216">Establish a context for communication.</span></span> 
    
   <span data-ttu-id="b8b5e-217">Der Kontext wird von der Projects-Auflistung als auch andere Objekte und Auflistungen durch Vererbung, einschließlich der Tasks-Auflistung, Assignments-Auflistung, die Stage-Objekts und benutzerdefinierte Felder verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-217">The context is used by the projects collection, as well as other objects and collections through inheritance, including the tasks collection, assignments collection, the stage object, and custom fields.</span></span> 
    
2. <span data-ttu-id="b8b5e-218">Verwenden des Objektmodells auf ein Objekt, Auflistung oder abzurufenden Daten angeben.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-218">Use the object model to specify an object, collection, or data to retrieve.</span></span>
    
   <span data-ttu-id="b8b5e-219">Dieser Schritt wird LINQ verwendet, als eine Abfrage oder eine Methode.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-219">This step uses LINQ as a query or as a method.</span></span> <span data-ttu-id="b8b5e-220">Die Spezifikation steuert, was Sie erhalten.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-220">The specification controls what you receive.</span></span> <span data-ttu-id="b8b5e-221">Dieser Schritt ist häufig als Hauptteil der Load-Methode (Schritt 3) eingebettet.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-221">Often, this step is embedded as the body of the Load method (step 3).</span></span> 
    
3. <span data-ttu-id="b8b5e-222">Laden der Abruf aus dem vorherigen Schritt die Load() oder LoadQuery()-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-222">Load the retrieval specification from the previous step using the Load() or LoadQuery() method.</span></span>
    
   <span data-ttu-id="b8b5e-223">Verwenden Sie zum Laden von Auflistungen und Objekte, Load().</span><span class="sxs-lookup"><span data-stu-id="b8b5e-223">For loading collections and objects, use Load().</span></span> <span data-ttu-id="b8b5e-224">Für Abfragen mit Klauseln wie "Where" und "group" LoadQuery() verwenden.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-224">For queries with clauses such as "where" and "group", use LoadQuery().</span></span> 
    
4. <span data-ttu-id="b8b5e-225">Führen Sie die Anforderung mithilfe der ExecuteQuery()-Methode.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-225">Execute the request using the ExecuteQuery() method.</span></span>
    
   <span data-ttu-id="b8b5e-226">Die Methode ExecuteQuery() benachrichtigt den Host, dass die Abfrage oder Abfragen ausführen können.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-226">The ExecuteQuery() method notifies the host that the query or queries are ready to execute.</span></span> <span data-ttu-id="b8b5e-227">Nachdem der Host-Benachrichtigung erhält, führt die Abfragen und sendet die Ergebnisse an den Client.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-227">Once the host receives notification, it executes the queries and sends the results to the client.</span></span> 
    
<span data-ttu-id="b8b5e-228">Sie mit den Informationen auf dem Client können die Anwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-228">With the information at the client, the application can use it.</span></span> <span data-ttu-id="b8b5e-229">Im folgenden Codefragment durch die veröffentlichten Projekte und druckt die Id und Name für jedes veröffentlichte Projekt auf dem Host.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-229">The following code fragment cycles through the published projects and prints the Id and Name for each published project on the host.</span></span>
  
```cs
// Get the list of projects in Project Web App.
var projects = projContext.Projects;
projContext.Load(projects);
projcontext.ExecuteQuery();
foreach (PublishedProject pubProj in projContext.Projects)
{
    Console.WriteLine("\n{0}. {1}   {2} \t{3} \n", j++, pubProj.Id, pubProj.Name, pubProj.CreatedDate);
}

```

<span data-ttu-id="b8b5e-230">Ausgabe:</span><span class="sxs-lookup"><span data-stu-id="b8b5e-230">Output:</span></span>
  
```cs
Published Project count:2
1. be80a848-b2ef-e511-80f4-00155dc84e01   A second Project     3/21/2016 10:14:40 PM
2. 9d730a1a-60ed-e511-80f6-00155dc87d01   Ent_Proj_1   3/18/2016 11:21:14 PM

```

### <a name="make-a-request"></a><span data-ttu-id="b8b5e-231">Stellen Sie eine Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8b5e-231">Make a request</span></span>

<span data-ttu-id="b8b5e-232">Verwenden die Aktionen aus dem vorherigen Codefragment, ruft die Anwendung die Liste der Projekte in das angegebene Konto auf der Website hosten.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-232">Using the actions from the previous code fragment, the application retrieves the list of projects in the specified account on the hosting site.</span></span> 
  
1. <span data-ttu-id="b8b5e-233">Die ProjectContext wird für die Projekte in der Liste angegeben.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-233">The ProjectContext is specified for the projects to list.</span></span> 
    
   ```cs
    var projects = projContext.Projects;
   ```

2. <span data-ttu-id="b8b5e-234">Geben Sie das Element abrufen.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-234">Specify the item to retrieve.</span></span> 
    
   ```cs
    projContext.Load(projects);
   ```

   <span data-ttu-id="b8b5e-235">Durch nur unter Angabe der Auflistung, ruft der Server Auffüllen jedes Projekt mit Werten für die Standardgruppe von Eigenschaften der Project-Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-235">By only stating the collection, the server retrieves the project collection, populating each project with values for the default set of properties.</span></span> <span data-ttu-id="b8b5e-236">Zugreifen auf Eigenschaften, die Teil der standardeigenschaftensatz sind bietet erfolgreiche Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-236">Accessing properties that are part of the default property set gives successful results.</span></span> <span data-ttu-id="b8b5e-237">Zugreifen auf Eigenschaften, die nicht Teil der standardmäßigen sind festzulegen, führt zu einer Ausnahme "Nicht initialisiert".</span><span class="sxs-lookup"><span data-stu-id="b8b5e-237">Accessing properties that are not part of the default set results in a "Not initialized" exception.</span></span>
    
3. <span data-ttu-id="b8b5e-238">Laden Sie die Anforderung (projContext.Load).</span><span class="sxs-lookup"><span data-stu-id="b8b5e-238">Load the request (projContext.Load).</span></span>
    
   <span data-ttu-id="b8b5e-239">Dies ist Teil der im vorherigen Schritt.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-239">This is part of the previous step.</span></span>
    
4. <span data-ttu-id="b8b5e-240">Ausführen der Abfrage (ExecuteQuery).</span><span class="sxs-lookup"><span data-stu-id="b8b5e-240">Execute the query (ExecuteQuery).</span></span> 
    
   ```cs
    projContext.ExecuteQuery();
   ```

### <a name="retrieve-high-level-project-information"></a><span data-ttu-id="b8b5e-241">Abrufen von allgemeinen Projektinformationen</span><span class="sxs-lookup"><span data-stu-id="b8b5e-241">Retrieve high-level project information</span></span>

<span data-ttu-id="b8b5e-242">Eigenschaften, die nicht standardmäßigen Eigenschaften in der Anforderung an den Server müssen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-242">Properties that are not default properties must be specified in the request to the server.</span></span> <span data-ttu-id="b8b5e-243">Im nächste Codefragment lädt den Projects-Auflistung Kontext wie im vorherigen Beispiel.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-243">The next code fragment loads the projects collection context as in the previous example.</span></span> <span data-ttu-id="b8b5e-244">Die Spezifikation angefordert zusätzliche nicht standardmäßigen Eigenschaften in das Ergebnis einbezogen.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-244">Then, the specification requests additional non-default properties to include in the result.</span></span> 
  
```cs
var projects = projContext.Projects;
projContext.Load(projects,
    ps => ps.IncludeWithDefaultProperties(
        p => p.StartDate, p => p.Phase, p => p.Stage));
projContext.ExecuteQuery();

```

<span data-ttu-id="b8b5e-245">Die Load-Anweisung gibt den Kontext der Projects-Auflistung und fügt die StartDate, Phase und Stufe Abfrageergebnis hinzu.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-245">The load statement specifies the projects collection context, and adds the StartDate, Phase, and Stage to the query result.</span></span> <span data-ttu-id="b8b5e-246">Die zusätzlichen Eigenschaften können skalare, werden Objekte und Auflistungen.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-246">The additional properties can be scalar, objects, or collections.</span></span> <span data-ttu-id="b8b5e-247">Skalare Elemente können direkt zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-247">Scalar items can be accessed directly.</span></span> <span data-ttu-id="b8b5e-248">Objekte und Auflistungen benötigen weitere Verarbeitung weiterleitet, wie im folgenden Codefragment dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-248">Objects and collections require additional processing, as in the following code fragment.</span></span>
  
```cs
// Using the previous definition and Load statement …
projContext.ExecuteQuery();
foreach (PublishedProject pubProj in projContext.Projects)
{
Console.WriteLine("\n\t{0}. \t{1} \n\t{2} \n\t{3} \n", j++, pubProj.Id, pubProj.Name,
    pubProj.CreatedDate);
             // The following statement generates an exception about the object 
             // reference not being set to an instance on the server. 
             // Console.WriteLine("\tCurrent Phase:\t{0}", pubProj.Phase.Name);
             // Phase and Stage are not published with the rest of the data. Need to pull these objects from the server.
             Phase oPhase = pubProj.Phase;
             projContext.Load(oPhase);
             projContext.ExecuteQuery();
             //if-else fails because the else case fails with "Microsoft.SharePoint.Client.ServerObjectNullReferenceException".
             //if (oPhase.ServerObjectIsNull != null)
             //Using try-catch instead
             try
             {
                  Console.WriteLine("\tCurrent Phase:\t{0}", oPhase.Name);
             }
             
             catch
             {
                  Console.WriteLine("\tCurrent Phase:\t Not available");
             }
             
             Stage oStage = pubProj.Stage;
             projContext.Load(oStage);
             projContext.ExecuteQuery();
             //Again, not using if-else combination for the same reason as above.
             try
             {
                  Console.WriteLine("\tCurrent Stage:\t{0}", oStage.Name);
             }
             
             catch
             {
                  Console.WriteLine("\tCurrent Stage:\t Not available");
    }

```

<span data-ttu-id="b8b5e-249">Ausgabe der ersten drei Projekte:</span><span class="sxs-lookup"><span data-stu-id="b8b5e-249">Output of the first three projects:</span></span>
  
```cs
Project counts:31
1. Project ID:  957d5fcd-5cbf-e111-9f1e-00155d022681
        Name:           Acquisition Target Analysis
        CreatedDate:            3/22/2016 5:14:34 PM
        Current Phase:  3. Plan
        Current Stage:  6. Plan
2. Project ID:  16905202-5fbf-e111-9f1e-00155d022681
        Name:           Apparel ERP Upgrade
        CreatedDate:            3/22/2016 5:36:40 PM
        Current Phase:  3. Plan
        Current Stage:  6. Plan
3. Project ID:  dce23152-63bf-e111-9f1e-00155d022681
        Name:           Audit Tracking Solution
        CreatedDate:            3/22/2016 5:02:24 PM
        Current Phase:  2. Select
        Current Stage:  4. Select Gate

```

### <a name="retrieve-all-tasks-in-a-project"></a><span data-ttu-id="b8b5e-250">Rufen Sie aller Vorgänge in einem Projekt ab</span><span class="sxs-lookup"><span data-stu-id="b8b5e-250">Retrieve all tasks in a project</span></span>

<span data-ttu-id="b8b5e-251">Jedes Projekt verfügt über viele Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-251">Each project has many tasks.</span></span> <span data-ttu-id="b8b5e-252">Also umfasst die Aufgaben für ein einzelnes Projekt abrufen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b8b5e-252">So, pulling the tasks for a single project consists of the following:</span></span>
  
1. <span data-ttu-id="b8b5e-253">Richten Sie im Kontext der Projects-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-253">Establish the context of the projects collection.</span></span>
    
   ```cs
    var projects = projContext.Projects;
   ```

2. <span data-ttu-id="b8b5e-254">Rufen Sie die Projektinformationen, einschließlich der Task-Eigenschaften ab.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-254">Retrieve the project information, including the Task properties.</span></span>
    
   ```cs
    projContext.Load(projects);
    ProjContext.ExecuteQuery();
    foreach (PublishedProject pubProj in projContext.Projects){
    
   ```

    <span data-ttu-id="b8b5e-255">Beachten Sie, dass die Anwendung veröffentlichte Projekte Adressierung ist.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-255">Note that the application is addressing published projects.</span></span> <span data-ttu-id="b8b5e-256">Der Kontext für das aktuelle veröffentlichten Projekt ist PubProj.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-256">The context for the current published project is pubProj.</span></span> 
    
3. <span data-ttu-id="b8b5e-257">Richten Sie im Kontext der Tasks-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-257">Establish the context for the Tasks collection.</span></span>
    
   ```cs
    PublishedTaskCollection collTask = pubProj.Tasks;
   ```

   <span data-ttu-id="b8b5e-258">Die `pubProj.Tasks` Eigenschaft verweist auf die Aufgaben des aktuellen Projekts veröffentlichte.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-258">The `pubProj.Tasks` property references the tasks of the current published project.</span></span> 
    
4. <span data-ttu-id="b8b5e-259">Laden Sie die Spezifikation zum Abrufen der Auflistung von Workflowaufgaben, einschließlich der entsprechenden nicht standardmäßigen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-259">Load the specification to retrieve Task collection, including the appropriate non-default properties.</span></span>
    
   ```cs
    projContext.Load(collTask,
        tsk => tsk.IncludeWithDefaultProperties(
            t => t.Id, t => t.Name, t => t.Start,
            t => t.ScheduledStart, t => t.Completion));
    
   ```

5. <span data-ttu-id="b8b5e-260">Führen Sie die Abfrage zum Abrufen der Aufgabe-Auflistung mit den entsprechenden Eigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-260">Execute the query to retrieve the Task collection with the appropriate properties.</span></span>
    
   ```cs
    projContext.ExecuteQuery();
   ```

<span data-ttu-id="b8b5e-261">Die Informationen sind jetzt lokalen.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-261">The information is now local.</span></span> <span data-ttu-id="b8b5e-262">Im folgenden Codefragment verarbeitet die veröffentlichten Tasks-Auflistung durch Schreiben die Informationen in der Konsole angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-262">The following code fragment processes the published tasks collection by writing the information to the console.</span></span>
  
```cs
    Console.WriteLine("Task collection count: {0}", collTask.Count.ToString());
    if (collTask.Count > 0)
    {
        int k = 1;    //Task counter.
        foreach (PublishedTask t in collTask)
        {
            Console.WriteLine("{0}. Id:{1} \tName:{2}", k++, t.Id, t.Name);
            Console.WriteLine("\t ScheduledStart:{0} \tStart:{1} \tCompletion:{2}", k, t.ScheduledStart, t.Start, t.Completion);
        }
    }

```

<span data-ttu-id="b8b5e-263">Ausgabe von Aufgaben für ein Projekt:</span><span class="sxs-lookup"><span data-stu-id="b8b5e-263">Output of tasks for one project:</span></span>
  
```cs
Task collection count: 5
1. Id:256fa850-b2ef-e511-80f6-00155dc87d01      Name:Load software onto computer
         ScheduledStart:2       Start:4/4/2016 8:00:00 AM       Completion:4/4/2016 8:00:00 AM
2. Id:266fa850-b2ef-e511-80f6-00155dc87d01      Name:Locate and load Project Online SDK
         ScheduledStart:3       Start:4/5/2016 8:00:00 AM       Completion:4/5/2016 8:00:00 AM
3. Id:276fa850-b2ef-e511-80f6-00155dc87d01      Name:Locate and load SP SDK
         ScheduledStart:4       Start:4/5/2016 1:00:00 PM       Completion:4/5/2016 1:00:00 PM
4. Id:286fa850-b2ef-e511-80f6-00155dc87d01      Name:Build app that accesses Proj Online
         ScheduledStart:5       Start:4/6/2016 8:00:00 AM       Completion:4/6/2016 8:00:00 AM
5. Id:296fa850-b2ef-e511-80f6-00155dc87d01      Name:Build app that accesses task assignments
         ScheduledStart:6       Start:4/7/2016 8:00:00 AM       Completion:4/7/2016 8:00:00 AM

```

### <a name="access-information-at-multiple-levels"></a><span data-ttu-id="b8b5e-264">Zugriff auf Informationen auf mehreren Ebenen</span><span class="sxs-lookup"><span data-stu-id="b8b5e-264">Access information at multiple levels</span></span>

<span data-ttu-id="b8b5e-265">Jede Aufgabe kann eine oder mehrere Personen (auch bekannt als verfügen.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-265">Each task can have one or more persons (a.k.a.</span></span> <span data-ttu-id="b8b5e-266">Ressource) beiträgt, dessen Abschluss.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-266">resource) contributing toward its completion.</span></span> <span data-ttu-id="b8b5e-267">Die Aufgaben und Ressourcen Auflistungen enthält diese Informationen für jeden Vorgang.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-267">The Assignments and Resources collections contain this information for each task.</span></span> 
  
<span data-ttu-id="b8b5e-268">Die Verarbeitung umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b8b5e-268">The processing consists of the following:</span></span>
  
1. <span data-ttu-id="b8b5e-269">Abrufen von einen Kontext für den Projektvorgang.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-269">Obtaining a context for the project task.</span></span>
    
2. <span data-ttu-id="b8b5e-270">Erstellen Sie eine Anforderung, und Laden Sie die Anforderung für die Zuweisung der Aufgabe gebunden.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-270">Build a request and load the request for the assignments tied to the task.</span></span> 
    
3. <span data-ttu-id="b8b5e-271">Führen Sie die Abfrage für die Zuordnungen.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-271">Execute the query for the assignments.</span></span>
    
4. <span data-ttu-id="b8b5e-272">Erstellen Sie eine Anforderung, und Laden Sie die Anforderung für die Ressource eine einzelne Zuordnung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-272">Build a request and load the request for the resource associated with an individual assignment.</span></span> 
    
5. <span data-ttu-id="b8b5e-273">Führen Sie die Abfrage für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-273">Execute the query for the resource.</span></span>
    
> [!NOTE] 
> - <span data-ttu-id="b8b5e-274">Assignments-Auflistung ist explizit in die Informationen vom Server angefordert, da es sich nicht um eine Standardeigenschaft der Tasks-Auflistung darstellt.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-274">The Assignments collection is explicitly requested in the information from the server because it is not a default property of the Tasks collection.</span></span> <span data-ttu-id="b8b5e-275">Als Sammlung erfolgt eine nachfolgende Abfrage zum Abrufen der Auflistung vom Server.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-275">As a collection, a subsequent query is made to pull the collection from the server.</span></span> 
> - <span data-ttu-id="b8b5e-276">Die Ressource ist ein Objekt.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-276">The Resource is an object.</span></span> <span data-ttu-id="b8b5e-277">Die Abfrage für eine Zuordnung enthält den Ressourcennamen der Zuordnung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-277">The query for an assignment includes the resource name associated with the assignment.</span></span>
    
```cs
PublishedTaskCollection collTask = pubProj.Tasks;
    projContext.Load(collTask,
        tsk => tsk.IncludeWithDefaultProperties(
            t => t.Id, t => t.Name, 
            t => t.Assignments));
    projContext.Load(collTask);
    projContext.ExecuteQuery();
    Console.WriteLine("Task collection count: {0}", collTask.Count.ToString());
    if (collTask.Count > 0)
    {
        int k = 1;    //Task counter.
        //Processing task list for current project
        foreach (PublishedTask t in collTask)
        {
            Console.WriteLine("{0}. Id:{1} \tName:{2}", k, t.Id, t.Name);
            k++;
            //Define and retrieve Assignments for current task
            PublishedAssignmentCollection collAssgns = t.Assignments;
            projContext.Load(collAssgns);
            projContext.ExecuteQuery();
            Console.WriteLine("    Assignment collection count: {0}", collAssgns.Count);
            if (collAssgns.Count > 0)
            {
                //Output string for resources assigned to task
                StringBuilder output = new StringBuilder();
                output.AppendFormat("\t Assignments: ");
                foreach (PublishedAssignment a in collAssgns)
                {
                    //Define and retrieve resource name for current assignment 
                    //(an object)
                    projContext.Load(a,
                        b => b.Resource.Name);
                    projContext.ExecuteQuery();
                    output.AppendFormat("{0}, ", a.Resource.Name);
                }
                Console.WriteLine(output);
            }
            else
            {
                Console.WriteLine("\t Assignments: None");
            }
        }
    }   // endif

```

<span data-ttu-id="b8b5e-278">Die Ausgabe für Aufgaben 52, 75 und 76 eines Projekts:</span><span class="sxs-lookup"><span data-stu-id="b8b5e-278">Output for tasks 52, 75, and 76 of a project:</span></span>
  
```cs
52. Id:2c729e96-54f0-e511-80c6-000d3a33235f     Name:Develop training materials
    Assignment collection count: 1
         Assignments: Robert Lyon,
75. Id:43729e96-54f0-e511-80c6-000d3a33235f     Name:Determine final deployment strategy
    Assignment collection count: 0
         Assignments: None
76. Id:44729e96-54f0-e511-80c6-000d3a33235f     Name:Develop deployment methodology
    Assignment collection count: 4
         Assignments: Molly Dempsey, Sara Davis, Shammi Mohamed, Zainal Arifin, 

```

### <a name="access-custom-enterprise-level-fields"></a><span data-ttu-id="b8b5e-279">Access benutzerdefinierte Unternehmensebene Felder</span><span class="sxs-lookup"><span data-stu-id="b8b5e-279">Access custom enterprise-level fields</span></span>

<span data-ttu-id="b8b5e-280">Benutzerdefinierte Felder für Project Online vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-280">Custom fields exist for Project Online.</span></span> <span data-ttu-id="b8b5e-281">Dies sind Unternehmensebene Felder, die einzelne Project zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-281">These are enterprise-level fields that can be associated with individual project.</span></span> <span data-ttu-id="b8b5e-282">In diesem Abschnitt wird beschrieben, wie diese Felder Zugriff auf.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-282">This section describes how to access these fields.</span></span> 
  
<span data-ttu-id="b8b5e-283">Benutzerdefinierte Felder sind nicht in die Standardgruppe von Eigenschaften, die einem Projekt zugeordnete enthalten.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-283">Custom fields are not included in the default set of properties associated with a project.</span></span> <span data-ttu-id="b8b5e-284">Ja, benötigen sie explizite Identifikation in der Spezifikation abrufen.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-284">So, they need explicit identification in the retrieval specification.</span></span> <span data-ttu-id="b8b5e-285">Allgemeine Ansicht über den Prozess umfasst die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="b8b5e-285">The high-level view of the process consists of the following items:</span></span>
  
1. <span data-ttu-id="b8b5e-286">Tunnelmodus an das benutzerdefinierte Feld mit den allgemeinen Namen.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-286">Tunnel to the custom field using its common name.</span></span>
    
2. <span data-ttu-id="b8b5e-287">Rufen Sie den internen Namen des benutzerdefinierten Felds ab.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-287">Retrieve the internal name of the custom field.</span></span>
    
3. <span data-ttu-id="b8b5e-288">Zurück zu globalen Kontext und Abfragen des Systems mit den internen Namen des benutzerdefinierten Felds.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-288">Return to the global context and query the system using the internal name of the custom field.</span></span>
    
#### <a name="tunnel-to-the-custom-field-retrieve-its-internal-name-and-used-it-to-query-the-system"></a><span data-ttu-id="b8b5e-289">An das benutzerdefinierte Feld Tunnel, seinen internen Namen abrufen und es für das System die Abfrage verwendet</span><span class="sxs-lookup"><span data-stu-id="b8b5e-289">Tunnel to the custom field, retrieve its internal name, and used it to query the system</span></span>

<span data-ttu-id="b8b5e-290">Für diese Aufgabe gibt eine abrufen, die eine Standardeigenschaft mit ein hinzugefügte Detail verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-290">This task specifies a retrieval that uses a non-default property with one added detail.</span></span>
  
1. <span data-ttu-id="b8b5e-291">Beginnen Sie mit dem Kontext Projekte wie am Anfang dieses Artikels beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-291">Begin by using the projects context, as described at the beginning of this article.</span></span>
    
   ```cs
    // Get the list of published projects in Project Web App.
    var projects = projContext.Projects;
    
   ```

2. <span data-ttu-id="b8b5e-292">Projects-Auflistung abrufen Anforderung zusätzlich zu anderen nicht standardmäßige-Eigenschaften zum Abrufen zwei Elemente hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="b8b5e-292">Add two items to the projects collection retrieval request in addition to any other non-default properties to retrieve:</span></span>
    
   ```cs
    projContext.Load(projects,
        ps => ps.IncludeWithDefaultProperties(
            p => p.Phase, p => p.Stage,                  // Other nondefault properties
            p => p.IncludeCustomFields,                  // Gets PublishedProject object 
                                                        // that contains custom fields
            p => p.IncludeCustomFields.CustomFields));   // Populates the custom fields
                    projContext.ExecuteQuery();
    
   ```

   <span data-ttu-id="b8b5e-293">Die `p => p.IncludeCustomFields` Klausel erkennt die muss ein Project-Objekt verwenden, benutzerdefinierte Felder unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-293">The  `p => p.IncludeCustomFields` clause identifies the need to use a project object that supports custom fields.</span></span> 
    
   <span data-ttu-id="b8b5e-294">Die `p => p.IncludeCustomFields.CustomFields` Klausel fordert die Aufnahme der Daten im Abfrageergebnis benutzerdefinierter Felder.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-294">The  `p => p.IncludeCustomFields.CustomFields` clause requests the inclusion of custom field data in the query result.</span></span> <span data-ttu-id="b8b5e-295">Diese Informationen werden verwendet, nachdem der interne Name des benutzerdefinierten Felds abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-295">This information is used after the custom field internal name is retrieved.</span></span> 
    
3. <span data-ttu-id="b8b5e-296">Laden Sie die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-296">Load the request.</span></span>
    
   <span data-ttu-id="b8b5e-297">Dies ist Teil der im vorherigen Schritt.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-297">This is part of the previous step.</span></span>
    
4. <span data-ttu-id="b8b5e-298">Ausführen der Abfrage.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-298">Execute the Query.</span></span>
    
   ```cs
    projContext.ExecuteQuery()
   ```

5. <span data-ttu-id="b8b5e-299">Erstellen Sie mithilfe dieser Informationen auf dem Client eine Anforderung an die benutzerdefinierten Feldern, die dem aktuellen Projekt zugeordnete abrufen.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-299">With this information on the client, build a request to retrieve the custom fields associated with the current project.</span></span>
    
   ```cs
    foreach (PublishedProject pubProj in projContext.Projects)
    {
        //Console.WriteLine("\n\t{0}. \t{1} \n\t\t{2} \n\t\t{3} \n", 
                j++, pubProj.Id, pubProj.Name, pubProj.CreatedDate);
        CustomFieldCollection collCustF = pubProj.CustomFields;
                        
        projContext.Load(collCustF);
        projContext.ExecuteQuery();
    
   ```

6. <span data-ttu-id="b8b5e-300">Suchen Sie die entsprechenden benutzerdefinierten Felds, und rufen Sie den internen Namen des Felds.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-300">Locate the appropriate custom field and retrieve the internal name of the field.</span></span> 
    
   ```cs
        foreach (CustomField oCF in collCustF)
        {
            if (oCF.Name == "Project Health")
            {
                Console.WriteLine("Name: {0}", oCF.Name);
                Console.WriteLine("InternalName: {0}", oCF.InternalName);
    
   ```

   <span data-ttu-id="b8b5e-301">Der interne Name des benutzerdefinierten Felds wird abgerufen.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-301">The internal name of the custom field is retrieved.</span></span> <span data-ttu-id="b8b5e-302">Elemente auf oberster Ebene 1 und 2 sind jetzt abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-302">High-level items 1 and 2 are now complete.</span></span>
    
7. <span data-ttu-id="b8b5e-303">Die Projekt-Kontext zurück, und rufen Sie den Wert des benutzerdefinierten Felds.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-303">Return to the project context and retrieve the value of the custom field.</span></span>
    
   ```cs
    Console.WriteLine("Value: {0}", 
        pubProj.IncludeCustomFields.FieldValues[oCF.InternalName]);
    
   ```

   > [!NOTE]
   > <span data-ttu-id="b8b5e-304">Der Wert des benutzerdefinierten Felds ist mit den internen Namen als Index abgerufen.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-304">The value of the custom field is retrieved using the internal name as an index.</span></span> 
  
<span data-ttu-id="b8b5e-305">Ausgabe des Project-ID, Name des Projekts, Name des benutzerdefinierten Felds, interne Name des benutzerdefinierten Felds und der Wert des benutzerdefinierten Felds bestehend aus drei Projekte.</span><span class="sxs-lookup"><span data-stu-id="b8b5e-305">Output of three projects consisting of project ID, project Name, custom field name, custom field internal name, and custom field value.</span></span>
  
```cs
Project counts:31
1. Project ID:  957d5fcd-5cbf-e111-9f1e-00155d022681
        Name:           Acquisition Target Analysis
Name: Project Health
InternalName: Custom_745de6dfcfb4e11195dc00155d02c97f
Value: Green
2. Project ID:  16905202-5fbf-e111-9f1e-00155d022681
        Name:           Apparel ERP Upgrade
Name: Project Health
InternalName: Custom_745de6dfcfb4e11195dc00155d02c97f
Value: Green
3. Project ID:  dce23152-63bf-e111-9f1e-00155d022681
        Name:           Audit Tracking Solution
Name: Project Health
InternalName: Custom_745de6dfcfb4e11195dc00155d02c97f
Value: Red

```

## <a name="see-also"></a><span data-ttu-id="b8b5e-306">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8b5e-306">See also</span></span>

<span data-ttu-id="b8b5e-307">Dokumentation und Beispiele im Zusammenhang mit Project Online und die Anwendungsentwicklung mithilfe von CSOM finden Sie im [Projekt Development Portal](http://dev.office.com/project.aspx).</span><span class="sxs-lookup"><span data-stu-id="b8b5e-307">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](http://dev.office.com/project.aspx).</span></span>
    
