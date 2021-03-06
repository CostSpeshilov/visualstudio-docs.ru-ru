---
title: Предоставление автоматизации для пакетов VSPackage | Документация Майкрософт
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- VSPackages, automation [Visual Studio SDK]
- automation [Visual Studio SDK], VSPackages
ms.assetid: 104c4c55-78b8-42f4-b6b0-9a334101aaea
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 50d707c42196d727a35ca7c9d9cef250c60f7d5b
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/25/2019
ms.locfileid: "55018076"
---
# <a name="providing-automation-for-vspackages"></a>Предоставление автоматизации для пакетов VSPackage
Существует два основных способа для обеспечения автоматизации пакетов VSPackage: путем реализации объекты VSPackage и реализации объектов автоматизации standard. Как правило они используются вместе для расширения модели автоматизации среды.  
  
## <a name="vspackage-specific-objects"></a>Объекты VSPackage  
 Определенных местах внутри модели автоматизации требуют предоставления объекты автоматизации, которые уникальны для VSPackage. Например новые проекты требуют различных объектов, которые предоставляет только VSPackage. Имена этих объектов являются занесен в реестр и получить с помощью вызовов к среде `DTE` объекта.  
  
 Также можно получить объекты определенного VSPackage, когда потребитель автоматизации использует объект, предоставленный через свойство объекта стандартный объект. Например, стандартные `Window` объект имеет `Object` свойство, часто называется `Windows.Object` свойство. При вызове метода потребители `Window.Object` в окне, реализованные в пакете VSPackage, передается обратно автоматизации объект вашего собственного.  
  
#### <a name="projects"></a>Проекты  
 Пакеты VSPackage может расширить модель автоматизации для новых типов проектов через собственные объекты определенного VSPackage. Основная цель предоставляя новые объекты автоматизации для VSPackage — для различения уникальный проекта объектов из <xref:Microsoft.VisualStudio.VCProjectEngine.VCProject> или <xref:VSLangProj80.VSProject2> объекта. Этих различий он удобен, если вы хотите предоставить возможность выделить или итерации вашего типа проекта, помимо других типов проектов, они отображаются side-by-side в решении. Дополнительные сведения см. в разделе [предоставление объектов проекта](../../extensibility/internals/exposing-project-objects.md).  
  
#### <a name="events"></a>События  
 Архитектура событий среды предлагает другое место, можно добавлять собственные объекты определенного VSPackage. Например путем создания собственных объектов событий с уникальным, вы можете расширить модель событий среды для проектов. Может потребоваться предоставить свои собственные события, при добавлении нового элемента в проект собственного типа. Дополнительные сведения см. в разделе [предоставление событий](../../extensibility/internals/exposing-events-in-the-visual-studio-sdk.md).  
  
#### <a name="window-objects"></a>Объекты окон  
 Windows может снова передавать объект автоматизации определенного VSPackage в среду, при вызове. Объект, который является производным от реализации <xref:Microsoft.VisualStudio.Shell.Interop.IVsExtensibleObject>, <xref:EnvDTE.IExtensibleObject> или `IDispatch` , передает обратно свойства, расширяя объект окна, в котором он размещен. Например этот подход можно использовать для предоставления службы автоматизации для элемента управления, находящегося в рамке окна. Этот объект и другие объекты, которые она может расширить семантика вам для разработки. Дополнительные сведения см. в разделе [Как Автоматизация для Windows](../../extensibility/internals/how-to-provide-automation-for-windows.md).  
  
#### <a name="options-pages-on-the-tools-menu"></a>Параметры страницы в меню "Сервис"  
 Можно создавать страницы для расширения инструментов, модель автоматизации параметры реализации страницы и добавления сведений в реестр, чтобы создать свои собственные параметры. На страницах можно затем вызывать с помощью объектной модели среды, как и все остальные параметры страницы. Если для разработки компонента, добавляемого в среде с помощью пакетов VSPackage требуются параметры страницы, то необходимо добавить также поддержка модели автоматизации. Дополнительные сведения см. в разделе [Поддержка автоматизации страниц параметров](../../extensibility/internals/automation-support-for-options-pages.md).  
  
## <a name="standard-automation-objects"></a>Объекты автоматизации Standard  
 Для расширения автоматизации для проектов, вы также реализовать объекты автоматизации standard (производный от `IDispatch`), рядом с другими объектами проекта, а также реализовывать стандартные методы и свойства. Стандартные объекты примеры, которые вставляются в иерархии решения, такие как объекты проекта `Projects`, `Project`, `ProjectItem`, и `ProjectItems`. Каждый новый тип проекта следует реализовать эти объекты (и, возможно, другие реестры в зависимости от семантики вашего проекта).  
  
 В некотором смысле эти объекты предоставляют противоположной преимущество объекты проекта определенного VSPackage. Объекты автоматизации standard разрешить проект, чтобы использовать обобщенный так, как любой другой проект, которые поддерживают те же объекты. Таким образом, надстройки, написанный для Общие `Project` и `ProjectItem` объектов может работать с проектами любого типа. Дополнительные сведения см. в разделе [проекта моделирования](../../extensibility/internals/project-modeling.md).