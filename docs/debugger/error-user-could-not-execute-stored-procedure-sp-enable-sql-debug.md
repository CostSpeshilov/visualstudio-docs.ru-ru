---
title: 'Ошибка: Не удалось выполнить хранимую процедуру sp_enable_sql_debug пользователя | Документация Майкрософт'
ms.date: 11/04/2016
ms.topic: troubleshooting
dev_langs:
- CSharp
- VB
- FSharp
- C++
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 9c80a4055b899f155b4be8e7832df9f3aa22db20
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MTE95
ms.contentlocale: ru-RU
ms.lasthandoff: 01/02/2019
ms.locfileid: "53903582"
---
# <a name="error-user-could-not-execute-stored-procedure-spenablesqldebug"></a>Ошибка: Пользователю не удалось выполнить хранимую процедуру sp_enable_sql_debug

Хранимую процедуру sp_enable_sql_debug не удалось выполнить на сервере. Для этого могут быть следующие причины:

- Проблема подключения. Подключение к серверу должно быть стабильным.

- Отсутствие необходимых разрешений на сервере. Для отладки на SQL Server 2005 учетная запись, запущенная Visual Studio, и учетная запись, используемая для подключения к SQL Server, должны быть членами роли системного администратора. Учетная запись, используемая для подключения к SQL Server, является либо учетной записью Windows (при использовании проверки подлинности Windows) либо учетной записью с идентификатором пользователя и паролем (при использовании проверки подлинности SQL).

Дополнительные сведения см. в разделе [Как Задайте разрешения SQL Server для отладки](https://msdn.microsoft.com/84e088d0-0409-41d4-841b-f5d4b0fda414).

## <a name="see-also"></a>См. также раздел

- [Практическое руководство. Задайте разрешения SQL Server для отладки](https://msdn.microsoft.com/84e088d0-0409-41d4-841b-f5d4b0fda414)
- [Настройка отладки SQL](/previous-versions/visualstudio/visual-studio-2010/s4sszxst\(v\=vs.100\))