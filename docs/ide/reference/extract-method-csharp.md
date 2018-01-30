---
title: "Извлечение метода в C# | Документация Майкрософт"
ms.custom: 
ms.date: 11/16/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: ghogen
f1_keywords: vs.csharp.refactoring.extractmethod
dev_langs: csharp
ms.workload: dotnet
ms.openlocfilehash: 805d215eb5d885d8ab38aa288ef2c8fd3e7e90cf
ms.sourcegitcommit: f89ed5fc2e5078213e30a6ade4604e34df48181f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/13/2018
---
# <a name="extract-a-method-in-c"></a>Извлечение метода в C# #

**Что?** Вы можете преобразовать фрагмент кода в отдельный метод.

**Когда?** Если в каком-либо методе существует фрагмент кода, который должен вызываться в другом методе.

**Зачем?** Вы можете скопировать и вставить этот код, но это приведет к дублированию.  Лучше выполнить рефакторинг этого фрагмента в отдельный метод, который можно свободно вызывать в любом другом методе.

**Как?**

1. Выделите код, который требуется извлечь:

   ![Выделенный код](media/extractmethod-highlight-cs.png)

1. Затем выполните одно из следующих действий:
   * **Клавиатура**
     * Нажмите клавиши **CTRL+R**, а затем — **CTRL+M**.  (Обратите внимание, что сочетание клавиш может отличаться в зависимости от выбранного профиля.)
     * Нажмите клавиши **CTRL+.**, чтобы активировать меню **Быстрые действия и рефакторинг**. Затем во всплывающем окне предварительного просмотра выберите пункт **Извлечь метод**.
   * **Мышь**
     * Выберите **Правка > Рефакторинг > Извлечь метод**.
     * Щелкните код правой кнопкой мыши и выберите **Рефакторинг > Извлечь > Извлечь метод**.
     * Щелкните код правой кнопкой мыши и выберите меню **Быстрые действия и рефакторинг**. Затем во всплывающем окне предварительного просмотра выберите пункт **Извлечь метод**.

   Метод будет создан немедленно.  Теперь вы можете переименовать метод. Для этого просто введите новое имя.

   > [!TIP]
   > Вы также можете обновить комментарии и другие строки, чтобы в них использовалось это новое имя. Также вы можете [просмотреть изменения](../../ide/preview-changes.md), прежде чем сохранить их. Для этого установите флажки в диалоговом окне **Переименование**, которое отображается в верхней правой части среды IDE.

   ![Переименование метода](media/extractmethod-rename-cs.png)

1. Если вы довольны результатами, щелкните **Применить** или нажмите клавишу **ВВОД**, чтобы зафиксировать изменения.

## <a name="see-also"></a>См. также

[Рефакторинг](../refactoring-in-visual-studio.md)  
[Просмотр изменений](../../ide/preview-changes.md)