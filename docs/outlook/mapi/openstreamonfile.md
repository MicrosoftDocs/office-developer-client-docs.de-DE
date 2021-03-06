---
title: OpenStreamOnFile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenStreamOnFile
api_type:
- COM
ms.assetid: 01fa459f-597d-4b16-b340-a79fb270cd71
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b05f5b30eceb7df1bed76c64f4bdda87ede0e463
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439093"
---
# <a name="openstreamonfile"></a>OpenStreamOnFile

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Weist ein OLE **IStream-Objekt** zu und initialisiert es, um auf den Inhalt einer Datei zu zugreifen. Diese Funktion verwendet eine ANSI-Zeichenfolge als Dateinamen, einschließlich des Pfads und der Dateierweiterung. Daher wird die Verwendung der Unicode-Version dieser Funktion, [OpenStreamOnFileW](openstreamonfilew.md), empfohlen.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
HRESULT STDMETHODCALLTYPE OpenStreamOnFile(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  LPSTR lpszFileName,
  LPSTR lpszPrefix,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a>Parameter

 _lpAllocateBuffer_
  
> [in] Zeiger auf die [MAPIAllocateBuffer-Funktion,](mapiallocatebuffer.md) die zum Zuordnen von Arbeitsspeicher verwendet werden soll. 
    
 _lpFreeBuffer_
  
> [in] Zeiger auf die [MAPIFreeBuffer-Funktion,](mapifreebuffer.md) die zum Freispeichern verwendet werden soll. 
    
 _ulFlags_
  
> [in] Bitmaske von Flags, die zum Steuern des Erstellens oder Öffnens der Datei verwendet werden, auf die über das OLE **IStream-Objekt zugegriffen werden** soll. Die folgenden Kennzeichen können festgelegt werden: 
    
SOF_UNIQUEFILENAME 
  
> Für das **IStream-Objekt** soll eine temporäre Datei erstellt werden. Wenn dieses Flag festgelegt ist, sollten auch die STGM_CREATE und STGM_READWRITE festgelegt werden. 
    
STGM_CREATE 
  
> Die Datei soll auch dann erstellt werden, wenn bereits eine vorhanden ist. Wenn der  _lpszFileName-Parameter_ nicht festgelegt ist, müssen sowohl dieses Flag als auch STGM_DELETEONRELEASE festgelegt werden. Wenn STGM_CREATE festgelegt ist, muss auch das STGM_READWRITE festgelegt werden. 
    
STGM_DELETEONRELEASE 
  
> Die Datei soll gelöscht werden, wenn das **IStream-Objekt** freigegeben wird. Wenn der  _lpszFileName-Parameter_ nicht festgelegt ist, müssen sowohl dieses Flag als auch STGM_CREATE festgelegt werden. 
    
STGM_READ 
  
> Die Datei soll mit schreibgeschützten Zugriff erstellt oder geöffnet werden. 
    
STGM_READWRITE 
  
> Die Datei soll mit Lese-/Schreibberechtigung erstellt oder geöffnet werden. Wenn dieses Flag nicht festgelegt ist, darf STGM_CREATE auch nicht festgelegt werden. 
    
 _lpszFileName_
  
> [in] Der Dateiname einschließlich Pfad und Erweiterung der Datei, für die **OpenStreamOnFile** das **IStream-Objekt initialisiert.** Wenn das SOF_UNIQUEFILENAME festgelegt ist, enthält  _lpszFileName_ den Pfad zum Verzeichnis, in dem eine temporäre Datei erstellt werden soll. Wenn  _lpszFileName_ null ist, **ruft OpenStreamOnFile** einen entsprechenden Pfad vom System ab, und sowohl die STGM_CREATE als auch STGM_DELETEONRELEASE müssen festgelegt werden. 
    
 _lpszPrefix_
  
> [in] Das Präfix für den Dateinamen, für den **OpenStreamOnFile** das **IStream-Objekt initialisiert.** Wenn festgelegt, darf das Präfix nicht mehr als drei Zeichen enthalten. Wenn  _lpszPrefix_ NULL ist, wird das Präfix "SOF" verwendet. 
    
 _lppStream_
  
> [out] Zeiger auf einen Zeiger auf ein Objekt, das die **IStream-Schnittstelle verfügbar** machen soll. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_NO_ACCESS 
  
> Der Zugriff auf die Datei konnte aufgrund unzureichender Benutzerberechtigungen oder aufgrund von schreibgeschützten Dateien nicht möglich sein. 
    
MAPI_E_NOT_FOUND 
  
> Die festgelegte Datei ist nicht vorhanden.
    
## <a name="remarks"></a>Hinweise

Die **OpenStreamOnFile-Funktion** verfügt über zwei wichtige Verwendungsmöglichkeiten, die sich durch die Einstellung des SOF_UNIQUEFILENAME unterscheiden. Wenn dieses Flag nicht festgelegt ist, öffnet **OpenStreamOnFile** ein **IStream-Objekt** in einer vorhandenen Datei, z. B. um dessen Inhalt in die **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md))-Eigenschaft einer Anlage mit der **IStream::CopyTo-Methode** zu kopieren. In diesem Fall gibt  _der lpszFileName-Parameter_ den Pfad und Dateinamen der Datei an. 
  
