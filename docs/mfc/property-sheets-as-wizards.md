---
description: Дополнительные сведения о страницах свойств см. в мастерах
title: Вкладки свойств как мастера
ms.date: 11/04/2016
helpviewer_keywords:
- property sheets, as wizards
ms.assetid: 1ea66ecb-23b0-484a-838d-58671a2999b5
ms.openlocfilehash: 2a68a16936e8ab134bab2fe78dac0d29c125b4db
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97248870"
---
# <a name="property-sheets-as-wizards"></a>Вкладки свойств как мастера

Ключевой характеристикой страницы свойств мастера является то, что переход осуществляется с помощью кнопок "Далее" или "Готово", "назад" и "Отмена" вместо вкладок. Чтобы воспользоваться преимуществами этой функции, необходимо вызвать метод [CPropertySheet:: сетвизардмоде](../mfc/reference/cpropertysheet-class.md#setwizardmode) перед вызовом [CPropertySheet::D омодал](../mfc/reference/cpropertysheet-class.md#domodal) в объекте страницы свойств.

При переходе с одной страницы на другую страница пользователь получает те же уведомления [CPropertyPage:: онсетактиве](../mfc/reference/cpropertypage-class.md#onsetactive) и [CPropertyPage:: онкиллактиве](../mfc/reference/cpropertypage-class.md#onkillactive) . Кнопки "Далее" и "Готово" являются взаимоисключающими элементами управления. то есть в каждый момент времени будет отображаться только один из них. На первой странице должна быть включена кнопка Далее. Если пользователь находится на последней странице, должна быть включена кнопка Готово. Это не выполняется автоматически платформой. Чтобы добиться этого, необходимо вызвать [CPropertySheet:: сетвизардбуттон](../mfc/reference/cpropertysheet-class.md#setwizardbuttons) на последней странице.

Чтобы отобразить все кнопки по умолчанию, должен отобразить кнопку Готово и переместить кнопку Далее. Затем переместите кнопку назад, чтобы сохранить ее относительное положение до кнопки Далее.

## <a name="example"></a>Пример

[!code-cpp[NVC_MFCDocView#5](../mfc/codesnippet/cpp/property-sheets-as-wizards_1.cpp)]

## <a name="see-also"></a>См. также раздел

[Вкладки свойств](../mfc/property-sheets-mfc.md)
