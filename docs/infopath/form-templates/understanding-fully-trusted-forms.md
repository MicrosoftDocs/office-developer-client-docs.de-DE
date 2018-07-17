---
title: Grundlegendes zu voll vertrauenswürdigen Formularen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 64d62990-6275-edef-c639-b6ba8d10c38c
description: InfoPath bietet die Möglichkeit, voll vertrauenswürdige Formulare erstellen Formulare, die größere Sicherheitsberechtigungen und Systemressourcen und anderen Komponenten auf dem Computer eines Benutzers zugreifen können. In diesem Artikel wird beschrieben, was ein voll vertrauenswürdiges Formular ist, und warum wird verwendet, und erstellen Sie ein voll vertrauenswürdiges Formular manuell konvertieren und Registrieren eines Standardformulars oder beim digitalen Signieren eines Standardformulars.
ms.openlocfilehash: b410d5bee0080aae5e0af9687999595655b42edf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790841"
---
# <a name="understanding-fully-trusted-forms"></a><span data-ttu-id="9b570-104">Grundlegendes zu voll vertrauenswürdigen Formularen</span><span class="sxs-lookup"><span data-stu-id="9b570-104">Understanding Fully Trusted Forms</span></span>

<span data-ttu-id="9b570-105">InfoPath bietet die Möglichkeit, voll vertrauenswürdige Formulare erstellen Formulare, die größere Sicherheitsberechtigungen und Systemressourcen und anderen Komponenten auf dem Computer eines Benutzers zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="9b570-105">InfoPath provides the ability to create fully trusted forms, which are forms that have greater security permissions and can access system resources and other components on a user's computer.</span></span> <span data-ttu-id="9b570-106">In diesem Artikel wird beschrieben, was ein voll vertrauenswürdiges Formular ist, und warum wird verwendet, und erstellen Sie ein voll vertrauenswürdiges Formular manuell konvertieren und Registrieren eines Standardformulars oder beim digitalen Signieren eines Standardformulars.</span><span class="sxs-lookup"><span data-stu-id="9b570-106">This article describes what a fully trusted form is, and why it is used, and create a fully trusted form by manually converting and registering a standard form, or by digitally signing a standard form.</span></span>

<span data-ttu-id="9b570-107">InfoPath-Formularvorlagen können mit unterschiedlichen Sicherheitsstufen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9b570-107">InfoPath form templates can be deployed with varying levels of security.</span></span> <span data-ttu-id="9b570-108">Die Ebene, die Sie verwenden, wird durch die Zugriffsebene zu externen Ressourcen vorgegeben, die ein Formular werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b570-108">The level you use is dictated by the level of access to external resources that you want a form to have.</span></span> <span data-ttu-id="9b570-109">In der Standardeinstellung InfoPath-Formularvorlagen aus den Zugriff auf Systemressourcen eingeschränkt werden und dürfen keine Softwarekomponenten, die nicht gekennzeichnet sind als sicher für Skripting verwenden.</span><span class="sxs-lookup"><span data-stu-id="9b570-109">By default, InfoPath form templates are restricted from accessing system resources and are not allowed to use any software components that are not marked as safe for scripting.</span></span> <span data-ttu-id="9b570-110">Dieses Verhalten kann jedoch überschrieben werden, damit ein Formular zugreifen kann, Systemressourcen und andere externen Ressourcen, einschließlich Softwarekomponenten, die nicht als sicher für Skripting gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="9b570-110">However, this behavior can be overridden so that a form can access system resources and other external resources, including software components that are not marked as safe for scripting.</span></span>
  
