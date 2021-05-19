---
title: Arbeiten mit digitalen Signaturen mithilfe des InfoPath 2003-Objektmodells
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- Digitale Signaturen [infopath 2007], infopath 2003-kompatible Formularvorlagen,InfoPath 2003-kompatible Formularvorlagen, digitale Signaturen
localization_priority: Normal
ms.assetid: d6318238-fd45-4854-a3c9-c27c5685bd6b
description: Das InfoPath 2003-kompatible Objektmodell bietet Features zum programmgesteuerten Verwenden von digitalen Signaturen.
ms.openlocfilehash: 86e2c85c7515c896612df09b6186462480ceff61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433444"
---
# <a name="work-with-digital-signatures-using-the-infopath-2003-object-model"></a><span data-ttu-id="b7929-104">Arbeiten mit digitalen Signaturen mithilfe des InfoPath 2003-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="b7929-104">Work with Digital Signatures Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="b7929-105">Das InfoPath 2003-kompatible Objektmodell bietet Features zum programmgesteuerten Verwenden von digitalen Signaturen.</span><span class="sxs-lookup"><span data-stu-id="b7929-105">The InfoPath 2003-compatible object model provides features for working with digital signatures programmatically.</span></span>
  
## <a name="digital-signature-features"></a><span data-ttu-id="b7929-106">Features für digitale Signaturen</span><span class="sxs-lookup"><span data-stu-id="b7929-106">Digital Signature Features</span></span>

<span data-ttu-id="b7929-107">Mithilfe der Features für digitale Signaturen in InfoPath können Sie Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="b7929-107">The digital signatures features available in InfoPath enable you to:</span></span> 
  
- <span data-ttu-id="b7929-108">Ermöglichen von Signaturen für das gesamte Formular oder für bestimmte Gruppen von Daten im Formular, die getrennt signiert werden können.</span><span class="sxs-lookup"><span data-stu-id="b7929-108">Enable signatures for the entire form, or for specific sets of data in the form that can be signed separately.</span></span>
    
- <span data-ttu-id="b7929-p101">Angeben bei jeder signierbaren Datengruppe, ob einzelne oder mehrere Signaturen zulässig sind und in welcher Beziehung diese zueinander stehen sollen. So können Sie beispielsweise angeben, ob es sich um parallele gemeinsame Signaturen handelt oder ob alle früheren Signaturen durch jede neue Signatur gegengezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="b7929-p101">Specify, for each set of data that can be signed, whether a single signature or multiple signatures are allowed and what their relationship will be. For example, you can specify whether they are parallel co-signatures or whether each new signature countersigns all the earlier signatures.</span></span>
    
- <span data-ttu-id="b7929-111">Angeben einer Meldung, die angezeigt werden soll, wenn Benutzer das Formular signieren.</span><span class="sxs-lookup"><span data-stu-id="b7929-111">Specify a message to be shown to form users as they sign the form.</span></span>
    
- <span data-ttu-id="b7929-112">Einfügen und Anzeigen einer Signatur im Dokument.</span><span class="sxs-lookup"><span data-stu-id="b7929-112">Insert and see a signature in the document.</span></span> 
    
- <span data-ttu-id="b7929-p102">Anzeigen überprüfbarer Nichtabstreitbarkeitsinformationen, die jeder Signatur zur Steigerung der Sicherheit hinzugefügt wurden. Diese zusätzlichen Informationen, die eine Ansicht des Formulars einschließen, wie es jeder signierenden Person vorgelegt wurde, sind ein Bestandteil der Signatur und können nicht entfernt werden, ohne die Signatur ungültig zu machen. Sie können diese Daten jederzeit erneut aufrufen, indem Sie auf die Signatur im Formular klicken, um das Dialogfeld **Digitale Signatur überprüfen** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b7929-p102">View verifiable non-repudiation information that has been added to each signature for increased security. This additional information, which includes a view of the form as it was presented to each signer, is part of the signature and cannot be removed without invalidating the signature. At any time, you can recall this data by clicking on the signature in the form to display the **Verify Digital Signature** dialog box.</span></span> 
    
