---
title: Управляемые пакеты VSPackage | Документация Майкрософт
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- devlang-csharp
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- VSPackages, managed
- managed VSPackages
ms.assetid: a4f17068-c563-45a8-bbbf-4203ea99e9d2
caps.latest.revision: 34
manager: douge
ms.openlocfilehash: 44507112ceb3e7bed452ef4ced7633001224ad82
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/12/2018
ms.locfileid: "49227088"
---
# <a name="managed-vspackages"></a>Управляемые пакеты VSPackage
Следующие разделы описывают создание пакета VSPackage. VSPackage — это модуль программного обеспечения, который расширяет [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] интегрированной среды разработки (IDE), предоставляя элементы пользовательского интерфейса (UI), службы, проекты, редакторы и конструкторы. Дополнительные сведения см. в разделе [VSPackages](../extensibility/internals/vspackages.md).  
  
## <a name="in-this-section"></a>В этом разделе  
 [Использование сборок взаимодействия Visual Studio](../extensibility/internals/using-visual-studio-interop-assemblies.md)  
 Описывает функции и расположение [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] взаимодействия сборки и пространства имен, они предоставляют.  
  
 [Информация HRESULT в управляемом коде](../misc/hresult-information-in-managed-code.md)  
 Описывает, как для преобразования значения HRESULT информацию в возникающих исключениях и `int` возвращаемые значения в управляемом коде.  
  
 [Маршалинг параметров сборки взаимодействия Visual Studio](../misc/visual-studio-interop-assembly-parameter-marshaling.md)  
 Обсуждаются проблемы взаимодействия между [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] сборок взаимодействия и COM-интерфейсов.  
  
 [Пакеты VSPackage и Managed Package Framework](../misc/vspackages-and-the-managed-package-framework.md)  
 Описывает и перечислены имена пространств классов framework (MPF) управляемых пакетов и DLL-файлы и показано, как использовать их для создания VSPackage.  
  
 [Ресурсы в пакетах VSPackage](../extensibility/internals/resources-in-vspackages.md)  
 Описывает использование управляемых и неуправляемых ресурсов в управляемые пакеты VSPackage.  
  
## <a name="related-sections"></a>Связанные разделы  
 [Служебные программы VSSDK](../extensibility/internals/vssdk-utilities.md)  
 Представляет коллекцию VSPackage внутренние компоненты и дополнительные разделы.