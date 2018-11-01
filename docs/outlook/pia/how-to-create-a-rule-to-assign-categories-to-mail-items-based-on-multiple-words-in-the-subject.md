---
title: Erstellen einer Regel zum Zuweisen von Kategorien zu E-Mail-Elementen basierend auf mehreren Wörtern im Betreff
TOCTitle: Create a rule to assign categories to mail items based on multiple words in the subject
ms:assetid: 6e1fa40c-edf3-407c-9e90-99f634fa8e24
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424472(v=office.15)
ms:contentKeyID: 55119918
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 1ff096454aa15a0a45c423913140eb50e6de9678
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406323"
---
# <a name="create-a-rule-to-assign-categories-to-mail-items-based-on-multiple-words-in-the-subject"></a><span data-ttu-id="bd407-102">Erstellen einer Regel zum Zuweisen von Kategorien zu E-Mail-Elementen basierend auf mehreren Wörtern im Betreff</span><span class="sxs-lookup"><span data-stu-id="bd407-102">Create a rule to assign categories to mail items based on multiple words in the subject</span></span>

<span data-ttu-id="bd407-103">In diesem Beispiel wird gezeigt, wie eine Regel zum Zuweisen von Kategorien zu E-Mail-Elementen basierend auf mehreren Wörtern im Betreff eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="bd407-103">This example shows how to set up a rule that assigns categories to mail items based on multiple words in the subject.</span></span>

## <a name="example"></a><span data-ttu-id="bd407-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="bd407-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="bd407-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="bd407-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="bd407-106">In Outlook können Elemente zur einfacheren Organisation und Anzeige kategorisiert werden.</span><span class="sxs-lookup"><span data-stu-id="bd407-106">In Outlook, items can be categorized for easier organization and display.</span></span> <span data-ttu-id="bd407-107">Das Outlook-Objektmodell stellt das [Category](https://msdn.microsoft.com/library/bb623480\(v=office.15\))-Objekt und die [Categories](https://msdn.microsoft.com/library/bb623535\(v=office.15\))-Auflistung zur Darstellung von Kategorien bereit.</span><span class="sxs-lookup"><span data-stu-id="bd407-107">The Outlook object model provides the [Category](https://msdn.microsoft.com/library/bb623480\(v=office.15\)) object and the [Categories](https://msdn.microsoft.com/library/bb623535\(v=office.15\)) collection to represent categories.</span></span> <span data-ttu-id="bd407-108">Weitere Informationen zum **Category**-Objekt und zur **Categories**-Auflistung für ein Outlook-Element finden Sie unter [Auflisten und Hinzufügen von Kategorien](how-to-enumerate-and-add-categories.md).</span><span class="sxs-lookup"><span data-stu-id="bd407-108">For more information about the **Category** object and the **Categories** collection for an Outlook item, see [How to: Enumerate and Add Categories](how-to-enumerate-and-add-categories.md).</span></span>

