---
title: IDebugBreakpointBoundEvent2 | Документация Майкрософт
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugBreakpointBoundEvent2
helpviewer_keywords:
- IDebugBreakpointBoundEvent2
ms.assetid: 24ba362e-5be1-481a-b071-e1ebd3cae6e8
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 59d42a2fe87efbca6dcf491942cdc5cf77505774
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/25/2019
ms.locfileid: "54942874"
---
# <a name="idebugbreakpointboundevent2"></a>IDebugBreakpointBoundEvent2
Этот интерфейс указывает диспетчер отладки сеансов (SDM) успешно привязать точку останова для загрузки программы.  
  
## <a name="syntax"></a>Синтаксис  
  
```  
IDebugBreakpointBoundEvent2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Примечания для разработчиков  
 DE реализует этот интерфейс как часть поддержки точек останова. [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md) на один и тот же объект как этот интерфейс должен быть реализован интерфейс (использует SDM [QueryInterface](/cpp/atl/queryinterface) для доступа к `IDebugEvent2` интерфейс).  
  
## <a name="notes-for-callers"></a>Заметки о вызывающих объектов  
 DE создает и отправляет этот объект события в том случае, если ожидающая точка останова успешно привязан к отлаживаемой программы. Это событие отправляется с помощью [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md) функции обратного вызова, предоставляемой SDM, если он присоединен к отлаживаемой программы.  
  
## <a name="methods-in-vtable-order"></a>Методы в порядке таблицы Vtable  
 В следующей таблице показаны методы `IDebugBreakpointBoundEvent2`.  
  
|Метод|Описание:|  
|------------|-----------------|  
|[GetPendingBreakpoint](../../../extensibility/debugger/reference/idebugbreakpointboundevent2-getpendingbreakpoint.md)|Получает ожидающая точка останова, к которому осуществляется привязка.|  
|[EnumBoundBreakpoints](../../../extensibility/debugger/reference/idebugbreakpointboundevent2-enumboundbreakpoints.md)|Создает перечислитель точек останова, которые были привязаны на это событие.|  
  
## <a name="remarks"></a>Примечания  
 Каждый раз, когда привязана точка останова, событие передается SDM. Если точка останова не может быть привязана, [IDebugBreakpointErrorEvent2](../../../extensibility/debugger/reference/idebugbreakpointerrorevent2.md) передаются; в противном случае — значение `IDebugBreakpointBoundEvent2` отправляется.  
  
## <a name="requirements"></a>Требования  
 Header: msdbg.h  
  
 Пространство имен: Microsoft.VisualStudio.Debugger.Interop  
  
 Сборка: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>См. также  
 [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md)   
 [IDebugPendingBreakpoint2](../../../extensibility/debugger/reference/idebugpendingbreakpoint2.md)   
 [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md)   
 [IDebugBreakpointErrorEvent2](../../../extensibility/debugger/reference/idebugbreakpointerrorevent2.md)