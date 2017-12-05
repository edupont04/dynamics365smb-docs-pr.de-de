---
title: 'Designdetails: Erwartete Kostenbuchung | Microsoft Docs'
description: "Soll-Kosten repräsentieren die Schätzung der Kosten, z. B. für die Kosten eines Einkaufsartikels, die Sie registrieren, bevor Sie die Rechnung für den Artikel erhalten."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: eae1608b8768771759ac717c59606c930472d261
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-expected-cost-posting"></a><span data-ttu-id="5229c-103">Designdetails: Soll-Kosten-Buchen</span><span class="sxs-lookup"><span data-stu-id="5229c-103">Design Details: Expected Cost Posting</span></span>
<span data-ttu-id="5229c-104">Soll-Kosten repräsentieren die Schätzung der Kosten, z. B. für die Kosten eines Einkaufsartikels, die Sie registrieren, bevor Sie die Rechnung für den Artikel erhalten.</span><span class="sxs-lookup"><span data-stu-id="5229c-104">Expected costs represent the estimation of, for example, a purchased item’s cost that you record before you receive the invoice for the item.</span></span>  

 <span data-ttu-id="5229c-105">Sie können Soll-Kosten buchen, um sowie Fibu-Posten in den Lagerbestand zurückgeführt.</span><span class="sxs-lookup"><span data-stu-id="5229c-105">You can post expected cost to inventory and to the general ledger.</span></span> <span data-ttu-id="5229c-106">Wenn Sie eine Menge buchen, die nur erhalten oder geliefert, aber nicht fakturiert wurde, kann ein Wertposten mit den Soll-Kosten erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5229c-106">When you post a quantity that is only received or shipped but not invoiced, then a value entry is created with the expected cost.</span></span> <span data-ttu-id="5229c-107">Diese Soll-Kosten beeinflussen den Lagerwert, werden aber nicht in der Finanzbuchhaltung gebucht, es sei denn, das System wird entsprechend eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="5229c-107">This expected cost affects the inventory value, but is not posted to the general ledger unless you set up the system up to do so.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="5229c-108">Soll-Kosten werden nur für Artikeltransaktionen verwaltet.</span><span class="sxs-lookup"><span data-stu-id="5229c-108">Expected costs are only managed for item transactions.</span></span> <span data-ttu-id="5229c-109">Soll-Kosten sind nicht für immaterielle Transaktionstypen, wie etwa Kapazität und Artikel Zu-/Abschläge.</span><span class="sxs-lookup"><span data-stu-id="5229c-109">Expected costs are not for immaterial transaction types, such as capacity and item charges.</span></span>  

 <span data-ttu-id="5229c-110">Wenn nur der Mengenteil eine Bestandserhöhung gebucht wurde, dann ändert sich der Lagerwert in der Finanzbuchhaltung nicht, es sei denn, Sie haben das Kontrollkästchen E**rwartete Soll-Kosten buchen** im Fenster **Bestand einrichten** ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="5229c-110">If only the quantity part of an inventory increase has been posted, then the inventory value in the general ledger does not change unless you have selected the **Expected Cost Posting to G/L** check box in the **Inventory Setup** window.</span></span> <span data-ttu-id="5229c-111">In diesem Fall werden die Soll-Kosten auf Interimskonten zum Zeitpunkt des Wareneingangs gebucht.</span><span class="sxs-lookup"><span data-stu-id="5229c-111">In that case, the expected cost is posted to interim accounts at the time of receipt.</span></span> <span data-ttu-id="5229c-112">Nachdem der Wareneingang vollständig fakturiert wurde, werden die Interimskonten ausgeglichen und die Ist-Kosten werden im Lagerkonto gebucht.</span><span class="sxs-lookup"><span data-stu-id="5229c-112">After the receipt has been fully invoiced, the interim accounts are then balanced and the actual cost is posted to the inventory account.</span></span>  

 <span data-ttu-id="5229c-113">Um Abstimmung und Verfolgbarkeit zu unterstützen, zeigt der fakturierte Wertposten den Soll-Kostenbetrag, der zum Ausgleichen der Interimskonten gebucht wurde.</span><span class="sxs-lookup"><span data-stu-id="5229c-113">To support reconciliation and traceability work, the invoiced value entry shows the expected cost amount that has been posted to balance the interim accounts.</span></span>  

