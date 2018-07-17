---
title: IFreeBusyDataGetFBPublishRange
manager: soliver
ms.date: 09/23/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a8bbe0c-17d1-9349-4c63-f257faf4edda
description: Dient zum Abrufen eines vordefinierten Zeitraums für eine Enumeration der Datenblöcke Frei/Gebucht-Informationen für einen Benutzer.
ms.openlocfilehash: 2a322a43da38a0b902789f4c83baaabd769154c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790960"
---
# <a name="ifreebusydatagetfbpublishrange"></a><span data-ttu-id="1705a-103">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="1705a-103">IFreeBusyData::GetFBPublishRange</span></span>

<span data-ttu-id="1705a-104">Dient zum Abrufen eines vordefinierten Zeitraums für eine Enumeration der Datenblöcke Frei/Gebucht-Informationen für einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="1705a-104">Gets a preset time range for an enumeration of free/busy blocks of data for a user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1705a-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="1705a-105">Quick info</span></span>

<span data-ttu-id="1705a-106">Finden Sie unter [IFreeBusyData](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="1705a-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT GetFBPublishRange( 
     LONG *prtmStart,  
     LONG *prtmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="1705a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1705a-107">Parameters</span></span>

<span data-ttu-id="1705a-108">_prtmStart_</span><span class="sxs-lookup"><span data-stu-id="1705a-108">_prtmStart_</span></span>
  
> <span data-ttu-id="1705a-109">[out] Ein relative Zeitwert für den Anfang des Frei/Gebucht-Informationen.</span><span class="sxs-lookup"><span data-stu-id="1705a-109">[out] A relative time value for the start of free/busy information.</span></span> <span data-ttu-id="1705a-110">Dieser Wert ist die Anzahl der Minuten seit dem 1. Januar 1601.</span><span class="sxs-lookup"><span data-stu-id="1705a-110">This value is the number of minutes since January 1, 1601.</span></span>
    
<span data-ttu-id="1705a-111">_prtmEnd_</span><span class="sxs-lookup"><span data-stu-id="1705a-111">_prtmEnd_</span></span>
  
> <span data-ttu-id="1705a-112">[out] Ein relative Zeitwert für das Ende des Frei/Gebucht-Informationen.</span><span class="sxs-lookup"><span data-stu-id="1705a-112">[out] A relative time value for the end of free/busy information.</span></span> <span data-ttu-id="1705a-113">Dieser Wert ist die Anzahl der Minuten seit dem 1. Januar 1601.</span><span class="sxs-lookup"><span data-stu-id="1705a-113">This value is the number of minutes since January 1, 1601.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="1705a-114">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="1705a-114">Return values</span></span>

<span data-ttu-id="1705a-115">S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="1705a-115">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1705a-116">Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="1705a-116">Remarks</span></span>

<span data-ttu-id="1705a-117">Ein Anbieter Frei/Gebucht-Informationen ruft [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) oder [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) , um den Zeitraum für eine Enumeration festzulegen.</span><span class="sxs-lookup"><span data-stu-id="1705a-117">A free/busy provider calls [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) or [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) to set the time range for an enumeration.</span></span> <span data-ttu-id="1705a-118">Wenn [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) oder [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) nicht aufgerufen wurde, müssen die Standardwerte für **PrtmStart** und **PrtmEnd** zwischen dem 1. April 1601 00:00:00Z und dem 31. August 4500 11:59:59Z festgelegt werden fest.</span><span class="sxs-lookup"><span data-stu-id="1705a-118">If either [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) or [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) has not been called, the default values for **prtmStart** and **prtmEnd** must be set between April 1st, 1601 00:00:00Z and August 31, 4500 11:59:59Z respectively.</span></span> <span data-ttu-id="1705a-119">Darüber hinaus sollten Sie die Startzeit größer sein als die Endzeit nicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="1705a-119">Additionally, you should not set the start time to be greater than the end time.</span></span> 
  
<span data-ttu-id="1705a-120">**IFreeBusyData::GetFBPublishRange** muss zurückgegeben werden, dass die zwischengespeicherten Werte für den Zeitraum vom letzten Aufruf für **IFreeBusyData::EnumBlocks** oder **IFreeBusyData::SetFBRange**festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1705a-120">**IFreeBusyData::GetFBPublishRange** must return the cached values for the time range set by the most recent call for **IFreeBusyData::EnumBlocks** or **IFreeBusyData::SetFBRange**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1705a-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1705a-121">See also</span></span>

- [<span data-ttu-id="1705a-122">Verwenden Sie relative Zeit Zugriff auf Frei/Gebucht-Daten</span><span class="sxs-lookup"><span data-stu-id="1705a-122">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)
- [<span data-ttu-id="1705a-123">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="1705a-123">IFreeBusyData::EnumBlocks</span></span>](ifreebusydata-enumblocks.md)
- [<span data-ttu-id="1705a-124">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="1705a-124">IFreeBusyData::SetFBRange</span></span>](ifreebusydata-setfbrange.md)
