---
title: 'Предупреждение системы безопасности: Отладчик должен выполнить ненадежную команду | Документация Майкрософт'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.debug.sourceserver.securityalert
dev_langs:
- FSharp
- VB
- CSharp
- C++
ms.assetid: e5c004b3-b364-4098-ac98-770076ca9981
caps.latest.revision: 16
author: MikeJo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: c4f37f629d12a94c65031543d196be92b3f259b6
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/16/2018
ms.locfileid: "51744731"
---
# <a name="security-warning-debugger-must-execute-untrusted-command"></a>Security Warning: Debugger Must Execute Untrusted Command
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Это диалоговое окно с предупреждением появляется при использовании сервера системы управления версиями. Оно указывает, что команды, которую должен выполнить отладчик для получения исходного кода, нет в списке доверенных команд для сервера системы управления версиями, содержащемся в файле srcsvr.ini. Если это допустимая команда, ее можно добавить в файл srcsvr.ini. В противном случае ее не следует выполнять. Дополнительные сведения см. в разделе [Указание файлов символов (.pdb) и файлов с исходным кодом](../debugger/specify-symbol-dot-pdb-and-source-files-in-the-visual-studio-debugger.md).  
  
## <a name="message-text"></a>Текст сообщения  
 **Отладчик должен выполнить следующую команду без доверия, чтобы получить исходный код с исходного сервера.**  
  
 **Если файл символов отладки (\*PDB-файл) — не из известного и надежного источника, эта команда может быть недопустимой или опасной.**  
  
 **Вы действительно хотите выполнить эту команду?**  
  
## <a name="uielement-list"></a>Список элементов пользовательского интерфейса  
 Текстовое поле  
 Команда из PDB-файла, подлежащая выполнению.  
  
 Запуск  
 Позволить выполнить команду.  
  
 Не выполнять  
 Прекратить выполнение команды и загрузку файла с сервера системы управления версиями.  
  
## <a name="see-also"></a>См. также  
 [Указание файлов символов (.pdb) и исходных файлов](../debugger/specify-symbol-dot-pdb-and-source-files-in-the-visual-studio-debugger.md)   
 [Безопасность отладчика](../debugger/debugger-security.md)   
 [Исходный сервер](http://msdn.microsoft.com/library/windows/desktop/ms680641\(v=vs.85\).aspx)



