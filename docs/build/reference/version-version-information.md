---
description: Дополнительные сведения о:/VERSION (сведения о версии)
title: /VERSION (Сведения о версии)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCLinkerTool.Version
- /version
helpviewer_keywords:
- -VERSION linker option
- Version Information linker option
- version numbers, specifying in .exe
- /VERSION linker option
- VERSION linker option
ms.assetid: b86d0e86-dca6-4316-aee2-d863ccb9f223
ms.openlocfilehash: 7c6a27e4829c4acf66db2887e01a147aceb1c5d3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97176370"
---
# <a name="version-version-information"></a>/VERSION (Сведения о версии)

```
/VERSION:major[.minor]
```

## <a name="arguments"></a>Аргументы

*основной* и *дополнительный*<br/>
Номер версии, который вы хотите использовать в заголовке exe-или DLL-файла.

## <a name="remarks"></a>Комментарии

Параметр/VERSION указывает компоновщику разместить номер версии в заголовке файла exe или DLL. Используйте параметр DUMPBIN [/headers](headers.md) , чтобы просмотреть поле версия изображения необязательных значений заголовка, чтобы увидеть результат/версион..

*Основной* и *дополнительный* аргументы — десятичные числа в диапазоне от 0 до 65 535. Значение по умолчанию — версия 0,0.

Сведения, указанные в параметре/VERSION, не влияют на сведения о версии, отображаемые для приложения при просмотре его свойств в проводнике. Эти сведения о версии берутся из файла ресурсов, который используется для сборки приложения. Дополнительные сведения см. в разделе [Редактор сведений о версии](../../windows/version-information-editor.md) .

Другим способом вставки номера версии является оператор [Version](version-c-cpp.md) -Definition.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите папку **компоновщика**.

1. Перейдите на страницу свойств **Общие** .

1. Измените свойство **Version** .

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.Version%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
