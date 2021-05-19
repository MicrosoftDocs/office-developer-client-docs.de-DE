---
title: Gewusst wie... (Outlook 2013 PIA-Referenz)
TOCTitle: How do I...
ms:assetid: ff647d52-bd32-4945-afa4-5b97d9a0d7dd
ms:mtpsurl: https://msdn.microsoft.com/library/Bb612741(v=office.15)
ms:contentKeyID: 55119792
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0bc4e19271e2747f5ffa8586b9f2ab226d6658b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355797"
---
# <a name="how-do-i-outlook-2013-pia-reference"></a><span data-ttu-id="07a4e-102">Gewusst wie... (Outlook 2013 PIA-Referenz)</span><span class="sxs-lookup"><span data-stu-id="07a4e-102">How do I... (Outlook 2013 PIA reference)</span></span>

<span data-ttu-id="07a4e-103">Dieser Abschnitt enthält Themen zu Vorgehensweisen und Codebeispiele in Visual Basic und C\#, die die Ausführung einiger allgemeiner Aufgaben in Outlook veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="07a4e-103">This section contains procedural tasks topics and code examples in Visual Basic and C\# that demonstrate how to perform some common tasks in Outlook.</span></span>

<span data-ttu-id="07a4e-104">Zum Ausführen dieser Codebeispiele müssen Outlook 2010 und Visual Studio 2008 oder eine höhere Version dieser Produkte installiert sein.</span><span class="sxs-lookup"><span data-stu-id="07a4e-104">To run these code examples, you must have installed Outlook 2010 and Visual Studio 2008, or a later version of these products.</span></span>

