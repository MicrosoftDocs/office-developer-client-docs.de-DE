---
title: WriteText-Methode (ADO)
TOCTitle: WriteText Method (ADO)
ms:assetid: 1ca2d9d5-11f4-d088-6fc3-53240208bb09
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248963(v=office.15)
ms:contentKeyID: 48543574
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 67dcf218814f938c4583ba9587085cff73066dc1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476049"
---
# <a name="writetext-method-ado"></a>WriteText-Methode (ADO)


**Betrifft**: Access 2013 | Office 2013

Schreibt eine angegebene Textzeichenfolge in ein [Stream](stream-object-ado.md)-Objekt.

## <a name="syntax"></a>Syntax

*Stream-Objekt*. WriteText*Daten*, *Optionen*

## <a name="parameters"></a>Parameter

  - *Data*

  - Ein Wert vom Datentyp **String**, der die Textzeichenfolge enthält, die geschrieben werden soll.

  - *Options*

  - Optional. Ein [StreamWriteEnum](streamwriteenum.md)-Wert, der angibt, ob am Ende der angegebenen Zeichenfolge ein Zeilentrennzeichen geschrieben werden muss.

## <a name="remarks"></a>Hinweise

Die angegebenen Zeichenfolgen werden ohne Leerzeichen oder Buchstaben zwischen den einzelnen Zeichenfolgen in das **Stream** -Objekt geschrieben.

Als aktuelle [Position](position-property-ado.md) wird der Buchstabe festgelegt, der auf die geschriebenen Daten folgt. Mit der **WriteText** -Methode werden die restlichen Daten in einem Datenstrom nicht abgeschnitten. Wenn Sie diese Buchstaben abschneiden möchten, rufen Sie [SetEOS](seteos-method-ado.md) auf.

Wenn Sie nach der aktuellen [EOS](eos-property-ado.md)-Position abschneiden, wird [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) für **Stream** um neue Buchstaben erhöht, und **EOS** wird auf das neue letzte Byte in **Stream** verschoben.


> [!NOTE]
> <P>Die <STRONG>WriteText</STRONG>-Methode wird für Textdatenströme verwendet (<A href="type-property-ado-stream.md">Type</A> ist <STRONG>adTypeText</STRONG>). Für binäre Datenströme (<STRONG>Type</STRONG> ist <STRONG>adTypeBinary</STRONG>) verwenden Sie <A href="write-method-ado.md">Write</A>.</P>

