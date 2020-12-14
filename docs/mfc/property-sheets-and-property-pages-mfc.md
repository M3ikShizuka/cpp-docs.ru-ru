---
description: 'Дополнительные сведения: вкладки свойств и страницы свойств (MFC)'
title: Вкладки свойств и страницы свойств (MFC)
ms.date: 11/04/2016
helpviewer_keywords:
- MFC dialog boxes [MFC], tabs
- property pages [MFC], property sheets
- CPropertyPage class [MFC], property sheets and pages
- CPropertySheet class [MFC], property sheets and pages
- property sheets, propert pages
ms.assetid: de8fea12-6c35-4cef-8625-b8073a379446
ms.openlocfilehash: 6819b890c699aeb428d2e0c76b048f5043e1dee7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97248857"
---
# <a name="property-sheets-and-property-pages-mfc"></a>Вкладки свойств и страницы свойств (MFC)

[Диалоговое окно](../mfc/dialog-boxes.md) MFC может занимать «диалоговое окно вкладки», включающее вкладки свойств и страницы свойств. Такое диалоговое окно, называемое «страницей свойств» в MFC, аналогично многим диалоговым окнам в Microsoft Word, Excel и Visual C++, содержит стек листов с вкладками, похожий на стек папок файлов, отображаемых спереди на задний план, или группу каскадных окон. Элементы управления на вкладке Front видимы. на задних вкладках отображается только вкладка с метками. Страницы свойств особенно полезны для управления большим количеством свойств или параметров, которые очень хорошо попадают в несколько групп. Как правило, одна страница свойств может упростить пользовательский интерфейс, заменив несколько отдельных диалоговых окон.

Начиная с MFC версии 4,0, вкладки свойств и страницы свойств реализуются с помощью стандартных элементов управления, входящих в состав Windows 95 и Windows NT версии 3,51 и более поздних версий.

Вкладки свойств реализуются с помощью классов [CPropertySheet](../mfc/reference/cpropertysheet-class.md) и [CPropertyPage](../mfc/reference/cpropertypage-class.md) (описывается в *справочнике по MFC*). `CPropertySheet` определяет общее диалоговое окно, которое может содержать несколько "страниц" на основе `CPropertyPage` .

Сведения о создании и работе со страницами свойств см. в разделе [страницы свойств](../mfc/property-sheets-mfc.md)раздела.

## <a name="see-also"></a>См. также раздел

[Диалоговые окна](../mfc/dialog-boxes.md)<br/>
[Работа с диалоговыми окнами в MFC](../mfc/life-cycle-of-a-dialog-box.md)<br/>
[Вкладки свойств и страницы свойств в MFC](../mfc/property-sheets-and-property-pages-in-mfc.md)<br/>
[Обмен данными](../mfc/exchanging-data.md)<br/>
[Создание немодальной страницы свойств](../mfc/creating-a-modeless-property-sheet.md)<br/>
[Обработка кнопки "Применить"](../mfc/handling-the-apply-button.md)
