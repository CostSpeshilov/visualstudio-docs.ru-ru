---
title: IDebugApplicationNode::GetParent | Документация Майкрософт
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugApplicationNode.GetParent
apilocation:
- pdm.dll
helpviewer_keywords:
- IDebugApplicationNode::GetParent
ms.assetid: 88ba3a53-0cd7-4e1f-8558-79c20ac76cc9
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 46b13c583f4e40b68610e50b37520f3d3882f364
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2019
ms.locfileid: "54089652"
---
# <a name="idebugapplicationnodegetparent"></a>IDebugApplicationNode::GetParent
Возвращает родительский узел данного узла приложения.  
  
## <a name="syntax"></a>Синтаксис  
  
```cpp
HRESULT GetParent(  
   IDebugApplicationNode**  pprddp  
);  
```  
  
#### <a name="parameters"></a>Параметры  
 `pprddp`  
 [out] Родительский узел приложения этого узла приложения.  
  
## <a name="return-value"></a>Возвращаемое значение  
 Метод возвращает `HRESULT`. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.  
  
|Значение|Описание:|  
|-----------|-----------------|  
|`S_OK`|Метод успешно выполнен.|  
  
## <a name="remarks"></a>Примечания  
 Этот метод возвращает родительский узел данного узла приложения.  
  
## <a name="see-also"></a>См. также  
 [Интерфейс IDebugApplicationNode](../../winscript/reference/idebugapplicationnode-interface.md)