---
description: Дополнительные сведения о:/c (компиляция без компоновки)
title: Параметр /c (компиляция без связывания)
ms.date: 11/04/2016
f1_keywords:
- /c
helpviewer_keywords:
- suppress link
- cl.exe compiler, compiling without linking
- -c compiler option [C++]
- c compiler option [C++]
- /c compiler option [C++]
ms.assetid: 8017fc3d-e5dd-4668-a1f7-3120daa95d20
ms.openlocfilehash: b9dd692dd99cddf63015fe26e37dc54841816f7f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97179373"
---
# <a name="c-compile-without-linking"></a>Параметр /c (компиляция без связывания)

Предотвращает автоматический вызов LINK.

## <a name="syntax"></a>Синтаксис

```
/c
```

## <a name="remarks"></a>Remarks

При компиляции с параметром **/c** создаются только OBJ-файлы. Необходимо явно вызвать LINK с соответствующими файлами и параметрами для выполнения фазы связывания сборки.

Во всех внутренних проектах, созданных в среде разработки, по умолчанию используется параметр **/c** .

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

- Этот параметр недоступен в среде разработки.

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- Сведения об установке этого параметра компилятора программными средствами см. в разделе <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.CompileOnly%2A>.

## <a name="example"></a>Пример

Следующая командная строка создает объектные файлы FIRST. obj и SECOND. obj. Третий obj игнорируется.

```
CL /c FIRST.C SECOND.C THIRD.OBJ
```

Чтобы создать исполняемый файл, необходимо вызвать LINK:

```
LINK firsti.obj second.obj third.obj /OUT:filename.exe
```

## <a name="see-also"></a>См. также раздел

[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)
