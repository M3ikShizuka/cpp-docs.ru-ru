---
description: 'Дополнительные сведения о: Общие сведения о ATL'
title: Введение в ATL
ms.custom: index-page
ms.date: 11/04/2016
helpviewer_keywords:
- COM objects, creating in ATL
- ATL
ms.assetid: 77f565e8-c4ec-4a80-af4b-7278fcfe5c98
ms.openlocfilehash: 43a99dbd784b33f0595cccfa6014bdda17a2bdd1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97147710"
---
# <a name="introduction-to-atl"></a>Введение в ATL

ATL — это активная библиотека шаблонов, набор классов C++ на основе шаблонов, с помощью которых можно легко создавать небольшие, быстрые объекты модели компонентов (COM). Она имеет специальную поддержку ключевых возможностей COM, включая следующие акции: стандартные реализации [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown), [IClassFactory](/windows/win32/api/unknwnbase/nn-unknwnbase-iclassfactory), [IClassFactory2](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2)и `IDispatch` ; сдвоенные интерфейсы перечислителя com, точки соединения, разрывы, а также элементы управления ActiveX.

Код ATL можно использовать для создания однопотоковых объектов, объектов модели-контейнера, объектов модели свободных потоков, а также для объектов модели с произвольным потоком и потоковым контейнером.

В этом разделе рассматриваются следующие темы:

- Отличия [библиотеки шаблонов](../atl/using-a-template-library.md) от стандартной библиотеки.

- Что вы [можете и не можете делать с помощью ATL](../atl/scope-of-atl.md).

- [Рекомендации по выбору между ATL и MFC](../atl/recommendations-for-choosing-between-atl-and-mfc.md).

## <a name="see-also"></a>См. также раздел

[Введение в модель COM и ATL](../atl/introduction-to-com-and-atl.md)