<span data-ttu-id="9b570-111">Für ein Formular kann verwendet werden muss InfoPath auf die Formularvorlage zugreifen, der das Formular basiert.</span><span class="sxs-lookup"><span data-stu-id="9b570-111">For a form to be used, InfoPath must be able to access the form template that the form is based on.</span></span> <span data-ttu-id="9b570-112">Wenn Sie eine Formularvorlage erstellen, erstellt InfoPath einen Eintrag in der Formulardefinitionsdatei (XSF) an, die die URL des Speicherorts der Formularvorlage enthält.</span><span class="sxs-lookup"><span data-stu-id="9b570-112">When you create a form template, InfoPath creates an entry in the form definition (.xsf) file that contains the URL of the location of the form template.</span></span> <span data-ttu-id="9b570-113">Ein URL-basiertes Formular wird als bezeichnet, *sandboxed*.</span><span class="sxs-lookup"><span data-stu-id="9b570-113">A URL-based form is said to be *sandboxed*.</span></span> <span data-ttu-id="9b570-114">Wenn ein Benutzer ausgefüllt wird, wird das Formular in einen lokalen Cache hinzugefügt und der Zugriff auf Systemressourcen verweigert.</span><span class="sxs-lookup"><span data-stu-id="9b570-114">When a user fills it out, the form is added in a local cache and denied access to system resources.</span></span> <span data-ttu-id="9b570-115">Diese Art von Formular erbt die Berechtigungen von der Domäne, in der es geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="9b570-115">This kind of form inherits its permissions from the domain in which it is opened.</span></span> 
  
<span data-ttu-id="9b570-116">Jedoch können Sie ein Formular ändern, damit sie auf einen Uniform Resource Name (URN) stattdessen basiert auf Systemressourcen zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="9b570-116">However, you can modify a form so that it is based on a Uniform Resource Name (URN) instead, which allows access to system resources.</span></span> <span data-ttu-id="9b570-117">Formulare dieser Art werden als *voll*vertrauenswürdig bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9b570-117">Forms of this kind are said to be *fully trusted*.</span></span> 
  
## <a name="why-use-a-fully-trusted-form"></a><span data-ttu-id="9b570-118">Gründe für die Verwendung von voll vertrauenswürdigen Formularen</span><span class="sxs-lookup"><span data-stu-id="9b570-118">Why Use a Fully Trusted Form?</span></span>

<span data-ttu-id="9b570-p106">Voll vertrauenswürdige Formulare verfügen über umfassendere Berechtigungen als Formulare mit eingeschränkter Sicherheitsstufe. Sie können beispielsweise Programmiercode enthalten, in dem über externe Objekte auf Systemressourcen zugegriffen wird. Sie können Softwarekomponenten oder Microsoft ActiveX-Steuerelemente verwenden, die nicht als sicher für die Verwendung von Skript gekennzeichnet sind, und sie können in .NET-Assemblys bereitgestellte benutzerdefinierte Geschäftslogik verwenden.</span><span class="sxs-lookup"><span data-stu-id="9b570-p106">Fully trusted forms have a better set of permissions than sandboxed forms. For example, they can contain programming code that uses external objects for accessing system resources, they can use software components or Microsoft ActiveX controls that are not marked as safe for scripting, and they can use custom business logic provided by .NET assemblies.</span></span>
  
<span data-ttu-id="9b570-121">Darüber hinaus werden einige Member des InfoPath-Objektmodells auf Sicherheitsstufe 3 festgelegt, was bedeutet, dass sie nur in einem voll vertrauenswürdigen Formular verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="9b570-121">In addition, some members of the InfoPath object model are set to security level 3, which means that they can only be used in a fully trusted form.</span></span> <span data-ttu-id="9b570-122">Beispielsweise verwenden, um das Microsoft Office- **CommandBars** -Objekt zuzugreifen, Sie die [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) -Eigenschaft des InfoPath- [Fenster](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) -Klasse um einen Verweis auf dieses festzulegen.</span><span class="sxs-lookup"><span data-stu-id="9b570-122">For example, to access the Microsoft Office **CommandBars** object, you use the [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) property of the InfoPath [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) class to set a reference to it.</span></span> <span data-ttu-id="9b570-123">Da diese Eigenschaft auf Sicherheitsstufe 3 festgelegt ist, kann nicht sie in einem Formular verwendet werden, das nicht vollständig vertrauenswürdig ist.</span><span class="sxs-lookup"><span data-stu-id="9b570-123">Because this property is set to security level 3, it cannot be used in a form that is not fully trusted.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9b570-124">Verwenden die [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) -Eigenschaft des [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) -Klasse oder eine beliebige andere Objektmodellelement, die Sicherheitsstufe 3 hat, führt in einem Formular, das nicht vollständig vertrauenswürdig ist ein Fehler "Berechtigung verweigert".</span><span class="sxs-lookup"><span data-stu-id="9b570-124">Using the [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) property of the [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) class, or any other object model member that has a security level of 3, in a form that is not fully trusted will result in a "permission denied" error.</span></span> 
  
