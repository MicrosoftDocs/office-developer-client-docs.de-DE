---
title: Informationen zur ShapeSheet-Kalkulationstabelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251822
localization_priority: Normal
ms.assetid: f403890d-4a3a-bacc-53d7-1b9920b23639
description: Jedem Objekt in Microsoft Visio (Dokument, Zeichenblatt, Formatvorlage, Shape, Gruppe, Shape oder Objekt in einer Gruppe, Master-Shape, Objekt aus einem anderen Programm, Führungslinie und Führungspunkt) ist eine ShapeSheet-Kalkulationstabelle zugeordnet, in der wichtige objektspezifische Informationen aufgeführt sind. Diese Kalkulationstabelle enthält Informationen wie Höhe, Breite, Winkel, Farbe sowie andere Attribute, die das Erscheinungsbild und das Verhalten des Shapes definieren.
ms.openlocfilehash: f443a596174ac4a555d53a271372e73367197da0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796359"
---
# <a name="about-the-shapesheet-spreadsheet"></a><span data-ttu-id="b7dff-104">Informationen zur ShapeSheet-Kalkulationstabelle</span><span class="sxs-lookup"><span data-stu-id="b7dff-104">About the ShapeSheet Spreadsheet</span></span>

<span data-ttu-id="b7dff-p102">Jedem Objekt in Microsoft Visio (Dokument, Zeichenblatt, Formatvorlage, Shape, Gruppe, Shape oder Objekt in einer Gruppe, Master-Shape, Objekt aus einem anderen Programm, Führungslinie und Führungspunkt) ist eine ShapeSheet-Kalkulationstabelle zugeordnet, in der wichtige objektspezifische Informationen aufgeführt sind. Diese Kalkulationstabelle enthält Informationen wie Höhe, Breite, Winkel, Farbe sowie andere Attribute, die das Erscheinungsbild und das Verhalten des Shapes definieren.</span><span class="sxs-lookup"><span data-stu-id="b7dff-p102">Everything in Microsoft Visio, every document, page, style, shape, group, shape or object within a group, master, object from another program, guide, and guide point, has a ShapeSheet spreadsheet where information about that object is stored. This spreadsheet contains information such as height, width, angle, color, and other attributes that determine the shape's appearance and behavior.</span></span>
  
<span data-ttu-id="b7dff-p103">Als Shape-Entwickler müssen Sie das Erscheinungsbild und Verhalten der von Ihnen erstellten Shapes ohne Einschränkungen und genauestens steuern können. Sie können das Standardverhalten eines Shapes ändern sowie seine Funktionalität erweitern, indem Sie es über seine ShapeSheet-Kalkulationstabelle bearbeiten. Auf diese Tabelle können Sie in einem ShapeSheet-Fenster oder programmgesteuert zugreifen.</span><span class="sxs-lookup"><span data-stu-id="b7dff-p103">As a shape developer, you need precise control over the appearance and behavior of the shapes you create. You can change a shape's default behavior and enhance what it can do by editing it in its ShapeSheet, which you can access in a ShapeSheet window or programmatically.</span></span>
  
## <a name="viewing-an-object-in-a-shapesheet-window"></a><span data-ttu-id="b7dff-109">Anzeigen eines Objekts in einem ShapeSheet-Fenster</span><span class="sxs-lookup"><span data-stu-id="b7dff-109">Viewing an object in a ShapeSheet window</span></span>

<span data-ttu-id="b7dff-110">Das Visio-Zeichnungsfenster und das ShapeSheet-Fenster stellen verschiedene Ansichten desselben Shapes dar.</span><span class="sxs-lookup"><span data-stu-id="b7dff-110">The Visio drawing window and ShapeSheet window are simply different views of the same shape.</span></span>
  
- <span data-ttu-id="b7dff-111">Wenn Sie ein Shape in einem Zeichnungsfenster anzeigen, wird es grafisch gerendert angezeigt. Darüber hinaus verhält es sich gemäß den Formeln, die in seiner ShapeSheet-Kalkulationstabelle definiert sind.</span><span class="sxs-lookup"><span data-stu-id="b7dff-111">When you view a shape in a drawing window, you see it rendered graphically and behaving according to the formulas in its ShapeSheet.</span></span>
    
- <span data-ttu-id="b7dff-112">Wenn Sie ein Shape in einem ShapeSheet-Fenster anzeigen, sehen Sie die zugrunde liegenden Formeln, die bestimmen, wie das Shape auf dem Zeichenblatt angezeigt wird und wie es sich verhält.</span><span class="sxs-lookup"><span data-stu-id="b7dff-112">When you view a shape in a ShapeSheet window, you see the underlying formulas that determine how it looks and behaves on the drawing page.</span></span>
    
