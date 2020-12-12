---
description: 'Дополнительные сведения о: Ксеттингссторесп Class'
title: Класс Ксеттингссторесп
ms.date: 11/04/2016
f1_keywords:
- CSettingsStoreSP
- AFXSETTINGSSTORE/CSettingsStoreSP
- AFXSETTINGSSTORE/CSettingsStoreSP::CSettingsStoreSP
- AFXSETTINGSSTORE/CSettingsStoreSP::Create
- AFXSETTINGSSTORE/CSettingsStoreSP::SetRuntimeClass
helpviewer_keywords:
- CSettingsStoreSP [MFC], CSettingsStoreSP
- CSettingsStoreSP [MFC], Create
- CSettingsStoreSP [MFC], SetRuntimeClass
ms.assetid: bcd37f40-cfd4-4d17-a5ce-3bfabe995dcc
ms.openlocfilehash: 67e9f881fc43722ab568aa7f149fc7a2b44cc764
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97264691"
---
# <a name="csettingsstoresp-class"></a>Класс Ксеттингссторесп

`CSettingsStoreSP`Класс является вспомогательным классом, который можно использовать для создания экземпляров [класса ксеттингссторе](../../mfc/reference/csettingsstore-class.md).

## <a name="syntax"></a>Синтаксис

```
class CSettingsStoreSP
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Ксеттингссторесп:: Ксеттингссторесп](#csettingsstoresp)|Формирует объект `CSettingsStoreSP`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ксеттингссторесп:: Create](#create)|Создает экземпляр класса, производного от `CSettingsStore` .|
|[Ксеттингссторесп:: Сетрунтимекласс](#setruntimeclass)|Задает класс среды выполнения. `Create`Метод использует класс среды выполнения, чтобы определить, какой класс объектов следует создать.|

### <a name="data-members"></a>Элементы данных

|Имя|Описание|
|----------|-----------------|
|`m_dwUserData`|Пользовательские данные пользователя, хранящиеся в `CSettingsStoreSP` объекте. Эти данные указываются в конструкторе `CSettingsStoreSP` объекта.|
|`m_pRegistry`|`CSettingsStore`Объект, производный от, который `Create` создается методом.|

## <a name="remarks"></a>Комментарии

Класс можно использовать `CSettingsStoreSP` для перенаправления всех операций реестра MFC в другие расположения, такие как XML-файл или база данных. Для этого выполните следующие действия:

1. Создайте класс (например, `CMyStore` ) и наследует его от `CSettingsStore` .

1. Используйте [DECLARE_DYNCREATE](run-time-object-model-services.md#declare_dyncreate) и [IMPLEMENT_DYNCREATE](run-time-object-model-services.md#implement_dyncreate) макросы с пользовательским `CSettingsStore` классом, чтобы включить динамическое создание.

1. Переопределите виртуальные функции и реализуйте `Read` `Write` функции и в пользовательском классе. Реализуйте любые другие функции для чтения и записи данных в нужное расположение.

1. В приложении вызовите `CSettingsStoreSP::SetRuntimeClass` и передайте указатель на [структуру крунтимекласс](../../mfc/reference/cruntimeclass-structure.md) , полученную из класса.

Когда платформа обычно обращается к реестру, она теперь динамически создает пользовательский класс и использует его для чтения или записи данных.

`CSettingsStoreSP::SetRuntimeClass` использует глобальную статическую переменную. Поэтому в каждый момент времени доступно только одно пользовательское хранилище.

## <a name="requirements"></a>Требования

**Заголовок:** афкссеттингссторе. h

## <a name="csettingsstorespcreate"></a><a name="create"></a> Ксеттингссторесп:: Create

Создает новый экземпляр объекта, производного от [класса ксеттингссторе](../../mfc/reference/csettingsstore-class.md).

```
CSettingsStore& CSettingsStoreSP Create(
    BOOL bAdmin,
    BOOL bReadOnly);
```

### <a name="parameters"></a>Параметры

*бадмин*<br/>
окне Логический параметр, определяющий, `CSettingsStore` создается ли объект в режиме администратора.

*бреадонли*<br/>
окне Логический параметр, определяющий, `CSettingsStore` создан ли объект для доступа только для чтения.

### <a name="return-value"></a>Возвращаемое значение

Ссылка на только что созданный `CSettingsStore` объект.

### <a name="remarks"></a>Комментарии

Чтобы определить, какой тип объекта будет создан, можно использовать метод [ксеттингссторесп:: сетрунтимекласс](#setruntimeclass) `CSettingsStoreSP::Create` . По умолчанию этот метод создает `CSettingsStore` объект.

При создании `CSettingsStore` объекта в режиме администратора расположением по умолчанию для всех систем доступа к реестру является HKEY_LOCAL_MACHINE. В противном случае расположением по умолчанию для всех обращений к реестру является HKEY_CURRENT_USER.

Если *бадмин* имеет значение true, приложение должно иметь права администратора. В противном случае произойдет сбой при попытке доступа к реестру.

### <a name="example"></a>Пример

В следующем примере показано, как использовать `Create` метод `CSettingsStoreSP` класса.

[!code-cpp[NVC_MFC_RibbonApp#33](../../mfc/reference/codesnippet/cpp/csettingsstoresp-class_1.cpp)]

## <a name="csettingsstorespcsettingsstoresp"></a><a name="csettingsstoresp"></a> Ксеттингссторесп:: Ксеттингссторесп

Конструирует объект [класса ксеттингссторесп](../../mfc/reference/csettingsstoresp-class.md) .

```
CSettingsStoreSP::CSettingsStoreSP(DWORD dwUserData = 0);
```

### <a name="parameters"></a>Параметры

*двусердата*<br/>
окне Определяемые пользователем данные, которые `CSettingsStoreSP` хранятся в объекте.

### <a name="remarks"></a>Комментарии

`CSettingsStoreSP`Объект сохраняет данные из *двусердата* в защищенной переменной члена `m_dwUserData` .

## <a name="csettingsstorespsetruntimeclass"></a><a name="setruntimeclass"></a> Ксеттингссторесп:: Сетрунтимекласс

Задает класс среды выполнения. Метод [ксеттингссторесп:: Create](#create) использует класс среды выполнения для определения типа создаваемого объекта.

```
static BOOL __stdcall CSettingsStoreSP::SetRuntimeClass(CRuntimeClass* pRTI);
```

### <a name="parameters"></a>Параметры

*прти*<br/>
окне Указатель на сведения о классе среды выполнения для класса, производного от [класса ксеттингссторе](../../mfc/reference/csettingsstore-class.md).

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE в случае успешного выполнения; Значение FALSE, если класс, идентифицируемый *прти* , не является производным от `CSettingsStore` .

### <a name="remarks"></a>Комментарии

[Класс ксеттингссторесп](../../mfc/reference/csettingsstoresp-class.md) можно использовать для наследования классов от `CSettingsStore` . Используйте метод, `SetRuntimeClass` Если требуется создать объекты пользовательского класса, производного от `CSettingsStore` .

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Класс Ксеттингссторе](../../mfc/reference/csettingsstore-class.md)
