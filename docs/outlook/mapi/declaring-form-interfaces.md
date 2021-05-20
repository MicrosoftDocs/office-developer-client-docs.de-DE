---
title: Deklarieren von Formularschnittstellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79283301-e544-4a4d-96c2-3f81dc5b3731
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0fa742b7ff6d98e3a0f475accbc440d22eac0919
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437511"
---
# <a name="declaring-form-interfaces"></a><span data-ttu-id="f8704-103">Deklarieren von Formularschnittstellen</span><span class="sxs-lookup"><span data-stu-id="f8704-103">Declaring Form Interfaces</span></span>

  
  
<span data-ttu-id="f8704-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8704-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8704-105">Sie können die Deklarationen Ihrer Implementierungen von MAPI-Formularschnittstellen vereinfachen, indem Sie die MAPI_ _interface__METHOD-Makros verwenden. Dabei handelt es sich bei der Schnittstelle um eine Formularschnittstelle, die in der Mapiform.h-Headerdatei definiert ist. </span><span class="sxs-lookup"><span data-stu-id="f8704-105">You can simplify the declarations of your implementations of MAPI form interfaces by using the MAPI_ _interface__METHOD macros, where  _interface_ is a form interface defined in the Mapiform.h header file.</span></span> <span data-ttu-id="f8704-106">Sie müssen diese Makros nicht verwenden, aber andern falls nicht, sollten Sie besonders darauf achten, dass Ihre Deklarationen den Deklarationen in der Mapiform.h-Headerdatei entsprechen.</span><span class="sxs-lookup"><span data-stu-id="f8704-106">You are not required to use these macros, but if you do not, you should take particular care that your declarations conform to the declarations in the Mapiform.h header file.</span></span> <span data-ttu-id="f8704-107">Beispielsweise können Sie die Formularobjektklasse des Formularservers wie folgt deklarieren:</span><span class="sxs-lookup"><span data-stu-id="f8704-107">For example, you could declare your form server's form object class like the following:</span></span> 
  
```cpp
class CMyForm : public IPersistMessage, public IMAPIForm,
                public IMAPIFormAdviseSink
{
public:
    CMyForm(CClassFactory *);    // constructorr takes a class factory object
    ~CMyForm(void);
// MAPI methods that need to be implemented.
    MAPI_IUNKNOWN_METHODS(IMPL);
    MAPI_GETLASTERROR_METHOD(IMPL);
    MAPI_IPERSISTMESSAGE_METHODS(IMPL);
    MAPI_IMAPIFORM_METHODS(IMPL);
    MAPI_IMAPIFORMADVISESINK_METHODS(IMPL);
// Add other implementation specific items.
};

```

## <a name="see-also"></a><span data-ttu-id="f8704-108">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8704-108">See also</span></span>



[<span data-ttu-id="f8704-109">Schreiben von Formularservercode</span><span class="sxs-lookup"><span data-stu-id="f8704-109">Writing Form Server Code</span></span>](writing-form-server-code.md)

