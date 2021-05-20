---
title: IProviderAdmin IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin
api_type:
- COM
ms.assetid: bdb4cdca-8dfd-4f90-9467-ec31cea3f518
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: bedec72e8371d0e8aa69415d2f0dc77b4c62ff76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437532"
---
# <a name="iprovideradmin--iunknown"></a>IProviderAdmin : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Funktioniert mit Dienstanbietern in einem Nachrichtendienst. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Anbieterverwaltungsobjekte  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IProviderAdmin  <br/> |
|Zeigertyp:  <br/> |LPPROVIDERADMIN  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[GetLastError](iprovideradmin-getlasterror.md) <br/> |Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Fehler enthält, der für das Anbieterverwaltungsobjekt aufgetreten ist.  <br/> |
|[GetProviderTable](iprovideradmin-getprovidertable.md) <br/> |Bietet Zugriff auf die Anbietertabelle des Nachrichtendiensts, eine Liste der Dienstanbieter im Nachrichtendienst.  <br/> |
|[CreateProvider](iprovideradmin-createprovider.md) <br/> |Fügt dem Nachrichtendienst einen Dienstanbieter hinzu.  <br/> |
|[DeleteProvider](iprovideradmin-deleteprovider.md) <br/> |Löscht einen Dienstanbieter aus dem Nachrichtendienst.  <br/> |
|[OpenProfileSection](iprovideradmin-openprofilesection.md) <br/> |Öffnet einen Profilabschnitt aus dem aktuellen Profil und gibt einen [IProfSect-Zeiger](iprofsectimapiprop.md) für weiteren Zugriff zurück.  <br/> |
   
## <a name="remarks"></a>Hinweise

Clients können einen Zeiger auf eine **IProviderAdmin-Schnittstelle** durch Aufrufen der [IMsgServiceAdmin::AdminProviders-Methode](imsgserviceadmin-adminproviders.md) erhalten. Dienstanbietern wird ein **IProviderAdmin-Zeiger** übergeben, wenn die Einstiegspunktfunktion des Nachrichtendiensts aufgerufen wird. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