## <a name="what-makes-a-form-fully-trusted"></a><span data-ttu-id="9b570-125">Wodurch wird ein Formular voll vertrauenswürdig?</span><span class="sxs-lookup"><span data-stu-id="9b570-125">What Makes a Form Fully Trusted?</span></span>

<span data-ttu-id="9b570-126">Zum Erstellen und Verwenden eines voll vertrauenswürdigen Formulars sind die folgenden Aktionen bezüglich der Benutzeroberfläche von InfoPath und der Formulardateien erforderlich:</span><span class="sxs-lookup"><span data-stu-id="9b570-126">The following actions, involving both the InfoPath user interface and the form files, are required to create and use a fully trusted form:</span></span>
  
- <span data-ttu-id="9b570-127">Aktivieren von InfoPath für die Verwendung von voll vertrauenswürdigen Formularen auf der Kategorie **Vertrauenswürdige Herausgeber** im Dialogfeld **Sicherheitscenter** zulassen.</span><span class="sxs-lookup"><span data-stu-id="9b570-127">Enabling InfoPath to allow for the use of fully trusted forms on the **Trusted Publishers** category of the **Trust Center** dialog box.</span></span> <span data-ttu-id="9b570-128">Diese Option muss für Benutzer voll vertrauenswürdige Formulare öffnen aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="9b570-128">This option must be enabled for users to open fully trusted forms.</span></span> 
    
- <span data-ttu-id="9b570-129">Registrieren des voll vertrauenswürdigen Formulars auf dem Zielcomputer mithilfe der **RegisterSolution** -Methode des InfoPath- **Application** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="9b570-129">Registering the fully trusted form on the target computer by using the **RegisterSolution** method of the InfoPath **Application** object.</span></span> 
    
## <a name="creating-a-fully-trusted-form"></a><span data-ttu-id="9b570-130">Erstellen eines voll vertrauenswürdigen Formulars</span><span class="sxs-lookup"><span data-stu-id="9b570-130">Creating a Fully Trusted Form</span></span>

- <span data-ttu-id="9b570-131">Sie können das Formular manuell erstellen. Dazu müssen Sie einige Formulardateien direkt ändern.</span><span class="sxs-lookup"><span data-stu-id="9b570-131">You can create the form manually, which involves modifying some of the form files directly.</span></span>
    
- <span data-ttu-id="9b570-132">Sie können die Formularvorlage digital signieren.</span><span class="sxs-lookup"><span data-stu-id="9b570-132">You can digitally sign the form template.</span></span>
    
### <a name="manually-creating-a-fully-trusted-form"></a><span data-ttu-id="9b570-133">Manuelles Erstellen eines voll vertrauenswürdigen Formulars</span><span class="sxs-lookup"><span data-stu-id="9b570-133">Manually Creating a Fully Trusted Form</span></span>

#### <a name="to-manually-create-a-fully-trusted-form"></a><span data-ttu-id="9b570-134">So erstellen Sie ein voll vertrauenswürdiges Formular manuell</span><span class="sxs-lookup"><span data-stu-id="9b570-134">To manually create a fully trusted form</span></span>

1. <span data-ttu-id="9b570-135">Erstellen Sie eine Sicherungskopie der Formularvorlage, die Sie zu einer voll vertrauenswürdigen Formularvorlage machen möchten.</span><span class="sxs-lookup"><span data-stu-id="9b570-135">Make a backup copy of the form template that you want to make fully trusted.</span></span>
    
2. <span data-ttu-id="9b570-136">Öffnen Sie die Formularvorlage in InfoPath.</span><span class="sxs-lookup"><span data-stu-id="9b570-136">Open the form template in InfoPath.</span></span>
    
3. <span data-ttu-id="9b570-137">Speichern Sie das Formular Quelldateien in einen Ordner auf der Festplatte, indem Sie auf der Registerkarte **Datei** auf **Veröffentlichen**, und dann auf **Quelldateien exportieren**.</span><span class="sxs-lookup"><span data-stu-id="9b570-137">Save the form source files to a folder on your hard disk by clicking the **File** tab, clicking **Publish**, and then clicking **Export Source Files**.</span></span>
    
