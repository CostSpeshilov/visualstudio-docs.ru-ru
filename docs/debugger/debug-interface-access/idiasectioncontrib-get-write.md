---
title: IDiaSectionContrib::get_write | Документация Майкрософт
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSectionContrib::get_write method
ms.assetid: 7e75348e-c12c-44ec-b004-e97767580a3f
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 677e42799c4098d2ba1100dd27b234855c7e7fcd
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MTE95
ms.contentlocale: ru-RU
ms.lasthandoff: 01/02/2019
ms.locfileid: "53832743"
---
# <a name="idiasectioncontribgetwrite"></a>IDiaSectionContrib::get_write
Получает флаг, указывающий, могут ли быть изменены разделе.  
  
## <a name="syntax"></a>Синтаксис  
  
```C++  
HRESULT get_write (   
   BOOL* pRetVal  
);  
```  
  
#### <a name="parameters"></a>Параметры  
 `pRetVal`  
 [out] Возвращает `TRUE` Если разделе могут быть записаны в противном случае возвращает `FALSE`.  
  
## <a name="return-value"></a>Возвращаемое значение  
 В случае успеха возвращает `S_OK`. Возвращает `S_FALSE` Если это свойство не поддерживается. В противном случае возвращается код ошибки.  
  
## <a name="see-also"></a>См. также раздел  
 [IDiaSectionContrib](../../debugger/debug-interface-access/idiasectioncontrib.md)