---
title: Конструктор рабочих процессов - конструктор действия TerminateWorkflow
ms.date: 11/04/2016
ms.topic: reference
ms.prod: visual-studio-dev15
f1_keywords:
- System.Activities.Statements.TerminateWorkflow.UI
ms.assetid: 08e632ed-0724-4fb4-9df1-f8d443eaf0ac
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 3a065deebe0629cb353acc64d6d40db8a4e00b3d
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/25/2019
ms.locfileid: "54993264"
---
# <a name="terminateworkflow-activity-designer"></a>Конструктор действия TerminateWorkflow

**TerminateWorkflow** конструктора действий используется для создания и настройки <xref:System.Activities.Statements.TerminateWorkflow> действия.

## <a name="the-terminateworkflow-activity"></a>Действие TerminateWorkflow

Действие <xref:System.Activities.Statements.TerminateWorkflow> прерывает выполнение текущего рабочего процесса.

### <a name="using-the-terminateworkflow-activity-designer"></a>Использование конструктора операций TerminateWorkflow

**TerminateWorkflow** конструктора действий можно найти в **среды выполнения** категории **элементов**, который нажав **панелиэлементов** вкладка (Кроме того, выберите **элементов** из **представление** меню или сочетание клавиш CTRL + ALT + X.)

**TerminateWorkflow** конструктор действия можно перетащить из **элементов** и сбрасываться в область конструктора рабочих процессов, везде, где обычно размещаются действия, например внутри <xref:System.Activities.Statements.Sequence>. При этом создается <xref:System.Activities.Statements.TerminateWorkflow> действие по умолчанию **DisplayName** для TerminateWorkflow. <xref:System.Activities.Activity.DisplayName%2A> Можно изменить в заголовке **TerminateWorkflow** конструктора действий или в **DisplayName** поле таблицы свойств.

### <a name="the-terminateworkflow-properties"></a>Свойства TerminateWorkflow

В следующей таблице показаны свойства <xref:System.Activities.Statements.TerminateWorkflow> и описано их использование в конструкторе. Эти свойства можно изменить в таблице свойств, и некоторые из них можно изменить на поверхности конструктора рабочих процессов.

|Имя свойства|Обязательно|Использование|
|-|--------------|-|
|<xref:System.Activities.Activity.DisplayName%2A>|False|Понятное имя действия <xref:System.Activities.Statements.TerminateWorkflow>. Значение по умолчанию - TerminateWorkflow. Несмотря на то что использовать отображаемое имя необязательно, его все же рекомендуется задавать.|
|<xref:System.Activities.Statements.TerminateWorkflow.Exception%2A>|False|Исключение, которое будет создано при прерывании рабочего процесса. Задайте это свойство в таблице свойств.|
|<xref:System.Activities.Statements.TerminateWorkflow.Reason%2A>|False|Причина, которая объясняет причину прерывания рабочего процесса. Задайте это свойство в таблице свойств.|

## <a name="see-also"></a>См. также

- [Среда выполнения](../workflow-designer/runtime-activity-designers.md)
- [Persist](../workflow-designer/persist-activity-designer.md)