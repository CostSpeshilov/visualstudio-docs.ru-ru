---
title: GETHOSTNAME_TYPE | Документация Майкрософт
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
- GETHOSTNAME_TYPE
helpviewer_keywords:
- GETHOSTNAME_TYPE enumeration
ms.assetid: 2be92bea-8133-412b-9015-1833baf16e1b
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: ae1060507d20f6416168e41f2e09ecbc45ee7a37
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/16/2018
ms.locfileid: "51732633"
---
# <a name="gethostnametype"></a>GETHOSTNAME_TYPE
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Указывает тип имени узла.  
  
## <a name="syntax"></a>Синтаксис  
  
```cpp#  
enum enum_GETHOSTNAME_TYPE {   
   GHN_FRIENDLY_NAME = 0,  
   GHN_FILE_NAME     = 1  
};  
typedef DWORD GETHOSTNAME_TYPE;  
```  
  
```csharp  
public enum enum_GETHOSTNAME_TYPE {   
   GHN_FRIENDLY_NAME = 0,  
   GHN_FILE_NAME     = 1  
};  
```  
  
## <a name="members"></a>Участники  
 GHN_FRIENDLY_NAME  
 Указывает понятное имя узла.  
  
 GHN_FILE_NAME  
 Указывает имя файла узла.  
  
## <a name="remarks"></a>Примечания  
 Эти значения передаются в качестве аргумента [GetHostName](../../../extensibility/debugger/reference/idebugprogramnode2-gethostname.md) метод для извлечения имени узла в различных форматах.  
  
## <a name="requirements"></a>Требования  
 Заголовок: msdbg.h  
  
 Пространство имен: Microsoft.VisualStudio.Debugger.Interop  
  
 Сборка: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>См. также  
 [Перечисления](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [GetHostName](../../../extensibility/debugger/reference/idebugprogramnode2-gethostname.md)

