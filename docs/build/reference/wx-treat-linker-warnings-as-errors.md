---
description: Дополнительные сведения:/WX (Обработка предупреждений компоновщика как ошибок)
title: /WX (Обрабатывать предупреждения компоновщика как ошибки)
ms.date: 11/04/2016
f1_keywords:
- /WX
helpviewer_keywords:
- /WX linker option
- -WX linker option
- WX linker option
ms.assetid: e4ba97c7-93f7-43ae-a4bb-d866790926c9
ms.openlocfilehash: 965c48ff9c9f975350f3c1e54d8090823be8fd2e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97261038"
---
# <a name="wx-treat-linker-warnings-as-errors"></a>/WX (Обрабатывать предупреждения компоновщика как ошибки)

```
/WX[:NO]
```

## <a name="remarks"></a>Комментарии

Параметр/WX приводит к тому, что выходной файл не создается, если компоновщик создает предупреждение.

Это похоже на параметр **/WX** для компилятора (Дополнительные сведения см. в разделе [/w,/W0,/W1,/W2,/W3,/W4,/W1,/W2,/W3,/W4,/Wall,/WD,/We,/WO,/WV,/WX (уровень предупреждений)](compiler-option-warning-level.md) . Однако при указании параметра **/WX** для компиляции не подразумевается, что параметр **/WX** также будет действовать для фазы компоновки. для каждого средства необходимо явно указать параметр **/WX** .

По умолчанию параметр **/WX** не действует. Чтобы обрабатывать предупреждения компоновщика как ошибки, укажите **/WX**. **/WX: No** не совпадает с указанием **/WX**.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите папку **компоновщика**.

1. Выберите страницу свойств **Командная строка** .

1. Введите параметр в поле **Дополнительные параметры** .

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

1. См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalOptions%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
