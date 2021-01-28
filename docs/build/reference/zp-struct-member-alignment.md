---
description: Дополнительные сведения о /Zp (Выравнивание элемента структуры)
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
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/11/2021
ms.locfileid: "98104782"
---
# <a name="zp-struct-member-alignment"></a>/Zp (Выравнивание члена структуры)

Управляет упаковкой элементов структуры в память и задает одну и ту же упаковку для всех структур в модуле.

## <a name="syntax"></a>Синтаксис

> **`/Zp`**[**`1`**|**`2`**|**`4`**|**`8`**|**`16`**]

## <a name="remarks"></a>Remarks

Параметр **`/ZpN`** указывает компилятору, где должен храниться каждый элемент структуры. Компилятор сохраняет элементы после первого элемента по границе, которая представляет собой меньшее из двух значений: размер типа элемента и *N* байт.

Возможные значения упаковки описаны в следующей таблице:

|Аргумент /Zp|Действие|
|-|-|
|1|Упаковывает структуры по 1-байтовым границам. Эквивалентно **`/Zp`** .|
|2|Упаковывает структуры по 2-байтовым границам.|
|4|Упаковывает структуры по 4-байтовым границам.|
|8|Упаковывает структуры по 8-байтовым границам (используется по умолчанию для x86, ARM и ARM64).|
|16| Упаковывает структуры по 16-байтовым границам (используется по умолчанию для x64).|

Не используйте этот параметр, если не заданы конкретные требования к выравниванию.

> [!WARNING]
> В заголовках C/C++ в Windows SDK предполагается внутренняя упаковка **`/Zp8`** . Не изменяйте значение параметра по умолчанию при включении заголовков Windows SDK с помощью **`/Zp`** в командной строке или с помощью `#pragma pack`. В противном случае во время выполнения приложения может произойти повреждение памяти.

Для управления упаковкой структур также можно использовать [`pack` pragma](../../preprocessor/pack.md). Дополнительные сведения о выравнивании см. в разделах:

- [`align`](../../cpp/align-cpp.md)

- [`alignof`Оператор](../../cpp/alignof-operator.md)

- [`__unaligned`](../../cpp/unaligned.md)

- [`/ALIGN` (выравнивание разделов)](align-section-alignment.md)

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Перейдите на страницу свойств **Свойства конфигурации** > **C/C++**  > **Создание кода**.

1. Измените свойство **Выравнивание элемента структуры**.

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.StructMemberAlignment%2A>.

## <a name="see-also"></a>См. также

[Параметры компилятора MSVC](compiler-options.md) \
[Синтаксис командной строки компилятора MSVC](compiler-command-line-syntax.md)
