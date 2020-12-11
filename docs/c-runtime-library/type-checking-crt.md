---
description: 'Дополнительные сведения: проверка типов (CRT)'
title: Проверка типов (CRT)
ms.date: 11/04/2016
f1_keywords:
- c.types
helpviewer_keywords:
- checking type
- variable argument functions
- type checking
ms.assetid: 1ba7590b-d1c0-4636-b6a0-e231395abdad
ms.openlocfilehash: cf27847bf2aeef278fb4699cea5a0cf74a961086
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97162358"
---
# <a name="type-checking-crt"></a>Проверка типов (CRT)

Компилятор выполняет ограниченную проверку типов для функций, которые могут принимать переменное число аргументов, как указано ниже:

|Вызов функции|Аргументы, для которых проверяется тип|
|-------------------|-----------------------------|
|`_cprintf_s`, `_cscanf_s`, `printf_s`, `scanf_s`|Первый аргумент (строка форматирования)|
|`fprintf_s`, `fscanf_s`, `sprintf_s`, `sscanf_s`|Первые два аргумента (файл или буфер и строка форматирования)|
|`_snprintf_s`|Первые три аргумента (файл или буфер, количество и строка форматирования)|
|`_open`|Первые два аргумента (путь и флаг `_open`)|
|`_sopen_s`|Первые три аргумента (путь, флаг `_open` и режим общего доступа)|
|`_execl`, `_execle`, `_execlp`, `_execlpe`|Первые два аргумента (путь и первый указатель на аргумент)|
|`_spawnl`, `_spawnle`, `_spawnlp`, `_spawnlpe`|Первые три аргумента (флаг режима, путь и первый указатель на аргумент)|

Компилятор выполняет такую же ограниченную проверку типов для аналогов этих функций для расширенных символов.

## <a name="see-also"></a>См. также раздел

[Возможности библиотеки CRT](../c-runtime-library/crt-library-features.md)
