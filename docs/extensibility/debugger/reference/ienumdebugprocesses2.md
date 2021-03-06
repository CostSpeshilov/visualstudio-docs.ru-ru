---
title: IEnumDebugProcesses2 | Документация Майкрософт
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IEnumDebugProcesses2
helpviewer_keywords:
- IEnumDebugProcesses2
ms.assetid: 06a1368f-10f0-44eb-af61-e388c2327111
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 7e7654338bfa04b2c48a8286f9996f9002a95bbd
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/25/2019
ms.locfileid: "55023685"
---
# <a name="ienumdebugprocesses2"></a>IEnumDebugProcesses2
Этот интерфейс перечисляет процессы, запущенные на порта отладки.  
  
## <a name="syntax"></a>Синтаксис  
  
```  
IEnumDebugProcesses : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Примечания для разработчиков  
 Пользовательский порт поставщик реализует этот интерфейс для предоставления списка процессов, работающий с портом.  
  
## <a name="notes-for-callers"></a>Заметки о вызывающих объектов  
 Visual Studio вызывает [EnumProcesses](../../../extensibility/debugger/reference/idebugport2-enumprocesses.md) для получения этого интерфейса.  
  
## <a name="methods-in-vtable-order"></a>Методы в порядке таблицы Vtable  
 В следующей таблице показаны методы `IEnumDebugProcesses2`.  
  
|Метод|Описание|  
|------------|-----------------|  
|[Вперед](../../../extensibility/debugger/reference/ienumdebugprocesses2-next.md)|Получает заданное число процессов в последовательности перечисления.|  
|[Skip](../../../extensibility/debugger/reference/ienumdebugprocesses2-skip.md)|Пропускает заданное число процессов в последовательности перечисления.|  
|[Reset](../../../extensibility/debugger/reference/ienumdebugprocesses2-reset.md)|Сбрасывает последовательность перечислений в начало.|  
|[Clone](../../../extensibility/debugger/reference/ienumdebugprocesses2-clone.md)|Создает перечислитель с тем же состоянием перечисления, что и текущий перечислитель.|  
|[GetCount](../../../extensibility/debugger/reference/ienumdebugprocesses2-getcount.md)|Получает число процессов в перечислителе.|  
  
## <a name="remarks"></a>Примечания  
 Visual Studio использует этот интерфейс для заполнения **процессы** окна.  
  
## <a name="requirements"></a>Требования  
 Header: msdbg.h  
  
 Пространство имен: Microsoft.VisualStudio.Debugger.Interop  
  
 Сборка: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>См. также  
 [Базовых интерфейсов](../../../extensibility/debugger/reference/core-interfaces.md)   
 [EnumProcesses](../../../extensibility/debugger/reference/idebugport2-enumprocesses.md)