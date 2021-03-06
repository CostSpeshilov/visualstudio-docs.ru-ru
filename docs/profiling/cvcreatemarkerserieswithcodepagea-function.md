---
title: Функция CvCreateMarkerSeriesWithCodePageA | Документы Майкрософт
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- cvmakers/CvCreateMarkerSeriesWithCodePageA
helpviewer_keywords:
- CvCreateMarkerSeriesWithCodePageA method
ms.assetid: 3d7ed601-2222-4be9-a557-f217db008753
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 55466cc96e4969f05bc34edfaf4a28564dba17ea
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/02/2019
ms.locfileid: "53822493"
---
# <a name="cvcreatemarkerserieswithcodepagea-function"></a>Функция CvCreateMarkerSeriesWithCodePageA
Создает набор маркеров для заданного поставщика и указывает кодовую страницу. Эту функцию можно использовать, чтобы явно указать кодовую страницу для текста ANSI, считанного с помощью функций API. Установка кодовой страницы может оказаться полезной в том случае, если трассировка сначала собирается, а затем анализируется на различных компьютерах с различными языковыми стандартами и языками. По умолчанию используется кодовая страница, возвращаемая функцией GetACP().  
  
## <a name="syntax"></a>Синтаксис  
  
```C  
HRESULT CvCreateMarkerSeriesWithCodePageA(  
   _In_ PCV_PROVIDER pProvider,  
   _In_ LPCSTR pSeriesName,  
   _In_ UINT nTextCodePage,  
   _Out_ PCV_MARKERSERIES* ppMarkerSeries  
);  
```  
  
#### <a name="parameters"></a>Параметры  
 `pProvider`  
 Объект поставщика, уже инициализированный функцией CvInitProvider. Не может принимать значение NULL.  
  
 `pSeriesName`  
 Имя набора маркеров. Не может принимать значение NULL, но пустая строка разрешена.  
  
 `nTextCodePage`  
 Допустимая кодовая страница.  
  
 `ppMarkerSeries`  
 Адрес выходной переменной, в которой будет храниться контекст набора маркеров. Не может принимать значение NULL.  
  
## <a name="return-value"></a>Возвращаемое значение  
 Значение S_OK, если набор маркеров успешно создан, или код ошибки, если были какие-либо ошибки. Для проверки условия ошибки используйте макрос SUCCEEDED/FAILED.  
  
## <a name="requirements"></a>Требования  
 **Заголовок:** *cvmarkers.h*  
  
## <a name="see-also"></a>См. также  
 [Справочник по библиотеке C++](../profiling/cpp-library-reference.md)