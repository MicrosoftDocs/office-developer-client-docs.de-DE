---
title: MNLS_lstrlenW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d342a956-1164-4c9c-b0bb-7a0b72dc97fc
description: 'Letzte Änderung: 21. Februar 2012'
ms.openlocfilehash: 31f699d1193e55a88e57a0f491658e0d537ef75d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338465"
---
# <a name="mnls_lstrlenw"></a><span data-ttu-id="827d8-103">MNLS_lstrlenW</span><span class="sxs-lookup"><span data-stu-id="827d8-103">MNLS_lstrlenW</span></span>

  
  
<span data-ttu-id="827d8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="827d8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="827d8-105">Bestimmt die Länge der angegebenen Unicode-Zeichenfolge, mit Ausnahme des endenden Nullzeichens.</span><span class="sxs-lookup"><span data-stu-id="827d8-105">Determines the length of the specified Unicode string, excluding the terminating null character.</span></span>
  
> [!TIP]
> <span data-ttu-id="827d8-106">Erwägen Sie stattdessen die Verwendung von [StringCchLength.](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="827d8-106">Consider using [StringCchLength](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx) instead.</span></span> 
  
```cpp
int MNLS_lstrlen(
  LPCWSTR lpsz);
```

## <a name="parameters"></a><span data-ttu-id="827d8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="827d8-107">Parameters</span></span>

 <span data-ttu-id="827d8-108">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="827d8-108">_lpsz_</span></span>
  
> <span data-ttu-id="827d8-109">[in] Die zu überprüfende Nullend-Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="827d8-109">[in] The null-terminated Unicode string to be checked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="827d8-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="827d8-110">Return value</span></span>

<span data-ttu-id="827d8-111">Die Funktion gibt eine ganze Zahl mit der Länge der Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="827d8-111">The function returns an integer with the length of the string.</span></span> <span data-ttu-id="827d8-112">Es handelt sich um eine Anzahl von Zeichen in der Zeichenfolge, mit Ausnahme des endenden Nullzeichens.</span><span class="sxs-lookup"><span data-stu-id="827d8-112">It is a count of characters in the string, excluding the terminating null character.</span></span> <span data-ttu-id="827d8-113">Wenn  _lpsz_ NULL ist, gibt die Funktion Null zurück.</span><span class="sxs-lookup"><span data-stu-id="827d8-113">If  _lpsz_ is NULL, the function returns zero.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="827d8-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="827d8-114">Remarks</span></span>

<span data-ttu-id="827d8-115">Diese Funktion umschließt die **lstrlen-Funktion.**</span><span class="sxs-lookup"><span data-stu-id="827d8-115">This function wraps the **lstrlen** function.</span></span> <span data-ttu-id="827d8-116">Weitere Informationen finden Sie unter [lstrlen](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="827d8-116">For more information, see [lstrlen](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="827d8-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="827d8-117">See also</span></span>



[<span data-ttu-id="827d8-118">lstrlen</span><span class="sxs-lookup"><span data-stu-id="827d8-118">lstrlen</span></span>](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx)
  
[<span data-ttu-id="827d8-119">StringCchLength</span><span class="sxs-lookup"><span data-stu-id="827d8-119">StringCchLength</span></span>](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx)

