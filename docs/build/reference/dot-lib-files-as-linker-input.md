---
description: Дополнительные сведения:. Lib Files в качестве входных файлов компоновщика
title: LIB-файлы в качестве входных файлов компоновщика
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCLinkerTool.AdditionalDependencies
helpviewer_keywords:
- OMF libraries
- linking [C++], OMF libraries
- import libraries, linker files
- libraries [C++], .lib files as linker input
- COFF files, import libraries
- default libraries [C++], linker output
- default libraries [C++]
- defaults [C++], libraries
- .lib files
ms.assetid: dc5d2b1c-2487-41fa-aa71-ad1e0647958b
ms.openlocfilehash: f4a3b6c6487947772fb72135fb26f67857f0937e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97201265"
---
# <a name="lib-files-as-linker-input"></a>LIB-файлы в качестве входных файлов компоновщика

ССЫЛКА принимает стандартные библиотеки COFF и библиотеки импорта COFF, обе из которых обычно имеют расширение LIB. Стандартные библиотеки содержат объекты и создаются средством LIB. Библиотеки импорта содержат сведения о экспортах в других программах и создаются по ссылке при сборке программы, содержащей EXPORTS или с помощью средства LIB. Сведения об использовании LIB для создания стандартных или импортируемых библиотек см. в [справочнике по lib](lib-reference.md). Дополнительные сведения об использовании ссылки для создания библиотеки импорта см. в разделе параметр [/DLL](dll-build-a-dll.md) .

Библиотека указывается для СВЯЗЫВАНИЯ в качестве аргумента имени файла или библиотеки по умолчанию. LINK разрешает внешние ссылки путем поиска в первую очередь в библиотеках, указанных в командной строке, затем в библиотеках по умолчанию, заданных параметром [параметр/DEFAULTLIB](defaultlib-specify-default-library.md) , а затем в библиотеках по умолчанию с именами в OBJ-файлах. Если путь указан с именем библиотеки, LINK ищет библиотеку в этом каталоге. Если путь не указан, ссылка сначала ищется в каталоге, из которого выполняется ссылка, а затем во всех каталогах, указанных в переменной среды LIB.

## <a name="to-add-lib-files-as-linker-input-in-the-development-environment"></a>Добавление LIB файлов в качестве входных данных компоновщика в среде разработки

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите страницу свойств **входные данные** в папке **Компоновщик** .

1. Измените свойство **Дополнительные зависимости** , чтобы добавить lib файлы.

## <a name="to-programmatically-add-lib-files-as-linker-input"></a>Программное добавление LIB файлов в качестве входных данных компоновщика

- См. [аддитионалдепенденЦиес](/dotnet/api/microsoft.visualstudio.vcprojectengine.vclinkertool.additionaldependencies).

## <a name="example"></a>Пример

В следующем примере показано, как создать и использовать LIB-файл. Сначала создайте LIB-файл:

```cpp
// lib_link_input_1.cpp
// compile by using: cl /LD lib_link_input_1.cpp
__declspec(dllexport) int Test() {
   return 213;
}
```

Затем скомпилируйте этот пример с помощью только что созданного файла. lib:

```cpp
// lib_link_input_2.cpp
// compile by using: cl /EHsc lib_link_input_1.lib lib_link_input_2.cpp
__declspec(dllimport) int Test();
#include <iostream>
int main() {
   std::cout << Test() << std::endl;
}
```

```Output
213
```

## <a name="see-also"></a>См. также раздел

[Входные файлы ссылок](link-input-files.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
