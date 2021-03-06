---
title: Создание элементов и отношений в моделях UML | Документация Майкрософт
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-tfs-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- UML API
ms.assetid: cae81d32-8cc7-4f7c-9f00-20119952bc51
caps.latest.revision: 17
author: gewarren
ms.author: gewarren
manager: douge
ms.openlocfilehash: 5ed918bc96168196400dd34d87ec65574fdfc5b6
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/16/2018
ms.locfileid: "51785876"
---
# <a name="create-elements-and-relationships-in-uml-models"></a>Создание элементов и отношений в моделях UML
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

В программном коде расширения Visual Studio можно создавать и удалять элементы и отношения.  
  
## <a name="create-a-model-element"></a>Создание элемента модели  
  
### <a name="namespace-imports"></a>Импорт пространства имен  
 Используются следующие операторы `using`.  
  
 Методы создания определены в этом пространстве имен как  методы расширения.  
  
 `using Microsoft.VisualStudio.ArchitectureTools.Extensibility.Uml;`  
  
### <a name="obtain-the-owner-of-the-element-you-want-to-create"></a>Получение владельца элемента, который необходимо создать  
 Модель создает одно дерево, так что каждый элемент, кроме корня модели, имеет одного владельца. Корень модели имеет тип `IModel`, который является типом `IPackage`.  
  
 Создавать элемент, который будет отображаться на определенной схеме, например на текущей схеме пользователя, как правило, необходимо в пакете, связанном с этой схемой. Например:  
  
```  
IPackage linkedPackage = Context.CurrentDiagram.Element as IPackage;  
```  
  
 В следующей таблице представлены владельцы общих элементов моделей.  
  
|Создаваемый элемент|Владелец|  
|---------------------------|-----------|  
|`IActor, IUseCase, IComponent, IClass, IInterface, IEnumeration`<br /><br /> `IActivity, IInteraction`|`IPackage, IModel`|  
|`IAttribute, IOperation`|`IClass, IInterface`|  
|`IPart, IPort`|`IComponent`|  
|`IAction, IObjectNode`|`IActivity`|  
|`ILifeline, IMessage, ICombinedFragment`|`IInteraction`|  
  
### <a name="invoke-the-create-method-on-the-owner"></a>Вызов метода создания для владельца  
 Имя метода имеет форму: `Create` *OwnedType*`()`. Пример:  
  
```  
IUseCase usecase1 = linkedPackage.CreateUseCase();  
```  
  
 Некоторые типы имеют более сложные методы создания, особенно в схемах последовательностей. См. в разделе [изменение последовательностей UML с помощью UML API](../modeling/edit-uml-sequence-diagrams-by-using-the-uml-api.md).  
  
 Некоторые типы элементов допускают неоднократное изменение владельца в течение жизненного цикла. Для этого используется функция `SetOwner(newOwner)`.  
  
### <a name="set-the-name-and-other-properties"></a>Задание имени и других свойств  
  
```  
usecase1.Name = "user logs in";  
```  
  
### <a name="example"></a>Пример  
  
```  
using Microsoft.VisualStudio.Uml.Classes;  
using Microsoft.VisualStudio.Uml.Extensions;  
...  
 void InstantiateObserverPattern (IPackage package, string namePrefix)  
 {    IInterface observer = package.CreateInterface();  
      observer.Name = namePrefix + "Observer";  
      IOperation operation = observer.CreateOperation();  
      operation.Name = "Update";  
      IClass subject = package.CreateClass();  
      subject.Name = namePrefix + "Subject"; ...  
```  
  
## <a name="create-an-association"></a>Создание ассоциации  
  
#### <a name="to-create-an-association"></a>Создание ассоциации  
  
1.  Получите владельца ассоциации. Как правило, это пакет или модель, которые содержат исходное окончание отношения.  
  
2.  Вызовите для владельца требуемый метод создания.  
  
3.  Задайте свойства отношения, такие как имя.  
  
     Например:  
  
    ```  
    IAssociation association = subject.Package.CreateAssociation(subject, observer);  
    association .Name = "Observes";  
    ```  
  
4.  Задайте свойства каждого окончания отношения. Параметров `MemberEnds` всегда два. Например:  
  
    ```  
    association .MemberEnds[0].Name = "subject";   // role name  
    association .MemberEnds[1].Name = "observers"; // role name  
    association .MemberEnds[1].SetBounds("0..*");           
                // multiplicity defaults to "1"  
    association.MemberEnds[0].Aggregation = AggregationKind.Composite;  
    ```  
  
## <a name="create-a-generalization"></a>Создание обобщения  
  
```  
IGeneralization generalization =   
  subclass.CreateGeneralization(superClass);  
```  
  
## <a name="delete-an-element-relationship-or-generalization-from-the-model"></a>Удаление из модели элемента, отношения или обобщения  
  
```  
anElement.Delete();  
```  
  
 При удалении элемента из модели происходит следующее:  
  
-   Удаляется каждое связанное с ним отношение.  
  
-   Удаляется каждая фигура, которая представляет его на схеме.  
  
## <a name="see-also"></a>См. также  
 [Расширение моделей и схем UML](../modeling/extend-uml-models-and-diagrams.md)   
 [Отображение модели UML на схемах](../modeling/display-a-uml-model-on-diagrams.md)



