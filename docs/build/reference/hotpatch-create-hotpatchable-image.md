---
description: Дополнительные сведения о:/hotpatch (создание образа допускающего оперативное обновление)
title: /hotpatch (Создать образ с обновлениями)
ms.date: 11/12/2018
f1_keywords:
- /hotpatch
- VC.Project.VCCLCompilerTool.CreateHotpatchableImage
helpviewer_keywords:
- hot patching
- -hotpatch compiler option [C++]
- /hotpatch compiler option [C++]
- hotpatching
ms.assetid: aad539b6-c053-4c78-8682-853d98327798
ms.openlocfilehash: 2fc5fe629afcb1e721943b852c6f92351900ab7e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97199874"
---
# <a name="hotpatch-create-hotpatchable-image"></a>/hotpatch (Создать образ с обновлениями)

Готовит образ к оперативному исправлению.

## <a name="syntax"></a>Синтаксис

```
/hotpatch
```

## <a name="remarks"></a>Remarks

Если в компиляции используется **/hotpatch** , компилятор гарантирует, что первая инструкция каждой функции будет иметь по крайней мере два байта, что требуется для горячего исправления.

Чтобы завершить подготовку к созданию образа допускающего оперативное обновление, после использования **/hotpatch** для компиляции необходимо использовать [/FUNCTIONPADMIN (создать допускающего оперативное обновление образ)](functionpadmin-create-hotpatchable-image.md) для связи. При компиляции и связывании изображения с помощью одного вызова cl.exe **/hotpatch** подразумевает **/FUNCTIONPADMIN**.

Поскольку инструкции всегда имеют размер 2 байта или больше в архитектуре ARM, и поскольку компиляция x64 всегда обрабатывается так, как если бы **/hotpatch** был указан, не нужно указывать **/hotpatch** при компиляции для этих целевых объектов. Однако по-прежнему необходимо использовать **/FUNCTIONPADMIN** для создания образов допускающего оперативное обновление для них. Параметр компилятора **/hotpatch** влияет только на компиляцию x86.

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите папку **C/C++** .

1. Выберите страницу свойств **Командная строка** .

1. Добавьте параметр компилятора в поле **Дополнительные параметры** .

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalOptions%2A>.

## <a name="see-also"></a>См. также раздел

[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)
