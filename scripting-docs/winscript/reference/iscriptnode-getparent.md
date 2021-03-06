---
title: IScriptNode::GetParent | Документация Майкрософт
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IScriptNode.GetParent
apilocation:
- scrobj.dll
helpviewer_keywords:
- IScriptNode::GetParent
ms.assetid: 0fb813f6-ab94-46b2-b0cf-ef5d1cd38ae4
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: b45fc7be1a5178e952fefcd794171410d149a1f4
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2019
ms.locfileid: "54090029"
---
# <a name="iscriptnodegetparent"></a>IScriptNode::GetParent
Возвращает `IScriptNode` объект, являющийся родительским для объекта.  
  
## <a name="syntax"></a>Синтаксис  
  
```cpp
HRESULT GetParent(  
   IScriptNode       **ppsnParent  
);  
```  
  
#### <a name="parameters"></a>Параметры  
 `ppsnParent`  
 [out] Адрес переменной, которая получает указатель на `IScriptNode` интерфейс родительского экземпляра.  
  
 Если класс реализует `IScriptEntry` или `IScriptScriptlet`, `IScriptNode` , то возвращается объект.  
  
 Если класс реализует `IScriptNode` (представляющие веб-страницы), возвращается значение NULL.  
  
## <a name="return-value"></a>Возвращаемое значение  
 Объект `HRESULT`. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.  
  
|Значение|Описание:|  
|-----------|-----------------|  
|`S_OK`|Метод успешно выполнен.|  
  
## <a name="remarks"></a>Примечания  
  
## <a name="see-also"></a>См. также  
 [Интерфейс IScriptNode](../../winscript/reference/iscriptnode-interface.md)