---
title: XML-фрагменты
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
ms.assetid: 348dbf64-3f09-4fff-b47a-a7ecdf3221cc
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 649617ac905e7d81ea68c5e5550dc106fbe1c24d
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/25/2019
ms.locfileid: "55020962"
---
# <a name="xml-snippets"></a>XML-фрагменты

XML Editor содержит возможность, называемую *XML-фрагменты*, который позволяет более быстро создавать XML-файлы. XML-фрагменты можно использовать повторно, вставляя их в файлы. Также можно создавать XML-данные, исходя из схемы на языке XSD.

## <a name="reusable-xml-snippets"></a>Повторно используемые XML-фрагменты

XML Editor включает множество фрагментов, охватывающих некоторые распространенные задачи. Это позволяет более легко создавать XML-файлы. Например, при создании или редактировании XML-схемы с помощью фрагментов «Элемент последовательности сложного типа» и «Элемент простого типа» в файл вставляется следующий текст XML. Затем при необходимости можно изменить значение `name`.

```xml
<xs:element name="name">
  <xs:complexType>
    <xs:sequence>
      <xs:element name="name">
        <xs:simpleType>
          <xs:restriction base="xs:string"></xs:restriction>
        </xs:simpleType>
      </xs:element>
    </xs:sequence>
  </xs:complexType>
</xs:element>
```

 Существует два способа вставки фрагментов. **Вставить фрагмент** команда вставляет фрагмент кода XML в позиции курсора. **Окружить** команда создает оболочку для XML-фрагмент вокруг выбранного текста. Обе команды доступны либо из **IntelliSense** подменю **изменить** меню или в контекстном меню редактора.

 Дополнительные сведения см. в разделе [Как Использовать XML-фрагменты](../xml-tools/how-to-use-xml-snippets.md).

## <a name="schema-generated-xml-snippets"></a>XML-фрагменты, сформированные схемой
 XML Editor также может создавать XML-фрагменты из XML-схем. Эта возможность позволяет заполнять элементы XML-элементами, созданными из информации схемы для этого элемента.

 Дополнительные сведения см. в разделе [Как Создание XML-фрагмент из схемы XML](../xml-tools/how-to-generate-an-xml-snippet-from-an-xml-schema.md).

## <a name="create-new-xml-snippets"></a>Создание нового XML-фрагментов
 Кроме фрагментов, которые входят в состав [!INCLUDE[msCoName](../xml-tools/includes/msconame_md.md)] Visual Studio по умолчанию, можно также создать и использовать собственные XML-фрагменты.

 Дополнительные сведения см. в разделе [Как Создание XML-фрагментов](../xml-tools/how-to-create-xml-snippets.md).

## <a name="see-also"></a>См. также

- [XML-редактор](../xml-tools/xml-editor.md)