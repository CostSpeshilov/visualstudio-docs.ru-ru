---
title: CA2207. Используйте встроенную инициализацию статических полей типов значений
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- InitializeValueTypeStaticFieldsInline
- CA2207
helpviewer_keywords:
- CA2207
- InitializeValueTypeStaticFieldsInline
ms.assetid: d1ea9d8b-ecc2-46ca-86e2-c41dd0e76658
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: fb75c6d06502c9d2fac437a8924af4d51ddd6d0a
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/25/2019
ms.locfileid: "55036164"
---
# <a name="ca2207-initialize-value-type-static-fields-inline"></a>CA2207. Используйте встроенную инициализацию статических полей типов значений

|||
|-|-|
|TypeName|InitializeValueTypeStaticFieldsInline|
|CheckId|CA2207|
|Категория|Microsoft.Usage|
|Критическое изменение|Не критическое|

## <a name="cause"></a>Причина
 Тип значения объявляет явный статический конструктор.

## <a name="rule-description"></a>Описание правила
 При объявлении типа значения, она подвергается инициализация по умолчанию, где все поля типа значения присваивается нулевое значение, а все поля ссылочного типа присваивается `null` (`Nothing` в Visual Basic). Явный статический конструктор гарантируется только до выполнения конструктора экземпляра или вызове статического члена типа. Таким образом Если тип создается без вызова конструктора экземпляра, статическом конструкторе не гарантируется для запуска.

 Если все статические данные инициализированный встроенные и объявляется явный статический конструктор, компиляторы C# и Visual Basic добавьте `beforefieldinit` флаг к определению класса MSIL. Компиляторы также добавить частный статический конструктор, который содержит статический код инициализации. Этот закрытый статический конструктор обязательно выполняется прежде, чем любые статические поля типа осуществляется.

## <a name="how-to-fix-violations"></a>Устранение нарушений
 Чтобы устранить нарушение этого правила инициализацию всех статических данных, если он объявлен и удалите статический конструктор.

## <a name="when-to-suppress-warnings"></a>Отключение предупреждений
 Для этого правила отключать вывод предупреждений не следует.

## <a name="related-rules"></a>Связанные правила
 [CA1810: Инициализируйте статические поля ссылочного типа встроенными](../code-quality/ca1810-initialize-reference-type-static-fields-inline.md)