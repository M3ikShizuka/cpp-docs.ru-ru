---
description: Дополнительные сведения см. в справочнике по EDITBIN.
title: Справочник ЕDITBIN
ms.date: 11/04/2016
f1_keywords:
- editbin
helpviewer_keywords:
- binary data, editing
- object files, modifying
- EDITBIN program
- COFF files, editing
ms.assetid: efdda03b-3dfc-4d31-90e6-caf5b3977914
ms.openlocfilehash: ad211ab85ac00cd716b7c3b8e381a9a448ea04ff
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97201031"
---
# <a name="editbin-reference"></a>Справочник ЕDITBIN

Редактор двоичных файлов Microsoft COFF (EDITBIN.EXE) изменяет двоичные файлы в формате COFF. EDITBIN можно использовать для изменения объектных файлов, исполняемых файлов и библиотек динамической компоновки (DLL).

> [!NOTE]
> Это средство можно запустить только из командной строки Visual Studio. В системной командной строке или проводнике это невозможно.

Программа EDITBIN недоступна для файлов, созданных с параметром компилятора [/GL](gl-whole-program-optimization.md) . Любые изменения в двоичных файлах, создаваемых с помощью/GL, должны быть достигнуты путем перекомпиляции и связывания.

- [Командная строка EDITBIN](editbin-command-line.md)

- [Параметры EDITBIN](editbin-options.md)

## <a name="see-also"></a>См. также раздел

[Дополнительные средства сборки КОМПИЛЯТОРОМ MSVC](c-cpp-build-tools.md)
