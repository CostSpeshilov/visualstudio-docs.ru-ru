---
title: Работа с концептуальной моделью(службы данных WCF)
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- data [Visual Studio], querying a service
- data [Visual Studio], LINQ to Entities
- data [Visual Studio], querying an EDM
ms.assetid: 2cd873cf-b010-49f2-a278-bb1277aaa934
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.workload:
- data-storage
ms.openlocfilehash: 6d49df542dbd134a6164e582459978bb2ef1aee3
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MTE95
ms.contentlocale: ru-RU
ms.lasthandoff: 01/02/2019
ms.locfileid: "53989650"
---
# <a name="work-with-a-conceptual-model-wcf-data-services"></a>Работа с концептуальной модели (службы данных WCF)

При использовании концептуальной модели для описания данных в базе данных, можно запросить данные через объекты вместо того, чтобы перевести вперед и назад между схему базы данных и модель объектов.

 Концептуальные модели можно использовать с приложениями WCF Data Services. Следующие разделы показывают, как запрашивать данные через концептуальную модель.


| Раздел | Описание |
| - | - |
| [Практическое руководство. Выполнение запросов к службе данных](/dotnet/framework/data/wcf/how-to-execute-data-service-queries-wcf-data-services) | Показано, как выполнять запросы к службе данных из [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] приложения. |
| [Практическое руководство. Спроецировать результаты запроса](/dotnet/framework/data/wcf/how-to-project-query-results-wcf-data-services) | Показано, как уменьшить объем данных, возвращаемых по запросу службы данных. |

 При использовании концептуальной модели, можно определить, какие данные является допустимым на языке, который совпадает с доменом. Можно определить допустимые данные в модели, или можно добавить проверку для операций, выполняемых в службе сущности или данных.

 Следующие разделы показывают, как добавить проверку в приложения служб WCF Data Services.

|Раздел|Описание|
|-----------|-----------------|
|[Практическое руководство. Перехват сообщений службы данных](/dotnet/framework/data/wcf/how-to-intercept-data-service-messages-wcf-data-services)|Показано, как добавить проверку в операцию службы данных.|

 Следующие разделы показывают, как для создания, изменения и удаления данных, выполняя операции с сущностями.

|Раздел|Описание|
|-----------|-----------------|
|[Практическое руководство. Добавление, изменение и удаление сущностей](/dotnet/framework/data/wcf/how-to-add-modify-and-delete-entities-wcf-data-services)|Показано, как создание, обновление и удаление данных сущности в службе данных.|
|[Практическое руководство. Определение связей сущностей](/dotnet/framework/data/wcf/how-to-define-entity-relationships-wcf-data-services)|Показано, как создать или изменить связи в службе данных.|

## <a name="see-also"></a>См. также

- [Службы Windows Communication Foundation и службы данных WCF в Visual Studio](../data-tools/windows-communication-foundation-services-and-wcf-data-services-in-visual-studio.md)
- [Выполнение запросов к службе данных](/dotnet/framework/data/wcf/querying-the-data-service-wcf-data-services)