<span data-ttu-id="b7dff-p104">Sie können ein ShapeSheet-Fenster und ein Zeichnungsfenster gleichzeitig anzeigen und sehen, wie das Shape im Zeichnungsfenster geändert wird, während Sie Zellen im entsprechenden ShapeSheet-Fenster ändern bzw. umgekehrt. Wenn Sie das Shape beispielsweise mit dem Mauszeiger verschieben, ändern sich die Formeln für PinX und PinY im Abschnitt Shape Transform, um die neue Position des Shapes auf dem Zeichenblatt anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b7dff-p104">You can view a ShapeSheet window and a drawing window simultaneously and see the shape change in the drawing window as you manipulate cells in its ShapeSheet window or vice versa. For example, when you move the shape with the pointer, the shape's PinX and PinY formulas in the Shape Transform section change to reflect its new position on the drawing page.</span></span>
  
## <a name="structure-of-the-shapesheet-window"></a><span data-ttu-id="b7dff-115">Struktur des ShapeSheet-Fensters</span><span class="sxs-lookup"><span data-stu-id="b7dff-115">Structure of the ShapeSheet window</span></span>

<span data-ttu-id="b7dff-116">Ein ShapeSheet ist unterteilt in *Abschnitte* , die einen bestimmten Aspekt der Verhalten eines Shapes oder die Darstellungsweise, steuern beispielsweise Geometrie oder Formatierung.</span><span class="sxs-lookup"><span data-stu-id="b7dff-116">A ShapeSheet is divided into  *sections*  that control a particular aspect of a shape's behavior or appearance, for example, its geometry or its formatting.</span></span> <span data-ttu-id="b7dff-117">Jeder Abschnitt enthält eine oder mehrere *Zeilen* , die *Zellen* enthalten.</span><span class="sxs-lookup"><span data-stu-id="b7dff-117">Each section contains one or more  *rows*  that contain  *cells*  .</span></span> <span data-ttu-id="b7dff-118">Jede Zelle kann eine Formel, dessen Ergebnis (häufig als der Wert der Zelle bezeichnet) und optionale Fehlerinformationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="b7dff-118">Each cell can contain a formula, its result (commonly called the cell value), and optional error information.</span></span> <span data-ttu-id="b7dff-119">Eine Formel, die möglicherweise erforderlich oder optional, je nach der jeweiligen Zelle.</span><span class="sxs-lookup"><span data-stu-id="b7dff-119">A formula may be required or optional, depending on the particular cell.</span></span> <span data-ttu-id="b7dff-120">Eine Zelle Daten (beispielsweise die Formel oder Wert) können lokal definiert oder häufiger aus der entsprechenden Zelle in der Form Master oder einer Formatvorlage geerbt.</span><span class="sxs-lookup"><span data-stu-id="b7dff-120">A cell's data (for example, its formula or value) may be locally defined or, more often, inherited from the equivalent cell in the shape's master or style.</span></span> 
  
<span data-ttu-id="b7dff-121">Im folgenden Beispiel werden die Formelleiste</span><span class="sxs-lookup"><span data-stu-id="b7dff-121">The following example shows the formula bar</span></span> ![Nummer 1](media/callout1_ZA01036259.gif)<span data-ttu-id="b7dff-123">, ein Abschnitt</span><span class="sxs-lookup"><span data-stu-id="b7dff-123">, a section</span></span> ![Nummer 2](media/callout2_ZA01036260.gif)<span data-ttu-id="b7dff-125">, eine Zelle</span><span class="sxs-lookup"><span data-stu-id="b7dff-125">, a cell</span></span> ![Nummer 3](media/callout3_ZA01036261.gif)<span data-ttu-id="b7dff-127">und eine Zeile</span><span class="sxs-lookup"><span data-stu-id="b7dff-127">, and a row</span></span> ![Nummer 4](media/callout4_ZA01036262.gif) <span data-ttu-id="b7dff-129">im ShapeSheet-Fenster veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="b7dff-129">in the ShapeSheet window.</span></span> 
  
![](media/ShpSheetRef_CA_02a_ZA07645861.gif)
  
<span data-ttu-id="b7dff-130">Wenn Sie ein Shape zeichnen, zeichnet Visio das Shape als eine Auflistung der horizontalen und vertikalen Speicherorte mit Liniensegmenten verbunden.</span><span class="sxs-lookup"><span data-stu-id="b7dff-130">When you draw a shape, Visio records the shape as a collection of horizontal and vertical locations connected with line segments.</span></span> <span data-ttu-id="b7dff-131">Diese Positionen (auch Scheitelpunkte genannt) werden in die Zellen X und Y die Shape- **Geometrie** -Abschnitt gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b7dff-131">These locations (called vertices) are recorded in the X and Y cells of the shape's **Geometry** section.</span></span> <span data-ttu-id="b7dff-132">Wie im folgenden Beispiel angezeigt, wenn Sie die Zellen X und Y im Abschnitt **Geometry** des ShapeSheet-Fenster für ein Shape klicken, wird ein Schwarz versehen Feld Hervorhebung des Scheitelpunkts auf dem Shape im Zeichnungsfenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b7dff-132">As shown in the following example, when you click the X and Y cells in the **Geometry** section of a shape's ShapeSheet window, you will see a black-bordered box highlighting the vertex on the shape in the drawing window.</span></span> 
  
