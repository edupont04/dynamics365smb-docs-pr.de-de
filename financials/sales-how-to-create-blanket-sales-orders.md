---
title: "Vorgehensweise: Erstellen von Rahmenaufträgen| Microsoft Docs"
description: "Verwenden Sie Rahmenaufträge, wenn ein Kunde der Abnahme großer Mengen zugestimmt hat, die in mehreren kleineren Lieferungen über einen bestimmten Zeitraum geliefert werden sollen."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0b91925a7ec6adb40cdf99d5bcf3398b62c28b3f
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-work-with-blanket-sales-orders"></a><span data-ttu-id="82983-103">Vorgehensweise: Arbeiten mit Rahmenaufträgen</span><span class="sxs-lookup"><span data-stu-id="82983-103">How to: Work with Blanket Sales Orders</span></span>
<span data-ttu-id="82983-104">Ein Rahmenauftrag stellt ein Gerüst für eine langfristige Vereinbarung zwischen Ihnen und einem Debitor dar.</span><span class="sxs-lookup"><span data-stu-id="82983-104">A blanket sales order represents a framework for a long-term agreement between you and your customer.</span></span>

<span data-ttu-id="82983-105">Ein Rahmenauftrag wird in der Regel erstellt, wenn sich ein Debitor verpflichtet hat, größere Mengen abzunehmen, die über einen längeren Zeitraum in mehreren kleineren bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="82983-105">A blanket order is typically made when a customer has committed to purchasing large quantities that are to be delivered in several smaller shipments over a certain period of time.</span></span> <span data-ttu-id="82983-106">Häufig decken Rahmenaufträge nur einen bestimmten Artikel ab, für den bestimmte Liefertermine vorgegeben sind.</span><span class="sxs-lookup"><span data-stu-id="82983-106">Often blanket orders cover only one item with predetermined delivery dates.</span></span> <span data-ttu-id="82983-107">Der Hauptgrund für die Verwendung eines Rahmenauftrags anstelle eines Verkaufsauftrags besteht darin, dass die bei einem Rahmenauftrag eingegebenen Mengen keinen Einfluss auf die Artikelverfügbarkeit haben und daher als Arbeitsvorlage für die Überwachung und Planung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="82983-107">The main reason for using a blanket order rather than a sales order is that quantities entered on a blanket order do not affect item availability and thus can be used as a worksheet for monitoring, forecasting, and planning purposes.</span></span>

<span data-ttu-id="82983-108">In einem Rahmenauftrag kann jede einzelne Lieferung als Auftragszeile eingerichtet werden, die dann zum Zeitpunkt der Lieferung in einen Auftrag umgewandelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="82983-108">On the blanket order, each separate shipment can be set up as an order line, which can then be converted into a sales order at the time of shipping.</span></span>

<span data-ttu-id="82983-109">Rahmenaufträge werden beispielsweise verwendet, wenn ein Kunde anruft und 1000 Einheiten eines Artikels bestellt, die über den kommenden Monat in Mengen von je 250 Stck. pro Woche geliefert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="82983-109">An example of when a blanket sales order could be used is if a customer calls and places an order of 1000 units of an item and they want the items to be delivered in 250 units every week over the next month.</span></span>

> [!NOTE]
> <span data-ttu-id="82983-110">Rahmenbestellungen funktionieren auf ähnliche Weise wie Rahmenaufträge.</span><span class="sxs-lookup"><span data-stu-id="82983-110">Blanket purchase orders work in a similar way as blanket sales orders.</span></span> <span data-ttu-id="82983-111">Die Dokumentation enthält keine Rahmenbestellungen.</span><span class="sxs-lookup"><span data-stu-id="82983-111">This documentation does not cover blanket purchase orders.</span></span>

