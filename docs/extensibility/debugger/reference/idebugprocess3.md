---
title: IDebugProcess3 | Документация Майкрософт
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugProcess3
helpviewer_keywords:
- IDebugProcess3 interface
ms.assetid: 7bd6b952-cf34-4e66-b8f6-d472dac3748f
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: bca432c7999d4ec3e7ff4a5a8700eea698486798
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/25/2019
ms.locfileid: "54962801"
---
# <a name="idebugprocess3"></a>IDebugProcess3
Этот интерфейс представляет выполняющемуся процессу и его программ. Этот интерфейс существует для замены нескольким методам в [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) интерфейс. Он позволяет контролировать все программы в процессе.  
  
> [!NOTE]
>  [По-прежнему](../../../extensibility/debugger/reference/idebugprogram2-continue.md), [Execute](../../../extensibility/debugger/reference/idebugprogram2-execute.md), и [шаг](../../../extensibility/debugger/reference/idebugprogram2-step.md) методы считаются устаревшими и больше не используется. Используйте соответствующие методы в `IDebugProcess3` интерфейса.  
  
## <a name="syntax"></a>Синтаксис  
  
```  
IDebugProcess3 : IDebugProcess2  
```  
  
## <a name="notes-for-implementers"></a>Примечания для разработчиков  
 Этот интерфейс реализуется поставщиком пользовательский порт, для управления программами как группу. Когда программ управляются как группу, можно управлять их выполнение и установить язык для вычислителя выражений. Этот интерфейс должен реализовываться поставщика порта.  
  
## <a name="notes-for-callers"></a>Заметки о вызывающих объектов  
 Этот интерфейс называется главным образом диспетчер отладки сеансов (SDM) для взаимодействия с группой программы, указанные в этом процессе.  
  
 Вызовите [QueryInterface](/cpp/atl/queryinterface) на [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md) интерфейс для получения этого интерфейса.  
  
## <a name="methods-in-vtable-order"></a>Методы в порядке таблицы Vtable  
 Помимо методов, наследуемых от [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md), `IDebugProcess3` реализует следующие методы.  
  
|Метод|Описание:|  
|------------|-----------------|  
|[Continue](../../../extensibility/debugger/reference/idebugprocess3-continue.md)|Продолжает выполнение или пошагового выполнения процесса.|  
|[Execute](../../../extensibility/debugger/reference/idebugprocess3-execute.md)|Начинает выполнение процесса.|  
|[Step](../../../extensibility/debugger/reference/idebugprocess3-step.md)|Действия пересылать одну инструкцию или инструкции в процессе.|  
|[GetDebugReason](../../../extensibility/debugger/reference/idebugprocess3-getdebugreason.md)|Возвращает причину, что процесс был запущен для отладки.|  
|[SetHostingProcessLanguage](../../../extensibility/debugger/reference/idebugprocess3-sethostingprocesslanguage.md)|Задает язык, размещения, таким образом, чтобы модуль отладки можно загрузить средство оценки выражений, соответствующую.|  
|[GetHostingProcessLanguage](../../../extensibility/debugger/reference/idebugprocess3-gethostingprocesslanguage.md)|Извлекает текущий язык для этого процесса.|  
|[DisableENC](../../../extensibility/debugger/reference/idebugprocess3-disableenc.md)|Отключает Изменить и продолжить "(ENC) для этого процесса.<br /><br /> Пользовательский порт поставщик не реализует этот метод (всегда должны возвращать `E_NOTIMPL`).|  
|[GetENCAvailableState](../../../extensibility/debugger/reference/idebugprocess3-getencavailablestate.md)|Получение состояния ENC для этого процесса.<br /><br /> Пользовательский порт поставщик не реализует этот метод (всегда должны возвращать `E_NOTIMPL`).|  
|[GetEngineFilter](../../../extensibility/debugger/reference/idebugprocess3-getenginefilter.md)|Извлекает массив уникальных идентификаторов для доступных отладчиков.|  
  
## <a name="requirements"></a>Требования  
 Заголовок: Msdbg.h  
  
 Пространство имен: Microsoft.VisualStudio.Debugger.Interop  
  
 Сборка: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>См. также  
 [Базовых интерфейсов](../../../extensibility/debugger/reference/core-interfaces.md)   
 [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)   
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)