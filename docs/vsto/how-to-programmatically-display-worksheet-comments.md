---
title: Как выполнить Программное отображение примечаний на листе
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- worksheets, comments
- comments, worksheets
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: aafd07e3f25e51388cfccc06260d7f96df0a7ad0
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/24/2019
ms.locfileid: "54868486"
---
# <a name="how-to-programmatically-display-worksheet-comments"></a>Как выполнить Программное отображение примечаний на листе
  Вы можете отображать и скрывать комментарии в листах Microsoft Office Excel программными средствами.  
  
 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]  
  
## <a name="to-display-all-comments-on-a-worksheet-in-a-document-level-customization"></a>Отображение всех комментариев на листе в настройке уровня документа  
  
1.  Присвойте свойству <xref:Microsoft.Office.Interop.Excel.Comment.Visible%2A> значение **true** , если нужно отображать комментарии; в противном случае присвойте ему значение **false**. Этот код следует разместить в классе листа, а не в классе `ThisWorkbook` .  
  
     [!code-csharp[Trin_VstcoreExcelAutomation#31](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#31)]
     [!code-vb[Trin_VstcoreExcelAutomation#31](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#31)]  
  
## <a name="to-display-all-comments-on-a-worksheet-in-an-application-level-vsto-add-in"></a>Отображение всех комментариев на листе в надстройке VSTO уровня приложения  
  
1.  Присвойте свойству <xref:Microsoft.Office.Interop.Excel.Comment.Visible%2A> значение **true** , если нужно отображать комментарии; в противном случае присвойте ему значение **false**.  
  
     [!code-csharp[Trin_VstcoreExcelAutomationAddIn#21](../vsto/codesnippet/CSharp/trin_vstcoreexcelautomationaddin/ThisAddIn.cs#21)]
     [!code-vb[Trin_VstcoreExcelAutomationAddIn#21](../vsto/codesnippet/VisualBasic/trin_vstcoreexcelautomationaddin/ThisAddIn.vb#21)]  
  
## <a name="see-also"></a>См. также  
 [Работа с листами](../vsto/working-with-worksheets.md)   
 [Практическое руководство. Программное добавление и удаление примечаний на листе](../vsto/how-to-programmatically-add-and-delete-worksheet-comments.md)   
 [Ведущие элементы и элементы управления](../vsto/host-items-and-host-controls-overview.md)  
