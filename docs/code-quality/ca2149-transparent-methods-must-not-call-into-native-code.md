---
title: CA2149. Прозрачные методы не должны вызывать машинный код
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- CA2149
ms.assetid: 28951bd7-f3db-4871-99aa-bad68d1ead80
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- cplusplus
ms.openlocfilehash: 4811a117220aa154283d97d44d49a8257c4be86e
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/25/2019
ms.locfileid: "55031803"
---
# <a name="ca2149-transparent-methods-must-not-call-into-native-code"></a>CA2149. Прозрачные методы не должны вызывать машинный код

|||
|-|-|
|TypeName|TransparentMethodsMustNotCallNativeCode|
|CheckId|CA2149|
|Категория|Microsoft.Security|
|Критическое изменение|Критическое|

## <a name="cause"></a>Причина
 Метод вызывает собственную функцию через прототип метода, например P/Invoke.

## <a name="rule-description"></a>Описание правила
 Это правило срабатывает для любого прозрачного метода, который напрямую вызывает машинный код, например, через P/Invoke. Нарушение этого правила приводит к <xref:System.MethodAccessException> в уровне 2 модели прозрачности и полного <xref:System.Security.Permissions.SecurityPermissionAttribute.UnmanagedCode%2A> на уровне 1 модели прозрачности.

## <a name="how-to-fix-violations"></a>Устранение нарушений
 Чтобы устранить нарушение этого правила, отметьте метод, который вызывает машинный код с <xref:System.Security.SecurityCriticalAttribute> или <xref:System.Security.SecuritySafeCriticalAttribute> атрибута.

## <a name="when-to-suppress-warnings"></a>Отключение предупреждений
 Для этого правила отключать вывод предупреждений не следует.

## <a name="example"></a>Пример
 [!code-csharp[FxCop.Security.CA2149.TransparentMethodsMustNotCallNativeCode#1](../code-quality/codesnippet/CSharp/ca2149-transparent-methods-must-not-call-into-native-code_1.cs)]