## <a name="example"></a><span data-ttu-id="5229c-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5229c-114">Example</span></span>  
 <span data-ttu-id="5229c-115">Das folgende Beispiel zeigt erwartete Kosten an, wenn das Kontrollkästchen **Automatische Lagerbuchung** und das Kontrollkästchen **Erwartete Kostenbuchung** im Fenster **Lager Einrichtung** ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="5229c-115">The following example shows expected cost if the **Automatic Cost Posting** check box and the **Expected Cost Posting to G/L** check box are selected in the **Inventory Setup** window.</span></span>  

 <span data-ttu-id="5229c-116">Sie buchen eine Einkaufsbestellung als erhalten.</span><span class="sxs-lookup"><span data-stu-id="5229c-116">You post a purchase order as received.</span></span> <span data-ttu-id="5229c-117">Die erwarteten Kosten sind MW 95,00.</span><span class="sxs-lookup"><span data-stu-id="5229c-117">The expected cost is LCY 95.00.</span></span>  

 <span data-ttu-id="5229c-118">**Wertposten**</span><span class="sxs-lookup"><span data-stu-id="5229c-118">**Value Entries**</span></span>  

|<span data-ttu-id="5229c-119">Buchungsdatum</span><span class="sxs-lookup"><span data-stu-id="5229c-119">Posting Date</span></span>|<span data-ttu-id="5229c-120">Postentyp</span><span class="sxs-lookup"><span data-stu-id="5229c-120">Entry Type</span></span>|<span data-ttu-id="5229c-121">Einstandsbetrag (erwartet)</span><span class="sxs-lookup"><span data-stu-id="5229c-121">Cost Amount (Expected)</span></span>|<span data-ttu-id="5229c-122">Auf Sachkonto geb. Soll-Kosten</span><span class="sxs-lookup"><span data-stu-id="5229c-122">Expected Cost Posted to G/L</span></span>|<span data-ttu-id="5229c-123">Soll-Kosten</span><span class="sxs-lookup"><span data-stu-id="5229c-123">Expected Cost</span></span>|<span data-ttu-id="5229c-124">Artikelposten Lfd. Nr.</span><span class="sxs-lookup"><span data-stu-id="5229c-124">Item Ledger Entry No.</span></span>|<span data-ttu-id="5229c-125">Lfd. Nr.</span><span class="sxs-lookup"><span data-stu-id="5229c-125">Entry No.</span></span>|  
|------------------|----------------|------------------------------|----------------------------------|-------------------|---------------------------|---------------|  
|<span data-ttu-id="5229c-126">01-01-20</span><span class="sxs-lookup"><span data-stu-id="5229c-126">01-01-20</span></span>|<span data-ttu-id="5229c-127">EK-Preis</span><span class="sxs-lookup"><span data-stu-id="5229c-127">Direct Cost</span></span>|<span data-ttu-id="5229c-128">95.00</span><span class="sxs-lookup"><span data-stu-id="5229c-128">95.00</span></span>|<span data-ttu-id="5229c-129">95.00</span><span class="sxs-lookup"><span data-stu-id="5229c-129">95.00</span></span>|<span data-ttu-id="5229c-130">Ja</span><span class="sxs-lookup"><span data-stu-id="5229c-130">Yes</span></span>|<span data-ttu-id="5229c-131">1</span><span class="sxs-lookup"><span data-stu-id="5229c-131">1</span></span>|<span data-ttu-id="5229c-132">1</span><span class="sxs-lookup"><span data-stu-id="5229c-132">1</span></span>|  

 <span data-ttu-id="5229c-133">**Relationsposten im Sachkonto – Tabelle Artikelpostenrelation**</span><span class="sxs-lookup"><span data-stu-id="5229c-133">**Relation Entries in the G/L – Item Ledger Relation Table**</span></span>  

