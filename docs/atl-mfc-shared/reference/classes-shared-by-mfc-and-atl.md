---
description: Дополнительные сведения о классах, совместно используемых MFC и ATL.
title: Общие классы MFC и ATL
ms.date: 11/04/2016
helpviewer_keywords:
- shared classes, classes
ms.assetid: ca8b4b6b-744d-430b-b31f-d5b2f17bf210
ms.openlocfilehash: df196f92b7b16742545a7d82320ef4fe8da77fe2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97166789"
---
# <a name="classes-shared-by-mfc-and-atl"></a>Общие классы MFC и ATL

В следующей таблице перечислены классы, общие для MFC и ATL.

|Класс|Описание|Файл заголовка|
|-----------|-----------------|-----------------|
|[кфилетиме](../../atl-mfc-shared/reference/cfiletime-class.md)|Предоставляет методы для управления значениями даты и времени, связанными с файлом.|атлтиме. h|
|[кфилетимеспан](../../atl-mfc-shared/reference/cfiletimespan-class.md)|Предоставляет методы для управления относительными значениями даты и времени, связанными с файлом.|атлтиме. h|
|[CFixedStringT](../../atl-mfc-shared/reference/cfixedstringt-class.md)|Представляет строковый объект с фиксированным буфером символов.|CStringT. h|
|[CImage](../../atl-mfc-shared/reference/cimage-class.md)|Обеспечивает улучшенную поддержку точечных рисунков, включая возможность загрузки и сохранения изображений в форматах JPEG, GIF, BMP и PNG.|атлимаже. h|
|[COleDateTime](../../atl-mfc-shared/reference/coledatetime-class.md)|Инкапсулирует тип данных DATE, используемый в OLE Automation.|atlcomtime. h|
|[коледатетимеспан](../../atl-mfc-shared/reference/coledatetimespan-class.md)|Представляет относительное время, интервал времени.|atlcomtime. h|
|[CPoint](../../atl-mfc-shared/reference/cpoint-class.md)|Класс, похожий на структуру [точек](/windows/win32/api/windef/ns-windef-point) Windows, который также включает функции-члены для работы со `CPoint` `POINT` структурами и.|атлтипес. h|
|[CRect](../../atl-mfc-shared/reference/crect-class.md)|Класс, аналогичный структуре [прямоугольника](/windows/win32/api/windef/ns-windef-rect) Windows, который также включает функции-члены для работы с `CRect` объектами и `RECT` структурами Windows.|атлтипес. h|
|[ксимплестрингт](../../atl-mfc-shared/reference/csimplestringt-class.md)|Представляет объект `CSimpleStringT`.|атлсимпстр. h|
|[CSize](../../atl-mfc-shared/reference/csize-class.md)|Класс, аналогичный структуре [размера](/windows/win32/api/windef/ns-windef-size) Windows, которая реализует относительную координату или положение.|атлтипес. h|
|[кстрбуфт](../../atl-mfc-shared/reference/cstrbuft-class.md)|Обеспечивает автоматическую очистку ресурсов для `GetBuffer` и `ReleaseBuffer` вызовов для существующего `CStringT` объекта.|атлсимпстр. h|
|[кстрингдата](../../atl-mfc-shared/reference/cstringdata-class.md)|Представляет данные строкового объекта.|атлсимпстр. h|
|[CStringT](../../atl-mfc-shared/reference/cstringt-class.md)|Представляет объект `CStringT`.|CStringT. h (зависит от MFC) atlstr. h (независимо от MFC)|
|[CTime](../../atl-mfc-shared/reference/ctime-class.md)|Представляет абсолютное время и дату.|атлтиме. h|
|[ктимеспан](../../atl-mfc-shared/reference/ctimespan-class.md)|Количество времени, которое внутренне хранится как количество секунд в интервале времени.|атлтиме. h|
|[иатлстрингмгр](../../atl-mfc-shared/reference/iatlstringmgr-class.md)|Представляет интерфейс для `CStringT` диспетчера памяти.|атлсимпстр. h|

## <a name="see-also"></a>См. также раздел

[Общие классы ATL и MFC](../../atl-mfc-shared/atl-mfc-shared-classes.md)