## <a name="to-create-a-blanket-sales-order"></a><span data-ttu-id="82983-112">So legen Sie einen Rahmenauftrag an:</span><span class="sxs-lookup"><span data-stu-id="82983-112">To create a blanket sales order</span></span>  
1. <span data-ttu-id="82983-113">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Rahmenbestellungen** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="82983-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Blanket Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="82983-114">Wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="82983-114">Choose the **New** action.</span></span>  
3. <span data-ttu-id="82983-115">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="82983-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  <span data-ttu-id="82983-116">Nehmen Sie im Feld **Auftragsdatum** keine Eingabe vor.</span><span class="sxs-lookup"><span data-stu-id="82983-116">Leave the **Order Date** field blank.</span></span> <span data-ttu-id="82983-117">Wenn die einzelnen Verkaufsaufträge anhand des Rahmenauftrags erstellt werden, wird als Auftragsdatum des Verkaufsauftrags automatisch das Arbeitsdatum festgelegt.</span><span class="sxs-lookup"><span data-stu-id="82983-117">When the separate sales orders are created from the blanket order, the order date of the sales order is set to equal the actual work date.</span></span>
5. <span data-ttu-id="82983-118">Erstellen Sie im Inforegister **Zeilen** einzelne Zeilen für jede Lieferung.</span><span class="sxs-lookup"><span data-stu-id="82983-118">On the **Lines** FastTab, create separate lines for each shipment.</span></span> <span data-ttu-id="82983-119">Wenn der Kunde beispielsweise 1.000 Einheiten gleichmäßig auf vier Wochen verteilt erhalten möchte, geben Sie vier separate Zeilen mit jeweils 250 Einheiten ein.</span><span class="sxs-lookup"><span data-stu-id="82983-119">For instance, if your customer wants 1000 units split out equally between four weeks, you would enter four separate lines of 250 units each.</span></span>   

## <a name="to-create-a-sales-order-from-a-blanket-sales-order"></a><span data-ttu-id="82983-120">So erstellen Sie einen Auftrag aus einem Rahmenauftrag:</span><span class="sxs-lookup"><span data-stu-id="82983-120">To create a sales order from a blanket sales order</span></span>  

1.  <span data-ttu-id="82983-121">Um einen Auftrag für eine oder mehrere der Zeilen des Montagerahmenauftrags zu erstellen, entfernen Sie die Menge im Feld **Zu liefern** in allen Zeilen, für die zum aktuellen Zeitpunkt KEINE Lieferung gewünscht wird.</span><span class="sxs-lookup"><span data-stu-id="82983-121">To create an order for any of the lines in the blanket assembly order, remove the quantity in the **Qty. to Ship** field on all the lines that you DO NOT wish to ship at this time.</span></span>  
2.  <span data-ttu-id="82983-122">Wenn Sie die Aufträge erstellen möchten, klicken Sie auf **Auftrag erst.** und anschließend auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="82983-122">When you are ready to create orders, choose the **Make Order**m action, and then choose **Yes**.</span></span> <span data-ttu-id="82983-123">Sie werden in einer Meldung darüber informiert, dass dem Rahmenauftrag eine Auftragsnummer zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="82983-123">A message appears informing you that the blanket order has been assigned an order number.</span></span> <span data-ttu-id="82983-124">Beachten Sie, dass der Rahmenauftrag nicht gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="82983-124">Note that the blanket order has not been deleted.</span></span>  
3.  <span data-ttu-id="82983-125">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="82983-125">Choose the **OK** button.</span></span>  
4.  <span data-ttu-id="82983-126">Um die Ergebnisse der vorangehenden Schritte anzuzeigen, wählen Sie auf dem Inforegister **Zeilen** die Option **Aktionen**, wählen Sie Zeile, wählen Sie Nicht gebuchte Zeilen, und wählen Sie dann **Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="82983-126">To see the results of the preceding steps, choose the **Line** action, choose the **Unposted Lines** action, and then choose the **Orders** action.</span></span>  
5.  <span data-ttu-id="82983-127">Wählen Sie im Fenster **Verkaufszeilen** den entsprechenden Verkaufsauftrag aus. Wählen Sie auf dem Inforegister **Zeilen** die Option Aktionen, wählen Sie Zeile, und wählen Sie dann **Beleg anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="82983-127">In the **Sales Lines** window, select the appropriate sales order, choose the **Line** action, and then choose the **Show Document** action.</span></span>  

