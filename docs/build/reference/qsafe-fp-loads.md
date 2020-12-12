---
description: Дополнительные сведения о:/Qsafe_fp_loads
title: /Qsafe_fp_loads
ms.date: 01/24/2018
ms.openlocfilehash: e569b308d2da982c72775699ff2149daa45a8f2a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97225522"
---
# <a name="qsafe_fp_loads"></a>/Qsafe_fp_loads

Требует целочисленных инструкций перемещения для значений с плавающей запятой и отключает определенные оптимизации нагрузки с плавающей запятой.

## <a name="syntax"></a>Синтаксис

> **/Qsafe_fp_loads**

## <a name="remarks"></a>Комментарии

**/Qsafe_fp_loads** доступен только в компиляторах, предназначенных для платформы x86; он недоступен в компиляторах, предназначенных для x64 или ARM.

**/Qsafe_fp_loads** заставляет компилятор использовать целочисленные инструкции перемещения вместо инструкций перемещения с плавающей точкой для перемещения данных между регистрами памяти и MMX. Этот параметр также отключает оптимизацию регистрации загрузки для значений с плавающей запятой, которые могут быть загружены в несколько путей управления, если значение может вызвать исключение при загрузке, например значение NaN.

Этот параметр переопределяется с помощью [/FP: except](fp-specify-floating-point-behavior.md). **/Qsafe_fp_loads** указывает подмножество поведения компилятора, заданное параметром **/FP: except**.

**/Qsafe_fp_loads** несовместим с [параметрами/CLR](clr-common-language-runtime-compilation.md) и [/FP: Fast](fp-specify-floating-point-behavior.md). Дополнительные сведения о параметрах компилятора с плавающей точкой см. в разделе [/FP (определение поведения Floating-Point)](fp-specify-floating-point-behavior.md).

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите страницу свойств **Свойства конфигурации**  >  **C/C++**  >  **Командная строка** .

1. В поле **Дополнительные параметры** введите параметр компилятора. Чтобы применить изменение, нажмите кнопку **ОК**.

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalOptions%2A>.

## <a name="see-also"></a>См. также раздел

[Параметры/q (низкоуровневые операции)](q-options-low-level-operations.md)<br/>
[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)
