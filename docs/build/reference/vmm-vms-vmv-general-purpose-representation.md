---
description: Дополнительные сведения о:/VMM,/VMS,/vmv (представление общего назначения)
title: /VMM,-VMS,-vmv (представление общего назначения)
ms.date: 11/04/2016
f1_keywords:
- /vms
- /vmm
- /vmv
helpviewer_keywords:
- Virtual Inheritance compiler option
- general purpose representation compiler options
- vms compiler option [C++]
- vmm compiler option [C++]
- /vmm compiler option [C++]
- -vmm compiler option [C++]
- -vms compiler option [C++]
- /vms compiler option [C++]
- vmv compiler option [C++]
- /vmv compiler option [C++]
- Single Inheritance compiler option
- -vmv compiler option [C++]
ms.assetid: 0fcd7ae0-3031-4c62-a2a8-e154c8685dae
ms.openlocfilehash: 8c5761a2f51ec9860a4afeb7d4aacbf7f882b3f1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97257229"
---
# <a name="vmm-vms-vmv-general-purpose-representation"></a>/vmm, /vms и /vmv (представление общего назначения)

Используется, если в качестве [метода представления](vmb-vmg-representation-method.md)выбран метод [/VMB,/vmg (представление)](vmb-vmg-representation-method.md) . Эти параметры указывают модель наследования определения класса, который еще не обнаружен.

## <a name="syntax"></a>Синтаксис

```
/vmm
/vms
/vmv
```

## <a name="remarks"></a>Remarks

Данные параметры описаны в следующей таблице.

|Параметр|Описание|
|------------|-----------------|
|**/VMM**|Задает наиболее общее представление указателя на член класса, который использует множественное наследование.<br /><br /> Соответствующее [ключевое слово и аргумент наследования](../../cpp/inheritance-keywords.md) для [#pragma pointers_to_members](../../preprocessor/pointers-to-members.md) **multiple_inheritance**.<br /><br /> Это представление больше, чем требуется для одиночного наследования.<br /><br /> Если модель наследования определения класса, для которой объявлен указатель на член, является виртуальной, компилятор выдает ошибку.|
|**/VMS**|Задает наиболее общее представление указателя на член класса, который не использует наследование или одиночное наследование.<br /><br /> Соответствующее [ключевое слово и аргумент наследования](../../cpp/inheritance-keywords.md) для [#pragma pointers_to_members](../../preprocessor/pointers-to-members.md) **single_inheritance**.<br /><br /> Это наименьшее возможное представление указателя на член класса.<br /><br /> Если модель наследования определения класса, для которой объявлен указатель на член, является несколько или виртуальная, компилятор выдает ошибку.|
|**/vmv**|Задает наиболее общее представление указателя на член класса в качестве одного из них, использующего виртуальное наследование. Он никогда не вызывает ошибку и является значением по умолчанию.<br /><br /> Соответствующее [ключевое слово и аргумент наследования](../../cpp/inheritance-keywords.md) для [#pragma pointers_to_members](../../preprocessor/pointers-to-members.md) **virtual_inheritance**.<br /><br /> Для этого параметра требуется больший указатель и дополнительный код для интерпретации указателя, а не других параметров.|

При указании одного из этих параметров модели наследования эта модель используется для всех указателей на члены класса, независимо от типа наследования или от того, объявлен ли указатель до или после класса. Таким образом, если всегда используются классы с одним наследованием, размер кода можно сократить путем компиляции с помощью **/VMS**; Однако если вы хотите использовать наиболее общий вариант (с учетом наибольшего представления данных), скомпилируйте его с помощью **/vmv**.

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Откройте папку **C/C++** .

1. Выберите страницу свойств **Командная строка** .

1. Введите параметр компилятора в поле **Дополнительные параметры** .

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalOptions%2A>.

## <a name="see-also"></a>См. также раздел

[/VMB,/vmg (метод представления)](vmb-vmg-representation-method.md)<br/>
[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)