4. <span data-ttu-id="9b570-138">Geben Sie den Ordner, in dem die Quelldateien des Formulars zu speichern, klicken Sie auf **OK**, und beenden Sie den InfoPath-Designer.</span><span class="sxs-lookup"><span data-stu-id="9b570-138">Specify the folder in which to save the form source files, click **OK**, and then exit the InfoPath designer.</span></span>
    
5. <span data-ttu-id="9b570-139">Öffnen Sie in den Ordner, in dem Sie die Dateien extrahiert haben, die Formulardefinitionsdatei (XSF)-Datei mit dem Namen `manifest.xsf` standardmäßig in einem Texteditor wie beispielsweise Microsoft Notepad.</span><span class="sxs-lookup"><span data-stu-id="9b570-139">In the folder in which you extracted the form files, open the form definition (.xsf) file, named  `manifest.xsf` by default, in a text editor such as Microsoft Notepad.</span></span> 
    
6. <span data-ttu-id="9b570-140">Fügen Sie dem **xDocumentClass** -Element in der XSF-Datei die folgenden Attribute:</span><span class="sxs-lookup"><span data-stu-id="9b570-140">Add the following attributes to the **xDocumentClass** element in the .xsf file:</span></span> 
   
   `requireFullTrust="yes"`<br/>
   `name="urn:MyForm:MyCompany`

   > [!NOTE]
   > Die Werte, die für den URN verwendet werden können beliebigen Typs String-Wert sein, solange dieser Wert eindeutig ist. Es muss mindestens zwei Werte nach der `urn:` Präfix und diese Werte durch einen Doppelpunkt getrennt werden müssen. <span data-ttu-id="9b570-143">Darüber hinaus sollten der URN 255 Zeichen nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="9b570-143">In addition, the URN should not exceed 255 characters.</span></span> 
  
7. <span data-ttu-id="9b570-144">Speichern und schließen Sie die XSF-Datei, und öffnen Sie die XML-Vorlagendatei (XML) mit dem Namen `Template.xml` standardmäßig in einem Text-Editor wie Editor.</span><span class="sxs-lookup"><span data-stu-id="9b570-144">Save and close the .xsf file, and then open the XML template (.xml) file that is named  `Template.xml` by default, in a text editor such as Notepad.</span></span> 
    
8. <span data-ttu-id="9b570-145">Entfernen Sie das **Href** -Attribut aus der `mso-infoPathSolution` verarbeitungsanweisung, und Ersetzen Sie es durch dasselbe **Name** -Attribut, das Sie in Schritt 6 für die XSF-Datei verwendet.</span><span class="sxs-lookup"><span data-stu-id="9b570-145">Remove the **href** attribute from the  `mso-infoPathSolution` processing instruction and replace it with the same **name** attribute that you used in step 6 for the .xsf file.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="9b570-146">Die URN-Werte, die für das **Name** -Attribut verwendet werden müssen in der XSF-Datei und die XML-Vorlagendatei übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9b570-146">The URN values that are used for the **name** attribute must be the same in both the .xsf file and XML template file.</span></span> 
  
9. <span data-ttu-id="9b570-147">Speichern und schließen Sie die XML-Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="9b570-147">Save and close the XML template file.</span></span>
    
10. <span data-ttu-id="9b570-148">Verpacken Sie die Dateien mit einem Tool wie makecab.exe neu im CAB-Format (XSN-Datei).</span><span class="sxs-lookup"><span data-stu-id="9b570-148">Repackage the files into the .xsn CAB format with a tool such as makecab.exe.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="9b570-p110">Der InfoPath-Formulardesigner unterstützt zwar das Neuverpacken der Formulardateien in einer XSN-Datei, das Formular wird jedoch dabei wieder zu einem URL-basierten Formular. Daher müssen Sie die Dateien manuell verpacken, um zu verhindern, dass Ihre Änderungen in den Formulardateien überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="9b570-p110">Although InfoPath form designer supports repackaging the form files into an .xsn file, doing this will revert the form to a URL-based form. For this reason, you must repackage the files manually to avoid overwriting your changes to the form files.</span></span> 
  
