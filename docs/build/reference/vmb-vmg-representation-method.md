---
description: Дополнительные сведения о:/VMB,/vmg (метод представления)
title: /vmb, /vmg (метод представления)
ms.date: 11/04/2016
f1_keywords:
- /vmb
- /vmg
helpviewer_keywords:
- vmb compiler option [C++]
- -vmg compiler option [C++]
- vmg compiler option [C++]
- -vmb compiler option [C++]
- /vmb compiler option [C++]
- representation method compiler options [C++]
- /vmg compiler option [C++]
ms.assetid: ecdb391c-7dab-40b1-916b-673d10889fd4
ms.openlocfilehash: 19d183ef8d1dd152043d7249d907c9d5b48de230
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97254290"
---
# <a name="vmb-vmg-representation-method"></a>/vmb, /vmg (метод представления)

Выберите метод, используемый компилятором для представления указателей на члены класса.

Используйте **/VMB** , если вы всегда определяете класс перед объявлением указателя на член класса.

Используйте **/vmg** , чтобы объявить указатель на член класса перед определением класса. Это может возникнуть при определении членов в двух разных классах, ссылающихся друг на друга. Для таких взаимосвязанных классов на один класс необходимо ссылаться до его определения.

## <a name="syntax"></a>Синтаксис

```
/vmb
/vmg
```

## <a name="remarks"></a>Remarks

Для указания представления указателя можно также использовать ключевые слова [pointers_to_members](../../preprocessor/pointers-to-members.md) или [наследования](../../cpp/inheritance-keywords.md) в коде.

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
