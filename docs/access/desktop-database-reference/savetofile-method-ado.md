---
title: SaveToFile-Methode (ADO)
TOCTitle: SaveToFile method (ADO)
ms:assetid: db0fd95e-8ef3-af87-5346-8f8713153ca7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250104(v=office.15)
ms:contentKeyID: 48548097
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f3b08c9df435c7ce995a40af7b8ad5466b79245d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308925"
---
# <a name="savetofile-method-ado"></a>SaveToFile-Methode (ADO)

**Gilt für**: Access 2013, Office 2013

Speichert den binären Inhalt eines [Stream](stream-object-ado.md)-Objekts in eine Datei.

## <a name="syntax"></a>Syntax

*Stream*. SaveToFile*filename*, *SaveOptions*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*FileName* |Ein **String** -Wert, der den vollqualifiziertern Namen der Datei enthält, in die der Inhalt des **Stream** -Objekts gespeichert wird. Sie können einen gültigen lokalen Speicherort oder einen Speicherort, auf den Sie über einen UNC-Wert zugreifen können, angeben.|
|*SaveOptions* |Ein [SaveOptionsEnum](saveoptionsenum.md)-Wert, der angibt, ob eine neue Datei mithilfe von **SaveToFile** erstellt werden soll, falls diese nicht bereits vorhanden ist. Der Standardwert lautet **adSaveCreateNotExists**. Mit diesen Optionen können Sie angeben, dass ein Fehler auftritt, falls die angegebene Datei nicht vorhanden ist. Sie können auch angeben, dass **SaveToFile** den aktuellen Inhalt einer vorhandenen Datei überschreibt.|

> [!NOTE]
> [!HINWEIS] Wenn Sie eine vorhandene Datei überschreiben (wenn **adSaveCreateOverwrite** festgelegt ist), ignoriert **SaveToFile** alle Bytes aus der vorhandenen ursprünglichen Datei, die dem neuen [EOS](eos-property-ado.md) folgen.

## <a name="remarks"></a>Bemerkungen

**SaveToFile** kann verwendet werden, um den Inhalt eines **Stream** -Objekts in eine lokale Datei zu speichern. Es werden keine Änderungen am Inhalt oder den Eigenschaften des **Stream** -Objekts vorgenommen. Das **Stream** -Objekt muss vor dem Aufrufen von **SaveToFile** geöffnet werden.

Diese Methode ändert die Zuordnung des **Stream** -Objekts zu dessen zugrunde liegender Quelle nicht. Das **Stream** -Objekt bleibt der ursprünglichen URL oder dem ursprünglichen **Record** -Objekt zugeordnet, die bzw. das beim Öffnen dessen Quelle darstellte.

Nach einem **SaveToFile**-Vorgang wird die aktuelle Position ([Position](position-property-ado.md)) im Datenstrom auf den Anfang des Datenstroms festgelegt (0).

