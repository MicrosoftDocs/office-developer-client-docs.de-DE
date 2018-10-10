---
title: Error-Objekt - Datenzugriff Objekte (DAO)
TOCTitle: Error Object
ms:assetid: e2608bc9-bece-9b47-4562-7a2689601f75
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835711(v=office.15)
ms:contentKeyID: 48548289
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 62b195907d5acc05832c1feac45165aadd9e14d1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473960"
---
# <a name="error-object-dao"></a>Error Object (DAO)


**Betrifft**: Access 2013 | Office 2013

Das **Error**-Objekt enthält Details zu Datenzugriffsfehlern. Dabei bezieht sich jeder Fehler auf eine einzelne Operation, an der DAO beteiligt ist.

## <a name="remarks"></a>Bemerkungen

Jede Operation, an der DAO beteiligt ist, kann mindestens einen Fehler generieren. Beispielsweise kann ein Aufruf an einen ODBC-Server zu einem Fehler des Datenbankservers, einem Fehler von ODBC und einem DAO-Fehler führen. Sobald einer dieser Fehler auftritt, wird ein **Error**-Objekt in die **Errors**-Auflistung des **DBEngine**-Objekts aufgenommen. Ein einzelnes Ereignis kann somit mehrere **Error**-Objekte ergeben, die in der **Errors**-Auflistung anzeigt werden.

Generiert eine anschließende DAO-Operation einen Fehler, wird die **Errors**-Auflistung gelöscht, und die neuen **Error**-Objekte werden in die **Errors**-Auflistung aufgenommen. DAO-Operationen, die keinen Fehler generieren, wirken sich nicht auf die **Errors**-Auflistung aus.

Die Gruppe der **Error**-Objekte in der **Errors**-Auflistung beschreibt einen Fehler. Das erste **Error**-Objekt ist der Fehler der niedrigsten Ebene (der verursachende Fehler), das zweite Objekt ist der Fehler der nächsten Ebene usw. Tritt z. B. ein ODBC-Fehler beim Öffnen eines **[Recordset](recordset-object-dao.md)** -Objekts auf, enthält das erste **Error**-Objekt, **Errors**(0), den ODBC-Fehler der niedrigsten Ebene; die folgenden Fehler enthalten ODBC-Fehler, die von den verschiedenen ODBC-Schichten zurückgegeben werden. In diesem Fall geben der ODBC-Treibermanager und möglicherweise direkt der Treiber gesonderte **Error**-Objekte zurück. Das letzte **Error**-Objekt, **Errors.Count-** 1, enthält den DAO-Fehler mit dem Hinweis, dass das Objekt nicht geöffnet werden konnte.

Das Auflisten der speziellen Fehler in der **Errors**-Auflistung ermöglicht den Fehlerbehandlungsroutinen eine präzisere Ermittlung der Fehlerursache und das Durchführen der richtigen Schritte zur Wiederherstellung. Sie können die Eigenschaften des **Error**-Objekts lesen, um die folgenden Details zu den einzelnen Fehlern zu erhalten:

  - Die **[Description](error-description-property-dao.md)** -Eigenschaft mit dem Text der Fehlermeldung, die beim Abfangen des Fehlers auf dem Bildschirm angezeigt wird.

  - Die **[Anzahl](error-number-property-dao.md)** -Eigenschaft, die den Long Integer-Wert der Fehlerkonstante enthält.

  - Die **[Source](error-source-property-dao.md)** -Eigenschaft, die das Objekt identifiziert, das den Fehler verursacht hat. Das ist besonders nützlich, wenn sich nach einem Aufruf der ODBC-Datenquelle mehrere **Error**-Objekte in der **Errors**-Auflistung befinden.

  - Die Eigenschaften **HelpFile** und **HelpContext**, die jeweils die betreffende Microsoft Windows-Hilfedatei und das Hilfethema (sofern vorhanden) zu dem Fehler angeben.
    

    > [!NOTE]
    > <P>Wenn in Microsoft Visual Basic für Applikationen (VBA) programmieren, wenn Sie das <STRONG>New</STRONG> -Schlüsselwort verwenden, um ein Objekt zu erstellen, die anschließend, tritt ein Fehler vor hat dieses Objekt einer Auflistung, das <STRONG>DBEngine</STRONG> -Objekt <STRONG>Fehler</STRONG> angefügt wurden Auflistung enthalten keinen Eintrag für dieses Objekt Fehler; sein, da das neue Objekt nicht das <STRONG>DBEngine</STRONG> -Objekt zugeordnet ist. Die Fehlerinformationen sind jedoch im VBA-Objekt <STRONG>Err</STRONG> verfügbar. Der VBA-Code für die Fehlerbehandlung sollten die <STRONG>Errors</STRONG> -Auflistung untersuchen, wenn Sie einen Fehler beim Datenzugriff erwarten. Wenn Sie einen zentralen Fehlerhandler schreiben, testen Sie die VBA <STRONG>Err</STRONG> -Objekts, um festzustellen, ob die Fehlerinformationen in der <STRONG>Errors</STRONG> -Auflistung gültig ist. Wenn die <STRONG>Number</STRONG> -Eigenschaft des letzten Elements der <STRONG>Errors</STRONG> -Auflistung (DBEngine.Errors.Count - 1) und der Wert der Übereinstimmung <STRONG>Err</STRONG> -Objekt, anschließend können Sie eine Reihe von <STRONG>Select Case</STRONG> -Anweisung zum Identifizieren des bestimmten DAO-Fehlers oder aufgetretenen Fehler. Wenn sie nicht übereinstimmen, verwenden Sie die <STRONG><A href="errors-refresh-method-dao.md">Refresh</A></STRONG> -Methode auf die <STRONG>Errors</STRONG> -Auflistung.</P>



## <a name="example"></a>Beispiel

Dieses Beispiel löst einen Fehler aus, fängt ihn auf und zeigt die Eigenschaften **Description**, **Number**, **Source**, **HelpContext** und **HelpFile** des resultierenden **Error**-Objekts an.

```vb 
Sub DescriptionX() 
 
   Dim dbsTest As Database 
 
   On Error GoTo ErrorHandler 
 
   ' Intentionally trigger an error. 
   Set dbsTest = OpenDatabase("NoDatabase") 
 
   Exit Sub 
 
ErrorHandler: 
   Dim strError As String 
   Dim errLoop As Error 
 
   ' Enumerate Errors collection and display properties of  
   ' each Error object. 
   For Each errLoop In Errors 
      With errLoop 
         strError = _ 
            "Error #" & .Number & vbCr 
         strError = strError & _ 
            "  " & .Description & vbCr 
         strError = strError & _ 
            "  (Source: " & .Source & ")" & vbCr 
         strError = strError & _ 
            "Press F1 to see topic " & .HelpContext & vbCr 
         strError = strError & _ 
            "  in the file " & .HelpFile & "." 
      End With 
      MsgBox strError 
   Next 
 
   Resume Next 
 
End Sub 
 
```
