---
description: Дополнительные сведения:. OBJ-файлы в качестве входных файлов компоновщика
title: OBJ-файлы в качестве входных файлов компоновщика
ms.date: 12/29/2017
helpviewer_keywords:
- linker [C++], OBJ files as input
- object files, linker output
- OMF object files
- LINK tool [C++], .obj files
- COFF files
- OBJ files as linker input
- .obj files as linker input
ms.openlocfilehash: 33b4a9d9a23854766100d0b023713f7ecbc71e32
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97192724"
---
# <a name="obj-files-as-linker-input"></a>OBJ-файлы в качестве входных файлов компоновщика

Средство компоновщика (LINK.EXE) принимает OBJ-файлы в формате COFF.

## <a name="remarks"></a>Комментарии

Корпорация Майкрософт предоставляет полное описание формата общего объектного файла. Дополнительные сведения см. в разделе [Формат PE](/windows/win32/Debug/pe-format).

## <a name="unicode-support"></a>Поддержка Юникода

Начиная с Visual Studio 2005 компилятор Microsoft КОМПИЛЯТОРОМ MSVC поддерживает символы Юникода в идентификаторах, как определено стандартами ISO/IEC C и C++. Предыдущие версии компилятора поддерживали только символы ASCII в идентификаторах. Для поддержки Юникода в именах функций, классов и статических элементов компилятор и компоновщик используют кодировку Юникод UTF-8 для символов COFF в OBJ-файлах. Кодировка UTF-8 обеспечивает обратную совместимость с кодировкой ASCII, используемой в более ранних версиях Visual Studio.

Дополнительные сведения о компиляторе и компоновщике см. в разделе [Поддержка Юникода в компиляторе и компоновщике](unicode-support-in-the-compiler-and-linker.md). Дополнительные сведения о стандарте Unicode см. в разделе Организация [Юникода](https://home.unicode.org/) .

## <a name="see-also"></a>См. также раздел

[Входные файлы ссылок](link-input-files.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)<br/>
[Поддержка Юникода](../../text/support-for-unicode.md)<br/>
[Поддержка Юникода в компиляторе и компоновщике](unicode-support-in-the-compiler-and-linker.md)<br/>
[Стандарт Юникод](https://home.unicode.org/)<br/>
[Формат PE](/windows/win32/Debug/pe-format)
