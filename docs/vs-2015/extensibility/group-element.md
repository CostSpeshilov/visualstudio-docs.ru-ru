---
title: Элемент Group | Документация Майкрософт
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- VSCT XML schema elements, Groups
- Groups element (VSCT XML schema)
ms.assetid: 69faee18-cbf4-470a-b952-c1919c583df8
caps.latest.revision: 10
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: dd9dda00c88a0702c6ce1efc4ff5816ac5e1d498
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/16/2018
ms.locfileid: "51817260"
---
# <a name="group-element"></a>Элемент Group
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Определяет группу команды VSPackage.  
  
## <a name="syntax"></a>Синтаксис  
  
```  
<Group guid="guidMyCommandSet" id="MyGroup" priority="0x101">  
  <Parent>... </Parent>  
</Group>  
```  
  
## <a name="attributes-and-elements"></a>Атрибуты и элементы  
 В следующих разделах описаны атрибуты, дочерние и родительские элементы.  
  
### <a name="attributes"></a>Атрибуты  
  
|Атрибут|Описание:|  
|---------------|-----------------|  
|guid|Обязательно. Идентификатор GUID идентификатора GUID и идентификатора команды.|  
|id|Обязательно. Идентификатор GUID и идентификатора идентификатор команды.|  
|priority|Необязательный. Числовое значение, указывающее приоритет.|  
|Условие|Необязательный. См. в разделе [условные атрибуты](../extensibility/vsct-xml-schema-conditional-attributes.md).|  
  
### <a name="child-elements"></a>Дочерние элементы  
  
|Элемент|Описание:|  
|-------------|-----------------|  
|Родительский|Необязательный. Родительский элемент кнопки.|  
|Комментарий|Дополнительный комментарий.|  
  
### <a name="parent-elements"></a>Родительские элементы  
  
|Элемент|Описание:|  
|-------------|-----------------|  
|[Элемент Groups](../extensibility/groups-element.md)|Содержит записи, которые определяют группы команд пакета VSPackage.|  
  
## <a name="example"></a>Пример  
  
```  
<Group guid="cmdSetGuidWidgetCommands" id="groupIDFileEdit">  
  <Parent guid="guidSHLMainMenu" id="IDM_VS_TOOL_MAINMENU"/>  
</Group>  
```  
  
## <a name="see-also"></a>См. также  
 [Файлы таблицы команд Visual Studio (VSCT-файлы)](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)

