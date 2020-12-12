---
description: 'Дополнительные сведения о: Кдатапаспроперти Class'
title: Класс Кдатапаспроперти
ms.date: 11/04/2016
f1_keywords:
- CDataPathProperty
- AFXCTL/CDataPathProperty
- AFXCTL/CDataPathProperty::CDataPathProperty
- AFXCTL/CDataPathProperty::GetControl
- AFXCTL/CDataPathProperty::GetPath
- AFXCTL/CDataPathProperty::Open
- AFXCTL/CDataPathProperty::ResetData
- AFXCTL/CDataPathProperty::SetControl
- AFXCTL/CDataPathProperty::SetPath
helpviewer_keywords:
- CDataPathProperty [MFC], CDataPathProperty
- CDataPathProperty [MFC], GetControl
- CDataPathProperty [MFC], GetPath
- CDataPathProperty [MFC], Open
- CDataPathProperty [MFC], ResetData
- CDataPathProperty [MFC], SetControl
- CDataPathProperty [MFC], SetPath
ms.assetid: 1f96efdb-54e4-460b-862c-eba5d4103488
ms.openlocfilehash: 7d9ff9f380fd44d5261374879bab63c9925c4442
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97247960"
---
# <a name="cdatapathproperty-class"></a>Класс Кдатапаспроперти

Реализует свойство элемента управления OLE, которое можно загрузить асинхронно.

## <a name="syntax"></a>Синтаксис

```
class CDataPathProperty : public CAsyncMonikerFile
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кдатапаспроперти:: Кдатапаспроперти](#cdatapathproperty)|Формирует объект `CDataPathProperty`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кдатапаспроперти:: oncontrol](#getcontrol)|Извлекает асинхронный элемент управления OLE, связанный с `CDataPathProperty` объектом.|
|[Кдатапаспроперти:: path](#getpath)|Извлекает путь к свойству.|
|[Кдатапаспроперти:: Open](#open)|Инициирует загрузку асинхронного свойства для связанного элемента управления ActiveX (OLE).|
|[Кдатапаспроперти:: Ресетдата](#resetdata)|Вызывает `CAsyncMonikerFile::OnDataAvailable` для уведомления контейнера об изменении свойств элемента управления.|
|[Кдатапаспроперти:: Сетконтрол](#setcontrol)|Задает асинхронный элемент управления ActiveX (OLE), связанный со свойством.|
|[Кдатапаспроперти:: Сетпас](#setpath)|Задает путь к свойству.|

## <a name="remarks"></a>Комментарии

Асинхронные свойства загружаются после синхронной инициации.

Класс `CDataPathProperty` является производным от `CAysncMonikerFile` . Чтобы реализовать асинхронные свойства в элементах управления OLE, создайте класс, производный от `CDataPathProperty` , и переопределите [ондатааваилабле](../../mfc/reference/casyncmonikerfile-class.md#ondataavailable).

Дополнительные сведения об использовании асинхронных моникеров и элементов управления ActiveX в веб – приложениях см. в следующих статьях:

- [Первые действия в Интернете: элементы управления ActiveX](../../mfc/activex-controls-on-the-internet.md)

- [Первые действия через Интернет: асинхронные моникеры](../../mfc/asynchronous-monikers-on-the-internet.md)

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CFile](../../mfc/reference/cfile-class.md)

[COleStreamFile](../../mfc/reference/colestreamfile-class.md)

[CMonikerFile](../../mfc/reference/cmonikerfile-class.md)

[CAsyncMonikerFile](../../mfc/reference/casyncmonikerfile-class.md)

`CDataPathProperty`

## <a name="requirements"></a>Требования

**Заголовок:** afxctl. h

## <a name="cdatapathpropertycdatapathproperty"></a><a name="cdatapathproperty"></a> Кдатапаспроперти:: Кдатапаспроперти

Формирует объект `CDataPathProperty`.

```
CDataPathProperty(COleControl* pControl = NULL);
CDataPathProperty(LPCTSTR lpszPath, COleControl* pControl = NULL);
```

### <a name="parameters"></a>Параметры

*pControl*<br/>
Указатель на управляющий объект OLE, связываемый с этим `CDataPathProperty` объектом.

*лпсзпас*<br/>
Путь, который может быть абсолютным или относительным, используется для создания асинхронного моникера, который ссылается на фактическое абсолютное расположение свойства. `CDataPathProperty` использует URL-адреса, а не имена файлов. Если требуется `CDataPathProperty` объект для файла, `file://` в начале пути.

### <a name="remarks"></a>Комментарии

`COleControl`Объект, на который указывает *пконтрол* , используется `Open` и извлекается производными классами. Если *пконтрол* имеет значение null, то элемент управления, используемый с, `Open` должен иметь значение `SetControl` . Если *лпсзпас* имеет значение null, можно передать путь через `Open` или задать его с помощью `SetPath` .

