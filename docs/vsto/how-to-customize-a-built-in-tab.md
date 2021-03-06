---
title: Как выполнить Настройка встроенной вкладки
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Ribbon [Office development in Visual Studio], tabs
- built-in tabs [Office development in Visual Studio]
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 939c9c6d2d50e9feb6a50d9b49b84620d96a03cc
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/24/2019
ms.locfileid: "54872226"
---
# <a name="how-to-customize-a-built-in-tab"></a>Как выполнить Настройка встроенной вкладки
  На встроенную вкладку можно добавить группы и элементы управления. Встроенная вкладка — это вкладка, которая уже есть на ленте приложения Microsoft Office. Например **данных** вкладка — это встроенная вкладка Excel. При создании настраиваемой группы она отображается на вкладке последней, но вы можете свободно перемещать группу на вкладке.  
  
 [!INCLUDE[appliesto_ribbon](../vsto/includes/appliesto-ribbon-md.md)]  
  
> [!NOTE]  
>  На встроенную вкладку можно добавлять группы, но нельзя удалить встроенные группы из встроенной вкладки.  
  
### <a name="to-add-groups-to-a-built-in-tab"></a>Добавление групп на встроенную вкладку  
  
1.  Щелкните правой кнопкой мыши файл кода ленты в **обозревателе решений**, а затем нажмите кнопку **конструктор представлений**.  
  
    > [!NOTE]  
    >  Если файл кода ленты не отображается в **обозревателе решений**, необходимо добавить **элемент ленты** в проект. См. практическое руководство по [ Приступая к настройке ленты](../vsto/how-to-get-started-customizing-the-ribbon.md).  
  
2.  Щелкните правой кнопкой мыши одну из вкладок в конструкторе лент, а затем нажмите кнопку **свойства**.  
  
3.  В **свойства** окне разверните **ControlId** свойства, а затем задайте **ControlIdType** свойства **Office**.  
  
4.  Задайте **OfficeId** свойства *идентификатор элемента управления* встроенной вкладки, которую нужно настроить.  
  
     Идентификатор элемента управления — это имя, однозначно определяющее вкладки, группы и элементы управления, которые встроены в приложения Microsoft Office.  
  
     Список идентификаторов элементов управления, см. в разделе [файлы справки Office 2010: Идентификаторы элементов управления интерфейса Office fluent пользователя](http://go.microsoft.com/fwlink/?LinkID=181052).  
  
5.  Из **элементы управления ленты Office** вкладке **элементов**, перетащите групп на вкладку.  
  
    > [!NOTE]  
    >  Встроенные группы не отображается в конструкторе. Таким образом, единственный способ определить, работаете ли вы со встроенной вкладкой является изучаемый **ControlId** свойство вкладки.  
  
### <a name="to-position-groups-on-a-built-in-tab"></a>Размещение групп на встроенной вкладке  
  
1.  В конструкторе лент выберите настраиваемую группу.  
  
2.  В **свойства** окне разверните **позиции** свойство.  
  
3.  Задайте **PositionType** свойство с соответствующим значением:  
  
    -   **BeforeOfficeId** размещает группу перед указанной встроенной группой.  
  
    -   **AfterOfficeId** размещает группу после указанной встроенной группы.  
  
4.  Задайте **OfficeId** свойство идентификатора встроенной группы.  
  
     Список идентификаторов элементов управления, см. в разделе [файлы справки Office 2010: Идентификаторы элементов управления интерфейса Office fluent пользователя](http://go.microsoft.com/fwlink/?LinkID=181052).  
  
## <a name="see-also"></a>См. также  
 [Обзор ленты](../vsto/ribbon-overview.md)   
 [Конструктор лент](../vsto/ribbon-designer.md)   
 [XML-ленты](../vsto/ribbon-xml.md)   
 [Пошаговое руководство: Создание настраиваемой вкладки с помощью конструктора лент](../vsto/walkthrough-creating-a-custom-tab-by-using-the-ribbon-designer.md)   
 [Пошаговое руководство: Создание настраиваемой вкладки с помощью XML-ленты](../vsto/walkthrough-creating-a-custom-tab-by-using-ribbon-xml.md)   
 [Практическое руководство. Приступая к настройке ленты](../vsto/how-to-get-started-customizing-the-ribbon.md)   
 [Практическое руководство. Изменение положения вкладки на ленте](../vsto/how-to-change-the-position-of-a-tab-on-the-ribbon.md)   
 [Практическое руководство. Добавление элементов управления в представление Backstage](../vsto/how-to-add-controls-to-the-backstage-view.md)   
 [Практическое руководство. Показывать ошибки надстройки пользовательского интерфейса](../vsto/how-to-show-add-in-user-interface-errors.md)  
