---
title: Kommissionierung und Lieferung in Basis-Lagerkonfigurationen | Microsoft Docs
description: In Business Central können die ausgehenden Prozesse für die Komissionierung und Lieferung auf vier Arten, mit den verschiedenen Funktionen, abhängig von der Lagerkomplexitätsebene, ausgeführt werden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2020
ms.author: edupont
ms.openlocfilehash: d607037d76f0778aa0f1037ac9540cfd3d497dbd
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3786821"
---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a>Exemplarische Vorgehensweise: Kommissionierung und Lieferung in Basis-Lagerkonfigurationen

[!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]

In [!INCLUDE[d365fin](includes/d365fin_md.md)] können die ausgehenden Prozesse für die Komissionierung und Lieferung auf vier Arten, mit den verschiedenen Funktionen, abhängig von der Lagerkomplexitätsebene, ausgeführt werden.  

|Art|Eingangsprozess|Lagerplätze|Kommissionierungen|Lieferungen|Komplexitätsebene anzeigen (siehe [Designdetails: Lagerhaus-Einrichtung](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Beitragsentnahme und -Lieferung aus der Auftragszeile|X|||2|  
|F|Buchen Sie die Kommissionierung und den Warenausgang aus einem Lagerkommissionierungsbeleg||X||3|  
|L|Buchen Sie die Kommissionierung und den Warenausgang aus einem Warenausgangsbeleg|||X|4/5/6|  
|T|Buchen Sie die Kommissionierung von einem Kommissionierbeleg und buchen Sie den Warenausgang aus einem Warenausgangsbeleg||X|X|4/5/6|  

Weitere Informationen finden Sie unter [Designdetails: Ausgehender Lagerfluss](design-details-outbound-warehouse-flow.md).  

In der folgenden Vorgehensweise wird Methode B in der vorhergegangenen Tabelle beschrieben.  

## <a name="about-this-walkthrough"></a>Informationen zu dieser exemplarischen Vorgehensweise

Bei Basis-Lagerkonfigurationen gilt Folgendes: Wenn ein Lagerort so eingerichtet wurde, dass Kommissionierung erforderlich ist, jedoch Warenausgang nicht erforderlich ist, verwenden Sie die Seite **Lagerkommissionierung**, um Kommissionier- und Warenausgangsinformationen für Ihre Herkunftsbelege zu erfassen und zu buchen. Der ausgehende Herkunftsbeleg kann ein Verkaufsauftrag, eine Einkaufsreklamation, ein ausgehender Umlagerungsauftrag, ein Fertigungsauftrag oder ein Komponentenbedarf sein.  

In dieser exemplarischen Vorgehensweise werden folgende Aufgaben erläutert:  

- Einrichtung des SILBERNEN Lagerorts für Lagerkommissionierung.  
- Erstellen eines Verkaufsauftrags für den Debitor 10000 für 30 Lautsprecher.  
- Freigeben des Verkaufsauftrags für Lagerdurchlaufzeit.  
- Erstellen einer Lagerkommissionierung basierend auf einem freigegebenen Herkunftsbeleg.  
- Erfassen der Lagerplatzumlagerung aus dem Lager und gleichzeitig Buchen der Verkaufslieferung für den ursprünglichen Verkaufsauftrag.  

## <a name="roles"></a>Rollen

Die Aufgaben in dieser Demonstration werden von den folgenden Benutzerrollen ausgeführt:  

- Lagerortleiter  
- Auftragsverarbeitung  
- Lagermitarbeiter  

## <a name="prerequisites"></a>Voraussetzungen

Für diese exemplarische Vorgehensweise gelten folgende Voraussetzungen:  

- Für [!INCLUDE[prodshort](includes/prodshort.md)] Online ein Unternehmen basierend auf der Option **Erweiterte Bewertung – Vollständige Beispieldaten** in einer Sandbox-Umgebung Für [!INCLUDE[prodshort](includes/prodshort.md)] (lokal) CRONUS International Ltd. installiert  
- Machen Sie sich selbst zum Lagerarbeiter am Standort SILVER, indem Sie die folgenden Schritte ausführen:  

  1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **Lagermitarbeiter** ein, und wählen Sie dann den entsprechenden Link.  
  2. Wählen Sie das Feld **Benutzer-ID** aus, und wählen Sie Ihr eigenes Benutzerkonto auf der Seite **Benutzer** aus.  
  3. Geben Sie im Feld **Lagerortcode** SILVER ein.  
  4. Wählen Sie das Feld **Standard** aus.  

- Stellen Sie Artikel LS-81 am SILBERNEN Lagerort bereit, indem Sie die folgenden Schritte ausführen:  

  1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **Artikel Buch.-Blätter** ein und wählen Sie dann den entsprechenden Link.  
  2. Öffnen Sie das Standardjournal, und erstellen Sie dann zwei Artikel Buch.-Blattzeilen mit den folgenden Informationen über das Arbeitsdatum (23. Januar).  

        |Postentyp|Artikelnummer|Lagerortcode|Lagerplatzcode|Menge|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |Zugang|LS-81|SILBER|S-01-0001|20|  
        |Zugang|LS-81|SILBER|S-01-0002|20|  

  3. Wählen Sie die Aktion **Beleg buchen** aus und wählen Sie dann die Schaltfläche **Ja** aus.  

## <a name="story"></a>Hintergrund

Ellen, die Lagermanagerin bei CRONUS, richtet das SILBER-Lager für grundlegende Komissionierungshandlung ein, in dem Lagermitarbeiter ausgehende Aufträge einzeln verarbeiten. Martha, die Verkaufsauftragsbearbeiterin, erstellt einen Verkaufsauftrag für 30 Einheiten des Artikels LS-81, die dem Debitor 10000 aus dem SILBERNEN Lager geliefert werden. John, der Lagermitarbeiter muss sicherstellen, dass die Lieferung an den Debitor vorbereitet und geliefert wird. John verwaltet alle beteiligten Aufgaben auf der Seite **Lagerkommissionierung**, das automatisch auf die Lagerplätze verweist, in denen LS-81 gespeichert wird.  

## <a name="setting-up-the-location"></a>Einrichten des Lagerorts

Das Einrichten der Seite **Standortkarte** definiert die Warenflüsse des Unternehmens.  

### <a name="to-set-up-the-location"></a>So richten Sie den Standort ein

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Lagerorte** ein und wählen Sie dann den entsprechenden Link.  
2. Öffnen Sie die Karte für den Standort SILVER.  
3. Aktivieren Sie im Inforegister **Lager** das Kontrollkästchen **Kommissionierung erforderlich**.  

## <a name="creating-the-sales-order"></a>Erstellen des Verkaufsauftrags

Verkaufsaufträge sind die häufigste Art des ausgehenden Herkunftsbelegs.  

### <a name="to-create-the-sales-order"></a>Den Verkaufsauftrag erstellen

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Tell Me-Funktion"), geben Sie **Verkaufsaufträge** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Neu** aus.  
3. Erstellen Sie einen Verkaufsauftrag für den Debitor 10000 auf das Arbeitsdatum (23. Januar) mit den folgenden Verkaufszeilen.  

    |Artikel|Lagerortcode|Menge|  
    |----|-------------|--------|  
    |LS_81|SILBER|30|  

     Fahren Sie fort, das Lager zu informieren, dass die Verkaufsbestellung in Lagerdurchlaufzeit bereit ist, wenn die Lieferung eingeht.  

4. Wählen Sie die Aktion **Freigabe** aus.  

    John fährt fort, die Verkaufsartikel zu kommissionieren und zu liefern.  

## <a name="picking-and-shipping-items"></a>Kommissionierung und Versand von Artikeln

Auf der Seite **Lagerkommissionierung** können Sie alle ausgehenden Lageraktivitäten für einen bestimmten Herkunftsbeleg, wie einen Verkauf, verwalten. [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

### <a name="to-pick-and-ship-items"></a>So kommissionieren Sie Artikel und liefern diese aus

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Lagerkommissionierungen** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Neu**.  

    Stellen Sie sicher, dass das Feld **Nr.** auf dem Inforegister **Allgemein** ausgefüllt ist.
3. Wählen Sie das Feld **Quellendokument** , und wählen Sie **Verkaufsauftrag** aus.  
4. Wählen Sie das Feld **Herkunftsnr.** aus, wählen Sie die Zeile für den Verkauf an Debitor 10000 aus, und wählen Sie dann die Schaltfläche **OK**.  

    Alternativ auf der Registerkarte Aktionen, in der Gruppe Funktion, wählen Sie **Herkunftsbeleg holen** und wählen Sie die Auftrag aus.  
5. Wählen Sie die Aktion **Die zu verarbeitende Menge automatisch ausfüllen**.  

    Alternativ im Feld **Menge zu verarbeiten** geben Sie 10 und 20 jeweils auf den zwei Lagerkommissionierzeilen ein.  
6. Wählen Sie die Aktion **Buchen** und **Versand** und klicken Sie anschließend auf die Schaltfläche **OK**.  

    Die 30 Lautsprecher werden nun erfasst, wie von den Lagerplätzen S-01-0001 und S-01-0002 kommissioniert, und ein negativer Artikelposten wird, die gebuchte Verkaufslieferung reflektierend, erstellt.  

## <a name="see-also"></a>Siehe auch

[Artikel mit der Lagerkommissionierung kommissionieren](warehouse-how-to-pick-items-with-inventory-picks.md)  
[Um Artikel für den Warenausgang zu kommissionieren](warehouse-how-to-pick-items-for-warehouse-shipment.md)  
[Einrichten von Basislagern mit Vorgangsbereichen](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[So verschieben Sie Komponenten in einen Arbeitsgangbereich in Basis-Lagerkonfigurationen](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  
[Kommissionierung für die Produktion oder Montage](warehouse-how-to-pick-for-production.md)  
[Ad-hoc-Umlagerung von Artikeln in Basis-Lagerkonfigurationen](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[Designdetails: Ausgehender Lagerfluss](design-details-outbound-warehouse-flow.md)  
[Exemplarische Vorgehensweisen für Geschäftsprozesse](walkthrough-business-process-walkthroughs.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
