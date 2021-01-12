---
description: Дополнительные сведения о:/ZP (выравнивание членов структуры)
title: /Zp (Выравнивание члена структуры)
ms.date: 01/08/2021
f1_keywords:
- /zp
- VC.Project.VCCLCompilerTool.StructMemberAlignment
- VC.Project.VCCLWCECompilerTool.StructMemberAlignment
helpviewer_keywords:
- Struct Member Alignment compiler option
- Zp compiler option
- /Zp compiler option [C++]
- -Zp compiler option [C++]
ms.assetid: 5242f656-ed9b-48a3-bc73-cfcf3ed2520f
ms.openlocfilehash: 8d29c442726aff9503a42378fce6a7b8b09526ed
ms.sourcegitcommit: 14d6ae0d527d05d153e26463d4cd5ada0f43e864
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/11/2021
ms.locfileid: "98104782"
---
# <a name="zp-struct-member-alignment"></a>/Zp (Выравнивание члена структуры)

Управляет упаковкой элементов структуры в память и задает одну и ту же упаковку для всех структур в модуле.

## <a name="syntax"></a>Синтаксис

> **`/Zp`**[**`1`**|**`2`**|**`4`**|**`8`**|**`16`**]

## <a name="remarks"></a>Комментарии

**`/ZpN`** Параметр указывает компилятору, где следует хранить каждый член структуры. Компилятор сохраняет элементы после первого элемента на границе, которая меньше либо размера типа элемента, либо *N*-байтовой границы.

Доступные значения упаковки описаны в следующей таблице.

|/ZP, аргумент|Действие|
|-|-|
|1|Упаковывает структуры по 1-байтным границам. Эквивалентно **`/Zp`** .|
|2|Упаковывает структуры на 2-байтовые границы.|
|4|Упаковывает структуры на 4-байтные границы.|
|8|Упаковывает структуры по 8-байтным границам (по умолчанию для x86, ARM и ARM64).|
|16| Упаковывает структуры по 16-байтным границам (по умолчанию для x64).|

Не используйте этот параметр, если не заданы конкретные требования к выравниванию.

> [!WARNING]
> Заголовки C/C++ в Windows SDK предполагают **`/Zp8`** внутреннюю упаковку. Не изменяйте настройку по умолчанию при включении заголовков Windows SDK с помощью **`/Zp`** в командной строке или с помощью `#pragma pack` . В противном случае приложение может вызвать повреждение памяти во время выполнения.

[ `pack` Директиву pragma](../../preprocessor/pack.md) можно также использовать для управления упаковкой структуры. Дополнительные сведения о выравнивании см. в разделах:

- [`align`](../../cpp/align-cpp.md)

- [`alignof` Станции](../../cpp/alignof-operator.md)

- [`__unaligned`](../../cpp/unaligned.md)

- [`/ALIGN` (Выравнивание разделов)](align-section-alignment.md)

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите страницу свойств **Свойства "**  >  Создание кода **C/C++**"  >   .

1. Измените свойство **Выравнивание члена структуры** .

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.StructMemberAlignment%2A>.

## <a name="see-also"></a>См. также статью

[Параметры компилятора КОМПИЛЯТОРОМ MSVC](compiler-options.md) \
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)
