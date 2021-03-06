---
title: Выбор места установки
description: Узнайте, как уменьшить пространство, занимаемое установкой Visual Studio на системном диске, переместив кэш загрузки, общие компоненты, пакеты SDK и средства на разные диски.
ms.date: 11/07/2018
ms.custom: seodec18
ms.prod: visual-studio-dev15
ms.topic: conceptual
helpviewer_keywords:
- change installation locations for Visual Studio
- select an installation location for Visual Studio files
- move installation files to different drives
- use the D drive
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: ce04592b6de6be16047baf3736e020c2ba71536a
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/02/2019
ms.locfileid: "53837619"
---
# <a name="select-the-installation-locations-in-visual-studio-2017"></a>Выбор расположения установки в Visual Studio 2017

**Новая возможность в версии 15.7**. Вы можете уменьшить место, занимаемое установкой Visual Studio на системном диске, изменив расположение ее файлов. В частности, можно использовать другое расположение для кэша загрузки, общих компонентов, пакетов SDK и файлов средств.

   > [!NOTE]
   > Некоторые средства и пакеты SDK имеют другие правила расположения установки. Эти средства и пакеты SDK устанавливаются на системном диске, даже если вы выбрали другое расположение.

Готовы начать работу? Ниже описывается порядок действий.

1. При установке Visual Studio откройте вкладку **Расположения установки**.

   ![Visual Studio 2017 — выбор расположения установки](media/vs-installation-locations.png "Выберите расположение установки.")

1. В разделе **Visual Studio IDE** примите значение по умолчанию. Visual Studio устанавливает основной продукт и файлы, относящиеся к этой версии Visual Studio.

   ![Раздел Visual Studio IDE на вкладке "Расположения установки"](media/vs-installation-locations-ide.png "Примите значение по умолчанию для раздела Visual Studio IDE на вкладке \"Расположения установки\".")

   > [!TIP]
   > Если системный диск является твердотельным накопителем (SSD), рекомендуется принять расположение по умолчанию на системном диске. Почему? При разработке с помощью Visual Studio вы часто считываете и записываете данные в большом количестве файлов, что увеличивает интенсивность дисковых операций ввода-вывода. Рекомендуется выбрать самый быстрый диск, чтобы справиться с нагрузкой.

1. В разделе **Кэш загрузки** решите, следует ли сохранить кэш загрузки, а затем выберите место для его хранения.

     ![Раздел "Кэш загрузки" вкладки "Расположения установки"](media/vs-installation-locations-cache.png "Выберите, следует ли сохранить кэш загрузки после установки, а затем укажите диск, где будут храниться файлы.")

    1. Установите или снимите флажок **Сохранить кэш скачивания после установки**.

       Если вы решили не сохранять кэш загрузки, это расположение будет использоваться временно. Это действие не повлияет на файлы из предыдущей установки и не приведет к их удалению.

    1. Укажите диск, где будут храниться файлы установки и манифесты из кэша загрузки.

        Например, при выборе рабочей нагрузки "Разработка классических приложений на C++" потребуется 1,58 ГБ пространства на системном диске, но после завершения установки этот объем будет освобожден.

       > [!IMPORTANT]
       > Это расположение задается во время первой установки. Его невозможно изменить позже в пользовательском интерфейсе установщика. Вместо этого вы можете [использовать параметры командной строки](use-command-line-parameters-to-install-visual-studio.md) для перемещения кэша загрузки.

1. В разделе **Общие компоненты, инструменты и пакеты SDK** укажите диск, где вы хотите сохранить файлы, используемые совместно параллельными установками Visual Studio. Пакеты SDK и инструменты также сохраняются в этом каталоге.

   ![Раздел "Общие компоненты, инструменты и пакеты SDK" вкладки "Расположения установки"](media/vs-installation-locations-shared.png "Укажите расположение, где вы хотите сохранить общие компоненты, инструменты и пакеты SDK.")

[!INCLUDE[install_get_support_md](includes/install_get_support_md.md)]

## <a name="see-also"></a>См. также

* [Установка Visual Studio 2017](install-visual-studio.md)
* [Обновление Visual Studio 2017](update-visual-studio.md)
* [Изменение Visual Studio 2017](update-visual-studio.md)
* [Удаление Visual Studio 2017](uninstall-visual-studio.md)
