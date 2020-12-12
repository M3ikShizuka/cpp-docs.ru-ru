---
description: 'Дополнительные сведения о: CD2DResource Class'
title: Класс CD2DResource
ms.date: 03/27/2019
f1_keywords:
- CD2DResource
- AFXRENDERTARGET/CD2DResource
- AFXRENDERTARGET/CD2DResource::CD2DResource
- AFXRENDERTARGET/CD2DResource::Create
- AFXRENDERTARGET/CD2DResource::Destroy
- AFXRENDERTARGET/CD2DResource::IsValid
- AFXRENDERTARGET/CD2DResource::IsAutoDestroy
- AFXRENDERTARGET/CD2DResource::ReCreate
- AFXRENDERTARGET/CD2DResource::m_bIsAutoDestroy
- AFXRENDERTARGET/CD2DResource::m_pParentTarget
helpviewer_keywords:
- CD2DResource [MFC], CD2DResource
- CD2DResource [MFC], Create
- CD2DResource [MFC], Destroy
- CD2DResource [MFC], IsValid
- CD2DResource [MFC], IsAutoDestroy
- CD2DResource [MFC], ReCreate
- CD2DResource [MFC], m_bIsAutoDestroy
- CD2DResource [MFC], m_pParentTarget
ms.assetid: 34e3ee18-aab6-4c39-9294-de869e1f7820
ms.openlocfilehash: a110732a7e2bde5ab2fb3b6025acf98d6a3278c6
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97118736"
---
# <a name="cd2dresource-class"></a>Класс CD2DResource

Абстрактный класс, предоставляющий интерфейс для создания ресурсов D2D, таких как кисти, слои и тексты, и управления ими.

## <a name="syntax"></a>Синтаксис

```
class CD2DResource : public CObject;
```

## <a name="members"></a>Члены

### <a name="protected-constructors"></a>Защищенные конструкторы

|Имя|Описание|
|----------|-----------------|
|[CD2DResource:: CD2DResource](#cd2dresource)|Конструирует объект CD2DResource.|
|[CD2DResource:: ~ CD2DResource](#_dtorcd2dresource)|Деструктор Вызывается при уничтожении объекта ресурса D2D.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CD2DResource:: Create](#create)|Создает CD2DResource.|
|[CD2DResource::D естрой](#destroy)|Уничтожает объект CD2DResource.|
|[CD2DResource:: IsValid](#isvalid)|Проверка действительности ресурсов|

### <a name="protected-methods"></a>Защищенные методы

|Имя|Описание|
|----------|-----------------|
|[CD2DResource:: Исаутодестрой](#isautodestroy)|Установите флажок Автоматическое уничтожение.|
|[CD2DResource:: повторное создание](#recreate)|Повторно создает CD2DResource.|

### <a name="protected-data-members"></a>Защищенные члены данных

|Имя|Описание|
|----------|-----------------|
|[CD2DResource:: m_bIsAutoDestroy](#m_bisautodestroy)|Ресурс будет уничтожен владельцем (Крендертаржет)|
|[CD2DResource:: m_pParentTarget](#m_pparenttarget)|Указатель на родительский Крендертаржет)|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

`CD2DResource`

## <a name="requirements"></a>Требования

**Заголовок:** афксрендертаржет. h

## <a name="cd2dresourcecd2dresource"></a><a name="_dtorcd2dresource"></a> CD2DResource:: ~ CD2DResource

Деструктор Вызывается при уничтожении объекта ресурса D2D.

```
virtual ~CD2DResource();
```

## <a name="cd2dresourcecd2dresource"></a><a name="cd2dresource"></a> CD2DResource:: CD2DResource

Конструирует объект CD2DResource.

```
CD2DResource(
    CRenderTarget* pParentTarget,
    BOOL bAutoDestroy);
```

### <a name="parameters"></a>Параметры

*ппаренттаржет*<br/>
Указатель на целевой объект прорисовки.

*баутодестрой*<br/>
Указывает, что объект будет уничтожен владельцем (Ппаренттаржет).

## <a name="cd2dresourcecreate"></a><a name="create"></a> CD2DResource:: Create

Создает CD2DResource.

```
virtual HRESULT Create(CRenderTarget* pRenderTarget) = 0;
```

### <a name="parameters"></a>Параметры

*прендертаржет*<br/>
Указатель на целевой объект прорисовки.

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращает значение S_OK. В противном случае возвращается код ошибки HRESULT.

## <a name="cd2dresourcedestroy"></a><a name="destroy"></a> CD2DResource::D естрой

Уничтожает объект CD2DResource.

```
virtual void Destroy() = 0;
```

## <a name="cd2dresourceisautodestroy"></a><a name="isautodestroy"></a> CD2DResource:: Исаутодестрой

Установите флажок Автоматическое уничтожение.

```
BOOL IsAutoDestroy() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если объект будет уничтожен его владельцем; в противном случае — FALSE.

## <a name="cd2dresourceisvalid"></a><a name="isvalid"></a> CD2DResource:: IsValid

Проверка действительности ресурсов

```
virtual BOOL IsValid() const = 0;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если ресурс является допустимым; в противном случае — FALSE.

## <a name="cd2dresourcem_bisautodestroy"></a><a name="m_bisautodestroy"></a> CD2DResource:: m_bIsAutoDestroy

Ресурс будет уничтожен владельцем (Крендертаржет)

```
BOOL m_bIsAutoDestroy;
```

## <a name="cd2dresourcem_pparenttarget"></a><a name="m_pparenttarget"></a> CD2DResource:: m_pParentTarget

Указатель на родительский Крендертаржет)

```
CRenderTarget* m_pParentTarget;
```

## <a name="cd2dresourcerecreate"></a><a name="recreate"></a> CD2DResource:: повторное создание

Повторно создает CD2DResource.

```
virtual HRESULT ReCreate(CRenderTarget* pRenderTarget);
```

### <a name="parameters"></a>Параметры

*прендертаржет*<br/>
Указатель на целевой объект прорисовки.

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращает значение S_OK. В противном случае возвращается код ошибки HRESULT.

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
