---
title: "Проекты в инструментах R для Visual Studio | Документация Майкрософт"
description: "Практическое руководство по созданию проектов диспетчера R в Visual Studio, в том числе свойства, команды и шаблоны."
ms.custom: 
ms.date: 06/29/2017
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-r
ms.devlang: r
ms.tgt_pltfrm: 
ms.topic: article
caps.latest.revision: 
author: kraigb
ms.author: kraigb
manager: ghogen
ms.workload:
- data-science
ms.openlocfilehash: f201eb31f907e8cacf6453651927e5639462e1c3
ms.sourcegitcommit: ba29e4d37db92ec784d4acf9c6e120cf0ea677e9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2018
---
# <a name="creating-r-projects-in-visual-studio"></a>Создание проектов R в Visual Studio

Проект R (файл `.rxproj`) определяет все исходные файлы и файлы содержимого, связанные с проектом. Он также содержит сведения о сборке каждого файла, хранит информацию для интеграции с системами управления версиями и помогает упорядочить приложение в виде логических компонентов. Однако сведения, относящиеся к рабочей области, такие как список установленных пакетов, хранятся отдельно в самой рабочей области.

Для управления проектами всегда используется *решение* Visual Studio, которое может содержать любое число проектов с возможностью ссылаться друг на друга. См. раздел [Использование проектов различных типов в Visual Studio](#use-multiple-project-types-in-visual-studio).

## <a name="creating-a-new-r-project"></a>Создание проекта R

1. Запустите Visual Studio.
1. Выберите **Файл > Создать > Проект...** (CTRL+SHIFT+N)
1. В разделе **Шаблоны > R** выберите "Проект R" и присвойте имя проекту, укажите его расположение, а затем нажмите **ОК**.

    ![Диалоговое окно создания проекта R в Visual Studio (RTVS в VS2017)](media/getting-started-01-new-project.png)

Эта команда создает проект с пустым файлом `script.R`, который будет открыт в редакторе. Обратите внимание также на то, что в **обозревателе решений** находятся два других файла проекта.

![Содержимое проекта R, созданного на основе шаблона](media/projects-template-results.png)

В файле `.Rhistory` фиксируются все команды, введенные в [интерактивном окне R](interactive-repl-for-r-in-visual-studio.md). Можно открыть выделенное окно журнала с помощью команды **Инструменты R > Окна > Журнал**. Это окно содержит кнопку на панели инструментов и элементы в контекстном меню, служащие для очистки содержимого журнала.

В файле `rproject.rproj` хранятся параметры проекта R, которые не управляются Visual Studio иным способом.

| Свойство. | По умолчанию | Описание: |
| --- | --- | --- |
| Версия | 1.0 | Версия инструментов R для Visual Studio, которая использовалась для создания проекта. |
| RestoreWorkspace | По умолчанию | Автоматическая загрузка переменных предыдущей рабочей области из файла `.RData` в каталоге проекта. |
| SaveWorkspace | По умолчанию | Сохранение переменных текущей рабочей области в файле `.RData` в каталоге проекта при закрытии проекта. |
| AlwaysSaveHistory | По умолчанию | Сохранение журнала интерактивного окна в файле `.RHistory` в каталоге проекта при закрытии проекта. |
| EnableCodeIndexing | Да | Определяет необходимость запуска фоновой задачи индексирования для ускорения поиска кода. |
| UseSpacesForTab | Да | Определяет, следует ли вставлять пробелы (Да) или символ табуляции (Нет) при нажатии клавиши TAB в редакторе. |
| NumSpacesForTab | 2 | Число пробелов для вставки, если для параметра UseSpacesForTab выбрано значение "Да". |
| кодировка | UTF-8 | Кодировка по умолчанию для файлов `.R`. |
| RnwWeave | Sweave | Пакет для использования при встраивании файла Rnw. |
| LaTeX | pdfLaTeX | Библиотека для использования при преобразовании RMarkdwon в PDF. |

### <a name="converting-a-folder-of-files-to-an-r-project"></a>Преобразование папки с файлами в проект R

Если имеется папка с файлами `.R`, которую требуется преобразовать в проект, выполните следующие действия.

1. Создайте новый проект в Visual Studio, как описано в предыдущем разделе.
1. Скопируйте файлы в папку проекта.
1. В обозревателе решений Visual Studio щелкните правой кнопкой мыши проект, выберите **Добавить > Существующий элемент** и перейдите к файлам, которые нужно добавить. Эти файлы отображаются в дереве проекта после нажатия кнопки **ОК**.
1. Чтобы упорядочить код по вложенным папкам, сначала щелкните правой кнопкой мыши проект, выберите **Добавить > Новая папка**, а затем скопируйте файлы в эту папку и добавьте существующие элементы из шага 3.

## <a name="project-properties"></a>Свойства проекта

Чтобы открыть страницу свойств проекта, щелкните правой кнопкой мыши проект в **обозревателе решений** и выберите **Свойства** или выберите пункт меню * *Проект > Свойства (название проекта)...* В появившемся окне отображаются свойства проекта:

| Вкладка | Свойство. | Описание: |
| --- | --- | --- |
| Выполнить | Файл запуска | Имя файла, который выполняется с помощью команды **Исходный файл запуска**, клавиши F5, команды **Отладка > Начать отладку** или команды **Отладка > Запуск без отладки**. Щелкнув правой кнопкой мыши файл в проекте и выбрав **Назначить запускаемым скриптом R**, можно также выбрать его в качестве файла запуска. |
| | Сбросить интерактивное окно R при запуске | Сброс всех переменных в рабочей области интерактивного окна при запуске проекта. Это гарантирует отсутствие в рабочей области остаточного содержимого предыдущих запусков. |
| | Путь к удаленному проекту | Путь к удаленной рабочей области. |
| | Передать файлы при запуске | Указание того, следует ли при каждом запуске копировать файлы проекта, к которым применен фильтр в разделе **Файлы для передачи**, в удаленную рабочую область. |
| | Файлы для передачи | Имена файлов и подстановочные знаки, указывающие определенные файлы для копирования в удаленную рабочую область, если выбран параметр **Передать файлы при запуске**. |
| Параметры | (Файл Settings.R) | Параметры проекта R берутся из файлов `Settings.R` или `*.Settings.R`, которые находятся внутри проекта. Если файл параметров отсутствует, можно добавить переменные, сохранить страницу, после чего автоматически создается файл `Settings.R` по умолчанию. Файл параметров также можно добавить в проект с помощью команды * *Файл > Добавить новый элемент*. <br/> Параметры хранятся в виде кода R, и файл можно выполнить перед выполнением других модулей, предварительно заполнив при этом окружение с помощью предварительно определенных параметров. |

## <a name="r-specific-project-commands"></a>Команды для проекта R

Проекты Visual Studio поддерживают ряд общих команд, которые представлены в контекстном меню и в меню **Проект**. Дополнительные сведения об этих общих возможностях см. в разделе [Решения и проекты в Visual Studio](../ide/solutions-and-projects-in-visual-studio.md). Однако следует помнить, что 

Инструменты R для Visual Studio (RTVS) добавляют ряд собственных команд в контекстное меню для проекта R, а также собственные файлы и папки в проект.

| Команда | Описание: |
| --- | --- |
| Задать текущий каталог в качестве рабочего | Задание рабочего каталога интерактивного окна R в качестве папки проекта, эту команду можно применить для любой вложенной папки внутри проекта. |
| Открыть содержащую папку | Открытие проводника в папке выбранного файла. | 
| Добавить скрипт R | Создание и открытие нового файла `.R` с именем по умолчанию. Можно также воспользоваться командой **Добавить > Новый элемент**, чтобы создать файлы `.R`, а также ряд файлов других типов. См. раздел [Шаблоны элементов R](#r-specific-item-templates). |
| Добавить разметку R Markdown | Создание и открытие нового документа `.rmd` с именем по умолчанию. Можно также воспользоваться командой **Добавить > Новый элемент**, чтобы создать файлы `.rmd`, а также ряд файлов других типов. См. раздел [Шаблоны элементов R](#r-specific-item-templates).  | 
| Публикация хранимых процедур | Запуск процесса публикации всех хранимых процедур, содержащихся в скриптах R. См. раздел [Работа с хранимыми процедурами SQL Server](integrating-sql-server-with-r.md#working-with-sql-server-stored-procedures). | 

## <a name="r-specific-item-templates"></a>Шаблоны элементов R

В состав RTVS входит несколько шаблонов для определенных типов файлов. Для доступа к шаблонам щелкните правой кнопкой мыши проект R и выберите команду **Добавить > Новый элемент...** или **Проект > Добавить новый элемент...** либо выберите команду **Файл > Создать > Файл...**, а затем откройте вкладку **R**. Лучший способ просмотра шаблона заключается в создании проекта и вставке файлов каждого типа.

> [!Note]
> Команды **Добавить > Новый элемент...** также позволяют отобразить общие типы файлов, которые отсутствуют в таблице; в меню **Файл > Создать > Файл...** эти типы находятся на вкладке **Общие**.

| Тип файла | Описание: |
| --- | --- |
| Скрипт R | Текстовый файл, содержащий те же команды, которые можно ввести в командной строке R. |
| Разметка R | Файл, содержащий документ с [разметкой R](rmarkdown-with-r-in-visual-studio.md). |
| Параметры R | Файл, содержащий параметры приложения R. | 
| Документация по R | Универсальный файл документации по R, содержащий только поля имени псевдонима и заголовка. |
| Документация по R (функция) | Файл документации по R, содержащий множество полей с комментариями для описания функции. |
| Документация по R (набор данных) | Файл документации по R, содержащий множество полей с комментариями для описания набора данных. |
| SQL-запрос | Пустой файл `.sql`. См. раздел [Интеграция с SQL Server](integrating-sql-server-with-r.md). |
| Хранимые процедуры с R | Файл R с дочерним SQL-запросом и дочерним файлом шаблона хранимой процедуры. См. раздел [Интеграция с SQL Server](integrating-sql-server-with-r.md). |

## <a name="use-multiple-project-types-in-visual-studio"></a>Использование проектов различных типов в Visual Studio

Решения Visual Studio являются удобным местом для сбора проектов и управления связанными проектами в одном логичном месте. Решения помогают обеспечить упорядочение кода и облегчают взаимодействие команд.

В примере ниже решение содержит проект R с моделью, созданной с использованием R и машинного обучения Azure, проект обучения Python/scikit, проект C++, содержащий модули для выполнения ресурсоемких вычислительных операций, проект SQL для управления данными и проект Python/Bottle для веб-сайта, который публикует результат.

![Visual Studio в обозревателе решений с несколькими проектами, объединенными в одном решении](media/projects-polyglot.png)

Проект, выделенный полужирным шрифтом, является "запускаемым" проектом для решения; чтобы изменить его, щелкните правой кнопкой мыши другой проект и выберите **Назначить запускаемым проектом**.

> [!Note]
> В настоящее время не существует явной интеграции языков R и C#/C++ (такой, которая имеется для Python, см. раздел [Создание расширения C++ для Python](../python/working-with-c-cpp-python-in-visual-studio.md)).  Тем не менее есть библиотеки, содержащие мосты C# и C++ для R.

Дополнительные сведения об управлении проектами и решениями см. в разделе [Решения и проекты в Visual Studio](../ide/solutions-and-projects-in-visual-studio.md).