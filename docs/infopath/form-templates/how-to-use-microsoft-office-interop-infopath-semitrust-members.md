---
title: Verwenden Sie Microsoft. Office.Interop.InfoPath.SemiTrust-Mitglieder, die nicht mit InfoPath kompatibel sind
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-kompatible Formularvorlagen mithilfe von infopath 2007-Features
localization_priority: Normal
ms.assetid: d082f3a3-387a-4db1-bbad-495c326b8ee3
description: Das von Microsoft bereitgestellte Objektmodell. Office.Interop.InfoPath.SemiTrust-Namespace enthält Objekte und Member, die neue Funktionen bereitstellen, die Office InfoPath 2007 und InfoPath hinzugefügt wurden.
ms.openlocfilehash: 45f7607aec8ccfd653780a550df0823730835a86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415341"
---
# <a name="use-microsoftofficeinteropinfopathsemitrust-members-not-compatible-with-infopath"></a><span data-ttu-id="46c26-104">Verwenden Sie Microsoft. Office.Interop.InfoPath.SemiTrust-Mitglieder, die nicht mit InfoPath kompatibel sind</span><span class="sxs-lookup"><span data-stu-id="46c26-104">Use Microsoft.Office.Interop.InfoPath.SemiTrust members not compatible with InfoPath</span></span>

<span data-ttu-id="46c26-105">Wenn Sie einer Formularvorlage, die mit dem Microsoft Office InfoPath 2003 Toolkit erstellt wurde, Code hinzufügen oder eine neue Formularvorlage erstellen, die mit dem InfoPath 2003-kompatiblen Objektmodell (wie unter Erstellen einer Formularvorlage mithilfe des [InfoPath 2003-Objektmodells](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)beschrieben) funktioniert, Microsoft InfoPath verwendet eine Teilmenge der Objekte und Member, die vom [Microsoft.Office.Interop.InfoPath.SemiTrust-Namespace](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) bereitgestellt werden und mit denen von InfoPath 2003 identisch sind.</span><span class="sxs-lookup"><span data-stu-id="46c26-105">When you add code to a form template that was created with the Microsoft Office InfoPath 2003 Toolkit or create a new form template that works with the InfoPath 2003-compatible object model (as described in [Create a Form Template Using the InfoPath 2003 Object Model](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)), by default, Microsoft InfoPath will use a subset of the objects and members provided by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace that are identical to those used by InfoPath 2003.</span></span> <span data-ttu-id="46c26-106">Dies dient der Kompatibilität mit InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="46c26-106">This is done to provide compatibility with InfoPath 2003.</span></span> <span data-ttu-id="46c26-107">Das vom [Microsoft.Office.Interop.InfoPath.SemiTrust-Namespace](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) bereitgestellte Objektmodell enthält jedoch zusätzliche Objekte und Member, die neue Funktionen bereitstellen, die Office InfoPath 2007 und InfoPath hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="46c26-107">However, the object model provided by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace includes additional objects and members that provide new functionality that was added to Office InfoPath 2007 and InfoPath.</span></span> 
  
<span data-ttu-id="46c26-108">Beispielsweise bieten die [Schnittstellen PermissionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.PermissionObject.aspx) und [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.aspx) neue Funktionen zur Verwaltung von Informationsrechten, die in InfoPath 2003 nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="46c26-108">For example, the [PermissionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.PermissionObject.aspx) and [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.aspx) interfaces provide new information rights management functionality that is not available in InfoPath 2003.</span></span> <span data-ttu-id="46c26-109">Dies und andere neue Objekte, die microsoft hinzugefügt wurden. Office.Interop.InfoPath.SemiTrust-Namespace sind standardmäßig nicht verfügbar, wenn Sie formularvorlage für verwalteten Code mit InfoPath 2003-kompatiblem Objektmodell öffnen oder erstellen.</span><span class="sxs-lookup"><span data-stu-id="46c26-109">This, and other new objects added to the Microsoft.Office.Interop.InfoPath.SemiTrust namespace are not available by default when you open or create managed code form template with InfoPath 2003-compatible object model.</span></span> 
  
