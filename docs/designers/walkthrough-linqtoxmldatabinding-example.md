---
title: Пошаговое руководство. Пример LinqToXmlDataBinding
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
ms.assetid: aedf42e8-896c-48fa-88df-7f7c9536aa69
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: a6642981934c764fc2f6d512cb19502a21ac224e
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/02/2019
ms.locfileid: "53850704"
---
# <a name="walkthrough-linqtoxmldatabinding-example"></a>Пошаговое руководство. пример LinqToXmlDataBinding
В этом пошаговом руководстве описывается пример LinqToXmlDataBinding, а также разъясняются наиболее интересные элементы содержимого его главных исходных файлов *L2DBForm.xaml* и *L2DBForm.xaml.cs*.

## <a name="prerequisites"></a>Предварительные требования
 Перед тем как вы приступите к знакомству с этим пошаговым руководством, настоятельно рекомендуем собрать и запустить программу LinqToXmlDataBinding, как это описано в статье [Практическое руководство. Сборка и выполнение примера LinqToXmlDataBinding](../designers/how-to-build-and-run-the-linqtoxmldatabinding-example.md).

## <a name="remarks"></a>Примечания
 Программа LinqToXmlDataBinding - это приложение WPF, состоящее из файлов на языках C# и XAML. Она содержит внедренный XML-документ, который определяет список книг и дает пользователю возможность просматривать, добавлять, удалять и изменять эти записи. Она состоит из двух следующих исходных файлов.

- Файл *L2DBForm.xaml* содержит декларацию кода XAML для пользовательского интерфейса главного окна. Он содержит также раздел ресурсов окна, который определяет поставщика данных, и внедренный XML-документ для листингов книг.

- Файл *L2DBForm.xaml.cs* содержит методы инициализации и обработки событий, связанные с этим пользовательским интерфейсом.

  Главное окно разделено по вертикали на четыре интерфейсных раздела.

- Раздел **XML** отображает необработанный код внедренного листинга книг на языке XML.

- Раздел **Список книг** отображает выполненные в формате стандартного текста записи книг и дает пользователю возможность выбирать и удалять отдельные записи.

- Раздел **Правка выделенной книги** позволяет пользователю изменять значения, связанные с книжной записью, выделенной в данный момент.

- Раздел **Добавить новую книгу** позволяет создавать новую запись в книге на базе значений, введенных пользователем.

## <a name="in-this-section"></a>Содержание раздела

|Раздел|Описание|
|-----------|-----------------|
|[Исходный код L2DBForm.xaml](../designers/l2dbform-xaml-source-code.md)|Включает в себя содержимое и описание кода XAML в файле L2DBForm.xaml.|
|[Исходный код L2DBForm.xaml.cs](../designers/l2dbform-xaml-cs-source-code.md)|Включает в себя содержимое и описание исходного кода C# в файле L2DBForm.xaml.cs.|

## <a name="see-also"></a>См. также

- [Привязка данных WPF с использованием примера LINQ to XML](../designers/wpf-data-binding-using-linq-to-xml-example.md)
- [Практическое руководство. Сборка и выполнение примера LinqToXmlDataBinding](../designers/how-to-build-and-run-the-linqtoxmldatabinding-example.md)