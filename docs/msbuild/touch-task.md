---
title: Задача Touch | Документация Майкрософт
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#Touch
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild, Touch task
- Touch task [MSBuild]
ms.assetid: 8a978645-1393-4904-ae69-42afabd8c109
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: c9ce9b12d67a43f290f6a83e85668233050d4047
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/02/2019
ms.locfileid: "53854728"
---
# <a name="touch-task"></a>Touch - задача
Задает время доступа и изменения файлов.  
  
## <a name="parameters"></a>Параметры  
 В следующей таблице приводятся параметры задачи `Touch` .  
  
|Параметр|Описание|  
|---------------|-----------------|  
|`AlwaysCreate`|Необязательный параметр `Boolean` .<br /><br /> Если `true`, создаются файлы, которые еще не существуют.|  
|`Files`|Обязательный параметр <xref:Microsoft.Build.Framework.ITaskItem>`[]`.<br /><br /> Определяет коллекцию файлов для изменения.|  
|`ForceTouch`|Необязательный параметр `Boolean` .<br /><br /> Если `true`, вызывает принудительное изменение файлов, даже если они доступны только для чтения.|  
|`Time`|Необязательный параметр `String` .<br /><br /> Задает время, отличное от текущего. Формат должен быть допустимым для метода <xref:System.DateTime.Parse%2A>.|  
|`TouchedFiles`|Необязательный выходной параметр <xref:Microsoft.Build.Framework.ITaskItem>`[]` .<br /><br /> Содержит коллекцию успешно измененных элементов.|  
  
## <a name="remarks"></a>Примечания  
 Помимо перечисленных выше параметров, эта задача наследует параметры от класса <xref:Microsoft.Build.Tasks.TaskExtension>, который, в свою очередь, наследует от класса <xref:Microsoft.Build.Utilities.Task>. Список этих дополнительных параметров и их описания см. в статье [Базовый класс TaskExtension](../msbuild/taskextension-base-class.md).  
  
## <a name="example"></a>Пример  
 В следующем примере используется задача `Touch` для изменения времени доступа и изменения файлов, указанных в элементе `Files` коллекции с последующим размещением списка успешно измененных файлов в коллекцию элементов `FilesTouched`.  
  
```xml  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
  
<ItemGroup>  
    <Files Include="File1.cs;File2.cs;File3.cs" />  
</ItemGroup>  
  
    <Target Name="TouchFiles">  
        <Touch  
            Files="@(Files)">  
            <Output  
                TaskParameter="TouchedFiles"  
                ItemName="FilesTouched"/>  
    </Touch>  
</Target>  
</Project>  
```  
  
## <a name="see-also"></a>См. также  
 [Задачи](../msbuild/msbuild-tasks.md)   
 [Справочные сведения о задачах](../msbuild/msbuild-task-reference.md)