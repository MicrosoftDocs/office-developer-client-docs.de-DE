---
title: State-Eigenschaft (ADO)
TOCTitle: State Property (ADO)
ms:assetid: ade0a50c-e2d8-23ac-4ea9-b012fedcd5db
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249819(v=office.15)
ms:contentKeyID: 48547053
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231176
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2bde03f1d6c7619e8140248b2551002f0453fc9a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475908"
---
# <a name="state-property-ado"></a>State-Eigenschaft (ADO)


**Betrifft**: Access 2013 | Office 2013

Gibt für alle entsprechenden Objekte an, ob deren Status als geöffnet oder geschlossen gilt.

Gibt für alle entsprechenden Objekte, die eine asynchrone Methode ausführen, den aktuellen Status des Objekts an: Verbindungsherstellung (connecting), Ausführen (executing) oder Abrufen (retrieving).

## <a name="return-value"></a>Rückgabewert

Gibt einen **Long** -Wert zurück, bei dem es sich um einen [ObjectStateEnum](objectstateenum.md)-Wert handeln kann. Der Standardwert ist **adStateClosed**.

## <a name="remarks"></a>Hinweise

Mit der **State** -Eigenschaft können Sie jederzeit den aktuellen Status eines bestimmten Objekts ermitteln.

Die **State** -Eigenschaft des Objekts kann kombinierte Werte besitzen. Wenn beispielsweise eine Anweisung ausgeführt wird, besitzt die Eigenschaft einen aus **adStateOpen** und **adStateExecuting** bestehenden kombinierten Wert.

Die **State** -Eigenschaft ist schreibgeschützt.
