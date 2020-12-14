---
description: Подробнее о:/ZL (опустить имя библиотеки по умолчанию)
title: /Zl (Опущенное по умолчанию имя библиотеки)
ms.date: 11/04/2016
f1_keywords:
- /zl
- VC.Project.VCCLCompilerTool.OmitDefaultLibName
helpviewer_keywords:
- -Zl compiler option [C++]
- ZI compiler option
- Omit Default Library Name compiler option
- /Zl compiler option [C++]
- default libraries, omitting names
ms.assetid: b27d39d0-44d6-498c-84ae-27c1326fee59
ms.openlocfilehash: eaf39b7bfe1a2b7f2d2c7754cccf8061543e4c7c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97224430"
---
# <a name="zl-omit-default-library-name"></a>/Zl (Опущенное по умолчанию имя библиотеки)

Опускает имя библиотеки времени выполнения C по умолчанию из OBJ-файла. По умолчанию компилятор помещает имя библиотеки в OBJ-файл, чтобы перенаправить компоновщик в правильную библиотеку.

## <a name="syntax"></a>Синтаксис

```
/Zl
```

## <a name="remarks"></a>Remarks

Дополнительные сведения о библиотеке по умолчанию см. в статье [использование Run-Time библиотеки](md-mt-ld-use-run-time-library.md).

Параметр **/Zl** можно использовать для компиляции OBJ-файлов, которые планируется разместить в библиотеке. Хотя пропуск имени библиотеки экономит лишь небольшой объем пространства для одного OBJ-файла, общее пространство сохраняется в библиотеке, содержащей множество модулей объектов.

Этот параметр является дополнительным. При установке этого параметра удаляется определенная поддержка библиотеки времени выполнения C, которая может потребоваться для приложения, что приведет к ошибкам во время компоновки, если приложение зависит от этой поддержки. При использовании этого параметра необходимо предоставить необходимые компоненты другим способом.

Используйте параметр [/NODEFAULTLIB (игнорировать библиотеки)](nodefaultlib-ignore-libraries.md). значение, чтобы направить компоновщику игнорировать ссылки на библиотеку во всех OBJ-файлах.

Дополнительные сведения см. в разделе [Функции библиотеки CRT](../../c-runtime-library/crt-library-features.md).

При компиляции с параметром **/Zl** `_VC_NODEFAULTLIB` определяется.  Пример:

```cpp
// vc_nodefaultlib.cpp
// compile with: /Zl
void Test() {
   #ifdef _VC_NODEFAULTLIB
      int i;
   #endif

   int i;   // C2086
}
```

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Откройте папку **C/C++** .

1. Перейдите на страницу свойств **Дополнительно** .

1. Измените свойство не **указывать имена библиотек по умолчанию** .

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.OmitDefaultLibName%2A>.

## <a name="see-also"></a>См. также раздел

[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)
