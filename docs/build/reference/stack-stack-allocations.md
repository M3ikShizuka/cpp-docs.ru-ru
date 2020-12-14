---
description: Дополнительные сведения о:/STACK (выделения стека)
title: Параметр /STACK (выделение памяти в стеке)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCLinkerTool.StackReserveSize
- VC.Project.VCLinkerTool.StackCommitSize
- /stack
helpviewer_keywords:
- STACK linker option
- -STACK linker option
- memory allocation, stack
- /STACK linker option
- stack, setting size
ms.assetid: 73283660-e4bd-47cc-b5ca-04c5d739034c
ms.openlocfilehash: 6e74b508d8cdb2340c73360bf35272d9113a0f75
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97224470"
---
# <a name="stack-stack-allocations"></a>Параметр /STACK (выделение памяти в стеке)

```
/STACK:reserve[,commit]
```

## <a name="remarks"></a>Комментарии

Параметр/STACK задает размер стека в байтах. Используйте этот параметр только при сборке exe.

`reserve`Значение определяет общее выделение стека в виртуальной памяти. Для компьютеров ARM, x86 и x64 размер стека по умолчанию составляет 1 МБ.

`commit` подлежит интерпретации операционной системы. В Windows Виндовсрт он указывает объем физической памяти, выделяемой за раз. Выделенная виртуальная память приводит к тому, что пространство резервируется в файле подкачки. Более высокое `commit` значение экономит время, когда приложению требуется больше пространства стека, но увеличивает требования к памяти и, возможно, время запуска. Для компьютеров ARM, x86 и x64 значение фиксации по умолчанию равно 4 КБ.

Укажите `reserve` значения и `commit` в десятичной или C-языковой нотации.

Другой способ задать размер стека — с помощью инструкции [STACKSIZE](stacksize.md) в файле определения модуля (DEF). **STACKSIZE** переопределяет параметр распределения стека (/stack), если указаны оба параметра. Размер стека можно изменить после сборки exe-файла с помощью средства [EDITBIN](editbin-reference.md) .

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите папку **Компоновщик** .

1. Выберите страницу свойств **системы** .

1. Измените одно из следующих свойств:

   - **Размер фиксации стека**

   - **Резервный размер стека**

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

1. См. описание свойств <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.StackCommitSize%2A> и <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.StackReserveSize%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
