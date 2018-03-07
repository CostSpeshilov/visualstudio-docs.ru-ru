---
title: "Создание класса или типа в Visual Studio | Документы Майкрософт"
ms.custom: 
ms.date: 01/26/2018
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.topic: article
author: gewarren
ms.author: gewarren
manager: ghogen
f1_keywords:
- vsl.GenerateFromUsage
dev_langs:
- CSharp
- VB
ms.workload:
- dotnet
ms.openlocfilehash: 3016df12481da0a7ea81dee1ff895fc5dcbd059d
ms.sourcegitcommit: 8cbe6b38b810529a6c364d0f1918e5c71dee2c68
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/28/2018
---
# <a name="generate-a-class-or-type-in-visual-studio"></a>Создание класса или типа в Visual Studio

Область применения этого формирования кода:

- C#

- Visual Basic

**Что?** Этот компонент позволяет немедленно создать код для класса или типа.

**Когда?** Вы представляете новый класс или тип и автоматически правильно объявляете его.

**Зачем?** Вы можете объявить класс или тип перед их использованием, но эта функция позволяет создать класс или тип автоматически.

## <a name="how-to"></a>Практические советы

1. Поместите курсор в строку с красной волнистой линией. Она указывает несуществующий класс.

   - C#:

    ![Выделенный код C#](media/class-highlight-cs.png)

   - Visual Basic:

    ![Выделенный код VB](media/class-highlight-vb.png)

1. Затем выполните одно из следующих действий:

   - **Клавиатура**
     - Нажмите клавиши **CTRL**+**.** чтобы открыть меню **Быстрые действия и рефакторинг**.
   - **Мышь**
     - Щелкните правой кнопкой мыши и выберите меню **Быстрые действия и рефакторинг**.
     - Наведите указатель мыши на красную волнистую линию и щелкните появившийся значок ![Значок лампочки](media/bulb-cs.png) .
     - Нажмите кнопку ![Значок лампочки](media/bulb-cs.png) , который отображается в левом поле, если текстовый курсор уже находится в строке выбора с красной волнистой линией.

    ![Создание класса — предварительный просмотр](media/class-preview-cs.png)

1. В раскрывающемся списке выберите один из параметров:

   - Generate class "*TypeName*" in new file (Создать класс "TypeName" в новом файле)&mdash;Создает класс с именем *TypeName* в файле с именем *TypeName*.cs или TypeName.vb.
   - Generate class "*TypeName*" (Создать класс "TypeName")&mdash;Создает класс с именем *TypeName* в текущем файле.
   - Generate nested class "*TypeName*" (Создать вложенный класс "TypeName")&mdash;Создает класс с именем *TypeName* внутри текущего класса.
   - Сформировать новый тип...&mdash;Создает класс или структуру со свойствами, которые вы выберете.

   > [!TIP]
   > Щелкните ссылку **Просмотреть изменения** в нижней части окна предварительного просмотра, [чтобы просмотреть все будущие изменения](../../ide/preview-changes.md), прежде чем выбрать элементы.

1. При выборе элемента **Сформировать новый тип** открывается диалоговое окно **Сформировать тип**. Настройте доступность, вид и расположение нового типа.

   ![Формирование типа](media/class-newtype-cs.png)

   Выбранное | Описание:
   --- | ---
   Access | Задайте для этого типа доступ *По умолчанию*, *Внутренний* или *Открытый*.
   Тип | Для этого параметра можно выбрать значения *class* или *struct*.
   name | Это имя нельзя изменить. Будет использоваться имя, которое вы уже ввели.
   Проект | Если решение содержит несколько проектов, вы можете выбрать проект, в котором будут находиться класс или структура.
   Имя файла | Можно создать новый файл или добавить тип в существующий.

Создается класс или структура. Для C# также создается конструктор.

- C#

   ![Результат создания класса C#](media/class-result-cs.png)

- Visual Basic

   ![Результат создания класса VB](media/class-result-vb.png)

## <a name="see-also"></a>См. также

- [Создание кода](../code-generation-in-visual-studio.md)
- [Просмотр изменений](../../ide/preview-changes.md)