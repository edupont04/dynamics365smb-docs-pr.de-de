---
title: Inventurauftragszeilen mit Artikelverfolgungszeilen
description: "Artikelverfolgungszeilen werden verwendet, um Seriennummern und Chargennummern für Inventurauftragszeilen einzugeben."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f551de570b47057a6f4af6469e51a86fb3d02f32
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="physical-inventory-order-lines-with-item-tracking-lines"></a>Inventurauftragszeilen mit Artikelverfolgungszeilen
Artikelverfolgungszeilen werden verwendet, um Seriennummern und Chargennummern für Inventurauftragszeilen einzugeben.  

 Die Anwendung berücksichtigt Artikelverfolgungszeilen nur dann, wenn das Kontrollkästchen  Verfolgungszeilen verwenden der Inventurauftragszeile aktiviert ist.  

 Diese Option wird je nach Einstellung für den Artikelverfolgungscode in der Artikeltabelle automatisch durch die Anwendung aktiviert. Sie können das Kontrollkästchen auch manuell aktivieren oder deaktivieren. Eine Aktivierung ist jedoch nur dann möglich, wenn der Artikel in der aktuellen Inventurauftragszeile ausschließlich unter Verwendung von Seriennummern oder Chargennummern gebucht wurde.  

 Wenn dieses Kontrollkästchen aktiviert ist, können sich Verfolgungsinformationen an drei Stellen innerhalb der Anwendung befinden:  

-   Erwartete Artikelverfolgungszeilen  

-   Zählmengen mit Seriennummern und Chargennummern in der Inventurerfassungszeile  

-   Zu buchende Artikelverfolgungszeilen  

 **Erwartete Verfolgungszeilen:**  

 Wenn die Anwendung das Feld Erwartete Menge (Basis) in der Inventurauftragszeile berechnen soll, wird für den aktuellen Artikel auch eine Liste der Mengen mit Seriennummern und Chargennummern berechnet, die am Lager verfügbar sein sollten.  

 Das Programm umfasst die Berechnung aller Artikelposten, die bis zum Buchungsdatum des Inventurauftragskopfes gebucht worden sind und die in den 4 Feldern Artikelnr., Variantencode,  Lagerortcode und Lagerplatzcode in der Inventurauftragszeile die gleichen Werte aufweisen.  

 Sie können die erwarteten Verfolgungszeilen für die aktuelle Inventurauftragszeile anzeigen. Klicken Sie auf **Zeile**, **Artikelverfolgungszeilen**, **Erwartete Verfolgungszeilen**. Das Fenster Erw. Inventurverfolg. Titelliste wird geöffnet.  

 **Seriennummer/Chargennummer in der Inventurerfassungszeile:**  

 Wenn bei der Inventurerfassung erfasste Mengen eingegeben wurden, können auch Seriennummern und Chargennummern eingegeben werden. Nach Abschluss der Inventurerfassung weist die Anwendung die Inventurerfassungszeilen mit Seriennummern/Chargennummern Inventurauftragszeilen zu.  

 Sie können die erwarteten Verfolgungszeilen für die aktuelle Inventurauftragszeile anzeigen. Klicken Sie auf **Zeile**, **Erfassungszeilen**. Das Fenster " Inventurerfassungszeilen. Erst. Die Erfassung von Zeilen wird geöffnet.  

 **Zu buchende Artikelverfolgungszeilen:**  

 Beim Abschluss des Inventurauftrags vergleicht die Anwendung die erwartete Menge und die erfasste (gezählte) Menge und berechnet die Abweichung. Beim Abschluss des Inventurauftrags vergleicht die Anwendung die erwartete Menge und die erfasste (gezählte) Menge und berechnet die Abweichung. Wenn die Anwendung auch Artikelverfolgungszeilen berücksichtigen soll (das Kontrollkästchen  Verfolgungszeilen verwenden der Inventurerfassungszeile ist aktiviert), berechnet die Anwendung auch die Differenzen zwischen erwarteten Seriennummern und Chargennummern und erfassten Seriennummern und Chargennummern. Die Liste der berechneten Differenzen wird von der Anwendung beim Buchen des Inventurauftrags verwendet.  

 Sie können die erwarteten Verfolgungselemente für die aktuelle Inventurauftragszeile anzeigen. Klicken Sie auf **Zeile**, **Artikelverfolgungszeilen**, **Erwartete Verfolgungszeilen Differenzen**. Das Fenster **Erw. Inventurverfolg. Titelliste** wird geöffnet.  

 Weitere Informationen finden Sie unter [Beispiel - Inventurauftragszeile mit Nachverfolgungszeilen](example-inventory-order-line-with-tracking-lines.md).  

 Wenn der Bericht Inventurauftr.-Diff.-Übersicht für die Inventurauftragszeilen gedruckt wird, können Sie bei Bedarf ebenfalls die Artikelverfolgungszeilen ausgeben lassen.  

## <a name="see-also"></a>Siehe auch  
 [Physische Inventuraufträge eingeben](how-to-enter-physical-inventory-orders.md)   
 [Berechnen der verfügbaren Menge für einen Inventurauftrag](how-to-calculate-quantity-on-hand-for-a-physical-inventory-order.md)   
 [Inventurerfassung – Inventurzählung](physical-inventory-recording-counting-physical-inventory.md)   
 [So schließen Sie eine Inventurerfassung ab](how-to-finish-a-physical-inventory-recording.md)   
 [So schließen Sie einen Inventurauftrag ab](how-to-finish-a-physical-inventory-order.md)   
 [Vorgehensweise beim Analysieren von Inventurdifferenzen](how-to-analyze-physical-inventory-differences.md)
