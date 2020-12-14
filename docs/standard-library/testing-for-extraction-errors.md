---
description: 'Дополнительные сведения: Проверка ошибок извлечения'
title: Проверка на наличие ошибок извлечения
ms.date: 11/04/2016
helpviewer_keywords:
- extraction errors
ms.assetid: 6a681028-adba-4557-8f7b-f137932905f8
ms.openlocfilehash: c4a9b5c1ffe4f78718563b33e39012272cfb8042
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97259361"
---
# <a name="testing-for-extraction-errors"></a>Проверка на наличие ошибок извлечения

Функции обработки ошибок вывода, рассматриваемые в разделе [Функции обработки ошибок](../standard-library/output-file-stream-member-functions.md), применяются к входным потокам. Проверка на наличие ошибок во время извлечения очень важна. Рассмотрим следующую инструкцию.

```cpp
cin>> n;
```

Если `n` — это целое число со знаком, значение больше 32 767 (максимальное допустимое значение или MAX_INT) задает бит `fail` потока, а объект `cin` становится непригодным для использования. Все последующие извлечения приводят к немедленному возврату без сохранения значений.

## <a name="see-also"></a>См. также раздел

[Входные потоки](../standard-library/input-streams.md)
