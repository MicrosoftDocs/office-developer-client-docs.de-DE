---
title: Importieren von Termin-XML-Daten in Outlook-Terminobjekte
TOCTitle: Import appointment XML data into Outlook appointment objects
ms:assetid: 166a648a-1c48-4984-8889-a7614cc277b1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff462092(v=office.15)
ms:contentKeyID: 55119821
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0af86772fced3e69d1d28cf8d98a544e3b4d90d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320062"
---
# <a name="import-appointment-xml-data-into-outlook-appointment-objects"></a><span data-ttu-id="ab16b-102">Importieren von Termin-XML-Daten in Outlook-Terminobjekte</span><span class="sxs-lookup"><span data-stu-id="ab16b-102">Import appointment XML data into Outlook appointment objects</span></span>

<span data-ttu-id="ab16b-103">In diesem Thema wird gezeigt, wie Termindaten im XML-Format gelesen, die Daten in Outlook [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) -Objekten im Standardkalender gespeichert und die Terminobjekte in einem Array zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ab16b-103">This topic shows how to read appointment data formatted in XML, save the data to Outlook [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) objects in the default calendar, and return the appointment objects in an array.</span></span>

## <a name="example"></a><span data-ttu-id="ab16b-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ab16b-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="ab16b-105">Helmut Obertanner hat das folgende Codebeispiel bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ab16b-105">Helmut Obertanner provided the following code examples.</span></span> <span data-ttu-id="ab16b-106">Helmut verfügt über Fachwissen zu Office Developer Tools für Visual Studio und Outlook.</span><span class="sxs-lookup"><span data-stu-id="ab16b-106">Helmut's expertise is in Office Developer Tools for Visual Studio and Outlook.</span></span> 


<span data-ttu-id="ab16b-107">Die folgenden Codebeispiele enthalten die CreateAppointmentsFromXml-Methode der Sample-Klasse, die als Teil eines Outlook-Add-In-Projekts implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="ab16b-107">The following code examples contain the CreateAppointmentsFromXml method of the Sample class, implemented as part of an Outlook add-in project.</span></span> <span data-ttu-id="ab16b-108">Jedes Projekt fügt einen Verweis auf die primäre Interopassembly für Outlook hinzu, der auf dem [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\))-Namespace basiert.</span><span class="sxs-lookup"><span data-stu-id="ab16b-108">Each project adds a reference to the Outlook Primary Interop Assembly, which is based on the [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)) namespace.</span></span>

