---
title: Создание многократно используемых элементов управления для веб-частей или страниц приложений | Документация Майкрософт
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- user controls [SharePoint development in Visual Studio], creating
- SharePoint development in Visual Studio, user controls
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 4b1605705b161dfdb8b5857dcab6075d9a997a55
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/24/2019
ms.locfileid: "54874579"
---
# <a name="create-reusable-controls-for-web-parts-or-application-pages"></a>Создание многократно используемых элементов управления для веб-частей или страниц приложений
  Visual Studio позволяет создавать пользовательские элементы управления с возможностью повторного использования, которые можно размещать на страницах приложений и в веб-частях, используемых в SharePoint. Эти элементы управления называются пользовательскими элементами управления. Пользовательский элемент управления представляет собой составной элемент управления, который работает практически аналогично веб-страницу ASP.NET — можно добавить существующий элемент управления и разметки в пользовательский элемент управления и определить свойства и методы для элемента управления. Затем их можно внедрить в веб-страницы ASP.NET, где они будут действовать как единое целое.  
  
## <a name="create-a-user-control"></a>Создать пользовательский элемент управления
 Чтобы создать пользовательский элемент управления, добавьте **пользовательский элемент управления** для **Empty SharePoint Project**. Дополнительные сведения см. в разделе [Как Создать пользовательский элемент управления для части страницы или веб-приложения SharePoint](../sharepoint/how-to-create-a-user-control-for-a-sharepoint-application-page-or-web-part.md).  
  
 При добавлении **пользовательский элемент управления** товар, Visual Studio создает папку в проекте, а затем добавляет несколько файлов в папку. В следующей таблице описаны каждого файла.  
  
|Файл|Описание:|  
|----------|-----------------|  
|Файл пользовательского элемента управления|Определяет пользовательский элемент управления. Проектирование пользовательского элемента управления путем добавления элементов управления и разметки в этот файл.|  
|Файл кода|Содержит код программной части пользовательского элемента управления. Добавьте код для обработки событий в этот файл.|  
|Файл кода конструктора|Содержит код, созданный с помощью конструктора, не следует изменять непосредственно.|  
  
## <a name="design-the-user-control"></a>Проектирование пользовательского элемента управления
 Разработка пользовательского элемента управления с помощью конструктора Visual Web Developer в Visual Studio. Этот конструктор появляется при открытии файла пользовательского элемента управления в проекте и выберите **разработки** вкладки.  

## <a name="consume-the-user-control"></a>Использование пользовательского элемента управления
 Пользовательские элементы управления не отображаются в SharePoint до их включения в страницу приложения или веб-части.  
  
 Чтобы включить пользовательский элемент управления в страницу приложения, откройте веб-страницы, к которому требуется добавить пользовательский элемент управления ASP.NET. Переключитесь в конструктор, а затем выберите файл настраиваемого пользовательского элемента управления в обозревателе решений и перетащите его на странице. Пользовательский элемент управления ASP.NET добавляется на страницу, а конструктор создает директиву @ Register, который необходим для распознавания в пользовательский элемент управления страницей. Теперь вы можете работать с открытые свойства и методы элемента управления.  
  
 Чтобы включить пользовательский элемент управления в веб-части, добавьте пользовательский элемент управления веб-части <xref:System.Web.UI.WebControls.WebParts.Part.Controls%2A> коллекции в файле кода веб-части. В следующем примере добавляется пользовательский элемент управления для <xref:System.Web.UI.WebControls.WebParts.Part.Controls%2A> коллекции веб-части.  
  
 [!code-vb[SP_VisualWebPart#5](../sharepoint/codesnippet/VisualBasic/sp_visualwebpart.vb/visualwebpart1/visualwebpart1.vb#5)]
 [!code-csharp[SP_VisualWebPart#5](../sharepoint/codesnippet/CSharp/sp_visualwebpart.cs/visualwebpart1/visualwebpart1.cs#5)]  
  
## <a name="debug-a-user-control"></a>Отладка пользовательского элемента управления
 Чтобы выполнить отладку пользовательского элемента управления, убедитесь, что пользовательский элемент управления включен в страницу приложения или веб-части в проекте SharePoint. Затем можно отлаживать код в пользовательский элемент управления так же, как отладка кода в любом проекте Visual Studio.  
  
 При запуске отладчика Visual Studio, Visual Studio открывает сайт SharePoint.  
  
 В SharePoint откройте страницу приложения, которая содержит пользовательский элемент управления. Если пользовательский элемент управления включен в веб-часть, добавьте веб-часть на страницу веб-части в SharePoint.  
  
 Дополнительные сведения об отладке проектов SharePoint см. в разделе [решений SharePoint, устранение неполадок](../sharepoint/troubleshooting-sharepoint-solutions.md).  
  
## <a name="related-topics"></a>См. также
  
|Заголовок|Описание:|  
|-----------|-----------------|  
|[Практическое руководство. Создать пользовательский элемент управления для части страницы или веб-приложения SharePoint](../sharepoint/how-to-create-a-user-control-for-a-sharepoint-application-page-or-web-part.md)|Показано, как создать пользовательские элементы управления, которые могут быть использованы на страницах приложений и веб-частях, используемых в SharePoint.|  