<span data-ttu-id="82983-128">Das folgende gilt für Verkaufsaufträge nach der Erstellung von Rahmenaufträgen:</span><span class="sxs-lookup"><span data-stu-id="82983-128">The following applies to sales orders after they have been created from blanket sales orders:</span></span>  

- <span data-ttu-id="82983-129">Nachdem der Rahmenauftrag in einen Auftrag umgewandelt wurde, enthält diese sämtliche Zeilen des Rahmenauftrags.</span><span class="sxs-lookup"><span data-stu-id="82983-129">After the blanket order is converted into a sales order, the sales order contains all the lines from the blanket order.</span></span> <span data-ttu-id="82983-130">Die Mengen der Zeilen, bei denen die Menge im Feld **Zu liefern** gelöscht wurde, werden mit leerem Feld **Menge** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="82983-130">The lines where the quantity in the **Qty. to Ship** field was deleted appear, but with blank **Quantity** fields.</span></span> <span data-ttu-id="82983-131">Sie können diese Zeilen bearbeiten oder löschen oder unverändert beibehalten.</span><span class="sxs-lookup"><span data-stu-id="82983-131">You may choose to leave, edit, or delete the lines.</span></span>  
- <span data-ttu-id="82983-132">Beachten Sie unbedingt, dass die Menge der Auftragszeile die Menge der zugehörigen Rahmenauftragszeile nicht übersteigen darf.</span><span class="sxs-lookup"><span data-stu-id="82983-132">It is important to remember that the sales order line quantity must not exceed the quantity of the associated blanket order line.</span></span> <span data-ttu-id="82983-133">Andernfalls kann der Auftrag nicht gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="82983-133">Otherwise, posting of the sales order will not be possible.</span></span>  
- <span data-ttu-id="82983-134">Wenn der Auftrag als geliefert und/oder als fakturiert gebucht wurde, werden die Felder **Menge geliefert** und **Menge fakturiert** auf des zugehörigen Rahmenauftrags automatisch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="82983-134">When the sales order is posted as shipped and/or invoiced, the **Quantity Shipped** and **Quantity Invoiced** fields are updated on the related blanket order.</span></span>  
- <span data-ttu-id="82983-135">Die Nummer des Rahmenauftrags und die Zeilennummer werden als Eigenschaften der Auftragszeilen erfasst, wenn diese aus einem Rahmenauftrag erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="82983-135">The blanket order number and line number are recorded as properties of the sales lines when created from a blanket order.</span></span>  
- <span data-ttu-id="82983-136">Wenn Aufträge nicht direkt aus einem Rahmenauftrag erstellt werden, aber dennoch zu diesem gehören, kann eine Verknüpfung zwischen einem Auftrag und einem Rahmenauftrag eingerichtet werden, indem die Nummer des verknüpften Rahmenauftrags im Feld **Rahmenauftragsnr.** in der Auftragszeile eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="82983-136">When sales orders are not created directly from the blanket order but still relate to it, a link between a sales order and a blanket order can be established by entering the associated blanket order number in the **Blanket Order No.**</span></span> <span data-ttu-id="82983-137">Lagerdurchlaufzeit" der Einkaufsbestellung.</span><span class="sxs-lookup"><span data-stu-id="82983-137">field on the sales order line.</span></span>  
- <span data-ttu-id="82983-138">Nachdem der Verkaufsauftrag für die Gesamtmenge einer Rahmenbestellzeile erstellt wurde, kann kein anderer Verkaufsauftrag für dieselbe Zeile erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="82983-138">After the sales order has been created for the total quantity of a blanket order line, no other sales order can be created for the same line.</span></span> <span data-ttu-id="82983-139">Benutzer können im Feld **Zu liefern** keine Menge eingeben.</span><span class="sxs-lookup"><span data-stu-id="82983-139">Users are prevented from entering a quantity in the **Qty. to Ship** field.</span></span> <span data-ttu-id="82983-140">Wenn in einem Rahmenauftrag jedoch weitere Mengen hinzugefügt werden müssen, kann der Wert im Feld **Menge** erhöht werden, und es können weitere Aufträge erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="82983-140">If, however, additional quantities need to be added to a blanket order, the value in the **Quantity** field can be increased and additional orders can then be created.</span></span>  
- <span data-ttu-id="82983-141">Der fakturierte Rahmenauftrag verbleibt im System, bis er gelöscht wird, und zwar entweder durch Löschen einzelner Rahmenaufträge oder durch Ausführen der Stapelverarbeitung **Erledigte Rahmenauftr. löschen**.</span><span class="sxs-lookup"><span data-stu-id="82983-141">The invoiced blanket sales order remains in the system until it is deleted, either by deleting individual blanket orders or by running the **Delete Invoiced Blanket Sales Orders** batch job.</span></span>  
- <span data-ttu-id="82983-142">Wenn ein Debitor im Anwendungsbereich "Marketing" auch als Kontakt eingerichtet wurde und Sie einen Aktivitätenvorlagencode für Rahmenaufträge im Fenster **Marketing & Vertrieb Einr.** angegeben haben, wird eine Aktivität in der Tabelle "Aktivitätenprotokollposten" aufgezeichnet, wenn Sie **Drucken** auswählen, um die Rahmenaufträge zu drucken.</span><span class="sxs-lookup"><span data-stu-id="82983-142">If a customer is also recorded as a contact in the Marketing application area, and if you have specified an interaction template code for blanket sales order in the **Marketing Setup** window, an interaction is recorded in the Interaction Log Entry table when you select **Print** to print the blanket sales order.</span></span>