<span data-ttu-id="ab16b-109">Die CreateAppointmentsFromXml-Methode akzeptiert zwei Eingabeparameter:</span><span class="sxs-lookup"><span data-stu-id="ab16b-109">The CreateAppointmentsFromXml method accepts two input parameters:</span></span>

  - <span data-ttu-id="ab16b-110">application ist ein vertrauenswürdiges [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\))-Objekt von Outlook.</span><span class="sxs-lookup"><span data-stu-id="ab16b-110">application is a trusted Outlook [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) object.</span></span>

  - <span data-ttu-id="ab16b-p103">xml ist entweder eine XML-Zeichenfolge oder eine Zeichenfolge, die einen Pfad zu einer gültigen XML-Datei darstellt. In den folgenden Codebeispielen begrenzt der XML-Code Termindaten mithilfe der folgenden XML-Tags:</span><span class="sxs-lookup"><span data-stu-id="ab16b-p103">xml is either an XML string, or a string that represents a path to a valid XML file. For the purpose of the following code examples, the XML delimits appointment data by using the following XML tags:</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p><span data-ttu-id="ab16b-113">Termindaten</span><span class="sxs-lookup"><span data-stu-id="ab16b-113">Appointment data</span></span></p></th>
    <th><p><span data-ttu-id="ab16b-114">Trennendes XML-Tag</span><span class="sxs-lookup"><span data-stu-id="ab16b-114">Delimiting XML tag</span></span></p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="ab16b-115">Gesamter Satz an Termindaten</span><span class="sxs-lookup"><span data-stu-id="ab16b-115">Entire set of appointment data</span></span></p></td>
    <td><p><span data-ttu-id="ab16b-116">Termine</span><span class="sxs-lookup"><span data-stu-id="ab16b-116">appointments</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="ab16b-117">Jeder Termine in der Gruppe</span><span class="sxs-lookup"><span data-stu-id="ab16b-117">Each appointment in the set</span></span></p></td>
    <td><p><span data-ttu-id="ab16b-118">Termin</span><span class="sxs-lookup"><span data-stu-id="ab16b-118">appointment</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="ab16b-119">Startzeit eines Termins</span><span class="sxs-lookup"><span data-stu-id="ab16b-119">Start time of an appointment</span></span></p></td>
    <td><p><span data-ttu-id="ab16b-120">starttime</span><span class="sxs-lookup"><span data-stu-id="ab16b-120">starttime</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="ab16b-121">Endzeit eines Termins</span><span class="sxs-lookup"><span data-stu-id="ab16b-121">End time of an appointment</span></span></p></td>
    <td><p><span data-ttu-id="ab16b-122">endtime</span><span class="sxs-lookup"><span data-stu-id="ab16b-122">endtime</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="ab16b-123">Titel eines Termins</span><span class="sxs-lookup"><span data-stu-id="ab16b-123">Title of an appointment</span></span></p></td>
    <td><p><span data-ttu-id="ab16b-124">Betreff</span><span class="sxs-lookup"><span data-stu-id="ab16b-124">subject</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="ab16b-125">Ort eines Termins</span><span class="sxs-lookup"><span data-stu-id="ab16b-125">Location of an appointment</span></span></p></td>
    <td><p><span data-ttu-id="ab16b-126">location</span><span class="sxs-lookup"><span data-stu-id="ab16b-126">location</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="ab16b-127">Details eines Termins</span><span class="sxs-lookup"><span data-stu-id="ab16b-127">Details of an appointment</span></span></p></td>
    <td><p><span data-ttu-id="ab16b-128">body</span><span class="sxs-lookup"><span data-stu-id="ab16b-128">body</span></span></p></td>
    </tr>
    </tbody>
    </table>


<span data-ttu-id="ab16b-129">Das folgende Beispiel zeigt Eingabedaten für den *xml*-Parameter.</span><span class="sxs-lookup"><span data-stu-id="ab16b-129">The following example shows input data for the *xml* parameter.</span></span>

```xml
<?xml version="1.0" encoding="utf-8" ?> 
<appointments>
    <appointment>
        <starttime>2009-06-01T15:00:00</starttime>
        <endtime>2009-06-01T16:15:00</endtime>
        <subject>This is a Test-Appointment</subject>
        <location>At your Desk</location>
        <body>Here is the Bodytext</body>
    </appointment>
    <appointment>
        <starttime>2009-06-01T17:00:00</starttime>
        <endtime>2009-06-01T17:15:00</endtime>
        <subject>This is a second Test-Appointment</subject>
        <location>At your Desk</location>
        <body>Here is the Bodytext</body>
    </appointment>
    <appointment>
        <starttime>2009-06-01T17:00:00</starttime>
        <endtime>2009-06-01T18:15:00</endtime>
        <subject>This is a third Test-Appointment</subject>
        <location>At your Desk</location>
        <body>Here is the Bodytext</body>
    </appointment>
</appointments>
```

