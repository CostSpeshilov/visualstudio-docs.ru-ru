---
title: Перечисление PROFILER_HEAP_ENUM_FLAGS | Документация Майкрософт
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 17936b7a-40d5-4774-b92b-b24ee391591e
caps.latest.revision: 6
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 2c711dd3a4174f38bf2f3b3e163805e6cfa1c314
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/16/2019
ms.locfileid: "54345231"
---
# <a name="profilerheapenumflags-enumeration"></a>Перечисление PROFILER_HEAP_ENUM_FLAGS
Флаги, представляющие ли предоставляется дополнительную информацию об объекте кучи, на который указывает указатель в объектном отношении. Используется в [EnumHeap2](../../winscript/reference/iactivescriptprofilercontrol5-enumheap2-method.md) метод.  
  
## <a name="syntax"></a>Синтаксис  
  
```cpp
typedef [v1_enum] enum {    PROFILER_HEAP_ENUM_FLAGS_NONE                      = 0x00000000,    PROFILER_HEAP_ENUM_FLAGS_STORE_RELATIONSHIP_FLAGS  = 0x00000001,} PROFILER_HEAP_ENUM_FLAGS;  
```  
  
## <a name="members"></a>Участники  
  
|Член|Значение|Описание|  
|------------|-----------|-----------------|  
|PROFILER_HEAP_ENUM_FLAGS_NONE|0x00000000|Этот объект кучи предоставляет дополнительные сведения о связи объекта. Этот объект кучи ведет себя так же, как [IActiveScriptProfilerControl3::HeapEnum](../../winscript/reference/iactivescriptprofilercontrol3-enumheap-method.md).|  
|PROFILER_HEAP_ENUM_ENUM_ STORE_RELATIONSHIP_FLAGS|0x00000001|Этот объект кучи предоставляет сведения о том, является ли объект, на который указывает указатель в объектном отношении метод доступа get или Set. Эти сведения будут храниться в двух байтах (16 бит) из [PROFILER_HEAP_OBJECT_RELATIONSHIP.relationshipInfo](../../winscript/reference/profiler-heap-object-relationship-structure.md) поле как один из [PROFILER_HEAP_OBJECT_RELATIONSHIP_FLAGS](../../winscript/reference/profiler-heap-object-relationship-flags-enumeration.md) значения перечисления.|  
|PROFILER_HEAP_ENUM_FLAGS_SUBSTRINGS|0x00000002|Этот объект кучи используется для правильного отображения подстроки.|  
|PROFILER_HEAP_ENUM_FLAGS_RELATIONSHIP_SUBSTRINGS|PROFILER_HEAP_ENUM_FLAGS_STORE_RELATIONSHIP_FLAGS &#124; PROFILER_HEAP_ENUM_FLAGS_SUBSTRINGS|Этот объект кучи используется для правильного отображения подстроки.|