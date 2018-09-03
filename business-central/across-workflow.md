---
title: Workflow | Microsoft Docs
description: "Sie können Workflows einrichten und verwenden, die Geschäftsprozessaufgaben von verschiedenen Benutzern verbinden. Systemaufgaben, wie automatische Buchung, können als Schritte in Workflows berücksichtigt werden, vor oder nach Benutzeraufgaben. Die Anforderung oder Bewilligung von Genehmigungen zum Erstellen neuer Datensätze sind typische Workflowschritte."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 05/09/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 75501b9402bb1c14fcfeb2fc6e61f055a2247493
ms.openlocfilehash: 128d20233d1750b2b89c3c7e2de6e497bd32b342
ms.contentlocale: de-de
ms.lasthandoff: 05/15/2018

---
# <a name="workflow"></a>Workflow
Sie können Workflows einrichten und verwenden, die Geschäftsprozessaufgaben von verschiedenen Benutzern verbinden. Systemaufgaben, wie automatische Buchung, können als Schritte in Workflows berücksichtigt werden, vor oder nach Benutzeraufgaben. Die Anforderung oder Bewilligung von Genehmigungen zum Erstellen neuer Datensätze sind typische Workflowschritte.  

 Im Fenster **Workflow** können Sie einen Workflow erstellen, indem Sie die entsprechenden Schritte in den Zeilen auflisten. Jeder Schritt besteht aus einem durch Ereignisbedingungen moderiertem Workflowereignis und einer durch Antwortoptionen moderierten Workflowantwort. Sie definieren Workflowschritte, indem Sie die Felder in Workflowzeilen mit Ereignis- und Antwortwerten aus festen Listen ausfüllen, die die Workflowszenarien darstellen, die durch den Anwendungscode unterstützt werden.  

 Die generische Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] umfasst mehrere vorkonfigurierte Workflows, für die Workflowvorlagen vorliegen. Diese können Sie kopieren, um Workflows zu erstellen. Dem Code für von Microsoft hinzugefügte Workflowvorlagen ist „MS-“ vorangestellt. Weitere Informationen finden Sie in der Liste mit Workflowvorlagen im Fenster Workflow-Vorlagen  

 Wenn ein Szenario ein Workflowereignis oder -antwort benötigt, die nicht unterstützt wird, muss ein Microsoft-Partner diese implementieren, indem er den Anwendungscode anpasst. Weitere Informationen finden Sie unter [Exemplarische Vorgehensweise: Implementieren von neuen Workflowereignissen und von Kampagnenreaktionen](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) in der Entwickler- und IT-Pro-Hilfe.

> [!NOTE]  
> Workflow können auch von Microsoft Flow initiert werden. Weitere Informationen finden Sie unter [Business Central in einem automatisierten Workflow nutzen](across-how-use-financials-data-source-flow.md).  

 In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.  

|**Aufgabe**|**Informationen**|  
|------------|-------------|  
|Richten Sie Workflowbenutzer ein, geben Sie an, wie Benutzer benachrichtigt werden, und erstellen Sie neue Workflows. Implementieren Sie für neue Workflow für nicht unterstützte Szenarien die erforderlichen Workflowelemente, indem Sie den Anwendungscode anpassen.|[Einrichten von Workflows](across-set-up-workflows.md)|  
|Aktivieren Sie Workflows, reagieren Sie auf Workflowbenachrichtigungen, einschließlich Anfragegenehmigungen und genehmigen Sie Anforderungen, um einen Workflowschritt auszuführen. Archivieren und löschen Sie Workflows.|[Verwenden von Workflows](across-use-workflows.md)|  

## <a name="see-also"></a>Siehe auch  
[Verkauf](sales-manage-sales.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Projekte verwalten](projects-manage-projects.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