|<span data-ttu-id="5229c-134">Sachposten Lfd. Nr.</span><span class="sxs-lookup"><span data-stu-id="5229c-134">G/L Entry No.</span></span>|<span data-ttu-id="5229c-135">Wertposten Lfd. Nr.</span><span class="sxs-lookup"><span data-stu-id="5229c-135">Value Entry No.</span></span>|<span data-ttu-id="5229c-136">Fibujournalnr.</span><span class="sxs-lookup"><span data-stu-id="5229c-136">G/L Register No.</span></span>|  
|--------------------|---------------------|-----------------------|  
|<span data-ttu-id="5229c-137">1</span><span class="sxs-lookup"><span data-stu-id="5229c-137">1</span></span>|<span data-ttu-id="5229c-138">1</span><span class="sxs-lookup"><span data-stu-id="5229c-138">1</span></span>|<span data-ttu-id="5229c-139">1</span><span class="sxs-lookup"><span data-stu-id="5229c-139">1</span></span>|  
|<span data-ttu-id="5229c-140">2</span><span class="sxs-lookup"><span data-stu-id="5229c-140">2</span></span>|<span data-ttu-id="5229c-141">1</span><span class="sxs-lookup"><span data-stu-id="5229c-141">1</span></span>|<span data-ttu-id="5229c-142">1</span><span class="sxs-lookup"><span data-stu-id="5229c-142">1</span></span>|  

 <span data-ttu-id="5229c-143">**Sachposten**</span><span class="sxs-lookup"><span data-stu-id="5229c-143">**General Ledger Entries**</span></span>  

|<span data-ttu-id="5229c-144">Buchungsdatum</span><span class="sxs-lookup"><span data-stu-id="5229c-144">Posting Date</span></span>|<span data-ttu-id="5229c-145">Sachkonto</span><span class="sxs-lookup"><span data-stu-id="5229c-145">G/L Account</span></span>|<span data-ttu-id="5229c-146">Kontonr. (En-US-Demo)</span><span class="sxs-lookup"><span data-stu-id="5229c-146">Account No. (En-US Demo)</span></span>|<span data-ttu-id="5229c-147">Betrag</span><span class="sxs-lookup"><span data-stu-id="5229c-147">Amount</span></span>|<span data-ttu-id="5229c-148">Lfd. Nr.</span><span class="sxs-lookup"><span data-stu-id="5229c-148">Entry No.</span></span>|  
|------------------|------------------|---------------------------------|------------|---------------|  
|<span data-ttu-id="5229c-149">01-01-20</span><span class="sxs-lookup"><span data-stu-id="5229c-149">01-01-20</span></span>|<span data-ttu-id="5229c-150">Lagerzugangskonto (Interim)</span><span class="sxs-lookup"><span data-stu-id="5229c-150">Inventory Accrual Account (Interim)</span></span>|<span data-ttu-id="5229c-151">5530</span><span class="sxs-lookup"><span data-stu-id="5229c-151">5530</span></span>|<span data-ttu-id="5229c-152">-95.00</span><span class="sxs-lookup"><span data-stu-id="5229c-152">-95.00</span></span>|<span data-ttu-id="5229c-153">2</span><span class="sxs-lookup"><span data-stu-id="5229c-153">2</span></span>|  
|<span data-ttu-id="5229c-154">01-01-20</span><span class="sxs-lookup"><span data-stu-id="5229c-154">01-01-20</span></span>|<span data-ttu-id="5229c-155">Lagerkonto (Interim)</span><span class="sxs-lookup"><span data-stu-id="5229c-155">Inventory Account (Interim)</span></span>|<span data-ttu-id="5229c-156">2131</span><span class="sxs-lookup"><span data-stu-id="5229c-156">2131</span></span>|<span data-ttu-id="5229c-157">95.00</span><span class="sxs-lookup"><span data-stu-id="5229c-157">95.00</span></span>|<span data-ttu-id="5229c-158">1</span><span class="sxs-lookup"><span data-stu-id="5229c-158">1</span></span>|  

 <span data-ttu-id="5229c-159">Sie können die Einkaufsbestellung sofort oder zu einem späteren Zeitpunkt buchen.</span><span class="sxs-lookup"><span data-stu-id="5229c-159">At a later date, you post the purchase order as invoiced.</span></span> <span data-ttu-id="5229c-160">Die fakturierten Kosten sind MW 100,00.</span><span class="sxs-lookup"><span data-stu-id="5229c-160">The invoiced cost is LCY 100.00.</span></span>  

 <span data-ttu-id="5229c-161">**Wertposten**</span><span class="sxs-lookup"><span data-stu-id="5229c-161">**Value Entries**</span></span>  

