---
title: Удаленная отладка проекта Visual C++ | Документация Майкрософт
ms.custom: remotedebugging
ms.date: 08/14/2017
ms.topic: conceptual
dev_langs:
- C++
- FSharp
- CSharp
- JScript
- VB
helpviewer_keywords:
- remote debugging, setup
ms.assetid: 8b8eca0d-122f-4eda-848a-cf0945f207d0
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- cplusplus
ms.openlocfilehash: bdbcefe1e0878ef6bf2520edb90ce904e414f211
ms.sourcegitcommit: 38db86369af19e174b0aba59ba1918a5c4fe4a61
ms.translationtype: MTE95
ms.contentlocale: ru-RU
ms.lasthandoff: 01/14/2019
ms.locfileid: "54269765"
---
# <a name="remote-debugging-a-visual-c-project-in-visual-studio"></a>Удаленная отладка проекта Visual C++ в Visual Studio
Для отладки приложения Visual Studio на другом компьютере, установите и запустите инструменты удаленной отладки на компьютере, где приложение будет развернуто, настройте проект для подключения к удаленному компьютеру из Visual Studio, а затем развернуть и запустить приложение.

![Компоненты удаленной отладки](../debugger/media/remote-debugger-client-apps.png "Remote_debugger_components")

Сведения об удаленной отладке универсальных приложениях Windows (UWP), см. в разделе [отлаживать установленный пакет приложения](debug-installed-app-package.md).

## <a name="requirements"></a>Требования

Удаленный отладчик поддерживается на Windows 7 и более поздних (не телефон) и версии Windows Server, начиная с пакета обновления 2 для Windows Server 2008. Полный список требований см. в разделе [требования](../debugger/remote-debugging.md#requirements_msvsmon).

> [!NOTE]
> Отладка между двумя компьютерами, подключенными через прокси-сервер не поддерживается. Отладка в различных странах высокой задержкой или низкой пропускной способностью, таких как удаленный доступ к Интернету, или через Интернет не рекомендуется и может произойти сбой или неприемлемо медленно.
  
## <a name="download-and-install-the-remote-tools"></a>Скачивание и установка инструментов удаленной отладки

[!INCLUDE [remote-debugger-download](../debugger/includes/remote-debugger-download.md)]
  
> [!TIP]
> В некоторых сценариях может быть наиболее эффективным для запуска удаленного отладчика из общей папки. Дополнительные сведения см. в разделе [запуск удаленного отладчика из общей папки](../debugger/remote-debugging.md#fileshare_msvsmon).
  
## <a name="BKMK_setup"></a> Установка удаленного отладчика

[!INCLUDE [remote-debugger-configuration](../debugger/includes/remote-debugger-configuration.md)]

> [!NOTE]
> Если требуется добавить разрешения для дополнительных пользователей, изменение режима проверки подлинности, или номер порта удаленного отладчика, см. в разделе [Настройка удаленного отладчика](../debugger/remote-debugging.md#configure_msvsmon).

## <a name="remote_cplusplus"></a> Удаленная отладка проекта Visual C++  
 В следующей процедуре, имя и путь проекта — C:\remotetemp\MyMfc, а имя удаленного компьютера — **MJO DL**.  
  
1. Создайте приложение MFC с именем **mymfc**.  
  
2. Создайте точку останова в легкодоступном месте приложения, например в файле **MainFrm.cpp**, в начале `CMainFrame::OnCreate`.  
  
3. В обозревателе решений щелкните правой кнопкой мыши проект и выберите **свойства**. Откройте вкладку **Отладка**.  
  
4. Для параметра **Загружаемый отладчик** задайте значение **Удаленный отладчик Windows**.  
  
    ![RemoteDebuggingCPlus](../debugger/media/remotedebuggingcplus.png "RemoteDebuggingCPlus")  
  
5. Внесите в свойства следующие изменения:  
  
   |Параметр|Значение|
   |-|-|  
   |Удаленная команда|C:\remotetemp\mymfc.exe|  
   |Рабочий каталог|C:\remotetemp|  
   |Имя удаленного сервера|Список Рассылки MJO:*номер_порта*|  
   |Подключение|Удаленный доступ с аутентификацией Windows|  
   |Тип отладчика|Только машинный код|  
   |Каталог развертывания|C:\remotetemp.|  
   |Дополнительные файлы, которые необходимо развернуть|C:\data\mymfcdata.txt.|  
  
    При развертывании дополнительных файлов (необязательно), папка должна существовать на обоих компьютерах.  
  
6. В обозревателе решений щелкните решение правой кнопкой мыши и выберите **Configuration Manager**.  
  
7. Для конфигурации **Отладка** установите флажок **Развертывание**.  
  
    ![RemoteDebugCplusDeploy](../debugger/media/remotedebugcplusdeploy.png "RemoteDebugCplusDeploy")  
  
8. Начните отладку (выберите **Отладка > Начать отладку** или нажмите клавишу **F5**).  
  
9. Исполняемый файл автоматически развернется на удаленном компьютере.  
  
10. При появлении запроса введите сетевые учетные данные для подключения к удаленному компьютеру.  
  
     Необходимые учетные данные зависят от конфигурации безопасности вашей сети. Например на компьютере домена, могут выбрать сертификат безопасности или введите имя домена и пароль. На компьютере не входящих в домен, можно ввести имя компьютера и имя учетной записи пользователя, например <strong>MJO-DL\name@something.com</strong>, а также правильный пароль.  
  
11. На компьютере с Visual Studio вы должны увидеть, что выполнение остановилось в точке останова.  
  
    > [!TIP]
    >  Кроме того, файлы можно развернуть как отдельный шаг. В **обозревателе решений** щелкните правой кнопкой мыши узел **mymfc** и выберите пункт **Развернуть**.  
  
    Если приложение должно использовать файлы, не являющиеся файлами кода, их нужно включить в проект Visual Studio. Создайте папку проекта для дополнительных файлов (в **обозревателе решений** выберите **Добавить > Новая папка**). Затем добавьте файлы в папку (в **обозревателе решений** выберите **Добавить > Существующий элемент**, а затем файлы). На странице **Свойства** для каждого файла задайте для свойства **Копировать в выходной каталог** значение **Всегда копировать**.
  
## <a name="set-up-debugging-with-remote-symbols"></a>Настройка отладки с удаленными символами 

[!INCLUDE [remote-debugger-symbols](../debugger/includes/remote-debugger-symbols.md)] 
  
## <a name="see-also"></a>См. также раздел  
 [Отладка в Visual Studio](../debugger/index.md)  
 [Первое знакомство с отладчиком](../debugger/debugger-feature-tour.md)   
 [Настройка брандмауэра Windows для удаленной отладки](../debugger/configure-the-windows-firewall-for-remote-debugging.md)   
 [Remote Debugger Port Assignments](../debugger/remote-debugger-port-assignments.md)   
 [Удаленная отладка ASP.NET на удаленном компьютере IIS](../debugger/remote-debugging-aspnet-on-a-remote-iis-computer.md)  
 [Ошибки удаленной отладки и их устранение](../debugger/remote-debugging-errors-and-troubleshooting.md)