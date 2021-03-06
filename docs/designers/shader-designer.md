---
title: Конструктор шейдеров
ms.date: 09/21/2018
ms.prod: visual-studio-dev15
ms.topic: conceptual
f1_keywords:
- vs.graphics.designer.effectdesigner
- vs.graphics.shaderdesigner
ms.assetid: 5db09a16-b82c-4ba3-8ec9-630cdc109397
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: dc48d2981e09dca55031b8ce78a06306a66ffbc0
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/02/2019
ms.locfileid: "53968544"
---
# <a name="shader-designer"></a>Конструктор шейдеров

Из этого документа вы узнаете, как с помощью **конструктора шейдеров** Visual Studio создавать, изменять и экспортировать пользовательские визуальные эффекты, также называемые *шейдерами*.

**Конструктор шейдеров** позволяет создавать пользовательские визуальные эффекты для игры или приложения, даже если вы не знакомы с языком высокого уровня для программирования шейдеров (HLSL). Чтобы создать шейдер в **конструкторе шейдеров**, спроектируйте его в виде графа. То есть добавьте в область конструктора *узлы*, представляющие данные и операции, а затем задайте связи между ними, чтобы определить способ обработки данных в рамках операций. На каждом узле операции осуществляется предварительный просмотр эффекта до этого момента, позволяя визуализировать его результат. Поток данных проходит через узлы, последний из которых представляет вывод шейдера.

## <a name="supported-formats"></a>Поддерживаемые форматы

**Конструктор шейдеров** поддерживает следующие форматы:

|Название формата|Расширение файла|Поддерживаемые операции (просмотр, правка, экспорт)|
|-----------------| - | - |
|Язык шейдеров ориентированных графов (Directed Graph Shader Language)|*DGSL*|Просмотр, правка|
|Шейдер HLSL (исходный код)|*HLSL*|Экспорт|
|Шейдер HLSL (байт-код)|*CSO*|Экспорт|
|Заголовок C++ (массив байт-кода HLSL)|*H*|Экспорт|

## <a name="get-started"></a>Начало работы

В этом разделе приведены инструкции по добавлению шейдера DGSL в проект Visual Studio на C++ и основные сведения, необходимые для начала работы.

> [!NOTE]
> Автоматическая интеграция сборок графических элементов, таких как графы шейдеров (DGSL-файлы), поддерживается только в проектах на C++.

### <a name="to-add-a-dgsl-shader-to-your-project"></a>Добавление шейдера DGSL в проект

1. Убедитесь, что у вас установлен компонент Visual Studio, необходимый для работы с графикой. Компонент называется **Image and 3D model editors** (Редакторы изображений и трехмерных моделей).

   Чтобы установить его, откройте Visual Studio Installer, выбрав в строке меню **Средства** > **Получить средства и компоненты**, а затем выберите вкладку **Individual components** (Отдельные компоненты). В категории **Games and Graphics** (Игры и графика) выберите компонент **Image and 3D model editors** (Редакторы изображений и трехмерных моделей) и нажмите кнопку **Modify** (Изменить).

   ![Компонент "Редакторы изображений и трехмерных моделей"](media/image-3d-model-editors-component.png)

2. В **обозревателе решений** откройте контекстное меню проекта на C++, в который требуется добавить шейдер, и последовательно выберите **Добавить** > **Создать элемент**.

3. В диалоговом окне **Добавление нового элемента** в разделе **Установленные** выберите **Графика**, а затем выберите **Визуальный граф шейдера (DGSL)**.

   > [!NOTE]
   > Если в диалоговом окне **Добавление нового элемента** категория **Графика** отсутствует, а **редакторы изображений и трехмерных моделей** установлены, значит графические элементы не поддерживаются для этого типа проекта.

4. Укажите **Имя** файла шейдера и **Расположение**, где его необходимо создать.

5. Нажмите кнопку **Добавить** .

### <a name="the-default-shader"></a>Шейдер по умолчанию

Всякий раз, когда вы создаете шейдер DGSL, сначала он представляет собой минимальный шейдер, имеющий только узел **Цвет точки**, подсоединенный к узлу **Окончательный цвет**. Хотя этот шейдер полностью функционален, функции его весьма ограничены. Поэтому первым шагом в создании рабочего шейдера часто является удаление узла **Цвет точки** или отсоединение его от узла **Окончательный цвет**, что дает возможность освободить место для других узлов.

## <a name="work-with-the-shader-designer"></a>Работа с конструктором шейдеров

В следующих разделах рассматривается порядок использования конструктора шейдеров для работы с пользовательскими шейдерами.

### <a name="shader-designer-toolbars"></a>Панели инструментов конструктора шейдеров