|<span data-ttu-id="5229c-162">Buchungsdatum</span><span class="sxs-lookup"><span data-stu-id="5229c-162">Posting Date</span></span>|<span data-ttu-id="5229c-163">Einstandsbetrag (tatsächl.)</span><span class="sxs-lookup"><span data-stu-id="5229c-163">Cost Amount (Actual)</span></span>|<span data-ttu-id="5229c-164">Einstandsbetrag (erwartet)</span><span class="sxs-lookup"><span data-stu-id="5229c-164">Cost Amount (Expected)</span></span>|<span data-ttu-id="5229c-165">Gebuchte Lagerregulierung an G/L</span><span class="sxs-lookup"><span data-stu-id="5229c-165">Cost Posted to G/L</span></span>|<span data-ttu-id="5229c-166">Soll-Kosten</span><span class="sxs-lookup"><span data-stu-id="5229c-166">Expected Cost</span></span>|<span data-ttu-id="5229c-167">Artikelposten Lfd. Nr.</span><span class="sxs-lookup"><span data-stu-id="5229c-167">Item Ledger Entry No.</span></span>|<span data-ttu-id="5229c-168">Lfd. Nr.</span><span class="sxs-lookup"><span data-stu-id="5229c-168">Entry No.</span></span>|  
|------------------|----------------------------|------------------------------|-------------------------|-------------------|---------------------------|---------------|  
|<span data-ttu-id="5229c-169">01-15-20</span><span class="sxs-lookup"><span data-stu-id="5229c-169">01-15-20</span></span>|<span data-ttu-id="5229c-170">100.00</span><span class="sxs-lookup"><span data-stu-id="5229c-170">100.00</span></span>|<span data-ttu-id="5229c-171">-95.00</span><span class="sxs-lookup"><span data-stu-id="5229c-171">-95.00</span></span>|<span data-ttu-id="5229c-172">100.00</span><span class="sxs-lookup"><span data-stu-id="5229c-172">100.00</span></span>|<span data-ttu-id="5229c-173">Nein</span><span class="sxs-lookup"><span data-stu-id="5229c-173">No</span></span>|<span data-ttu-id="5229c-174">1</span><span class="sxs-lookup"><span data-stu-id="5229c-174">1</span></span>|<span data-ttu-id="5229c-175">2</span><span class="sxs-lookup"><span data-stu-id="5229c-175">2</span></span>|  

 <span data-ttu-id="5229c-176">**Relationsposten im Sachkonto – Tabelle Artikelpostenrelation**</span><span class="sxs-lookup"><span data-stu-id="5229c-176">**Relation Entries in the G/L – Item Ledger Relation Table**</span></span>  

