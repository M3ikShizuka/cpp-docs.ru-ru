---
description: Дополнительные сведения о:/APPCONTAINER (Microsoft Store приложение)
title: /APPCONTAINER (приложение UWP/Microsoft Store)
ms.date: 11/04/2016
ms.assetid: 9a432db5-7640-460b-ab18-6f61fa7daf6f
ms.openlocfilehash: 4cb78c85aa59ebd7fc0eb82af9497606bc3c431c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97179581"
---
# <a name="appcontainer-microsoft-store-app"></a>/APPCONTAINER (Microsoft Store приложение)

Указывает, создает ли компоновщик исполняемый образ, который должен выполняться в контейнере приложения.

## <a name="syntax"></a>Синтаксис

```
/APPCONTAINER[:NO]
```

## <a name="remarks"></a>Remarks

По умолчанию/APPCONTAINER отключен.

Этот параметр изменяет исполняемый файл, чтобы указать, должно ли приложение запускаться в среде изоляции процессов appcontainer. Укажите/APPCONTAINER для приложения, которое должно выполняться в среде APPCONTAINER (например, универсальная платформа Windows (UWP) или Windows Phone 8. x). (Параметр задается автоматически в Visual Studio при создании универсального приложения Windows из шаблона.) Для классического приложения укажите/APPCONTAINER: NO или просто опустите параметр.

Параметр/APPCONTAINER появился в Windows 8.

### <a name="to-set-this-linker-option-in-visual-studio"></a>Настройка этого параметра компоновщика в Visual Studio

1. Откройте диалоговое окно **Окна свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойств сборки в Visual Studio](../working-with-project-properties.md).

1. Разверните узел **Свойства конфигурации**.

1. Разверните узел **Компоновщик**.

1. Выберите страницу свойств **Командная строка** .

1. В окне **Дополнительные параметры** введите `/APPCONTAINER` или `/APPCONTAINER:NO` .

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
