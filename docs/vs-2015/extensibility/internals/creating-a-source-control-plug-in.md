---
title: Создание подключаемого модуля системы управления версиями | Документация Майкрософт
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- plug-ins, source control
- source control plug-ins
- source control [Visual Studio SDK], plug-ins
ms.assetid: c7e69fa4-150e-469a-a6fc-fa1260bdbb07
caps.latest.revision: 19
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 04f8cc2f165ddbce41055bc087e1449d3be8ab9e
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/16/2018
ms.locfileid: "51804427"
---
# <a name="creating-a-source-control-plug-in"></a>Создание подключаемого модуля системы управления версиями
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Пакет SDK для Visual Studio предоставляет ресурсы, которые позволяют добавлять возможности элемента управления источника для [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] интегрированной среды разработки (IDE). Он позволяет использовать библиотеку DLL для подключаемого модуля, который соответствует с API подключаемых модулей управления источника, приведенные в этой документации.  
  
## <a name="in-this-section"></a>В этом разделе  
 [Начало работы](../../extensibility/internals/getting-started-with-source-control-plug-ins.md)  
 Описывается, как установить подключаемый модуль системы управления версиями и выделяет в настоящее время доступные версии API подключаемого модуля управления источника.  
  
 [Архитектура](../../extensibility/internals/source-control-plug-in-architecture.md)  
 Использует схему архитектуры, чтобы объяснить, интеграция системы управления версиями, подключаемый модуль с [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] интегрированной среды разработки.  
  
 [Руководство по тестированию подключаемых модулей системы управления версиями](../../extensibility/internals/test-guide-for-source-control-plug-ins.md)  
 Содержит рекомендации о том, как для проверки установки и работы подключаемого модуля системы управления версиями.  
  
## <a name="related-sections"></a>Связанные разделы  
 [Создание пакета VSPackage системы управления версиями](../../extensibility/internals/creating-a-source-control-vspackage.md)  
 Описывает, как создать пакет VSPackage, который не только предоставляет функции системы управления версиями, но заменяет элемент управления источником [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] система управления версиями пользовательского интерфейса.  
  
 [Подключаемые модули системы управления версиями](../../extensibility/source-control-plug-ins.md)  
 Предоставляет полный список всех элементов в API подключаемых модулей управления источника.  
  
 [Система управления версиями](../../extensibility/internals/source-control.md)  
 Обсуждаются параметры для реализации системы управления версиями в виде интегрированной функцией [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)].

