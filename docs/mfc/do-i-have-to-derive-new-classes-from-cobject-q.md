---
description: 'Дополнительные сведения: требуется ли создавать новые классы от CObject?'
title: Необходимо ли создавать новые классы как производные от CObject?
ms.date: 11/04/2016
helpviewer_keywords:
- derived classes [MFC], from CObject
- CObject class [MFC], when to use
ms.assetid: 26021031-feaf-424c-80d1-9547c4409d6a
ms.openlocfilehash: d37570cb62f1ee274e4cea85fc95a9221c95fd8a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97261311"
---
# <a name="do-i-have-to-derive-new-classes-from-cobject"></a>Необходимо ли создавать новые классы как производные от CObject?

Нет, нет.

Создавайте класс от [CObject](reference/cobject-class.md) , если вам нужны предоставляемые им средства, такие как сериализация или динамическое создание. Многие классы данных должны быть сериализованы в файлы, поэтому часто рекомендуется наследовать их от `CObject` . Пример класса, производного от `CObject` , см. в [образце Scribble](../overview/visual-cpp-samples.md).

## <a name="see-also"></a>См. также раздел

[Класс CObject: часто задаваемые вопросы](cobject-class-frequently-asked-questions.md)