## <a name="to-view-the-status-of-a-blanket-purchase-order"></a><span data-ttu-id="82983-143">So zeigen Sie den Status einer Rahmenbestellung an</span><span class="sxs-lookup"><span data-stu-id="82983-143">To view the status of a blanket purchase order</span></span>  
<span data-ttu-id="82983-144">Sie können sich den Status einer Rahmenbestellung in dem Fenster **Einkaufsstatistik Rahmenbestellung** anzeigen lassen.</span><span class="sxs-lookup"><span data-stu-id="82983-144">You can see the status of a blanket sales order in the **Purchase Blanket Order Statistics** window.</span></span> <span data-ttu-id="82983-145">Dies kann dann von Bedeutung sein, wenn Sie beginnen, die Bestellung zu fakturieren, die aus der Rahmenbestellung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="82983-145">This may be relevant when you start to invoice the order that is created from the blanket purchase order.</span></span>  

1.  <span data-ttu-id="82983-146">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Rahmenbestellungen** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="82983-146">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Blanket Purchase Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="82983-147">Wählen Sie eine Rahmenbestellung aus, und wählen Sie die **Statistik** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="82983-147">Select a blanket purchase order, and then choose the **Statistics** action.</span></span>  
3.  <span data-ttu-id="82983-148">Im Fenster **Einkaufsstatistik Rahmenbestellung** finden Sie auf dem Inforegister **Allgemein** zusammengefasste Informationen über die gesamte Bestellung, basierend auf den Gesamtmengen in den verschiedenen **Mengenfeldern** in den Rahmeneinkaufsbestellungszeilen.</span><span class="sxs-lookup"><span data-stu-id="82983-148">In the **Purchase Blanket Order Statistics** window, on the **General** FastTab, you can see summary information about the entire order based on the total quantity in the various **Quantity fields** on the blanket purchase order lines.</span></span>  

    - <span data-ttu-id="82983-149">Auf dem Inforegister **Fakturierung** finden Sie zusammengefasste Informationen über die Gesamtmenge in den verschiedenen Feldern **Zu fakturieren** in den Einkaufsrahmenbestellungszeilen.</span><span class="sxs-lookup"><span data-stu-id="82983-149">On the **Invoicing** FastTab, you can see summary information based on the total quantity in the **Qty. to Invoice** fields on the purchase blanket order lines.</span></span>  
    - <span data-ttu-id="82983-150">Auf dem Inforegister **Lieferung** werden zusammengefasste Informationen über die Gesamtmenge in den verschiedenen Feldern **Zu liefern** in den Einkaufsrahmenbestellungszeilen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="82983-150">On the **Shipping** FastTab, you can see summary information based on the total quantity in the **Qty. to Receive** fields on the purchase blanket order lines.</span></span>  
    - <span data-ttu-id="82983-151">Auf dem Inforegister **Vorauszahlung** werden zusammenfassende Informationen zu den vorab bezahlten Beträgen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="82983-151">On the **Prepayment** FastTab, you can see summary information about any prepaid amounts.</span></span>  
    - <span data-ttu-id="82983-152">Auf dem Inforegister **Kreditor** werden bestimmte grundlegende Informationen über den Kreditor angezeigt.</span><span class="sxs-lookup"><span data-stu-id="82983-152">On the **Vendor** FastTab, you can see certain basic information about the vendor.</span></span>    