Панели инструментов конструктора шейдеров содержат команды, помогающие работать с графами шейдеров DGSL.

Команды, влияющие на состояние конструктора шейдеров, находятся на панели инструментов **Режим конструктора шейдеров** в главном окне Visual Studio. Средства проектирования и команды расположены на панели инструментов **Конструктор шейдеров** в области конструктора шейдеров.

Ниже приведена панель инструментов **Режим конструктора шейдеров**:

![Модальная панель инструментов конструктора шейдера.](../designers/media/digit-dsd-modal-toolbar.png)

Эта таблица описывает элементы на панели инструментов **Режим конструктора шейдеров**, перечисленные в порядке отображения, слева направо:

|Элемент панели инструментов|Описание|
|------------------|-----------------|
|**Выбрать**|Активирует взаимодействие с узлами и краями на графе. В этом режиме можно выбирать, перемещать или удалять узлы, а также устанавливать края или прерывать их.|
|**Панорама**|Активирует перемещение графа шейдера по отношению к рамке окна. Чтобы выполнить панорамирование, выберите точку в области конструктора и переместите ее.<br /><br /> В режиме **Выбрать**, нажав и удерживая клавишу **CTRL**, можно временно активировать режим **Панорама**.|
|**Масштаб**|Позволяет отображать граф шейдера более или менее детально по отношению к рамке окна. В режиме **Масштаб** выберите точку в области конструктора, а затем переместите ее вправо или вниз, чтобы увеличить масштаб, либо влево или вверх, чтобы уменьшить масштаб.<br /><br /> В режиме **Выбрать** можно увеличить или уменьшить масштаб, прокручивая колесо мыши с нажатой клавишей **Ctrl**.|
|**Масштабировать по данным**|Отображает полный граф шейдера в рамке окна.|
|**Режим отрисовки в реальном времени**|Если отрисовка в реальном времени включена, Visual Studio перерисовывает поверхность разработки, даже если пользователь не выполняет никаких действий. Этот режим полезен при работе с шейдерами, которые изменяются со временем.|
|**Просмотр на сфере**|При включении функции для предварительного просмотра шейдера используется модель сферы. Одновременно может быть активна только одна фигура предварительного просмотра.|
|**Просмотр на кубе**|При включении функции для предварительного просмотра шейдера используется модель куба. Одновременно может быть активна только одна фигура предварительного просмотра.|
|**Просмотр на цилиндре**|При включении функции для предварительного просмотра шейдера используется модель цилиндра. Одновременно может быть активна только одна фигура предварительного просмотра.|
|**Просмотр на конусе**|При включении функции для предварительного просмотра шейдера используется модель конуса. Одновременно может быть активна только одна фигура предварительного просмотра.|
|**Просмотр на чайнике**|При включении функции для предварительного просмотра шейдера используется модель чайника. Одновременно может быть активна только одна фигура предварительного просмотра.|
|**Просмотр на плоскости**|При включении функции для предварительного просмотра шейдера используется модель плоскости. Одновременно может быть активна только одна фигура предварительного просмотра.|
|**Панель элементов**|Отображает или скрывает **Панель элементов**.|
|**Свойства**|Отображает или скрывает окно **Свойства**.|
|**Дополнительно**|Содержит расширенные команды и параметры.<br /><br /> **Экспорт**: позволяет экспортировать шейдер в нескольких форматах.<br /><br /> **Экспортировать как**: экспортирует шейдер в виде исходного кода HLSL или скомпилированного байт-кода шейдера. Дополнительные сведения об экспорте шейдеров см. в разделе [Практическое руководство. Экспорт шейдера](../designers/how-to-export-a-shader.md).<br /><br /> **Графические модули**: позволяет выбрать отрисовщик, используемый для отображения области конструктора.<br /><br /> **Отобразить с D3D11**: использует Direct3D 11, чтобы отрисовать область конструктора шейдеров.<br /><br /> **Отобразить с D3D11WARP**: использует платформу Windows Advanced Rasterization Platform (WARP) Direct3D 11, чтобы отрисовать область конструктора шейдеров.<br /><br /> **Вид**: позволяет выбрать дополнительные сведения о конструкторе шейдеров.<br /><br /> **Частота кадров**: при включении эта функция указывает текущую частоту кадров в правом верхнем углу области конструктора. Частота кадров — это количество кадров, рисуемых в секунду. Этот параметр полезен при включении параметра **Режим отрисовки в реальном времени**.|

> [!TIP]
> Чтобы повторно запустить последнюю команду, нажмите кнопку **Дополнительно**.

### <a name="work-with-nodes-and-connections"></a>Работа с узлами и соединениями