|<span data-ttu-id="5229c-177">Sachposten Lfd. Nr.</span><span class="sxs-lookup"><span data-stu-id="5229c-177">G/L Entry No.</span></span>|<span data-ttu-id="5229c-178">Wertposten Lfd. Nr.</span><span class="sxs-lookup"><span data-stu-id="5229c-178">Value Entry No.</span></span>|<span data-ttu-id="5229c-179">Fibujournalnr.</span><span class="sxs-lookup"><span data-stu-id="5229c-179">G/L Register No.</span></span>|  
|--------------------|---------------------|-----------------------|  
|<span data-ttu-id="5229c-180">3</span><span class="sxs-lookup"><span data-stu-id="5229c-180">3</span></span>|<span data-ttu-id="5229c-181">2</span><span class="sxs-lookup"><span data-stu-id="5229c-181">2</span></span>|<span data-ttu-id="5229c-182">2</span><span class="sxs-lookup"><span data-stu-id="5229c-182">2</span></span>|  
|<span data-ttu-id="5229c-183">4</span><span class="sxs-lookup"><span data-stu-id="5229c-183">4</span></span>|<span data-ttu-id="5229c-184">2</span><span class="sxs-lookup"><span data-stu-id="5229c-184">2</span></span>|<span data-ttu-id="5229c-185">2</span><span class="sxs-lookup"><span data-stu-id="5229c-185">2</span></span>|  
|<span data-ttu-id="5229c-186">5</span><span class="sxs-lookup"><span data-stu-id="5229c-186">5</span></span>|<span data-ttu-id="5229c-187">2</span><span class="sxs-lookup"><span data-stu-id="5229c-187">2</span></span>|<span data-ttu-id="5229c-188">2</span><span class="sxs-lookup"><span data-stu-id="5229c-188">2</span></span>|  
|<span data-ttu-id="5229c-189">6</span><span class="sxs-lookup"><span data-stu-id="5229c-189">6</span></span>|<span data-ttu-id="5229c-190">2</span><span class="sxs-lookup"><span data-stu-id="5229c-190">2</span></span>|<span data-ttu-id="5229c-191">2</span><span class="sxs-lookup"><span data-stu-id="5229c-191">2</span></span>|  

 <span data-ttu-id="5229c-192">**Sachposten**</span><span class="sxs-lookup"><span data-stu-id="5229c-192">**General Ledger Entries**</span></span>  

