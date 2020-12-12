---
description: Дополнительные сведения:/DLL (сборка библиотеки DLL)
title: /DLL (построение библиотеки DLL)
ms.date: 11/04/2016
f1_keywords:
- /dll
helpviewer_keywords:
- -DLL linker option
- /DLL linker option [C++]
- exporting DLLs [C++], specifying exports
- DLLs [C++], building
- DLL linker option [C++]
ms.assetid: c7685aec-31d0-490f-9503-fb5171a23609
ms.openlocfilehash: 42535fb15762e5c0f1691d5c28029c7368005f87
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97201408"
---
# <a name="dll-build-a-dll"></a>/DLL (построение библиотеки DLL)

```
/DLL
```

## <a name="remarks"></a>Комментарии

Параметр/DLL создает библиотеку DLL в качестве основного выходного файла. Библиотека DLL обычно содержит экспорты, которые могут использоваться другой программой. Существует три метода для указания экспортов, которые перечислены в рекомендуемом порядке использования:

1. [__declspec (dllexport)](../../cpp/dllexport-dllimport.md) в исходном коде

1. Инструкция [EXPORTS](exports.md) в DEF-файле

1. Спецификация [/Export](export-exports-a-function.md) в команде LINK

Программа может использовать более одного метода.

Другим способом построения библиотеки DLL является оператор **библиотечного** определения. Параметры/BASE и/DLL эквивалентны оператору **Library** .

Не указывайте этот параметр в среде разработки. Этот параметр предназначен только для использования в командной строке. Этот параметр задается при создании проекта библиотеки DLL с помощью мастера приложений.

Обратите внимание, что при создании библиотеки импорта на предварительном этапе перед созданием библиотеки DLL необходимо передать один и тот же набор объектных файлов при сборке DLL-файла, как было передано при построении библиотеки импорта.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Щелкните папку **Свойства конфигурации** .

1. Перейдите на страницу свойств **Общие** .

1. Измените свойство **тип конфигурации** .

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCPropertySheet.ConfigurationType%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
