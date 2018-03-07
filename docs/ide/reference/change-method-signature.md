---
title: "Рефакторинг сигнатуры метода на Visual Studio | Документы Майкрософт"
ms.custom: 
ms.date: 01/26/2018
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: ghogen
f1_keywords:
- vs.csharp.refactoring.remove
- vs.csharp.refactoring.reorder
dev_langs:
- CSharp
- VB
ms.workload:
- dotnet
ms.openlocfilehash: c181eb27ccdbc2f1efb7294e1610a6055245241c
ms.sourcegitcommit: 8cbe6b38b810529a6c364d0f1918e5c71dee2c68
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/28/2018
---
# <a name="change-a-method-signature-refactoring"></a>Рефакторинг для изменения сигнатуры метода

Область применения этого рефакторинга:

- C#

- Visual Basic

**Что?** Это средство позволяет удалить или изменить порядок параметров метода.

**Когда?** Если нужно переместить или удалить параметр метода, который сейчас используется в различных расположениях.

**Зачем?** Вы можете вручную удалить параметры и изменить их порядок, а затем найти все вызовы этого метода и изменить их по одному, но это может привести к ошибкам.  Это средство рефакторинга выполнит указанную задачу автоматически.

## <a name="how-to"></a>Практические советы

1. Выделите имя метода (или один из вариантов его использования), который требуется изменить, либо поместите в него текстовый курсор:

   - C#:

    ![Выделенный код C#](media/changesignature-highlight-cs.png)

   - VB:

    ![выделенный код Visual Basic](media/changesignature-highlight-vb.png)

1. Затем выполните одно из следующих действий:

   - **Клавиатура**
     - Нажмите клавиши **CTRL+R**, а затем — **CTRL+V**.  (Обратите внимание, что сочетание клавиш может отличаться в зависимости от выбранного профиля.)
     - Нажмите клавиши **CTRL**+**.** чтобы активировать меню **Быстрые действия и рефакторинг**. Затем во всплывающем окне предварительного просмотра выберите пункт **Изменить сигнатуру**.
   - **Мышь**
     - Последовательно выберите **Правка > Рефакторинг > Удалить параметры**.
     - Последовательно выберите **Правка > Рефакторинг > Упорядочить параметры**.
     - Щелкните код правой кнопкой мыши и выберите меню **Быстрые действия и рефакторинг**. Затем во всплывающем окне предварительного просмотра выберите пункт **Изменить сигнатуру**.

1. Во всплывающем диалоговом окне **Изменить сигнатуру** воспользуйтесь кнопками справа, чтобы изменить сигнатуру метода.

   ![Диалоговое окно "Изменить сигнатуру"](media/changesignature-dialog-cs.png)

   | Кнопка | Описание:
   | ------ | ---
   | **Up/Down** | Перемещение выбранного параметра вверх или вниз в списке.
   | **Remove**  | Удаление выбранного параметра из списка.
   | **Восстановить** | Восстановление выбранного удаленного параметра в списке.

   > [!TIP]
   > Установите флажок **Просмотр изменений ссылок**, чтобы узнать, [каким будет результат](../../ide/preview-changes.md), прежде чем зафиксировать его.

1. По завершении нажмите кнопку **ОК**, чтобы применить изменения.

   - C#:

    ![Результат изменения сигнатуры — C#](media/changesignature-result-cs.png)

   - Visual Basic:

    ![Результат изменения сигнатуры — Visual Basic](media/changesignature-result-vb.png)

## <a name="see-also"></a>См. также

- [Рефакторинг](../refactoring-in-visual-studio.md)
- [Просмотр изменений](../../ide/preview-changes.md)