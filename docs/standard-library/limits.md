---
description: 'Дополнительные сведения: &lt; ограничения&gt;'
title: '&lt;limits&gt;'
ms.date: 11/04/2016
f1_keywords:
- <limits>
helpviewer_keywords:
- limits header
ms.assetid: e07d6379-5b00-4a3d-a789-40d41538b59e
ms.openlocfilehash: 23601b4b7f7ea06071a6b1f5fbd87ce0a0babce3
ms.sourcegitcommit: 118e4ad82c0f1c9ac120f105d84224e5fe4cef28
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/12/2021
ms.locfileid: "98126394"
---
# <a name="ltlimitsgt"></a>&lt;limits&gt;

Определяет шаблон класса `numeric_limits` и два перечисления, касающиеся представления чисел с плавающей запятой и округления.

## <a name="requirements"></a>Требования

**Заголовок:**\<limits>

**Пространство имен:** std

## <a name="remarks"></a>Remarks

Явные специализации `numeric_limits` класса описывают множество свойств фундаментальных типов, включая символы, целые числа и типы с плавающей запятой, а **`bool`** также определенные реализации, а не фиксированные правилами языка C++. Свойства, описанные в \<limits> , включают в себя точность, минимальное и максимальное размеры, округление и тип сигнала.

## <a name="members"></a>Элементы

### <a name="enumerations"></a>Перечисления

|Имя|Описание|
|-|-|
|[float_denorm_style](../standard-library/limits-enums.md#float_denorm_style)|Перечисление описывает различные методы, которые могут быть выбраны реализацией для представления ненормализованного значения с плавающей запятой, если оно мало для представления в качестве нормализованного значения:|
|[float_round_style](../standard-library/limits-enums.md#float_round_style)|Перечисление описывает различные методы, которые могут быть выбраны реализацией для округления значения с плавающей запятой до целочисленного.|

### <a name="classes"></a>Классы

|name|Описание|
|-|-|
|[Класс numeric_limits](../standard-library/numeric-limits-class.md)|Шаблон класса описывает арифметические свойства встроенных числовых типов.|

## <a name="see-also"></a>См. также раздел

[Справочник по файлам заголовков](../standard-library/cpp-standard-library-header-files.md)\
[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)
