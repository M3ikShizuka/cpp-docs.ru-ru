---
description: Дополнительные сведения о:/GR (включение сведений о типе Run-Time)
title: /GR (Предоставление информации о типах во время выполнения)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCCLWCECompilerTool.RuntimeTypeInfo
- VC.Project.VCCLCompilerTool.RuntimeTypeInfo
helpviewer_keywords:
- -Gr compiler option [C++]
- Gr compiler option [C++]
- RTTI compiler option
- /Gr compiler option [C++]
- enable run-time type information compiler option [C++]
ms.assetid: d1f9f850-dcec-49fd-96ef-e72d01148906
ms.openlocfilehash: 61b1a595999e5e00bf6b28c75be2de03467cc4ed
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97200171"
---
# <a name="gr-enable-run-time-type-information"></a>/GR (Предоставление информации о типах во время выполнения)

Добавляет код для проверки типов объектов во время выполнения.

## <a name="syntax"></a>Синтаксис

```
/GR[-]
```

## <a name="remarks"></a>Remarks

Если параметр **/GR** имеет значение ON, компилятор определяет `_CPPRTTI` макрос препроцессора. По умолчанию **/GR** имеет значение ON. **/GR-** отключает сведения о типах времени выполнения.

Используйте **/GR** , если компилятор не может статически разрешить тип объекта в коде. Обычно требуется параметр **/GR** , если в коде используется [оператор dynamic_cast](../../cpp/dynamic-cast-operator.md) или [typeid](../../cpp/typeid-operator.md). Однако **/GR** увеличивает размер разделов RDATA изображения. Если код не использует **`dynamic_cast`** или **`typeid`** , **/GR-** может создать меньшее изображение.

Дополнительные сведения о проверке типов во время выполнения см. в *справочнике по языку C++* в разделе [сведения о типах времени выполнения](../../cpp/run-time-type-information.md) .

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Откройте папку **C/C++** .

1. Перейдите на страницу свойств **язык** .

1. Измените свойство **включить сведения о типе Run-Time** .

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.RuntimeTypeInfo%2A>.

## <a name="see-also"></a>См. также раздел

[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)