![](media/ShpSheetRef_CA_01_ZA07645860.gif)
  
## <a name="editing-an-object-in-the-shapesheet-window"></a><span data-ttu-id="b7dff-133">Bearbeiten eines Objekts im ShapeSheet-Fenster</span><span class="sxs-lookup"><span data-stu-id="b7dff-133">Editing an object in the ShapeSheet window</span></span>

<span data-ttu-id="b7dff-p107">Wenn ein ShapeSheet-Fenster aktiv ist, ändert sich das Menüband entsprechend, um Optionen für das Arbeiten in diesem Fenster anzuzeigen. Wenn Sie eine ShapeSheet-Zelle auswählen, wird eine Formelleiste angezeigt, die Sie verwenden können, um die Formeln eines Objekts einzugeben oder zu ändern. Sie können aber auch direkt in der Zelle arbeiten.</span><span class="sxs-lookup"><span data-stu-id="b7dff-p107">When a ShapeSheet window is active, the ribbon changes to display options specific to working in this window. When you select a ShapeSheet cell, a formula bar appears, which you can use to enter and edit an object's formulas. Or, you can work directly in the cell.</span></span>
  
<span data-ttu-id="b7dff-137">In einem ShapeSheet-Fenster können Sie die Abschnitte zu einer Form hinzu, um die neue Eigenschaften mit dem Shape auf dem Zeichenblatt hinzufügen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b7dff-137">In a ShapeSheet window, you can add sections to a shape's sheet to add new characteristics to the shape on the drawing page.</span></span> <span data-ttu-id="b7dff-138">Beispielsweise können Sie einen Abschnitt **Connection Points** zum Erstellen einer Verbindung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b7dff-138">For example, you can add a **Connection Points** section to create a connection.</span></span> <span data-ttu-id="b7dff-139">Wenn Sie einen Abschnitt nicht mehr benötigen, können Sie ihn löschen.</span><span class="sxs-lookup"><span data-stu-id="b7dff-139">When you no longer need a section, you can delete it.</span></span> 
  
<span data-ttu-id="b7dff-140">Sie können Zeilen auch Abschnitten zusätzliche Formeln zu speichern oder zum Ändern der Darstellung eines Shapes hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b7dff-140">You also can add rows to sections to hold additional formulas or to change a shape's appearance.</span></span> <span data-ttu-id="b7dff-141">Beispielsweise können Sie eine Zeile zu einem **Geometrie** -Abschnitt ein Segment mit einer Form hinzufügen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b7dff-141">For example, you can add a row to a **Geometry** section to add a segment to a shape.</span></span> <span data-ttu-id="b7dff-142">In ähnlicher Weise können Sie Zeilen löschen, die Sie nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="b7dff-142">Similarly, you can delete rows you no longer need.</span></span> 
  
<span data-ttu-id="b7dff-p110">Sie können in Zellen entweder Formeln oder Werte anzeigen. Zeigen Sie Formeln an, wenn Sie neue Formeln eingeben, vorhandene Formeln ändern oder überprüfen möchten, in welcher Beziehung Formeln in verschiedenen Zellen zueinander stehen. Ein Wert ist das Ergebnis, das Sie erhalten, wenn Visio die Formel in einer Zelle berechnet. Sie können die Werte in den Zellen anzeigen, um die Ergebnisse der Berechnungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b7dff-p110">You can display either formulas or values in cells. Display formulas when you are entering new formulas, editing existing formulas, or to see how formulas in cells relate to each other. A value is the result you get when Visio evaluates a cell's formula. You can display values in cells to see the result of an evaluation.</span></span>
  
## <a name="additional-shapesheet-references"></a><span data-ttu-id="b7dff-147">Weitere Informationen zu ShapeSheets</span><span class="sxs-lookup"><span data-stu-id="b7dff-147">Additional ShapeSheet references</span></span>

<span data-ttu-id="b7dff-148">Details zu einer bestimmten Abschnitt, eine Zeile oder eine Zelle im ShapeSheet finden Sie entsprechenden Artikel in dieser [ShapeSheet-Referenz](reference-visio-shapesheet.md).</span><span class="sxs-lookup"><span data-stu-id="b7dff-148">For details on a particular section, row, or cell in the ShapeSheet, view the corresponding article in this [ShapeSheet Reference](reference-visio-shapesheet.md).</span></span>
  
<span data-ttu-id="b7dff-149">Einzelheiten zum programmgesteuerten Zugriff auf die ShapeSheet-Kalkulationstabelle finden Sie in der Microsoft Visio Automation Reference.</span><span class="sxs-lookup"><span data-stu-id="b7dff-149">For details on programmatically accessing the ShapeSheet spreadsheet, see the Microsoft Visio Automation Reference.</span></span>
  
