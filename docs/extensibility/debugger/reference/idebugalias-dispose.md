---
title: IDebugAlias::Dispose | Документация Майкрософт
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugAlias::Dispose
helpviewer_keywords:
- IDebugAlias::Dispose method
ms.assetid: e84909a4-d378-4f48-bf25-2c014c77c8e3
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: f5dffc8e9bb5440fb1a05cd733c609af43104f72
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/25/2019
ms.locfileid: "55028417"
---
# <a name="idebugaliasdispose"></a>IDebugAlias::Dispose
Помечает этот псевдоним для удаления.  
  
## <a name="syntax"></a>Синтаксис  
  
```cpp  
HRESULT Dispose();  
```  
  
```csharp  
int Dispose();  
```  
  
#### <a name="parameters"></a>Параметры  
 Отсутствует.  
  
## <a name="return-value"></a>Возвращаемое значение  
 В случае успешного выполнения возвращает значение S_OK; в противном случае возвращает код ошибки.  
  
## <a name="remarks"></a>Примечания  
 Когда этот метод вызывается, псевдоним больше не доступен.  
  
## <a name="see-also"></a>См. также  
 [IDebugAlias](../../../extensibility/debugger/reference/idebugalias.md)