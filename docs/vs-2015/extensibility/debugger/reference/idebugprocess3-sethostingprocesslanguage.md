---
title: IDebugProcess3::SetHostingProcessLanguage | Документация Майкрософт
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
- IDebugProcess3::SetHostingProcessLanguage
helpviewer_keywords:
- IDebugProcess3::SetHostingProcessLanguage
ms.assetid: e42f33ed-f29c-4e45-92ce-ab504b72d77c
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: a106ad8462f397399c0ede16bc5889248abe4475
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/16/2018
ms.locfileid: "51773630"
---
# <a name="idebugprocess3sethostingprocesslanguage"></a>IDebugProcess3::SetHostingProcessLanguage
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Этот метод задает язык, процесс будет размещаться в группе. Этот язык можно использоваться ядром отладки (DE), загрузить соответствующий вычислителя выражений.  
  
## <a name="syntax"></a>Синтаксис  
  
```cpp  
HRESULT SetHostingProcessLanguage(  
   REFGUID guidLang  
);  
```  
  
```csharp  
int SetHostingProcessLanguage(  
   ref Guid guidLang  
);  
```  
  
#### <a name="parameters"></a>Параметры  
 `guidLang`  
 [in] `GUID` языка, который следует использовать DE. Укажите `GUID_NULL` (C++) или `Guid.Empty` (C#), чтобы иметь DE использования языка по умолчанию.  
  
## <a name="return-value"></a>Возвращаемое значение  
 В случае успешного выполнения возвращает `S_OK`; в противном случае возвращает код ошибки.  
  
## <a name="remarks"></a>Примечания  
 [GetHostingProcessLanguage](../../../extensibility/debugger/reference/idebugprocess3-gethostingprocesslanguage.md) может использоваться для получения текущих языковых параметров.  
  
## <a name="see-also"></a>См. также  
 [IDebugProcess3](../../../extensibility/debugger/reference/idebugprocess3.md)   
 [GetHostingProcessLanguage](../../../extensibility/debugger/reference/idebugprocess3-gethostingprocesslanguage.md)

