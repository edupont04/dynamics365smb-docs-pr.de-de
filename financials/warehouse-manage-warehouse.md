---
title: "Lageraktivitäten | Microsoft Docs"
description: "Nach dem Eingang und vor der Lieferung von Waren finden einige interne Lageraktivitäten statt, um einen effektiven Ablauf im Lager zu gewährleisten und um den Lagerbestand des Unternehmens zu organisieren und zu verwalten."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 5aa3728aa5658f61fd5bb094c7274405f6f9daa2
ms.contentlocale: de-de
ms.lasthandoff: 01/30/2018

---
# <a name="warehouse-management"></a>Logistik
Nach dem Eingang und vor der Lieferung von Waren finden einige interne Lageraktivitäten statt, um einen effektiven Ablauf im Lager zu gewährleisten und um den Lagerbestand des Unternehmens zu organisieren und zu verwalten.

Zu den typischen Lageraktivitäten gehören das Einlagern von Artikeln, das Umlagern von Artikeln in Lagern oder zwischen Lagern und die Kommissionierung von Artikeln für die Montage, Produktion oder Lieferung. Die Montage von Artikeln für Verkäufe oder Lager gilt auch als Lageraktivität, doch diese werden an anderer Stelle behandelt. Weitere Informationen finden Sie unter [Montageverwaltung](assembly-assemble-items.md).  

In großen Lagern können diese unterschiedlichen Aufgaben nach Abteilungen getrennt sein und die Integration kann durch einen gesteuerten Workflow verwaltet werden. In einfacheren Installationen ist der Auftragsfluss weniger formalisiert und die Lageraktivitäten werden mit sogenannten Lagerbestandseinlagerungen und -kommissionierungen durchgeführt. Weitere Informationen über grundlegende und erweiterte Lagerkonfigurationen finden Sie unter [Designdetails: Logistik Übersicht](design-details-warehouse-overview.md).

Bevor Sie Lageraktivitäten ausführen können, müssen Sie das System für die relevante Komplexität der Lagerverarbeitung einrichten. Weitere Informationen finden Sie unter [Lagerortverwaltung einrichten](warehouse-setup-warehouse.md).

 Die folgende Tabelle enthält eine Abfolge von Aufgaben sowie Links zu den entsprechenden Themen, in denen diese Aufgaben erläutert werden.   

|**Aufgabe**|**Siehe**|  
|------------|-------------|  
|Erfassen Sie den Eingang von Artikeln an Lagerorten, entweder mit nur einer Einkaufsbestellung, in einfachen Lagerorteinrichtungen oder mit einem Wareneingang, im Falle von halb- oder vollautomatisierter Lagerverarbeitung am Lagerort.|[Empfangen von Artikeln](warehouse-how-receive-items.md)|
|Umgehen Sie die Einlagerungs- und Kommissionierungsvorgänge, um einen Artikel direkt vom Wareneingang oder der Fertigung zum Versenden zu beschleunigen.|[Zuordnungselemente](warehouse-how-to-cross-dock-items.md)|    
|Lagern Sie Artikel ein, die bei Einkäufen, Verkaufsrücksendungen, Umlagerungen oder Fertigerzeugnissen eingehen, gemäß dem konfigurierten Lageraktivitätsvorgang ein.|[Einlagerung von Artikeln](warehouse-put-away-items.md)|
|Lagern Sie Artikel zwischen Lagerplätzen in dem Lager um.|[Umlagern von Artikeln](warehouse-move-items.md)|
|Kommissionieren Sie Artikel, die geliefert, umgelagert oder bei der Montage bzw. Produktion verbraucht werden, gemäß dem konfigurierten Lageraktivitätsvorgang.|[Kommissionieren von Artikeln](warehouse-pick-items.md)|
|Erfassen Sie die Lieferung von Artikeln aus Lagerorten, entweder mit nur einem Verkaufsauftrag, in einfachen Lagerorteinrichtungen oder mit einem Warenausgang, im Falle von halb- oder vollautomatisierter Lagerverarbeitung am Lagerort.|[Versenden von Artikeln](warehouse-how-ship-items.md)|  

## <a name="see-also"></a>Siehe auch  
[Lagerbest](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]
