---
title: "Извлечение метода в Visual Studio | Документы Майкрософт"
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
- vs.csharp.refactoring.extractmethod
dev_langs:
- CSharp
- VB
ms.workload:
- dotnet
ms.openlocfilehash: d66a0e41f0c68d3d5c4378a664ef36aba0d869b7
ms.sourcegitcommit: 8cbe6b38b810529a6c364d0f1918e5c71dee2c68
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/28/2018
---
# <a name="extract-a-method-refactoring"></a>Рефакторинг для извлечения метода

Область применения этого рефакторинга:

- C#

- Visual Basic

**Что?** Вы можете преобразовать фрагмент кода в отдельный метод.

**Когда?** Если в каком-либо методе существует фрагмент кода, который должен вызываться в другом методе.

**Зачем?** Вы можете скопировать и вставить этот код, но это приведет к дублированию. Лучше выполнить рефакторинг этого фрагмента в отдельный метод, который можно свободно вызывать в любом другом методе.

## <a name="how-to"></a>Практические советы

1. Выделите код, который требуется извлечь:

   - C#:

    ![Выделенный код — C#](media/extractmethod-highlight-cs.png)

   - Visual Basic:

    ![Выделенный код — Visual Basic](media/extractmethod-highlight-vb.png)

1. Затем выполните одно из следующих действий:

   - **Клавиатура**
     - Нажмите клавиши **CTRL+R**, а затем — **CTRL+M**. (Обратите внимание, что сочетание клавиш может отличаться в зависимости от выбранного профиля.)
     - Нажмите клавиши **CTRL**+**.** чтобы активировать меню **Быстрые действия и рефакторинг**. Затем во всплывающем окне предварительного просмотра выберите пункт **Извлечь метод**.
   - **Мышь**
     - Выберите **Правка > Рефакторинг > Извлечь метод**.
     - Щелкните код правой кнопкой мыши и выберите **Рефакторинг > Извлечь > Извлечь метод**.
     - Щелкните код правой кнопкой мыши и выберите меню **Быстрые действия и рефакторинг**. Затем во всплывающем окне предварительного просмотра выберите пункт **Извлечь метод**.

   Метод будет создан немедленно. Теперь вы можете переименовать метод. Для этого просто введите новое имя.

   > [!TIP]
   > Вы также можете обновить комментарии и другие строки, чтобы в них использовалось это новое имя. Также вы можете [просмотреть изменения](../../ide/preview-changes.md), прежде чем сохранить их. Для этого установите флажки в диалоговом окне **Переименование**, которое отображается в верхней правой части среды IDE.

   - C#:

    ![Переименование метода — C#](media/extractmethod-rename-cs.png)

   - Visual Basic:

    ![Переименование метода — Visual Basic](media/extractmethod-rename-vb.png)

1. Если вы довольны результатами, выберите **Применить** или нажмите клавишу **ВВОД**, чтобы зафиксировать изменения.

## <a name="see-also"></a>См. также

- [Рефакторинг](../refactoring-in-visual-studio.md)
- [Просмотр изменений](../../ide/preview-changes.md)