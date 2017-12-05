---
title: 'Vorgehensweise: Titel-Beziehungen zwischen Bedarf und Vorrat | Microsoft Docs'
description: "Verfolgen des Auftragsbedarfs (Menge mit Bedarfsverursacher), der Absatzplanung, des Rahmenauftrags oder der Planungsparameter (Menge ohne Bedarfsverursacher), auf den bzw. auf die die betreffende Planungszeile zurückzuführen ist"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 511381e4f6d469ff16714a30fde60d3e238ad975
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-track-relations-between-demand-and-supply"></a><span data-ttu-id="f8609-103">Vorgehensweise: Titel-Beziehungen zwischen Bedarf und Vorrat</span><span class="sxs-lookup"><span data-stu-id="f8609-103">How to: Track Relations Between Demand and Supply</span></span>
<span data-ttu-id="f8609-104">Verfolgen des Auftragsbedarfs (Menge mit Bedarfsverursacher), der Absatzplanung, des Rahmenauftrags oder der Planungsparameter (Menge ohne Bedarfsverursacher), auf den bzw. auf die die betreffende Planungszeile zurückzuführen ist</span><span class="sxs-lookup"><span data-stu-id="f8609-104">From any supply or demand document in the so-called order network, you can track the order demand (tracked quantity), forecast, blanket sales order, or planning parameter (untracked quantity) that has given rise to the planning line in question.</span></span>

<span data-ttu-id="f8609-105">Die Planungsvorschläge beinhalten zusätzliche Planungsinformationen wie  Nachverfolgung zu nicht auftragsbezogenen Entitäten und  Warnungen, um den Planer bei der Erstellung eines optimalen Beschaffungsplans zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="f8609-105">The planning worksheets also offers supporting planning information about non-order entities to help the planner obtain an optimal supply plan.</span></span> <span data-ttu-id="f8609-106">Weitere Informationen zu Planungsüberschuss ohne Bedarfsverursacher finden Sie unter  Planungselement ohne Bedarfsverursacher.</span><span class="sxs-lookup"><span data-stu-id="f8609-106">For more information, see the "Untracked Planning Elements" section.</span></span>

## <a name="to-track-linked-items"></a><span data-ttu-id="f8609-107">Um verknüpfte Artikel zu verfolgen</span><span class="sxs-lookup"><span data-stu-id="f8609-107">To track linked items</span></span>
<span data-ttu-id="f8609-108">Die Verfolgung zeigt, wie Verkaufsaufträge, Fertigungsaufträge und Bestellungen über Reservierungen mit einem Fertigungsauftrag verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="f8609-108">Order tracking shows how sales orders, production orders, and purchase orders are related to the manufacturing order through the planning and reservation systems.</span></span>

<span data-ttu-id="f8609-109">Nachfolgend wird erläutert, wie Artikel für einen fest geplanten Fertigungsauftrag verfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="f8609-109">The following describes how to track linked items on a firm planned production order.</span></span> <span data-ttu-id="f8609-110">Die Schritte sind für alle anderen Auftragsarten und der Planungsvorschlagszeilen ähnlich.</span><span class="sxs-lookup"><span data-stu-id="f8609-110">The steps are similar for all other order types, and from planning worksheet lines.</span></span>

1. <span data-ttu-id="f8609-111">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen") aus und geben Sie **Feste Auftragsplanung** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="f8609-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Firm Planned Prod. Order**, and then choose the related link.</span></span>
2. <span data-ttu-id="f8609-112">Öffnen Sie den relevanten fest geplanten Fertigungsauftrag in der Liste.</span><span class="sxs-lookup"><span data-stu-id="f8609-112">Open the relevant firm planned production order from the list.</span></span>
3. <span data-ttu-id="f8609-113">Wählen Sie im Inforegister **Zeilen** in Aktionen **Funktion** aus, und wählen Sie dann **Auftrag-Verfolgung**.</span><span class="sxs-lookup"><span data-stu-id="f8609-113">On the **Lines** FastTab, choose the **Functions** action, and then choose the **Order Tracking** action.</span></span>

<span data-ttu-id="f8609-114">In den Zeilen im Fenster  **Auftragsverfolgung**werden die Dokumente angezeigt, die sich auf die aktuelle Fertigungsauftragszeile beziehen.</span><span class="sxs-lookup"><span data-stu-id="f8609-114">The lines in the **Order Tracking** display the documents that are related to the current production order line.</span></span>

## <a name="untracked-planning-elements"></a><span data-ttu-id="f8609-115">Planungselemente ohne Bedarfsverursacher</span><span class="sxs-lookup"><span data-stu-id="f8609-115">Untracked Planning Elements</span></span>
<span data-ttu-id="f8609-116">Das Fenster **Planungselemente ohne Bedarfsverursacher** öffnet sich, wenn Sie das Feld **Mge. ohne Bedarfsverursacher** im Fenster **Auftragsplanung** auswählen.</span><span class="sxs-lookup"><span data-stu-id="f8609-116">The **Untracked Planning Elements** window opens when you choose the **Untracked Qty.** field in the **order Planning** window.</span></span> <span data-ttu-id="f8609-117">Er dient beiden Zwecken:</span><span class="sxs-lookup"><span data-stu-id="f8609-117">It serves two purposes:</span></span>

