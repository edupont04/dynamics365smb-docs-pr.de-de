---
title: 'Designdetails: Artikelnachverfolgung im Lager | Microsoft Docs'
description: Der Umgang mit Serien- oder Chargennummern ist hauptsächlich eine Lageraufgabe; daher haben alle eingehenden und ausgehenden Lagerbelege Standardfunktionen für die Zuordnung und die Auswahl von Artikelverfolgungsnummern. Da das Reservierungssystem auf Artikelposten basiert, werden Lageraktivitätsbelege, die nur Lagerplatzposten erfassen, jedoch nicht vollständig unterstützt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, tracking, serial number, lot number, outbound documents
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 6ffce5d73eabe8586ac682f6d1a549993b1b6d2a
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3787546"
---
# <a name="design-details-item-tracking-in-the-warehouse"></a>Designdetails: Artikelverfolgung im Lager
Der Umgang mit Serien- oder Chargennummern ist hauptsächlich eine Lageraufgabe; daher haben alle eingehenden und ausgehenden Lagerbelege Standardfunktionen für die Zuordnung und die Auswahl von Artikelverfolgungsnummern.  

Da das Reservierungssystem auf Artikelposten basiert, werden Lageraktivitätsbelege, die nur Lagerplatzposten erfassen, jedoch nicht vollständig unterstützt. Da Reservierungen und Artikelverfolgungsnummern nur auf Lagerort- (und nicht auf Lagerplatz- oder Zonen-) Ebene bearbeitet werden können, kann die Seite **Artikelverfolgungszeilen** nicht aus den Lageraktivitätsbelegen heraus geöffnet werden. Dies gilt auch für die Seite **Reservierung**.  

Nachdem eine Serien- oder eine Chargennummer dem Bestand an einem Lagerort hinzugefügt wurde, kann sie verschoben und frei im Lager neuklassifiziert werden, indem eine unabhängige Artikelnachverfolgungsstruktur, die keine Beziehung zum Reservierungssystem hat, verwendet wird. Auf die Felder **Seriennr.** und **Chargennr.** wird direkt auf Logistikbelegzeilen zugegriffen. Wenn die Serien- oder Chargennummer später in der ausgehenden Buchung erscheint, wird sie mit dem Reservierungssystem als Teil einer gewöhnlichen Lagerplatzanpassung synchronisiert. Weitere Informationen finden Sie unter [Designdetails: Bestandintegration](design-details-integration-with-inventory.md).  

Das Reservierungssystem berücksichtigt jedoch Lageraktivitäten, wenn es die Verfügbarkeit berechnet. Beispielsweise können Artikel, die Kommissionierungen zugewiesen oder als kommissioniert registriert sind, nicht reserviert werden. Weitere Informationen finden Sie unter [Designdetails: Verfügbarkeit im Lager](design-details-availability-in-the-warehouse.md).

## <a name="see-also"></a>Siehe auch  
[Designdetails: Artikelnachverfolgung](design-details-item-tracking.md)  
[Designdetails: Integration mit dem Lagerbestand](design-details-integration-with-inventory.md)  
[Designdetails: Verfügbarkeit im Lager](design-details-availability-in-the-warehouse.md)  
[Designdetails: Artikelverfolgungsdesign](design-details-item-tracking-design.md)
