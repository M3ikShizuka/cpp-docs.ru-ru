---
description: 'Дополнительные сведения о: Колеконтролмодуле Class'
title: Класс Колеконтролмодуле
ms.date: 11/04/2016
f1_keywords:
- OleControlModule
helpviewer_keywords:
- OLE control modules [MFC]
- MFC ActiveX controls [MFC], OLE control modules
- COleControlModule class [MFC]
- control modules [MFC]
ms.assetid: 0721724d-d4af-4eda-ad34-5a2b27810dd4
ms.openlocfilehash: f88296b7c0e897f82227343b31ca2f639902256e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97227485"
---
# <a name="colecontrolmodule-class"></a>Класс Колеконтролмодуле

Базовый класс, от которого необходимо наследовать объект модуля элемента управления OLE.

## <a name="syntax"></a>Синтаксис

```
class COleControlModule : public CWinApp
```

## <a name="remarks"></a>Remarks

Этот класс предоставляет функции элементов для инициализации модуля управления. Каждый модуль управления OLE, использующий классы Microsoft Foundation, может содержать только один объект, производный от `COleControlModule` . Этот объект создается при создании других глобальных объектов C++. Объявите производный `COleControlModule` объект на глобальном уровне.

Дополнительные сведения об использовании `COleControlModule` класса см. в разделе класс [CWinApp](../../mfc/reference/cwinapp-class.md) и [элементы управления ActiveX](../../mfc/mfc-activex-controls.md)статьи.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWinThread](../../mfc/reference/cwinthread-class.md)

[CWinApp](../../mfc/reference/cwinapp-class.md)

`COleControlModule`

## <a name="requirements"></a>Требования

**Заголовок:** afxctl. h

## <a name="see-also"></a>См. также раздел

[Пример ТЕССЕЛП для MFC](../../overview/visual-cpp-samples.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)
