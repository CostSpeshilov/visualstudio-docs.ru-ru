---
title: Как выполнить построить и запустить пример LinqToXmlDataBinding
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 4087ea9d97970621a2ec8b51dc37d38f0306b0e6
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/02/2019
ms.locfileid: "53989021"
---
# <a name="how-to-build-and-run-the-linqtoxmldatabinding-example"></a>Как выполнить Сборка и запуск примера LinqToXmlDataBinding

В этом разделе показано создание и построение проекта среды Visual Studio LinqToXmlDataBinding, а также запуск полученного в результате образца программы WPF LinqToXmlDataBinding.

Дополнительные сведения о настройке интегрированной среды разработки см. в [обзоре Visual Studio IDE](../get-started/visual-studio-ide.md).

## <a name="create-and-populate-the-project"></a>Создание и заполнение проекта

### <a name="to-create-the-starting-project"></a>Создание начального проекта

1. Запустите среду Visual Studio и создайте приложение C# WPF с именем LinqToXmlDataBinding. В проекте должна использоваться инфраструктура .NET Framework 3.5 (или более поздняя версия).

1. Добавьте в проект ссылки для следующих сборок .NET, если они еще не заданы:

    - System.Data

    - System.Data.DataSetExtensions

    - System.Xml

    - System.Xml.Linq

1. Выполните сборку решения, нажав **Ctrl**+**Shift**+**B**, а затем запустите его с помощью клавиши **F5**. Проект должен быть скомпилирован без ошибок и выполнен как обычное приложение WPF.

### <a name="to-add-custom-code-to-the-project"></a>Добавление в проект пользовательского кода

1. В обозревателе решений переименуйте исходный файл **Window1.xaml** в **L2XDBForm.xaml**. Зависимый исходный файл **Window1.xaml.cs** должен быть автоматически переименован в **L2XDBForm.xaml.cs**.

1. Замените исходный код в файле **L2XDBForm.xaml** фрагментом кода из статьи [Исходный код L2DBForm.xaml](../designers/l2dbform-xaml-source-code.md). Для работы с этим файлом используйте представление источника данных XAML.

1. Аналогичным образом замените исходный код в файле **L2XDBForm.xaml.cs** кодом из статьи [Исходный код L2DBForm.xaml.cs](../designers/l2dbform-xaml-cs-source-code.md).

1. В файле **App.xaml** замените все экземпляры строки `Window1.xaml` на `L2XDBForm.xaml`.

1. Выполните сборку решения, нажав **Ctrl**+**Shift**+**B**.

## <a name="run-the-program"></a>Запуск программы

Программа LinqToXmlDataBinding дает пользователю возможность просматривать и управлять списком книг, который хранится в виде внедренного XML-элемента.

### <a name="to-run-the-program-and-view-the-book-list"></a>Выполнение программы и просмотр списка книг

- Запустите программу LinqToXmlDataBinding, нажав клавишу **F5** (**Начать отладку**) или клавиши **Ctrl**+**F5** (**Запуск без отладки**).

   Откроется окно программы с заголовком **Привязка данных WPF с помощью LINQ to XML**.

- Обратите внимание на верхнюю часть пользовательского интерфейса, в котором отображается необработанный код **XML**, представляющий список книг. Он выводится с помощью элемента управления WPF <xref:System.Windows.Controls.TextBlock>, не включающего взаимодействие с мышью или клавиатурой.

- Второй вертикальный раздел, обозначенный как **Список книг**, отображает упорядоченный список книг в виде простого текста. В нем используется элемент управления <xref:System.Windows.Controls.ListBox>, допускающий выбор с помощью мыши или клавиатуры.

### <a name="to-add-and-delete-books-from-the-list"></a>Добавление и удаление книг из списка

- Чтобы добавить новую книгу в список, введите значения в элементы управления **Идентификатор** и **Значение**<xref:System.Windows.Controls.TextBox> в последнем разделе **Добавление книги**, а затем нажмите кнопку **Добавить книгу**. Обратите внимание, что новая книга добавляется в конец списка и исходного текста XML. Эта программа не выполняет проверку правильности входных значений.

- Чтобы удалить существующую книгу из списка, выделите ее в разделе **Список книг** и нажмите кнопку **Remove Selected Book** (Удалить выбранную книгу). Обратите внимание, что запись книги удаляется не только из списка, но и из необработанного исходного текста XML.

### <a name="to-edit-an-existing-book-entry"></a>Редактирование существующей записи книги

1. Выделите книгу во втором разделе **Список книг**. Текущие значения для выделенной книги отобразятся в третьем разделе — **Edit Selected Book** (Редактирование выделенной книги).

1. Измените значения с клавиатуры. Как только элемент управления <xref:System.Windows.Controls.TextBox> теряет фокус, изменения автоматически распространяются на список книг и исходный текст XML.

## <a name="see-also"></a>См. также

- [Привязка данных WPF с использованием примера LINQ to XML](../designers/wpf-data-binding-using-linq-to-xml-example.md)
- [Пошаговое руководство: пример LinqToXmlDataBinding](../designers/walkthrough-linqtoxmldatabinding-example.md)
- [Обзор интегрированной среды разработки Visual Studio](../get-started/visual-studio-ide.md)