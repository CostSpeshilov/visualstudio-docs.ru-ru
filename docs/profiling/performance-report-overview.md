---
title: Обзор отчета о производительности | Документы Майкрософт
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- profiling tools, about performance rerports
- performance, reports
- performance reports, about performance reports
ms.assetid: 7324c24c-fd09-479b-b2ad-e0c3b613e040
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: e2ed748ab3353dc8f5164c562b3523ee49930931
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/02/2019
ms.locfileid: "53839379"
---
# <a name="performance-report-overview"></a>Обзор отчета о производительности
Данные, собранные во время сеанса анализа производительности, можно просматривать в окне **Отчет о производительности** интегрированной среды разработки Visual Studio Team System Development Edition. Данные профилирования сохраняются в VSP- и VSPS-файлах. Окна представления отчета позволяют просматривать и анализировать данные о проблемах производительности приложения.  
  
> [!CAUTION]
>  В файле данных профилирования содержится конфиденциальная информация, например имя компьютера, версия операционной системы, пути к файлам, сведения о памяти и другие данные о настройке компьютера. Следует обеспечивать строгий контроль за распространением данных как в собственном формате (*VSP*), так и при экспорте этих данных в *CSV*- или *XML*-файл.  
>   
>  Если во время сеанса анализа производительности собираются данные о трассировке событий, дополнительная информация может сохраняться в файле журнала трассировке событий (*ETL*-файле). Эта информация содержит имя пользователя и домена, поэтому необходимо соблюдать крайнюю осторожность при распространении файла журнала.  
  
## <a name="performance-report-window"></a>Окно отчета о производительности  
 Отчет о производительности представляет собой окно инструментов, предназначенное для просмотра, управления и фильтрации данных о производительности, кроме того, в это окно включен элемент управления для формирования настраиваемых запросов.  
  
 С помощью главной панели инструментов окна отчета о производительности можно открыть любое из представлений. Щелкните стрелку рядом со списком **Текущее представление** и выберите одно из доступных представлений.  
  
 Ниже перечислены представления данных, которые можно просматривать в окне отчета о производительности.  
  
### <a name="summary-view"></a>Представление "Сводка"  
 По умолчанию данные профилирования отображаются в представлении "Сводка". Это представление является отправной точкой для исследования проблем производительности. Из каждой точки данных в представлении "Сводка" можно перейти к более подробным представлениям, щелкнув правой кнопкой мыши имя функции или модуля. Дополнительные сведения см. в разделе [Представление "Сводка"](../profiling/summary-view.md).  
  
### <a name="callercallee-view"></a>Представление «Вызывающий/вызываемый»  
 Представление "Вызывающий/вызываемый" позволяет просмотреть дерево вызовов для отдельной функции. Представление состоит из трех частей.  
  
- Целевая функция отображается в средней части представления.  
  
- Функции, которые вызывают текущую функцию, (вызывающие) отображаются над целевой функцией.  
  
- Функции, которые вызываются текущей функцией, (вызываемые) отображаются под целевой функцией.  
  
  Можно выбрать другую функцию, дважды щелкнув ее в списке вызывающих или вызываемых функций. Дополнительные сведения см. в разделе [Представление "Вызывающий/вызываемый"](../profiling/caller-callee-view.md).  
  
### <a name="call-tree-view"></a>Представление "Дерево вызовов"  
 В преставлении "Дерево вызовов" отображаются пути выполнения функции, пересеченные в профилируемом приложении. Корнем дерева является точка входа в приложение или компонент. В каждом узле функции перечислены все вызванные в нем функции и содержатся данные о производительности, связанные с этими вызовами функций.  
  
 Кроме того, можно развернуть представление "Дерево вызовов" и проанализировать путь выполнения функции, приведший к наибольшей задержке или встречавшийся наиболее часто. Чтобы отобразить самый активный путь, щелкните функцию правой кнопкой мыши и выберите команду **Развернуть критический путь**. Дополнительные сведения см. в разделе [Представление "Дерево вызовов"](../profiling/call-tree-view.md).  
  
### <a name="process-view"></a>Представление "Процесс"  
 В представлении "Процесс" отображаются данные о производительности каждого профилируемого процесса и потока. Дополнительные сведения см. в разделе [Представление "Процесс"](../profiling/process-view.md).  
  
