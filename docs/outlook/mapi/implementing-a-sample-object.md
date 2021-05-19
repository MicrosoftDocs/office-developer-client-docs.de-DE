---
title: Implementieren eines Beispielsobjekts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 23b6ad1a-0b50-429f-8819-ab72c56581c2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a681e68c0718e49da331946d75ecb7b4fab7afe2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332830"
---
# <a name="implementing-a-sample-object"></a><span data-ttu-id="d466b-103">Implementieren eines Beispielsobjekts</span><span class="sxs-lookup"><span data-stu-id="d466b-103">Implementing a sample object</span></span>

<span data-ttu-id="d466b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d466b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d466b-105">Advise sink objects — objects that support the [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface – are MAPI objects that client applications implement for processing notifications.</span><span class="sxs-lookup"><span data-stu-id="d466b-105">Advise sink objects — objects that support the [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface — are MAPI objects that client applications implement for processing notifications.</span></span> <span data-ttu-id="d466b-106">**IMAPIAdviseSink** erbt direkt von [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) und enthält nur eine Methode, **OnNotify**.</span><span class="sxs-lookup"><span data-stu-id="d466b-106">**IMAPIAdviseSink** inherits directly from [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) and contains only one method, **OnNotify**.</span></span> <span data-ttu-id="d466b-107">Daher erstellt ein Client code für die drei Methoden in **IUnknown** und [OnNotify,](imapiadvisesink-onnotify.md)um ein Advise Sink-Objekt zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="d466b-107">Therefore, to implement an advise sink object, a client creates code for the three methods in **IUnknown** and for [OnNotify](imapiadvisesink-onnotify.md).</span></span>
  
<span data-ttu-id="d466b-108">Die Mapidefs.h-Headerdatei definiert eine **IMAPIAdviseSink-Schnittstellenimplementierung** mithilfe von **DECLARE_MAPI_INTERFACE**, wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d466b-108">The Mapidefs.h header file defines an **IMAPIAdviseSink** interface implementation by using **DECLARE_MAPI_INTERFACE**, as follows:</span></span>
  
```cpp
#define      INTERFACE  IMAPIAdviseSink
DECLARE_MAPI_INTERFACE_(IMAPIAdviseSink, IUnknown)
{
    BEGIN_INTERFACE
    MAPI_IUNKNOWN_METHODS(PURE)
    MAPI_IMAPIADVISESINK_METHODS(PURE)
};
 
```

<span data-ttu-id="d466b-109">Clients, die beratende Sink-Objekte implementieren, können ihre Schnittstellen in ihren Objekten manuell oder mit den Makros MAPI_IUNKNOWN_METHODS **und** **MAPI_IMAPIADVISESINK_METHODS** definieren.</span><span class="sxs-lookup"><span data-stu-id="d466b-109">Clients that implement advise sink objects can define their interfaces in their objects manually or with the **MAPI_IUNKNOWN_METHODS** and **MAPI_IMAPIADVISESINK_METHODS** macros.</span></span> <span data-ttu-id="d466b-110">Objekt implementierer sollten die Schnittstellenmakros nach Möglichkeit verwenden, um die Konsistenz zwischen Objekten sicherzustellen und Zeit und Aufwand zu sparen.</span><span class="sxs-lookup"><span data-stu-id="d466b-110">Object implementers should use the interface macros whenever possible to ensure consistency across objects and to save time and effort.</span></span> 
  
<span data-ttu-id="d466b-111">Die Implementierung [der Methoden IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) und [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) ist relativ einfach, da in der Regel nur wenige Codezeilen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="d466b-111">Implementing the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) and [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) methods is relatively simple because typically only a few lines of code are needed.</span></span> <span data-ttu-id="d466b-112">Daher können Clients und Dienstanbieter, die Objekte implementieren, ihre **AddRef-** und **Releaseimplementierung** inline umsetzen.</span><span class="sxs-lookup"><span data-stu-id="d466b-112">Therefore, clients and service providers that implement objects can make their **AddRef** and **Release** implementations inline.</span></span> <span data-ttu-id="d466b-113">Der folgende Code zeigt, wie Sie ein C++ advise sink-Objekt mit Inlineimplementierung von **AddRef** und **Release definieren.**</span><span class="sxs-lookup"><span data-stu-id="d466b-113">The following code shows how to define a C++ advise sink object with inline implementations of **AddRef** and **Release**.</span></span>
  
```cpp
class  CMAPIAdviseSink : public IMAPIAdviseSink
{
public:
    STDMETHODIMP QueryInterface
                    (REFIID                     riid,
                     LPVOID *                   ppvObj);
    inline STDMETHODIMP_(ULONG) AddRef
                    () { InterlockedIncrement(m_cRef);
                         ++m_cRef;
                         InterlockedDecrement(m_cRef);
                         return m_cRef; };
    inline STDMETHODIMP_(ULONG) Release
                    () { InterlockedIncrement(m_cRef);
                         ULONG ulCount = --m_cRef;
                         InterlockedDecrement(m_cRef);
                         if (!ulCount)  delete this;
                         return ulCount;};
    MAPI_IMAPIADVISESINK_METHODS(IMPL);
    BOOL WINAPI AddConnection (LPMDB pMDBObj, ULONG ulConnection);
    void WINAPI RemoveAllLinks (LPMDB pMDBObj);
// Constructors and destructors.
public :
    inline CMAPIAdviseSink  (CStoreClient * pStore)
                            { m_cRef = 1;
                              m_ulConnection = 0;
                              m_pStore = pStore;
                              AddRef;};
    ~CMAPIAdviseSink () {Release};
private :
    ULONG               m_cRef;
    CStoreClient *      m_pStore;
    ULONG               m_ulConnection;
};
 
```

<span data-ttu-id="d466b-114">In C besteht das Objekt advise sink aus den folgenden Elementen:</span><span class="sxs-lookup"><span data-stu-id="d466b-114">In C, the advise sink object is composed of the following elements:</span></span>
  
- <span data-ttu-id="d466b-115">Ein Zeiger auf eine vtable, die Zeiger auf Implementierungen der einzelnen Methoden in **IUnknown** und **IMAPIAdviseSink enthält.**</span><span class="sxs-lookup"><span data-stu-id="d466b-115">A pointer to a vtable that contains pointers to implementations of each of the methods in **IUnknown** and **IMAPIAdviseSink**.</span></span>
    
- <span data-ttu-id="d466b-116">Datenm member.</span><span class="sxs-lookup"><span data-stu-id="d466b-116">Data members.</span></span>
    
<span data-ttu-id="d466b-117">Das folgende Codebeispiel zeigt, wie Sie ein #A0 in C definieren und dessen vtable erstellen.</span><span class="sxs-lookup"><span data-stu-id="d466b-117">The following code example shows how to define an advise sink object in C and construct its vtable.</span></span> 
  
```cpp
// Object definition.
typedef struct _ADVISESINK
{
    const ADVISE_Vtbl FAR *    lpVtbl;
    ULONG             cRef;
    STORECLIENT      *pStore;
    ULONG             ulConnection;
} ADVISESINK, *LPADVISESINK;
// vtable definition.
static const ADVISE_Vtbl vtblADVISE =
{
    ADVISE_QueryInterface,
    ADVISE_AddRef,
    ADVISE_Release,
    ADVISE_OnNotify
};
 
```

<span data-ttu-id="d466b-118">Nachdem Sie ein Objekt in C deklariert haben, müssen Sie es initialisieren, indem Sie den #A0 auf die Adresse der konstruierten vtable festlegen, wie im folgenden Code gezeigt:</span><span class="sxs-lookup"><span data-stu-id="d466b-118">After you declare an object in C, you must initialize it by setting the vtable pointer to the address of the constructed vtable, as shown in the following code:</span></span>
  
```cpp
LPADVISESINK lpMyObj = NULL;
HRESULT hr = (*lpAllocateBuffer) (sizeof(ADVISESINK),
                 (LPVOID *)&lpMyObj);
lpMyObj->lpVtbl = &vtblADVISE;
 
```

## <a name="see-also"></a><span data-ttu-id="d466b-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d466b-119">See also</span></span>

- [<span data-ttu-id="d466b-120">Übersicht über die MAPI-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d466b-120">MAPI Property Overview</span></span>](mapi-property-overview.md)
- [<span data-ttu-id="d466b-121">Implementieren von MAPI-Objekten</span><span class="sxs-lookup"><span data-stu-id="d466b-121">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

