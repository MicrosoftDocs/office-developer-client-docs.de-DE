---
title: SSortOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSortOrder
api_type:
- COM
ms.assetid: fe181b9a-5903-4cc0-bcd5-2061b440b5b1
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f9d38c90fa5795d34f78c61ce0faa5f76d8f740d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439723"
---
# <a name="ssortorder"></a><span data-ttu-id="29d38-103">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="29d38-103">SSortOrder</span></span>
 
<span data-ttu-id="29d38-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="29d38-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="29d38-105">Definiert, wie die Zeilen einer Tabelle sortiert werden, welche Spalte als Sortiertaste verwendet werden soll, und die Sortierrichtung.</span><span class="sxs-lookup"><span data-stu-id="29d38-105">Defines how to sort the rows of a table, what column to use as the sort key, and the direction of the sort.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="29d38-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="29d38-106">Header file:</span></span>  <br/> |<span data-ttu-id="29d38-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="29d38-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSortOrder
{
  ULONG ulPropTag;
  ULONG ulOrder;
} SSortOrder, FAR *LPSSortOrder;

```

## <a name="members"></a><span data-ttu-id="29d38-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="29d38-108">Members</span></span>

<span data-ttu-id="29d38-109">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="29d38-109">**ulPropTag**</span></span>
  
> <span data-ttu-id="29d38-110">Eigenschaftstag, das den Sortierschlüssel oder für eine kategorisierte Sortierung die Kategoriespalte identifiziert.</span><span class="sxs-lookup"><span data-stu-id="29d38-110">Property tag identifying the sort key or, for a categorized sort, the category column.</span></span>
    
<span data-ttu-id="29d38-111">**ulOrder**</span><span class="sxs-lookup"><span data-stu-id="29d38-111">**ulOrder**</span></span>
  
> <span data-ttu-id="29d38-112">Die Reihenfolge, in der die Daten sortiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="29d38-112">The order in which the data is to be sorted.</span></span> <span data-ttu-id="29d38-113">Mögliche Werte sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="29d38-113">Possible values are as follow:</span></span>
    
  - <span data-ttu-id="29d38-114">TABLE_SORT_ASCEND: Die Tabelle sollte in aufsteigender Reihenfolge sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="29d38-114">TABLE_SORT_ASCEND: The table should be sorted in ascending order.</span></span>
      
  - <span data-ttu-id="29d38-115">TABLE_SORT_COMBINE: Der Sortiervorgang sollte eine Kategorie erstellen, die die eigenschaft, die als Sortierschlüsselspalte im **ulPropTag-Element** identifiziert ist, mit der Sortierschlüsselspalte kombiniert, die in der vorherigen **SSortOrder-Struktur angegeben** ist.</span><span class="sxs-lookup"><span data-stu-id="29d38-115">TABLE_SORT_COMBINE: The sort operation should create a category that combines the property identified as the sort key column in the **ulPropTag** member with the sort key column specified in the previous **SSortOrder** structure.</span></span> 
      
    <span data-ttu-id="29d38-116">TABLE_SORT_COMBINE kann nur verwendet werden, wenn die **SSortOrder-Struktur** als Eintrag in einer [SSortOrderSet-Struktur](ssortorderset.md) verwendet wird, um mehrere Sortierreihenfolgen für eine kategorisierte Sortierung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="29d38-116">TABLE_SORT_COMBINE can only be used when the **SSortOrder** structure is being used as an entry in an [SSortOrderSet](ssortorderset.md) structure to specify multiple sort orders for a categorized sort.</span></span> <span data-ttu-id="29d38-117">TABLE_SORT_COMBINE kann nicht in der ersten **SSortOrder-Struktur** in einer **SSortOrderSet-Struktur verwendet** werden.</span><span class="sxs-lookup"><span data-stu-id="29d38-117">TABLE_SORT_COMBINE cannot be used in the first **SSortOrder** structure in an **SSortOrderSet** structure.</span></span> 
      
  - <span data-ttu-id="29d38-118">TABLE_SORT_DESCEND: Die Tabelle sollte in absteigender Reihenfolge sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="29d38-118">TABLE_SORT_DESCEND: The table should be sorted in descending order.</span></span>
      
  - <span data-ttu-id="29d38-119">TABLE_SORT_CATEG_MAX: Die Tabelle sollte nach dem Maximalwert des **ulPropTag-Members** für die Datenzeilen in den Kategorien sortiert werden, die durch die vorherige Sortierreihenfolge in der **SSortOrderSet-Struktur angegeben** wurden.</span><span class="sxs-lookup"><span data-stu-id="29d38-119">TABLE_SORT_CATEG_MAX: The table should be sorted on the maximum value of the **ulPropTag** member for the data rows in the categories specified by the previous sort order in the **SSortOrderSet** structure.</span></span> 
      
  - <span data-ttu-id="29d38-120">TABLE_SORT_CATEG_MIN: Die Tabelle sollte nach dem Minimalwert des **ulPropTag-Members** für die Datenzeilen in den Kategorien sortiert werden, die in der vorherigen Sortierreihenfolge in der **SSortOrderSet-Struktur** angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="29d38-120">TABLE_SORT_CATEG_MIN: The table should be sorted on the minimum value of the **ulPropTag** member for the data rows in the categories specified by the previous sort order in the in **SSortOrderSet** structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="29d38-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="29d38-121">Remarks</span></span>

<span data-ttu-id="29d38-122">Eine **SSortOrder-Struktur** wird verwendet, um zu beschreiben, wie sie entweder einen Standardsortierungsvorgang oder einen kategorisierten Sortiervorgang ausführen.</span><span class="sxs-lookup"><span data-stu-id="29d38-122">An **SSortOrder** structure is used to describe how to perform either a standard sort operation or a categorized sort operation.</span></span> <span data-ttu-id="29d38-123">**SSortOrder-Strukturen** werden in der Regel in einer **SSortOrderSet-Struktur** kombiniert, um mehrere Sortiertasten und Wegbeschreibungen zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="29d38-123">**SSortOrder** structures are typically combined into an **SSortOrderSet** structure to describe multiple sort keys and directions.</span></span> <span data-ttu-id="29d38-124">**SSortOrderSet-Strukturen** werden in den folgenden Funktionen und Schnittstellenmethoden verwendet:</span><span class="sxs-lookup"><span data-stu-id="29d38-124">**SSortOrderSet** structures are used in the following functions and interface methods:</span></span> 
  
- [<span data-ttu-id="29d38-125">ITableData::HrGetView</span><span class="sxs-lookup"><span data-stu-id="29d38-125">ITableData::HrGetView</span></span>](itabledata-hrgetview.md)
    
- [<span data-ttu-id="29d38-126">IMAPIFolder::SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="29d38-126">IMAPIFolder::SaveContentsSort</span></span>](imapifolder-savecontentssort.md)
    
- [<span data-ttu-id="29d38-127">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="29d38-127">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
    
- [<span data-ttu-id="29d38-128">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="29d38-128">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
- [<span data-ttu-id="29d38-129">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="29d38-129">FBadSortOrderSet</span></span>](fbadsortorderset.md)
    
- [<span data-ttu-id="29d38-130">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="29d38-130">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
<span data-ttu-id="29d38-131">Der Bereich der zulässigen Spalten in einer Tabelle, die als Sortierschlüssel verwendet werden können, hängt vom Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="29d38-131">The range of allowed columns in a table that can be used as a sort key depends on the provider.</span></span> <span data-ttu-id="29d38-132">Spalten, die Teil des aktuellen Spaltensatzes sind, können immer als Sortiertasten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="29d38-132">Columns that are part of the current column set can always be used as sort keys.</span></span> <span data-ttu-id="29d38-133">Jeder Anbieter bestimmt jedoch, ob Sortierschlüssel mithilfe verfügbarer Spalten definiert werden können, die sich nicht im aktuellen Spaltensatz befinden.</span><span class="sxs-lookup"><span data-stu-id="29d38-133">However, each provider determines whether sort keys can be defined by using available columns that are not in the current column set.</span></span> <span data-ttu-id="29d38-134">Eine verfügbare Spalte ist eine Spalte, die von [IMAPITable::QueryColumns](imapitable-querycolumns.md) zurückgegeben wird, wenn TBL_ALL_COLUMNS festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="29d38-134">An available column is a column that is returned from [IMAPITable::QueryColumns](imapitable-querycolumns.md) when the TBL_ALL_COLUMNS flag is set.</span></span> 
  
<span data-ttu-id="29d38-135">Das **ulOrder-Element** gibt sowohl Richtungsreihenfolge als auch Kategorisierungsinformationen an, z. B. nach Unterhaltung ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)), d. h. Unterhaltungsthread, bei dem es sich um eine Reihe von Nachrichten und Antworten handelt.</span><span class="sxs-lookup"><span data-stu-id="29d38-135">The **ulOrder** member indicates both directional order and categorization information, for example, by conversation ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)), that is, conversational thread, which is a series of messages and replies.</span></span> <span data-ttu-id="29d38-136">Zeilen können entweder in aufsteigender oder absteigender Reihenfolge sortiert werden, und alle NULL-Einträge werden zuletzt positioniert.</span><span class="sxs-lookup"><span data-stu-id="29d38-136">Rows can be sorted in either an ascending or descending sequence with all NULL entries positioned last.</span></span> 
  
<span data-ttu-id="29d38-137">Der TABLE_SORT_COMBINE gibt an, dass die in **ulPropTag** angegebene Spalte mit der vorherigen Kategoriespalte kombiniert werden soll, um eine zusammengesetzte Kategorie zu bilden.</span><span class="sxs-lookup"><span data-stu-id="29d38-137">The TABLE_SORT_COMBINE value indicates that the column specified in **ulPropTag** should be combined with the previous category column to form a composite category.</span></span> <span data-ttu-id="29d38-138">Das heißt, anstatt eindeutige Werte einzelner Spalten zu kategorisieren, TABLE_SORT_COMBINE die Kategorisierung für eindeutige Werte einer Spaltenkombination möglich.</span><span class="sxs-lookup"><span data-stu-id="29d38-138">That is, instead of categorizing on unique values of individual columns, TABLE_SORT_COMBINE allows for categorization on unique values of a combination of columns.</span></span> <span data-ttu-id="29d38-139">Beispielsweise kann eine einzelne Kategorie definiert werden, um Nachrichten zu gruppieren, die von einem bestimmten Absender eines bestimmten Betreffs empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="29d38-139">For example, a single category could be defined to group messages received from a particular sender on a particular subject.</span></span> <span data-ttu-id="29d38-140">Wenn Sie den Wert auf TABLE_SORT_COMBINE reduziert sich die Anzahl der angezeigten Kategoriezeilen.</span><span class="sxs-lookup"><span data-stu-id="29d38-140">Setting the value to TABLE_SORT_COMBINE reduces the number of category rows that are displayed.</span></span> 
  
<span data-ttu-id="29d38-141">Das Sortieren nach mehrwertigen Spalten wird nicht von allen Tabellenimplementierungen universell unterstützt.</span><span class="sxs-lookup"><span data-stu-id="29d38-141">Sorting on multi-valued columns is not universally supported by all table implementations.</span></span> <span data-ttu-id="29d38-142">Wenn unterstützt, wenden Sie das MV_FLAG mithilfe des makros MVI_PROP auf das Eigenschaftstag im **ulPropTag-Element** an, um den Sortierschlüssel als mehrwertige Spalte zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="29d38-142">If supported, apply the MV_FLAG using the MVI_PROP macro to the property tag in the **ulPropTag** member to identify the sort key as a multi-valued column.</span></span> <span data-ttu-id="29d38-143">Die Sortierung nach einer mehrwertigen Spalte basiert auf der Verwendung der einzelnen Werte.</span><span class="sxs-lookup"><span data-stu-id="29d38-143">Sorting on a multi-valued column is based on using the individual values.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="29d38-144">Die **ulOrder-Memberwerte** TABLE_SORT_CATEG_MAX und TABLE_SORT_CATEG_MIN sind möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben. In diesem Fall können Sie sie ihrem Code mithilfe der folgenden Werte hinzufügen: >  `#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`</span><span class="sxs-lookup"><span data-stu-id="29d38-144">The **ulOrder** member values TABLE_SORT_CATEG_MAX and TABLE_SORT_CATEG_MIN might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following values: >  `#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`</span></span>
  
<span data-ttu-id="29d38-145">Weitere Informationen zur standard- und kategorisierten Sortierung finden Sie unter [Sorting and Categorization](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="29d38-145">For more information about standard and categorized sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="29d38-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29d38-146">See also</span></span>

- [<span data-ttu-id="29d38-147">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="29d38-147">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="29d38-148">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="29d38-148">MAPI Structures</span></span>](mapi-structures.md)

