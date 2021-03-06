---
title: Автономная справочная документация
ms.date: 11/02/2017
ms.prod: visual-studio-dev15
ms.topic: conceptual
f1_keywords:
- hv_general
helpviewer_keywords:
- Microsoft Help Viewer Help
- Help Viewer, printing a topic
- printing a topic [Help Viewer]
- Help Viewer, toolbar
- Help on Help [Help Viewer]
- Help Viewer, window components
- Help Viewer, navigating
- toolbar [Help Viewer]
ms.assetid: 74e41666-2ce8-4ac0-a0e5-3723d1e322c2
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: bc9fd8b8684782f92c27563fb5d19a46d61c554e
ms.sourcegitcommit: 75e02ed88a1ace6e8265fd4e3a82a1bc78f3adca
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/13/2018
ms.locfileid: "54406122"
---
# <a name="microsoft-help-viewer"></a>Окно справки (Майкрософт)

Вы можете установить различные продукты и технологии и просмотреть содержимое их справки на локальном компьютере, используя окно справки (Майкрософт). Эти продукты включают Visual Studio, .NET Framework, справочник по языку, SQL Server и сведения по разработке Windows. Окно справки позволяет вам:

- Скачайте наборы содержимого, которые также называют книгами. Это может быть удобно, если вам нужно работать автономно и по-прежнему иметь доступ к документации.

- Найти разделы по названию с помощью поиска в оглавлении.

- Найти темы в индексе.

- Найти информацию с помощью полнотекстового поиска.

- Просмотреть и распечатать разделы, а также установить закладки.

Чтобы установить окно справки, см. раздел [Установка окна справки (Майкрософт)](../help-viewer/installation.md). Чтобы просматривать разделы справки в окне справки, а не в Интернете, перейдите в меню **Справка** в Visual Studio, а затем выберите **Задать параметры справки** > **Запустить в средстве просмотра справки**.

> [!TIP]
> Кроме того, чтобы получить локальную копию материалов, которую можно просмотреть при отсутствии подключения к Интернету, можно скачать PDF-версию этих материалов. Многие наборы документации на сайте docs.microsoft.com содержат ссылку в нижней части содержания, позволяющую скачать PDF-файл со всеми статьями для этого содержания.
>
> ![Скачать PDF с документацией Visual Studio](media/overview/download-pdf.png)

## <a name="help-viewer-tour"></a>Обзор окна справки

Вы можете найти информацию в установленном содержимом, используя вкладки навигации, просматривая содержимое во вкладках разделов и управляя им на вкладке **Управление содержимым**. Вы также можете выполнять другие задачи с помощью кнопок на панели инструментов и искать дополнительные сведения в правом нижнем углу окна.

### <a name="navigation-tabs"></a>Вкладки навигации

|Tab|Описание|
|---|-----------|
|Описание|Отображает установленное содержимое в виде иерархии (оглавление). Вы можете указать условия для фильтрации отображаемых заголовков.|
|Индекс|Отображает список индексированных терминов в алфавитном порядке. Вы можете выполнить поиск по индексу, указать критерии для фильтрации записей и потребовать, чтобы записи индекса содержали указанный текст или начинались с него.|
|Избранное|Вы можете добавить разделы в избранное, нажав кнопку **Добавить в избранное** и выбрав отображаемые на этой вкладке разделы. В разделе **Журнал** отображается список недавно просмотренных разделов.|
|Поиск|Предоставляет поле поиска, где можно искать термины по всему содержимому, включая код и названия разделов.|

### <a name="view-topics"></a>Просмотр разделов

Каждый раздел отображается на отдельной вкладке, и вы можете открыть несколько разделов одновременно.

### <a name="manage-content"></a>Управление содержимым

Вы можете установить, обновить, переместить и удалить содержимое на вкладке **Управление содержимым**. В верхней части вкладки можно использовать элемент управления **Источник установки**, чтобы указать, следует ли устанавливать книги из сетевого расположения, с диска или из Интернета по универсальному коду ресурса (URI). В поле **Путь к локальному хранилищу** показано, где устанавливаются книги на локальном компьютере, и вы можете переместить их в другое расположение, нажав кнопку **Переместить**.

В списке содержимого отображаются установленные книги и книги, которые можно установить, а также наличие обновлений и размер каждой книги. Вы можете установить или удалить одну книгу или несколько, щелкнув ссылку **Добавить** или **Удалить**, а затем нажать кнопку **Обновить** на панели **Ожидают изменений**. При наличии обновлений для установленных книг можно обновить содержимое, выбрав ссылку **Щелкните, чтобы начать загрузку** в нижней части окна. Кроме того, если обновления появляются при установке книг, все установленные книги обновляются.

> [!NOTE]
> Функциональные возможности вкладки **Управление содержимым** могут измениться, если администратор окна справки отключит эти возможности, а также при отсутствии подключения к Интернету.

### <a name="toolbar-buttons"></a>Кнопки на панели инструментов

На панели инструментов в **окне справки** находятся следующие кнопки:

- Кнопка **Показать раздел в содержании** показывает расположение раздела на вкладке **Содержание**.

- Кнопка **Добавить в избранное** добавляет активный раздел на вкладку **Избранное**.

- Кнопка **Найти в разделе** выделяет искомый текст в активном разделе.

- Кнопка **Печать** распечатывает или открывает предварительный просмотр активного раздела.

- Кнопка **Параметры окна справки** отображает параметры, например размер текста, количество возвращаемых результатов поиска, количество разделов в журнале и необходимость проверки наличия обновлений в Интернете.

- Кнопка **Управление содержимым** открывает вкладку **Управление содержимым**.

- Расположенный справа маленький треугольник открывает список вкладок, включая вкладки разделов и вкладку **Управление содержимым**. Вы можете выбрать имя вкладки, чтобы сделать ее активной.

## <a name="see-also"></a>См. также

- [Установка окна справки (Майкрософт)](../help-viewer/installation.md)
- [Руководство по окну справки для администраторов](../help-viewer/administrator-guide.md)
- [Установка локального содержимого и управление им](../help-viewer/install-manage-local-content.md)