11. <span data-ttu-id="9b570-151">Erstellen eines benutzerdefinierten Installationsprogramms mithilfe der **RegisterSolution** -Methode des InfoPath- **Application** -Objekts zum Installieren des voll vertrauenswürdigen Formulars.</span><span class="sxs-lookup"><span data-stu-id="9b570-151">Create a custom installation program by using the **RegisterSolution** method of the InfoPath **Application** object to install the fully trusted form.</span></span> <span data-ttu-id="9b570-152">Eine einfache Möglichkeit hierzu ist eine Skriptdatei erstellen, die folgenden Codezeilen (in Microsoft JScript oder VBScript-Syntax) verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="9b570-152">A simple way to do this is to create a script file that uses the following lines of code (in either Microsoft JScript or VBScript syntax):</span></span> 
    
    ```js
        objIPApp = new ActiveXObject("InfoPath.Application"); 
        objIPApp.RegisterSolution("C:\\MyForms\\MyTrustedForm.xsn"); 
        objIPApp.Quit(); 
        objIPApp = null;
    ```
   
    ```vb
        Public Sub InstallForm()
            Dim objIPApp As Object
            ' Create a reference to the Application object.
            Set objIPApp = CreateObject("InfoPath.Application")
            ' Register the InfoPath form template.
            objIPApp.RegisterSolution ("C:\\My Forms\\MyFormTemplate.xsn")
            MsgBox "The InfoPath form template has been registered."
            Set objIPApp = Nothing
        End Sub
        
    ```

> [!NOTE] 
> <span data-ttu-id="9b570-153">Obwohl in diesem Beispiel wird eine einfache Skriptdatei verwendet wird, können Sie auch einen robusteren Installationsmechanismus wie Microsoft Windows Installer (MSI)-Dateien.</span><span class="sxs-lookup"><span data-stu-id="9b570-153">Although this example uses a simple script file, you can also use a more robust installation mechanism such as Microsoft Windows Installer (.msi) files.</span></span> <span data-ttu-id="9b570-154">Unbedingt, allerdings mit der **RegisterSolution** -Methode des voll vertrauenswürdigen Formulars auf dem Zielcomputer korrekt installiert.</span><span class="sxs-lookup"><span data-stu-id="9b570-154">Be sure, however, to use the **RegisterSolution** method to correctly install the fully trusted form on the target computer.</span></span> <span data-ttu-id="9b570-155">Legen Sie einen Verweis auf die Microsoft InfoPath 3.0-Typbibliothek, die vom IPEDITOR.dll bereitgestellt wird, die in der C:\Program installiert ist, um die **RegisterSolution** -Methode des **Application** -Objekts InfoPath in Visual Basic oder Visual Studio zugreifen Ordner c:\Programme\Microsoft Office\Office14.</span><span class="sxs-lookup"><span data-stu-id="9b570-155">To access the **RegisterSolution** method of the InfoPath the **Application** object from Visual Basic or Visual Studio, set a reference to the Microsoft InfoPath 3.0 Type Library, which is provided by IPEDITOR.dll that is installed in the C:\Program Files\Microsoft Office\Office14 folder.</span></span> 
  
<span data-ttu-id="9b570-156">Wenn Sie ein voll vertrauenswürdiges Formular entfernt haben, können Sie die **UnregisterSolution** -Methode des **Application** -Objekts verwenden, wie in den folgenden JScript- und VBScript-Beispielen gezeigt.</span><span class="sxs-lookup"><span data-stu-id="9b570-156">If you have to remove a fully trusted form, you can use the **UnregisterSolution** method of the **Application** object as shown in the following JScript and VBScript examples.</span></span> 
    
```js
    objIPApp = new ActiveXObject("InfoPath.Application"); 
    objIPApp.UnregisterSolution("C:\\MyForms\\MyTrustedForm.xsn"); 
    objIPApp.Quit(); 
    objIPApp = null;
```

```vb
    Public Sub UninstallForm()
        Dim objIPApp As Object
        ' Create a reference to the Application object.
        Set objIPApp = CreateObject("InfoPath.Application")
        ' Unregister the InfoPath form template.
        objIPApp.UnregisterSolution ("C:\My Forms\MyFormTemplate.xsn")
        MsgBox ("The InfoPath form template has been unregistered.")
        Set objIPApp = Nothing
    End Sub
    
```

