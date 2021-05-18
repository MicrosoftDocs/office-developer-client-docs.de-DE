---
title: GUARD-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251435
localization_priority: Normal
ms.assetid: 6c85414c-9fb6-cdc5-f5b6-8eb13c9608af
description: Schützt Ausdruck vor Löschung und Änderung durch Aktionen im Zeichnungsfenster, z. B. Verschieben, Größenanpassung, Gruppieren oder Aufheben der Gruppierung von Shapes.
ms.openlocfilehash: 0bdfa023d53e739a970cab65b1dbd67bc1a44461
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408152"
---
# <a name="guard-function"></a><span data-ttu-id="b4537-103">GUARD Function</span><span class="sxs-lookup"><span data-stu-id="b4537-103">GUARD Function</span></span>

<span data-ttu-id="b4537-104">Schützt  *Ausdruck*  vor Löschung und Änderung durch Aktionen im Zeichnungsfenster, z. B. Verschieben, Größenanpassung, Gruppieren oder Aufheben der Gruppierung von Shapes.</span><span class="sxs-lookup"><span data-stu-id="b4537-104">Protects  *expression*  from deletion and change by actions performed in the drawing window, for example, moving, sizing, grouping, or ungrouping shapes.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b4537-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4537-105">Syntax</span></span>

<span data-ttu-id="b4537-106">GUARD(\*\* *Expression* \*\* )</span><span class="sxs-lookup"><span data-stu-id="b4537-106">GUARD(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b4537-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4537-107">Parameters</span></span>

|<span data-ttu-id="b4537-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="b4537-108">**Name**</span></span>|<span data-ttu-id="b4537-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="b4537-109">**Required/Optional**</span></span>|<span data-ttu-id="b4537-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="b4537-110">**Data Type**</span></span>|<span data-ttu-id="b4537-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b4537-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b4537-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="b4537-112">_expression_</span></span> <br/> |<span data-ttu-id="b4537-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="b4537-113">Required</span></span>  <br/> |<span data-ttu-id="b4537-114">**String**</span><span class="sxs-lookup"><span data-stu-id="b4537-114">**String**</span></span> <br/> |<span data-ttu-id="b4537-115">Eine Kombination aus Konstanten, Operatoren, Funktionen und Bezügen auf ShapeSheet-Zellen, die einen Wert ergeben.</span><span class="sxs-lookup"><span data-stu-id="b4537-115">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b4537-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b4537-116">Remarks</span></span>

<span data-ttu-id="b4537-117">Zu den Zellen, auf die sich die GUARD-Funktion am häufigsten auswirkt, zählen Breite, Höhe, DrehbezX und DrehbezY.</span><span class="sxs-lookup"><span data-stu-id="b4537-117">The cells most often affected by the GUARD function are Width, Height, PinX, and PinY.</span></span> 
  
<span data-ttu-id="b4537-p101">Durch Schützen einer Zellformel verhindern Sie, dass der Wert dieser Zelle nicht durch im Zeichenfenster ausgeführte Aktionen verändert wird. Eine einzelne Aktion in dem Zeichenfenster kann sich jedoch auf mehrere Zellen auswirken. Jede dieser einzelnen Zellen muss geschützt werden, wenn Sie unerwartete Änderungen an der Darstellung eines Shapes verhindern möchten.</span><span class="sxs-lookup"><span data-stu-id="b4537-p101">Guarding a formula in any cell prevents that cell's value from being changed by actions in the drawing window. However, one action in the drawing window can affect several cells, and each of these cells must be guarded if you want to prevent unexpected changes to the shape's appearance.</span></span> 
  
## <a name="example"></a><span data-ttu-id="b4537-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b4537-120">Example</span></span>

<span data-ttu-id="b4537-121">GUARD(TEXTBREITE(DerText) + 0,5 in)</span><span class="sxs-lookup"><span data-stu-id="b4537-121">GUARD(TEXTWIDTH(TheText) + 0.5 in)</span></span> 
  
<span data-ttu-id="b4537-p102">Dieser Ausdruck in der Zelle Breite im Abschnitt Shape Transform eines Shapes verhindert, dass der Ausdruck (TEXTWIDTH(DerText) + 0,5 in) durch einen anderen Wert ersetzt wird, wenn die Breite des Shapes im Zeichnungsfenster geändert wird. Bei dem Text handelt es sich um eine Zelle, die bei Änderung der Textgestaltung des zugeordneten Shapes ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="b4537-p102">This expression in the Width cell of a shape's Shape Transform section prevents the expression (TEXTWIDTH(TheText) + 0.5 in) from being replaced with another value when the shape's width is changed in the drawing window. TheText is a cell that gets triggered when the associated shape's text composition changes.</span></span> 
  