## <a name="to-view-unposted-and-posted-blanket-sales-order-lines"></a><span data-ttu-id="82983-153">Um gebuchte und nicht gebuchte Rahmenbestellungszeilen anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="82983-153">To view unposted and posted blanket sales order lines</span></span>   
<span data-ttu-id="82983-154">Die Verknüpfung zwischen dem Rahmenauftrag und dem daraus stammenden Verkaufsauftrag und jeder andere Verkaufsbeleg wird beibehalten, nachdem sie als Liste gebuchter und ungebuchter Verkaufsauftrags- und Rechnungszeilen gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="82983-154">The link between the blanket sales order and the originating sales order, and any other sales document, is retained after posting as a list of posted and unposted sales order invoice lines.</span></span>  

1. <span data-ttu-id="82983-155">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Rahmenbestellungen** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="82983-155">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon enter **Blanket Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="82983-156">Öffnen Sie die Rahmenbestellung, die Sie anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="82983-156">Open the blanket sales order you want to view.</span></span>
3. <span data-ttu-id="82983-157">Sie können nicht gebuchte Posten anzeigen, indem Sie die entsprechende Zeile markieren und dann auf dem Inforegister  Zeilen auf  Aktionen,  **Zeile**,  **Nicht gebuchte Zeilen** klicken.</span><span class="sxs-lookup"><span data-stu-id="82983-157">To view unposted entries, select the line in question, choose the **Line** action, and then choose the **Unposted Lines** action.</span></span> <span data-ttu-id="82983-158">Wählen Sie eine der folgenden Optionen aus.</span><span class="sxs-lookup"><span data-stu-id="82983-158">Choose one of the following options.</span></span>  

    <table>
    <tr>
    <th><span data-ttu-id="82983-159">Option</span><span class="sxs-lookup"><span data-stu-id="82983-159">Option</span></span></th>
    <th><span data-ttu-id="82983-160">Description</span><span class="sxs-lookup"><span data-stu-id="82983-160">Description</span></span></th>
    </tr>
    <tr>
    <td><span data-ttu-id="82983-161">**Aufträge**</span><span class="sxs-lookup"><span data-stu-id="82983-161">**Orders**</span></span></td>
    <td><span data-ttu-id="82983-162">Gibt mit der ausgewählten Zeile verknüpfte offene Aufträge an.</span><span class="sxs-lookup"><span data-stu-id="82983-162">Specifies open orders associated with the selected line.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="82983-163">**Rechnungen**</span><span class="sxs-lookup"><span data-stu-id="82983-163">**Invoices**</span></span></td>
    <td><span data-ttu-id="82983-164">Gibt mit der ausgewählten Zeile verknüpfte offene Rechnungen an.</span><span class="sxs-lookup"><span data-stu-id="82983-164">Specifies open invoices that have been associated with the selected line.</span></span> <span data-ttu-id="82983-165">Offene Rechnungen werden durch Eingabe der Nummer des Rahmenauftrags in der Verkaufsrechnungszeile manuell mit einem Rahmenauftrag verknüpft.</span><span class="sxs-lookup"><span data-stu-id="82983-165">Open invoices are manually associated with a blanket order by entering the blanket order number on the sales invoice line.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="82983-166">**Reklamationen**</span><span class="sxs-lookup"><span data-stu-id="82983-166">**Return Orders**</span></span></td>
    <td><span data-ttu-id="82983-167">Gibt mit der ausgewählten Zeile verknüpfte offene Reklamationen an.</span><span class="sxs-lookup"><span data-stu-id="82983-167">Specifies open return orders that have been associated with the selected line.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="82983-168">**Gutschriften**</span><span class="sxs-lookup"><span data-stu-id="82983-168">**Credit Memos**</span></span></td>
    <td><span data-ttu-id="82983-169">Gibt mit der ausgewählten Zeile verknüpfte offene Gutschriften an.</span><span class="sxs-lookup"><span data-stu-id="82983-169">Specifies open credit memos that have been associated with the selected line.</span></span></td>
    </tr>
    </table><span data-ttu-id="82983-170">