<span data-ttu-id="07a4e-105">Für die Codebeispiele in diesem Abschnitt müssen die Office Developer Tools für Visual Studio nicht installiert sein.</span><span class="sxs-lookup"><span data-stu-id="07a4e-105">The code examples in this section do not require that you have installed Office Developer Tools for Visual Studio.</span></span> <span data-ttu-id="07a4e-106">Im Portal für den [Einstieg in die Office-Entwicklung](https://developer.microsoft.com/office/docs) finden Sie Informationen zur Verwendung der Tools. Unter [Outlook-Lösungen](https://docs.microsoft.com/visualstudio/vsto/outlook-solutions?view=vs-2017) finden Sie grundlegende Anleitungen, die in verwaltetem Code geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="07a4e-106">However, you can refer to the [Getting started with Office development](https://developer.microsoft.com/office/docs) portal for information about using the tools, and refer to [Outlook solutions](https://docs.microsoft.com/visualstudio/vsto/outlook-solutions?view=vs-2017) for some basic how-to tasks written in managed code.</span></span>

<span data-ttu-id="07a4e-107">Die Codebeispiele in diesem Abschnitt reichen vom Anfänger- bis zum Fortgeschrittenenniveau, und einige basieren auf dem Buch [Programming Applications for Microsoft Office Outlook 2007 (Programmieren von Anwendungen für Microsoft Office Outlook 2007, in englischer Sprache)](https://www.amazon.com/gp/product/0735622493?ie=utf8%26tag=msmsdn-20%26linkcode=as2%26camp=1789%26creative=9325%26creativeasin=0735622493).</span><span class="sxs-lookup"><span data-stu-id="07a4e-107">Code examples in this section range from the beginner to the intermediate levels, and some of them are adapted from the book [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=utf8%26tag=msmsdn-20%26linkcode=as2%26camp=1789%26creative=9325%26creativeasin=0735622493).</span></span>

<span data-ttu-id="07a4e-108">Das für die Office-Entwicklerdokumentation zuständige Team freut sich über Ihre Vorstellungen zu Aufgaben und Codebeispiele.</span><span class="sxs-lookup"><span data-stu-id="07a4e-108">The Office Developer Documentation team welcomes your task ideas and code samples.</span></span> <span data-ttu-id="07a4e-109">Sollten wir Ihre Codebeispiele in Outlook-Inhalten verwenden, erkennen wir Ihre Arbeit mit einer Verfasserzeile und einem Link zu Ihrer Website an.</span><span class="sxs-lookup"><span data-stu-id="07a4e-109">If we use your code samples in Outlook content, we will recognize your work with a byline and a link to your website.</span></span> <span data-ttu-id="07a4e-110">Wenn Sie weitere Informationen wünschen, wenden Sie sich unter docthis@microsoft.com an uns.</span><span class="sxs-lookup"><span data-stu-id="07a4e-110">For more information, contact us at docthis@microsoft.com.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="07a4e-111">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="07a4e-111">In this section</span></span> 

[<span data-ttu-id="07a4e-112">Konten</span><span class="sxs-lookup"><span data-stu-id="07a4e-112">Accounts</span></span>](accounts.md)

- [<span data-ttu-id="07a4e-113">Abrufen von Kontoinformationen</span><span class="sxs-lookup"><span data-stu-id="07a4e-113">Get account information</span></span>](how-to-get-account-information.md)
- [<span data-ttu-id="07a4e-114">Erstellen eines sendbaren Elements für ein bestimmtes Konto auf der Basis des aktuellen Ordners</span><span class="sxs-lookup"><span data-stu-id="07a4e-114">Create a sendable item for a specific account based on the current folder</span></span>](how-to-create-a-sendable-item-for-a-specific-account-based-on-the-current-folder.md)
- [<span data-ttu-id="07a4e-115">Abrufen des Kontos für einen Ordner</span><span class="sxs-lookup"><span data-stu-id="07a4e-115">Get the account for a folder</span></span>](how-to-get-the-account-for-a-folder.md)
- [<span data-ttu-id="07a4e-116">Abrufen von Informationen über mehrere Konten</span><span class="sxs-lookup"><span data-stu-id="07a4e-116">Get information about multiple accounts</span></span>](how-to-get-information-about-multiple-accounts.md)
- [<span data-ttu-id="07a4e-117">Senden eines E-Mail-Elements mithilfe eines Hotmail-Kontos</span><span class="sxs-lookup"><span data-stu-id="07a4e-117">Send a mail item by using a Hotmail account</span></span>](how-to-send-a-mail-item-by-using-a-hotmail-account.md)

[<span data-ttu-id="07a4e-118">Add-In-Verwaltung</span><span class="sxs-lookup"><span data-stu-id="07a4e-118">Add-in administration</span></span>](add-in-administration.md)

- [<span data-ttu-id="07a4e-119">Bestimmen, ob Outlook eine Klick-und-Los-Anwendung auf einem Computer ist</span><span class="sxs-lookup"><span data-stu-id="07a4e-119">Determine whether Outlook is a Click-to-Run application on a computer</span></span>](how-to-determine-whether-outlook-is-a-click-to-run-application-on-a-computer.md)


[<span data-ttu-id="07a4e-120">Adressbuch</span><span class="sxs-lookup"><span data-stu-id="07a4e-120">Address book</span></span>](address-book.md)

- [<span data-ttu-id="07a4e-121">Anzeigen des Adressbuchs, das einem Ordner „Kontakte“ entspricht, im Dialogfeld „Namen auswählen“</span><span class="sxs-lookup"><span data-stu-id="07a4e-121">Display in the Select Names dialog box the address book corresponding to a Contacts folder</span></span>](how-to-display-in-the-select-names-dialog-box-the-address-book-corresponding-to-a-contacts-folder.md)
- [<span data-ttu-id="07a4e-122">Abrufen der globalen Adressliste oder eines Satzes von Adresslisten für einen Speicher</span><span class="sxs-lookup"><span data-stu-id="07a4e-122">Get the Global Address List or a set of address lists for a store</span></span>](how-to-get-the-global-address-list-or-a-set-of-address-lists-for-a-store.md)
- [<span data-ttu-id="07a4e-123">Aufzählen der Einträge in der globalen Adressliste</span><span class="sxs-lookup"><span data-stu-id="07a4e-123">Enumerate the entries in the Global Address List</span></span>](how-to-enumerate-the-entries-in-the-global-address-list.md)
- [<span data-ttu-id="07a4e-124">Anzeigen der Adresslisten für ein Profil</span><span class="sxs-lookup"><span data-stu-id="07a4e-124">Display the address lists for a profile</span></span>](how-to-display-the-address-lists-for-a-profile.md)

[<span data-ttu-id="07a4e-125">Termine</span><span class="sxs-lookup"><span data-stu-id="07a4e-125">Appointments</span></span>](appointments.md)

- [<span data-ttu-id="07a4e-126">Erstellen eines Termins, der ein ganztägiges Ereignis darstellt</span><span class="sxs-lookup"><span data-stu-id="07a4e-126">Create an appointment that is an all-day event</span></span>](how-to-create-an-appointment-that-is-an-all-day-event.md)
- [<span data-ttu-id="07a4e-127">Erstellen eines Termins mit Startzeit in der Pacific Time-Zone und Endzeit in der Eastern Time-Zone</span><span class="sxs-lookup"><span data-stu-id="07a4e-127">Create an appointment that starts in the Pacific Time Zone and ends in the Eastern Time Zone</span></span>](how-to-create-an-appointment-that-starts-in-the-pacific-time-zone-and-ends-in-the-eastern-time-zone.md)
- [<span data-ttu-id="07a4e-128">Angeben verschiedener Empfängertypen für ein Terminelement</span><span class="sxs-lookup"><span data-stu-id="07a4e-128">Specify different recipient types for an appointment item</span></span>](how-to-specify-different-recipient-types-for-an-appointment-item.md)
- [<span data-ttu-id="07a4e-129">Erstellen einer Terminserie mithilfe des Standardserienmusters</span><span class="sxs-lookup"><span data-stu-id="07a4e-129">Create a recurring appointment by using the default recurrence pattern</span></span>](how-to-create-a-recurring-appointment-by-using-the-default-recurrence-pattern.md)
- [<span data-ttu-id="07a4e-130">Erstellen einer Terminserie mit einem wöchentlichen Muster</span><span class="sxs-lookup"><span data-stu-id="07a4e-130">Create a recurring appointment that has a weekly pattern</span></span>](how-to-create-a-recurring-appointment-that-has-a-weekly-pattern.md)
- [<span data-ttu-id="07a4e-131">Erstellen einer jährlichen Terminserie mit einem YearNth-Muster</span><span class="sxs-lookup"><span data-stu-id="07a4e-131">Create an annual recurring appointment that uses a YearNth pattern</span></span>](how-to-create-an-annual-recurring-appointment-that-uses-a-yearnth-pattern.md)
- [<span data-ttu-id="07a4e-132">Suchen nach einem bestimmten Termin in einer Terminserie</span><span class="sxs-lookup"><span data-stu-id="07a4e-132">Find a specific appointment in a recurring appointment series</span></span>](how-to-find-a-specific-appointment-in-a-recurring-appointment-series.md)
- [<span data-ttu-id="07a4e-133">Erstellen eines Ausnahmetermins in einer Terminserie</span><span class="sxs-lookup"><span data-stu-id="07a4e-133">Create an exception appointment in a recurring appointment series</span></span>](how-to-create-an-exception-appointment-in-a-recurring-appointment-series.md)
- [<span data-ttu-id="07a4e-134">Erstellen einer Erinnerung für ein Terminelement</span><span class="sxs-lookup"><span data-stu-id="07a4e-134">Create a reminder for an appointment item</span></span>](how-to-create-a-reminder-for-an-appointment-item.md)
- [<span data-ttu-id="07a4e-135">Importieren von Termin-XML-Daten in Outlook-Terminobjekte</span><span class="sxs-lookup"><span data-stu-id="07a4e-135">Import appointment XML data into Outlook appointment objects</span></span>](how-to-import-appointment-xml-data-into-outlook-appointment-objects.md)

[<span data-ttu-id="07a4e-136">Anlagen</span><span class="sxs-lookup"><span data-stu-id="07a4e-136">Attachments</span></span>](attachments.md)

- [<span data-ttu-id="07a4e-137">Anhängen einer Datei an eine E-Mail-Nachricht</span><span class="sxs-lookup"><span data-stu-id="07a4e-137">Attach a file to a mail item</span></span>](https://docs.microsoft.com/office/vba/outlook/How-to/Items-Folders-and-Stores/attach-a-file-to-a-mail-item)
- [<span data-ttu-id="07a4e-138">Anfügen eines Outlook-Kontaktelements an eine E-Mail-Nachricht</span><span class="sxs-lookup"><span data-stu-id="07a4e-138">Attach an Outlook Contact item to an email message</span></span>](https://docs.microsoft.com/office/vba/outlook/Concepts/Attachments/attach-an-outlook-contact-item-to-an-email-message)
- [<span data-ttu-id="07a4e-139">Beschränken der Größe einer Anlage für eine Outlook-E-Mail-Nachricht</span><span class="sxs-lookup"><span data-stu-id="07a4e-139">Limit the size of an attachment to an Outlook email message</span></span>](https://docs.microsoft.com/office/vba/outlook/Concepts/Attachments/limit-the-size-of-an-attachment-to-an-outlook-email-message)
- [<span data-ttu-id="07a4e-140">Ändern einer Anlage einer Outlook-E-Mail</span><span class="sxs-lookup"><span data-stu-id="07a4e-140">Modify an attachment of an Outlook email message</span></span>](https://docs.microsoft.com/office/vba/outlook/concepts/attachments/modify-an-attachment-of-an-outlook-email-message)
- [<span data-ttu-id="07a4e-141">Programmgesteuertes Entfernen von Anlagen der Sicherheitsstufe 2 aus Nachrichten und Speichern der Anlagen auf einem Datenträger</span><span class="sxs-lookup"><span data-stu-id="07a4e-141">Programmatically remove security level 2 attachments from messages and save them to disk</span></span>](how-to-programmatically-remove-security-level-2-attachments-from-messages-and-save-them-to-disk.md)

[<span data-ttu-id="07a4e-142">Kalender</span><span class="sxs-lookup"><span data-stu-id="07a4e-142">Calendar</span></span>](calendar.md)

- [<span data-ttu-id="07a4e-143">Freigeben eines Frei-/Gebucht-Zeitplans innerhalb eines bestimmten Zeitraums in einem Kalender</span><span class="sxs-lookup"><span data-stu-id="07a4e-143">Share Free/Busy schedule within a specified period in a calendar</span></span>](how-to-share-free-busy-schedule-within-a-specified-period-in-a-calendar.md)
- [<span data-ttu-id="07a4e-144">Freigeben von Kalenderinformationen per E-Mail</span><span class="sxs-lookup"><span data-stu-id="07a4e-144">Share calendar information through email</span></span>](how-to-share-calendar-information-through-e-mail.md)
- [<span data-ttu-id="07a4e-145">Anzeigen eines freigegebenen Kalenders eines Empfängers</span><span class="sxs-lookup"><span data-stu-id="07a4e-145">Display a shared calendar of a recipient</span></span>](how-to-display-a-shared-calendar-of-a-recipient.md)
- [<span data-ttu-id="07a4e-146">Speichern eines Kalenders auf einem Datenträger</span><span class="sxs-lookup"><span data-stu-id="07a4e-146">Save a calendar to disk</span></span>](how-to-save-a-calendar-to-disk.md)
- [<span data-ttu-id="07a4e-147">Öffnen und Anzeigen des Inhalts einer iCalendar-Datei</span><span class="sxs-lookup"><span data-stu-id="07a4e-147">Open and display the contents of an iCalendar file</span></span>](how-to-open-and-display-the-contents-of-an-icalendar-file.md)

[<span data-ttu-id="07a4e-148">Farbkategorien</span><span class="sxs-lookup"><span data-stu-id="07a4e-148">Color categories</span></span>](color-categories.md)

- [<span data-ttu-id="07a4e-149">Aufzählen und Hinzufügen von Kategorien</span><span class="sxs-lookup"><span data-stu-id="07a4e-149">Enumerate and add categories</span></span>](how-to-enumerate-and-add-categories.md)
- [<span data-ttu-id="07a4e-150">Zuweisen von Kategorien zu einem Element</span><span class="sxs-lookup"><span data-stu-id="07a4e-150">Assign categories to an item</span></span>](how-to-assign-categories-to-an-item.md)

[<span data-ttu-id="07a4e-151">Kontakte</span><span class="sxs-lookup"><span data-stu-id="07a4e-151">Contacts</span></span>](contacts.md)

- [<span data-ttu-id="07a4e-152">Erstellen eines Kontaktelements</span><span class="sxs-lookup"><span data-stu-id="07a4e-152">Create a Contact item</span></span>](how-to-create-a-contact-item.md)
- [<span data-ttu-id="07a4e-153">Erstellen eines benutzerdefinierten Kontaktelements</span><span class="sxs-lookup"><span data-stu-id="07a4e-153">Create a custom Contact item</span></span>](how-to-create-a-custom-contact-item.md)
- [<span data-ttu-id="07a4e-154">Erstellen eines Kontaktelements aus einer vCard-Datei und Speichern des Elements in einem Ordner</span><span class="sxs-lookup"><span data-stu-id="07a4e-154">Create a Contact item from a vCard file and save the item in a folder</span></span>](how-to-create-a-contact-item-from-a-vcard-file-and-save-the-item-in-a-folder.md)

[<span data-ttu-id="07a4e-155">Unterhaltungen</span><span class="sxs-lookup"><span data-stu-id="07a4e-155">Conversations</span></span>](conversations.md)

- [<span data-ttu-id="07a4e-156">Abrufen und Anzeigen von Elementen in einer Unterhaltung</span><span class="sxs-lookup"><span data-stu-id="07a4e-156">Get and display items in a conversation</span></span>](how-to-get-and-display-items-in-a-conversation.md)
- [<span data-ttu-id="07a4e-157">Abrufen und Aufzählen von ausgewählten Unterhaltungen</span><span class="sxs-lookup"><span data-stu-id="07a4e-157">Get and enumerate selected conversations</span></span>](how-to-get-and-enumerate-selected-conversations.md)

[<span data-ttu-id="07a4e-158">Elektronische Visitenkarten</span><span class="sxs-lookup"><span data-stu-id="07a4e-158">Electronic business cards</span></span>](electronic-business-cards.md)

- [<span data-ttu-id="07a4e-159">Ändern des Layouts einer elektronischen Visitenkarte</span><span class="sxs-lookup"><span data-stu-id="07a4e-159">Modify the layout of an electronic business card</span></span>](how-to-modify-the-layout-of-an-electronic-business-card.md)
- [<span data-ttu-id="07a4e-160">Senden eines E-Mail-Elements mit einer elektronischen Visitenkarte</span><span class="sxs-lookup"><span data-stu-id="07a4e-160">Send a mail item with an electronic business card</span></span>](how-to-send-a-mail-item-with-an-electronic-business-card.md)

[<span data-ttu-id="07a4e-161">Exchange-Benutzer</span><span class="sxs-lookup"><span data-stu-id="07a4e-161">Exchange users</span></span>](exchange-users.md)

- [<span data-ttu-id="07a4e-162">Abrufen von Informationen über den aktuellen Benutzer</span><span class="sxs-lookup"><span data-stu-id="07a4e-162">Get information about the current user</span></span>](how-to-get-information-about-the-current-user.md)
- [<span data-ttu-id="07a4e-163">Abrufen von Informationen über alle Verteilerlisten, in denen der aktuelle Benutzer Mitglied ist</span><span class="sxs-lookup"><span data-stu-id="07a4e-163">Get information about all distribution lists of which the current user is a member</span></span>](how-to-get-information-about-all-distribution-lists-of-which-the-current-user-is-a-member.md)
- [<span data-ttu-id="07a4e-164">Erstellen einer Verteilerliste</span><span class="sxs-lookup"><span data-stu-id="07a4e-164">Create a distribution list</span></span>](how-to-create-a-distribution-list.md)
- [<span data-ttu-id="07a4e-165">Abrufen der Mitglieder einer Exchange-Verteilerliste</span><span class="sxs-lookup"><span data-stu-id="07a4e-165">Get members of an Exchange distribution list</span></span>](how-to-get-members-of-an-exchange-distribution-list.md)
- [<span data-ttu-id="07a4e-166">Abrufen von Informationen zum Vorgesetzten des aktuellen Benutzers</span><span class="sxs-lookup"><span data-stu-id="07a4e-166">Get information about the current user's manager</span></span>](how-to-get-information-about-the-current-user-s-manager.md)
- [<span data-ttu-id="07a4e-167">Abrufen von Verfügbarkeitsinformationen für den Vorgesetzten eines Exchange-Benutzers</span><span class="sxs-lookup"><span data-stu-id="07a4e-167">Get availability information for an Exchange user's manager</span></span>](how-to-get-availability-information-for-an-exchange-user-s-manager.md)
- [<span data-ttu-id="07a4e-168">Überprüfen der Antwort eines Vorgesetzten auf eine Besprechungsanfrage</span><span class="sxs-lookup"><span data-stu-id="07a4e-168">Check a manager's response to a meeting request</span></span>](how-to-check-a-manager-s-response-to-a-meeting-request.md)
- [<span data-ttu-id="07a4e-169">Abrufen von Informationen zu direkten Mitarbeitern des Vorgesetzten des aktuellen Benutzers</span><span class="sxs-lookup"><span data-stu-id="07a4e-169">Get information about direct reports of the current user's manager</span></span>](how-to-get-information-about-direct-reports-of-the-current-user-s-manager.md)

[<span data-ttu-id="07a4e-170">Ordner</span><span class="sxs-lookup"><span data-stu-id="07a4e-170">Folders</span></span>](folders.md)

- [<span data-ttu-id="07a4e-171">Hinzufügen eines Ordners zur Ordnerliste</span><span class="sxs-lookup"><span data-stu-id="07a4e-171">Add a folder to the folder list</span></span>](how-to-add-a-folder-to-the-folder-list.md)
- [<span data-ttu-id="07a4e-172">Aufzählen von Ordnern</span><span class="sxs-lookup"><span data-stu-id="07a4e-172">Enumerate folders</span></span>](how-to-enumerate-folders.md)
- [<span data-ttu-id="07a4e-173">Abrufen eines Standardordners und Auflisten seiner Unterordner</span><span class="sxs-lookup"><span data-stu-id="07a4e-173">Get a default folder and enumerate its subfolders</span></span>](how-to-get-a-default-folder-and-enumerate-its-subfolders.md)
- [<span data-ttu-id="07a4e-174">Abrufen eines Ordners basierend auf seinem Ordnerpfad</span><span class="sxs-lookup"><span data-stu-id="07a4e-174">Get a folder based on its folder path</span></span>](how-to-get-a-folder-based-on-its-folder-path.md)
- [<span data-ttu-id="07a4e-175">Auswählen eines Ordners und Anzeigen von Ordnerinformationen</span><span class="sxs-lookup"><span data-stu-id="07a4e-175">Select a folder and display folder information</span></span>](how-to-select-a-folder-and-display-folder-information.md)
- [<span data-ttu-id="07a4e-176">Abrufen der Standardnachrichtenklasse eines Ordners</span><span class="sxs-lookup"><span data-stu-id="07a4e-176">Get the default message class of a folder</span></span>](how-to-get-the-default-message-class-of-a-folder.md)
- [<span data-ttu-id="07a4e-177">Zugreifen auf lösungsspezifische Daten, die als ausgeblendete Nachricht in einem Ordner gespeichert sind</span><span class="sxs-lookup"><span data-stu-id="07a4e-177">Access solution-specific data stored as a hidden message in a folder</span></span>](how-to-access-solution-specific-data-stored-as-a-hidden-message-in-a-folder.md)
- [<span data-ttu-id="07a4e-178">Sicherstellen, dass benutzerdefinierte Elementeigenschaften in Abfragen auf Ordnerebene unterstützt werden</span><span class="sxs-lookup"><span data-stu-id="07a4e-178">Ensure that custom item properties are supported in folder-level queries</span></span>](how-to-ensure-that-custom-item-properties-are-supported-in-folder-level-queries.md)

[<span data-ttu-id="07a4e-179">Allgemeine Outlook-Elemente</span><span class="sxs-lookup"><span data-stu-id="07a4e-179">General Outlook items</span></span>](general-outlook-items.md)

- [<span data-ttu-id="07a4e-180">Erstellen einer Hilfsklasse zum Zugriff auf allgemeine Member von Outlook-Elementen</span><span class="sxs-lookup"><span data-stu-id="07a4e-180">Create a Helper class to access common Outlook item members</span></span>](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)
- [<span data-ttu-id="07a4e-181">Anzeigen von ausgewählten Elementen im aktiven Explorer</span><span class="sxs-lookup"><span data-stu-id="07a4e-181">Display selected items in the active Explorer</span></span>](how-to-display-selected-items-in-the-active-explorer.md)

[<span data-ttu-id="07a4e-182">Gruppenfreigabe</span><span class="sxs-lookup"><span data-stu-id="07a4e-182">Group sharing</span></span>](group-sharing.md)

- [<span data-ttu-id="07a4e-183">Abonnieren eines RSS-Feeds</span><span class="sxs-lookup"><span data-stu-id="07a4e-183">Subscribe to an RSS feed</span></span>](how-to-subscribe-to-an-rss-feed.md)
- [<span data-ttu-id="07a4e-184">Synchronisieren von Outlook mit einem SharePoint-Ordner</span><span class="sxs-lookup"><span data-stu-id="07a4e-184">Synchronize Outlook with a SharePoint folder</span></span>](how-to-synchronize-outlook-with-a-sharepoint-folder.md)

[<span data-ttu-id="07a4e-185">Mail</span><span class="sxs-lookup"><span data-stu-id="07a4e-185">Mail</span></span>](mail.md)

- [<span data-ttu-id="07a4e-186">Erstellen eines E-Mail-Elements mithilfe einer Nachrichtenvorlage</span><span class="sxs-lookup"><span data-stu-id="07a4e-186">Create a mail item by using a message template</span></span>](how-to-create-a-mail-item-by-using-a-message-template.md)
- [<span data-ttu-id="07a4e-187">Erstellen eines E-Mail-Elements, Anfügen eines Berichts und Senden des E-Mail-Elements an den Vorgesetzten des Benutzers</span><span class="sxs-lookup"><span data-stu-id="07a4e-187">Create a mail item, attach a report, and send the mail item to the user's manager</span></span>](how-to-create-a-mail-item-attach-a-report-and-send-the-mail-item-to-the-user-s-manager.md)
- [<span data-ttu-id="07a4e-188">Senden einer E-Mail-Nachricht mithilfe der SMTP-Adresse eines Kontos</span><span class="sxs-lookup"><span data-stu-id="07a4e-188">Send an email given the SMTP address of an account</span></span>](how-to-send-an-e-mail-given-the-smtp-address-of-an-account.md)
- [<span data-ttu-id="07a4e-189">Hinzufügen von Abstimmungsoptionen zu einem E-Mail-Element</span><span class="sxs-lookup"><span data-stu-id="07a4e-189">Add voting options to a mail item</span></span>](how-to-add-voting-options-to-a-mail-item.md)
- [<span data-ttu-id="07a4e-190">Hinzufügen einer benutzerdefinierten Aktion als Antwort auf ein E-Mail-Element</span><span class="sxs-lookup"><span data-stu-id="07a4e-190">Add a custom action as a response to a mail item</span></span>](how-to-add-a-custom-action-as-a-response-to-a-mail-item.md)
- [<span data-ttu-id="07a4e-191">Abrufen der SMTP-Adresse des Absenders eines E-Mail-Elements</span><span class="sxs-lookup"><span data-stu-id="07a4e-191">Get the SMTP address of the sender of a mail item</span></span>](how-to-get-the-smtp-address-of-the-sender-of-a-mail-item.md)
- [<span data-ttu-id="07a4e-192">Angeben verschiedener Empfängertypen für ein E-Mail-Element</span><span class="sxs-lookup"><span data-stu-id="07a4e-192">Specify different recipient types for a mail item</span></span>](how-to-specify-different-recipient-types-for-a-mail-item.md)

[<span data-ttu-id="07a4e-193">Besprechungsanfragen</span><span class="sxs-lookup"><span data-stu-id="07a4e-193">Meeting requests</span></span>](meeting-requests.md)

- [<span data-ttu-id="07a4e-194">Erstellen einer Besprechungsanfrage, Hinzufügen von Empfängern und Angeben eines Orts</span><span class="sxs-lookup"><span data-stu-id="07a4e-194">Create a meeting request, add recipients, and specify a location</span></span>](how-to-create-a-meeting-request-add-recipients-and-specify-a-location.md)
- [<span data-ttu-id="07a4e-195">Abrufen des Organisators einer Besprechung</span><span class="sxs-lookup"><span data-stu-id="07a4e-195">Get the organizer of a meeting</span></span>](how-to-get-the-organizer-of-a-meeting.md)
- [<span data-ttu-id="07a4e-196">Überprüfen aller Antworten auf eine Besprechungsanfrage</span><span class="sxs-lookup"><span data-stu-id="07a4e-196">Check all responses to a meeting request</span></span>](how-to-check-all-responses-to-a-meeting-request.md)
- [<span data-ttu-id="07a4e-197">Suchen des einer Besprechungsanfrage zugeordneten Terminelements</span><span class="sxs-lookup"><span data-stu-id="07a4e-197">Find the appointment item associated with a meeting request</span></span>](how-to-find-the-appointment-item-associated-with-a-meeting-request.md)
- [<span data-ttu-id="07a4e-198">Automatisches Annehmen einer Besprechungsanfrage</span><span class="sxs-lookup"><span data-stu-id="07a4e-198">Automatically accept a meeting request</span></span>](how-to-automatically-accept-a-meeting-request.md)
- [<span data-ttu-id="07a4e-199">Auffordern eines Benutzers zum Antworten auf eine Besprechungsanfrage</span><span class="sxs-lookup"><span data-stu-id="07a4e-199">Prompt a user to respond to a meeting request</span></span>](how-to-prompt-a-user-to-respond-to-a-meeting-request.md)

[<span data-ttu-id="07a4e-200">Empfänger</span><span class="sxs-lookup"><span data-stu-id="07a4e-200">Recipients</span></span>](recipients.md)

- [<span data-ttu-id="07a4e-201">Anzeigen des Dialogfelds „Namen auswählen“ zum Auflösen von Empfängern</span><span class="sxs-lookup"><span data-stu-id="07a4e-201">Display the Select Names dialog box to resolve recipients</span></span>](how-to-display-the-select-names-dialog-box-to-resolve-recipients.md)
- [<span data-ttu-id="07a4e-202">Verwenden des Dialogfelds „Namen auswählen“ zum Abrufen und Zuweisen von Empfängern zu einem Termin</span><span class="sxs-lookup"><span data-stu-id="07a4e-202">Use the Select Names dialog box to obtain and assign recipients to an appointment</span></span>](how-to-use-the-select-names-dialog-box-to-obtain-and-assign-recipients-to-an-appointment.md)
- [<span data-ttu-id="07a4e-203">Abrufen der E-Mail-Adresse eines Empfängers</span><span class="sxs-lookup"><span data-stu-id="07a4e-203">Get the email address of a recipient</span></span>](how-to-get-the-e-mail-address-of-a-recipient.md)

[<span data-ttu-id="07a4e-204">Regeln</span><span class="sxs-lookup"><span data-stu-id="07a4e-204">Rules</span></span>](rules.md)

- [<span data-ttu-id="07a4e-205">Erstellen einer Regel zum Ablegen von E-Mail-Elementen von einem Vorgesetzten und Kennzeichnen dieser Elemente für die Nachverfolgung</span><span class="sxs-lookup"><span data-stu-id="07a4e-205">Create a rule to file mail items from a manager and flag them for follow-up</span></span>](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md)
- [<span data-ttu-id="07a4e-206">Sofortiges Ausführen einer Regel</span><span class="sxs-lookup"><span data-stu-id="07a4e-206">Execute a rule instantly</span></span>](how-to-execute-a-rule-instantly.md)
- [<span data-ttu-id="07a4e-207">Ausführen einer Regel auf einem lokalen Computer</span><span class="sxs-lookup"><span data-stu-id="07a4e-207">Execute a rule on a local computer</span></span>](how-to-execute-a-rule-on-a-local-computer.md)
- [<span data-ttu-id="07a4e-208">Erstellen einer Regel zum Zuweisen von Kategorien zu E-Mail-Elementen basierend auf mehreren Wörtern im Betreff</span><span class="sxs-lookup"><span data-stu-id="07a4e-208">Create a rule to assign categories to mail items based on multiple words in the subject</span></span>](how-to-create-a-rule-to-assign-categories-to-mail-items-based-on-multiple-words-in-the-subject.md)


[<span data-ttu-id="07a4e-209">Beispielaufgaben mit Outlook-Ereignissen</span><span class="sxs-lookup"><span data-stu-id="07a4e-209">Sample tasks using Outlook events</span></span>](sample-tasks-using-outlook-events.md)

- [<span data-ttu-id="07a4e-210">Implementieren eines Wrappers für Prüfungen und Nachverfolgung von Ereignissen auf Elementebene in jedem Inspektor</span><span class="sxs-lookup"><span data-stu-id="07a4e-210">Implement a wrapper for inspectors and track item-level events in each inspector</span></span>](how-to-implement-a-wrapper-for-inspectors-and-track-item-level-events-in-each-inspector.md)

[<span data-ttu-id="07a4e-211">Suchen und Filtern</span><span class="sxs-lookup"><span data-stu-id="07a4e-211">Search and filter</span></span>](search-and-filter.md)

- [<span data-ttu-id="07a4e-212">Filtern und effizientes Aufzählen von Elementen in einem Ordner</span><span class="sxs-lookup"><span data-stu-id="07a4e-212">Filter and efficiently enumerate items in a folder</span></span>](how-to-filter-and-efficiently-enumerate-items-in-a-folder.md)
- [<span data-ttu-id="07a4e-213">Verwenden von SetColumns zum effizienten Aufzählen von Elementen in einem Ordner</span><span class="sxs-lookup"><span data-stu-id="07a4e-213">Use SetColumns to efficiently enumerate items in a folder</span></span>](how-to-use-setcolumns-to-efficiently-enumerate-items-in-a-folder.md)
- [<span data-ttu-id="07a4e-214">Verwenden von Arrays zum effizienten Aufzählen von Elementen in einem Ordner</span><span class="sxs-lookup"><span data-stu-id="07a4e-214">Use arrays to efficiently enumerate items in a folder</span></span>](how-to-use-arrays-to-efficiently-enumerate-items-in-a-folder.md)
- [<span data-ttu-id="07a4e-215">Aufzählen der Elemente im Posteingang basierend auf dem Zeitpunkt der letzten Änderung</span><span class="sxs-lookup"><span data-stu-id="07a4e-215">Enumerate items in the Inbox based on the last modification time</span></span>](how-to-enumerate-items-in-the-inbox-based-on-the-last-modification-time.md)
- [<span data-ttu-id="07a4e-216">Filtern und Anzeigen der im letzten Monat geänderten Posteingangselemente</span><span class="sxs-lookup"><span data-stu-id="07a4e-216">Filter and display Inbox items modified in the last month</span></span>](how-to-filter-and-display-inbox-items-modified-in-the-last-month.md)
- [<span data-ttu-id="07a4e-217">Filtern und Anzeigen von mehrwertigen Eigenschaften beim Aufzählen von Elementen in einem Ordner</span><span class="sxs-lookup"><span data-stu-id="07a4e-217">Filter and display multivalued properties when enumerating items in a folder</span></span>](how-to-filter-and-display-multivalued-properties-when-enumerating-items-in-a-folder.md)
- [<span data-ttu-id="07a4e-218">Filtern und Anzeigen von berechneten Eigenschaften beim Aufzählen von Elementen in einem Ordner</span><span class="sxs-lookup"><span data-stu-id="07a4e-218">Filter and display computed properties when enumerating items in a folder</span></span>](how-to-filter-and-display-computed-properties-when-enumerating-items-in-a-folder.md)
- [<span data-ttu-id="07a4e-219">Aufzählen von ausgeblendeten Elementen in einem Ordner</span><span class="sxs-lookup"><span data-stu-id="07a4e-219">Enumerate hidden items in a folder</span></span>](how-to-enumerate-hidden-items-in-a-folder.md)
- [<span data-ttu-id="07a4e-220">Verwenden der Sofortsuche zum Durchsuchen aller Ordner und aller Stores nach einem Ausdruck im Betreff</span><span class="sxs-lookup"><span data-stu-id="07a4e-220">Use instant search to search all folders and all stores for a phrase in the subject</span></span>](how-to-use-instant-search-to-search-all-folders-and-all-stores-for-a-phrase-in-the-subject.md)
- [<span data-ttu-id="07a4e-221">Suchen nach einem Ausdruck im Textkörper von Elementen in einem Ordner</span><span class="sxs-lookup"><span data-stu-id="07a4e-221">Search for a phrase in the body of items in a folder</span></span>](how-to-search-for-a-phrase-in-the-body-of-items-in-a-folder.md)
- [<span data-ttu-id="07a4e-222">Durchsuchen der Anlagen von Elementen in einem Ordner nach einem exakten Ausdruck</span><span class="sxs-lookup"><span data-stu-id="07a4e-222">Search attachments of items in a folder for an exact phrase</span></span>](how-to-search-attachments-of-items-in-a-folder-for-an-exact-phrase.md)
- [<span data-ttu-id="07a4e-223">Suchen und Abrufen von Terminen in einem Zeitbereich</span><span class="sxs-lookup"><span data-stu-id="07a4e-223">Search and obtain appointments in a time range</span></span>](how-to-search-and-obtain-appointments-in-a-time-range.md)
- [<span data-ttu-id="07a4e-224">Filtern von Terminserien und Suchen nach einer Zeichenfolge im Betreff</span><span class="sxs-lookup"><span data-stu-id="07a4e-224">Filter recurring appointments and search for a string in the subject</span></span>](how-to-filter-recurring-appointments-and-search-for-a-string-in-the-subject.md)
- [<span data-ttu-id="07a4e-225">Suchen und Abrufen von Elementen in einer aggregierten Ansicht</span><span class="sxs-lookup"><span data-stu-id="07a4e-225">Search and obtain items in an aggregated view</span></span>](how-to-search-and-obtain-items-in-an-aggregated-view.md)

[<span data-ttu-id="07a4e-226">Sitzungen</span><span class="sxs-lookup"><span data-stu-id="07a4e-226">Sessions</span></span>](sessions.md)

- [<span data-ttu-id="07a4e-227">Abrufen einer Instanz von Outlook und Anmelden bei dieser</span><span class="sxs-lookup"><span data-stu-id="07a4e-227">Get and sign in to an instance of Outlook</span></span>](how-to-get-and-log-on-to-an-instance-of-outlook.md)

[<span data-ttu-id="07a4e-228">Speicher</span><span class="sxs-lookup"><span data-stu-id="07a4e-228">Stores</span></span>](stores.md)

- [<span data-ttu-id="07a4e-229">Abrufen von Informationen zu Speichern in einem Profil</span><span class="sxs-lookup"><span data-stu-id="07a4e-229">Get information about stores in a profile</span></span>](how-to-get-information-about-stores-in-a-profile.md)
- [<span data-ttu-id="07a4e-230">Hinzufügen oder Entfernen eines Speichers</span><span class="sxs-lookup"><span data-stu-id="07a4e-230">Add or remove a store</span></span>](how-to-add-or-remove-a-store.md)

[<span data-ttu-id="07a4e-231">Aufgaben</span><span class="sxs-lookup"><span data-stu-id="07a4e-231">Tasks</span></span>](tasks.md)

- [<span data-ttu-id="07a4e-232">Erstellen eines Aufgabenelements</span><span class="sxs-lookup"><span data-stu-id="07a4e-232">Create a task item</span></span>](how-to-create-a-task-item.md)
- [<span data-ttu-id="07a4e-233">Zuordnen einer Aufgabe zu einem Empfänger</span><span class="sxs-lookup"><span data-stu-id="07a4e-233">Assign a task to a recipient</span></span>](how-to-assign-a-task-to-a-recipient.md)
- [<span data-ttu-id="07a4e-234">Anzeigen der an einen Empfänger gesendeten Aufgabenanforderungselemente</span><span class="sxs-lookup"><span data-stu-id="07a4e-234">Display the task request items sent to a recipient</span></span>](how-to-display-the-task-request-items-sent-to-a-recipient.md)
- [<span data-ttu-id="07a4e-235">Antworten auf ein Aufgabenanforderungselement</span><span class="sxs-lookup"><span data-stu-id="07a4e-235">Respond to a task request item</span></span>](how-to-respond-to-a-task-request-item.md)
- [<span data-ttu-id="07a4e-236">Erstellen eines periodischen Vorgangs</span><span class="sxs-lookup"><span data-stu-id="07a4e-236">Create a recurring task</span></span>](how-to-create-a-recurring-task.md)
- [<span data-ttu-id="07a4e-237">Kennzeichnen von E-Mail-Elementen von einem Vorgesetzten zur Nachverfolgung</span><span class="sxs-lookup"><span data-stu-id="07a4e-237">Flag mail items from a manager for follow-up</span></span>](how-to-flag-mail-items-from-a-manager-for-follow-up.md)

[<span data-ttu-id="07a4e-238">Ansichten</span><span class="sxs-lookup"><span data-stu-id="07a4e-238">Views</span></span>](views.md)

- [<span data-ttu-id="07a4e-239">Erstellen einer Ansicht</span><span class="sxs-lookup"><span data-stu-id="07a4e-239">Create a view</span></span>](how-to-create-a-view.md)
- [<span data-ttu-id="07a4e-240">Hinzufügen von Feldern zu einer Ansicht</span><span class="sxs-lookup"><span data-stu-id="07a4e-240">Add fields to a view</span></span>](how-to-add-fields-to-a-view.md)
- [<span data-ttu-id="07a4e-241">Auflisten der Elemente in einer Tabellenansicht</span><span class="sxs-lookup"><span data-stu-id="07a4e-241">Enumerate items in a table view</span></span>](how-to-enumerate-items-in-a-table-view.md)



