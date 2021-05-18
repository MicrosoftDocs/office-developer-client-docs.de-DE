---
title: Auflisten der Elemente in einer Tabellenansicht
TOCTitle: Enumerate items in a table view
ms:assetid: c7d9a667-cfec-49c1-af7a-4c8063991588
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184640(v=office.15)
ms:contentKeyID: 55119900
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b3bde66fd07a39aa8a63219876b9bdbcf72e00f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320384"
---
# <a name="enumerate-items-in-a-table-view"></a><span data-ttu-id="3aaa2-102">Auflisten der Elemente in einer Tabellenansicht</span><span class="sxs-lookup"><span data-stu-id="3aaa2-102">Enumerate items in a table view</span></span>

<span data-ttu-id="3aaa2-103">In diesem Beispiel werden Elemente in einer Tabellenansicht mit der [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\))-Methode aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="3aaa2-103">This example enumerates items in a table view by using the [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) method.</span></span>

## <a name="example"></a><span data-ttu-id="3aaa2-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3aaa2-104">Example</span></span>

<span data-ttu-id="3aaa2-p101">Das folgende Codebeispiel ruft ein [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) -Objekt aus der aktuellen Ansicht des Posteingangsordners ab. Der aktuelle Ordner des aktiven Explorers wird auf den Posteingang festgelegt. Anschließend wird überprüft, ob es sich bei der aktuellen Ansicht des Posteingangs um eine Tabellenansicht handelt. Ist die aktuelle Ansicht eine Tabelle, wird im Codebeispiel die [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) -Methode aufgerufen und jedes durch jeweils eine Zeile im zurückgegebenen **Table**-Objekt dargestellte Element angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3aaa2-p101">The following code example obtains a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object from the current view of the Inbox folder. The code example sets the current folder of the active explorer to the Inbox, and then checks that the current view of the Inbox is a table view. If the current view is a table, the code example calls the [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) method and displays each item represented by each row in the returned **Table**.</span></span>

<span data-ttu-id="3aaa2-108">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="3aaa2-108">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="3aaa2-109">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="3aaa2-109">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="3aaa2-110">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="3aaa2-110">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoViewGetTable()
{
    // Obtain Inbox.
    Outlook.Folder inbox =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // Set ActiveExplorer.CurrentFolder to Inbox.
    // Inbox must be current folder
    // for View.GetTable to work correctly.
    Application.ActiveExplorer().CurrentFolder = inbox;
    // Ensure that current view is TableView.
    if (inbox.CurrentView.ViewType == 
        Outlook.OlViewType.olTableView)
    {
        Outlook.TableView view = 
            inbox.CurrentView as Outlook.TableView;
        // No arguments needed for View.GetTable.
        Outlook.Table table = view.GetTable();
        Debug.WriteLine("View Count=" 
            + table.GetRowCount().ToString());
        while (!table.EndOfTable)
        {
            // First row in Table.
            Outlook.Row nextRow = table.GetNextRow();
            Debug.WriteLine(nextRow["Subject"]
                + " Modified: "
                + nextRow["LastModificationTime"]);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="3aaa2-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3aaa2-111">See also</span></span>

- [<span data-ttu-id="3aaa2-112">Views</span><span class="sxs-lookup"><span data-stu-id="3aaa2-112">Views</span></span>](views.md)

