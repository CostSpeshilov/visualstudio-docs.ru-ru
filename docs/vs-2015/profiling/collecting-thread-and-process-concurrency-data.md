---
title: Сбор данных о параллелизме потоков и процессов | Документы Майкрософт
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- concurrency profiling method
- Profiling Tools, concurrency method
ms.assetid: fa03d381-a9ee-408c-876d-05111e29225b
caps.latest.revision: 19
author: MikeJo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: df473bea51edd157e3856d274663b72dcc11bc23
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/16/2018
ms.locfileid: "51762621"
---
# <a name="collecting-thread-and-process-concurrency-data"></a>Сбор данных о параллелизме потоков и процессов
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Метод профилирования параллелизма средств профилирования [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] позволяет собирать данные о конфликтах ресурсов, которые содержат информацию о каждом событии синхронизации, которое принуждает функцию в профилируемом приложении ожидать доступ к ресурсу.  
  
 **Требования**  
  
- [!INCLUDE[vsUltLong](../includes/vsultlong-md.md)], [!INCLUDE[vsPreLong](../includes/vsprelong-md.md)], [!INCLUDE[vsPro](../includes/vspro-md.md)]  
  
  Метод профилирования параллелизма можно задать с помощью одной из приведенных ниже процедур.  
  
- На первой странице мастера профилирования щелкните **Параллелизм**.  
  
- На странице **Общие** диалогового окна свойств сеанса анализа производительности выберите **Параллелизм**.  
  
- На панели инструментов **обозревателя производительности** в списке **Метод** щелкните пункт **Параллелизм**.  
  
## <a name="common-tasks"></a>Общие задачи  
 Дополнительные параметры можно указать в диалоговом окне _Сеанс производительности_**страницы свойств** сеанса анализа производительности. Чтобы открыть это диалоговое окно, выполните указанные ниже действия.  
  
- В **обозревателе производительности**щелкните правой кнопкой мыши имя сеанса анализа производительности и выберите пункт **Свойства**.  
  
  В задачах в приведенной ниже таблице описываются параметры, которые можно задать в диалоговом окне _Сеанс производительности_**Страницы свойств** при профилировании с помощью метода параллелизма.  
  
|Задача|Связанное содержимое|  
|----------|---------------------|  
|На странице **Общие** задайте сведения об имени создаваемого файла данных профилирования (VSP).|-   [Практическое руководство. Настройка параметров имени файла с данными о производительности](../profiling/how-to-set-performance-data-file-name-options.md)|  
|На странице **Запуск** укажите приложение для запуска, если в решении с кодом содержится несколько проектов исполняемых файлов (EXE).|-   [Практическое руководство. Указание двоичного файла для запуска](../profiling/how-to-specify-the-binary-to-start.md)|  
|На странице **Взаимодействие уровней** добавьте данные вызова ADO.NET в сеанс профилировщика.|-   [Сбор данных взаимодействия уровней](../profiling/collecting-tier-interaction-data.md)|  
|На странице **Счетчики Windows** выберите один или несколько счетчиков производительности операционной системы, значения которых будут добавляться в данные профилирования в качестве меток.|-   [Практическое руководство. Сбор данных счетчиков производительности Windows](../profiling/how-to-collect-windows-counter-data.md)|  
|На странице **Дополнительно** укажите версию среды выполнения .NET Framework для профилирования, если модули приложения используют несколько версий. По умолчанию профилируется первая загруженная версия.|-   [Практическое руководство. Определение среды выполнения .NET Framework](../profiling/how-to-specify-the-dotnet-framework-runtime.md)|