Используйте режим **Выбрать**, чтобы добавлять, удалять, перемещать, соединять и настраивать узлы. Ниже описано, как выполнять основные операции:

#### <a name="to-perform-basic-operations-in-select-mode"></a>Выполнение основных операций в режиме "Выбрать"

- Это делается так.

   - Чтобы добавить на граф, выберите его на **панели элементов** и переместите в область конструктора.

   - Чтобы удалить узел из графа, выберите его и нажмите клавишу **DELETE**.

   - Чтобы изменить положение узла, выберите его и переместите на новое место.

   - Для соединения двух узлов переместите выходной терминал одного из узлов на входной терминал другого узла. Соединять можно только терминалы совместимых типов. Линия между терминалами обозначает соединение.

   - Чтобы удалить соединение, в контекстном меню для одного из соединенных терминалов выберите пункт **Разорвать связи**.

   - Для настройки свойств узла выберите его, а затем в окне **Свойства** укажите новые значения.

### <a name="preview-shaders"></a>Предварительный просмотр шейдеров

Чтобы понять, как шейдер будет выглядеть в приложении, вы можете настроить предварительный просмотр эффектов. Чтобы оценить приложение, вы можете выбрать одну из нескольких фигур для отрисовки, настроить текстуры и другие параметры материала, включить анимацию эффектов, учитывающих время, и осуществить предварительный просмотр с разных углов.

#### <a name="shapes"></a>Фигуры

Конструктор шейдеров включает в себя шесть фигур — сферу, куб, цилиндр, конус, чайник и плоскость, которые можно использовать для предварительного просмотра шейдера. В зависимости от конкретного шейдера некоторые фигуры могут лучше других подходить для предварительного просмотра.

Чтобы выбрать фигуру для предварительного просмотра, выберите нужную фигуру на панели инструментов **Режим конструктора шейдеров**.

#### <a name="textures-and-material-parameters"></a>Текстуры и параметры материалов

Многие шейдеры используют текстуры и свойства материалов, чтобы создать уникальный внешний вид для каждого типа объектов в приложении. Чтобы увидеть, как шейдер будет выглядеть в приложении, можно задать те текстуры и свойства материалов, применяемые при отображении предварительного просмотра, которые могут использоваться в вашем приложении.

Чтобы привязать другую текстуру к регистру текстуры или изменить другие параметры материалов, выполните следующие действия:

1. В режиме **Выбрать** выберите пустое пространство в области конструктора. При этом в окне **Свойства** отображаются глобальные свойства шейдера.

2. В окне **Свойства** укажите новые значения для свойств параметров и текстур, которые требуется изменить.

Параметры шейдера, которые можно изменить, указаны в приведенной ниже таблице.

|Параметр|Свойства|
|---------------|----------------|
|**Текстура 1** - **Текстура 8**|**Доступ**.                             Значение **Открытый**, чтобы разрешить задание этого свойства в редакторе моделей; в противном случае — значение **Закрытый**.<br /><br /> **Имя файла**. Полный путь к файлу текстуры, связанному с этим регистром текстуры.|
|**Материал — окружающий**|**Доступ**.                             Значение **Открытый**, чтобы разрешить задание этого свойства в редакторе моделей; в противном случае — значение **Закрытый**.<br /><br /> **Значение**. Диффузный цвет текущего пикселя, вызванный непрямым или окружающим освещением.|
|**Материал — диффузный**|**Доступ**. Значение **Открытый**, чтобы разрешить задание этого свойства в редакторе моделей; в противном случае — значение **Закрытый**.<br /><br /> **Значение**.  Цвет, который описывает, как текущий пиксель рассеивает прямое освещение.|
|**Материал — эмиссионный**|**Доступ**.                              Значение **Открытый**, чтобы разрешить задание этого свойства в редакторе моделей; в противном случае — значение **Закрытый**.<br /><br /> **Значение**. Добавочный цвет текущего пикселя, который образуется вследствие освещения, предоставляемого пользователем.|
|**Материал — отражающий**|**Доступ**.                              Значение **Открытый**, чтобы разрешить задание этого свойства в редакторе моделей; в противном случае — значение **Закрытый**.<br /><br /> **Значение**. Цвет, который описывает, как текущий пиксель отражает прямое освещение.|
|**Отражающая способность материала**|**Доступ**.                             Значение **Открытый**, чтобы разрешить задание этого свойства в редакторе моделей; в противном случае — значение **Закрытый**.<br /><br /> **Значение**. Экспонента, которая определяет интенсивность зеркального отражения от текущего пикселя.|

#### <a name="time-based-effects"></a>Эффекты с учетом времени

