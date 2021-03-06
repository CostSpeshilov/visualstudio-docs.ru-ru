---
title: Метод IJsDebugDataTarget::GetThreadContext | Документация Майкрософт
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IJsDebugDataTarget.GetThreadContext
apilocation:
- jscript9diag.dll
ms.assetid: faf2a689-6c49-4a7d-b5a6-2b323e2257a7
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 50e2bdb7b8720549aac5e5b3c4cebffc4b7ae892
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2019
ms.locfileid: "54090068"
---
# <a name="ijsdebugdatatargetgetthreadcontext-method"></a>Метод IJsDebugDataTarget::GetThreadContext
Возвращает контекст для данного потока.  
  
## <a name="syntax"></a>Синтаксис  
  
```cpp
HRESULT GetThreadContext(  
   DWORD threadId,  
   ULONG32 contextFlags,  
   ULONG32 contextSize,  
   void *pContext  
);  
```  
  
#### <a name="parameters"></a>Параметры  
 `threadId`  
 [in] Поток, выполняемый в целевом процессе.  
  
 `contextFlags`  
 [in] Задает флаги контекста. Это же поле ContextFlags контекста (Подробнее см. в разделе winnt.h, ищите CONTEXT_ALL).  
  
 `contextSize`  
 [in] Размер буфера, заданного pContext.  
  
 `pContext`  
 [out] Принимает от платформы структура КОНТЕКСТА в буфер, заданного pContext.  
  
## <a name="return-value"></a>Возвращаемое значение  
  
## <a name="requirements"></a>Требования  
 **Заголовок:** jscript9diag.h  
  
## <a name="see-also"></a>См. также  
 [Интерфейс IJsDebugDataTarget](../../winscript/reference/ijsdebugdatatarget-interface.md)