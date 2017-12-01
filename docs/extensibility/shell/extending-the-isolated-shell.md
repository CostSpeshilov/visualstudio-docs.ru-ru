---
title: "Расширение изолированной оболочки | Документы Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords: Visual Studio shell, isolated mode
ms.assetid: 9a641d8f-211e-4486-a1b1-4a89fafe7ee8
caps.latest.revision: "10"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 063a569ff047b3febd2608cb3c1e0003f40f7785
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2017
---
# <a name="extending-the-isolated-shell"></a>Расширение изолированной оболочки
Оболочка Visual Studio изоляцией можно расширить путем добавления пакетов VSPackage, Managed Extensibility Framework (MEF) компонент или универсального проекта VSIX в приложение изолированной оболочки.  
  
> [!NOTE]
>  Следующие шаги presuppose, что вы создали приложение основные изолированной оболочки с помощью шаблона проекта изолированной оболочки Visual Studio. Дополнительные сведения об этом шаблоне проекта см. в разделе [Пошаговое руководство: создание базового приложения Isolated Shell](walkthrough-creating-a-basic-isolated-shell-application.md).  
  
## <a name="locations-for-the-visual-studio-package-project-template"></a>Расположения для шаблона Visual Studio Package  
 Шаблон проекта пакета Visual Studio можно найти в трех разных местах диалогового окна **Создание проекта** .  
  
1.  В разделе **Visual Basic**, **расширяемости**. Язык проекта по умолчанию — Visual Basic.  
  
2.  В разделе **Visual C#**, **расширяемости**. Язык проекта по умолчанию — C#.  
  
3.  В разделе **других типов проектов**, **расширяемости**. Язык проекта по умолчанию — C++.  
  
## <a name="adding-a-vspackage"></a>Добавление пакетов VSPackage  
 Пакет VSPackage можно добавить в приложение изолированной оболочки. Ниже показано, как создать ключ, добавляющий команды меню.  
  
#### <a name="to-add-a-new-vspackage"></a>Добавление нового пакета VSPackage  
  
1.  Добавление проекта пакета Visual Studio с именем `MenuCommandsPackage`.  
  
2.  На **базовых сведений о VSPackage** мастера, установить **название компании** для `Fabrikam` и **имя VSPackage** для `FabrikamMenuCommands`. Выберите **Далее** кнопки.  
  
3.  На следующей странице выберите **команду меню** и выберите **Далее**.  
  
4.  На следующей странице установите **имя команды** для `Fabrikam Command` и **идентификатор команды** для `cmdidFabrikamCommand`и нажмите кнопку **Далее**.  
  
5.  На **Выбор параметров тестирования проекта** снимите параметры тестирования и нажмите кнопку **Готово** кнопки.  
  
6.  В проект ShellExtensionsVSIX откройте файл source.extension.vsixmanifest.  
  
     **Активы** раздел должен содержать запись для проекта VSShellStub.AboutBoxPackage.  
  
7.  Выберите **New** кнопки.  
  
8.  В **добавить новый актив** окна в **тип** выберите **Microsoft.VisualStudio.VsPackage**.  
  
9. В **источника** списке, убедитесь, что **проекта в текущем решении** выбран. В **проекта** выберите **MenuCommandsPackage**.  
  
10. Сохраните и закройте файл.  
  
11. Перестройте решение и запустить отладку изолированной оболочки.  
  
12. В строке меню выберите **средства** меню, затем **команда Fabrikam**.  
  
     Появится окно сообщения.  
  
13. Остановите отладку приложения.  
  
## <a name="adding-a-mef-component-part"></a>Добавление элемента отчета компонентов MEF  
 Ниже показано, как добавить в приложение изолированной оболочки компонент MEF.  
  
#### <a name="to-add-a-mef-component"></a>Чтобы добавить компонент MEF  
  
1.  В **Добавление нового проекта** диалогового **Visual C#**, **расширяемости**, используйте **поле редактора** шаблона, чтобы добавить в проект. Присвойте обработчику события имя `ShellEditorMargin`.  
  
2.  В проект ShellExtensionsVSIX откройте файл Source.extension.vsixmanifest в режиме конструктора, а не в представлении кода.  
  
3.  В `Asset` выберите **Добавление содержимого**.  
  
4.  В **добавить новый актив** окна в **тип** выберите **Microsoft.VisualStudio.MefComponent**.  
  
5.  В **источника** списке, убедитесь, что **проекта в текущем решении** выбран. В **проекта** выберите **ShellEditorMargin**.  
  
6.  Сохраните и закройте файл.  
  
7.  Перестройте решение и запустить отладку изолированной оболочки.  
  
8.  Откройте текстовый файл.  
  
     Зеленый поля, который содержит слова «Hello world!» должны отображаться в нижней части файла в текстовом окне.  
  
9. Остановите отладку приложения.  
  
## <a name="adding-a-generic-vsix-project"></a>Добавление проекта VSIX, универсальные  
  
#### <a name="to-add-a-generic-vsix-project"></a>Добавление универсального проекта VSIX  
  
1.  В **Добавление нового проекта** диалогового **Visual C#**, **расширяемости**, используйте **VSIXProject** шаблона, чтобы добавить в проект. Присвойте обработчику события имя `EmptyVSIX`.  
  
2.  В проект ShellExtensionsVSIX откройте файл Source.extensions.vsixmanifest в режиме конструктора, а не в представлении кода.  
  
3.  В `Assets` выберите **New**.  
  
4.  В **добавить новый актив** окна в **тип** выберите тип содержимого, которые вы хотите добавить.  
  
5.  В **источника**, убедитесь, что **проект в текущем решении** выбран параметр. В окне списка выберите имя проекта VSIX.  
  
6.  Сохраните и закройте файл.  
  
7.  Если этот проект содержит скомпилированный код, необходимо изменить проект, чтобы сборка включена в выходных данных.  
  
    1.  Выгрузить проект VSIX и откройте файл проекта.  
  
    2.  В первом `<PropertyGroup>` блока, измените значение `<CopyBuildOutputToOutputDirectory>` для `true`.  
  
    3.  Сохраните и перезагрузить проект.  
  
8.  Постройте и запустите это решение.  
  
## <a name="see-also"></a>См. также  
 [Пошаговое руководство. Создание базового приложения изолированной оболочки](walkthrough-creating-a-basic-isolated-shell-application.md)