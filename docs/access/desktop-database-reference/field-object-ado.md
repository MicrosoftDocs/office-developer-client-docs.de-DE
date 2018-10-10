---
title: Field-Objekt - ActiveX Data Objects (ADO)
TOCTitle: Field Object (ADO)
ms:assetid: 1dbd535e-48ad-a5c8-a1b2-6776c1e3e19d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248968(v=office.15)
ms:contentKeyID: 48543600
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 240cb821ec861d33f22d157207cd62a566b4013a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472672"
---
# <a name="field-object-ado"></a>Field-Objekt (ADO)


**Betrifft**: Access 2013 | Office 2013

Stellt Daten mit einem gemeinsamen Datentyp in einer Spalte dar.

## <a name="remarks"></a>Hinweise

Jedes **Field** -Objekt entspricht einer Spalte im [Recordset](recordset-object-ado.md)-Objekt. Mit der [Value](value-property-ado.md)-Eigenschaft von **Field** -Objekten können Sie Daten für den aktuellen Datensatz festlegen oder zurückgeben. Abhängig von der vom Anbieter unterstützten Funktionalität sind bestimmte Auflistungen, Methoden oder Eigenschaften eines **Field** -Objekts möglicherweise nicht verfügbar.

Die Auflistungen, Methoden und Eigenschaften eines **Field** -Objekts ermöglichen Folgendes:

  - Zurückgeben des Namens eines Felds mit der [Name](name-property-ado.md)-Eigenschaft.

  - Anzeigen oder Ändern der Daten im Feld mithilfe der **Value** -Eigenschaft. **Value** ist die Standardeigenschaft des **Field** -Objekts.

  - Zurückgeben der grundlegenden Merkmale eines Felds mithilfe der Eigenschaften [Type](type-property-ado.md), [Precision](precision-property-ado.md) und [NumericScale](numericscale-property-ado.md).

  - Zurückgeben der deklarierten Größe eines Felds mit der [DefinedSize](definedsize-property-ado.md)-Eigenschaft.

  - Zurückgeben der tatsächlichen Größe der Daten in einem bestimmten Feld mit der [ActualSize](actualsize-property-ado.md)-Eigenschaft.

  - Bestimmen der für ein bestimmtes Feld unterstützten Funktionalitätstypen mithilfe der [Attributes](attributes-property-ado.md)-Eigenschaft und der [Properties](properties-collection-ado.md)-Auflistung.

  - Bearbeiten der Daten von Feldern, die lange Binär- oder Zeichendaten enthalten, mit den Methoden [AppendChunk](appendchunk-method-ado.md) und [GetChunk](getchunk-method-ado.md).

  - Auflösen von Diskrepanzen in Feldwerten während der Batchaktualisierung mit den Eigenschaften [OriginalValue](originalvalue-property-ado.md) und [UnderlyingValue](underlyingvalue-property-ado.md), sofern der Anbieter Batchaktualisierungen unterstützt.

Alle Metadateneigenschaften (**Name**, **Type**, **DefinedSize**, **Precision** und **NumericScale**) sind vor dem Öffnen des **Recordset**-Objekts des **Field**-Objekts verfügbar. Für die dynamische Erstellung von Formularen ist es nützlich, diese Eigenschaften zu diesem Zeitpunkt festzulegen.
