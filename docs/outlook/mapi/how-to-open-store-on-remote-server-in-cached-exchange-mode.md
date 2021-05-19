---
title: Öffnen eines Speichers auf dem Remoteserver, Outlook sich im Cache-Exchange-Modus befindet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: cf01eab7-164d-c3b3-8bb0-9281e2119bc5
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: 419c9ae734e8b58d0958970e7127b94d220b8382
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417819"
---
# <a name="open-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a><span data-ttu-id="8f71b-103">Öffnen eines Speichers auf dem Remoteserver, Outlook sich im Cache-Exchange-Modus befindet</span><span class="sxs-lookup"><span data-stu-id="8f71b-103">Open a store on the remote server when Outlook is in Cached Exchange Mode</span></span>

<span data-ttu-id="8f71b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f71b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8f71b-105">Dieses Thema enthält ein Codebeispiel in C++, in dem gezeigt wird, wie Sie das **MDB_ONLINE-Flag** verwenden, um einen Nachrichtenspeicher auf dem Remoteserver zu öffnen, wenn Microsoft Outlook 2010 oder Microsoft Outlook 2013 sich im Cached Exchange Mode befindet.</span><span class="sxs-lookup"><span data-stu-id="8f71b-105">This topic contains a code sample in C++ that shows how to use the **MDB_ONLINE** flag to open a message store on the remote server when Microsoft Outlook 2010 or Microsoft Outlook 2013 is in Cached Exchange Mode.</span></span> 
  
<span data-ttu-id="8f71b-106">Im cached Exchange Mode können Outlook 2010 und Outlook 2013 eine lokale Kopie des Postfachs eines Benutzers verwenden, während Outlook 2010 oder Outlook 2013 eine Onlineverbindung zu einer Remotekopie des Postfachs des Benutzers auf dem Remoteserver des Exchange verwaltet.</span><span class="sxs-lookup"><span data-stu-id="8f71b-106">Cached Exchange Mode permits Outlook 2010 and Outlook 2013 to use a local copy of a user's mailbox while Outlook 2010 or Outlook 2013 maintains an online connection to a remote copy of the user's mailbox on the remote Exchange server.</span></span> <span data-ttu-id="8f71b-107">Wenn Outlook 2010 oder Outlook 2013 im Cached Exchange Mode ausgeführt wird, sind standardmäßig alle MAPI-Lösungen, die sich bei derselben Sitzung anmelden, auch mit dem zwischengespeicherten Nachrichtenspeicher verbunden.</span><span class="sxs-lookup"><span data-stu-id="8f71b-107">When Outlook 2010 or Outlook 2013 is running in Cached Exchange Mode, by default, any MAPI solutions that log on to the same session are also connected to the cached message store.</span></span> <span data-ttu-id="8f71b-108">Alle Daten, auf die zugegriffen wird, und alle vorgenommenen Änderungen werden für die lokale Kopie des Postfachs vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="8f71b-108">Any data that is accessed and any changes that are made are made against the local copy of the mailbox.</span></span>
  
<span data-ttu-id="8f71b-109">Ein **Client** oder Dienstanbieter kann die Verbindung zum lokalen Nachrichtenspeicher überschreiben und den Speicher auf dem Remoteserver öffnen, indem er das Bit für MDB_ONLINE im  *ulFlags-Parameter*  beim Aufrufen von [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)festlegen.</span><span class="sxs-lookup"><span data-stu-id="8f71b-109">A client or service provider can override the connection to the local message store and open the store on the remote server by setting the bit for **MDB_ONLINE** in the  *ulFlags*  parameter when calling [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).</span></span> <span data-ttu-id="8f71b-110">Nachdem der Speicher auf dem Remoteserver für diese Sitzung erfolgreich geöffnet wurde, können Sie [IMAPISession::OpenEntry](imapisession-openentry.md) verwenden, um Elemente oder Ordner im Remotespeicher zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8f71b-110">After the store has been successfully opened on the remote server for that session, you can use [IMAPISession::OpenEntry](imapisession-openentry.md) to open items or folders on the remote store.</span></span> 
  
<span data-ttu-id="8f71b-111">Sie können einen Exchange im Cachemodus und im nicht zwischengespeicherten Modus nicht gleichzeitig in derselben MAPI-Sitzung öffnen.</span><span class="sxs-lookup"><span data-stu-id="8f71b-111">You cannot open an Exchange store in cached mode and in non-cached mode at the same time in the same MAPI session.</span></span> <span data-ttu-id="8f71b-112">Wenn Sie den zwischengespeicherten Nachrichtenspeicher bereits geöffnet haben, müssen Sie entweder den Speicher schließen, bevor Sie ihn mit dieser Kennzeichnung öffnen, oder eine neue MAPI-Sitzung öffnen, in der Sie den Exchange-Speicher auf dem Remoteserver mit dieser Kennzeichnung öffnen können.</span><span class="sxs-lookup"><span data-stu-id="8f71b-112">If you have already opened the cached message store, you must either close the store before you open it with this flag, or open a new MAPI session where you can open the Exchange store on the remote server by using this flag.</span></span>
  