1. <span data-ttu-id="f8609-118">Sie enthält Informationen zu Mengen ohne Bedarfsverursacher, die angezeigt werden, wenn der Benutzer im Fenster "Bedarfsverursacher" Mengen ohne Bedarfsverursacher aufruft.</span><span class="sxs-lookup"><span data-stu-id="f8609-118">To hold information about untracked quantities displayed when the user looks up from the Order Tracking window to see untracked quantities.</span></span>
2. <span data-ttu-id="f8609-119">Sie enthält Warnmeldungen, die angezeigt werden, wenn der Benutzer im **Planungsvorschlag** auf ein **Warnungs**symbol klickt.</span><span class="sxs-lookup"><span data-stu-id="f8609-119">To hold warning messages displayed when the user chooses the **Warning** icon in the **Planning Worksheet** window.</span></span>

<span data-ttu-id="f8609-120">Die Tabelle enthält Posten, die eine Überschussmenge ohne Bedarfsverursacher im Bedarfsverursachernetzwerk ausweisen.</span><span class="sxs-lookup"><span data-stu-id="f8609-120">The window contains entries which account for an untracked surplus quantity in order tracking network.</span></span> <span data-ttu-id="f8609-121">Diese Posten werden während der Planung erzeugt und zeigen die Herkunft der Überschussmenge ohne Bedarfsverursacher in den Bedarfsverursacherzeilen.</span><span class="sxs-lookup"><span data-stu-id="f8609-121">These entries are generated during the planning run and explain where the untracked surplus quantity in the order tracking lines came from.</span></span> <span data-ttu-id="f8609-122">Die folgende Herkunft ist für den Überschuss ohne Bedarfsverursacher möglich:</span><span class="sxs-lookup"><span data-stu-id="f8609-122">This untracked surplus can come from:</span></span>

- <span data-ttu-id="f8609-123">Absatzplanung</span><span class="sxs-lookup"><span data-stu-id="f8609-123">Production forecast</span></span>
- <span data-ttu-id="f8609-124">Rahmenbestellungen</span><span class="sxs-lookup"><span data-stu-id="f8609-124">Blanket orders</span></span>
- <span data-ttu-id="f8609-125">Sicherheitsbestand</span><span class="sxs-lookup"><span data-stu-id="f8609-125">Safety stock quantity</span></span>
- <span data-ttu-id="f8609-126">Minimalbestand</span><span class="sxs-lookup"><span data-stu-id="f8609-126">Reorder point</span></span>
- <span data-ttu-id="f8609-127">Maximalbestand</span><span class="sxs-lookup"><span data-stu-id="f8609-127">Maximum inventory</span></span>
- <span data-ttu-id="f8609-128">Bestellmenge</span><span class="sxs-lookup"><span data-stu-id="f8609-128">Reorder quantity</span></span>
- <span data-ttu-id="f8609-129">Maximale Losgröße</span><span class="sxs-lookup"><span data-stu-id="f8609-129">Maximum order quantity</span></span>
- <span data-ttu-id="f8609-130">Minimale Losgröße</span><span class="sxs-lookup"><span data-stu-id="f8609-130">Minimum order quantity</span></span>
- <span data-ttu-id="f8609-131">Losgrößenrundungsfaktor</span><span class="sxs-lookup"><span data-stu-id="f8609-131">Order multiple</span></span>
- <span data-ttu-id="f8609-132">Toleranz (% der Losgröße)</span><span class="sxs-lookup"><span data-stu-id="f8609-132">Dampener (% of lot size)</span></span>

## <a name="see-also"></a><span data-ttu-id="f8609-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8609-133">See Also</span></span>  
<span data-ttu-id="f8609-134">[Planung](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="f8609-134">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="f8609-135">Produktion einrichten</span><span class="sxs-lookup"><span data-stu-id="f8609-135">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="f8609-136">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="f8609-136">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="f8609-137">Lagerbest</span><span class="sxs-lookup"><span data-stu-id="f8609-137">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="f8609-138">Einkauf</span><span class="sxs-lookup"><span data-stu-id="f8609-138">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="f8609-139">Designdetails: Reservierung, Auftragsnachverfolgung und Aktionsmeldungen</span><span class="sxs-lookup"><span data-stu-id="f8609-139">Design Details: Reservation, Tracking, and Action Messaging</span></span>](design-details-reservation-order-tracking-and-action-messaging.md)  
<span data-ttu-id="f8609-140">[Designdetails: Vorratsplanung](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="f8609-140">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="f8609-141">Bewährte Einrichtungsmethoden: Beschaffungsplanung</span><span class="sxs-lookup"><span data-stu-id="f8609-141">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="f8609-142">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f8609-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
