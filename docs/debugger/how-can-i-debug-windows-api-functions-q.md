---
title: Функции Windows API отладки | Документация Майкрософт
ms.custom: seodec18
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.debug.api
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- debugging [C++], Windows API functions
- NT symbols and debugging Windows API functions
- Windows API functions, debugging
- Windows API, debugging API functions
- APIs, debugging
ms.assetid: 7c126f57-62ab-4d94-9805-632d696ba1f0
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 9d10c4804d4d53c22281c11d8afc464cf2ac3732
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MTE95
ms.contentlocale: ru-RU
ms.lasthandoff: 01/02/2019
ms.locfileid: "53861518"
---
# <a name="how-can-i-debug-windows-api-functions"></a>Как отладить функции Windows API?
Если нужно отладить функцию Windows API с загруженными символами NT, необходимо выполнить следующие действия.  
  
### <a name="to-set-a-breakpoint-on-a-windows-api-function-with-nt-symbols-loaded"></a>Установка точки останова в функции Windows API с загруженными символами NT  
  
-   Введите имя функции вместе с именем DLL-файла, в котором эта функция находится. В 32-разрядном коде используйте декорированную форму имени функции. Например, чтобы задать точку останова на **MessageBeep**, необходимо ввести следующее.  
  
    ```cpp
    {,,USER32.DLL}_MessageBeep@4  
    ```  
  
     Чтобы получить декорированное имя, см. в разделе [Просмотр декорированные имена](https://msdn.microsoft.com/library/f79e2717-a4db-4d12-a689-69830cce2be0).  
  
## <a name="see-also"></a>См. также раздел  
 [Вопросы и ответы по отладке машинного кода](../debugger/debugging-native-code-faqs.md)   
 [Отладка машинного кода](../debugger/debugging-native-code.md)