<span data-ttu-id="46c26-110">In ähnlicher Weise bietet [die _XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) die gleiche Funktionalität wie InfoPath 2003. Die [_XDocument3-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.aspx) wurde so versioniert, dass sie zusätzliche Eigenschaften und Methoden enthält, die in Office InfoPath 2007 hinzugefügt wurden, und die [_XDocument4](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument4.aspx) wurde so versioniert, dass sie zusätzliche Eigenschaften und Methoden enthält, die in InfoPath hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="46c26-110">Similarly, while the [_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) interface provides the same functionality as InfoPath 2003; the [_XDocument3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.aspx) interface has been versioned to include additional properties and methods that were added in Office InfoPath 2007, and the [_XDocument4](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument4.aspx) has been versioned to include additional properties and methods that were added in InfoPath.</span></span> 
  
<span data-ttu-id="46c26-111">Wenn Sie Objekte und Elemente verwenden möchten, die in Office InfoPath 2007 oder InfoPath in einem Formularvorlagenprojekt hinzugefügt wurden, das mithilfe des vom **Microsoft.Office.Interop.InfoPath.SemiTrust-Namespace** bereitgestellten Objektmodells erstellt wurde, können Sie dies tun, aber Code, der diese Elemente verwendet, ist nicht mit InfoPath 2003 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="46c26-111">If you want to use objects and members that were added in Office InfoPath 2007 or InfoPath in a form template project created using the object model provided by the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace, you can do so, but code that uses these members will not be compatible with InfoPath 2003.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="46c26-112">Alle Formularvorlagen mit Geschäftslogik, die mithilfe des vom **Microsoft.Office.Interop.InfoPath.SemiTrust-Namespace** bereitgestellten Objektmodells erstellt wurden, unabhängig davon, ob sie Objekte und Elemente verwenden, die mit InfoPath kompatibel sind oder nicht, werden für browserfähige Formularvorlagen, die in Microsoft SharePoint Server 2010 mit InfoPath Forms Services bereitgestellt werden, nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="46c26-112">All form templates with business logic created using the object model provided by the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace, whether they use objects and members compatible with InfoPath or not, are not supported for browser-enabled form templates deployed to Microsoft SharePoint Server 2010 with InfoPath Forms Services.</span></span> <span data-ttu-id="46c26-113">Die Geschäftslogik für browserfähige Formularvorlagen muss das neue InfoPath-Objektmodell mit verwalteten Code verwenden, das von [Microsoft.Office. InfoPath-Namespace.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx)</span><span class="sxs-lookup"><span data-stu-id="46c26-113">Business logic for browser-enabled form templates must use the new InfoPath managed code object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace.</span></span> 
  
## <a name="example"></a><span data-ttu-id="46c26-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="46c26-114">Example</span></span>

### <a name="creating-an-xdocument-or-application-object-variable-to-access-new-object-model-members"></a><span data-ttu-id="46c26-115">Erstellen einer XDocument- oder Anwendungsobjektvariablen zum Zugreifen auf neue Objektmodellmember</span><span class="sxs-lookup"><span data-stu-id="46c26-115">Creating an XDocument or Application Object Variable to Access New Object Model Members</span></span>

