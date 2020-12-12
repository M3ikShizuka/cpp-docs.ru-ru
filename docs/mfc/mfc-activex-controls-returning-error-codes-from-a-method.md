---
description: 'Дополнительные сведения см. в статье элементы управления ActiveX в MFC: Возвращение кодов ошибок из метода'
title: Элементы управления ActiveX в MFC. Возврат кодов ошибок из метода
ms.date: 11/04/2016
helpviewer_keywords:
- MFC ActiveX controls [MFC], error codes
- SetNotSupported method, using
- errors [MFC], ActiveX control error codes
- GetNotSupported method [MFC]
- FireError method [MFC]
- SCODE, MFC ActiveX controls
- ThrowError method [MFC]
ms.assetid: 771fb9c9-2413-4dcc-b386-7bc4c4adeafd
ms.openlocfilehash: f6a1f372442ee67787a7a5421dabb4460acfcc7a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97206075"
---
# <a name="mfc-activex-controls-returning-error-codes-from-a-method"></a>Элементы управления ActiveX в MFC. Возврат кодов ошибок из метода

В этой статье описывается, как вернуть коды ошибок из метода элемента управления ActiveX.

Чтобы указать, что в методе произошла ошибка, следует использовать функцию-член [COleControl:: ThrowError](reference/colecontrol-class.md#throwerror) , которая принимает в качестве параметра значение SCODE (код состояния). Вы можете использовать предопределенный SCODE или определить один из них.

> [!NOTE]
> `ThrowError` предназначен для использования только в качестве способа возвращения ошибки из функции Get или Set свойства или метода автоматизации. Это единственный раз, когда в стеке будет присутствовать соответствующий обработчик исключений.

Вспомогательные функции существуют для наиболее распространенных предопределенных Скодес, таких как [COleControl:: сетнотсуппортед](reference/colecontrol-class.md#setnotsupported), [COleControl:: жетнотсуппортед](reference/colecontrol-class.md#getnotsupported)и [COleControl:: сетнотпермиттед](reference/colecontrol-class.md#setnotpermitted).

Список предопределенных Скодес и инструкции по определению пользовательских Скодес см. в разделе [Обработка ошибок в элементе управления ActiveX в элементах](mfc-activex-controls-advanced-topics.md) управления ActiveX: дополнительные разделы.

Дополнительные сведения о сообщениях об исключениях в других областях кода см. в разделах [COleControl:: фириррор](reference/colecontrol-class.md#fireerror) и [Обработка ошибок в элементе управления ActiveX в элементах](mfc-activex-controls-advanced-topics.md) управления ActiveX: дополнительные разделы.

## <a name="see-also"></a>См. также раздел

[Элементы управления ActiveX в MFC](mfc-activex-controls.md)
