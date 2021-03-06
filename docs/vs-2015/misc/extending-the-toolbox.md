---
title: Расширение панели элементов | Документация Майкрософт
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- devlang-csharp
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- tools [Visual Studio], Toolbox
- Toolbox [Visual Studio SDK]
ms.assetid: bb84a79e-cd4c-4a58-8871-2513e7119b6e
caps.latest.revision: 38
manager: douge
ms.openlocfilehash: 444cf6b27179408414cc7df55d634497683004a6
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/12/2018
ms.locfileid: "49230338"
---
# <a name="extending-the-toolbox"></a>Расширение панели элементов
[!INCLUDE[vsprvs](../includes/vsprvs-md.md)] **Панель элементов** представляет коллекцию объектов, которые предоставляют функциональные возможности в редакторах и конструкторах через механизм перетаскивания IDE.  
  
 Существует два основных способа, которыми VSPackage работает с [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] **панелью элементов**.  
  
-   VSPackage может добавлять в **панель элементов**новые элементы данных и элементы управления.  
  
-   VSPackage может быть целевым объектом или потребителем существующих функциональных возможностей **панели элементов** с поддержкой операций перетаскивания и настройки внешнего вида **панели элементов**.  
  
## <a name="in-this-section"></a>В этом разделе  
 [Практическое руководство. Создание элемента управления панели элементов, использующего Windows Forms](../misc/how-to-create-a-toolbox-control-that-uses-windows-forms.md)  
 Описывается создание элемента управления "Панель элементов" с помощью шаблона элемента управления панели элементов Windows Forms.  
  
 [Создание элемента управления панели элементов WPF](../extensibility/creating-a-wpf-toolbox-control.md)  
 Описывается создание элемента управления "Панель элементов" с помощью шаблона элемента управления панели элементов WPF.  
  
 [Управление панелью элементов](../misc/managing-the-toolbox.md)  
 Описывается, как VSPackage может управлять содержимым и внешним видом **панели элементов**.  
  
## <a name="related-sections"></a>Связанные разделы  
 [Практическое руководство. Управление окном панели элементов](http://msdn.microsoft.com/en-us/a022c3fe-298c-4a59-a48f-b050da90ebc2)  
 Описывается, как работать с **панелью элементов** в интегрированной среде разработки (IDE) [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] .  
  
 [Практическое: Control the Toolbox](http://msdn.microsoft.com/library/c9d8a18a-d2bc-43d4-a803-601bfc6a6599)  
 Описывается, как управлять **панелью элементов** с помощью модели программирования автоматизации.  
  
 [Расширение других частей Visual Studio](../extensibility/extending-other-parts-of-visual-studio.md)  
 Объясняется использование служб [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] для создания элементов пользовательского интерфейса, соответствующих остальным частям [!INCLUDE[vsprvs](../includes/vsprvs-md.md)].