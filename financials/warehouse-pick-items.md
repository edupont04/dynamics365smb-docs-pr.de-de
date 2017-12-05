---
title: Entnahme von Artikeln | Microsoft Docs
description: "Die Lageraktivität des Kommissionierens von Artikeln vor ihrer Lieferung oder ihrem Verbrauch erfolgt je nach Konfiguration der Logistikfunktionen auf unterschiedliche Arten. Die [Einrichtung](../configure-warehouse-processes.md) Komplexität reicht von keinen Lagerfunktionen über Basis- Lagerkonfigurationen für die individuelle Abwicklung einzelner Aufträge in einer Aktivität oder mehreren Aktivitäten bis hin zu erweiterten Konfigurationen, bei denen alle Lageraktivitäten in einem gesteuerten Workflow durchgeführt werden müssen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 13db47dcfcc7eb6d30230490baa5ac961fc825a8
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="pick-items"></a><span data-ttu-id="38917-104">Entnahme von Artikeln</span><span class="sxs-lookup"><span data-stu-id="38917-104">Pick Items</span></span>
<span data-ttu-id="38917-105">Die Lageraktivität des Kommissionierens von Artikeln vor ihrer Lieferung oder ihrem Verbrauch erfolgt je nach Konfiguration der Logistikfunktionen auf unterschiedliche Arten.</span><span class="sxs-lookup"><span data-stu-id="38917-105">The warehouse activity of picking items before they are shipped or consumed is performed in different ways, depending on how warehouse management features are configured.</span></span> <span data-ttu-id="38917-106">Die Komplexität reicht von keinen Lagerfunktionen über Basis-Lagerkonfigurationen für die individuelle Abwicklung einzelner Aufträge in einer Aktivität oder mehreren Aktivitäten bis hin zu erweiterten Konfigurationen, bei denen alle Lageraktivitäten in einem gesteuerten Workflow durchgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="38917-106">The complexity can rank from no warehouse features, through basic warehouse configurations for order-by-order handling in one or more activities only, to advanced configurations where all warehouse activities must be performed in a directed workflow.</span></span> <span data-ttu-id="38917-107">Weitere Informationen finden Sie unter [Lagerortverwaltung einrichten](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="38917-107">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

<span data-ttu-id="38917-108">Wenn Sie sich entscheiden, Ihre Kommissionieraktivitäten mit Lagerbelegen zu organisieren und zu erfassen, setzen Sie ein Häkchen in das Feld **Kommissionierung erforderlich** auf der Lagerortkarte.</span><span class="sxs-lookup"><span data-stu-id="38917-108">If you decide to organize and record your picking activity with warehouse documents, you place a check mark in the **Require Pick** field on the location card.</span></span> <span data-ttu-id="38917-109">Dies zeigt an, dass Sie – wenn Sie Artikel haben, die für einen ausgehenden Herkunftsbeleg kommissioniert werden müssen – möchten, dass die Kommissionierung dieser Artikel durch die Anwendung gesteuert werden soll.</span><span class="sxs-lookup"><span data-stu-id="38917-109">This indicates that when you have items that need to be picked for an outbound source document you want the picking of those items to be controlled by the system.</span></span> <span data-ttu-id="38917-110">Ein ausgehender Herkunftsbeleg kann ein Verkaufsauftrag, eine Einkaufsreklamation, ein ausgehender Umlagerungsauftrag, Serviceauftrag oder ein Fertigungsauftrag sein, dessen Komponenten kommissioniert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="38917-110">An outbound source document can be a sales order, a purchase return order, an outbound transfer order, a service order, or a production order whose components should be picked.</span></span>

> [!NOTE]
> <span data-ttu-id="38917-111">Obwohl die Einstellung **Kommissionierung erforderlich** genannt wird, können Sie weiterhin Wareneingänge und Lieferungen direkt aus den Quellgeschäftsunterlagen an Lagerorten, in denen Sie dieses Kontrollkästchen aktivieren, buchen.</span><span class="sxs-lookup"><span data-stu-id="38917-111">Even though the setting is called **Require Pick**, you can still post shipments directly from the source business document at location where you select this check box.</span></span>

<span data-ttu-id="38917-112">Wenn Ihr Lagerort so eingerichtet wurde, dass die Bearbeitung der Kommissionierung erforderlich ist, jedoch nicht die Bearbeitung des Warenausgangs, verwenden Sie das Fenster **Lagerkommissionierung**, um die Kommissionierungsinformationen zu strukturieren, zu drucken, die Ergebnisse der tatsächlichen Kommissionierung einzugeben und die Kommissionierungsinformationen zu buchen, wodurch gleichzeitig die Lieferung der Artikel gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="38917-112">If your location is set up to require pick processing but not shipment processing, you use the **Inventory Pick** window to organize the picking information, print the picking information, enter the result of the pick, and post the picking information, which in turn posts the shipment of the items.</span></span> <span data-ttu-id="38917-113">Im Falle der Kommissionierung von Komponenten für einen Fertigungsauftrag wird beim Buchen der Kommissionierung auch der Verbrauch gebucht.</span><span class="sxs-lookup"><span data-stu-id="38917-113">In the case of picking components for a production order, the posting of the pick also posts the consumption.</span></span>

<span data-ttu-id="38917-114">Wenn Ihr Lagerort so eingerichtet ist, dass die Bearbeitung der Kommissionierung und des Warenausgangs erforderlich ist, Sie also Häkchen im Feld **Kommissionierung erforderlich** und **Warenausgang erforderlich** auf der Lagerortkarte gesetzt haben, verwenden Sie das Fenster **Kommissionierung** für die Abwicklung der Kommissionierung.</span><span class="sxs-lookup"><span data-stu-id="38917-114">If your location is set up to require both pick and shipment processing, so that you have placed check marks in both the **Require Pick** and **Require Shipment** field on the location card, you use the **Warehouse Pick** window to handle the pick.</span></span> <span data-ttu-id="38917-115">Die Kommissionierfunktionen sind ähnlich wie die Lagerkommissionierung, außer dass Sie anstatt die Kommissionierinformationen zu buchen, die Kommissionierung registrieren.</span><span class="sxs-lookup"><span data-stu-id="38917-115">The warehouse pick functions similarly to the inventory pick, except that instead of posting the picking information, you register the pick.</span></span> <span data-ttu-id="38917-116">Dieser Registrierungsprozess bucht nicht den Warenausgang, sondern stellt lediglich die Artikel für den Warenausgang zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="38917-116">This registering process does not post the shipment, but merely makes the items available for shipment.</span></span> <span data-ttu-id="38917-117">Als Lagerbestandsmanager können Sie Kommissionierungsvorschläge verwenden, um Kommissionierungsinformationen zu organisieren, bevor Sie die individuellen Kommissionierungsanweisungen erstellen.</span><span class="sxs-lookup"><span data-stu-id="38917-117">As a warehouse manager, you can use a pick worksheets to organize pick information before creating the individual warehouse pick instructions.</span></span>

<span data-ttu-id="38917-118">Die folgende Tabelle enthält eine Abfolge von Aufgaben sowie Links zu den entsprechenden Themen, in denen diese Aufgaben erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="38917-118">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="38917-119">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="38917-119">**To**</span></span>|<span data-ttu-id="38917-120">**Siehe**</span><span class="sxs-lookup"><span data-stu-id="38917-120">**See**</span></span>|
|------------|-------------|  
|<span data-ttu-id="38917-121">Buchen Sie die Lieferung von Artikeln direkt im Beleg des ausgehenden Auftrags, da keine Lagerfunktionen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="38917-121">Post the shipment of items directly in the outbound order document because no warehouse features exist.</span></span> <span data-ttu-id="38917-122">(Funktioniert analog für Verkaufsaufträge, ausgehende Umlagerungsaufträge und Rücklieferungen.)</span><span class="sxs-lookup"><span data-stu-id="38917-122">(Works the same for sales orders, outbound transfer orders, and return shipments.)</span></span>|[<span data-ttu-id="38917-123">So geht's: Artikel versenden</span><span class="sxs-lookup"><span data-stu-id="38917-123">How to: Ship Items</span></span>](warehouse-how-ship-items.md)|  
|<span data-ttu-id="38917-124">Kommissionieren Sie Artikel auftragsweise, und buchen Sie bei einer Basis-Lagerkonfiguration die Lieferung in derselben Aktivität.</span><span class="sxs-lookup"><span data-stu-id="38917-124">Pick items order by order and post the shipment in the same activity, in a basic warehouse configuration.</span></span>|[<span data-ttu-id="38917-125">So wird's gemacht: Artikel mit der Lagerkommissionierung kommissionieren</span><span class="sxs-lookup"><span data-stu-id="38917-125">How to: Pick Items with Inventory Picks</span></span>](warehouse-how-to-pick-items-with-inventory-picks.md)|
|<span data-ttu-id="38917-126">Kommissionieren Sie Artikel für mehrere Aufträge in einer erweiterten Lagerkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="38917-126">Pick items for multiple orders in an advanced warehouse configuration.</span></span>|[<span data-ttu-id="38917-127">So wird's gemacht: Artikel mit Kommissionierungen kommissionieren</span><span class="sxs-lookup"><span data-stu-id="38917-127">How to: Pick Items with Warehouse Picks</span></span>](warehouse-how-to-pick-items-for-warehouse-shipment.md)|  
|<span data-ttu-id="38917-128">Kommissionieren Sie Komponenten für Produktion oder Montage in einer grundlegenden oder erweiterten Lagerkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="38917-128">Pick components for production or assembly in a basic or an advanced warehouse configuration.</span></span>|[<span data-ttu-id="38917-129">Vorgehensweise: Kommissionierung für die Produktion oder Montage</span><span class="sxs-lookup"><span data-stu-id="38917-129">How to: Pick for Production or Assembly</span></span>](warehouse-how-to-pick-for-production.md)|  
|<span data-ttu-id="38917-130">Planen Sie optimierte Kommissionierungsanweisungen für eine Reihe von Lieferungen, bevor Sie die Lagermitarbeiter die gebuchten Lieferungen direkt bearbeiten lassen.</span><span class="sxs-lookup"><span data-stu-id="38917-130">Plan optimized pick instructions for a number of shipments rather than have warehouse workers act directly on posted shipments.</span></span>|[<span data-ttu-id="38917-131">Vorgehensweise: Kommissionierungen im Vorschlag bearbeiten</span><span class="sxs-lookup"><span data-stu-id="38917-131">How to: Plan Picks in Worksheets</span></span>](warehouse-how-to-plan-picks-in-worksheets.md)|  
|<span data-ttu-id="38917-132">Kommissionieren Sie Artikel für einen bestimmten Zweck, z. B. eine Produktion benötigt zusätzliche Komponenten. Dies geschieht technisch gesehen so, dass die Artikel das Lager nicht verlassen.</span><span class="sxs-lookup"><span data-stu-id="38917-132">Pick items technically for a special purpose, such as a production unit in need of extra components, in such a way that the items do not technically leave the warehouse.</span></span>|[<span data-ttu-id="38917-133">Vorgehensweise: Wählen und setzen Sie die Einlagerung verwendet ohne Herkunftsbeleg</span><span class="sxs-lookup"><span data-stu-id="38917-133">How to: Pick and Put Away Without a Source Document</span></span>](warehouse-how-to-create-put-aways-from-internal-put-aways.md)|
|<span data-ttu-id="38917-134">Die automatische Kommissionierung von Artikeln entsprechend ihres Ablaufdatums, beispielsweise begrenzt haltbare Lebensmittel, verstehen.</span><span class="sxs-lookup"><span data-stu-id="38917-134">Understand how to automatically pick items according to their expiration date, for example perishable goods.</span></span>|[<span data-ttu-id="38917-135">Kommissionierung nach FEFO</span><span class="sxs-lookup"><span data-stu-id="38917-135">Picking By FEFO</span></span>](warehouse-picking-by-fefo.md)|
|<span data-ttu-id="38917-136">Teilen Sie eine Kommissionierungszeile in mehrere Zeilen auf, z. B., da es nicht genügend Artikel verfügbare sind, um sie aus dem festgelegten Lagerplatz zu entnehmen.</span><span class="sxs-lookup"><span data-stu-id="38917-136">Split a pick line into multiple lines, for example because there are not enough items to take from in the designated bin.</span></span>|[<span data-ttu-id="38917-137">Vorgehensweise: Aufteilen von Lageraktivitätszeilen</span><span class="sxs-lookup"><span data-stu-id="38917-137">How to: Split Warehouse Activity Lines</span></span>](warehouse-how-to-split-warehouse-activity-lines.md)|
|<span data-ttu-id="38917-138">Sie erhalten sofortigen Zugriff auf Kommissionierungen, die Ihnen als Lagermitarbeiter zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="38917-138">Get immediate access to picks that are assigned to you as a warehouse worker.</span></span>|[<span data-ttu-id="38917-139">Vorgehensweise: Suchen der Lagerzuweisungen</span><span class="sxs-lookup"><span data-stu-id="38917-139">How to: Find Your Warehouse Assignments</span></span>](warehouse-how-to-find-your-warehouse-assignments.md)|  

## <a name="see-also"></a><span data-ttu-id="38917-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38917-140">See Also</span></span>  
[<span data-ttu-id="38917-141">Logistik</span><span class="sxs-lookup"><span data-stu-id="38917-141">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="38917-142">Lagerbest</span><span class="sxs-lookup"><span data-stu-id="38917-142">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="38917-143">[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="38917-143">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="38917-144">[Montageverwaltung](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="38917-144">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="38917-145">Designdetails: Logistik</span><span class="sxs-lookup"><span data-stu-id="38917-145">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="38917-146">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="38917-146">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
