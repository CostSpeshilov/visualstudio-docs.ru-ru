---
title: Задача CL | Документы Майкрософт
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- VC.Project.VCCLCompilerTool.UseUnicodeForAssemblerListing
- vc.task.cl
- VC.Project.VCCLCompilerTool.TreatSpecificWarningsAsErrors
- VC.Project.VCCLCompilerTool.CreateHotpatchableImage
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild (Visual C++), CL task
- CL task (MSBuild (Visual C++))
ms.assetid: 651ba971-b755-4f03-a549-4816beb3cc0d
caps.latest.revision: 21
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: e10c5d6ed0e4b992f5b573cd46bd1248d8d24d90
ms.sourcegitcommit: 6944ceb7193d410a2a913ecee6f40c6e87e8a54b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/05/2018
ms.locfileid: "47592820"
---
# <a name="cl-task"></a>Задача CL
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Последнюю версию этого раздела можно найти в [CL-задача](https://docs.microsoft.com/visualstudio/msbuild/cl-task).  
  
  
Использует оболочку компилятора Visual C++ — cl.exe. Компилятор создает исполняемые файлы (EXE-файлы), библиотеки динамической компоновки (DLL-файлы) или модули кода (NETMODULE-файлы). Дополнительные сведения см. в разделе [Параметры компилятора](http://msdn.microsoft.com/library/ed3376c8-bef4-4c9a-80e9-3b5da232644c).  
  
## <a name="parameters"></a>Параметры  
 В следующей таблице приводятся параметры задачи **CL**. Большинство параметров задачи и некоторые наборы параметров соответствуют параметрам командной строки.  
  
-   **AdditionalIncludeDirectories**  
  
     Необязательный параметр String[].  
  
     Добавляет каталог к списку каталогов, в которых выполняется поиск включаемых файлов.  
  
     Дополнительные сведения см. в разделе [/I (дополнительные каталоги включения)](http://msdn.microsoft.com/library/3e9add2a-5ed8-4d15-ad79-5b411e313a49).  
  
-   **AdditionalOptions**  
  
     Необязательный параметр String.  
  
     Список параметров командной строки. Например, "/*параметр_1* /*параметр_2* /*параметр_#*". Этот параметр используется для указания параметров командной строки, не представленных каким-либо другим параметром задачи.  
  
     Дополнительные сведения см. в разделе [Параметры компилятора](http://msdn.microsoft.com/library/ed3376c8-bef4-4c9a-80e9-3b5da232644c).  
  
-   **AdditionalUsingDirectories**Необязательный параметр String[].  
  
     Указывает каталог, в котором компилятор будет производить поиск для разрешения ссылок, переданных в директиву **#using**.  
  
     Дополнительные сведения см. в разделе [/AI (указание каталогов метаданных)](http://msdn.microsoft.com/library/fb9c1846-504c-4a3b-bb39-c8696de32f6f).  
  
-   **AlwaysAppend**  
  
     Необязательный параметр String.  
  
     Строка, которая всегда выводится в командной строке. Значение по умолчанию — "**/c**".  
  
-   **AssemblerListingLocation**  
  
     Создает файл листинга, содержащий код сборки.  
  
     Дополнительные сведения см. в описании параметра **/Fa** в разделе [/FA, /Fa (файл листинга)](http://msdn.microsoft.com/library/c7507d0e-c69d-44f9-b8e2-d2c398697402).  
  
-   **AssemblerOutput**  
  
     Необязательный параметр String.  
  
     Создает файл листинга, содержащий код сборки.  
  
     Укажите одно из следующих значений, каждое из которых соответствует параметру командной строки.  
  
    -   **NoListing** - *\<отсутствует>*  
  
    -   **AssemblyCode** - **/FA**  
  
    -   **AssemblyAndMachineCode** - **/FAc**  
  
    -   **AssemblyAndSourceCode** - **/FAs**  
  
    -   **All** - **/FAcs**  
  
     Дополнительные сведения см. в описании параметров **/FA**, **/FAc**, **/FAs** и **/FAcs** в разделе [/FA, /Fa (файл листинга)](http://msdn.microsoft.com/library/c7507d0e-c69d-44f9-b8e2-d2c398697402).  
  
-   **BasicRuntimeChecks**  
  
     Необязательный параметр String.  
  
     Включает и отключает функцию проверки ошибок во время выполнения совместно с атрибутом директивы pragma [runtime_checks](http://msdn.microsoft.com/library/ae50b43f-f88d-47ad-a2db-3389e9e7df5b).  
  
     Укажите одно из следующих значений, каждое из которых соответствует параметру командной строки.  
  
    -   **Default** -                          *\<отсутствует>*  
  
    -   **StackFrameRuntimeCheck** - **/RTCs**  
  
    -   **UninitializedLocalUsageCheck** - **/RTCu**  
  
    -   **EnableFastChecks** -                          **/RTC1**  
  
     Дополнительные сведения см. в разделе [/RTC (проверки ошибок во время выполнения)](http://msdn.microsoft.com/library/9702c558-412c-4004-acd5-80761f589368).  
  
-   **BrowseInformation**  
  
     Необязательный логический параметр.  
  
     Если он имеет значение `true`, создается файл информации об исходном коде.  
  
     Дополнительные сведения см. в описании параметра **/FR** в разделе [/FR, /Fr (создать SBR-файл)](http://msdn.microsoft.com/library/3fd8f88b-3924-4feb-9393-287036a28896).  
  
-   **BrowseInformationFile**  
  
     Необязательный параметр String.  
  
     Задает имя для файла информации об исходном коде.  
  
     Дополнительные сведения см. в описании параметра **BrowseInformation** в этой таблице, а также в разделе [/FR, /Fr (создать SBR-файл)](http://msdn.microsoft.com/library/3fd8f88b-3924-4feb-9393-287036a28896).  
  
-   **BufferSecurityCheck**  
  
     Необязательный логический параметр.  
  
     Если значение равно `true`, обнаруживаются некоторые переполнения буфера, при которых перезаписывается обратный адрес. Это стандартный способ работы с кодом, в котором не используется принудительное ограничение размера буфера.  
  
     Дополнительные сведения см. в разделе [Параметр /GS (проверка безопасности буфера)](http://msdn.microsoft.com/library/8d8a5ea1-cd5e-42e1-bc36-66e1cd7e731e).  
  
-   **BuildingInIDE**  
  
     Необязательный логический параметр.  
  
     Если он имеет значение `true`, то указывает, что **MSBuild** вызывается средой IDE. В противном случае **MSBuild** вызывается в командной строке.  
  
-   **CallingConvention**  
  
     Необязательный параметр String.  
  
     Задает соглашение о вызове, определяющее порядок, в котором аргументы функции передаются в стек, то, удаляет ли вызывающая или вызываемая функция аргументы из стека в конце вызова, а также соглашение о декорировании имен, используемое компилятором для идентификации отдельных функций.  
  
     Укажите одно из следующих значений, каждое из которых соответствует параметру командной строки.  
  
    -   **Cdecl** - **/Gd**  
  
    -   **FastCall** -                          **/Gr**  
  
    -   **StdCall** -                          **/Gz**  
  
     Дополнительные сведения см. в разделе [/Gd, /Gr, /Gv, /Gz (соглашение о вызовах)](http://msdn.microsoft.com/library/fd3110cb-2d77-49f2-99cf-a03f9ead00a3).  
  
-   **CompileAs**  
  
     Необязательный параметр String.  
  
     Указывает, должен ли входной файл компилироваться как исходный файл C или C++.  
  
     Укажите одно из следующих значений, каждое из которых соответствует параметру командной строки.  
  
    -   **Default** - *\<отсутствует>*  
  
    -   **CompileAsC** - **/TC**  
  
    -   **CompileAsCpp** - **/TP**  
  
     Дополнительные сведения см. в разделе [Параметры /Tc, /Tp, /TC, /TP (определение типа исходного файла)](http://msdn.microsoft.com/library/7d9d0a65-338b-427c-8b48-fff30e2f9d2b).  
  
-   **CompileAsManaged**  
  
     Необязательный параметр String.  
  
     Позволяет приложениям и компонентам использовать возможности из среды CLR.  
  
     Укажите одно из следующих значений, каждое из которых соответствует параметру командной строки.  
  
    -   **false** - *\<отсутствует>*  
  
    -   **true** - **/clr**  
  
    -   **Pure** - **/clr:pure**  
  
    -   **Safe** - **/clr:safe**  
  
    -   **OldSyntax** - **/clr:oldSyntax**  
  
     Дополнительные сведения см. в разделе [/clr (компиляция CLR)](http://msdn.microsoft.com/library/fec5a8c0-40ec-484c-a213-8dec918c1d6c).  
  
-   **CreateHotpatchableImage**  
  
     Необязательный логический параметр.  
  
     Если он имеет значение `true`, то компилятор должен подготовить образ для *критического обновления*. Этот параметр позволяет добиться того, что длина первой инструкции каждой функции равна двум байтам, что необходимо для выполнения критического обновления.  
  
     Дополнительные сведения см. в разделе [/hotpatch (создать образ с обновлениями)](http://msdn.microsoft.com/library/aad539b6-c053-4c78-8682-853d98327798).  
  
-   **DebugInformationFormat**  
  
     Необязательный параметр String.  
  
     Выбирает тип отладочной информации, создаваемой для программы, и место хранения этой информации: объектные файлы (OBJ) или база данных программы (PDB).  
  
     Укажите одно из следующих значений, каждое из которых соответствует параметру командной строки.  
  
    -   **OldStyle** - **/Z7**  
  
    -   **ProgramDatabase** - **/Zi**  
  
    -   **EditAndContinue** - **/ZI**  
  
     Дополнительные сведения см. в разделе [/Z7, /Zi, /ZI (формат отладочной информации)](http://msdn.microsoft.com/library/ce9fa7e1-0c9b-47e3-98ea-26d1a16257c8).  
  
-   **DisableLanguageExtensions**  
  
     Необязательный логический параметр.  
  
     Если он имеет значение **true**, то компилятор должен выдавать ошибку для языковых конструкций, несовместимых либо с ANSI C, либо с ANSI C++.  
  
     Дополнительные сведения см. в описании параметра **/Za** в разделе [/Za, /Ze (отключить расширения языка)](http://msdn.microsoft.com/library/65e49258-7161-4289-a176-7c5c0656b1a2).  
  
-   **DisableSpecificWarnings**  
  
     Необязательный параметр String[].  
  
     Отключает номера предупреждений, которые указаны в списке, разделенном точками с запятой.  
  
     Дополнительные сведения см. в описании параметра `/wd` в разделе [/w, /W0, /W1, /W2, /W3, /W4, /w1, /w2, /w3, /w4, /Wall, /wd, /we, /wo, /Wv, /WX (уровень предупреждений)](http://msdn.microsoft.com/library/d6bc7bf5-c754-4879-909c-8e3a67e2629f).  
  
-   **EnableEnhancedInstructionSet**  
  
     Необязательный параметр String.  
  
     Этот параметр задает архитектуру для создания кода с помощью наборов инструкций Streaming SIMD Extensions (SSE) и Streaming SIMD Extensions 2 (SSE2).  
  
     Укажите одно из следующих значений, каждое из которых соответствует параметру командной строки.  
  
    -   **StreamingSIMDExtensions** - **/arch:SSE**  
  
    -   **StreamingSIMDExtensions2** - **/arch:SSE2**  
  
     Дополнительные сведения см. в разделе [/arch (x86)](http://msdn.microsoft.com/library/9dd5a75d-06e4-4674-aade-33228486078d).  
  
-   **EnableFiberSafeOptimizations**  
  
     Необязательный логический параметр.  
  
     Если он имеет значение `true`, то поддерживается безопасность волокон для данных, выделенных с помощью статической локальной памяти потока, то есть данных, выделенных с помощью `__declspec(thread)`.  
  
     Дополнительные сведения см. в разделе [/GT (поддержка локальной памяти потока, безопасной относительно волокон)](http://msdn.microsoft.com/library/071fec79-c701-432b-9970-457344133159).  
  
-   **EnablePREfast**  
  
     Необязательный логический параметр.  
  
     Если он имеет значение `true`, то включается анализ кода.  
  
     Дополнительные сведения см. в разделе [/analyze (анализ кода)](http://msdn.microsoft.com/library/81da536a-e030-4bd4-be18-383927597d08).  
  
-   **ErrorReporting**  
  
     Необязательный параметр String.  
  
     Разрешает передавать данные о внутренних ошибках компилятора (ICE) непосредственно в корпорацию Майкрософт. По умолчанию в сборках среды IDE этот параметр имеет значение **Prompt**, а в сборках командной строки — значение **Queue**.  
  
     Укажите одно из следующих значений, каждое из которых соответствует параметру командной строки.  
  
    -   **None** - **/errorReport:none**  
  
    -   **Prompt** - **/errorReport:prompt**  
  
    -   **Queue** - **/errorReport:queue**  
  
    -   **Send** - **/errorReport:send**  
  
     Дополнительные сведения см. в разделе [Параметр /errorReport (отчет о внутренних ошибках компилятора)](http://msdn.microsoft.com/library/819828f8-b0a5-412c-9c57-bf822f17e667).  
  
-   **ExceptionHandling**  
  
     Необязательный параметр String.  
  
     Задает модель обработки исключений, используемую компилятором.  
  
     Укажите одно из следующих значений, каждое из которых соответствует параметру командной строки.  
  
    -   **false** - *\<отсутствует>*  
  
    -   **Async** - **/EHa**  
  
    -   **Sync** - **/EHsc**  
  
    -   **SyncCThrow** - **/EHs**  
  
     Дополнительные сведения см. в статье [/EH (модель обработки исключений)](http://msdn.microsoft.com/library/754b916f-d206-4472-b55a-b6f1b0f2cb4d).  
  
-   **ExpandAttributedSource**  
  
     Необязательный логический параметр.  
  
     Если он имеет значение `true`, то создается файл списка, имеющий расширенные атрибуты, внедренные в исходный файл.  
  
     Дополнительные сведения см. в разделе [/Fx (слияние подставляемого кода)](http://msdn.microsoft.com/library/14f0e301-3bab-45a3-bbdf-e7ce66f20560) .  
  
-   **FavorSizeOrSpeed**  
  
     Необязательный параметр String.  
  
     Указывает, нужно ли предпочитать скорость или размер кода.  
  
     Укажите одно из следующих значений, каждое из которых соответствует параметру командной строки.  
  
    -   **Neither** - *\<отсутствует>*  
  
    -   **Size** - **/Os**  
  
    -   **Speed** - **/Ot**  
  
     Дополнительные сведения см. в разделе [/Os, /Ot (приоритет размера кода или скорости кода)](http://msdn.microsoft.com/library/9a340806-fa15-4308-892c-355d83cac0f2).  
  
-   **FloatingPointExceptions**  
  
     Необязательный логический параметр.  
  
     Если он имеет значение `true`, то включается надежная модель исключения с плавающей запятой. Исключения вызываются сразу же после их инициализации.  
  
     Дополнительные сведения см. в описании параметра /**fp:except** в разделе [/fp (Определение поведения с плавающей запятой)](http://msdn.microsoft.com/library/10469d6b-e68b-4268-8075-d073f4f5d57e).  
  
-   **FloatingPointModel**  
  
     Необязательный параметр String.  
  
     Задает модель с плавающей запятой.  
  
     Укажите одно из следующих значений, каждое из которых соответствует параметру командной строки.  
  
    -   **Precise** - **/fp:precise**  
  
    -   **Strict** - **/fp:strict**  
  
    -   **Fast** - **/fp:fast**  
  
     Дополнительные сведения см. в разделе [/fp (определение поведения с плавающей запятой)](http://msdn.microsoft.com/library/10469d6b-e68b-4268-8075-d073f4f5d57e).  
  
-   **ForceConformanceInForLoopScope**  
  
     Необязательный логический параметр.  
  
     Если он имеет значение `true`, то реализуется стандартное поведение C++ в для циклов [for](http://msdn.microsoft.com/library/6c7d01b3-c4c1-4c6a-aa58-e2d198f33d4a), использующих расширения Майкрософт ([/Ze](http://msdn.microsoft.com/library/65e49258-7161-4289-a176-7c5c0656b1a2)).  
  
     Дополнительные сведения см. в разделе [/Zc:forScope (принудительное обеспечение соответствия в области видимости оператора for)](http://msdn.microsoft.com/library/3031f02d-3b14-4ad0-869e-22b0110c3aed).  
  
-   **ForcedIncludeFiles**  
  
     Необязательный параметр `String[]` .  
  
     Вызывает обработку препроцессором одного или нескольких указанных файлов заголовков.  
  
     Дополнительные сведения см. в разделе [/FI (имя принудительно включаемого файла)](http://msdn.microsoft.com/library/07e79577-8152-4df9-a64c-aae08c603397).  
  
-   **ForcedUsingFiles**  
  
     Необязательный параметр типа **String[]**.  
  
     Вызывает обработку препроцессором одного или нескольких указанных файлов **#using**.  
  
     Дополнительные сведения см. в разделе [/FU (именование файла с принудительно используемым атрибутом #using)](http://msdn.microsoft.com/library/698f8603-457f-435a-baff-5ac9243d6ca1).  
  
-   **FunctionLevelLinking**  
  
     Необязательный параметр `Boolean` .  
  
     Если значение равно `true`, компилятор может упаковывать отдельные функции в форме упакованных функций (COMDAT).  
  
     Дополнительные сведения см. в разделе [/Gy (включение компоновки на уровне функций)](http://msdn.microsoft.com/library/0d3cf14c-ed7d-4ad3-b4b6-104e56f61046).  
  
-   **GenerateXMLDocumentationFiles**  
  
     Необязательный параметр `Boolean` .  
  
     Если значение равно `true`, компилятор обрабатывает комментарии к документации в файлах исходного кода и создает XDC-файл для каждого файла с исходным кодом, в котором есть комментарии к документации.  
  
     Дополнительные сведения см. в разделе [/doc (обработка комментариев документации) (C/C++)](http://msdn.microsoft.com/library/b54f7e2c-f28f-4f46-9ed6-0db09be2cc63). См. также описание параметра **XMLDocumentationFileName** в этой таблице.  
  
-   **IgnoreStandardIncludePath**  
  
     Необязательный параметр `Boolean` .  
  
     Если значение равно `true`, компилятор не выполняет поиск файлов для включения в каталогах, указанных в переменных среды PATH и INCLUDE.  
  
     Дополнительные сведения см. в разделе [/X (отклонение стандартных путей включения)](http://msdn.microsoft.com/library/16bdf2cc-c8dc-46e4-bdcc-f3caeba5e1ef).  
  
-   **InlineFunctionExpansion**  
  
     Необязательный параметр типа **String**.  
  
     Задает уровень расширения встраиваемых функций для сборки.  
  
     Укажите одно из следующих значений, каждое из которых соответствует параметру командной строки.  
  
    -   **Default** - *\<отсутствует>*  
  
    -   **Disabled** - **/Ob0**  
  
    -   **OnlyExplicitInline** - **/Ob1**  
  
    -   **AnySuitable** - **/Ob2**  
  
     Дополнительные сведения см. в разделе [Параметр /Ob (расширение встраиваемых функций)](http://msdn.microsoft.com/library/f134e6df-e939-4980-a01d-47425dbc562a).  
  
-   **IntrinsicFunctions**  
  
     Необязательный параметр `Boolean` .  
  
     Если значение равно `true`, вызов некоторых функций заменяется на встроенные или какие-либо другие формы функции, которые способствуют более быстрому выполнению приложения.  
  
     Дополнительные сведения см. в разделе [/Oi (создание встроенных функций)](http://msdn.microsoft.com/library/fa4a3bf6-0ed8-481b-91c0-add7636132b4).  
  
-   **MinimalRebuild**  
  
     Необязательный параметр `Boolean` .  
  
     Если значение равно `true`, включается минимальное перестроение, определяющее, необходимо ли перекомпилировать исходные файлы C++, содержащие измененные определения классов C++ (хранящиеся в файлах заголовка (H)).  
  
     Дополнительные сведения см. в разделе [/Gm (включение минимального перепостроения)](http://msdn.microsoft.com/library/d8869ce0-d2ea-40eb-8dae-6d2cdb61dd59).  
  
-   **MultiProcessorCompilation**  
  
     Необязательный параметр `Boolean` .  
  
     Если он имеет значение `true`, то для компиляции используется несколько процессоров. Этот параметр создает процесс для каждого эффективного процессора на компьютере.  
  
     Дополнительные сведения см. в разделе [/MP (построить с несколькими процессами)](http://msdn.microsoft.com/library/a932b14a-74fe-4b45-84e4-6bf53f0f5e07). См. также описание параметра **ProcessorNumber** в этой таблице.  
  
-   **ObjectFileName**  
  
     Необязательный параметр типа **String**.  
  
     Указывает имя файла или каталога объектного файла (OBJ), которое следует использовать вместо имени по умолчанию.  
  
     Дополнительные сведения см. в разделе [/Fo (имя объектного файла)](http://msdn.microsoft.com/library/0e6d593e-4e7f-4990-9e6e-92e1dcbcf6e6).  
  
-   **ObjectFiles**  
  
     Необязательный параметр типа **String[]**.  
  
     Список объектных файлов.  
  
-   **OmitDefaultLibName**  
  
     Необязательный параметр `Boolean` .  
  
     Если он имеет значение `true`, то имя библиотеки времени выполнения С, установленное по умолчанию, опускается в объектном файле (OBJ-файле). По умолчанию компилятор помещает имя библиотеки в OBJ-файл, чтобы перенаправить компоновщик в правильную библиотеку.  
  
     Дополнительные сведения см. в разделе [/Zl (опущенное по умолчанию имя библиотеки)](http://msdn.microsoft.com/library/b27d39d0-44d6-498c-84ae-27c1326fee59).  
  
-   **OmitFramePointers**  
  
     Необязательный параметр `Boolean` .  
  
     Если значение равно `true`, подавляется создание указателей фрейма в стеке вызова.  
  
     Дополнительные сведения см. в разделе [/Oy (подавление указателей фрейма)](http://msdn.microsoft.com/library/c451da86-5297-4c5a-92bc-561d41379853).  
  
-   **OpenMPSupport**  
  
     Необязательный параметр `Boolean` .  
  
     Если он имеет значение `true`, то компилятор будет обрабатывать предложения и директивы OpenMP.  
  
     Дополнительные сведения см. в разделе [/openmp (включение поддержки OpenMP 2.0)](http://msdn.microsoft.com/library/9082b175-18d3-4378-86a7-c0eb95664e13).  
  
-   **Optimization**  
  
     Необязательный параметр типа **String**.  
  
     Задает различные оптимизации скорости и размера кода.  
  
     Укажите одно из следующих значений, каждое из которых соответствует параметру командной строки.  
  
    -   **Disabled** - **/Od**  
  
    -   **MinSpace** - **/O1**  
  
    -   **MaxSpeed** - **/O2**  
  
    -   **Full** - **/Ox**  
  
     Дополнительные сведения см. в разделе [Параметры /O (оптимизация кода)](http://msdn.microsoft.com/library/77997af9-5555-4b3d-aa57-6615b27d4d5d).  
  
-   **PrecompiledHeader**  
  
     Необязательный параметр типа **String**.  
  
     Создание или использование файла предкомпилированного заголовка (PCH-файла) во время сборки.  
  
     Укажите одно из следующих значений, каждое из которых соответствует параметру командной строки.  
  
    -   **NotUsing** - *\<отсутствует>*  
  
    -   **Create** - **/Yc**  
  
    -   **Use** - **/Yu**  
  
     Дополнительные сведения см. в разделах [/Yc (создать предкомпилированный заголовочный файл)](http://msdn.microsoft.com/library/47c2e555-b4f5-46e6-906e-ab5cf21f0678) и [/Yu (использование файла предкомпилированного заголовка)](http://msdn.microsoft.com/library/24f1bd0e-b624-4296-a17e-d4b53e374e1f). Кроме того, см. параметры **PrecompiledHeaderFile** и **PrecompiledHeaderOutputFile** в этой таблице.  
  
-   **PrecompiledHeaderFile**  
  
     Необязательный параметр типа **String**.  
  
     Задает имя файла предкомпилированного заголовка для создания или использования.  
  
     Дополнительные сведения см. в разделах [/Yc (создать предкомпилированный заголовочный файл)](http://msdn.microsoft.com/library/47c2e555-b4f5-46e6-906e-ab5cf21f0678) и [/Yu (использование файла предкомпилированного заголовка)](http://msdn.microsoft.com/library/24f1bd0e-b624-4296-a17e-d4b53e374e1f).  
  
-   **PrecompiledHeaderOutputFile**  
  
     Необязательный параметр типа **String**.  
  
     Задает путь для предкомпилированного заголовка, который используется вместо пути по умолчанию.  
  
     Дополнительные сведения см. в разделе [/Fp (имя PCH-файла)](http://msdn.microsoft.com/library/0fcd9cbd-e09f-44d3-9715-b41efb5d0be2).  
  
-   **PreprocessKeepComments**  
  
     Необязательный параметр `Boolean` .  
  
     Если значение равно `true`, в ходе предварительной обработки комментарии сохраняются.  
  
     Дополнительные сведения см. в разделе [/C (сохранять комментарии во время предварительной обработки)](http://msdn.microsoft.com/library/944567ca-16bc-4728-befe-d414a7787f26).  
  
-   **PreprocessorDefinitions**  
  
     Необязательный параметр `String[]` .  
  
     Определяет символ предобработки для исходного файла.  
  
     Для получения дополнительной информации см. раздел [Определения препроцессора (/D)](http://msdn.microsoft.com/library/b53fdda7-8da1-474f-8811-ba7cdcc66dba).  
  
-   **PreprocessOutput**  
  
     Необязательный параметр `ITaskItem[]` .  
  
     Определяет массив выходных элементов препроцессора, которые могут использоваться и создаваться задачами.  
  
-   **PreprocessOutputPath**  
  
     Необязательный параметр `String` .  
  
     Задает имя выходного файла, в который параметр **PreprocessToFile** записывает предварительно обработанные выходные данные.  
  
     Дополнительные сведения см. в разделе [/Fi (предварительная обработка имени выходного файла)](http://msdn.microsoft.com/library/6d0ba983-a8b7-41ec-84f5-b4688ef8efee).  
  
-   **PreprocessSuppressLineNumbers**  
  
     Необязательный параметр `Boolean` .  
  
     Если значение равно `true`, выполняется предобработка исходных файлов C и C++, которые копируются на стандартное устройство вывода.  
  
     Дополнительные сведения см. в разделе [/EP (предварительная обработка в поток стандартных выходных файлов без директив #line)](http://msdn.microsoft.com/library/6ec411ae-e33d-4ef5-956e-0054635eabea).  
  
-   **PreprocessToFile**  
  
     Необязательный параметр `Boolean` .  
  
     Если значение равно `true`, выполняется предобработка файлов на языке C и С++, а выходные данные записываются в файл.  
  
     Дополнительные сведения см. в разделе [/P (вывод результатов предварительной обработки в файл)](http://msdn.microsoft.com/library/123ee54f-8219-4a6f-9876-4227023d83fc).  
  
-   **ProcessorNumber**  
  
     Необязательный параметр `Integer` .  
  
     Задает максимальное число процессоров, которые могут использоваться в многопроцессорной компиляции. Используйте этот параметр вместе с параметром **MultiProcessorCompilation**.  
  
-   **ProgramDataBaseFileName**  
  
     Необязательный параметр `String` .  
  
     Задает имя файла для базы данных программы (PDB-файла).  
  
     Дополнительные сведения см. в разделе [/Fd (имя файла базы данных программы)](http://msdn.microsoft.com/library/3977a9ed-f0ac-45df-bf06-01cedd2ba85a).  
  
-   **RuntimeLibrary**  
  
     Необязательный параметр `String` .  
  
     Указывает, является ли многопотоковый модуль библиотекой DLL, и выбирает версию библиотеки времени выполнения для отладки или выпуска.  
  
     Укажите одно из следующих значений, каждое из которых соответствует параметру командной строки.  
  
    -   **MultiThreaded** - **/MT**  
  
    -   **MultiThreadedDebug** - **/MTd**  
  
    -   **MultiThreadedDLL** - **/MD**  
  
    -   **MultiThreadedDebugDLL** - **/MDd**  
  
     Дополнительные сведения см. в разделе [/MD, /MT, /LD (использование библиотеки времени выполнения)](http://msdn.microsoft.com/library/cf7ed652-dc3a-49b3-aab9-ad60e5395579).  
  
-   **RuntimeTypeInfo**  
  
     Необязательный параметр `Boolean` .  
  
     Если он имеет значение `true`, то добавляется код для проверки типов объектов C++ во время выполнения (сведения о типе времени выполнения).  
  
     Дополнительные сведения см. в разделе [/GR (предоставление информации о типах во время выполнения)](http://msdn.microsoft.com/library/d1f9f850-dcec-49fd-96ef-e72d01148906).  
  
-   **ShowIncludes**  
  
     Необязательный параметр `Boolean` .  
  
     Если значение равно `true`, компилятор выводит список включаемых файлов.  
  
     Дополнительные сведения см. в разделе [/showIncludes (список включаемых файлов)](http://msdn.microsoft.com/library/0b74b052-f594-45a6-a7c7-09e1a319547d).  
  
-   **SmallerTypeCheck**  
  
     Необязательный параметр `Boolean` .  
  
     Если он имеет значение `true`, то выводится сообщение об ошибке времени выполнения, когда значение назначается типу данных меньшего размера, что приводит к потере данных.  
  
     Дополнительные сведения см. в описании параметра **/RTCc** в разделе [/RTC (проверки ошибок во время выполнения)](http://msdn.microsoft.com/library/9702c558-412c-4004-acd5-80761f589368).  
  
-   **Sources**  
  
     Обязательный параметр `ITaskItem[]` .  
  
     Задает список исходных файлов, разделенных пробелами.  
  
-   **StringPooling**  
  
     Необязательный параметр `Boolean` .  
  
     Если он имеет значение `true`, то компилятору позволено создавать одну копию одинаковых строк в образе программы.  
  
     Дополнительные сведения см. в разделе [/GF (исключение повторяющихся строк)](http://msdn.microsoft.com/library/bb7b5d1c-8e1f-453b-9298-8fcebf37d16c).  
  
-   **StructMemberAlignment**  
  
     Необязательный параметр `String` .  
  
     Задает байтовое выравнивание для всех элементов в структуре.  
  
     Укажите одно из следующих значений, каждое из которых соответствует параметру командной строки.  
  
    -   **Default** - **/Zp1**  
  
    -   **1Byte** - **/Zp1**  
  
    -   **2Bytes** - **/Zp2**  
  
    -   **4Bytes** - **/Zp4**  
  
    -   **8Bytes** - **/Zp8**  
  
    -   **16Bytes** - **/Zp16**  
  
     Дополнительные сведения см. в статье [/Zp (выравнивание членов структур)](http://msdn.microsoft.com/library/5242f656-ed9b-48a3-bc73-cfcf3ed2520f).  
  
-   **SuppressStartupBanner**  
  
     Необязательный параметр `Boolean` .  
  
     Если задано значение `true`, запрещается отображение сообщения о номере версии и авторских правах при запуске задачи.  
  
     Дополнительные сведения см. в разделе [/nologo (отмена вывода начального заголовка) (C/C++)](http://msdn.microsoft.com/library/75930d8b-b11c-4db8-99e5-b52f97da0693).  
  
-   **TrackerLogDirectory**  
  
     Необязательный параметр `String` .  
  
     Задает промежуточный каталог, в котором хранятся журналы отслеживания для этой задачи.  
  
     Дополнительные сведения см. в описании параметров **TLogReadFiles** и **TLogWriteFiles** в этой таблице.  
  
-   **TreatSpecificWarningsAsErrors**  
  
     Необязательный параметр типа **String[]**.  
  
     Обрабатывает указанный список предупреждений компилятора как ошибки.  
  
     Дополнительные сведения см. в описании параметра **/we**`n` в разделе [/w, /W0, /W1, /W2, /W3, /W4, /w1, /w2, /w3, /w4, /Wall, /wd, /we, /wo, /Wv, /WX (уровень предупреждений)](http://msdn.microsoft.com/library/d6bc7bf5-c754-4879-909c-8e3a67e2629f).  
  
-   **TreatWarningAsError**  
  
     Необязательный параметр `Boolean` .  
  
     Если значение равно `true`, все предупреждения компилятора обрабатываются как ошибки.  
  
     Дополнительные сведения см. в описании параметра **/WX** в разделе [/w, /W0, /W1, /W2, /W3, /W4, /w1, /w2, /w3, /w4, /Wall, /wd, /we, /wo, /Wv, /WX (уровень предупреждений)](http://msdn.microsoft.com/library/d6bc7bf5-c754-4879-909c-8e3a67e2629f).  
  
-   **TreatWChar_tAsBuiltInType**  
  
     Необязательный параметр `Boolean` .  
  
     Если он имеет значение `true`, то тип `wchar_t` трактуется как собственный тип.  
  
     Дополнительные сведения см. в разделе [/Zc:wchar_t (wchar_t — это собственный тип)](http://msdn.microsoft.com/library/b0de5a84-da72-4e5a-9a4e-541099f939e0).  
  
-   **UndefineAllPreprocessorDefinitions**  
  
     Необязательный параметр `Boolean` .  
  
     Если значение равно `true`, отменяется определение символов для систем Майкрософт, определяемых компилятором.  
  
     Дополнительные сведения см. в описании параметра **/u** в разделе [Параметры /U и /u (отмена определения символа)](http://msdn.microsoft.com/library/7bc0474f-6d1f-419b-807d-0d8816763b2a).  
  
-   **UndefinePreprocessorDefinitions**  
  
     Необязательный параметр `String[]` .  
  
     Задает список одного или нескольких символов препроцессора для отмены определения.  
  
     Дополнительные сведения см. в описании параметра **/U** в разделе [Параметры /U и /u (отмена определения символа)](http://msdn.microsoft.com/library/7bc0474f-6d1f-419b-807d-0d8816763b2a).  
  
-   **UseFullPaths**  
  
     Необязательный параметр `Boolean` .  
  
     Если значение равно `true`, отображается полный путь к файлам исходного кода, переданный компилятору в диагностике.  
  
     Дополнительные сведения см. в разделе [/FC (полный путь к файлу исходного кода в папке Diagnostics)](http://msdn.microsoft.com/library/1f11414e-cb42-421b-be68-9d369aab036b).  
  
-   **UseUnicodeForAssemblerListing**  
  
     Необязательный параметр `Boolean` .  
  
     Если он имеет значение `true`, то выходной файл будет создан в формате UTF-8.  
  
     Дополнительные сведения см. в описании параметра **/FAu** в разделе [/FA, /Fa (файл листинга)](http://msdn.microsoft.com/library/c7507d0e-c69d-44f9-b8e2-d2c398697402).  
  
-   **WarningLevel**  
  
     Необязательный параметр `String` .  
  
     Задает высший уровень предупреждений, создаваемых компилятором.  
  
     Укажите одно из следующих значений, каждое из которых соответствует параметру командной строки.  
  
    -   **TurnOffAllWarnings** - **/W0**  
  
    -   **Level1** - **/W1**  
  
    -   **Level2** - **/W2**  
  
    -   **Level3** - **/W3**  
  
    -   **Level4** - **/W4**  
  
    -   **EnableAllWarnings** - **/Wall**  
  
     Дополнительные сведения см. в описании параметра **/W**_n_ в разделе [/w, /W0, /W1, /W2, /W3, /W4, /w1, /w2, /w3, /w4, /Wall, /wd, /we, /wo, /Wv, /WX (уровень предупреждений)](http://msdn.microsoft.com/library/d6bc7bf5-c754-4879-909c-8e3a67e2629f).  
  
-   **WholeProgramOptimization**  
  
     Необязательный параметр `Boolean` .  
  
     Если значение равно `true`, включается оптимизация всей программы.  
  
     Дополнительные сведения см. в разделе [/GL (оптимизация всей программы)](http://msdn.microsoft.com/library/09d51e2d-9728-4bd0-b5dc-3b8284aca1d1).  
  
-   **XMLDocumentationFileName**  
  
     Необязательный параметр `String` .  
  
     Задает имя создаваемых XML-файлов документации. Этот параметр может быть именем файла или каталога.  
  
     Дополнительные сведения см. описание аргумента `name` в разделе [/doc (обработка комментариев документации) (C/C++)](http://msdn.microsoft.com/library/b54f7e2c-f28f-4f46-9ed6-0db09be2cc63). См. также описание параметра **GenerateXMLDocumentationFiles** в этой таблице.  
  
-   **MinimalRebuildFromTracking**  
  
     Необязательный параметр `Boolean` .  
  
     Если он имеет значение `true`, то выполняется отслеживаемая инкрементная сборка; если значение `false`, то выполняется перестроение.  
  
-   **TLogReadFiles**  
  
     Необязательный параметр `ITaskItem[]` .  
  
     Определяет массив элементов, представляющих *журналы отслеживания чтения из файла*.  
  
     Журнал отслеживания чтения из файла (TLOG) содержит имена входных файлов, прочитанных задачей, и используется в системе сборки проекта для поддержки инкрементных сборок. Дополнительные сведения см. в описании параметров **TrackerLogDirectory** и **TrackFileAccess** в этой таблице.  
  
-   **TLogWriteFiles**  
  
     Необязательный параметр `ITaskItem[]` .  
  
     Определяет массив элементов, представляющих *журналы отслеживания записи в файл*.  
  
     Журнал отслеживания записи в файл (TLOG) содержит имена выходных файлов, записанных задачей, и используется в системе сборки проекта для поддержки инкрементных сборок. Дополнительные сведения см. в описании параметров **TrackerLogDirectory** и **TrackFileAccess** в этой таблице.  
  
-   **TrackFileAccess**  
  
     Необязательный параметр `Boolean` .  
  
     Если он имеет значение `true`, то выполняется отслеживание шаблонов доступа к файлу.  
  
     Дополнительные сведения см. в описании параметров **TLogReadFiles** и **TLogWriteFiles** в этой таблице.  
  
## <a name="remarks"></a>Примечания  
  
## <a name="see-also"></a>См. также  
 [Справочные сведения о задачах](../msbuild/msbuild-task-reference.md)