### <a name="modules-view"></a>Представление "Модули"  
 В представлении "Модули" перечисляются модули проекта и отображаются данные профилирования для каждого модуля. Чтобы отобразить данные о производительности функции, следует развернуть или свернуть имя модуля. Если сбор данных выполнялся с использованием метода выборки, пользователю также доступны данные о строке исходного кода и значения указателя инструкций. Дополнительные сведения см. в разделе [Представление "Модули"](../profiling/modules-view.md).  
  
### <a name="functions-view"></a>Представление "Функции"  
 В представлении "Функции" отображается список функций, которые вызывались во время сеанса профилирования. Дополнительные сведения см. в разделе [Представление "Функции"](../profiling/functions-view.md).  
  
### <a name="line-view"></a>Представление "Строки"  
 Представление "Строки" позволяет просматривать отдельные строки исходного кода, которые выполнялись во время профилирования с выборкой. Дополнительные сведения см. в разделе [Представление "Строки"](../profiling/lines-view.md).  
  
### <a name="instruction-pointer-ip-view"></a>Представление "Указатель инструкций"  
 Представление "Указатели инструкций" позволяет просматривать инструкции, которые выполнялись во время профилирования с выборкой. Дополнительные сведения см. в разделе [Представление "Указатели инструкций"](../profiling/instruction-pointers-ips-view.md).  
  
### <a name="allocation-view"></a>Представление "Выделение"  
 Представление "Выделение" доступно в том случае, если на странице **Общие** диалогового окна свойств **Сеанс производительности** установлен флажок **Собирать сведения о выделении объектов .NET**. См. раздел [Общие сведения о сеансе анализа производительности](../profiling/performance-session-overview.md). В представлении "Выделение" перечислены объекты .NET, которые были выделены приложением или компонентом. Когда строка объекта развернута, отображается дерево вызовов. В дереве вызовов показаны пути выполнения, приведшие к созданию объекта. Кроме того, отображаются сведения о количестве эксклюзивных и инклюзивных операций выделения памяти для каждой из функций в дереве вызовов. Кроме того, можно развернуть представление "Выделение" и проанализировать путь выполнения функции, приведший к выделению памяти для наибольшего количества объектов. Чтобы отобразить самый активный путь, щелкните функцию правой кнопкой мыши и выберите команду **Развернуть критический путь**. Дополнительные сведения см. в разделах [Сбор данных о выделении памяти для объектов .NET и времени их жизни](../profiling/collecting-dotnet-memory-allocation-and-lifetime-data.md) и [Представление "Выделения"](../profiling/dotnet-memory-allocations-view.md).  
  
### <a name="objects-lifetime-view"></a>Представление "Время существования объектов"  
 Представление "Время существования объектов" доступно в том случае, если на странице **Общие** диалогового окна свойств **Сеанс производительности** установлены флажки **Собирать сведения о выделении объектов .NET** и **Также собирать сведения о времени жизни объектов .NET**.  
  
 В представлении "Время существования объектов" отображается общее количество экземпляров каждого типа и количество объектов, которые были собраны в каждом поколении сборки мусора. Дополнительные сведения см. в разделе [Представление "Время существования объектов"](../profiling/object-lifetime-view.md).  
  
## <a name="customizable-filter-control"></a>Настраиваемый элемент управления фильтра  
 Ниже перечислены параметры, которые можно установить в настраиваемом элементе управления фильтра.  
  
-   **Импорт фильтра** — загрузка ранее сохраненного пользовательского запроса.  
  
-   **Экспорт фильтра** — сохранение пользовательского запроса в указанном местоположении.  
  
-   **Выполнить запрос** — выполнение запроса, отображаемого в окне настраиваемого элемента управления фильтра.  
  
-   **Остановить запрос** — остановка выполнения запроса. Если запросы не выполняются, эта кнопка недоступна.  
  
-   **Показать запрос** — отображение или скрытие настраиваемого элемента управления фильтра.  
  
-   **Сохранить проанализированные** — сохранение отчета с текущими данными анализа в VSPS-файле.  
  
-   **Экспорт** — сохранение текущего отчета в файле формата CVS или XML с возможностью сохранения различных представлений.  
  
## <a name="see-also"></a>См. также  
 [Анализ данных из средств оценки производительности](../profiling/analyzing-performance-tools-data.md)   
 [Представления отчетов о производительности](../profiling/performance-report-views.md)