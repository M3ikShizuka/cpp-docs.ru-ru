---
description: Дополнительные сведения о:/Qfast_transcendentals (принудительная Быстрая трансцендентные функции)
title: /Qfast_transcendentals (принудительное использование быстрых трансцендентных функций)
ms.date: 11/04/2016
f1_keywords:
- /Qfast_transcendentals
helpviewer_keywords:
- /Qfast_transcendentals
- Force Fast Transcendentals
ms.assetid: 4de24bd1-38e6-49d4-9a05-04c9937d24ac
ms.openlocfilehash: 7701925aa7df33107b0829ade1c0c711eda14c08
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97225665"
---
# <a name="qfast_transcendentals-force-fast-transcendentals"></a>/Qfast_transcendentals (принудительное использование быстрых трансцендентных функций)

Создает встроенный код для функций трансцендентных.

## <a name="syntax"></a>Синтаксис

```
/Qfast_transcendentals
```

## <a name="remarks"></a>Remarks

Этот параметр компилятора принудительно преобразует функции трансцендентных в встроенный код для повышения скорости выполнения. Этот параметр действует только в том случае, если он связан с **/FP: except** или **/FP: точным**. Создание встроенного кода для функций трансцендентных уже является поведением по умолчанию в разделе **/FP: Fast**.

Этот параметр несовместим с **/FP: Option**. Дополнительные сведения о параметрах компилятора с плавающей точкой см. в разделе [/FP (Указание поведения Floating-Point)](fp-specify-floating-point-behavior.md) .

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Откройте папку **C/C++** .

1. Выберите страницу свойств **Командная строка** .

1. Введите параметр компилятора в поле **Дополнительные параметры** .

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalOptions%2A>.

## <a name="see-also"></a>См. также раздел

[Параметры/q (низкоуровневые операции)](q-options-low-level-operations.md)<br/>
[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)
