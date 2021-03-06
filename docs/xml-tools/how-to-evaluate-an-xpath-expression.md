---
title: Как выполнить вычислить выражение XPath
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
ms.assetid: 159ba4ef-75e4-4ac8-80dc-e064e0bec345
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 9ab895bb10c9f1b70ba103aebeb0ad83cdb84418
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/25/2019
ms.locfileid: "55000982"
---
# <a name="how-to-evaluate-an-xpath-expression"></a>Как выполнить вычислить выражение XPath

Можно оценить выражения XPath **"Быстрая проверка"** диалоговое окно. Выражение XPath должно быть допустимым и соответствовать рекомендация W3C языка XPath версии 1.0. Текущий контекст XSLT — то есть `self::node()` узел в **"Локальные"** окно — предоставляет контекст оценки для выражения XPath.

 В следующем списке перечислены функции, которые поддерживаются при оценке выражения XPath.

-   Поддерживаются встроенные функции XPath.

-   Не поддерживаются встроенные функции XSLT.

-   Не поддерживаются определяемые пользователем функции.

> [!NOTE]
> В следующей процедуре используется *belowAvg.xsl* и *books.xml* файлов из [Пошаговое руководство: Отладка таблицы стилей XSLT](../xml-tools/walkthrough-debug-an-xslt-style-sheet.md) раздела.

## <a name="to-evaluate-an-xpath-expression"></a>Оценка выражения XPath

1.  Добавьте точку останова в начальный тег `xsl:if`.

2.  Нажмите кнопку **Отладка XSL** кнопки на панели инструментов редактора XML.

     Отладчик начинается и останавлявается на теге `xsl:if`.

3.  Щелкните правой кнопкой мыши и выберите **"Быстрая проверка"**.

     **"Быстрая проверка"** диалоговое окно.

4.  Введите `./price/text()` в **выражение** поле **"Быстрая проверка"** диалоговое окно и нажмите кнопку **пересчитать**.

     Цены на текущий узел книги отображается в **значение** поле.

5.  Измените выражение XPath `./price/text() < $bookAverage` и нажмите кнопку **пересчитать**.

     **Значение** поле показывает, что возвращает выражение XPath `true`.

## <a name="see-also"></a>См. также

- [Отладка XSLT](../xml-tools/debugging-xslt.md)