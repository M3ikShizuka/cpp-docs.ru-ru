---
description: Дополнительные сведения о:/LN (создание модуля MSIL)
title: /LN (создание модуля MSIL)
ms.date: 11/04/2016
f1_keywords:
- /LN
helpviewer_keywords:
- -LN compiler option [C++]
- /LN compiler option [C++]
ms.assetid: 4f38f4f4-3176-4caf-8200-5c7585dc1ed3
ms.openlocfilehash: 63b6f47fe6bef24341d3c19a6ad96ac3808e486e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97190927"
---
# <a name="ln-create-msil-module"></a>/LN (создание модуля MSIL)

Указывает, что манифест сборки не должен быть включен в выходной файл.

## <a name="syntax"></a>Синтаксис

```
/LN
```

## <a name="remarks"></a>Remarks

По умолчанию параметр **/LN** не действует (манифест сборки вставляется в выходной файл).

При использовании параметра **/LN** также необходимо использовать один из параметров [/CLR (компиляция общеязыковой среды выполнения)](clr-common-language-runtime-compilation.md) .

Управляемая программа, которая не имеет метаданных сборки в манифесте, называется модулем. При компиляции с параметром [/c (компиляция без компоновки)](c-compile-without-linking.md) и **/LN** укажите [/NOASSEMBLY (создание модуля MSIL)](noassembly-create-a-msil-module.md) на этапе компоновщика, чтобы создать выходной файл.

Если вы хотите использовать для построения сборок подход на основе компонентов, может потребоваться создать модули.  То есть вы можете создавать типы и компилировать их в модули.  Затем можно создать сборку из одного или нескольких модулей.  Дополнительные сведения о создании сборок из модулей см. в разделе [NETMODULE-файлы в качестве входных данных компоновщика](netmodule-files-as-linker-input.md) или [Al.exe (компоновщик сборок)](/dotnet/framework/tools/al-exe-assembly-linker).

Расширение файла по умолчанию для модуля —. netmodule.

В выпусках, предшествующих Visual Studio 2005, был создан модуль с **параметром/clr: Assembly**.

Компоновщик КОМПИЛЯТОРОМ MSVC принимает файлы NETMODULE в качестве входных данных, а выходной файл, создаваемый компоновщиком, будет сборкой или файлом. netmodule без зависимости времени выполнения ни с одним из файлов NETMODULE, которые были введены компоновщиком.  Дополнительные сведения см. в разделе [NETMODULE-файлы в качестве входных файлов компоновщика](netmodule-files-as-linker-input.md).

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

- Укажите [/NOASSEMBLY (создание модуля MSIL)](noassembly-create-a-msil-module.md) на этапе компоновщика, чтобы создать выходной файл.

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- Этот параметр компилятора нельзя изменить программным способом.

## <a name="see-also"></a>См. также раздел

[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)
