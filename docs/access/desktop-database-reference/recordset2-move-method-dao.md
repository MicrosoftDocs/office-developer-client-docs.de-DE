---
title: Recordset2. Move-Methode (DAO)
TOCTitle: Move Method
ms:assetid: df39c05e-c5f8-3b66-fa5f-c91b687c147d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835635(v=office.15)
ms:contentKeyID: 48548211
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d57e73c52ca515f13d613ed3aeb9cf361054396e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307266"
---
# <a name="recordset2move-method-dao"></a>Recordset2. Move-Methode (DAO)

**Gilt für**: Access 2013, Office 2013

Verschiebt die Position des aktuellen Datensatzes in ein **[Recordset](recordset-object-dao.md)** -Objekt.

## <a name="syntax"></a>Syntax

*Ausdruck* . Move (***Rows***, ***Start Bookmark***)

*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.

## <a name="parameters"></a>Parameter

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Erforderlich/optional</p></th>
<th><p>Datentyp</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Rows</em></p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Die Anzahl von Zeilen, um die sich die Position verschiebt. Ist rows größer als 0, wird die Position nach vorne verschoben (Richtung Dateiende). Ist rows kleiner als 0, wird die Position nach hinten verschoben (Richtung Dateianfang).</p></td>
</tr>
<tr class="even">
<td><p><em>Start Bookmark</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Ein Wert, der ein Lesezeichen identifiziert. Bei Angabe von startbookmark beginnt die Verschiebung relativ zu diesem Lesezeichen. Andernfalls beginnt Move mit dem aktuellen Datensatz.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Wenn Sie mithilfe von **Move** den aktuellen Datensatzzeiger vor dem ersten Datensatz positionieren, wird der aktuelle Datensatzzeiger an den Dateianfang verschoben. Falls das **Recordset** keine Datensätze enthält und seine **[BOF](recordset2-bof-property-dao.md)** -Eigenschaft auf **True** festgelegt ist, wird ein Fehler zurückgegeben, wenn Sie sich mit dieser Methode rückwärts bewegen.

Wenn Sie mithilfe von **Move** den aktuellen Datensatzzeiger hinter dem letzten Datensatz positionieren, wird der aktuelle Datensatzzeiger an das Dateiende verschoben. Falls das **Recordset** keine Datensätze enthält und seine **[EOF](recordset2-eof-property-dao.md)** -Eigenschaft auf **True** festgelegt ist, wird ein Fehler zurückgegeben, wenn Sie sich mit dieser Methode vorwärts bewegen.

Wenn für die **BOF**- oder die **EOF**-Eigenschaft der Wert **True** festgelegt ist und Sie versuchen, die **Move**-Methode ohne ein zulässiges Lesezeichen zu verwenden, tritt ein Laufzeitfehler auf.

> [!NOTE]
> - When you use **Move** on a forward-only-type **Recordset** object, the rows argument must be a positive integer and bookmarks aren't allowed. This means you can only move forward.
> - Verwenden Sie eine der Methoden **MoveFirst**, **MoveLast**, **MoveNext** oder **MovePrevious**, um den ersten, letzten, nächsten oder vorherigen Datensatz in einem **Recordset** zum aktuellen Datensatz zu machen.
> - Das Verwenden von **Move** mit einer Zeilenanzahl gleich 0 ist eine einfache Möglichkeit, die zugrunde liegenden Daten für den aktuellen Datensatz abzurufen. Das ist hilfreich, wenn Sie sicherstellen möchten, dass der aktuelle Datensatz die aktuellsten Daten aus den Basistabellen enthält. Außerdem werden alle anstehenden **[Edit](recordset2-edit-method-dao.md)** - oder **[AddNew](recordset-addnew-method-dao.md)** -Aufrufe abgebrochen.


## <a name="example"></a>Beispiel

In diesem Beispiel wird die **Move**-Methode verwendet, um den Zeiger für den Datensatz auf der Grundlage der Benutzereingabe zu positionieren.

```vb
    Sub MoveX() 
     
       Dim dbsNorthwind As Database 
       Dim rstSuppliers As Recordset2 
       Dim varBookmark As Variant 
       Dim strCommand As String 
       Dim lngMove As Long 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstSuppliers = _ 
          dbsNorthwind.OpenRecordset("SELECT CompanyName, " & _ 
          "City, Country FROM Suppliers ORDER BY CompanyName", _ 
          dbOpenDynaset) 
     
       With rstSuppliers 
          ' Populate recordset. 
          .MoveLast 
          .MoveFirst 
     
          Do While True 
             ' Display information about current record and ask  
             ' how many records to move. 
             strCommand = InputBox( _ 
                "Record " & (.AbsolutePosition + 1) & " of " & _ 
                .RecordCount & vbCr & "Company: " & _ 
                !CompanyName & vbCr & "Location: " & !City & _ 
                ", " & !Country & vbCr & vbCr & _ 
                "Enter number of records to Move " & _ 
                "(positive or negative).") 
     
             If strCommand = "" Then Exit Do 
     
             ' Store bookmark in case the Move doesn't work. 
             varBookmark = .Bookmark 
     
             ' Move method requires parameter of data type Long. 
             lngMove = CLng(strCommand) 
             .Move lngMove 
     
             ' Trap for BOF or EOF. 
             If .BOF Then 
                MsgBox "Too far backward! " & _ 
                   "Returning to current record." 
                .Bookmark = varBookmark 
             End If 
             If .EOF Then 
                MsgBox "Too far forward! " & _ 
                   "Returning to current record." 
                .Bookmark = varBookmark 
             End If 
          Loop 
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```