### <a name="digitally-signing-a-form-template-to-create-a-fully-trusted-form"></a><span data-ttu-id="9b570-157">Digitales Signieren einer Formularvorlage zum Erstellen eines voll vertrauenswürdigen Formulars</span><span class="sxs-lookup"><span data-stu-id="9b570-157">Digitally Signing a Form Template to Create a Fully Trusted Form</span></span>

<span data-ttu-id="9b570-158">Digitales Signieren einer Formularvorlage ermöglicht Ihnen die Bereitstellung einer voll vertrauenswürdigen Formularvorlage per e-Mail oder auf einem Webserver, wie beispielsweise einen Server mit Microsoft SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="9b570-158">Digitally signing a form template enables you to deploy a fully trusted form template by email or on a Web server, such as a server that is running Microsoft SharePoint Foundation.</span></span> <span data-ttu-id="9b570-159">Verwenden Sie die Schritte in den folgenden drei Verfahren, um Stellen Sie ein Formular voll vertrauenswürdig als voll vertrauenswürdig für das Formular digital signieren und anschließend veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="9b570-159">Use the steps in the following three procedures to make a form fully trusted by specifying full trust for the form, signing it digitally, and then publishing it.</span></span>
  
#### <a name="to-digitally-sign-a-form-template"></a><span data-ttu-id="9b570-160">So können Sie eine Formularvorlage digital signieren</span><span class="sxs-lookup"><span data-stu-id="9b570-160">To digitally sign a form template</span></span>

1. <span data-ttu-id="9b570-161">Öffnen Sie das Formular im InfoPath-Designer, klicken Sie auf der Registerkarte **Datei** , und klicken Sie dann auf der Registerkarte **Info** auf **Formularoptionen** .</span><span class="sxs-lookup"><span data-stu-id="9b570-161">Open the form in the InfoPath designer, click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
2. <span data-ttu-id="9b570-162">Klicken Sie im Dialogfeld **Formularoptionen** auf die Kategorie **Sicherheit und Vertrauensstellung** .</span><span class="sxs-lookup"><span data-stu-id="9b570-162">In the **Form Options** dialog box, click the **Security and Trust** category.</span></span> 
    
3. <span data-ttu-id="9b570-163">Deaktivieren Sie die Auswahl für **Sicherheitsstufe automatisch ermitteln (empfohlen)**.</span><span class="sxs-lookup"><span data-stu-id="9b570-163">Clear the selection for **Automatically determine security level (recommended)**.</span></span>
    
