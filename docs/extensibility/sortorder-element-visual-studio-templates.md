---
title: Элемент SortOrder (шаблоны Visual Studio) | Документация Майкрософт
ms.date: 11/04/2016
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/vstemplate/2005#SortOrder
helpviewer_keywords:
- SortOrder element [Visual Studio Templates]
- <SortOrder> element [Visual Studio Templates]
ms.assetid: 151932c1-f08a-4f78-a8d0-bd2f32211a9c
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 6af40c2af3a16f313ea9eac496198562c7678165
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/25/2019
ms.locfileid: "54960013"
---
# <a name="sortorder-element-visual-studio-templates"></a>Элемент SortOrder (шаблоны Visual Studio)
Указывает значение, которое используется для размещения шаблона, других шаблонов в той же категории, как оно отображается в любом **новый проект** или **Добавление нового элемента** диалоговое окно.  
  
 \<VSTemplate >  
 \<TemplateData >  
 \<SortOrder >  
  
## <a name="syntax"></a>Синтаксис  
  
```  
<SortOrder> ... </SortOrder>  
```  
  
## <a name="attributes-and-elements"></a>Атрибуты и элементы  
 В следующих разделах описаны атрибуты, дочерние и родительские элементы.  
  
### <a name="attributes"></a>Атрибуты  
 Отсутствует.  
  
### <a name="child-elements"></a>Дочерние элементы  
 Отсутствует.  
  
### <a name="parent-elements"></a>Родительские элементы  
  
|Элемент|Описание|  
|-------------|-----------------|  
|[TemplateData](../extensibility/templatedata-element-visual-studio-templates.md)|Обязательный элемент.<br /><br /> Определяет категорию шаблона и то, отображается ли он в диалоговом окне **Новый проект** или **Добавить новый элемент** .|  
  
## <a name="text-value"></a>Текстовое значение  
 Текстовое значение является обязательным.  
  
 `integer` , Представляющий значения порядка сортировки.  
  
## <a name="remarks"></a>Примечания  
 `SortOrder` — это необязательный элемент. Значение по умолчанию — 100, а все значения должны быть кратными 10.  
  
 `SortOrder` Элемент игнорируется для шаблонов, созданных пользователем. Все шаблоны, созданные пользователем сортируются в алфавитном порядке.  
  
 Шаблоны, в которых малыми значениями порядка сортировки присутствующие в одной **новый проект** или **добавить новый элемент** диалоговое окно перед шаблонами с высокими значениями порядка сортировки.  
  
## <a name="example"></a>Пример  
 В следующем примере показано метаданные для стандартного [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] шаблона класса.  
  
```  
<VSTemplate Type="Item" Version="3.0.0"  
    xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">  
    <TemplateData>  
        <Name>MyClass</Name>  
        <Description>My custom C# class template.</Description>  
        <Icon>Icon.ico</Icon>  
        <ProjectType>CSharp</ProjectType>  
        <SortOrder>290</SortOrder>  
        <DefaultName>MyClass</DefaultName>  
    </TemplateData>  
    <TemplateContent>  
        <ProjectItem>MyClass.cs</ProjectItem>  
    </TemplateContent>  
</VSTemplate>  
```  
  
 В этом примере `SortOrder` элемент относительно велико. Вполне вероятно, что другие [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] будет иметь шаблоны элементов `SortOrder` меньшее значение, чем `290` и будет отображаться перед этот шаблон в **новый элемент** диалоговое окно.  
  
## <a name="see-also"></a>См. также  
 [Справочник по схеме шаблонов Visual Studio](../extensibility/visual-studio-template-schema-reference.md)   
 [Создание шаблонов проектов и элементов](../ide/creating-project-and-item-templates.md)