---
title: Конструктор действия FinalState | Документация Майкрософт
ms.custom: ''
ms.date: 11/15/2016
ms.prod: .net-framework-4.6
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: aa186893-8775-40dd-981f-8593ead831d0
caps.latest.revision: 5
author: steved0x
ms.author: gewarren
manager: erikre
ms.openlocfilehash: 48c44dc585ce1c9cf4e7b29970b4014f128b873d
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/12/2018
ms.locfileid: "49209174"
---
# <a name="finalstate-activity-designer"></a>Конструктор FinalState Activity
Конструктор <xref:System.Activities.Core.Presentation.FinalState> используется для создания <xref:System.Activities.Statements.State>, которое завершает экземпляр конечного автомата.  
  
## <a name="using-the-finalstate-activity-designer"></a>Использование конструктора действий FinalState  
 **FinalState** конструктор используется для создания <xref:System.Activities.Statements.State> , предварительно настраиваемого как завершающее состояние конечного автомата. Объект <xref:System.Activities.Statements.State> , созданного при помощи <xref:System.Activities.Core.Presentation.FinalState> имеет конструктор действия его <xref:System.Activities.Statements.State.IsFinal%2A> свойство значение **true**, не имеет <xref:System.Activities.Statements.State.Exit%2A> действия и не переходы, исходящие из него. Чтобы использовать <xref:System.Activities.Core.Presentation.FinalState> конструктора действий, чтобы добавить <xref:System.Activities.Statements.State> действие, которое предварительно настроенного как завершающее состояние конечного автомата, перетащите **FinalState** конструктор из **конечный автомат**раздел **элементов** и поместите его в конструктор рабочего процесса. Конструктор действий <xref:System.Activities.Core.Presentation.FinalState> можно перетащить в <xref:System.Activities.Statements.StateMachine> и переходы, добавленные позже. Переход также можно создать при сбросе конструктора действий <xref:System.Activities.Core.Presentation.FinalState> на поверхность. Дополнительные сведения о создании переходов см. в разделе [перехода](../workflow-designer/transition-activity-designer.md).  
  
### <a name="state-activity-properties-in-the-workflow-designer"></a>Свойства действия состояния в конструкторе рабочих процессов  
 В следующей таблице приведены свойства, которые можно задать с помощью конструктора <xref:System.Activities.Core.Presentation.FinalState>, и описано их использование в конструкторе. Некоторые из этих свойств можно изменить в таблице свойств, а некоторые из них ― в области конструктора.  
  
|Имя свойства|Обязательно|Использование|  
|-------------------|--------------|-----------|  
|<xref:System.Activities.Statements.State.DisplayName%2A>|False|Указывает дополнительное понятное имя конструктора действия <xref:System.Activities.Statements.State> в заголовке. Значение по умолчанию — **состояние**. Значение можно дополнительно изменить в таблице свойств или напрямую в заголовке конструктора операций. <xref:System.Activities.Statements.State.DisplayName%2A> используется в строке навигатора, которая отображается в верхней части конструктора рабочих процессов.<br /><br /> Несмотря на то что свойство <xref:System.Activities.Statements.State.DisplayName%2A> не является обязательным, его все же рекомендуется использовать.|  
|<xref:System.Activities.Statements.State.Entry%2A>|False|Указывает действие, которое выполняется при переходе в это состояние. Это значение может быть задано путем перетаскивания действия из **элементов** и помещения его в <xref:System.Activities.Statements.State.Entry%2A> раздел состояния.|  
  
## <a name="see-also"></a>См. также  
 [Конечный автомат](../workflow-designer/statemachine-activity-designer.md)   
 [Состояние](../workflow-designer/state-activity-designer.md)   
 [Transition](../workflow-designer/transition-activity-designer.md)