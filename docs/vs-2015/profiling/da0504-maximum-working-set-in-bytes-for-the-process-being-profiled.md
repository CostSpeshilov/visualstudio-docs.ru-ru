---
title: DA0504. Максимальный рабочий набор в байтах для профилируемого процесса | Документы Майкрософт
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.performance.DA0504
- vs.performance.504
- vs.performance.rules.DA0504
ms.assetid: 36e71603-ece7-4000-85fc-9da4eed61bf2
caps.latest.revision: 12
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 554db9edb121b1d0c72eb7c78a10e869b921e0c3
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/22/2018
ms.locfileid: "47563775"
---
# <a name="da0504-maximum-working-set-in-bytes-for-the-process-being-profiled"></a>DA0505. Максимальный рабочий набор в байтах для профилируемого процесса
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Последнюю версию этого раздела можно найти в [DA0504: максимальный рабочий набор в байтах для профилируемого процесса](https://docs.microsoft.com/visualstudio/profiling/da0504-maximum-working-set-in-bytes-for-the-process-being-profiled).  
  
ИД правила | DA0504 |  
| Категория | Управление ресурсами |  
| Метод профилирования | Все |  
| Сообщение | Эти сведения были собраны только для информации. Счетчик рабочего набора процесса измеряет объем использования физической памяти профилируемым процессом. Полученное значение является максимальным по всем интервалам измерения. |  
| Тип правила | Сведения |  
  
 При профилировании с помощью выборки, памяти .NET или методов разрешения конфликтов ресурсов необходимо собрать минимум 10 выборок, чтобы активировать это правило.  
  
## <a name="rule-description"></a>Описание правила  
 В этом сообщении указывается максимальный объем физической памяти (в байтах), используемой процессом в данный момент. Рабочий набор процесса представляет страницы из адресного пространства процесса, которые в настоящий момент находятся в физической памяти. Это правило передает максимальное значение для рабочего набора процесса на момент выполнения профилирования.  
  
 В указываемом значении учитываются постоянные страницы из сегментов общей памяти, на которые ссылается процесс. Общие библиотеки DLL, на которые ссылается процесс, включаются в сегменты общей памяти, которые учитываются счетчиком. Значение рабочего набора процесса может превышать объем виртуальной памяти, выделенной процессом из-за сегментов общей памяти.  
  
 Размер рабочего набора процесса отражает объем виртуальной памяти, активно используемой процессом. На него также влияет объем физической памяти (или ОЗУ), доступной для запуска приложения, и состязание за физическую память с другими процессами. Дополнительные сведения о рабочих наборах процесса см. в разделе [Рабочий набор](http://go.microsoft.com/fwlink/?LinkId=177830) в документации MSDN по управлению памятью Windows.  
  
## <a name="how-to-use-rule-data"></a>Использование данных правила  
 Правило собирает данные измерений, передаваемые средством отслеживания производительности Windows, и выводит их исключительно в информационных целях. Это значение используется для сравнения производительности разных версий или сборок программы или для анализа производительности приложения в различных сценариях тестирования.  
  
 Дважды щелкните сообщение в окне "Список ошибок", чтобы перейти к представлению [Метки](../profiling/marks-view.md) данных профилирования. Найдите столбцы счетчика **Процесс\Рабочий набор** и **Память\Страниц в секунду**. Затем найдите максимальное значение в столбце **Процесс\Рабочий набор** и сравните его со значением **Память\Страниц в секунду**. Зачастую максимальное значение рабочего набора связано с интервалом, в котором наблюдается снижение числа операций ввода-вывода подкачки, особенно в том случае, если ресурсы памяти компьютера ограничены.


