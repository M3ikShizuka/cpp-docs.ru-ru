---
description: Дополнительные сведения о:/CGTHREADS (потоки компилятора)
title: /CGTHREADS (потоки компилятора)
ms.date: 11/04/2016
helpviewer_keywords:
- /CGTHREADS linker option
- -CGTHREADS linker option
- CGTHREADS linker option
ms.assetid: 4b52cfdb-3702-470b-9580-fabeb1417488
ms.openlocfilehash: 71c5031c7013ec6f8ddad153d9cc16bee2004751
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97179256"
---
# <a name="cgthreads-compiler-threads"></a>/CGTHREADS (потоки компилятора)

Задает число потоков cl.exe, используемых для оптимизации и создания кода, если задано создание кода во время компоновки.

## <a name="syntax"></a>Синтаксис

```
/CGTHREADS:[1-8]
```

## <a name="arguments"></a>Аргументы

*number*<br/>
Максимальное число потоков, используемых cl.exe, — в диапазоне от 1 до 8.

## <a name="remarks"></a>Комментарии

Параметр **/CGTHREADS** указывает максимальное число потоков, используемых cl.exe параллельно для этапов оптимизации и создания кода компиляции, когда задано создание кода во время компоновки ([/LTCG](ltcg-link-time-code-generation.md)). По умолчанию cl.exe использует четыре потока, как если бы были указаны **/CGTHREADS: 4** . Если доступно больше ядер процессора, увеличение значения `number` может ускорить сборку.

Для сборки можно указать несколько уровней параллелизма. Параметр msbuild.exe **/maxcpucount** указывает количество процессов MSBuild, которые могут выполняться параллельно. Флаг компилятора [/MP (сборка с несколькими процессами)](mp-build-with-multiple-processes.md) указывает количество процессов cl.exe, одновременно выполняющих компиляцию исходных файлов. Параметр компилятора [/cgthreads](cgthreads-code-generation-threads.md) указывает количество потоков, используемых каждым процессом cl.exe. Так как число потоков, одновременно выполняемых процессором, не может превышать число ядер процессора, указывать более высокие значения для всех этих параметров бессмысленно. Более того, это может иметь обратный эффект. Дополнительные сведения о параллельной сборке проектов см. [в разделе параллельное построение нескольких проектов](/visualstudio/msbuild/building-multiple-projects-in-parallel-with-msbuild).

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите **Свойства конфигурации**, папка **компоновщика** .

1. Выберите страницу свойств **Командная строка** .

1. Измените свойство **Дополнительные параметры** , включив **/CGTHREADS:** `number` , где `number` — это значение от 1 до 8, а затем нажмите кнопку **ОК**.

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.AdditionalOptions%2A>.

## <a name="see-also"></a>См. также раздел

[Параметры компоновщика MSVC](linker-options.md)<br/>
[Справочник по компоновщику MSVC](linking.md)
