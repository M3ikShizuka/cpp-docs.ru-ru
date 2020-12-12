---
description: Дополнительные сведения о:/GZ (включение кадра стека Run-Time проверка ошибок)
title: /GZ (Позволяет проверку фрейма стека ошибки во время выполнения)
ms.date: 11/04/2016
f1_keywords:
- /gz
helpviewer_keywords:
- -GZ compiler option [C++]
- release-build errors
- /GZ compiler option [C++]
- GZ compiler option [C++]
- debug builds, catch release-build errors
ms.assetid: b3efeeff-d5e3-4057-91c9-f6fc73d0270c
ms.openlocfilehash: 0b0936037c265bf57413c458ffc0a831184cb074
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97191697"
---
# <a name="gz-enable-stack-frame-run-time-error-checking"></a>/GZ (Позволяет проверку фрейма стека ошибки во время выполнения)

Выполняет те же операции, что и параметр [/RTC (проверки ошибок во время выполнения)](rtc-run-time-error-checks.md) . Не рекомендуется.

## <a name="syntax"></a>Синтаксис

```
/GZ
```

## <a name="remarks"></a>Remarks

**/Gz** используется только в неоптимизированной сборке (/OD ([Disable (Отладка)](od-disable-debug.md))).

**/Gz** является устаревшим, так как Visual Studio 2005; Вместо этого используйте [/RTC (проверки ошибок во время выполнения)](rtc-run-time-error-checks.md) . Список устаревших параметров компилятора см. в разделе **устаревшие и удаленные параметры** компилятора в [параметрах компилятора, перечисленных по категориям](compiler-options-listed-by-category.md).

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Откройте папку **C/C++** .

1. Выберите страницу свойств **Командная строка** .

1. Введите параметр компилятора в поле **Дополнительные параметры** .

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalOptions%2A>.

## <a name="see-also"></a>См. также раздел

[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)
