---
title: Как выполнить Использование, изменить и продолжить (C#) | Документация Майкрософт
ms.date: 10/04/2018
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- Edit and Continue [C#], about Edit and Continue
ms.assetid: 40e136d8-a08c-43bd-b313-fb821c55eb3c
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- dotnet
ms.openlocfilehash: b694f2d3603c9b768a9a4ddbf7b2c66cf5c61b21
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MTE95
ms.contentlocale: ru-RU
ms.lasthandoff: 01/02/2019
ms.locfileid: "53861972"
---
# <a name="how-to-use-edit-and-continue-c"></a>Как выполнить Изменить и продолжить (C#)
Изменить и продолжить можно создать и применить изменения в код в режиме приостановки выполнения во время отладки, без необходимости остановки и перезапуска сеанса отладки.  

Изменить и продолжить для C# происходит автоматически, когда вы измените код в режиме приостановки выполнения, а затем продолжить отладку с помощью **Продолжить**, **шаг**, или **задать следующий оператор**, или вычислите функцию в окне отладчика.  

Дополнительные сведения см. в разделе [изменить и продолжить (Visual C#)](../debugger/edit-and-continue-visual-csharp.md).

>[!NOTE]
>Изменить и продолжить, не поддерживается для оптимизированных для операций, одновременно, или кода интеграции (со средой CLR) среды CLR SQL Server. Сведения о других неподдерживаемых сценариев, см. в разделе [поддерживаемые изменения кода (C# и Visual Basic)](../debugger/supported-code-changes-csharp.md). Если попытаться изменить и продолжить с помощью одного из этих сценариев, появится сообщение о том, что изменить и продолжить не поддерживается.  
  
**Чтобы включить или отключить, изменить и продолжить:**  
   
1. Если вы в сеансе отладки, Остановите отладку (**Отладка** > **остановить отладку** или **Shift**+**F5**) .
   
1. В **средства** > **параметры** (или **Отладка** > **параметры**) > **отладки**  >  **Общие**установите или снимите **включить изменить и продолжить** "флажок".  
  
Параметр вступает в силу при запуске или перезапустить сеанс отладки.  

**Чтобы изменить и продолжить использовать:**  
   
1. Во время отладки в режиме приостановки выполнения, внести изменения в исходный код.  
   
1. В меню **Отладка** выберите команду **Продолжить**, **Шаг** или **Задать следующий оператор** или вычислите функцию в окне отладчика.  
   
   Отладка продолжается с новой, скомпилированный код. 

Некоторые виды изменений кода не поддерживаются в режиме Edit и Continue. Дополнительные сведения см. в разделе [поддерживаемые изменения кода (C# и Visual Basic)](../debugger/supported-code-changes-csharp.md).   
