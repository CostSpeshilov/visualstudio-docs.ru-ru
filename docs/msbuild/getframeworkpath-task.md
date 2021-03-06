---
title: Задача GetFrameworkPath | Документы Майкрософт
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#GetFrameworkPath
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- GetFrameworkPath task [MSBuild]
- MSBuild, GetFrameworkPath task
ms.assetid: 5b7bcdd7-d4a0-442d-af29-8aadb3b10598
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 2eeee3865a9b2a607df48ca6d9ade1990401f759
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/02/2019
ms.locfileid: "53944870"
---
# <a name="getframeworkpath-task"></a>GetFrameworkPath - задача
Извлекает путь к сборкам [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)].  
  
## <a name="task-parameters"></a>Параметры задачи  
 В следующей таблице приводятся параметры задачи `GetFrameworkPath` .  
  
|Параметр|Описание|  
|---------------|-----------------|  
|`FrameworkVersion11Path`|Необязательный выходной параметр `String`.<br /><br /> Содержит путь к сборкам платформы .NET Framework версии 1.1, если они есть. В противном случае возвращает значение `null`.|  
|`FrameworkVersion20Path`|Необязательный выходной параметр `String`.<br /><br /> Содержит путь к сборкам платформы .NET Framework версии 2.0, если они есть. В противном случае возвращает значение `null`.|  
|`FrameworkVersion30Path`|Необязательный выходной параметр `String`.<br /><br /> Содержит путь к сборкам платформы .NET Framework версии 3.0, если они есть. В противном случае возвращает значение `null`.|  
|`FrameworkVersion35Path`|Необязательный выходной параметр `String`.<br /><br /> Содержит путь к сборкам платформы .NET Framework версии 3.5, если они есть. В противном случае возвращает значение `null`.|  
|`FrameworkVersion40Path`|Необязательный выходной параметр `String`.<br /><br /> Содержит путь к сборкам платформы .NET Framework версии 4.0, если они есть. В противном случае возвращает значение `null`.|  
|`Path`|Необязательный выходной параметр `String`.<br /><br /> Содержит путь к самым новым сборкам платформы, если они есть. В противном случае возвращает значение `null`.|  
  
## <a name="remarks"></a>Примечания  
 Если установлено несколько версий [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)], эта задача возвращает версию, для которой предназначен [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)].  
  
 Помимо перечисленных выше параметров, эта задача наследует параметры от класса <xref:Microsoft.Build.Tasks.TaskExtension>, который, в свою очередь, наследует от класса <xref:Microsoft.Build.Utilities.Task>. Список этих дополнительных параметров и их описания см. в статье [Базовый класс TaskExtension](../msbuild/taskextension-base-class.md).  
  
## <a name="example"></a>Пример  
 Следующий пример использует задачу `GetFrameworkPath` для сохранения пути к [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] в свойстве `FrameworkPath`.  
  
```xml  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
    <Target Name="GetPath">  
        <GetFrameworkPath>  
            <Output  
                TaskParameter="Path"  
                PropertyName="FrameworkPath" />  
        </GetFrameworkPath>  
    </Target>  
</Project>  
```  
  
## <a name="see-also"></a>См. также  
 [Задачи](../msbuild/msbuild-tasks.md)   
 [Справочные сведения о задачах](../msbuild/msbuild-task-reference.md)