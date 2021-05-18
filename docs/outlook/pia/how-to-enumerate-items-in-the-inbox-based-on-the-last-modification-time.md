---
title: Aufzählen der Elemente im Posteingang basierend auf dem Zeitpunkt der letzten Änderung
TOCTitle: Enumerate items in the Inbox based on the last modification time
ms:assetid: 93a25143-def6-4832-bac2-3744558c2736
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184626(v=office.15)
ms:contentKeyID: 55119920
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0a568209caf172fbab26af1441ba7c208562ae19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320356"
---
# <a name="enumerate-items-in-the-inbox-based-on-the-last-modification-time"></a><span data-ttu-id="33d20-102">Aufzählen der Elemente im Posteingang basierend auf dem Zeitpunkt der letzten Änderung</span><span class="sxs-lookup"><span data-stu-id="33d20-102">Enumerate items in the Inbox based on the last modification time</span></span>

<span data-ttu-id="33d20-103">Dieses Beispiel zeigt das Aufzählen der Elemente im Posteingangsordner basierend auf dem Zeitpunkt der letzten Änderung.</span><span class="sxs-lookup"><span data-stu-id="33d20-103">This example shows how to enumerate items in the Inbox folder based on the last modification time.</span></span>

## <a name="example"></a><span data-ttu-id="33d20-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="33d20-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="33d20-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="33d20-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="33d20-106">Das [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\))-Objekt repräsentiert eine Gruppe von Elementen aus dem [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\))- oder [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\))-Objekt.</span><span class="sxs-lookup"><span data-stu-id="33d20-106">The [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object represents a set of items from a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) or [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) object.</span></span> <span data-ttu-id="33d20-107">Um ein **Table**-Objekt abzurufen, rufen Sie die [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\))-Methode in einem **Folder**- oder **Search**-Objekt auf.</span><span class="sxs-lookup"><span data-stu-id="33d20-107">To obtain a **Table**, call the [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) method on a **Folder** or **Search** object.</span></span> <span data-ttu-id="33d20-108">Jedes Element in dem zurückgegebenen **Table**-Objekt enthält nur eine Standarduntermenge der Eigenschaften des Elements.</span><span class="sxs-lookup"><span data-stu-id="33d20-108">Each item in the returned **Table** contains only a default subset of the item’s properties.</span></span> <span data-ttu-id="33d20-109">Jedes [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\))-Objekt kann als ein Element im Ordner betrachtet werden und jedes [Column](https://msdn.microsoft.com/library/bb609646\(v=office.15\))-Objekt als eine Eigenschaft eines Elements.</span><span class="sxs-lookup"><span data-stu-id="33d20-109">Each [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) object can be regarded as an item in the folder, and each [Column](https://msdn.microsoft.com/library/bb609646\(v=office.15\)) object as a property of an item.</span></span> <span data-ttu-id="33d20-110">Das Entfernen, Hinzufügen oder Ändern von Zeilen wird im **Table**-Objekt nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="33d20-110">Removing, adding, or changing rows is not supported in the **Table**.</span></span> <span data-ttu-id="33d20-111">Zum Auflisten der Elemente in einer **Table** prüfen Sie zuerst mithilfe der [EndOfTable](https://msdn.microsoft.com/library/bb647715\(v=office.15\)) -Eigenschaft, ob die aktuelle Position das Ende der Tabelle ist.</span><span class="sxs-lookup"><span data-stu-id="33d20-111">To enumerate items in a **Table**, first use the [EndOfTable](https://msdn.microsoft.com/library/bb647715\(v=office.15\)) property to see whether your current position is at the end of the table.</span></span> <span data-ttu-id="33d20-112">Wenn **EndOfTable** den Wert **false** zurückgibt, verwenden Sie die [GetNextRow()](https://msdn.microsoft.com/library/bb609740\(v=office.15\)) -Methode, um ein **Row**-Objekt zurückzugeben, das eine Standardanzahl von **Column**-Objekten enthält.</span><span class="sxs-lookup"><span data-stu-id="33d20-112">If **EndOfTable** returns **false**, use the [GetNextRow()](https://msdn.microsoft.com/library/bb609740\(v=office.15\)) method to return a **Row**, which contains a default number of **Column** objects.</span></span> <span data-ttu-id="33d20-113">Sie durchlaufen das **Table**-Objekt weiterhin vorwärts, indem Sie **GetNextRow** aufrufen, bis **EndOfTable** **true** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="33d20-113">You continue iterating in a forward manner through the **Table** by calling **GetNextRow** until **EndOfTable** returns **true**.</span></span>

<span data-ttu-id="33d20-114">Im folgenden Codebeispiel ruft DemoTableForInbox ein **Table**-Objekt für den Posteingangsordner ab, sortiert das **Table**-Objekt mithilfe der **LastModificationTime**-Eigenschaft und der [Sort(String, Object)](https://msdn.microsoft.com/library/bb652667\(v=office.15\))-Methode und durchläuft die Tabelle, um den Betreff jedes Elements in die Listener der Ablaufverfolgung für die [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx)-Auflistung zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="33d20-114">In the following code example, DemoTableForInbox obtains a **Table** object for the Inbox folder, sorts the **Table** object by using the **LastModificationTime** property and [Sort(String, Object)](https://msdn.microsoft.com/library/bb652667\(v=office.15\)) method, and iterates through the table to write the subject of each item to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="33d20-115">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="33d20-115">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="33d20-116">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="33d20-116">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="33d20-117">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="33d20-117">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoTableForInbox()
{
    //Obtain Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    //Obtain Table using defaults
    Outlook.Table table =
        folder.GetTable(Type.Missing, Type.Missing);
    table.Sort("LastModificationTime",
        Outlook.OlSortOrder.olDescending);
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        Debug.WriteLine(nextRow["Subject"]);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="33d20-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33d20-118">See also</span></span>

- [<span data-ttu-id="33d20-119">Suchen und Filtern</span><span class="sxs-lookup"><span data-stu-id="33d20-119">Search and filter</span></span>](search-and-filter.md)