- <span data-ttu-id="b7929-p103">Profitieren von einem umfangreicheren Objektmodell zum Arbeiten mit digitalen Signaturen. Fügen Sie dem Signaturblock in vollständig vertrauenswürdigen Formularen benutzerdefinierte Informationen zum Objektmodell für digitale Signaturen hinzu. </span><span class="sxs-lookup"><span data-stu-id="b7929-p103">Take advantage of an object model for working with digital signatures. Add custom information to the signature block in fully trusted forms through the digital signature object model.</span></span> 
    
## <a name="overview-of-the-digital-signatures-object-model"></a><span data-ttu-id="b7929-118">Übersicht über das Objektmodell für digitale Signaturen</span><span class="sxs-lookup"><span data-stu-id="b7929-118">Overview of the Digital Signatures Object Model</span></span>

### <a name="events"></a><span data-ttu-id="b7929-119">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="b7929-119">Events</span></span>

<span data-ttu-id="b7929-120">Das Objektmodell für digitale Signaturen stellt das folgende Ereignis bereit.</span><span class="sxs-lookup"><span data-stu-id="b7929-120">The object model for digital signatures provides the following event.</span></span>
  
|<span data-ttu-id="b7929-121">**Name**</span><span class="sxs-lookup"><span data-stu-id="b7929-121">**Name**</span></span>|<span data-ttu-id="b7929-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b7929-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b7929-123">OnSign</span><span class="sxs-lookup"><span data-stu-id="b7929-123">OnSign</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx) <br/> |<span data-ttu-id="b7929-124">Tritt ein, nachdem eine signierbare Datengruppe zum Signieren ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="b7929-124">Occurs after a set of signable data has been selected to sign.</span></span>  <br/> <span data-ttu-id="b7929-p104">Mithilfe dieses Ereignisses können Sie die in der digitalen Signatur gespeicherten Daten bearbeiten. So können Sie beispielsweise Daten eines vertrauenswürdigen Zeitstempelservers oder eine serverseitige Gegensignatur der Transaktion hinzufügen. Sie können mit diesem Ereignis auch Signaturen blockieren, wenn der aktuelle Benutzer kein Mitglied einer bestimmten Gruppe ist.</span><span class="sxs-lookup"><span data-stu-id="b7929-p104">You can use this event to manipulate the data stored within the digital signature. For example, you can add data from a trusted timestamp server, or add a server-side countersignature of the transaction. You can also use this event to block signing if the current user is not a member of a particular group.</span></span>  <br/> |
   
<span data-ttu-id="b7929-128">Das **OnSign-Ereignis** gibt einen Verweis auf das [SignEventObject-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEventObject.aspx) zurück, das die folgenden Eigenschaften bietet.</span><span class="sxs-lookup"><span data-stu-id="b7929-128">The **OnSign** event returns a reference to the [SignEventObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEventObject.aspx) object, which provides the following properties.</span></span> 
  
|<span data-ttu-id="b7929-129">**Name**</span><span class="sxs-lookup"><span data-stu-id="b7929-129">**Name**</span></span>|<span data-ttu-id="b7929-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b7929-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b7929-131">ReturnStatus</span><span class="sxs-lookup"><span data-stu-id="b7929-131">ReturnStatus</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SignEvent.ReturnStatus.aspx) <br/> |<span data-ttu-id="b7929-132">Ruft einen Wert vom Typ **Boolean** ab, der den Rückgabestatus des **OnSign**-Ereignisses angibt, oder legt diesen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="b7929-132">Gets or sets a **Boolean** value indicating the return status of the **OnSign** event.</span></span>  <br/> |
|[<span data-ttu-id="b7929-133">SignedDataBlock</span><span class="sxs-lookup"><span data-stu-id="b7929-133">SignedDataBlock</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SignEvent.SignedDataBlock.aspx) <br/> |<span data-ttu-id="b7929-134">Ruft den signierten Datenblock ab, durch den das **OnSign**-Ereignis ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="b7929-134">Gets the signed data block that triggered the **OnSign** event.</span></span>  <br/> |
|[<span data-ttu-id="b7929-135">XDocument</span><span class="sxs-lookup"><span data-stu-id="b7929-135">XDocument</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.XDocument.aspx) <br/> |<span data-ttu-id="b7929-136">Ruft einen Verweis auf das **XDocument**-Objekt ab, das dem **OnSign**-Ereignis zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b7929-136">Gets a reference to the **XDocument** object associated with the **OnSign** event.</span></span>  <br/> |
   
