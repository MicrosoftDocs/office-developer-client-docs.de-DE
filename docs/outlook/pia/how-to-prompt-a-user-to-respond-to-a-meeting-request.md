---
title: Auffordern eines Benutzers zum Antworten auf eine Besprechungsanfrage
TOCTitle: Prompt a user to respond to a meeting request
ms:assetid: a0d69f82-8659-457d-9418-1a897a10882f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184630(v=office.15)
ms:contentKeyID: 55119877
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 26e59cca7431e9f11f3fea5fa058548b9a5903a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320048"
---
# <a name="prompt-a-user-to-respond-to-a-meeting-request"></a><span data-ttu-id="faf69-102">Auffordern eines Benutzers zum Antworten auf eine Besprechungsanfrage</span><span class="sxs-lookup"><span data-stu-id="faf69-102">Prompt a user to respond to a meeting request</span></span>

<span data-ttu-id="faf69-103">Dieses Beispiel zeigt, wie der Benutzer zu einer Antwort auf eine Besprechungsanfrage aufgefordert wird und wie ihm ermöglicht wird, die Antwort vor dem Senden zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="faf69-103">This example shows how to prompt the user for a response to a meeting request, and to enable the user to edit the response before sending it.</span></span>

## <a name="example"></a><span data-ttu-id="faf69-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="faf69-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="faf69-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="faf69-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="faf69-106">Die [Respond](https://msdn.microsoft.com/library/bb647086\(v=office.15\))-Methode des [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\))-Objekts wird zum Benachrichtigen des Besprechungsorganisators darüber verwendet, ob die Besprechung zum Kalender des Empfängers als "Angenommen", "Abgelehnt" oder "Mit Vorbehalt" hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="faf69-106">The [Respond](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) method of the [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object is used to notify the meeting organizer whether the meeting has been accepted, declined, or tentatively added to the recipient’s calendar.</span></span> <span data-ttu-id="faf69-107">Mithilfe der **Respond**-Methode können Sie angeben, ob Sie die Benachrichtigung automatisch senden möchten oder ob der Benutzer die Antwort vor dem Absenden bearbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="faf69-107">By using the **Respond** method, you can indicate whether you want to send the notification automatically, or whether you want to allow the user to edit the response before sending it.</span></span> <span data-ttu-id="faf69-108">Die **Respond**-Methode akzeptiert drei Parameter.</span><span class="sxs-lookup"><span data-stu-id="faf69-108">The **Respond** method accepts three parameters.</span></span> <span data-ttu-id="faf69-109">Der *Response*-Parameter gibt an, ob die Antwort "Angenommen", "Abgelehnt" oder "Mit Vorbehalt" lautet.</span><span class="sxs-lookup"><span data-stu-id="faf69-109">The *Response* parameter indicates whether the response is accept, decline, or tentative.</span></span> <span data-ttu-id="faf69-110">Die Parameter *fNoUI* und *fAdditionalTextDialog* sind **bool**-Werte, die bestimmen, ob die Antwort gesendet wird und ob der Benutzer die Antwort bearbeitet hat.</span><span class="sxs-lookup"><span data-stu-id="faf69-110">The *fNoUI* and *fAdditionalTextDialog* parameters are **bool** values that indicate whether the response will be sent to the organizer, and whether the user can edit the body of the response before sending it, respectively.</span></span> 

<span data-ttu-id="faf69-111">Im folgenden Codebeispiel listet PromptUserMeetingRequest die [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\))-Objekte auf, um die zugehörigen **AppointmentItem**-Objekte abzurufen. Anschließend wird die **Respond**-Methode aufgerufen, wobei der *fNoUI*-Parameter auf **false** und der *fAdditionalTextDialog*-Parameter auf **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="faf69-111">In the following code example, PromptUserMeetingRequest enumerates through the [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) objects to get the associated **AppointmentItem** objects, and then calls the **Respond** method with the *fNoUI* parameter set to **false** and the *fAdditionalTextDialog* parameter set to **true**.</span></span> <span data-ttu-id="faf69-112">Auf diese Weise kann der Benutzer auswählen, ob eine Antwort gesendet werden soll und ob der Text der Antwort vor dem Absenden bearbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="faf69-112">This allows the user to choose whether to send a response, and whether to edit the body of the response before sending it.</span></span>

<span data-ttu-id="faf69-113">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="faf69-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="faf69-114">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="faf69-114">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="faf69-115">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="faf69-115">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void PromptUserMeetingRequest()
{
    Outlook.MeetingItem mtgResponse;
    Outlook.Folder folder = Application.Session.
        GetDefaultFolder(Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    string filter = "[MessageClass] = " +
        "'IPM.Schedule.Meeting.Request'";
    Outlook.Items items = folder.Items.Restrict(filter);
    foreach (Outlook.MeetingItem request in items)
    {
        Outlook.AppointmentItem appt =
            request.GetAssociatedAppointment(true);
        if (appt != null)
        {
            mtgResponse = appt.Respond(
                Outlook.OlMeetingResponse.olMeetingAccepted,
                false, true);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="faf69-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="faf69-116">See also</span></span>

- [<span data-ttu-id="faf69-117">Besprechungsanfragen</span><span class="sxs-lookup"><span data-stu-id="faf69-117">Meeting requests</span></span>](meeting-requests.md)

