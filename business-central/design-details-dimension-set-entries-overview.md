---
title: Dimensionssatzposten Übersicht | Microsoft Docs
description: In diesem Thema wird beschrieben, wie Dimensionssatzposten in Dynamics 365 gespeichert und gebucht werden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dimension
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: b9b69b539228e92776e1a7ee4c2fb491b20c1a15
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3787996"
---
# <a name="dimension-set-entries-overview"></a>Dimensionssatz-Eintrags-Übersicht
In diesem Thema wird beschrieben, wie Dimensionssatzposten in [!INCLUDE[d365fin](includes/d365fin_md.md)] gespeichert und gebucht werden.  

## <a name="dimension-sets"></a>Dimensionssätze  
Ein Dimensionssatz ist eine eindeutige Kombination von Dimensionswerten. Er wird als Dimensionssatzposten in die Datenbank gespeichert. Jeder Dimensionssatzposten stellt einen einzelnen Dimensionswert dar. Der Dimensionssatz wird durch eine allgemeine Dimensionssatz-ID identifiziert, die jedem Dimensionssatzposten zugewiesen wird, der zum Dimensionssatz gehört.  

Im folgenden Beispiel wird ein Dimensionssatz gezeigt, der drei Dimensionssatzposten aufweist. Der Dimensionssatz wird durch eine Dimensionssatz-ID, nämlich 108, identifiziert.  

|Dimensionssatz-ID|Dimensionscode|Dimensionswertcode|Dimensionswertname|  
|----------------------|--------------------|--------------------------|--------------------------|  
|108|BEREICH|70|Nordamerika|  
|108|UNTERNEHMENSGRUPPE|POS1|Start|  
|108|KOSTENSTELLE|VERKAUF|Verkauf|  

## <a name="dimension-set-entries"></a>Dimensionssatzposten  
Dimensionssätze werden in der Tabelle als **Dimensionssatzposten** mit derselben Dimensionssatz-ID gespeichert.  

![Fluss von Dimensionssatzeinträgen](media/dimensionentrynav7.png "Fluss der Dimensionssatzeinträge")  

Wenn Sie eine neue Buch.-Blattzeile, einen Belegkopf oder eine Belegzeile erstellen, können Sie eine Kombination von Dimensionswerten angeben. Anstatt jeden Dimensionswert explizit in der Datenbank zu speichern, wird eine Dimensionssatz-ID der Buch.-Blattzeile, dem Belegkopf oder der Belegzeile zugewiesen, um den Dimensionssatz anzugeben.  

Wenn Sie die Seite **Dimensionssatzeinträge bearbeiten**bearbeiten und schließen, wird eine Prüfung ausgeführt, um festzustellen, ob die Kombination aus Dimensionswerten als Dimensionssatz in der Tabelle existiert. Wenn die Kombination in der Tabelle auftritt, wird die entsprechende Dimensionssatz-ID der Buch.-Blattzeile, dem Belegkopf oder der Belegzeile zugeordnet. Andernfalls wird ein neuer Dimensionssatz der Tabelle hinzugefügt, und die neue Dimensionssatz-ID wird der Buch.-Blattzeile, dem Belegkopf oder der Belegzeile zugeordnet.

## <a name="codeunit-408-dimension-management"></a>Codeunit 408 Dimension Management
Codeunit 408 Dimension Management ist eine Funktionsbibliothek, die häufige Aufgaben im Zusammenhang mit Dimensionen behandelt, wie etwa das Kopieren von einer Tabelle zu einer anderen oder von einem Beleg zu einem anderen.

## <a name="performance-improvement"></a>Leistungsverbesserung  
Durch das einmalige Speichern von Dimensionssätzen in der Datenbank wird Datenbankplatz beibehalten und die Gesamtleistung verbessert.  

## <a name="see-also"></a>Siehe auch  
[Designdetails: Suche nach Dimensionskombinationen](design-details-searching-for-dimension-combinations.md)   
[Designdetails: Tabellenstruktur](design-details-table-structure.md)   
[Designdetails: Dimensionssatzeinträge](design-details-dimension-set-entries.md)   