### <a name="collections-and-objects"></a><span data-ttu-id="b7929-137">Auflistungen und Objekte</span><span class="sxs-lookup"><span data-stu-id="b7929-137">Collections and Objects</span></span>

<span data-ttu-id="b7929-138">Das Objektmodell für digitale Signaturen stellt die folgenden Auflistungen bereit.</span><span class="sxs-lookup"><span data-stu-id="b7929-138">The object model for digital signatures provides the following collections.</span></span>
  
|<span data-ttu-id="b7929-139">**Name**</span><span class="sxs-lookup"><span data-stu-id="b7929-139">**Name**</span></span>|<span data-ttu-id="b7929-140">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b7929-140">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b7929-141">SignedDataBlocksCollection</span><span class="sxs-lookup"><span data-stu-id="b7929-141">SignedDataBlocksCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlocksCollection.aspx) <br/> |<span data-ttu-id="b7929-142">Die Auflistung der [SignedDataBlockObject-Objekte](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlockObject.aspx) in der Formularvorlage, wie in der Formulardefinitionsdatei (XSF) definiert.</span><span class="sxs-lookup"><span data-stu-id="b7929-142">The collection of the [SignedDataBlockObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlockObject.aspx) objects in the form template as defined in the form definition file (.xsf).</span></span>  <br/> <span data-ttu-id="b7929-143">Die **SignedDataBlocksCollection**-Auflistung implementiert Eigenschaften, die den Zugriff auf die einem Formular zugeordneten **SignedDataBlockObjects**-Objekte ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="b7929-143">The **SignedDataBlocksCollection** collection implements properties that can be used to access the **SignedDataBlockObjects** objects associated with a form.</span></span> <span data-ttu-id="b7929-144">Auf **die SignedDataBlocks-Auflistung** kann über die [SignedDataBlocks-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SignedDataBlocks.aspx) des [XDocument-Objekts zugegriffen](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) werden.</span><span class="sxs-lookup"><span data-stu-id="b7929-144">The **SignedDataBlocks** collection is accessible through the [SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SignedDataBlocks.aspx) property of the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) object.</span></span>  <br/> |
|[<span data-ttu-id="b7929-145">SignaturesCollection</span><span class="sxs-lookup"><span data-stu-id="b7929-145">SignaturesCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignaturesCollection.aspx) <br/> |<span data-ttu-id="b7929-146">Enthält eine Auflistung von [SignatureObject-Objekten](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignatureObject.aspx) für jedes **SignedDataBlockObject-Objekt** im Formular.</span><span class="sxs-lookup"><span data-stu-id="b7929-146">Contains a collection of [SignatureObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignatureObject.aspx) objects for each **SignedDataBlockObject** in the form.</span></span>  <br/> <span data-ttu-id="b7929-p106">Die **SignaturesCollection**-Auflistung implementiert Eigenschaften und eine Methode, um auf die zugeordneten **SignatureObject**-Objekte eines Formulars zuzugreifen und eine Signatur zu erstellen. Der Zugriff darauf ist über das **SignedDataBlockObject**-Objekt möglich. </span><span class="sxs-lookup"><span data-stu-id="b7929-p106">The **SignaturesCollection** collection implements properties and a method that can be used to access a form's associated **SignatureObject** objects and to create a signature. It is accessible through the **SignedDataBlockObject** object.  </span></span><br/> <span data-ttu-id="b7929-149">Wenn Sie die [Create-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signatures.Create.aspx) der **SignaturesCollection-Auflistung** verwenden, beachten Sie, dass die Signatur erst geschrieben wird, wenn die [Sign-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) für das **SignatureObject-Objekt aufgerufen** wird.</span><span class="sxs-lookup"><span data-stu-id="b7929-149">When you use the [Create](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signatures.Create.aspx) method of the **SignaturesCollection** collection, keep in mind that the signature is not written until the [Sign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) method is called on the **SignatureObject** object.</span></span> <span data-ttu-id="b7929-150">Diese Methoden können nur vom **OnSign**-Ereignishandler einer vollständig vertrauenswürdigen Formularvorlage aus aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b7929-150">These methods can be called only from the **OnSign** event handler of a fully trusted form template.</span></span>  <br/> |
   
