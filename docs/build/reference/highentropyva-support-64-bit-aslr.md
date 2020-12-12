---
description: Дополнительные сведения о:/HIGHENTROPYVA (поддержка 64-разрядного ASLR)
title: /HIGHENTROPYVA (поддержка 64-разрядной рандомизации ASLR)
ms.date: 06/12/2018
ms.assetid: fe35f9f7-d28e-4694-9aeb-a79db06168e0
ms.openlocfilehash: aed5d5eea2d3351d4eff88a58818a953563ba0e5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97191554"
---
# <a name="highentropyva-support-64-bit-aslr"></a>/HIGHENTROPYVA (поддержка 64-разрядной рандомизации ASLR)

Указывает, поддерживает ли исполняемый образ 64-разрядную технологию ASLR с высокой энтропией.

## <a name="syntax"></a>Синтаксис

> **`/HIGHENTROPYVA`**[**`:NO`**]

## <a name="remarks"></a>Комментарии

**`/HIGHENTROPYVA`** изменяет заголовок файла *исполняемого образа* (например, *`.dll`* *`.exe`* файла или), чтобы указать, может ли ASLR использовать все 64-битные адресные пространства.  Чтобы получить результат, задайте параметр как для исполняемого файла, так и для всех модулей, от которых он зависит. Затем операционная система, которая поддерживает 64-разрядный ASLR, может перераспределять сегменты исполняемого образа во время загрузки с помощью 64-битных случайных виртуальных адресов. Благодаря обширному адресному пространству злоумышленнику будет труднее догадаться о расположении определенной области в памяти.

По умолчанию **`/HIGHENTROPYVA`** включено для 64-разрядных исполняемых образов. Для этого параметра требуется [`/LARGEADDRESSAWARE`](largeaddressaware-handle-large-addresses.md) , который также включен по умолчанию для 64-разрядных изображений. **`/HIGHENTROPYVA`** не применяется к 32-разрядным исполняемым образам, где компоновщик игнорирует параметр. Чтобы явно отключить этот параметр, используйте **`/HIGHENTROPYVA:NO`** .

Для **`/HIGHENTROPYVA`** , чтобы обеспечить воздействие на время загрузки, [`/DYNAMICBASE`](dynamicbase-use-address-space-layout-randomization.md) также необходимо включить. **`/DYNAMICBASE`** параметр включен по умолчанию и необходим для включения ASLR в Windows Vista и более поздних операционных системах. В более ранних версиях Windows этот флаг игнорируется.

### <a name="to-set-this-linker-option-in-visual-studio"></a>Настройка этого параметра компоновщика в Visual Studio

1. Откройте диалоговое окно **Окна свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойств сборки в Visual Studio](../working-with-project-properties.md).

1. Перейдите на страницу свойств **Свойства конфигурации** > **Компоновщик** > **Командная строка**.

1. В окне **Дополнительные параметры** введите `/HIGHENTROPYVA` или `/HIGHENTROPYVA:NO` .

## <a name="see-also"></a>См. также раздел

- [Справочник по компоновщику MSVC](linking.md)
- [Параметры компоновщика MSVC](linker-options.md)
- [`/DYNAMICBASE`](dynamicbase-use-address-space-layout-randomization.md)
- [`/LARGEADDRESSAWARE`](largeaddressaware-handle-large-addresses.md)
- [Средства защиты программного обеспечения Windows ISV](/previous-versions/bb430720(v=msdn.10))
