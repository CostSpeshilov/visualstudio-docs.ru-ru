---
title: IDebugStackFrame3::GetUnwindCodeContext | Документация Майкрософт
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugStackFrame3::GetUnwindCodeContext
helpviewer_keywords:
- IDebugStackFrame3::GetUnwindCodeContext method
ms.assetid: b25f7e7d-2b24-48e4-93b3-829e61d73ebf
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 032e7f05ebb1ba8367ffaa7ef1ffbfb974aa0df1
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/25/2019
ms.locfileid: "54933572"
---
# <a name="idebugstackframe3getunwindcodecontext"></a>IDebugStackFrame3::GetUnwindCodeContext
Возвращает контекст кода, представляющая расположение в том случае, если операция развертывания стека произошла.  
  
## <a name="syntax"></a>Синтаксис  
  
```cpp  
HRESULT GetUnwindCodeContext(  
   IDebugCodeContext2 **ppCodeContext  
);  
```  
  
```csharp  
int GetUnwindCodeContext(  
   out IDebugCodeContext2 ppCodeContext  
);  
```  
  
#### <a name="parameters"></a>Параметры  
 `ppCodeContext`  
 [out] Возвращает [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md) , представляющий контекст расположения кода в том случае, если произошла очистки стека.  
  
## <a name="return-value"></a>Возвращаемое значение  
 В случае успешного выполнения возвращает `S_OK`; в противном случае возвращает код ошибки.  
  
## <a name="remarks"></a>Примечания  
 Несмотря на то, что этот метод может возвращать контекст кода для расположения после очистки стека, он не обязательно означает, что очистки стека может происходить в текущем кадре стека.  
  
## <a name="see-also"></a>См. также  
 [IDebugStackFrame3](../../../extensibility/debugger/reference/idebugstackframe3.md)   
 [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md)