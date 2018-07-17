---
title: Analysieren Sie einen Datenstrom aus eine binäre Eigenschaft zum Lesen der TZREG-Struktur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 9e36e0d9-a28b-5978-0e23-f76e1bf506b5
description: In diesem Thema wird wie die TZREG-Struktur aus der beibehaltenen Format gespeichert, in die binäre Eigenschaft PidLidTimeZoneStruct lesen.
ms.openlocfilehash: 4dd63e7f1539ab7496c45a80b5ec6a17683ffcb2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790943"
---
# <a name="parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure"></a><span data-ttu-id="22e93-103">Analysieren Sie einen Datenstrom aus eine binäre Eigenschaft zum Lesen der TZREG-Struktur</span><span class="sxs-lookup"><span data-stu-id="22e93-103">Parse a stream from a binary property to read the TZREG structure</span></span>

<span data-ttu-id="22e93-104">In diesem Thema wird wie die [TZREG](tzreg.md) -Struktur aus der beibehaltenen Format gespeichert, in die binäre Eigenschaft [PidLidTimeZoneStruct](http://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx)lesen.</span><span class="sxs-lookup"><span data-stu-id="22e93-104">This topic shows how to read the [TZREG](tzreg.md) structure from the persisted format stored in the binary property [PidLidTimeZoneStruct](http://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx).</span></span>
  
```cpp
TZREG* BinToTZREG(ULONG cbReg, LPBYTE lpbReg)  
{ 
    if (!lpbReg) return NULL;  
 
    // Update this if parsing code is changed. 
    if (cbReg &amp;lt; 3*sizeof(long) + 2*sizeof(WORD) + 2*sizeof(SYSTEMTIME)) return NULL; 
 
    TZREG tzReg = {0}; 
    LPBYTE lpPtr = lpbReg; 
 
    tzReg.lBias = *((long*)lpPtr); 
    lpPtr += sizeof(long); 
    tzReg.lStandardBias = *((long*)lpPtr); 
    lpPtr += sizeof(long); 
    tzReg.lDaylightBias = *((long*)lpPtr); 
    lpPtr += sizeof(long); 
    lpPtr += sizeof(WORD);// reserved 
 
    tzReg.stStandardDate = *((SYSTEMTIME*)lpPtr); 
    lpPtr += sizeof(SYSTEMTIME); 
    lpPtr += sizeof(WORD);// reserved 
    tzReg.stDaylightDate = *((SYSTEMTIME*)lpPtr); 
    lpPtr += sizeof(SYSTEMTIME); 
 
    TZREG* ptzReg = NULL; 
    ptzReg = new TZREG; 
    if (ptzReg) 
    { 
        *ptzReg = tzReg; 
    } 
 
    return ptzReg; 
} 

```

## <a name="see-also"></a><span data-ttu-id="22e93-105">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22e93-105">See also</span></span>

- [<span data-ttu-id="22e93-106">Lesen Sie Zeitzone Eigenschaften, ausgehend von einem Termin</span><span class="sxs-lookup"><span data-stu-id="22e93-106">Read time zone properties from an appointment</span></span>](how-to-read-time-zone-properties-from-an-appointment.md)
