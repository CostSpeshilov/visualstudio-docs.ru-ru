---
title: IDiaEnumDebugStreamData::Next | Документация Майкрософт
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaEnumDebugStreamData::Next method
ms.assetid: 114171dd-38fd-4bd7-a702-8ff887ffc99b
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 781fd79611e8de323085ed73dc7682808d69b6ff
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MTE95
ms.contentlocale: ru-RU
ms.lasthandoff: 01/02/2019
ms.locfileid: "53958388"
---
# <a name="idiaenumdebugstreamdatanext"></a>IDiaEnumDebugStreamData::Next
Извлекает указанное число записей в перечисленной последовательности.  
  
## <a name="syntax"></a>Синтаксис  
  
```C++  
HRESULT Next (   
   ULONG  celt,  
   DWORD  cbData,  
   DWORD* pcbData,  
   BYTE   data[],  
   ULONG* pceltFetched  
);  
```  
  
#### <a name="parameters"></a>Параметры  
 celt  
 [in] Число записей, которые требуется извлечь.  
  
 cbData  
 [in] Размер буфера данных, в байтах.  
  
 pcbData  
 [out] Возвращает количество байтов, возвращаемых. Если `data` имеет значение NULL, затем `pcbData` содержит общее число байтов данных, доступные для всех запрошенных записей.  
  
 data[]  
 [out] Буфер, который должен быть заполнен данными отладки потока записи.  
  
 pceltFetched  
 [in, out] Возвращает число записей в `data`.  
  
## <a name="return-value"></a>Возвращаемое значение  
 В случае успеха возвращает `S_OK`. Возвращает `S_FALSE` Если отсутствуют дополнительные записи. В противном случае возвращается код ошибки.  
  
## <a name="see-also"></a>См. также раздел  
 [IDiaEnumDebugStreamData](../../debugger/debug-interface-access/idiaenumdebugstreamdata.md)   
 [IDiaEnumDebugStreams::Next](../../debugger/debug-interface-access/idiaenumdebugstreams-next.md)