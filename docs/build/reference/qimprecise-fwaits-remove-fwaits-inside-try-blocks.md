---
description: Дополнительные сведения о:/Qimprecise_fwaits (удаление fwaits внутри блоков try)
title: /Qimprecise_fwaits (Удалить ожидания в блоке try)
ms.date: 11/04/2016
f1_keywords:
- /Qimprecise_fwaits
helpviewer_keywords:
- -Qimprecise_fwaits compiler option (C++)
- /Qimprecise_fwaits compiler option (C++)
ms.assetid: b1501f21-7e08-4fea-95e8-176ec03a635b
ms.openlocfilehash: 5f3d96656d062a7e5b0c4ad78ba7cd536069e013
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97225626"
---
# <a name="qimprecise_fwaits-remove-fwaits-inside-try-blocks"></a>/Qimprecise_fwaits (Удалить ожидания в блоке try)

Удаляет `fwait` команды, внутренние для **`try`** блоков, при использовании параметра компилятора [/FP: except](fp-specify-floating-point-behavior.md) .

## <a name="syntax"></a>Синтаксис

```
/Qimprecise_fwaits
```

## <a name="remarks"></a>Remarks

Этот параметр не действует, если **/FP: except** также не задан. Если указать параметр **/FP: except** , компилятор вставит `fwait` в блоке команды вокруг каждой строки кода **`try`** . Таким образом, компилятор может опознать конкретную строку кода, которая создает исключение. **/Qimprecise_fwaits** удаляют внутренние `fwait` инструкции, в результате чего выполняется только ожидание **`try`** блока. Это повышает производительность, но компилятор может только сказать, какой **`try`** блок вызывает исключение, а не какую строку.

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Откройте папку **C/C++** .

1. Выберите страницу свойств **Командная строка** .

1. Введите параметр компилятора в поле **Дополнительные параметры** .

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalOptions%2A>.

## <a name="see-also"></a>См. также раздел

[Параметры/q (низкоуровневые операции)](q-options-low-level-operations.md)<br/>
[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)