<span data-ttu-id="bd407-109">Eine Regel, die von einem [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\))-Objekt dargestellt wird, kann mehreren Bedingungen zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="bd407-109">A rule, represented by a [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) object, can be assigned with multiple conditions.</span></span> <span data-ttu-id="bd407-110">Sie können ein Array abrufen oder festlegen, das auszuwertende Bedingungen oder auszuführende Aktionen darstellt.</span><span class="sxs-lookup"><span data-stu-id="bd407-110">You can get or set an array that represents conditions to be evaluated or actions to be completed.</span></span> <span data-ttu-id="bd407-111">Beispielsweise wird von der [Text](https://msdn.microsoft.com/library/bb611271\(v=office.15\)) -Eigenschaft des [TextRuleCondition](https://msdn.microsoft.com/library/bb644796\(v=office.15\)) -Objekts ein Array von Zeichenfolgenelementen zurückgegeben oder festgelegt, das den von der Regelbedingung auszuwertenden Text darstellt.</span><span class="sxs-lookup"><span data-stu-id="bd407-111">For example, the [Text](https://msdn.microsoft.com/library/bb611271\(v=office.15\)) property of the [TextRuleCondition](https://msdn.microsoft.com/library/bb644796\(v=office.15\)) object returns or sets an array of string elements that represents the text to be evaluated by the rule condition.</span></span> <span data-ttu-id="bd407-112">Sie müssen ein Array mit einer oder mehreren Zeichenfolgen für die Auswertung zuordnen.</span><span class="sxs-lookup"><span data-stu-id="bd407-112">You must assign an array with one string or multiple strings for evaluation.</span></span> <span data-ttu-id="bd407-113">Um mehrere Textzeichenfolgen auszuwerten, die in einem Array zugewiesen sind, verwenden Sie die logische ODER-Operation.</span><span class="sxs-lookup"><span data-stu-id="bd407-113">To evaluate multiple text strings that are assigned in an array, use the logical OR operation.</span></span> 

<span data-ttu-id="bd407-114">Folgende Eigenschaften können Sie zum Abrufen oder Festlegen eines Arrays verwenden: [Address](https://msdn.microsoft.com/library/bb647045\(v=office.15\)), [Categories](https://msdn.microsoft.com/library/bb611021\(v=office.15\)), [Categories](https://msdn.microsoft.com/library/bb612345\(v=office.15\)), [FormName](https://msdn.microsoft.com/library/bb647042\(v=office.15\)) und **TextRuleCondition.Text**.</span><span class="sxs-lookup"><span data-stu-id="bd407-114">The properties that you can use to get or set an array are as follows: [Address](https://msdn.microsoft.com/library/bb647045\(v=office.15\)) , [Categories](https://msdn.microsoft.com/library/bb611021\(v=office.15\)) , [Categories](https://msdn.microsoft.com/library/bb612345\(v=office.15\)) , [FormName](https://msdn.microsoft.com/library/bb647042\(v=office.15\)) , and **TextRuleCondition.Text**.</span></span> <span data-ttu-id="bd407-115">Weitere Informationen zu Regeln finden Sie unter [Erstellen einer Regel zum Ablegen von E-Mail-Elementen von einem Vorgesetzten und Kennzeichnen dieser Elemente für die Nachverfolgung](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md).</span><span class="sxs-lookup"><span data-stu-id="bd407-115">For more information about rules, see [How to: Create a Rule to File Mail Items from a Manager and Flag Them for Follow-Up](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md).</span></span>

<span data-ttu-id="bd407-116">Im folgenden Beispiel verwendet CreateTextAndCategoryRule die CategoryExists-Methode, um die E-Mail-Elemente des Benutzers anhand des Namens "Office" oder "Outlook" in der **Categories**-Auflistung auf Kategorien zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="bd407-116">In the following example,   uses the   method to check the user's mail items for any categories by the name "Office" or "Outlook" in the Categories collection.</span></span> <span data-ttu-id="bd407-117">Wenn keine Kategorien gefunden werden, werden diese hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bd407-117">If no categories are found, they are added.</span></span> <span data-ttu-id="bd407-118">Anschließend wird in dem Beispiel ein Array von Zeichenfolgen erstellt, die "Office", "Outlook" und "2007" enthalten.</span><span class="sxs-lookup"><span data-stu-id="bd407-118">The example then creates an array of strings that include "Office, "Outlook", and "2007".</span></span> <span data-ttu-id="bd407-119">Dieses Array stellt die Kriterien dar, die ausgewertet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bd407-119">This array will represent the conditions to be evaluated.</span></span> <span data-ttu-id="bd407-120">Danach wird von CreateTextAndCategoryRule eine Regel erstellt, die durch Untersuchen des Betreffs auf die Bedingungen in dem Array mithilfe der **Text**-Eigenschaft des **TextRuleCondition**-Objekts und der [BodyOrSubject](https://msdn.microsoft.com/library/bb612744\(v=office.15\))-Eigenschaft der [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\))-Auflistung Kategorien zuordnet.</span><span class="sxs-lookup"><span data-stu-id="bd407-120"> then creates a rule that assigns categories by examining the subject for any of the conditions in the array by using the Text property of the TextRuleCondition object and the BodyOrSubject property of the RuleConditions collection.</span></span> <span data-ttu-id="bd407-121">Ist die Bedingung erfüllt, werden dem Element mithilfe der [AssignToCategory](https://msdn.microsoft.com/library/bb623146\(v=office.15\)) -Methode des [RuleActions](https://msdn.microsoft.com/library/bb610113\(v=office.15\)) -Objekts die Kategorien Office und Outlook zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="bd407-121">If the condition is satisfied, the categories of Office and Outlook are assigned to the item by using the [AssignToCategory](https://msdn.microsoft.com/library/bb623146\(v=office.15\)) method of the [RuleActions](https://msdn.microsoft.com/library/bb610113\(v=office.15\)) object.</span></span>

<span data-ttu-id="bd407-122">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="bd407-122">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="bd407-123">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="bd407-123">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="bd407-124">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="bd407-124">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateTextAndCategoryRule()
{
    if (!CategoryExists("Office"))
    {
        Application.Session.Categories.Add(
            "Office", Type.Missing, Type.Missing);
    }
    if (!CategoryExists("Outlook"))
    {
        Application.Session.Categories.Add(
            "Outlook", Type.Missing, Type.Missing);
    }
    Outlook.Rules rules =
        Application.Session.DefaultStore.GetRules();
    Outlook.Rule textRule =
        rules.Create("Demo Text and Category Rule",
        Outlook.OlRuleType.olRuleReceive);
    Object[] textCondition = 
        { "Office", "Outlook", "2007" };
    Object[] categoryAction = 
        { "Office", "Outlook" };
    textRule.Conditions.BodyOrSubject.Text =
        textCondition;
    textRule.Conditions.BodyOrSubject.Enabled = true;
    textRule.Actions.AssignToCategory.Categories =
        categoryAction;
    textRule.Actions.AssignToCategory.Enabled = true;
    rules.Save(true);
}

// Determines if categoryName exists in Categories collection
private bool CategoryExists(string categoryName)
{
    try
    {
        Outlook.Category category =
            Application.Session.Categories[categoryName];
        if (category != null)
        {
            return true;
        }
        else
        {
            return false;
        }
    }
    catch { return false; }
}
```

## <a name="see-also"></a><span data-ttu-id="bd407-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd407-125">See also</span></span>

- [<span data-ttu-id="bd407-126">Regeln</span><span class="sxs-lookup"><span data-stu-id="bd407-126">Rules</span></span>](rules.md)