<span data-ttu-id="46c26-116">Damit Sie auf die neuen im **Microsoft.Office.Interop.InfoPath.SemiTrust**-Namespace verfügbaren Objekte und Member zugreifen können, müssen Sie Objektvariablen deklarieren und in die richtige Version der Schnittstelle umwandeln, die diese Member implementiert.</span><span class="sxs-lookup"><span data-stu-id="46c26-116">To access the new objects and members that are available in the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace, you must declare and cast object variables to the correct version of the interface that implements these members.</span></span> <span data-ttu-id="46c26-117">Standardmäßig greifen die `thisXDocument` Variablen und auf die `thisApplication` InfoPath 2003-kompatiblen  Versionen der entsprechenden _XDocument2 und [_Application2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) zu.</span><span class="sxs-lookup"><span data-stu-id="46c26-117">By default, the  `thisXDocument` and  `thisApplication` variables access the InfoPath 2003-compatible versions of the corresponding **_XDocument2** and [_Application2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) interfaces.</span></span> <span data-ttu-id="46c26-118">Um auf die **_XDocument3-** und [_Application3-Schnittstellen](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application3.aspx) zu zugreifen, die Zugriff auf neue Funktionen bieten, müssen Sie eine Objektvariable des Typs **_XDocument3** oder **_Application3** deklarieren und dann das von der oder -Variable zurückgegebene Objekt in denselben Typ wie in den folgenden Beispielen dargestellt `thisXDocument` casten. `thisApplication`</span><span class="sxs-lookup"><span data-stu-id="46c26-118">To access the **_XDocument3** and [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application3.aspx) interfaces that provide access to new functionality, you must declare an object variable of the **_XDocument3** or **_Application3** type, and then cast the object returned by the  `thisXDocument` or  `thisApplication` variable to the same type as shown in the following examples.</span></span> 
  
```cs
// Declare an object variable of type _XDocument3 and
// cast the object returned by the thisXDocument variable to
// the same type.
_XDocument3 thisXDocument3 = (_XDocument3)thisXDocument;
```

```vb
' Declare an object variable of type _XDocument3 and
' cast the object returned by the thisXDocument variable to
' the same type.
Dim thisXDocument3 As _XDocument3 = _
   DirectCast(thisXDocument, _XDocument3)
```

```cs
// Declare an object variable of type _Application3 and
// cast the object returned by the thisApplication variable to
// the same type.
_Application3 thisApplication3 = (_Application3)thisXDocument;
```

```vb
' Declare an object variable of type _Application3 and
' cast the object returned by the thisXApplication variable to
' the same type.
Dim thisDocument As _XDocument3 = _
   DirectCast(thisXDocument, _XDocument3)
```

### <a name="accessing-a-new-object-from-the-xdocument-or-application-object-variable-using-an-accessor-property"></a><span data-ttu-id="46c26-119">Zugreifen auf ein neues Objekt von der XDocument- oder Anwendungsobjektvariable aus mithilfe einer Accessoreigenschaft</span><span class="sxs-lookup"><span data-stu-id="46c26-119">Accessing a New Object From The XDocument or Application Object Variable Using an Accessor Property</span></span>

<span data-ttu-id="46c26-120">Nachdem Sie eine Variable der späteren Version _ **XDocument3** oder _Application3 erstellt haben, können Sie damit auf ein Objekt oder Element zugreifen, das neue InfoPath-Funktionen bietet. </span><span class="sxs-lookup"><span data-stu-id="46c26-120">After you have created a variable of the later version _ **XDocument3** or **_Application3** type, you can use it to access an object or member that provides new InfoPath functionality.</span></span> 
  
<span data-ttu-id="46c26-121">Im folgenden Beispiel wird gezeigt, wie Sie eine Objektvariable vom Typ _ **XDocument3** mit der [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.Permission.aspx) accessor-Eigenschaft verwenden, um auf die neue **Permission-Schnittstelle** und deren [Enabled-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.Enabled.aspx) zu zugreifen, um zu ermitteln, ob Berechtigungseinstellungen für das Formular aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="46c26-121">The following example shows how to use an object variable of type _ **XDocument3** with the [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.Permission.aspx) accessor property to access the new **Permission** interface and its [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.Enabled.aspx) property to determine if permission settings are enabled for the form.</span></span> 
  
