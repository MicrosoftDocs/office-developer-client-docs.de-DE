---
title: Freigeben von Kalenderinformationen per E-Mail
TOCTitle: Share calendar information through email
ms:assetid: 3382010c-0a16-4dca-a99e-669e9178354e
ms:mtpsurl: https://msdn.microsoft.com/library/Bb609881(v=office.15)
ms:contentKeyID: 55119817
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 48b299ad4d3afe5c0c9aaa05f5d8af3b92bf655d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332080"
---
# <a name="share-calendar-information-through-email"></a><span data-ttu-id="c8051-102">Freigeben von Kalenderinformationen per E-Mail</span><span class="sxs-lookup"><span data-stu-id="c8051-102">Share calendar information through email</span></span>

<span data-ttu-id="c8051-103">In diesem Beispiel wird gezeigt, wie Informationen aus einem Kalender mithilfe einer E-Mail-Nachricht im iCalendar-Format freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c8051-103">This example shows how to share information from a calendar by email in the iCalendar format.</span></span>

## <a name="example"></a><span data-ttu-id="c8051-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c8051-104">Example</span></span>

<span data-ttu-id="c8051-p101">Das iCalendar-Format ermöglicht das Senden von Elementen an andere Outlook- oder Nicht-Outlook-Clients über Standard-Internet-Mailformate und -Protokolle. Im Codebeispiel wird das [CalendarSharing](https://msdn.microsoft.com/library/bb624344\(v=office.15\)) -Objekt verwendet, das den Export von Informationen aus einem Kalenderordner in das iCalendar-Format unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c8051-p101">The iCalendar format allows you to send items to other Outlook or non-Outlook clients via standard Internet mail formats and protocols. The code sample uses the [CalendarSharing](https://msdn.microsoft.com/library/bb624344\(v=office.15\)) object that supports exporting information from a calendar folder to the iCalendar format.</span></span>

<span data-ttu-id="c8051-p102">Zuerst wird [GetCalendarExporter](https://msdn.microsoft.com/library/bb610021\(v=office.15\)) für den standardmäßigen Kalenderordner aufgerufen, um ein **CalendarSharing**-Objekt abzurufen. Dann werden die Eigenschaften des **CalendarSharing**-Objekts festgelegt, um die Exportkriterien, wie Datumsbereich der Kalenderinformation, die Zulässigkeit von Anhängen und Einzelheiten zu Besprechungen anzugeben, die als privat gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="c8051-p102">The code sample first calls [GetCalendarExporter](https://msdn.microsoft.com/library/bb610021\(v=office.15\)) on the default Calendar folder to obtain a **CalendarSharing** object. Then it sets properties of the **CalendarSharing** object to specify criteria for the export, such as the date range of calendar information, whether to include attachments, and details of appointments that are marked "private."</span></span>

<span data-ttu-id="c8051-109">Damit die Kalenderinformation dann per E-Mail gesendet wird, wird durch das Codebeispiel die [ForwardAsICal](https://msdn.microsoft.com/library/bb652866\(v=office.15\))-Methode des **CalendarSharing**-Objekts aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="c8051-109">To send the calendar information by email, the code sample calls the [ForwardAsICal](https://msdn.microsoft.com/library/bb652866\(v=office.15\)) method of the **CalendarSharing** object.</span></span>

<span data-ttu-id="c8051-110">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="c8051-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="c8051-111">Die Anweisung **Imports** oder **using** darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="c8051-111">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="c8051-112">Die folgenden Codezeilen zeigen, wie Sie den Import und die Zuweisung in Visual Basic und C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="c8051-112">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```vb
Private Sub SendNextWeekToAddress(ByVal sendToAddresses As String)
    If String.IsNullOrEmpty(sendToAddresses) Then
        Throw New ArgumentException( _
            "Parameter must contain a value.", "sendToAddress")
    End If

    Dim calendar As Outlook.Folder = TryCast( _
        Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderCalendar), Outlook.Folder)
    Dim exporter As Outlook.CalendarSharing = calendar.GetCalendarExporter()

    '' Set the properties for the export
    exporter.CalendarDetail = Outlook.OlCalendarDetail.olFullDetails
    exporter.IncludeAttachments = True
    exporter.IncludePrivateDetails = False
    exporter.RestrictToWorkingHours = False
    exporter.StartDate = DateTime.Today.Date
    exporter.EndDate = DateTime.Today.Date.AddDays(7)

    '' Create a new mail item
    Dim calendarMail As Outlook.MailItem = exporter.ForwardAsICal _
        (Outlook.OlCalendarMailFormat. _
        olCalendarMailFormatDailySchedule)
    calendarMail.To = sendToAddresses
    calendarMail.Send()
    calendarMail.Display()
End Sub
```

```csharp
private void SendNextWeekToAddress(string sendToAddresses)
{
    if (string.IsNullOrEmpty(sendToAddresses))
        throw new ArgumentException(
        "sendToAddress","Parameter must contain a value.");
    Outlook.Folder calendar = 
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderCalendar)
        as Outlook.Folder;
    Outlook.CalendarSharing exporter = calendar.GetCalendarExporter();

    // Set the properties for the export
    exporter.CalendarDetail = Outlook.OlCalendarDetail.olFullDetails;
    exporter.IncludeAttachments = true;
    exporter.IncludePrivateDetails = false;
    exporter.RestrictToWorkingHours = false;
    exporter.StartDate = DateTime.Today.Date;
    exporter.EndDate = DateTime.Today.Date.AddDays(7);

    // Create a new mail item
    Outlook.MailItem calendarMail = 
        exporter.ForwardAsICal(Outlook.OlCalendarMailFormat.
        olCalendarMailFormatDailySchedule);
    calendarMail.To = sendToAddresses;
    ((Outlook.MailItemClass)calendarMail).Send();
    ((Outlook.MailItemClass)calendarMail).Display(Type.Missing);
}
```

## <a name="see-also"></a><span data-ttu-id="c8051-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8051-113">See also</span></span>

- [<span data-ttu-id="c8051-114">Calendar</span><span class="sxs-lookup"><span data-stu-id="c8051-114">Calendar</span></span>](calendar.md)

