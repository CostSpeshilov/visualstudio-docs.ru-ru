---
title: EndTrackingContext | Документы Майкрософт
ms.date: 11/04/2016
ms.topic: conceptual
apiname:
- EndTrackingContext
apilocation:
- filetracker.dll
apitype: COM
helpviewer_keywords:
- EndTrackingContext
ms.assetid: c2c5d794-8dc8-4594-8717-70dc79a0e75d
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: fba2d86ca02bf0ddc12e288b3bcbbd4b7189120e
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/02/2019
ms.locfileid: "53911511"
---
# <a name="endtrackingcontext"></a>EndTrackingContext
Конц текущего контекста отслеживания.  
  
## <a name="syntax"></a>Синтаксис  
  
```cpp  
HRESULT WINAPI EndTrackingContext();  
```  
  
## <a name="return-value"></a>Возвращаемое значение  
 **HRESULT** с установленным битом **SUCCEEDED**, если контекст отслеживания был закончен.  
  
## <a name="requirements"></a>Требования  
 **Заголовок.** *FileTracker.h*  
  
## <a name="see-also"></a>См. также  
 [StartTrackingContext](../msbuild/starttrackingcontext.md)