---
title: IActiveScriptErrorDebug::GetStackFrame | Документация Майкрософт
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptErrorDebug.GetStackFrame
apilocation:
- jscript.dll
helpviewer_keywords:
- IActiveScriptErrorDebug::GetStackFrame
ms.assetid: a6f43102-68c5-46f5-a4df-fa3aaf53a967
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: b9331738c52453f4ef80b70ab7eebd79907d1f54
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2019
ms.locfileid: "54094137"
---
# <a name="iactivescripterrordebuggetstackframe"></a>IActiveScriptErrorDebug::GetStackFrame
Предоставляет кадр стека, который распространяется на ошибки времени выполнения.  
  
## <a name="syntax"></a>Синтаксис  
  
```cpp
HRESULT GetStackFrame(  
   IDebugStackFrame**  ppdsf  
);  
```  
  
#### <a name="parameters"></a>Параметры  
 `ppdsf`  
 [out] Кадр стека для ошибки.  
  
## <a name="return-value"></a>Возвращаемое значение  
 Метод возвращает `HRESULT`. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.  
  
|Значение|Описание:|  
|-----------|-----------------|  
|`S_OK`|Метод успешно выполнен.|  
  
## <a name="remarks"></a>Примечания  
 Этот метод предоставляет кадр стека, который распространяется на ошибки времени выполнения.  
  
## <a name="see-also"></a>См. также  
 [Интерфейс IActiveScriptErrorDebug](../../winscript/reference/iactivescripterrordebug-interface.md)