```cs
// Declare an object variable of type _XDocument3 and
// cast the object returned by the thisXDocument variable to
// the same type.
_XDocument3 thisXDocument3 = (_XDocument3)thisXDocument;
// Use the object variable to access the later version object and
// property.
thisXDocument.UI.Alert(thisDocument3.Permission.Enabled.ToString());
```

```vb
' Declare an object variable of type _XDocument3 and
' cast the object returned by the thisXDocument variable to
' the same type.
Dim thisXDocument3 As _XDocument3 = _
   DirectCast(thisXDocument, _XDocument3)
' Use the object variable to access the later version object and
' property.
thisXDocument.UI.Alert(thisDocument3.Permission.Enabled.ToString())
```

### <a name="accessing-a-versioned-object-and-casting-to-the-versioned-type"></a><span data-ttu-id="46c26-122">Zugreifen auf ein Versionsobjekt und Umwandeln in den Versionstyp</span><span class="sxs-lookup"><span data-stu-id="46c26-122">Accessing a Versioned Object and Casting to the Versioned Type</span></span>

<span data-ttu-id="46c26-123">Wenn einem Objekt, das im InfoPath 2003-Objektmodell vorhanden war, neue Eigenschaften oder Methoden hinzugefügt werden, hat das Objekt, das diese neuen Member implementiert, einen Versionsnamen.</span><span class="sxs-lookup"><span data-stu-id="46c26-123">If an object that existed in the InfoPath 2003 object model has new properties or methods added to it, the object that implements those new members will have a name that is versioned.</span></span>
  
<span data-ttu-id="46c26-124">Beispielsweise bietet das [ViewInfo-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.aspx) keinen Zugriff auf zwei neue Eigenschaften, die nur verfügbar sind, wenn das [viewInfo2-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.aspx) mit der Version verwendet wird: die [Eigenschaften Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.Caption.aspx) und [HideName.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.HideName.aspx)</span><span class="sxs-lookup"><span data-stu-id="46c26-124">For example, the [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.aspx) object does not provide access to two new properties that are only available when using the versioned [ViewInfo2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.aspx) object: the [Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.Caption.aspx) and [HideName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.HideName.aspx) properties.</span></span> 
  
<span data-ttu-id="46c26-125">Für den Zugriff auf diese Eigenschaften müssen Sie eine Objektvariable vom Typ **ViewInfo2** deklarieren und das von der [ViewInfos-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.ViewInfos.aspx) der **_XDocument3-Objektvariable** zurückgegebene Objekt in den **ViewInfo2-Typ** umverknen, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="46c26-125">To access these properties, you must declare an object variable of type **ViewInfo2** and cast the object returned by the [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.ViewInfos.aspx) property of the _ **XDocument3** object variable to the **ViewInfo2** type as shown in the following example.</span></span> 
  
```cs
// Declare an object variable of type _XDocument3 and
// cast the object returned by the thisXDocument variable to
// the same type.
_XDocument3 thisXDocument3 = (_XDocument3)thisXDocument;
// Declare an object variable of type ViewInfo2 and cast the object 
// returned by the ViewInfos property to that type.
ViewInfo2 thisView = (ViewInfo2)thisXDocument3.ViewInfos["View2"];
// Display the value of the new HideName property.
thisXDocument3.UI.Alert(thisView.HideName.ToString());
```

```vb
' Declare an object variable of type _XDocument3 and
' cast the object returned by the thisXDocument variable to
' the same type.
Dim thisXDocument3 As _XDocument3 = _
   DirectCast(thisXDocument, _XDocument3)
' Declare an object variable of type ViewInfo2 and cast the object 
' returned by the ViewInfos property to that type.
Dim thisView As ViewInfo2 = _
   DirectCast(thisXDocument3.ViewInfos("View2"), ViewInfo2)
' Display the value of the new HideName property.
thisXDocument3.UI.Alert(thisView.HideName.ToString())
```


