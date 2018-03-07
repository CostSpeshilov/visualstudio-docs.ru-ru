---
title: "Перемещение объявления переменной рядом со ссылкой в Visual Studio | Документы Майкрософт"
ms.custom: 
ms.date: 01/26/2018
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.topic: reference
author: kuhlenh
ms.author: kaseyu
manager: ghogen
dev_langs:
- csharp
ms.workload:
- dotnet
ms.openlocfilehash: a76e6024a2b61bcae08fb8db169483bcee6e5d19
ms.sourcegitcommit: 8cbe6b38b810529a6c364d0f1918e5c71dee2c68
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/28/2018
---
# <a name="move-declaration-near-reference-refactoring"></a>Рефакторинг для перемещения объявления рядом со ссылкой

Область применения этого рефакторинга:

- C#

**Что?** Вы можете переместить объявления переменных в расположение, соответствующее их использованию.

**Когда?** У вас есть объявления переменных, которые могут находиться в более узкой области.

**Зачем?** Вы можете оставить все как есть, но это может привести к проблемам с удобочитаемостью или отображением информации. Такой рефакторинг позволяет повысить удобочитаемость.

## <a name="how-to"></a>Практические советы

1. Поместите курсор в объявление переменной.

1. Затем выполните одно из следующих действий:

   - **Клавиатура**
     - Нажмите клавиши **CTRL**+**.** чтобы активировать меню **Быстрые действия и рефакторинг**. Затем выберите во всплывающем окне предварительного просмотра пункт **Переместить объявление рядом со ссылкой**.
   - **Мышь**
     - Щелкните код правой кнопкой мыши и выберите меню **Быстрые действия и рефакторинг**. Затем выберите во всплывающем окне предварительного просмотра пункт **Переместить объявление рядом со ссылкой**.

1. Если вы довольны результатами, нажмите клавишу **ВВОД** или выберите соответствующий пункт в меню, чтобы зафиксировать изменения.

Пример

```csharp
// Before
int x;
if (condition)
{
    x = 1;
    Console.WriteLine(x);
}

// Move declaration near reference

// After
if (condition)
{
    int x = 1;
    Console.WriteLine(x);
}
```

## <a name="see-also"></a>См. также

- [Рефакторинг](../refactoring-in-visual-studio.md)
- [Просмотр изменений](../../ide/preview-changes.md)