---
title: Конструктор рабочих процессов - диалоговое окно редактора коллекций типов
ms.date: 11/04/2016
ms.topic: reference
ms.prod: visual-studio-dev15
f1_keywords:
- TypeCollectionEditor.UI
ms.assetid: 63cdea6b-bca2-4c06-b8b4-c8faabd40726
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 257091b6693bdf37c063b1bc992bdec4531e1710
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/25/2019
ms.locfileid: "55036112"
---
# <a name="type-collection-editor-dialog-box"></a>Диалоговое окно редактора коллекций типов

**Редактор коллекции типов** диалоговое окно используется для добавления известных типов для **отправки** и **Receive** действий. Это диалоговое окно также используется для добавления аргументов универсального типа для **InvokeMethod** действия. При использовании для **отправки** и **Receive** действия для добавления известных типов **редактор коллекции типов** диалоговое окно требует добавления типов должны быть уникальными. При добавлении дублирующего типа и подтверждении, нажав кнопку **ОК**, возвращается сообщение об ошибке. При использовании для **InvokeMethod** действия для добавления аргументов универсального типа, **редактор коллекции типов** диалоговое окно позволяет добавлять дублирующих типов.

Дополнительные сведения см. в разделе [известные типы контрактов данных](/dotnet/framework/wcf/feature-details/data-contract-known-types).

В следующей таблице описаны элементы пользовательского интерфейса (UI) **коллекция типов** диалоговое окно.

|Элемент пользовательского интерфейса|Описание:|
|-|-----------------|
|**Список типов**|Список добавленных или удаленных типов объектов.|

## <a name="to-bring-up-the-type-collection-editor-for-the-send-and-receive-activities"></a>Отображение редактора коллекций типов для действий Send и Receive

1.  Выберите **отправки** или **Receive** действий в представлении конструктора.

2.  Нажмите клавишу **F4** откроется **свойства** окна.

3.  В **свойства** окно, нажмите кнопку с многоточием, расположенную рядом с полем **KnownTypes** свойство.

## <a name="to-bring-up-the-type-collection-editor-for-the-invokemethod-activity"></a>Отображение редактора коллекций типов для действия InvokeMethod

1.  Выберите **InvokeMethod** действий в представлении конструктора.

2.  Нажмите клавишу **F4** откроется **свойства** окна.

3.  В **свойства** окно, нажмите кнопку с многоточием, расположенную рядом с полем **GenericTypeArguments** свойство.