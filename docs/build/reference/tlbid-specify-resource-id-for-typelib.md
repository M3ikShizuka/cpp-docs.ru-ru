---
description: Дополнительные сведения о:/TLBID (указание идентификатора ресурса для TypeLib)
title: /TLBID (указать идентификатор ресурса для TypeLib)
ms.date: 11/04/2016
f1_keywords:
- /tlbid
- VC.Project.VCLinkerTool.TypeLibraryResourceID
helpviewer_keywords:
- tlb files, specifying resource ID
- -TLBID linker option
- .tlb files, specifying resource ID
- /TLBID linker option
- TLBID linker option
- type libraries, specifying resource ID
ms.assetid: 434b28a2-4656-4d52-ac82-8b18bf486fb2
ms.openlocfilehash: 4958229cbebe988867c5419d7953b6ffd968e45f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97230020"
---
# <a name="tlbid-specify-resource-id-for-typelib"></a>/TLBID (указать идентификатор ресурса для TypeLib)

```
/TLBID:id
```

## <a name="arguments"></a>Аргументы

*id*<br/>
Заданное пользователем значение для библиотеки типов, созданной компоновщиком. Он переопределяет идентификатор ресурса по умолчанию 1.

## <a name="remarks"></a>Комментарии

При компиляции программы, использующей атрибуты, компоновщик создаст библиотеку типов. Компоновщик присвоит библиотеке типов идентификатор ресурса 1.

Если этот идентификатор ресурса конфликтует с одним из существующих ресурсов, можно указать другой идентификатор с помощью/ТЛБИД.. Диапазон значений, в который можно передать значение, `id` — от 1 до 65535.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите папку **компоновщика**.

1. Щелкните страницу свойств **встроенного IDL** .

1. Измените свойство **идентификатора ресурса TypeLib** .

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

1. См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.TypeLibraryResourceID%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
