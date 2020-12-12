---
description: Дополнительные сведения:/MERGE (объединение разделов)
title: /MERGE (Слияние разделов)
ms.date: 11/04/2016
f1_keywords:
- /merge
- VC.Project.VCLinkerTool.MergeSections
helpviewer_keywords:
- sections, combining
- /MERGE linker option
- sections, naming
- sections
- -MERGE linker option
- MERGE linker option
ms.assetid: 10fb20c2-0b3f-4c8d-98a8-f69aedf03d52
ms.openlocfilehash: 579e5432facd6deb8d2b26b997d9b61f167d2b3e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97199107"
---
# <a name="merge-combine-sections"></a>/MERGE (Слияние разделов)

```
/MERGE:from=to
```

## <a name="remarks"></a>Комментарии

Параметр/MERGE объединяет первый раздел (*из*) со вторым разделом (*to*), присваивая результирующему разделу *имя.* Например, `/merge:.rdata=.text`.

Если второй раздел не существует, LINK переименовывает раздел *с* *на*.

Параметр/MERGE полезен при создании VxD и переопределении имен разделов, созданных компилятором.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите папку **компоновщика**.

1. Перейдите на страницу свойств **Дополнительно** .

1. Измените свойство **Merge Sections** .

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

1. См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.MergeSections%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
