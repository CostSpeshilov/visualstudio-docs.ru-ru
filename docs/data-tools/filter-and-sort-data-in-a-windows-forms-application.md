---
title: Фильтрация и сортировка данных в приложении Windows Forms
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- row states, filtering
- data views, sorting
- row version, filtering
- row states
- data views, filtering
- sorting datasets, using data views
- dataset filtering, using data views
ms.assetid: f4f100f1-776d-46dc-b2fd-5b35b98d9561
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.workload:
- data-storage
ms.openlocfilehash: 6da584d4966d61a873ca43477930084c4f9a464b
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MTE95
ms.contentlocale: ru-RU
ms.lasthandoff: 01/02/2019
ms.locfileid: "53890015"
---
# <a name="filter-and-sort-data-in-a-windows-forms-application"></a>Фильтрация и сортировка данных в приложении Windows Forms

Фильтрация данных, задав <xref:System.Windows.Forms.BindingSource.Filter%2A> свойства строковое выражение, возвращающее нужные записи.

Сортировать данные, задав <xref:System.Windows.Forms.BindingSource.Sort%2A> свойства имя столбца, на котором должна быть выполнена сортировка; добавьте `DESC` отсортировать в нисходящем порядке или добавить `ASC` для сортировки по возрастанию.

> [!NOTE]
> Если приложение не использует <xref:System.Windows.Forms.BindingSource> компонентов, можно фильтровать и сортировать данные с помощью <xref:System.Data.DataView> объектов. Дополнительные сведения см. в разделе [объекты DataView](/dotnet/framework/data/adonet/dataset-datatable-dataview/dataviews).

## <a name="to-filter-data-by-using-a-bindingsource-component"></a>Для фильтрации данных с помощью компонента BindingSource

-   Задайте <xref:System.Windows.Forms.BindingSource.Filter%2A> значение выражения, который необходимо вернуть. Например, следующий код возвращает клиентов с `CompanyName` , начинающегося с «B»:

     [!code-csharp[VbRaddataDisplaying#6](../data-tools/codesnippet/CSharp/filter-and-sort-data-in-a-windows-forms-application_1.cs)]
     [!code-vb[VbRaddataDisplaying#6](../data-tools/codesnippet/VisualBasic/filter-and-sort-data-in-a-windows-forms-application_1.vb)]

## <a name="to-sort-data-by-using-a-bindingsource-component"></a>Для сортировки данных с помощью компонента BindingSource

-   Задать <xref:System.Windows.Forms.BindingSource.Sort%2A> свойства столбца, нужно выполнить сортировку. Например, следующий код сортирует клиентов по `CompanyName` столбец в порядке убывания:

     [!code-csharp[VbRaddataDisplaying#7](../data-tools/codesnippet/CSharp/filter-and-sort-data-in-a-windows-forms-application_2.cs)]
     [!code-vb[VbRaddataDisplaying#7](../data-tools/codesnippet/VisualBasic/filter-and-sort-data-in-a-windows-forms-application_2.vb)]

## <a name="see-also"></a>См. также

- [Привязка элементов управления к данным в Visual Studio](../data-tools/bind-controls-to-data-in-visual-studio.md)