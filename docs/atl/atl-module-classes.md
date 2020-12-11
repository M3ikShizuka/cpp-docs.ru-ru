---
description: Дополнительные сведения см. в статье классы модулей ATL.
title: Модульные классы ATL
ms.date: 11/04/2016
helpviewer_keywords:
- CComModule class, what's changed
- ATL, module classes
- module classes
ms.assetid: fd75382d-c955-46ba-a38e-37728b7fa00f
ms.openlocfilehash: 16c38a6a38f4179e5846a445bd9573e7dc4500f5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97163305"
---
# <a name="atl-module-classes"></a>Модульные классы ATL

В этом разделе обсуждаются классы модулей, которые появились в ATL 7,0.

## <a name="ccommodule-replacement-classes"></a>Классы для замены CComModule

Используются более ранние версии ATL `CComModule` . В ATL 7,0 `CComModule` функциональные возможности заменяются несколькими классами:

- [Катлбасемодуле](../atl/reference/catlbasemodule-class.md) Содержит сведения, необходимые большинству приложений, использующих библиотеку ATL. Содержит значение HINSTANCE модуля и экземпляра ресурса.

- [Катлкоммодуле](../atl/reference/catlcommodule-class.md) Содержит сведения, необходимые для классов COM в ATL.

- [Катлвинмодуле](../atl/reference/catlwinmodule-class.md) Содержит сведения, необходимые классам окон в библиотеке ATL.

- [Катлдебугинтерфацесмодуле](../atl/reference/catldebuginterfacesmodule-class.md) Содержит поддержку для отладки интерфейса.

- [Катлмодуле](../atl/reference/catlmodule-class.md) Следующие `CAtlModule` классы, производные от класса, настраиваются для хранения сведений, необходимых для конкретного типа приложения. Большинство членов этих классов можно переопределить:

  - [CAtlDllModuleT](../atl/reference/catldllmodulet-class.md) Используется в приложениях DLL. Предоставляет код для стандартных операций экспорта.

  - [CAtlExeModuleT](../atl/reference/catlexemodulet-class.md) Используется в приложениях EXE. Предоставляет код, необходимый для исполняемого файла.

  - [Функция CAtlServiceModuleT](../atl/reference/catlservicemodulet-class.md) Предоставляет поддержку для создания служб Windows NT и Windows 2000.

`CComModule` по-прежнему доступен для обеспечения обратной совместимости.

## <a name="reasons-for-distributing-ccommodule-functionality"></a>Причины распространения функций CComModule

Функциональные возможности `CComModule` распределены по нескольким новым классам по следующим причинам.

- Обеспечьте `CComModule` детальную функциональность.

   Поддержка COM, окон, отладки интерфейса и функций, зависящих от приложения (DLL или EXE), теперь реализована в отдельных классах.

- Автоматически объявлять глобальный экземпляр каждого из этих модулей.

   Глобальный экземпляр требуемых классов модулей связан с проектом.

- Удалите необходимость вызова методов init и Term.

   Методы init и Term были перемещены в конструкторы и деструкторы для классов модулей. больше не нужно вызывать init и Term.

## <a name="see-also"></a>См. также раздел

[Основные понятия](../atl/active-template-library-atl-concepts.md)<br/>
[Общие сведения о классах](../atl/atl-class-overview.md)
