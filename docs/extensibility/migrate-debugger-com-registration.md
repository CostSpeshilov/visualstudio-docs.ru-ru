---
title: Перенос регистрации класса 64-разрядного отладчика COM | Документация Майкрософт
ms.date: 11/10/2016
ms.topic: conceptual
ms.assetid: 45cfcee6-7a68-4d4f-b3f6-e2d8a0fa066a
author: gregg-miskelly
ms.author: greggm
manager: jillfra
ms.workload:
- greggm
ms.openlocfilehash: 91c834e61452667a0af236eddb65355f23234715
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/25/2019
ms.locfileid: "54990541"
---
# <a name="migrate-64-bit-debugger-com-class-registration"></a>Миграция на 64-разрядного отладчика регистрации классов COM

Расширения отладчика, которые регистрируют COM-классов в HKEY_CLASSES_ROOT с помощью regasm regsvr32, или непосредственно записи в реестр и загружаются в *msvsmon.exe* (удаленного отладчика), стало возможным предоставить Регистрация для msvsmon без необходимости писать на HKEY_CLASSES_ROOT. Это влияет на устаревшие вычислители выражений отладчик .NET или отладчики, которые настроены для загрузки в *msvsmon.exe* процесса.

## <a name="msvsmon-comclass-def"></a>Msvsmon-comclass-def

Чтобы использовать этот метод, добавьте  **.msvsmon-comclass-def.json* файл рядом с msvsmon (InstallDir:* \Common7\IDE\Remote Debugger\x64*).

Ниже приведен пример msvsmon comclass-def файла, который регистрирует управляемой и один собственный класс.

Имя файла: *MyCompany.MyExample.msvsmon-comclass-def.json*

```json
{
  "managedCOMClasses": [
    {
      "clsid": "{C9F48B25-36ED-4B22-8210-98BC5BE4D1E7}",
      "assemblyName": "MyCompany.MyAssembly",
      "className": "MyCompany.MyNamespace.MyClass"
    }
  ],
  "nativeCOMClasses": [
    {
      "clsid": "{42A476E9-8FA7-44D5-ADFE-216AD371EEC9}",
      "dllPath": "MyExample.dll"
    }
  ]
}
```
