---
title: debugPrintf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- debugPrintf
keywords:
- debugprintf-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 9ad541f6-0b35-4f50-926a-8940e3f8033a
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 08bde61573874c137b18856fd24d23b324a35328
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424798"
---
# <a name="debugprintf"></a><span data-ttu-id="06ea2-104">debugPrintf</span><span class="sxs-lookup"><span data-stu-id="06ea2-104">debugPrintf</span></span>

<span data-ttu-id="06ea2-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="06ea2-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="06ea2-106">Framework library function that writes a null-terminated byte-string to the active debugger via the Windows SDK function **OutputDebugStringA**.</span><span class="sxs-lookup"><span data-stu-id="06ea2-106">Framework library function that writes a null-terminated byte-string to the active debugger via the Windows SDK function **OutputDebugStringA**.</span></span> <span data-ttu-id="06ea2-107">Wenn die Anwendung keinen Debugger besitzt, zeigt der Systemdebugger die Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="06ea2-107">If the application has no debugger, the system debugger displays the string.</span></span> <span data-ttu-id="06ea2-108">Wenn die Anwendung keinen Debugger hat und der Systemdebugger nicht aktiv ist, **führt debugPrintf** nichts aus.</span><span class="sxs-lookup"><span data-stu-id="06ea2-108">If the application has no debugger and the system debugger is not active, **debugPrintf** does nothing.</span></span> 
  
<span data-ttu-id="06ea2-109">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="06ea2-109">This function does not return a value.</span></span>
  
```cs
void WINAPI debugPrintf(LPSTR lpFormat, arguments);
```

## <a name="parameters"></a><span data-ttu-id="06ea2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="06ea2-110">Parameters</span></span>

 <span data-ttu-id="06ea2-111">_lpFormat (LPSTR)_</span><span class="sxs-lookup"><span data-stu-id="06ea2-111">_lpFormat (LPSTR)_</span></span>
  
<span data-ttu-id="06ea2-112">Die Formatzeichenfolge, die der Syntax und Regeln für die mit der **sprintf-Funktion verwendete Folgt.**</span><span class="sxs-lookup"><span data-stu-id="06ea2-112">The format string, which follows the syntax and rules for that used with the **sprintf** function.</span></span> 
  
 <span data-ttu-id="06ea2-113">_Argumente_</span><span class="sxs-lookup"><span data-stu-id="06ea2-113">_arguments_</span></span>
  
<span data-ttu-id="06ea2-114">Null oder mehr Argumente, die der Formatzeichenfolge entsprechen.</span><span class="sxs-lookup"><span data-stu-id="06ea2-114">Zero or more arguments to match the format string.</span></span>
  
## <a name="example"></a><span data-ttu-id="06ea2-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="06ea2-115">Example</span></span>

<span data-ttu-id="06ea2-116">Diese Funktion druckt eine Zeichenfolge, um zu zeigen, dass das Steuerelement an sie übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="06ea2-116">This function prints a string to show that control was passed to it.</span></span> <span data-ttu-id="06ea2-117">Das _DEBUG muss vor der Kompilierung definiert werden, sonst führt diese Funktion nichts aus.</span><span class="sxs-lookup"><span data-stu-id="06ea2-117">The _DEBUG flag must be defined before compiling or else this function does nothing.</span></span>
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI debugPrintfExample(void)
{
#ifdef _DEBUG
   debugPrintf("Made it!\r");
#endif
   return 1;
}

```

## <a name="see-also"></a><span data-ttu-id="06ea2-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06ea2-118">See also</span></span>



[<span data-ttu-id="06ea2-119">Funktionen in der Framework-Klassenbibliothek</span><span class="sxs-lookup"><span data-stu-id="06ea2-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