<span data-ttu-id="b7929-151">Das Objektmodell für digitale Signaturen stellt die folgenden Objekte bereit.</span><span class="sxs-lookup"><span data-stu-id="b7929-151">The object model for digital signatures provides the following objects.</span></span>
  
|<span data-ttu-id="b7929-152">**Name**</span><span class="sxs-lookup"><span data-stu-id="b7929-152">**Name**</span></span>|<span data-ttu-id="b7929-153">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b7929-153">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b7929-154">SignedDataBlockObject</span><span class="sxs-lookup"><span data-stu-id="b7929-154">SignedDataBlockObject</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlockObject.aspx) <br/> |<span data-ttu-id="b7929-p108">Stellt eine signierbare Datengruppe in einem Formular dar. Das **SignedDataBlock**-Objekt stellt eine Reihe von Eigenschaften und eine Methode für die programmgesteuerte Interaktion mit einer signierbaren Datengruppe bereit.</span><span class="sxs-lookup"><span data-stu-id="b7929-p108">Represents a set of signable data in a form. The **SignedDataBlock** object provides a number of properties and one method that can be used to programmatically interact with a set of signable data.  </span></span><br/> |
|[<span data-ttu-id="b7929-157">SignatureObject</span><span class="sxs-lookup"><span data-stu-id="b7929-157">SignatureObject</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignatureObject.aspx) <br/> |<span data-ttu-id="b7929-158">Stellt eine digitale Signatur dar, die einem Formular oder einer signierbaren Datengruppe in einem Formular hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b7929-158">Represents a digital signature that has been added to a form or set of signable data in a form.</span></span> <span data-ttu-id="b7929-159">Die **SignatureObject-Auflistung** implementiert Eigenschaften, die verwendet werden können, um Informationen zur digitalen Signatur abzurufen, und die [Sign-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) zum Schreiben des digitalen #A0 und zum Berechnen des kryptografischen Hashwerts.</span><span class="sxs-lookup"><span data-stu-id="b7929-159">The **SignatureObject** collection implements properties that can be used to retrieve information about the digital signature, and the [Sign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) method for writing the XML digital signature block and computing its cryptographic hash value.</span></span>  <br/> |
|[<span data-ttu-id="b7929-160">CertificateObject</span><span class="sxs-lookup"><span data-stu-id="b7929-160">CertificateObject</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.CertificateObject.aspx) <br/> |<span data-ttu-id="b7929-161">Stellt das digitale X.509-Zertifikat dar, das zum Erstellen der Signatur verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="b7929-161">Represents the X.509 digital certificate that has been used to create the signature.</span></span>  <br/> |
   
## <a name="working-with-digital-signatures-programmatically"></a><span data-ttu-id="b7929-162">Programmgesteuertes Arbeiten mit digitalen Signaturen</span><span class="sxs-lookup"><span data-stu-id="b7929-162">Working with Digital Signatures Programmatically</span></span>

<span data-ttu-id="b7929-p110">Das InfoPath 2003-kompatible Objektmodell stellt Member für die programmgesteuerte Interaktion mit digitalen Signaturen bereit. So können insbesondere in vollständig vertrauenswürdigen Formularen benutzerdefinierte Informationen dem Signaturblock hinzugefügt werden, bevor ein Commit für ihn ausgeführt wird. Dies geschieht entsprechend dem folgenden Zeitplan:</span><span class="sxs-lookup"><span data-stu-id="b7929-p110">The InfoPath 2003-compatible object model provides members for interacting with digital signatures programmatically. In particular, fully-trusted forms can add custom information to the signature block before it is committed, according to the following timeline:</span></span>
  
