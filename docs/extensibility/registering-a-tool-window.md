---
title: Регистрация окна инструментов | Документация Майкрософт
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- tool windows, registering managed
- tool windows, registering
ms.assetid: 8c8c4a24-3da4-497b-9db2-0ddd7cfbfdd2
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: f09788cb69e90114839a66ff0652c779535b066b
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/25/2019
ms.locfileid: "54944050"
---
# <a name="register-a-tool-window"></a>Регистрация окна инструментов
Можно зарегистрировать с помощью средства windows <xref:Microsoft.VisualStudio.Shell.ProvideToolWindowAttribute> и <xref:Microsoft.VisualStudio.Shell.ProvideToolWindowVisibilityAttribute>.  
  
## <a name="example"></a>Пример  
  
```csharp
  
[ProvideToolWindow(typeof(PersistedWindowPane), Style = MsVsShell.VsDockStyle.Tabbed, Window = "3ae79031-e1bc-11d0-8f78-00a0c9110057")]
[ProvideToolWindow(typeof(DynamicWindowPane), PositionX=250, PositionY=250, Width=160, Height=180, Transient=true)]
[ProvideToolWindowVisibility(typeof(DynamicWindowPane), /*UICONTEXT_SolutionExists*/"f1536ef8-92ec-443c-9ed7-fdadf150da82")]  
[ProvideMenuResource(1000, 1)]  
[PackageRegistration(UseManagedResourcesOnly = true)]  
[Guid("01069CDD-95CE-4620-AC21-DDFF6C57F012")]  
public class PackageToolWindow : Package  
{  
```
  
 В приведенном выше коде в <xref:Microsoft.VisualStudio.Shell.ProvideToolWindowAttribute> регистрирует `PersistedWindowPane` и `DynamicWindowPane` средство windows с помощью Visual Studio. Окно материализованных инструментов закреплено и с вкладками с **обозревателе решений**, и динамические окна по умолчанию, начальной позицией и размер. Динамическое окно становится временными, которое указывает, что она не была создана во время запуска. Записывает `DontForceCreate` значение в `ToolWindows` ключа в системном реестре. Дополнительные сведения см. в разделе [конфигурацию отображаемое окно средства](../extensibility/tool-window-display-configuration.md).