В некоторых шейдерах присутствует компонент учета времени, который анимирует эффект. Чтобы показать, как выглядит эффект в действии, предварительный просмотр должен обновляться несколько раз в секунду. По умолчанию предварительный просмотр обновляется только при изменении шейдера. Чтобы изменить такое поведение для просмотра эффектов с учетом времени, нужно включить отрисовку в реальном времени.

Чтобы включить отрисовку в режиме реального времени, на панели инструментов "Конструктор шейдеров" выберите **Отрисовка в реальном времени**.

#### <a name="examine-the-effect"></a>Наблюдение за эффектом

Многие шейдеры зависят от переменных, таких как угол просмотра и направленное освещение. Чтобы наблюдать, как эффект реагирует на изменение этих переменных, можно свободно вращать фигуру для предварительного просмотра и отслеживать поведение шейдера.

Чтобы повернуть фигуру, удерживая нажатой клавишу **ALT**, выберите точку в области конструктора и переместите ее.

### <a name="export-shaders"></a>Экспорт шейдеров

Прежде чем использовать шейдер в приложении, нужно экспортировать его в формате, совместимом с DirectX.

Шейдеры можно экспортировать в виде исходного кода HLSL или скомпилированного байт-кода шейдера. Исходный код HLSL экспортируется в текстовый файл с расширением *HLSL*. Байт-код шейдера можно экспортировать в необработанный двоичный файл, который имеет расширение *CSO*, или в файл заголовков C++ (с расширением *H*), который кодирует байт-код шейдера в массив.

Дополнительные сведения об экспорте шейдеров см. в разделе [Практическое руководство. Экспорт шейдера](../designers/how-to-export-a-shader.md).

## <a name="keyboard-shortcuts"></a>Сочетания клавиш

|Команда|Сочетания клавиш|
|-------------| - |
|Переход в режим **Выбрать**|**Ctrl**+**G**, **Ctrl**+**Q**<br /><br /> **S**|
|Переход в режим **Масштаб**|**Ctrl**+**G**, **Ctrl**+**Z**<br /><br /> **Z**|
|Переход в режим **Панорама**|**Ctrl**+**G**, **Ctrl**+**P**<br /><br /> **K**|
|Выбрать все|**CTRL**+**A**|
|Удалить текущее выделение|**Удалить**|
|Отменить текущее выделение|**Escape** (**Esc**)|
|Увеличить|**CTRL**+**Прокручивание колеса мыши вперед**<br /><br /> Знак плюса (**+**)|
|Мельче|**CTRL**+**Прокручивание колеса мыши назад**<br /><br /> Знак минуса (**-**)|
|Панорамирование области конструктора вверх|**Прокручивание колеса мыши назад**<br /><br /> **PageDown**|
|Панорамирование области конструктора вниз|**Прокручивание колеса мыши вперед**<br /><br /> **PageUp**|
|Панорамирование области конструктора влево|**SHIFT**+**Прокручивание колеса мыши назад**<br /><br /> **Прокручивание колеса мыши влево**<br /><br /> **SHIFT**+**PageDown**|
|Панорамирование области конструктора вправо|**SHIFT**+**Прокручивание колеса мыши вперед**<br /><br /> **Прокручивание колеса мыши вправо**<br /><br /> **SHIFT**+**PageUp**|
|Перемещение фокуса клавиатуры на другой узел|Клавиши со **стрелками**|
|Выбор узла, на который установлен фокус клавиатуры (узел добавляется к группе выбора)|**Shift**+**Пробел**|
|Переключение выделения узла, на который установлен фокус клавиатуры|**Ctrl**+**Пробел**|
|Переключение текущего выделения (если узлы не выбраны, выбирается узел, на который установлен фокус клавиатуры)|**ПРОБЕЛ**|
|Перемещение текущего выделения вверх|**Shift**+**Стрелка вверх**|
|Перемещение текущего выделения вниз|**Shift**+**Стрелка вниз**|
|Перемещение текущего выделения влево|**Shift**+**Стрелка влево**|
|Перемещение текущего выделения вправо|**Shift**+**Стрелка вправо**|

## <a name="related-topics"></a>См. также

|Заголовок|Описание|
|-----------|-----------------|
|[Работа с трехмерными ресурсами для игр и приложений](../designers/working-with-3-d-assets-for-games-and-apps.md)|Обзор средств Visual Studio для работы с текстурами и изображениями, трехмерными моделями и эффектами шейдеров.|
|[Image Editor](../designers/image-editor.md)|Описывается использование редактора изображений Visual Studio для работы с текстурами и изображениями.|
|[Редактор моделей](../designers/model-editor.md)|Описывается работа с трехмерными моделями с помощью редактора моделей Visual Studio.|