<span data-ttu-id="8f71b-113">Im folgenden Codebeispiel wird gezeigt, wie **Sie IMAPISession::OpenMsgStore** mit dem im *ulFlags-Parameter* festgelegten **MDB_ONLINE** aufrufen, um den Standardspeicher auf dem Remoteserver zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8f71b-113">The following code sample shows how to call **IMAPISession::OpenMsgStore** with the **MDB_ONLINE** flag set in the  *ulFlags*  parameter to open the default store on the remote server.</span></span> 
  
```cpp
HRESULT HrRemoteMessageStore( 
    LPMAPISESSION lpMAPISession, 
    LPMDB* lppMDB) 
{ 
    HRESULT hRes = S_OK; 
    LPMAPITABLE pStoresTbl = NULL; 
    SRestriction sres = {0}; 
    SPropValue spv = {0}; 
    LPSRowSet pRow = NULL; 
    LPMDB lpTempMDB = NULL; 
    enum {EID,NUM_COLS}; 
    static SizedSPropTagArray(NUM_COLS,sptCols) = {NUM_COLS, 
        PR_ENTRYID, 
    }; 
 
    //Obtain the table of all the message stores that are available 
    hRes = lpMAPISession-&gt;GetMsgStoresTable(0, &amp;pStoresTbl); 
     
    if (SUCCEEDED(hRes) &amp;&amp; pStoresTbl) 
    { 
        //Set up restrictions for the default store 
        sres.rt = RES_PROPERTY;                                  //Comparing a property 
        sres.res.resProperty.relop = RELOP_EQ;                   //Testing equality 
        sres.res.resProperty.ulPropTag = PR_DEFAULT_STORE;       //Tag to compare 
        sres.res.resProperty.lpProp = &amp;spv;                      //Prop tag and value to compare against 
     
        spv.ulPropTag = PR_DEFAULT_STORE;                        //Tag type 
        spv.Value.b   = TRUE;                                    //Tag value 
     
        //Convert the table to an array that can be stepped through 
        //Only one message store should have PR_DEFAULT_STORE set to true, so that only one will be returned 
        hRes = HrQueryAllRows( 
            pStoresTbl,                                          //Table to query 
            (LPSPropTagArray) &amp;sptCols,                          //Which columns to obtain 
            &amp;sres,                                               //Restriction to use 
            NULL,                                                //No sort order 
            0,                                                   //Max number of rows (0 means no limit) 
            &amp;pRow);                                              //Array to return 
 
        if (SUCCEEDED(hRes) &amp;&amp; pRow &amp;&amp; pRow-&gt;cRows) 
        {     
            //Open the first returned (default) message store 
            hRes = lpMAPISession-&gt;OpenMsgStore( 
                NULL,                                                //Window handle for dialogs 
                pRow-&gt;aRow[0].lpProps[EID].Value.bin.cb,             //size and... 
                (LPENTRYID)pRow-&gt;aRow[0].lpProps[EID].Value.bin.lpb, //value of entry to open 
                NULL,                                                //Use default interface (IMsgStore) to open store 
                MAPI_BEST_ACCESS | MDB_ONLINE,                       //Flags 
                &amp;lpTempMDB);                                         //Pointer to put the store in 
            if (SUCCEEDED(hRes) &amp;&amp; lppMDB) lppMDB* = lpTempMDB; 
        } 
    } 
    FreeProws(pRow); 
    if (pStoresTbl) pStoresTbl-&gt;Release(); 
 
    return hRes; 
}

```

## <a name="see-also"></a><span data-ttu-id="8f71b-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8f71b-114">See also</span></span>

- [<span data-ttu-id="8f71b-115">Informationen zu MAPI-Ergänzungen</span><span class="sxs-lookup"><span data-stu-id="8f71b-115">About MAPI Additions</span></span>](about-mapi-additions.md) 
- [<span data-ttu-id="8f71b-116">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="8f71b-116">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="8f71b-117">Zugreifen auf einen Speicher auf dem Remoteserver, wenn Outlook sich im Exchange-Cache-Modus befindet</span><span class="sxs-lookup"><span data-stu-id="8f71b-117">Access a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)

