---
title: Erstellen eines Kontaktelements aus einer vCard-Datei und Speichern des Elements in einem Ordner
TOCTitle: Create a Contact item from a vCard file and save the item in a folder
ms:assetid: b207b584-ffcf-4ac5-ab1f-4f91d43000e1
ms:mtpsurl: https://msdn.microsoft.com/library/Bb646856(v=office.15)
ms:contentKeyID: 55119826
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3a048d090c946ff5a86fddf4b1ac8c6818e061b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321259"
---
# <a name="create-a-contact-item-from-a-vcard-file-and-save-the-item-in-a-folder"></a>Erstellen eines Kontaktelements aus einer vCard-Datei und Speichern des Elements in einem Ordner

In diesem Beispiel werden alle vCard-Dateien aus einem Dateisystemordner importiert und die Kontakte im durch den *targetFolder*-Parameter angegebenen Ordner gespeichert.

## <a name="example"></a>Beispiel

In dem Beispiel wird die [OpenSharedItem](https://msdn.microsoft.com/library/bb645399\(v=office.15\))-Methode verwendet. Die **OpenSharedItem**-Methode öffnet Nachrichten, die als Dateien im Outlook-Nachrichtenformat (MSG), iCalendar-Termindateien (ICS) oder vCard-Dateien (VCF) gespeichert sind. Vergessen Sie nicht, das zurückgegebene Objekt in den entsprechenden Elementtyp umzuwandeln und die entsprechende **Save**-Methode aufzurufen, um das Element dauerhaft zu speichern. Standardmäßig wird das von **OpenSharedItem** zurückgegebene Element im Standardordner für den jeweiligen Elementtyp gespeichert. Sie können das Element mit der entsprechenden **Move**-Methode in einen anderen Ordner verschieben.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die Anweisung **Imports** oder **using** darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgenden Codezeilen zeigen, wie Sie den Import und die Zuweisung in Visual Basic und C\# vornehmen.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub ImportContacts( _
    ByVal path As String, ByVal targetFolder As Outlook.Folder)
    Dim contact As Outlook.ContactItem
    Dim moveContact As Outlook.ContactItem
    If (Directory.Exists(path)) Then
        Dim files As String() = Directory.GetFiles(path, "*.vcf")
        For Each file As String In files
            contact = CType(Application.Session.OpenSharedItem(file), _
                Outlook.ContactItem)
            If (targetFolder Is _
                CType(Application.Session.GetDefaultFolder( _
                    Outlook.OlDefaultFolders.olFolderContacts) _
                    , Outlook.Folder)) Then
                contact.Save()
            Else
                moveContact = CType(contact.Move(targetFolder), _
                    Outlook.ContactItem)
                moveContact.Save()
            End If
        Next
    End If
End Sub
```


```csharp
private void ImportContacts(string path, Outlook.Folder targetFolder)
{
    Outlook.ContactItem contact;
    Outlook.ContactItem moveContact;
    if (Directory.Exists(path))
    {
        string[] files = Directory.GetFiles(path, "*.vcf");
        foreach (string file in files)
        {
            contact = Application.Session.OpenSharedItem(file)
                as Outlook.ContactItem;
            if (targetFolder ==
                Application.Session.GetDefaultFolder(
                Outlook.OlDefaultFolders.olFolderContacts)
                as Outlook.Folder)
            {
                contact.Save();
            }
            else
            {
                moveContact = contact.Move(targetFolder)
                    as Outlook.ContactItem;
                moveContact.Save();
            }
        }
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Kontakte](contacts.md)

