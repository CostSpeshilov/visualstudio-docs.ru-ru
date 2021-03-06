---
title: Страница "Общие", папка "Среда", диалоговое окно "Параметры"
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- VS.Message.0x800a002e
- VS.ToolsOptionsPages.Environment.General
- VS.Environment.General
helpviewer_keywords:
- MRU lists
- windows, customizing
- MDI, environment options
- speed, environment animation
- File menu
- menus, customizing
- Windows menu customizing
- status bars, displaying
- Visual Studio Start page, setting
- IDE, startup options
- editors, autocompletion
- Options dialog box, General Environment
- General Environment Options dialog box
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 15af9d627e425df57443cbf663b2b231b74f9a7e
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/02/2019
ms.locfileid: "53945539"
---
# <a name="general-environment-options-dialog-box"></a>Страница "Общие", папка "Среда", диалоговое окно "Параметры"

Используйте эту страницу для изменения цветовых тем, параметров строки состояния, сопоставлений расширений файлов и т. д. для интегрированной среды разработки (IDE). Чтобы открыть диалоговое окно **Параметры**, щелкните меню **Сервис**, выберите **Параметры**, откройте папку **Среда** и выберите страницу **Общие**. Если этой страницы нет в списке, установите флажок **Показать все параметры** в диалоговом окне **Параметры**.

## <a name="visual-experience"></a>Визуальное представление

**Цветовая тема**

Для интегрированной среды разработки можно выбрать **синюю**, **светлую** или **темную** цветовую тему.

Вы можете устанавливать дополнительные предопределенные темы и создавать пользовательские темы, скачав и установив **редактор цветовых тем Visual Studio** из [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=VisualStudioPlatformTeam.VisualStudio2017ColorThemeEditor). После установки этого средства в списке «Цветовая тема» появятся дополнительные темы.

**Применение регистра заголовков в строке меню**

По умолчанию в меню используется **регистр заголовков**. Отмените этот параметр, чтобы задать **ВСЕ ПРОПИСНЫЕ БУКВЫ**.

**Автонастройка представления в зависимости от быстродействия клиента**

Определяет, задает ли Visual Studio корректировку визуального представления автоматически или это делает пользователь. Эта корректировка может изменить способ отображения цветов с градиентов на простые цвета или может ограничить применение анимации в меню или всплывающих окнах.

**Включить расширенное визуальное представление клиента**

Включает все визуальные возможности Visual Studio, в том числе градиенты и анимации. Снимите этот флажок при использовании подключений к удаленному рабочему столу или графических адаптеров старых моделей, так как эти возможности могут снизить производительность в таких случаях. Этот параметр доступен, только если флажок **Автонастройка представления в зависимости от быстродействия клиента** снят.

**Использовать аппаратное ускорение обработки изображения, если доступно**

Позволяет использовать аппаратное ускорение графики вместо программного, если оно доступно.

## <a name="other"></a>Другое

**Пунктов в меню "Окно"**

Задает количество окон, отображаемых в списке окон меню **Окно**. Введите число от 1 до 24. Число по умолчанию — 10.

**Пунктов в списках последних использованных элементов**

Задает число недавно использованных проектов и файлов, отображаемых в меню **Файл**. Введите число от 1 до 24. Число по умолчанию — 10. Это удобный способ доступа к недавно использованным проектам и файлам.

**Показать строку состояния**

Отображает строку состояния. Строка состояния расположена в нижней части окна интегрированной среды разработки и содержит сведения о ходе выполнения текущих операций.

**Кнопка закрытия действует только на активное окно**

Указывает, что при нажатии кнопки **Закрыть** закрывается только активное окно с фокусом, а не все закрепленные окна инструментов. Этот параметр выбран по умолчанию.

**Кнопка автоскрытия действует только на активное окно**

Указывает, что при нажатии кнопки **Автоматическое скрытие** автоматически закрывается только окно инструментов с фокусом, а не все закрепленные окна инструментов. По умолчанию этот флажок не установлен.

## <a name="see-also"></a>См. также

- [Диалоговое окно "Параметры среды"](../../ide/reference/environment-options-dialog-box.md)
- [Настройка макетов окон](../../ide/customizing-window-layouts-in-visual-studio.md)