4.Sie können nicht gebuchte Posten anzeigen, indem Sie die entsprechende Zeile markieren und dann auf dem Inforegister  **Zeilen** auf  Aktionen,  Zeile,  **Gebuchte Zeilen** klicken.</span><span class="sxs-lookup"><span data-stu-id="82983-170">
4. To view posted entries, select the line in question, choose the **Line** action, and then choose the **Posted Lines** action.</span></span> <span data-ttu-id="82983-171">Wählen Sie eine der folgenden Optionen aus.</span><span class="sxs-lookup"><span data-stu-id="82983-171">Choose one of the following options.</span></span>  

    <table>
    <tr>
    <th><span data-ttu-id="82983-172">Option</span><span class="sxs-lookup"><span data-stu-id="82983-172">Option</span></span></th>
    <th><span data-ttu-id="82983-173">Description</span><span class="sxs-lookup"><span data-stu-id="82983-173">Description</span></span></th>
    </tr>
    <tr>
    <td><span data-ttu-id="82983-174">**Lieferungen**</span><span class="sxs-lookup"><span data-stu-id="82983-174">**Shipments**</span></span></td>
    <td><span data-ttu-id="82983-175">Mit der ausgewählten Zeile verknüpfte gebuchte Lieferungen.</span><span class="sxs-lookup"><span data-stu-id="82983-175">Posted shipments associated with the selected line.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="82983-176">**Rechnungen**</span><span class="sxs-lookup"><span data-stu-id="82983-176">**Invoices**</span></span></td>
    <td><span data-ttu-id="82983-177">Mit der ausgewählten Zeile verknüpfte gebuchte Rechnungen.</span><span class="sxs-lookup"><span data-stu-id="82983-177">Posted invoices associated with the selected line.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="82983-178">**Rücksendungen**</span><span class="sxs-lookup"><span data-stu-id="82983-178">**Return Receipts**</span></span></td>
    <td><span data-ttu-id="82983-179">Mit der ausgewählten Zeile verknüpfte gebuchte Rücksendungen.</span><span class="sxs-lookup"><span data-stu-id="82983-179">Posted return receipts that have been associated with the selected line.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="82983-180">**Gutschriften**</span><span class="sxs-lookup"><span data-stu-id="82983-180">**Credit Memos**</span></span></td>
    <td><span data-ttu-id="82983-181">Mit der ausgewählten Zeile verknüpfte gebuchte Gutschriften.</span><span class="sxs-lookup"><span data-stu-id="82983-181">Posted credit memos that have been associated with the selected line.</span></span></td>
    </tr>
    </table><span data-ttu-id="82983-182">
5. Klicken Sie im Fenster **Verkaufszeile** auf Zeile, **Beleg anzeigen**, um den Posten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="82983-182">
5. In the **Sales Lines** window, choose the **Show Document** action to view the entry.</span></span>

## <a name="see-also"></a><span data-ttu-id="82983-183">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82983-183">See Also</span></span>
[<span data-ttu-id="82983-184">Verkauf</span><span class="sxs-lookup"><span data-stu-id="82983-184">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="82983-185">Einrichten von Verkäufen</span><span class="sxs-lookup"><span data-stu-id="82983-185">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="82983-186">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="82983-186">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
