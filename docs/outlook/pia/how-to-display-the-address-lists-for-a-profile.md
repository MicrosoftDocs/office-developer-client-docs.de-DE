---
title: Anzeigen der Adresslisten für ein Profil
TOCTitle: Display the address lists for a profile
ms:assetid: ced8230b-110b-4ccb-a699-588798144154
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184643(v=office.15)
ms:contentKeyID: 55119802
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b69ed930241dc058b22b75c6ccc9121f8856d28f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356371"
---
# <a name="display-the-address-lists-for-a-profile"></a><span data-ttu-id="ed261-102">Anzeigen der Adresslisten für ein Profil</span><span class="sxs-lookup"><span data-stu-id="ed261-102">Display the address lists for a profile</span></span>

<span data-ttu-id="ed261-103">In diesem Beispiel wird gezeigt, wie die Adresslisten für das aktuelle Profil angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ed261-103">This example shows how to display the address lists for the current profile.</span></span>

## <a name="example"></a><span data-ttu-id="ed261-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ed261-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="ed261-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="ed261-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="ed261-p101">Das aktuelle Profil enthält Adresslisten, die durch die [AddressLists](https://msdn.microsoft.com/library/bb611894\(v=office.15\)) -Auflistung dargestellt werden. Zum Abrufen einer Instanz der AddressLists-Auflistung verwenden Sie die [AddressLists](https://msdn.microsoft.com/library/bb624048\(v=office.15\)) -Eigenschaft des [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="ed261-p101">The current profile contains address lists that are represented by the [AddressLists](https://msdn.microsoft.com/library/bb611894\(v=office.15\)) collection. To get an instance of the AddressLists collection, you must use the [AddressLists](https://msdn.microsoft.com/library/bb624048\(v=office.15\)) property of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object.</span></span>

<span data-ttu-id="ed261-108">Im folgenden Codebeispiel zählt EnumerateAddressLists zunächst alle [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\))-Objekte in der AddressLists-Auflistung mithilfe einer foreach-Anweisung auf.</span><span class="sxs-lookup"><span data-stu-id="ed261-108">In the following code example, EnumerateAddressLists first enumerates each [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) object in the AddressLists collection by using a foreach statement.</span></span> <span data-ttu-id="ed261-109">Anschließend wird im Beispiel eine Zeichenfolge erstellt, die die Werte der Eigenschaften [Name](https://msdn.microsoft.com/library/bb609849\(v=office.15\)), [ResolutionOrder](https://msdn.microsoft.com/library/bb646853\(v=office.15\)), [IsReadOnly](https://msdn.microsoft.com/library/bb612676\(v=office.15\)) und [IsInitialAddressList](https://msdn.microsoft.com/library/bb646646\(v=office.15\)) enthält.</span><span class="sxs-lookup"><span data-stu-id="ed261-109">The example then creates a string that contains the values of the [Name](https://msdn.microsoft.com/library/bb609849\(v=office.15\)), [ResolutionOrder](https://msdn.microsoft.com/library/bb646853\(v=office.15\)), [IsReadOnly](https://msdn.microsoft.com/library/bb612676\(v=office.15\)), and [IsInitialAddressList](https://msdn.microsoft.com/library/bb646646\(v=office.15\)) properties.</span></span> <span data-ttu-id="ed261-110">Zuletzt schreibt EnumerateAddressLists die Zeichenfolge in die Listener der Ablaufverfolgung der [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx)-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="ed261-110">Finally, EnumerateAddressLists writes the string to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span> <span data-ttu-id="ed261-111">Dadurch wird die Adressliste für das aktuelle Profil angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ed261-111">This displays each address list for the current profile.</span></span>

<span data-ttu-id="ed261-112">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="ed261-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="ed261-113">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="ed261-113">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="ed261-114">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="ed261-114">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void EnumerateAddressLists()
{
    Outlook.AddressLists addrLists =
         Application.Session.AddressLists;
    foreach (Outlook.AddressList addrList in addrLists)
    {
        StringBuilder sb = new StringBuilder();
        sb.AppendLine("Display Name: " + addrList.Name);
        sb.AppendLine("Resolution Order: "
            + addrList.ResolutionOrder.ToString());
        sb.AppendLine("Read-only : "
            + addrList.IsReadOnly.ToString());
        sb.AppendLine("Initial Address List: "
            + addrList.IsInitialAddressList.ToString());
        sb.AppendLine("");
        Debug.WriteLine(sb.ToString());
    }
}
```

## <a name="see-also"></a><span data-ttu-id="ed261-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed261-115">See also</span></span>

- [<span data-ttu-id="ed261-116">Adressbuch</span><span class="sxs-lookup"><span data-stu-id="ed261-116">Address book</span></span>](address-book.md)

