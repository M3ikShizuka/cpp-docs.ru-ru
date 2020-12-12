---
description: Дополнительные сведения о:/Wp64 (обнаружение проблем переносимости 64-разрядных)
title: /Wp64 (выявление проблем переносимости на 64-разрядные платформы)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCCLWCECompilerTool.Detect64BitPortabilityProblems
- VC.Project.VCCLCompilerTool.Detect64BitPortabilityProblems
- /wp64
helpviewer_keywords:
- 64-bit compiler [C++], detecting portability problems
- /Wp64 compiler option [C++]
- -Wp64 compiler option [C++]
- Wp64 compiler option [C++]
ms.assetid: 331ae5aa-e627-4d03-8f63-dd2c2d76dadd
ms.openlocfilehash: d1ee441089531c4ebe222c73f6cec16b59fa7583
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97261090"
---
# <a name="wp64-detect-64-bit-portability-issues"></a>/Wp64 (выявление проблем переносимости на 64-разрядные платформы)

Этот параметр компилятора не рекомендуется. В версиях до Visual Studio 2013 это позволяет выявить проблемы с 64-разрядной переносимостью для типов, помеченных также ключевым словом [__w64](../../cpp/w64.md) .

## <a name="syntax"></a>Синтаксис

```
/Wp64
```

## <a name="remarks"></a>Remarks

По умолчанию в версиях Visual Studio до Visual Studio 2013 параметр компилятора **/Wp64** отключен в компиляторе компилятором MSVC, который строит 32-разрядный код x86, а также в компиляторе компилятором MSVC, который строит 64-разрядный код x64.

> [!IMPORTANT]
> Параметр компилятора [/Wp64](wp64-detect-64-bit-portability-issues.md) и ключевое слово [__w64](../../cpp/w64.md) являются устаревшими в Visual Studio 2010 и Visual Studio 2012. Они не поддерживаются в версиях начиная с Visual Studio 2013. Если вы преобразуете проект, использующий этот параметр, то во время преобразования он не будет перенесен. Для использования этого параметра в Visual Studio 2010 или Visual Studio 2012 следует ввести параметр компилятора в области **Дополнительные параметры** раздела **Командная строка** в свойствах проекта. Если в командной строке используется параметр компилятора **/Wp64** , компилятор выводит предупреждение командной строки D9002. Вместо использования этого параметра и ключевого слова для обнаружения проблем переносимости в 64-разрядном режиме используйте компилятор КОМПИЛЯТОРОМ MSVC, предназначенный для 64-разрядной платформы, и укажите параметр [/W4](compiler-option-warning-level.md) . Дополнительные сведения см. в статье [Настройка проектов C++ для 64-разрядных целевых объектов x64](../configuring-programs-for-64-bit-visual-cpp.md).

Следующие типы переменных проверяются в 32-разрядной операционной системе, как если бы они использовались в 64-разрядной операционной системе:

- INT

- long

- указатель

Если вы регулярно компилируете приложение с помощью компилятора, который строит 64-разрядный код x64, можно просто отключить **/Wp64** в 32-разрядных компиляциях, так как компилятор 64-bit обнаружит все проблемы. Дополнительные сведения о том, как ориентироваться на операционную систему Windows 64-bit, см. в статье [Настройка проектов C++ для 64-разрядных целевых объектов x64](../configuring-programs-for-64-bit-visual-cpp.md).

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

1. Откройте диалоговое окно **Окна свойств** проекта.

   Подробнее см. в статье [Настройка компилятора C++ и свойств сборки в Visual Studio](../working-with-project-properties.md).

1. Откройте папку **C/C++** .

1. Выберите страницу свойств **Командная строка** .

1. Измените поле **Дополнительные параметры** , включив в него параметр **/Wp64**.

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.Detect64BitPortabilityProblems%2A>.

## <a name="see-also"></a>См. также раздел

[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)<br/>
[Настройка проектов C++ для 64-разрядных целевых объектов с архитектурой x64](../configuring-programs-for-64-bit-visual-cpp.md)
