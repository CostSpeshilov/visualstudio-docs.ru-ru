---
title: Время обработки пользовательского интерфейса | Документы Майкрософт
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.cv.threads.timeline.uiprocessing
helpviewer_keywords:
- Concurrency Visualizer, UI Processing Time
ms.assetid: 0ddb05a3-8c6b-448b-8488-2751c1e5abcc
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 51f34bb5396c1cadeab7c02c72f8ed13412e33b0
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/02/2019
ms.locfileid: "53858942"
---
# <a name="ui-processing-time"></a>Время обработки пользовательского интерфейса
Эти сегменты на временной шкале связаны с периодами блокирования, отнесенными к категории "Обработка UI". Это означает, что поток переносит сообщения Windows или выполняет другие операции пользовательского интерфейса. В это время поток был заблокирован в интерфейсе API, который визуализатор параллелизма интерпретирует как обработку пользовательского интерфейса. К этой группе относятся такие интерфейсы API, как `GetMessage()` и `MsgWaitForMultipleObjects()`.  
  
 Если предварительно заданные блокирующие интерфейсы API отсутствуют, просмотрите стеки вызовов и отчеты профилирования, чтобы определить изначальную причину задержки.  
  
 Категория "Обработка UI" помогает понять скорость отклика приложений с графическим пользовательским интерфейсом и желательна для приложений, зависящих от скорости отклика пользовательского интерфейса. Например, если поток пользовательского интерфейса приложения 100 % времени находился в состоянии "Обработка UI", скорость его отклика, по всей вероятности, высока. Если значительная часть времени выполнения потока пользовательского интерфейса была затрачена на операции иных категорий, нужно искать корневые причины и рассмотреть возможности сокращения в этом потоке числа операций, не относящихся к категории пользовательского интерфейса.  
  
## <a name="see-also"></a>См. также  
 [Представление потоков](../profiling/threads-view-parallel-performance.md)