1. <span data-ttu-id="b7929-165">Der Benutzer entscheidet, dass einem Formular eine digitale Signatur hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b7929-165">User chooses to add a digital signature to a form.</span></span>
    
2. <span data-ttu-id="b7929-166">Das erste Fenster desAssistenten für digitale Signaturen wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b7929-166">The first panel of the **Digital Signature Wizard** is displayed.</span></span> 
    
3. <span data-ttu-id="b7929-167">Das **OnSign**-Ereignis für die ausgewählten Daten, die durch das **SignedDataBlockObject**-Objekt dargestellt werden, wird ausgelöst. Die **Sign**-Methode des **SignedDataBlockObject**-Objekts und die **Create**-Methode der **SignaturesCollection**-Auflistung werden ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b7929-167">The **OnSign** event for the selected data represented by the **SignedDataBlockObject** object is raised, and the **Sign** method of **SignedDataBlockObject** and the **Create** method of the **SignaturesCollection** collection are executed.</span></span> 
    
4. <span data-ttu-id="b7929-168">Alle optionalen benutzerdefinierten Aktionen werden ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b7929-168">Any optional custom actions are executed.</span></span>
    
5. <span data-ttu-id="b7929-169">Die **Sign**-Methode des **SignatureObject**-Objekts wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b7929-169">The **Sign** method of the **SignatureObject** is executed.</span></span> 
    
6. <span data-ttu-id="b7929-170">Das zweite und dritte Fenster des Assistenten werden angezeigt, in denen ein Zertifikat zum Signieren ausgewählt und Kommentare eingegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="b7929-170">Second and third panes of the wizard are displayed for selecting a certificate to sign with and to enter comments.</span></span>
    
7. <span data-ttu-id="b7929-171">Die Nichtabstreitbarkeitsinformationen werden angezeigt (und können später im Dialogfeld **Digitale Signatur überprüfen** angezeigt werden).</span><span class="sxs-lookup"><span data-stu-id="b7929-171">The non-repudiation information is displayed (which can be viewed later with the **Verify Digital Signature** dialog box).</span></span> 
    
8. <span data-ttu-id="b7929-172">Beim Klicken auf die Schaltfläche **Signieren** wird die Signatur der Auflistung von Signaturen für das Formular hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b7929-172">When the **Sign** button is clicked, the signature is added to collection of signatures for the form.</span></span> 
    
<span data-ttu-id="b7929-173">Im folgenden Beispiel wird das Dialogfeld **Signieren** aufgerufen und verwendet, um eine Signatur mit einem Zeitstempelwert gegenzuzeichnen, der von einem vertrauenswürdigen Zeitstempeldienst abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="b7929-173">The following example invokes the **Sign** dialog box and countersigns the signature with a timestamp value retrieved from a trusted timestamp service.</span></span> 
  
```cs
[InfoPathEventHandler(EventType=InfoPathEventType.OnSign)]
public void OnSign(SignEvent e)
{
    Signature signature = e.SignedDataBlock.Signatures.Create();
    // Invoke the Sign dialog box to sign the data block.
    signature.Sign();
    // Countersign the signature with a trusted timestamp
    // Get the XML node storing the signature block
    IXMLDOMNode oNodeSig = signature.SignatureBlockXmlNode;
    IXMLDOMNode oNodeSigValue = oNodeSig.selectSingleNode(".//*[local-name(.)='signatureValue']");
    // Get timestamp from a trusted timestamp service (fictitious).
    MyTrustedTimeStampService s = new MyTrustedTimeStampService();
    string strVerifiedTimeStamp = s.AddTimeStamp(oNodeSigValue.text);
    
    //Add the value returned from the timestamp service to the 
    //unsigned part of the signature block
    IXMLDOMNode oNodeObj = oNodeSig.selectSingleNode(".//*[local-name(.)='Object']");
    IXMLDOMNode oNode = oNodeObj.cloneNode(false);
    oNode.text = strVerifiedTimeStamp;
    oNodeObj.parentNode.appendChild(oNode);
    e.ReturnStatus = true;
}
```


