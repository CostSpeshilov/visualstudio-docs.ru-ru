---
title: Команда Toggle Breakpoint
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- debug.togglebreakpoint
helpviewer_keywords:
- ToggleBreakpoint command
- Debug.ToggleBreakPoint command
- Toggle Breakpoint command
ms.assetid: d50dfadb-ce79-4d5e-9c09-1cfddd57876d
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 7a2e9857e752d01f03e7d9219c5e030dae921cc9
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/02/2019
ms.locfileid: "53833757"
---
# <a name="toggle-breakpoint-command"></a>Команда Toggle Breakpoint
Включает или отключает точку останова в зависимости от ее текущего состояния и текущей позиции в файле.

## <a name="syntax"></a>Синтаксис

```
Debug.ToggleBreakpoint [text]
```

## <a name="arguments"></a>Аргументы
 `text` Необязательный. Если текст указан, строка помечается как именованная точка останова. В противном случае строка помечается как неименованная точка останова, что аналогично нажатию клавиши F9.

## <a name="example"></a>Пример
 В этом примере переключается текущая точка останова.

```
>Debug.ToggleBreakpoint
```

## <a name="see-also"></a>См. также раздел

- [Команды Visual Studio](../../ide/reference/visual-studio-commands.md)
- [Командное окно](../../ide/reference/command-window.md)
- [Поле "Поиск/команда"](../../ide/find-command-box.md)
- [Visual Studio Command Aliases](../../ide/reference/visual-studio-command-aliases.md)