4. <span data-ttu-id="9b570-164">Wählen Sie **Voll vertrauenswürdig (das Formular verfügt über Zugriff auf Dateien und Einstellungen auf dem Computer des Benutzers)**.</span><span class="sxs-lookup"><span data-stu-id="9b570-164">Select **Full Trust (the form has access to files and settings on the user's computer)**.</span></span>
    
5. <span data-ttu-id="9b570-165">Wählen Sie unter **Signatur der Formularvorlage** **Diese Formularvorlage signieren**.</span><span class="sxs-lookup"><span data-stu-id="9b570-165">Under **Form Template Signature**, select **Sign this form template**.</span></span>
    
6. <span data-ttu-id="9b570-166">Klicken Sie auf **Zertifikat auswählen,** um ein Zertifikat auszuwählen, das zuvor heruntergeladen und von einem vertrauenswürdigen Zertifikatanbieter installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="9b570-166">Click **Select Certificate** to select a certificate that was previously downloaded and installed from a trusted certificate provider.</span></span> 
    
7. <span data-ttu-id="9b570-167">Klicken Sie zweimal auf OK, um den Vorgang vollständig zu beenden.</span><span class="sxs-lookup"><span data-stu-id="9b570-167">Click OK two times to exit completely.</span></span>
    
#### <a name="to-publish-the-form-template-to-a-sharepoint-document-library"></a><span data-ttu-id="9b570-168">So veröffentlichen Sie die Formularvorlage in einer SharePoint-Dokumentbibliothek</span><span class="sxs-lookup"><span data-stu-id="9b570-168">To publish the form template to a SharePoint Document Library</span></span>

1. <span data-ttu-id="9b570-169">Klicken Sie auf der Registerkarte **Datei** , klicken Sie auf **Veröffentlichen**, und klicken Sie dann auf **SharePoint Server**.</span><span class="sxs-lookup"><span data-stu-id="9b570-169">Click the **File** tab, click **Publish**, and then click **SharePoint Server**.</span></span>
    
2. <span data-ttu-id="9b570-170">Befolgen Sie die Anweisungen des **Veröffentlichungs-Assistenten** zum Veröffentlichen der Formularvorlage in einer neuen oder vorhandenen SharePoint-Dokumentbibliothek.</span><span class="sxs-lookup"><span data-stu-id="9b570-170">Follow the instructions in the **Publishing Wizard** to publish the form template to a new or existing SharePoint document library.</span></span> 
    
#### <a name="to-a-create-a-form-that-is-based-on-your-fully-trusted-digitally-signed-form-template"></a><span data-ttu-id="9b570-171">So erstellen Sie ein Formular auf der Basis der voll vertrauenswürdigen, digital signierten Formularvorlage</span><span class="sxs-lookup"><span data-stu-id="9b570-171">To a create a form that is based on your fully trusted, digitally signed form template</span></span>

1. <span data-ttu-id="9b570-172">Klicken Sie in der SharePoint-Dokumentbibliothek auf **Fill Out the Form**.</span><span class="sxs-lookup"><span data-stu-id="9b570-172">In the SharePoint document library, click **Fill Out the Form**.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="9b570-173">Nach dem Veröffentlichen der Formularvorlage in einer SharePoint-Dokumentbibliothek mit dem **Veröffentlichen-Assistenten**, wird die Vorlage nicht als ein Element in der Formularbibliothek angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9b570-173">After publishing the form template to a SharePoint document library using the **Publishing Wizard**, the template is not displayed as an item in the form library.</span></span> <span data-ttu-id="9b570-174">Wenn Sie ein Formular in dieser Dokumentbibliothek erstellen, wird die Vorlage standardmäßig als Vorlage für das neue Formular verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9b570-174">When you create a form in that document library, the template will be used by default as the template for the new form.</span></span> 
  
2. <span data-ttu-id="9b570-175">Wenn die Standard-Formularvorlage digital signiert wurde, zeigt InfoPath einen Sicherheitshinweis über digital signierten Formularvorlage an.</span><span class="sxs-lookup"><span data-stu-id="9b570-175">If the default form template was digitally signed, InfoPath displays a security warning about the digitally signed form template.</span></span> <span data-ttu-id="9b570-176">Wählen Sie **Always Dateien von dieser Quelle vertrauen und automatisch öffnen**, und klicken Sie dann auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="9b570-176">Select **Always trust files from this publisher and open them automatically**, and then click **Open**.</span></span>
    
## <a name="using-a-fully-trusted-form"></a><span data-ttu-id="9b570-177">Verwenden eines voll vertrauenswürdigen Formulars</span><span class="sxs-lookup"><span data-stu-id="9b570-177">Using a Fully Trusted Form</span></span>

<span data-ttu-id="9b570-p116">Ein voll vertrauenswürdiges Formular wird ähnlich verwendet wie ein Standardformular. Der wesentliche Unterschied besteht darin, dass das Formular auf beschränkte Ressourcen zugreifen kann und keine Warnungen mehr angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9b570-p116">Using a fully trusted form is very similar to using a standard form. The only significant differences are that the form can access restricted resources and warnings will no longer be displayed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="9b570-180">Um InfoPath verwenden ein voll vertrauenswürdiges Formulars zu aktivieren, müssen Benutzer sicherstellen, dass das Kontrollkästchen **Zulassen voll vertrauenswürdige Formulare auf meinem Computer ausführen** der Kategorie **Vertrauenswürdige Herausgeber** im Dialogfeld **Sicherheitscenter** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="9b570-180">To enable InfoPath to use a fully trusted form, users must ensure that the **Allow fully trusted forms to run on my computer** check box is selected on the **Trusted Publishers** category of the **Trust Center** dialog box.</span></span> <span data-ttu-id="9b570-181">Um das Dialogfeld **Trust Center** zu öffnen, klicken Sie auf der Registerkarte **Datei** , klicken Sie auf **Optionen** (unter der Registerkarte **InfoPath** ), klicken Sie auf **Sicherheitscenter**, und klicken Sie dann auf **Einstellungen für das Sicherheitscenter**.</span><span class="sxs-lookup"><span data-stu-id="9b570-181">To open the **Trust Center** dialog box, click the **File** tab, click **Options** (below the **InfoPath** tab), click **Trust Center**, and then click **Trust Center Settings**.</span></span> 
  
<span data-ttu-id="9b570-182">Ein voll vertrauenswürdiges Formular kann in InfoPath im Dialogfeld **Ein Formular ausfüllen** geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="9b570-182">A fully trusted form can be opened in InfoPath from the **Fill Out a Form** dialog box.</span></span> 
  
<span data-ttu-id="9b570-183">Das Dialogfeld **Ein Formular ausfüllen** geöffnet wird, wenn Sie auf **Weitere Formulare** im Aufgabenbereich **Ein Formular ausfüllen** , oder klicken Sie auf **Ein Formular ausfüllen** im Menü **Datei** .</span><span class="sxs-lookup"><span data-stu-id="9b570-183">The **Fill Out a Form** dialog box opens when you click **More Forms** in the **Fill Out a Form** task pane, or you click **Fill Out a Form** on the **File** menu.</span></span> 
  
### <a name="making-changes-to-a-fully-trusted-form"></a><span data-ttu-id="9b570-184">Ändern eines voll vertrauenswürdigen Formulars</span><span class="sxs-lookup"><span data-stu-id="9b570-184">Making Changes to a Fully Trusted Form</span></span>

<span data-ttu-id="9b570-p118">Wenn Sie nur die XSN-Datei ändern müssen, können Sie die Benutzer nach der Vornahme der Änderungen bitten, ihre vorhandenen XSN-Dateien durch die neue zu ersetzen. Die Benutzer müssen die Datei nicht mit einem benutzerdefinierten Installationsprogramm neu installieren.</span><span class="sxs-lookup"><span data-stu-id="9b570-p118">If you only have to make changes to the .xsn file, you can have users replace their existing .xsn file with the new one after the changes are made. They will not have to reinstall it by using a custom installation program.</span></span>
  
<span data-ttu-id="9b570-187">Wenn Sie jedoch Änderungen an den in der XSN-Datei enthaltenen Formulardateien vornehmen, müssen Sie die Dateien wie oben erläutert neu verpacken. Anschließend müssen die Benutzer das voll vertrauenswürdige Formular neu installieren.</span><span class="sxs-lookup"><span data-stu-id="9b570-187">However, if you are making changes to the form files that the .xsn file contains, you must repackage the files, as explained earlier, and then have users reinstall the fully trusted form.</span></span>
  
> [!NOTE]
> <span data-ttu-id="9b570-188">Die beste Methode ist es, die Formularvorlage im InfoPath-Designer erneut im XSN-Format zu speichern und dann mit den hier beschriebenen Schritten ein voll vertrauenswürdiges Formular zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9b570-188">The best approach is to save the form template back to the .xsn format from the InfoPath designer, and then follow the steps in this article to create a fully trusted form.</span></span> 
  
## <a name="conclusion"></a><span data-ttu-id="9b570-189">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="9b570-189">Conclusion</span></span>

<span data-ttu-id="9b570-p119">Abhängig von Ihren Unternehmensanforderungen und den Bedürfnissen der Benutzer müssen Sie unter Umständen ein Formular erstellen, das über höhere Berechtigungen verfügt als das InfoPath-Standardformular. In InfoPath können Formulare so geändert werden, dass sie Zugriff auf Systemressourcen und andere externe Ressourcen haben, die nicht als sicher für die Verwendung von Skript gekennzeichnet sind. Dies kann manuell durch Ändern der Formulardateien einer Formularvorlage und Ausführen eines Installationsskripts erfolgen oder durch digitales Signieren der Formularvorlage.</span><span class="sxs-lookup"><span data-stu-id="9b570-p119">Depending on your business requirements and the needs of your users, you may have to create a form that has a higher set of permissions than the standard InfoPath form. InfoPath provides the ability to modify a form so that it can access system resources and other external resources that are not marked as safe for scripting. This can be done manually by making modifications to the form files that a form template contains and running an installation script, or by digitally signing the form template.</span></span>
  
