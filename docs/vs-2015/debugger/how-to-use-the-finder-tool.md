---
title: 'Практическое: использование инструмента поиска | Документация Майкрософт'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Window Finder Tool
ms.assetid: 5841926b-08c3-4e43-88bd-4223d04f9aef
caps.latest.revision: 9
author: MikeJo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 5fe233182115c8e10e78f59870d92eed69b8c492
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/16/2018
ms.locfileid: "51747083"
---
# <a name="how-to-use-the-finder-tool"></a>Практическое руководство. Использование инструмента поиска
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Можно использовать инструмент поиска в **найти окно** диалогового окна свойств или окна сообщений. Инструмент поиска можно находить отключенные дочерние окна и понять, какое окно, чтобы выделить, если отключены дочерние окна перекрываются.  
  
 ![Spy&#43; &#43; "Поиск окна" диалогового окна](../debugger/media/icon-spy-find.png "Icon_Spy ++ _Find")  
Инструмент поиска в диалоговом окне Поиск окна  
  
 На рисунке выше показано диалоговое окно "Поиск окна" после выполнения шага 3 ниже.  
  
### <a name="to-display-window-properties-or-messages"></a>Для отображения свойств или окна сообщений  
  
1.  Расположите окна таким образом, Spy ++ и окно являются видимыми.  
  
2.  Из **Spy** меню, выберите **найти окно**.  
  
     [Окно поиска](../debugger/find-window-dialog-box.md) открывает.  
  
3.  Перетащите **инструмент поиска** на конечное окно.  
  
     При перетаскивании, **найти окно** диалоговое окно отображает сведения о выбранном окне.  
  
     — или —  
  
     Если у вас есть дескриптор окна, которое необходимо исследовать (например, скопирован из отладчика), введите его в **обрабатывать** текстовое поле.  
  
    > [!TIP]
    >  Чтобы не загромождать экран, выберите **Скрыть Spy** параметр. Этот параметр позволяет скрывать главное окно Spy ++, оставляя только **найти окно** диалоговое окно поверх других приложений. Главное окно Spy ++ восстанавливается в том случае, если щелкнуть **ОК** или **отменить**, или при удалении **Скрыть Spy ++** параметр.  
  
4.  В разделе **Показать**, выберите пункт **свойства** или **сообщений**.  
  
5.  Нажмите клавишу **ОК**.  
  
     Если вы выбрали **свойства**, [диалоговое окно "Свойства окна"](../debugger/window-properties-dialog-box.md) открывает. Если вы выбрали **сообщений**, [представления сообщений](../debugger/messages-view.md) откроется окно.  
  
## <a name="see-also"></a>См. также  
 [Представления Spy ++](../debugger/spy-increment-views.md)   
 [Использование Spy ++](../debugger/using-spy-increment.md)   
 [Справочник по Spy++](../debugger/spy-increment-reference.md)



