---
description: Дополнительные сведения о версии (C/C++)
title: VERSION (C/C++)
ms.date: 11/04/2016
f1_keywords:
- VERSION
helpviewer_keywords:
- VERSION .def file statement
ms.assetid: 3533b97c-5183-45f9-9ca8-4e63462b5d26
ms.openlocfilehash: 1a63435c752220ab9fef54628ab101a14ef58582
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97176396"
---
# <a name="version-cc"></a>VERSION (C/C++)

Указывает ссылке на размещение номера в заголовке EXE-файла или библиотеки DLL.

```
VERSION major[.minor]
```

## <a name="remarks"></a>Комментарии

*Основной* и *дополнительный* аргументы — десятичные числа в диапазоне от 0 до 65 535. Значение по умолчанию — версия 0,0.

Аналогичный способ указания номера версии — с параметром [сведения о версии](version-version-information.md) (/Version).

## <a name="see-also"></a>См. также раздел

[Правила для Module-Definitionных инструкций](rules-for-module-definition-statements.md)
