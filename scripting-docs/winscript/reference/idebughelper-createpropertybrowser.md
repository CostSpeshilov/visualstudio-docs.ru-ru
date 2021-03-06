---
title: IDebugHelper::CreatePropertyBrowser | Документация Майкрософт
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugHelper.CreatePropertyBrowser
apilocation:
- pdm.dll
helpviewer_keywords:
- IDebugHelper::CreatePropertyBrowser
ms.assetid: 2fa819cf-c7f7-4bd7-b018-ea33b804ba8f
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: c3eedf9d6ed07b510d7912a5b28d23e0a1f05dda
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2019
ms.locfileid: "54087754"
---
# <a name="idebughelpercreatepropertybrowser"></a>IDebugHelper::CreatePropertyBrowser
Возвращает браузер свойств, который создает оболочку для типа VARIANT.  
  
## <a name="syntax"></a>Синтаксис  
  
```cpp
HRESULT CreatePropertyBrowser(  
   VARIANT*                  pvar,  
   LPCOLESTR                 bstrName,  
   IDebugApplicationThread*  pdat,  
   IDebugProperty**          ppdob  
);  
```  
  
#### <a name="parameters"></a>Параметры  
 `pvar`  
 [in] Корневой тип variant для просмотра.  
  
 `bstrName`  
 [in] Имя корневой.  
  
 `pdat`  
 [in] Поток, выступающей в качестве свойства запроса. Если этот параметр имеет значение NULL, выполняется без упаковки.  
  
 `ppdob`  
 [out] Браузер свойств.  
  
## <a name="return-value"></a>Возвращаемое значение  
 Метод возвращает `HRESULT`. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.  
  
|Значение|Описание:|  
|-----------|-----------------|  
|`S_OK`|Метод успешно выполнен.|  
  
## <a name="remarks"></a>Примечания  
 Этот метод возвращает браузер свойств, который создает оболочку для типа VARIANT.  
  
## <a name="see-also"></a>См. также  
 [IDebugHelper::CreatePropertyBrowserEx](../../winscript/reference/idebughelper-createpropertybrowserex.md)   
 [Интерфейс IDebugHelper](../../winscript/reference/idebughelper-interface.md)   
 [Интерфейс IDebugProperty](../../winscript/reference/idebugproperty-interface.md)