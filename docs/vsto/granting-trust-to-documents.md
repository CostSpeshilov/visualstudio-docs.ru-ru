---
title: Предоставить доверие к документам
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- security [Office development in Visual Studio], trust
- inclusion lists [Office development in Visual Studio], about inclusion lists
- trust [Office development in Visual Studio], 2007 Office system
- granting trust [Office development in Visual Studio]
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: aba47e277b1c109bf4b0d03efb5694733f45760c
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/24/2019
ms.locfileid: "54871888"
---
# <a name="grant-trust-to-documents"></a>Предоставить доверие к документам
  К проекту уровня документа предъявляются те же требования безопасности, что и к проектам уровня приложения. Это подписание манифестов сертификатом или подтверждение при запросе доверия. Кроме того, документ или книга должны быть расположены в каталоге, назначенном в качестве надежного расположения.  
  
 [!INCLUDE[appliesto_alldoc](../vsto/includes/appliesto-alldoc-md.md)]  
  
## <a name="trusted-locations"></a>Надежные расположения  
 Приложения в [!INCLUDE[Office_15_short](../vsto/includes/office-15-short-md.md)] и Office 2010 имеют центры управления безопасностью, где пользователи могут настраивать параметры безопасности и конфиденциальности, например надежные расположения. Для решений Office локальный компьютер считается надежного расположения. Однако из-за повышенного риска некоторые каталоги нельзя считать надежными. Это, например, временные системные папки для каждого пользователя и для браузера Internet Explorer.  
  
 Дополнительные сведения о центре управления безопасностью, см. в разделе [безопасности, политики и параметры в Office 2010](http://go.microsoft.com/fwlink/?LinkId=89202). Дополнительные сведения о том, как создание, управление, удаление и настройке надежных папок см. в разделе [Настройка надежных расположений и параметров доверенных издателей системы Office 2007](http://go.microsoft.com/fwlink/?LinkId=89203) и [создание, удаление или изменение Надежные расположения для файлов](https://support.office.com/article/Create-remove-or-change-a-trusted-location-for-your-files-f5151879-25ea-4998-80a5-4208b3540a62).  
  
## <a name="security-considerations-for-office-solutions"></a>Вопросы безопасности для решений Office  
 При выборе папок для добавления в список надежных расположений необходимо учесть несколько аспектов безопасности.  
  
-   Локальные папки являются более защищенными, поэтому они автоматически считаются надежными. Удаленные местоположения, такие как общие файловые ресурсы, необходимо назначить в качестве надежных расположений.  
  
-   При добавлении каталога в список надежных расположений полное доверие предоставляется не только решениям Office, но также коду VBA и ActiveX. По этой причине корневой каталог и *Мои документы* папки не должны быть обозначены как доверенные.  
  
-   Хотя сам документ является надежным при использовании надежного расположения, для предоставления доверия в целях настройки необходимы дополнительные разрешения. Можно предоставить полное доверие в настройке, используя подписание манифестов сертификатом, подтверждая доверие по запросу или установив решение Office для *Program Files* каталога.  
  
-   Документ или книгу решения на уровне документа можно сохранять в том же каталоге, что и сборку, или в другом каталоге. Например, документ может быть размещен на сервере SharePoint, а сборка может находиться на общем сетевом ресурсе. Дополнительные сведения см. в разделе [Как Публикация решения Office уровня документа на сервере SharePoint с помощью ClickOnce](https://msdn.microsoft.com/2408e809-fb78-42a1-9152-00afa1522e58).  
  
## <a name="see-also"></a>См. также  
 [Предоставление доверия решениям Office](../vsto/granting-trust-to-office-solutions.md)   
 [Устранение неполадок с безопасностью решений Office](../vsto/troubleshooting-office-solution-security.md)   
 [Безопасные решения Office](../vsto/securing-office-solutions.md)  