<span data-ttu-id="ab16b-p104">Die CreateAppointmentsFromXml-Methode arbeitet mit der Microsoft COM-Implementierung des XML-Dokumentobjektmodells (DOM) zum Laden und Verarbeiten der XML-Daten, die xml bereitstellt. CreateAppointmentsFromXml überprüft zuerst, ob xml eine gültige XML-Datenquelle angibt. Falls ja, werden die Daten in ein XML-Dokument ([DOMDocument](https://msdn.microsoft.com/library/ms756987\(v=office.15\))) geladen. Andernfalls löst CreateAppointmentsFromXml eine Ausnahme aus. Weitere Informationen zum XML-DOM finden Sie unter [DOM](https://msdn.microsoft.com/library/ms766487\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="ab16b-p104">The CreateAppointmentsFromXml method uses the Microsoft COM implementation of the XML Document Object Model (DOM) to load and process the XML data that xml provides. CreateAppointmentsFromXml first checks whether xml specifies a valid source of XML data. If so, it loads the data into an XML document, [DOMDocument](https://msdn.microsoft.com/library/ms756987\(v=office.15\)). Otherwise, CreateAppointmentsFromXml throws an exception. For more information about the XML DOM, see [DOM](https://msdn.microsoft.com/library/ms766487\(v=office.15\)).</span></span>

<span data-ttu-id="ab16b-135">Für jeden untergeordneten Terminknoten, der vom appointment-Tag in den XML-Daten begrenzt wird, sucht CreateAppointmentsFromXml nach spezifischen Tags, verwendet das DOM zum Extrahieren der Daten und weist die Daten den entsprechenden Eigenschaften eines **AppointmentItem**-Objekts zu: [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)), [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), [Subject](https://msdn.microsoft.com/library/bb611653\(v=office.15\)), [Location](https://msdn.microsoft.com/library/bb608946\(v=office.15\)) und [Body](https://msdn.microsoft.com/library/bb644880\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="ab16b-135">For each appointment child node delimited by the appointment tag in the XML data, CreateAppointmentsFromXml looks for specific tags, uses the DOM to extract the data, and assigns the data to corresponding properties of an **AppointmentItem** object: [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)), [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), [Subject](https://msdn.microsoft.com/library/bb611653\(v=office.15\)), [Location](https://msdn.microsoft.com/library/bb608946\(v=office.15\)), and [Body](https://msdn.microsoft.com/library/bb644880\(v=office.15\)).</span></span> <span data-ttu-id="ab16b-136">CreateAppointmentsFromXml speichert anschließend den Termin im Standardkalender.</span><span class="sxs-lookup"><span data-stu-id="ab16b-136">CreateAppointmentsFromXml then saves the appointment to the default calendar.</span></span>

<span data-ttu-id="ab16b-137">CreateAppointmentsFromXml verwendet die [Add](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.add?view=netframework-4.7.2)-Methode der [List\<T\>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1?view=netframework-4.7.2)-Klasse im [System.Collections.Generic](https://docs.microsoft.com/dotnet/api/system.collections.generic?view=netframework-4.7.2)-Namespace zum Aggregieren dieser AppointmentItem-Objekte.</span><span class="sxs-lookup"><span data-stu-id="ab16b-137">CreateAppointmentsFromXml uses the [Add](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.add?view=netframework-4.7.2) method of the [List\<T\>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1?view=netframework-4.7.2) class in the [System.Collections.Generic](https://docs.microsoft.com/dotnet/api/system.collections.generic?view=netframework-4.7.2) namespace to aggregate these AppointmentItem objects.</span></span> <span data-ttu-id="ab16b-138">Wenn die Methode alle Termine in den XML-Daten verarbeitet hat, gibt sie die AppointmentItem-Objekte in einem Array zurück.</span><span class="sxs-lookup"><span data-stu-id="ab16b-138">When the method has processed all the appointments in the XML data, it returns the AppointmentItem objects in an array.</span></span>

<span data-ttu-id="ab16b-139">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="ab16b-139">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="ab16b-140">Die Anweisung **Imports** oder **using** darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="ab16b-140">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="ab16b-141">Die folgenden Codezeilen zeigen, wie Sie den Import und die Zuweisung in Visual Basic und C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="ab16b-141">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>


```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```



```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

<span data-ttu-id="ab16b-142">Es folgen das Visual Basic-Codebeispiel und anschließend das C\#-Codebeispiel.</span><span class="sxs-lookup"><span data-stu-id="ab16b-142">The following is the Visual Basic code example, followed by the C\# code example.</span></span>



```vb
Imports System.IO
Imports System.Xml
Imports Outlook = Microsoft.Office.Interop.Outlook

Namespace OutlookAddIn2
    Class Sample
        Function CreateAppointmentsFromXml(ByVal application As Outlook.Application, _
            ByVal xml As String) As Outlook.AppointmentItem()

            Dim appointments As New List(Of Outlook.AppointmentItem)
            Dim xmlDoc As New XmlDocument()

            ' If xml is an XML string, create the XML document directly.
            If xml.StartsWith("<?xml") Then
                xmlDoc.LoadXml(xml)
            ElseIf (File.Exists(xml)) Then
                xmlDoc.Load(xml)
            Else
                Throw New Exception("The input string is not valid XML data or the specified file doesn't exist.")
            End If


            ' Select all appointment nodes under the root appointments node.
            Dim appointmentNodes As XmlNodeList = xmlDoc.SelectNodes("appointments/appointment")

            For Each appointmentNode As XmlNode In appointmentNodes

                ' Create a new AppointmentItem object.
                Dim newAppointment As Outlook.AppointmentItem = _
                    DirectCast(application.CreateItem(Outlook.OlItemType.olAppointmentItem), _
                    Outlook.AppointmentItem)

                ' Loop over all child nodes, check the node name, and import the data into the appointment fields.

                For Each node As XmlNode In appointmentNode.ChildNodes
                    Select Case (node.Name)

                        Case "starttime"
                            newAppointment.Start = DateTime.Parse(node.InnerText)


                        Case "endtime"
                            newAppointment.End = DateTime.Parse(node.InnerText)


                        Case "subject"
                            newAppointment.Subject = node.InnerText


                        Case "location"
                            newAppointment.Location = node.InnerText


                        Case "body"
                            newAppointment.Body = node.InnerText


                    End Select
                Next

                ' Save the item in the default calendar.
                newAppointment.Save()
                appointments.Add(newAppointment)
            Next

            ' Return an array of new appointments.
            Return appointments.ToArray()
        End Function


    End Class
End Namespace
```



```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Text;
using System.Xml;
using Outlook = Microsoft.Office.Interop.Outlook;

namespace OutlookAddIn1
{
    class Sample
    {
        Outlook.AppointmentItem[] CreateAppointmentsFromXml(Outlook.Application application, 
            string xml)
        {
            // Create a list of appointment objects.
            List<Outlook.AppointmentItem> appointments = new 
                List<Microsoft.Office.Interop.Outlook.AppointmentItem>();
            XmlDocument xmlDoc = new XmlDocument();

            // If xml is an XML string, create the document directly. 
            if (xml.StartsWith("<?xml"))
            {
                xmlDoc.LoadXml(xml);
            }
            else if (File.Exists(xml))
            {
                xmlDoc.Load(xml);
            }
            else
            {
                throw new Exception(
                    "The input string is not valid XML data or the specified file doesn't exist.");
            }

            // Select all appointment nodes under the root appointments node.
            XmlNodeList appointmentNodes = xmlDoc.SelectNodes("appointments/appointment");
            foreach (XmlNode appointmentNode in appointmentNodes)
            {

                // Create a new AppointmentItem object.
                Outlook.AppointmentItem newAppointment = 
                    (Outlook.AppointmentItem)application.CreateItem(Outlook.OlItemType.olAppointmentItem);

                // Loop over all child nodes, check the node name, and import the data into the 
                // appointment fields.
                foreach (XmlNode node in appointmentNode.ChildNodes)
                {
                    switch (node.Name)
                    {

                        case "starttime":
                            newAppointment.Start = DateTime.Parse(node.InnerText);
                            break;

                        case "endtime":
                            newAppointment.End = DateTime.Parse(node.InnerText);
                            break;

                        case "subject":
                            newAppointment.Subject = node.InnerText;
                            break;

                        case "location":
                            newAppointment.Location = node.InnerText;
                            break;

                        case "body":
                            newAppointment.Body = node.InnerText;
                            break;

                    }
                }

                // Save the item in the default calendar.
                newAppointment.Save();
                appointments.Add(newAppointment);
            }

            // Return an array of new appointments.
            return appointments.ToArray();
        }

    }
}
```

## <a name="see-also"></a><span data-ttu-id="ab16b-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab16b-143">See also</span></span>

- [<span data-ttu-id="ab16b-144">Termine</span><span class="sxs-lookup"><span data-stu-id="ab16b-144">Appointments</span></span>](appointments.md)

