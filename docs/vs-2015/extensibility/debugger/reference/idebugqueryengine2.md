---
title: IDebugQueryEngine2 | Документация Майкрософт
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- IDebugQueryEngine2
helpviewer_keywords:
- IDebugQueryEngine2 interface
ms.assetid: 8f0e1838-a818-4459-9138-a3dceb7408de
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 284cae38309938d51f6ad5c58a89fc0297d8a10a
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/16/2018
ms.locfileid: "51735237"
---
# <a name="idebugqueryengine2"></a>IDebugQueryEngine2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Этот интерфейс позволяет сеанс отладки manager (SDM) получить интерфейс, который представляет модуль отладки (DE).  
  
## <a name="syntax"></a>Синтаксис  
  
```  
IDebugQueryEngine2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Примечания для разработчиков  
 DE реализует этот интерфейс для объектов, реализующих наиболее широко распространенными интерфейсами DE (такие как [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md), [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md), и [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md)) в Чтобы разрешить доступ к [IDebugEngine2](../../../extensibility/debugger/reference/idebugengine2.md) DE, сам интерфейс.  
  
## <a name="notes-for-callers"></a>Заметки о вызывающих объектов  
 Вызовите [QueryInterface](http://msdn.microsoft.com/library/62fce95e-aafa-4187-b50b-e6611b74c3b3) на типичный интерфейс DE для получения этого интерфейса.  
  
## <a name="methods-in-vtable-order"></a>Методы в порядке таблицы Vtable  
 В следующей таблице показаны методы `IDebugQueryEngine2`.  
  
|Метод|Описание:|  
|------------|-----------------|  
|[GetEngineInterface](../../../extensibility/debugger/reference/idebugqueryengine2-getengineinterface.md)|Получает интерфейс отладки ядра (DE).|  
  
## <a name="remarks"></a>Примечания  
 Этот интерфейс обычно реализуется в объект, реализующий [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) интерфейс для поддержки упорядоченного причинно-следственных связей пошагового выполнения функции, то есть когда отладчик шаг с выходом из функции Далее функция, выполняемая может оказаться предыдущую функцию в стеке, но функции в другом потоке полностью. Определение «причинно-следственных связей», см. в разделе [глоссарий отладчика Visual Studio](../../../extensibility/debugger/reference/visual-studio-debugger-glossary.md).  
  
## <a name="requirements"></a>Требования  
 Заголовок: msdbg.h  
  
 Пространство имен: Microsoft.VisualStudio.Debugger.Interop  
  
 Сборка: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>См. также  
 [Базовых интерфейсов](../../../extensibility/debugger/reference/core-interfaces.md)   
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)   
 [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)   
 [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md)   
 [IDebugEngine2](../../../extensibility/debugger/reference/idebugengine2.md)

