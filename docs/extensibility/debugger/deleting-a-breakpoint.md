---
title: Удаление точки останова | Документация Майкрософт
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- breakpoints, deleting
- debugging [Debugging SDK], deleting breakpoints
ms.assetid: 75a046cc-d20a-4c79-ad2d-1f18426ac5d0
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 294c8b04bb95501ef4bf6ba635a047f46a8703f0
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/25/2019
ms.locfileid: "55002838"
---
# <a name="deleting-a-breakpoint"></a>Удаление точки останова
Ниже описан процесс, при удалении ожидающая точка останова:  
  
## <a name="deletion-process"></a>Процесс удаления  
 Диспетчер отладки сеансов (SDM) вызывает [IDebugPendingBreakpoint2::Delete](../../extensibility/debugger/reference/idebugpendingbreakpoint2-delete.md) привязан метод для удаления ожидающая точка останова и всех связанных точек останова из него.  
  
> [!NOTE]
>  Связанная точка останова также можно удалить с помощью вызова [IDebugBoundBreakpoint2::Delete](../../extensibility/debugger/reference/idebugboundbreakpoint2-delete.md).  
  
## <a name="see-also"></a>См. также  
 [Вызов событий отладчика](../../extensibility/debugger/calling-debugger-events.md)