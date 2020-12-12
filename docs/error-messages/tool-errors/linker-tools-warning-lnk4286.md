---
description: 'Дополнительные сведения: Предупреждение средств компоновщика LNK4286'
title: Предупреждение средств компоновщика LNK4286
ms.date: 04/15/2019
f1_keywords:
- LNK4286
helpviewer_keywords:
- LNK4286
ms.openlocfilehash: 6a1e397967857ae3f982bf8f5e55f4bf74c9abe4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97244450"
---
# <a name="linker-tools-warning-lnk4286"></a>Предупреждение средств компоновщика LNK4286

> символ "*symbol*", определенный в "*filename_1. obj*", импортируется "*filename_2. obj*"

для *symbol* был указан [__declspec (dllimport)](../../cpp/dllexport-dllimport.md) , хотя символ определен в объектном файле *filename_1. obj* в том же образе. `__declspec(dllimport)`Чтобы устранить это предупреждение, удалите модификатор.

## <a name="remarks"></a>Комментарии

Предупреждение LNK4286 — это более общая версия [средств компоновщика LNK4217 Warning](linker-tools-warning-lnk4217.md). Компоновщик создает предупреждение LNK4286, когда он может определить, какой объектный файл ссылается на символ, но не какая функция.

Чтобы разрешить LNK4286, удалите `__declspec(dllimport)` Модификатор объявления из прямого объявления *символа* , указанного в *filename_2. obj*.

Хотя окончательный созданный код работает правильно, код, созданный для вызова импортированной функции, менее эффективен, чем вызов функции напрямую. Это предупреждение не появляется при компиляции с параметром [/CLR](../../build/reference/clr-common-language-runtime-compilation.md) .

Дополнительные сведения об объявлениях импорта и экспорта данных см. в разделе [dllexport, dllimport](../../cpp/dllexport-dllimport.md).

## <a name="see-also"></a>См. также раздел

[Предупреждение средств компоновщика LNK4049](linker-tools-warning-lnk4049.md) \
[Предупреждение средств компоновщика LNK4217](linker-tools-warning-lnk4217.md) \
[dllexport, dllimport](../../cpp/dllexport-dllimport.md)