## <a name="cdatapathpropertygetcontrol"></a><a name="getcontrol"></a> Кдатапаспроперти:: oncontrol

Вызовите эту функцию члена, чтобы получить `COleControl` объект, связанный с `CDataPathProperty` объектом.

```
COleControl* GetControl();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на элемент управления OLE, связанный с `CDataPathProperty` объектом. Значение NULL, если элемент управления не связан.

## <a name="cdatapathpropertygetpath"></a><a name="getpath"></a> Кдатапаспроперти:: path

Вызовите эту функцию-член, чтобы получить путь, задать, когда `CDataPathProperty` объект был создан или указан в `Open` предыдущем вызове `SetPath` функции-члена.

```
CString GetPath() const;
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает путь к самому свойству. Может быть пустым, если путь не указан.

## <a name="cdatapathpropertyopen"></a><a name="open"></a> Кдатапаспроперти:: Open

Вызовите эту функцию члена, чтобы инициировать загрузку асинхронного свойства для связанного элемента управления.

```
virtual BOOL Open(
    COleControl* pControl,
    CFileException* pError = NULL);

virtual BOOL Open(
    LPCTSTR lpszPath,
    COleControl* pControl,
    CFileException* pError = NULL);

virtual BOOL Open(
    LPCTSTR lpszPath,
    CFileException* pError = NULL);

virtual BOOL Open(CFileException* pError = NULL);
```

### <a name="parameters"></a>Параметры

*pControl*<br/>
Указатель на управляющий объект OLE, связываемый с этим `CDataPathProperty` объектом.

*pError*<br/>
Указатель на исключение файла. В случае ошибки будет задана причина.

*лпсзпас*<br/>
Путь, который может быть абсолютным или относительным, используется для создания асинхронного моникера, который ссылается на фактическое абсолютное расположение свойства. `CDataPathProperty` использует URL-адреса, а не имена файлов. Если требуется `CDataPathProperty` объект для файла, `file://` в начале пути.

### <a name="return-value"></a>Возвращаемое значение

Имеет ненулевое значение в случае успешного выполнения, иначе — 0.

### <a name="remarks"></a>Комментарии

Функция пытается получить `IBindHost` интерфейс из элемента управления.

Перед вызовом `Open` без пути необходимо задать значение для пути к свойству. Это можно сделать при создании объекта или путем вызова `SetPath` функции-члена.

Перед вызовом `Open` без элемента управления элемент управления ActiveX (прежнее название — элемент управления OLE) может быть связан с объектом. Это можно сделать при создании объекта или путем вызова `SetControl` .

Все перегрузки [касинкмоникерфиле:: Open](../../mfc/reference/casyncmonikerfile-class.md#open) также доступны из `CDataPathProperty` .

## <a name="cdatapathpropertyresetdata"></a><a name="resetdata"></a> Кдатапаспроперти:: Ресетдата

Вызовите эту функцию, чтобы получить `CAsyncMonikerFile::OnDataAvailable` уведомление контейнера об изменении свойств элемента управления, и вся информация, загруженная асинхронно, больше не полезна.

```
virtual void ResetData();
```

### <a name="remarks"></a>Комментарии

Необходимо перезапустить открытие. Производные классы могут переопределять эту функцию для различных значений по умолчанию.

## <a name="cdatapathpropertysetcontrol"></a><a name="setcontrol"></a> Кдатапаспроперти:: Сетконтрол

Вызовите эту функцию члена, чтобы связать асинхронный элемент управления OLE с `CDataPathProperty` объектом.

```cpp
void SetControl(COleControl* pControl);
```

### <a name="parameters"></a>Параметры

*pControl*<br/>
Указатель на асинхронный элемент управления OLE, который должен быть связан со свойством.

## <a name="cdatapathpropertysetpath"></a><a name="setpath"></a> Кдатапаспроперти:: Сетпас

Вызовите эту функцию члена, чтобы задать путь к свойству.

```cpp
void SetPath(LPCTSTR lpszPath);
```

### <a name="parameters"></a>Параметры

*лпсзпас*<br/>
Путь, который может быть абсолютным или относительным для свойства, загружаемого асинхронно. `CDataPathProperty` использует URL-адреса, а не имена файлов. Если требуется `CDataPathProperty` объект для файла, `file://` в начале пути.

## <a name="see-also"></a>См. также раздел

[Пример изображения MFC](../../overview/visual-cpp-samples.md)<br/>
[Класс Касинкмоникерфиле](../../mfc/reference/casyncmonikerfile-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Класс Касинкмоникерфиле](../../mfc/reference/casyncmonikerfile-class.md)
