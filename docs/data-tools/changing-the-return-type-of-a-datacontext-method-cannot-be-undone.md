---
title: Невозможно отменить замену типа значений, возвращаемых методом DataContext
ms.date: 11/04/2016
ms.topic: reference
ms.assetid: 76b161fc-5075-4192-8d94-f15b02e199e9
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.workload:
- data-storage
ms.openlocfilehash: e133a609b8e3a0b8b47d0c2ea7408d7c3e9bd9c3
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MTE95
ms.contentlocale: ru-RU
ms.lasthandoff: 01/02/2019
ms.locfileid: "53947781"
---
# <a name="changing-the-return-type-of-a-datacontext-method-cannot-be-undone"></a>Невозможно отменить замену типа значений, возвращаемых методом DataContext

Операция изменения типа возвращаемого значения метода DataContext не может быть отменена. Чтобы возвратиться назад к автоматически сгенерированному типу, необходимо снова перетащить элемент из **обозревателя серверов** или **обозревателя базы** данных на область реляционного конструктора объектов. Вы уверены, что хотите изменить тип возвращаемого значения?

Тип возвращения метода <xref:System.Data.Linq.DataContext> различен в зависимости от того, куда вы сбросили элемент в [!INCLUDE[vs_ordesigner_short](../data-tools/includes/vs_ordesigner_short_md.md)]. Если сбрасываете элемент прямо на существующий класс сущностей, то создается метод <xref:System.Data.Linq.DataContext>, который имеет тип возврата класса сущностей. Если вы сбрасываете элемент на пустую область конструктора [!INCLUDE[vs_ordesigner_short](../data-tools/includes/vs_ordesigner_short_md.md)], то создается метод <xref:System.Data.Linq.DataContext>, который возвращает автоматически сгенерированный тип. Можно изменить тип возврата метода <xref:System.Data.Linq.DataContext> после его добавления в область методов. Чтобы проверить или изменить тип возврата метода <xref:System.Data.Linq.DataContext>, выберите его и щелкните по свойству **Тип возврата** в окне **Свойства**.

## <a name="to-change-the-return-type-of-a-datacontext"></a>Для изменения типа возвращаемого значения метода DataContext

- Нажмите кнопку **Да**.

## <a name="to-exit-the-message-box-and-leave-the-return-type-unchanged"></a>Для закрытия окна сообщения, оставляя тип возврата неизмененным

- Нажмите кнопку **Нет**.

## <a name="to-revert-to-the-original-return-type-after-changing-the-return-type"></a>Чтобы возвратиться к первоначальному типу возврата после изменения типа возвращаемого значения

1. Выберите метод <xref:System.Data.Linq.DataContext> на [!INCLUDE[vs_ordesigner_short](../data-tools/includes/vs_ordesigner_short_md.md)] и удалите его.

2. Найдите элемент в **обозревателе серверов/обозревателе базы данных** и перетащите его на [!INCLUDE[vs_ordesigner_short](../data-tools/includes/vs_ordesigner_short_md.md)].

    Метод <xref:System.Data.Linq.DataContext> создается с первоначальным типом возврата по умолчанию.

## <a name="see-also"></a>См. также

- [Сообщения реляционного конструктора объектов](../data-tools/o-r-designer-messages.md)
- [Средства LINQ to SQL в Visual Studio](../data-tools/linq-to-sql-tools-in-visual-studio2.md)