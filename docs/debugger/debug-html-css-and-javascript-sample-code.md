---
title: Отладка примера кода HTML и CSS | Документация Майкрософт
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
ms.assetid: 51893967-98c8-4141-ba40-03646f221760
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 1ffb41dc978598264cfff165602c9c9a8e4cce71
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MTE95
ms.contentlocale: ru-RU
ms.lasthandoff: 01/02/2019
ms.locfileid: "53947560"
---
# <a name="debug-html-and-css-sample-code"></a>Пример кода для отладки HTML и CSS
  
 В этом разделе приведен пример файла для [краткое руководство: Отладка HTML и CSS](../debugger/quickstart-debug-html-and-css.md) Ошибки, намеренно допущенные в кратком руководстве, исправлены в этой версии кода.  
  
## <a name="sample-code"></a>Пример кода  
 Следующий код HTML используется в кратком руководстве в теге \<body>.  
  
```html  
<div id="flipTemplate" data-win-control="WinJS.Binding.Template"  
         style="display:none">  
    <div class="fixedItem" >  
        <img src="#" data-win-bind="src: flipImg" />  
    </div>  
</div>  
<div id="fView" data-win-control="WinJS.UI.FlipView" data-win-options="{  
    itemDataSource: Data.items.dataSource, itemTemplate: flipTemplate }">  
</div>  
```  
  
 В следующем коде CSS показаны добавления, сделанные в файл default.css.  
  
```css  
#fView {  
    background-color:#0094ff;  
    height: 500px;  
    margin: 25px;  
}  
```  
  
 В следующем примере кода показан выполненный код JavaScript в default.js. Ссылки на пространство имен WinJS для данного кода находятся в файле шаблона default.html.  
  
```javascript  
(function () {  
    "use strict";  
  
    var app = WinJS.Application;  
    var activation = Windows.ApplicationModel.Activation;  
  
    var myData = [];  
    for (var x = 0; x < 3; x++) {  
        myData[x] = { flipImg: "/images/logo.png" }  
    };  
  
    var pages = new WinJS.Binding.List(myData, { proxy: true });  
  
    app.onactivated = function (args) {  
        if (args.detail.kind === activation.ActivationKind.launch) {  
            if (args.detail.previousExecutionState !==  
            activation.ApplicationExecutionState.terminated) {  
                // TODO: . . .  
            } else {  
                // TODO: . . .  
            }  
            args.setPromise(WinJS.UI.processAll());  
  
            updateImages();  
        }  
    };  
  
    function updateImages() {  
  
        pages.setAt(0, { flipImg: "http://public-domain-photos.com/free-stock-photos-1/flowers/cactus-76.jpg" });  
        pages.setAt(1, { flipImg: "http://public-domain-photos.com/free-stock-photos-1/flowers/cactus-77.jpg" });  
        pages.setAt(2, { flipImg: "http://public-domain-photos.com/free-stock-photos-1/flowers/cactus-78.jpg" });  
    };  
  
    app.oncheckpoint = function (args) {  
    };  
  
    app.start();  
  
    var publicMembers = {  
        items: pages  
    };  
  
    WinJS.Namespace.define("Data", publicMembers);  
  
})();  
```  
  
## <a name="see-also"></a>См. также раздел  
 [Краткое руководство. Отладка HTML и CSS](../debugger/quickstart-debug-html-and-css.md)