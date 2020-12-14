---
description: 'Дополнительные сведения: управляющие флаги'
title: Флаги управления
ms.date: 11/04/2016
f1_keywords:
- c.flags
helpviewer_keywords:
- flags, control
- heap allocation, control flags
- debug heap, control flags
ms.assetid: 8dbd24a5-0633-42d1-9771-776db338465f
ms.openlocfilehash: 6b49bfa49e2e231a64af8d88739778964ce8ed21
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97195740"
---
# <a name="control-flags"></a>Флаги управления

Отладочная версия библиотеки времени выполнения Microsoft C использует следующие флаги для управления выделением памяти в куче и процессом создания отчетов. Дополнительные сведения см. в статье [Методы отладки CRT](/visualstudio/debugger/crt-debugging-techniques).

|Флаг|Описание|
|----------|-----------------|
|[_CRTDBG_MAP_ALLOC](../c-runtime-library/crtdbg-map-alloc.md)|Сопоставляет основные функции кучи и их отладочные версии|
|[_DEBUG](../c-runtime-library/debug.md)|Позволяет использовать отладочные версий функций среды выполнения|
|[_crtDbgFlag](../c-runtime-library/crtdbgflag.md)|Контролирует способ отслеживания выделения памяти отладочным диспетчером кучи|

Эти флаги можно определить с помощью параметра командной строки /D или с помощью директивы `#define`. Если этот флаг определяется с помощью директивы `#define`, она должна предшествовать оператору включения заголовочного файла, содержащего объявления подпрограмм.

## <a name="see-also"></a>См. также раздел

[Глобальные переменные и стандартные типы](../c-runtime-library/global-variables-and-standard-types.md)
