---
title: DEBUG_REFERENCE_INFO | Документация Майкрософт
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- DEBUG_REFERENCE_INFO
helpviewer_keywords:
- DEBUG_REFERENCE_INFO structure
ms.assetid: 24b83d00-d756-42a1-8083-730f998761dc
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: eb3b9f0c89d350fece18d49eee34d14d01d03352
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/25/2019
ms.locfileid: "55007685"
---
# <a name="debugreferenceinfo"></a>DEBUG_REFERENCE_INFO
Описывает ссылку.  
  
## <a name="syntax"></a>Синтаксис  
  
```cpp  
typedef struct tagDEBUG_REFERENCE_INFO {   
   DEBUGREF_INFO_FLAGS dwFields;  
   BSTR                bstrName;  
   BSTR                bstrType;  
   BSTR                bstrValue;  
   DBG_ATTRIB_FLAGS    dwAttrib;  
   REFERENCE_TYPE.     dwRefType;  
   IDebugReference2*   m_pReference;  
} DEBUG_REFERENCE_INFO;  
```  
  
```csharp  
public struct DEBUG_REFERENCE_INFO {   
   public uint             dwFields;  
   public string           bstrName;  
   public string           bstrType;  
   public string           bstrValue;  
   public ulong            dwAttrib;  
   public uint.            dwRefType;  
   public IDebugReference2 m_pReference;  
};  
```  
  
## <a name="members"></a>Участники  
 dwFields  
 Сочетание флагов из [DEBUGREF_INFO_FLAGS](../../../extensibility/debugger/reference/debugref-info-flags.md) перечисление, указывающее, какие поля заполнены.  
  
 bstrName  
 Определяемое пользователем имя [IDebugReference2](../../../extensibility/debugger/reference/idebugreference2.md) объекта.  
  
 bstrType  
 Ссылочный тип, как отформатированную строку.  
  
 bstrValue  
 Значение ссылки как отформатированную строку  
  
 dwAttrib  
 Сочетание флагов из [DBG_ATTRIB_FLAGS](../../../extensibility/debugger/reference/dbg-attrib-flags.md) перечисление, указывающее флаги для атрибутов свойства отладки.  
  
 dwRefType  
 Значение из [REFERENCE_TYPE](../../../extensibility/debugger/reference/reference-type.md) перечисление, указывающее, является ли тип ссылки строгие или слабые.  
  
 m_pReference  
 [IDebugReference2](../../../extensibility/debugger/reference/idebugreference2.md) , указывающий справочные сведения.  
  
## <a name="remarks"></a>Примечания  
 Эта структура передается в вызов [GetReferenceInfo](../../../extensibility/debugger/reference/idebugreference2-getreferenceinfo.md) метод для заполнения. Эта структура также возвращается как часть списка из [IEnumDebugReferenceInfo2](../../../extensibility/debugger/reference/ienumdebugreferenceinfo2.md) интерфейс, который, в свою очередь, возвращается из вызова [EnumChildren](../../../extensibility/debugger/reference/idebugreference2-enumchildren.md) метод.  
  
## <a name="requirements"></a>Требования  
 Header: msdbg.h  
  
 Пространство имен: Microsoft.VisualStudio.Debugger.Interop  
  
 Сборка: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>См. также  
 [Структуры и объединения](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [IDebugReference2](../../../extensibility/debugger/reference/idebugreference2.md)   
 [DEBUGREF_INFO_FLAGS](../../../extensibility/debugger/reference/debugref-info-flags.md)   
 [DBG_ATTRIB_FLAGS](../../../extensibility/debugger/reference/dbg-attrib-flags.md)   
 [REFERENCE_TYPE](../../../extensibility/debugger/reference/reference-type.md)   
 [GetReferenceInfo](../../../extensibility/debugger/reference/idebugreference2-getreferenceinfo.md)   
 [EnumChildren](../../../extensibility/debugger/reference/idebugreference2-enumchildren.md)   
 [IEnumDebugReferenceInfo2](../../../extensibility/debugger/reference/ienumdebugreferenceinfo2.md)