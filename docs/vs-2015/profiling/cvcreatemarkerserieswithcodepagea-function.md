---
title: Функция CvCreateMarkerSeriesWithCodePageA | Документы Майкрософт
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- cvmakers/CvCreateMarkerSeriesWithCodePageA
helpviewer_keywords:
- CvCreateMarkerSeriesWithCodePageA method
ms.assetid: 3d7ed601-2222-4be9-a557-f217db008753
caps.latest.revision: 8
author: MikeJo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: f2a1a1380869ae26dbda30f47f6b3de08b288b7a
ms.sourcegitcommit: f6dd17b0864419083d0a1bf54910023045526437
ms.translationtype: MTE95
ms.contentlocale: ru-RU
ms.lasthandoff: 12/27/2018
ms.locfileid: "53802385"
---
# <a name="cvcreatemarkerserieswithcodepagea-function"></a>Функция CvCreateMarkerSeriesWithCodePageA
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Создает набор маркеров для заданного поставщика и указывает кодовую страницу. Эту функцию можно использовать, чтобы явно указать кодовую страницу для текста ANSI, считанного с помощью функций API. Установка кодовой страницы может оказаться полезной в том случае, если трассировка сначала собирается, а затем анализируется на различных компьютерах с различными языковыми стандартами и языками. По умолчанию используется кодовая страница, возвращаемая функцией GetACP().  
  
## <a name="syntax"></a>Синтаксис  
  
```  
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
 **Заголовок:** cvmarkers.h  
  
## <a name="see-also"></a>См. также  
 [Справочник по библиотеке C++](../profiling/cpp-library-reference.md)



