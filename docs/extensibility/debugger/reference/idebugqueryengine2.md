---
title: IDebugQueryEngine2 | Документация Майкрософт
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugQueryEngine2
helpviewer_keywords:
- IDebugQueryEngine2 interface
ms.assetid: 8f0e1838-a818-4459-9138-a3dceb7408de
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b32464084a209aa7d6f41ffaa837d2f377b9720a
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/25/2019
ms.locfileid: "54984396"
---
# <a name="idebugqueryengine2"></a>IDebugQueryEngine2
Этот интерфейс позволяет сеанс отладки manager (SDM) получить интерфейс, который представляет модуль отладки (DE).  
  
## <a name="syntax"></a>Синтаксис  
  
```  
IDebugQueryEngine2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Примечания для разработчиков  
 DE реализует этот интерфейс для объектов, реализующих наиболее широко распространенными интерфейсами DE (такие как [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md), [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md), и [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md)) в Чтобы разрешить доступ к [IDebugEngine2](../../../extensibility/debugger/reference/idebugengine2.md) DE, сам интерфейс.  
  
## <a name="notes-for-callers"></a>Заметки о вызывающих объектов  
 Вызовите [QueryInterface](/cpp/atl/queryinterface) на типичный интерфейс DE для получения этого интерфейса.  
  
## <a name="methods-in-vtable-order"></a>Методы в порядке таблицы Vtable  
 В следующей таблице показаны методы `IDebugQueryEngine2`.  
  
|Метод|Описание|  
|------------|-----------------|  
|[GetEngineInterface](../../../extensibility/debugger/reference/idebugqueryengine2-getengineinterface.md)|Получает интерфейс отладки ядра (DE).|  
  
## <a name="remarks"></a>Примечания  
 Этот интерфейс обычно реализуется в объект, реализующий [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) интерфейс для поддержки упорядоченного причинно-следственных связей пошагового выполнения функции, то есть когда отладчик шаг с выходом из функции Далее функция, выполняемая может оказаться предыдущую функцию в стеке, но функции в другом потоке полностью. Определение «причинно-следственных связей», см. в разделе [глоссарий отладчика Visual Studio](../../../extensibility/debugger/reference/visual-studio-debugger-glossary.md).  
  
## <a name="requirements"></a>Требования  
 Header: msdbg.h  
  
 Пространство имен: Microsoft.VisualStudio.Debugger.Interop  
  
 Сборка: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>См. также  
 [Базовых интерфейсов](../../../extensibility/debugger/reference/core-interfaces.md)   
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)   
 [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)   
 [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md)   
 [IDebugEngine2](../../../extensibility/debugger/reference/idebugengine2.md)