Wenn SOF_UNIQUEFILENAME festgelegt ist, erstellt **OpenStreamOnFile** eine temporäre Datei zum Speichern von Daten für ein **IStream-Objekt.** Für diese Verwendung kann der  _lpszFileName-Parameter_ optional den Pfad zum Verzeichnis festlegen, in dem die Datei erstellt werden soll, und der  _lpszPrefix-Parameter_ kann optional ein Präfix für den Dateinamen angeben. 
  
Wenn die aufrufende Clientanwendung oder der aufrufende Dienstanbieter mit dem **IStream-Objekt** fertig ist, sollte es durch Aufrufen der OLE **IStream::Release-Methode freigegeben** werden. 
  
MAPI verwendet die Funktionen, auf die  _von lpAllocateBuffer_ und  _lpFreeBuffer_ verwiesen wird, für die meisten Speicherzuweisungen und Deallocation, insbesondere zum Zuordnen von Arbeitsspeicher zur Verwendung durch Clientanwendungen beim Aufrufen von Objektschnittstellen wie [IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPITable::QueryRows](imapitable-queryrows.md). 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Das SOF_UNIQUEFILENAME wird verwendet, um eine temporäre Datei mit einem für das Messagingsystem eindeutigen Namen zu erstellen. Wenn dieses Flag festgelegt ist, gibt der  _lpszFileName-Parameter_ den Pfad für die temporäre Datei an, und der  _lpszPrefix-Parameter_ enthält die Präfixzeichen des Dateinamens. Der konstruierte Dateiname ist <prefix> HHHH. TMP, wobei HHHH eine Hexadezimalzahl ist. Wenn _lpszFileName_ NULL ist, wird die Datei im temporären Dateiverzeichnis erstellt, das von der Windows-Funktion **GetTempPath** oder dem aktuellen Verzeichnis zurückgegeben wird, wenn kein temporäres Dateiverzeichnis festgelegt wurde. 
  
Wenn das SOF_UNIQUEFILENAME nicht festgelegt ist,  _wird lpszPrefix_ ignoriert, und  _lpszFileName_ sollte den vollqualifizierten Pfad und Dateinamen der datei enthalten, die geöffnet oder erstellt werden soll. Die Datei wird basierend auf den anderen Flags geöffnet oder erstellt, die in _ulFlags festgelegt sind._ 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|File.cpp  <br/> |WriteAttachStreamToFile  <br/> |MFCMAPI verwendet die **OpenStreamOnFile-Methode,** um einen Datenstrom in einer Datei zu öffnen, damit eine Anlage darauf geschrieben werden kann.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

