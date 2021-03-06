---
title: Как выполнить Заполнение документов данными из служб
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- documents [Office development in Visual Studio], populating with data
- Web services [Office development in Visual Studio], populating documents
- data [Office development in Visual Studio], adding to documents
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 137755ae4e1bfab97cbaec063a29a95caa1d9cd6
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/24/2019
ms.locfileid: "54865025"
---
# <a name="how-to-populate-documents-with-data-from-services"></a>Как выполнить Заполнение документов данными из служб

Доступ к данным в проектах уровня документа для Microsoft Office работает точно так же, как в проектах Windows Forms. Вы используете те же средства и код для получения данных в ваше решение и даже можете отображать данные с помощью элементов управления Windows Forms. Кроме того, можно воспользоваться преимуществами элементов управления ведущего приложения, которые являются собственными объектами в Microsoft Office Excel и Microsoft Office Word, дополненными событиями и функциями привязки данных. Дополнительные сведения см. в разделе [ведущие элементы и размещать элементы управления](../vsto/host-items-and-host-controls-overview.md).

[!INCLUDE[appliesto_alldoc](../vsto/includes/appliesto-alldoc-md.md)]

В следующем примере показано, как добавить элементы управления с привязкой к данным в документы во время разработки. Пример добавления элементов управления с привязкой данных в надстройках VSTO во время выполнения, см. в разделе [Пошаговое руководство: Привязка к данным из службы в проекте надстройки VSTO](../vsto/walkthrough-binding-to-data-from-a-service-in-a-vsto-add-in-project.md).

![ссылка на видео](../vsto/media/playvideo.gif "ссылка на видео") демонстрационные видеоматериалы см. в разделе [инструкции: Взаимодействует с веб-службами из Microsoft Excel? ](http://go.microsoft.com/fwlink/?LinkID=130284).

## <a name="to-populate-a-document-level-project-with-data-from-a-web-service"></a>Заполнение проекта уровня документа данными из веб-службы

1.  Откройте окно **Источники данных** и создайте источник данных для проекта. Дополнительные сведения см. в разделе [Добавление новых источников данных](../data-tools/add-new-data-sources.md).

2.  Перетащите нужное поле или таблицу из окна **Источники данных** в ваш документ.

     В документе создается элемент управления, создается объект <xref:System.Windows.Forms.BindingSource> , привязанный к классу объекта в проекте, и создаются классы для службы.

3.  В коде создайте экземпляр класса веб-службы, которая использовалась на шаге 1.

4.  Если имеются свойства, необходимые для взаимодействия с веб-службой, создайте экземпляры этих свойств.

5.  Создайте и отправьте запрос данных с помощью методов, предоставляемых веб-службой, и экземпляров свойств, созданных на шаге 4.

     Методы, которые можно использовать, зависят от того, веб-службы.

6.  Назначьте данные, возвращенные из веб-службы для <xref:System.Windows.Forms.BindingSource.DataSource%2A> свойство <xref:System.Windows.Forms.BindingSource>.

При запуске проекта элемент управления отображает первую запись в источнике данных. Вы можете включить прокрутку записей посредством обработки текущих событий, используя объекты в <xref:System.Windows.Forms.BindingSource>.

## <a name="see-also"></a>См. также

- [Привязка данных к элементам управления в решениях Office](../vsto/binding-data-to-controls-in-office-solutions.md)
- [Добавление новых источников данных](../data-tools/add-new-data-sources.md)
- [Привязка элементов управления Windows Forms к данным в Visual Studio](../data-tools/bind-windows-forms-controls-to-data-in-visual-studio.md)
- [Практическое руководство. Заполнение листов данными из базы данных](../vsto/how-to-populate-worksheets-with-data-from-a-database.md)
- [Практическое руководство. Заполнение документов данными из объектов](../vsto/how-to-populate-documents-with-data-from-objects.md)
- [Практическое руководство. Заполнение документов данными из базы данных](../vsto/how-to-populate-documents-with-data-from-a-database.md)
- [Практическое руководство. Обновить источник данных с данными из элемента управления ведущего приложения](../vsto/how-to-update-a-data-source-with-data-from-a-host-control.md)