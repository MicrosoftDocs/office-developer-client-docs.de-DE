---
title: Recordset2. reQuery-Methode (DAO)
TOCTitle: Requery Method
ms:assetid: d063c1e0-2fb7-b5cf-4d98-6f77a5a13cec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834712(v=office.15)
ms:contentKeyID: 48547837
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052940
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 44f573d179c26677fc801dac82e0deecc3874fb1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307210"
---
# <a name="recordset2requery-method-dao"></a>Recordset2. reQuery-Methode (DAO)

**Gilt für**: Access 2013, Office 2013

Die Daten in einem **[Recordset](recordset-object-dao.md)** -Objekt werden aktualisiert durch erneutes Ausführen der Abfrage, auf der das Objekt basiert.

## <a name="syntax"></a>Syntax

*Ausdruck* . ReQuery (***NewQueryDef***)

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
<td><p><em>NewQueryDef</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Stellt den <strong>Name</strong> -Eigenschaftenwert eines <strong><a href="querydef-object-dao.md">QueryDef</a></strong> -Objekts dar</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Methode, um sicherzustellen, dass ein **Recordset** die neuesten Daten enthält. Diese Methode füllt das aktuelle  **Recordset** neu aus, indem sie entweder die aktuellen Abfrageparameter oder (in einem Microsoft Access-Arbeitsbereich) die vom newquerydef-Argument neu bereitgestgellten verwendet.

Wenn Sie kein newquerydef-Argument angeben haben, wird das **Recordset** basierend auf der gleichen Abfragedefinition und den gleichen Parametern neu ausgefüllt, die ursprünglich zum Ausfüllen des **Recordset** verwendet wurden. Änderungen der zugrunde liegenden Daten werden während des erneuten Ausfüllens berücksichtigt. Wenn Sie keine **QueryDef** zum Erstellen des **Recordset** verwendet haben, wird das **Recordset** komplett neu erstellt.

Wenn Sie das ursprüngliche **QueryDef** -Objekt im newquerydef-Argument angeben, wird das **Recordset** mithilfe der vom **QueryDef**-Objekt angegebenen Parameter erneut abgefragt. Änderungen der zugrunde liegenden Daten werden während des erneuten Ausfüllens übernommen. Um Änderungen der Abfrageparameterwerte im **Recordset** zu übernehmen, müssen Sie das newquerydef-Argument angeben.

Wenn Sie eine andere **QueryDef** als die angeben, die ursprünglich zum Erstellen des **Recordset** verwendet wurde, wird das **Recordset** komplett neu erstellt.

Wenn Sie **Requery** verwenden, wird der erste Datensatz im **Recordset** der aktuelle Datensatz.

You can't use the **Requery** method on dynaset- or snapshot-type **Recordset** objects whose **[Restartable](recordset2-restartable-property-dao.md)** property is set to **False**. Wenn Sie jedoch das optionale newquerydef-Argument angeben, wird **** die Restartable-Eigenschaft ignoriert.

Ist für die beiden Eigenschafteneinstellungen **[BOF](recordset2-bof-property-dao.md)** und **[EOF](recordset2-eof-property-dao.md)** des **Recordset**-Objekts nach dem Verwenden der **Requery**-Methode **True** festgelegt, hat die Abfrage keine Datensätze zurückgegeben, und das **Recordset** enthält keine Daten.

## <a name="example"></a>Beispiel

Dieses Beispiel zeigt, wie die **Requery**-Methode zum Aktualisieren einer Abfrage verwendet werden kann, nachdem die zugrunde liegenden Daten geändert wurden.

```vb
    Sub RequeryX() 
     
     Dim dbsNorthwind As Database 
     Dim qdfTemp As QueryDef 
     Dim rstView As Recordset2 
     Dim rstChange As Recordset2 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set qdfTemp = dbsNorthwind.CreateQueryDef("", _ 
     "PARAMETERS ViewCountry Text; " & _ 
     "SELECT FirstName, LastName, Country FROM " & _ 
     "Employees WHERE Country = [ViewCountry] " & _ 
     "ORDER BY LastName") 
     
     qdfTemp.Parameters!ViewCountry = "USA" 
     Debug.Print "Data after initial query, " & _ 
     [ViewCountry] = USA" 
     Set rstView = qdfTemp.OpenRecordset 
     Do While Not rstView.EOF 
     Debug.Print " " & rstView!FirstName & " " & _ 
     rstView!LastName & ", " & rstView!Country 
     rstView.MoveNext 
     Loop 
     
     ' Change underlying data. 
     Set rstChange = dbsNorthwind.OpenRecordset("Employees") 
     rstChange.AddNew 
     rstChange!FirstName = "Nina" 
     rstChange!LastName = "Roberts" 
     rstChange!Country = "USA" 
     rstChange.Update 
     
     rstView.Requery 
     Debug.Print "Requery after changing underlying data" 
     Set rstView = qdfTemp.OpenRecordset 
     Do While Not rstView.EOF 
     Debug.Print " " & rstView!FirstName & " " & _ 
     rstView!LastName & ", " & rstView!Country 
     rstView.MoveNext 
     Loop 
     
     ' Restore original data because this is only a 
     ' demonstration. 
     rstChange.Bookmark = rstChange.LastModified 
     rstChange.Delete 
     rstChange.Close 
     
     rstView.Close 
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

Dieses Beispiel zeigt, wie die **Requery**-Methode zum Aktualisieren einer Abfrage verwendet werden kann, nachdem die Abfrageparamter geändert wurden.

```vb
Sub RequeryX2() 
 
 Dim dbsNorthwind As Database 
 Dim qdfTemp As QueryDef 
 Dim prmCountry As Parameter 
 Dim rstView As Recordset2 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 Set qdfTemp = dbsNorthwind.CreateQueryDef("", _ 
 "PARAMETERS ViewCountry Text; " & _ 
 "SELECT FirstName, LastName, Country FROM " & _ 
 "Employees WHERE Country = [ViewCountry] " & _ 
 "ORDER BY LastName") 
 Set prmCountry = qdfTemp.Parameters!ViewCountry 
 
 qdfTemp.Parameters!ViewCountry = "USA" 
 Debug.Print "Data after initial query, " & _ 
 [ViewCountry] = USA" 
 Set rstView = qdfTemp.OpenRecordset 
 Do While Not rstView.EOF 
 Debug.Print " " & rstView!FirstName & " " & _ 
 rstView!LastName & ", " & rstView!Country 
 rstView.MoveNext 
 Loop 
 
 ' Change query parameter. 
 qdfTemp.Parameters!ViewCountry = "UK" 
 ' QueryDef argument must be included so that the 
 ' resulting Recordset reflects the change in the query 
 ' parameter. 
 rstView.Requery qdfTemp 
 Debug.Print "Requery after changing parameter, " & _ 
 "[ViewCountry] = UK" 
 Do While Not rstView.EOF 
 Debug.Print " " & rstView!FirstName & " " & _ 
 rstView!LastName & ", " & rstView!Country 
 rstView.MoveNext 
 Loop 
 
 rstView.Close 
 dbsNorthwind.Close 
 
End Sub 
 
```