|<span data-ttu-id="5229c-193">Buchungsdatum</span><span class="sxs-lookup"><span data-stu-id="5229c-193">Posting Date</span></span>|<span data-ttu-id="5229c-194">Sachkonto</span><span class="sxs-lookup"><span data-stu-id="5229c-194">G/L Account</span></span>|<span data-ttu-id="5229c-195">Kontonr. (En-US-Demo)</span><span class="sxs-lookup"><span data-stu-id="5229c-195">Account No. (En-US Demo)</span></span>|<span data-ttu-id="5229c-196">Betrag</span><span class="sxs-lookup"><span data-stu-id="5229c-196">Amount</span></span>|<span data-ttu-id="5229c-197">Lfd. Nr.</span><span class="sxs-lookup"><span data-stu-id="5229c-197">Entry No.</span></span>|  
|------------------|------------------|---------------------------------|------------|---------------|  
|<span data-ttu-id="5229c-198">01-15-20</span><span class="sxs-lookup"><span data-stu-id="5229c-198">01-15-20</span></span>|<span data-ttu-id="5229c-199">Lagerzugangskonto (Interim)</span><span class="sxs-lookup"><span data-stu-id="5229c-199">Inventory Accrual Account (Interim)</span></span>|<span data-ttu-id="5229c-200">5530</span><span class="sxs-lookup"><span data-stu-id="5229c-200">5530</span></span>|<span data-ttu-id="5229c-201">95.00</span><span class="sxs-lookup"><span data-stu-id="5229c-201">95.00</span></span>|<span data-ttu-id="5229c-202">4</span><span class="sxs-lookup"><span data-stu-id="5229c-202">4</span></span>|  
|<span data-ttu-id="5229c-203">01-15-20</span><span class="sxs-lookup"><span data-stu-id="5229c-203">01-15-20</span></span>|<span data-ttu-id="5229c-204">Lagerkonto (Interim)</span><span class="sxs-lookup"><span data-stu-id="5229c-204">Inventory Account (Interim)</span></span>|<span data-ttu-id="5229c-205">2131</span><span class="sxs-lookup"><span data-stu-id="5229c-205">2131</span></span>|<span data-ttu-id="5229c-206">-95.00</span><span class="sxs-lookup"><span data-stu-id="5229c-206">-95.00</span></span>|<span data-ttu-id="5229c-207">3</span><span class="sxs-lookup"><span data-stu-id="5229c-207">3</span></span>|  
|<span data-ttu-id="5229c-208">01-15-20</span><span class="sxs-lookup"><span data-stu-id="5229c-208">01-15-20</span></span>|<span data-ttu-id="5229c-209">Direkte Kosten Verrech.-Konto</span><span class="sxs-lookup"><span data-stu-id="5229c-209">Direct Cost Applied Account</span></span>|<span data-ttu-id="5229c-210">7291</span><span class="sxs-lookup"><span data-stu-id="5229c-210">7291</span></span>|<span data-ttu-id="5229c-211">-100</span><span class="sxs-lookup"><span data-stu-id="5229c-211">-100</span></span>|<span data-ttu-id="5229c-212">6</span><span class="sxs-lookup"><span data-stu-id="5229c-212">6</span></span>|  
|<span data-ttu-id="5229c-213">01-15-20</span><span class="sxs-lookup"><span data-stu-id="5229c-213">01-15-20</span></span>|<span data-ttu-id="5229c-214">Lagerkonto</span><span class="sxs-lookup"><span data-stu-id="5229c-214">Inventory Account</span></span>|<span data-ttu-id="5229c-215">2130</span><span class="sxs-lookup"><span data-stu-id="5229c-215">2130</span></span>|<span data-ttu-id="5229c-216">100</span><span class="sxs-lookup"><span data-stu-id="5229c-216">100</span></span>|<span data-ttu-id="5229c-217">5</span><span class="sxs-lookup"><span data-stu-id="5229c-217">5</span></span>|  

## <a name="see-also"></a><span data-ttu-id="5229c-218">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5229c-218">See Also</span></span>
 <span data-ttu-id="5229c-219">[Designdetails: Lagerkostenberechnung](design-details-inventory-costing.md) </span><span class="sxs-lookup"><span data-stu-id="5229c-219">[Design Details: Inventory Costing](design-details-inventory-costing.md) </span></span>  
 <span data-ttu-id="5229c-220">[Designdetails: Kostenregulierung](design-details-cost-adjustment.md) </span><span class="sxs-lookup"><span data-stu-id="5229c-220">[Design Details: Cost Adjustment](design-details-cost-adjustment.md) </span></span>  
 <span data-ttu-id="5229c-221">[Designdetails: Abgleich mit der Finanzbuchhaltung](design-details-reconciliation-with-the-general-ledger.md) </span><span class="sxs-lookup"><span data-stu-id="5229c-221">[Design Details: Reconciliation with the General Ledger](design-details-reconciliation-with-the-general-ledger.md) </span></span>  
 <span data-ttu-id="5229c-222">[Designdetails: Bestandsbuchung](design-details-inventory-posting.md) </span><span class="sxs-lookup"><span data-stu-id="5229c-222">[Design Details: Inventory Posting](design-details-inventory-posting.md) </span></span>  
 [<span data-ttu-id="5229c-223">Designdetails: Abweichung</span><span class="sxs-lookup"><span data-stu-id="5229c-223">Design Details: Variance</span></span>](design-details-variance.md)  
 [<span data-ttu-id="5229c-224">Verwalten der Lagerregulierung</span><span class="sxs-lookup"><span data-stu-id="5229c-224">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
 [<span data-ttu-id="5229c-225">Finanzen</span><span class="sxs-lookup"><span data-stu-id="5229c-225">Finance</span></span>](finance.md)  
 <span data-ttu-id="5229c-226">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5229c-226">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
