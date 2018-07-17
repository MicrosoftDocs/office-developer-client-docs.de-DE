---
title: Zelle "Address" (Abschnitt "Hyperlinks")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251387
localization_priority: Normal
ms.assetid: 3864aadd-3f86-c20e-1a74-b0aaff5106f7
description: Legt eine aufzurufende URL-Adresse, einen Dateinamen oder einen UNC-Pfad fest.
ms.openlocfilehash: 840ce0c4ce73da378f80e5d8a185073ac3915daf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796403"
---
# <a name="address-cell-hyperlinks-section"></a><span data-ttu-id="4cd9a-103">Address Cell (Hyperlinks Section)</span><span class="sxs-lookup"><span data-stu-id="4cd9a-103">Address Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="4cd9a-104">Legt eine aufzurufende URL-Adresse, einen Dateinamen oder einen UNC-Pfad fest.</span><span class="sxs-lookup"><span data-stu-id="4cd9a-104">Specifies a URL address, file name, or UNC path to which to jump.</span></span>
  
<span data-ttu-id="4cd9a-105">Sie können eine Adresse angeben, wie ein relativer Pfad basierend auf der Basispfad für das Dokument in das Feld **Hyperlinkbasis** auf der Registerkarte **Zusammenfassung** des Dialogfelds **Eigenschaften** definiert (klicken Sie auf der Registerkarte **Datei** , klicken Sie auf **Info**, klicken Sie auf ** Eigenschaften ** und klicken Sie dann auf **Erweiterte Eigenschaften**).</span><span class="sxs-lookup"><span data-stu-id="4cd9a-105">You can specify Address as a relative path based on the base path defined for the document in the **Hyperlink base** box on the **Summary** tab of the **Properties** dialog box (click the **File** tab, click **Info**, click ** Properties **, and then click **Advanced Properties**).</span></span> <span data-ttu-id="4cd9a-106">Wenn das Dokument keinen Basispfad verfügt, navigiert die Anwendung basierend auf den Dokumentpfad.</span><span class="sxs-lookup"><span data-stu-id="4cd9a-106">If the document has no base path, the application navigates based on the document path.</span></span> <span data-ttu-id="4cd9a-107">Wenn das Dokument nicht gespeichert wurde, ist der Hyperlink nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="4cd9a-107">If the document has not been saved, the hyperlink is undefined.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4cd9a-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4cd9a-108">Remarks</span></span>

<span data-ttu-id="4cd9a-109">Sie können den Wert der Zelle Address auch im Dialogfeld **Hyperlinks** festlegen (klicken Sie auf der Registerkarte **Einfügen** auf **Hyperlink** ).</span><span class="sxs-lookup"><span data-stu-id="4cd9a-109">You can also set the value of the Address cell in the **Hyperlinks** dialog box (click **Hyperlink** on the **Insert** tab).</span></span> 
  
<span data-ttu-id="4cd9a-110">Wenn Sie einen Verweis auf die Zelle Address aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="4cd9a-110">To get a reference to the Address cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4cd9a-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="4cd9a-111">Cell name:</span></span>  <br/> |<span data-ttu-id="4cd9a-112">Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="4cd9a-112">Hyperlink.</span></span> <span data-ttu-id="4cd9a-113">*Name* . Beheben von Where Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="4cd9a-113">*name*  .Address           where Hyperlink.</span></span> <span data-ttu-id="4cd9a-114">*ist der Name der Hyperlinkzeile*</span><span class="sxs-lookup"><span data-stu-id="4cd9a-114">*name*  is the name of the hyperlink row</span></span>  <br/> |
   
<span data-ttu-id="4cd9a-115">Zum Abrufen eines Verweises auf die Zelle Address nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="4cd9a-115">To get a reference to the Address cell by name from another formula, or from a program, by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4cd9a-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="4cd9a-116">Section index:</span></span>  <br/> |<span data-ttu-id="4cd9a-117">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="4cd9a-117">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="4cd9a-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="4cd9a-118">Row index:</span></span>  <br/> |<span data-ttu-id="4cd9a-119">**visRow1stHyperlink** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="4cd9a-119">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="4cd9a-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="4cd9a-120">Cell index:</span></span>  <br/> |<span data-ttu-id="4cd9a-121">**visHLinkAddress**</span><span class="sxs-lookup"><span data-stu-id="4cd9a-121">**visHLinkAddress**</span></span> <br/> |
   
