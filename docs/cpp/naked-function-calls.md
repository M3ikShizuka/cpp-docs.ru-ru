---
description: 'Дополнительные сведения: вызовы функций с атрибутом naked'
title: Вызовы функций Naked
ms.date: 11/04/2016
helpviewer_keywords:
- virtual device drivers
- VXD virtual device drivers
- virtual device drivers, naked function calls
- naked functions
- prolog code
- epilog code
- naked keyword [C++]
- naked keyword [C++], storage-class attribute
ms.assetid: 2a66847a-a43f-4541-a7be-c9f5f29b5fdb
ms.openlocfilehash: ffc28b65a8c16881164805f0cfa55ffe1bc54e9b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97313805"
---
# <a name="naked-function-calls"></a>Вызовы функций Naked

**Блок, относящийся только к системам Microsoft**

Функции, объявленные с **`naked`** атрибутом, создаются без кода пролога или эпилога, что позволяет создавать собственные последовательности пролога или эпилога с помощью [встроенного ассемблера](../assembler/inline/inline-assembler.md). Функции с атрибутом naked предоставляются как дополнительные функции. С их помощью можно объявить функцию, которая вызывается из другого контекста (и не C или C++), и тем самым указать другое место расположения параметров, в которых хранятся регистры. В качестве примера можно назвать такие процедуры, как обработчики прерываний. Эта возможность особенно полезна при написании драйверов виртуальных устройств (VxD).

## <a name="what-do-you-want-to-know-more-about"></a>Дополнительные сведения

- [naked](../cpp/naked-cpp.md)

- [Правила и ограничения для функций с атрибутом naked](../cpp/rules-and-limitations-for-naked-functions.md)

- [Рекомендации по написанию кода пролога или эпилога](../cpp/considerations-for-writing-prolog-epilog-code.md)

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Соглашения о вызовах](../cpp/calling-conventions.md)
