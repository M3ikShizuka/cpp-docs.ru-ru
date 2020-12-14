---
description: 'Дополнительные сведения о: TN039: реализация автоматизации MFC/OLE'
title: 'TN039: реализация автоматизации MFC-OLE'
ms.date: 06/28/2018
helpviewer_keywords:
- MFC, COM support
- IDispatch interface
- MFC, OLE DB and
- TN039
- Automation, MFC COM interface entry points
ms.assetid: 765fa3e9-dd54-4f08-9ad2-26e0546ff8b6
ms.openlocfilehash: caabd3719a467e534e47ca61ed8f9a9f1f0d2eb6
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97215421"
---
# <a name="tn039-mfcole-automation-implementation"></a>TN039. Реализация автоматизации MFC/OLE

> [!NOTE]
> Следующее техническое примечание не было обновлено, поскольку сначала оно было включено в электронную документацию. В результате некоторые процедуры и разделы могут быть устаревшими или неверными. Для получения последних сведений рекомендуется выполнить поиск интересующей темы в алфавитном указателе документации в Интернете.

## <a name="overview-of-ole-idispatch-interface"></a>Общие сведения об интерфейсе OLE IDispatch

`IDispatch`Интерфейс — это средства, с помощью которых приложения предоставляют методы и свойства, которые позволяют другим приложениям, таким как Visual Basic, или другим языкам, использовать функции приложения. Самой важной частью этого интерфейса является `IDispatch::Invoke` функция. Для реализации MFC использует "карты диспетчеризации" `IDispatch::Invoke` . Схема диспетчеризации предоставляет сведения о реализации MFC в макете или "форме" `CCmdTarget` производных классов, что позволяет напрямую манипулировать свойствами объекта или вызывать функции-члены в объекте для удовлетворения `IDispatch::Invoke` запросов.

В большинстве случаев ClassWizard и MFC работают для скрытия большей части деталей OLE Automation от программиста приложения. Программист сосредоточен на фактической функциональности, которую можно предоставить приложению, и не должен беспокоиться о базовых механизмах.

Однако в некоторых случаях необходимо понимать, что делает MFC в фоновом режиме. В этом заметке будет показано, как платформа назначает **идентификатор DISPID** для функций и свойств элементов. Знание алгоритма, используемого MFC для назначения **DISPID**, требуется только в том случае, если необходимо знать идентификаторы, например при создании библиотеки типов для объектов приложения.

## <a name="mfc-dispid-assignment"></a>Назначение DISPID в MFC

Несмотря на то, что пользователь автоматизации (например, Visual Basic пользователь) видит фактические имена свойств и методов, включенных в автоматизацию, в коде (например, obj). ShowWindow), реализация `IDispatch::Invoke` не получает фактические имена. В целях оптимизации он получает **идентификатор DISPID**, который представляет собой 32-разрядный "волшебный" файл cookie, описывающий метод или свойство, к которому осуществляется доступ. Эти значения **DISPID** возвращаются из `IDispatch` реализации с помощью другого метода, который называется `IDispatch::GetIDsOfNames` . Клиентское приложение автоматизации будет вызываться `GetIDsOfNames` по одному разу для каждого члена или свойства, к которому он обращается, и кэширует их для последующего вызова `IDispatch::Invoke` . Таким образом, дорогостоящий Поиск строки выполняется только один раз для каждого объекта, а не один раз в каждом `IDispatch::Invoke` вызове.

MFC определяет **DISPID** для каждого метода и свойства, основываясь на двух вещах:

- Расстояние от верхнего края схемы диспетчеризации (1 относительный)

- Расстояние от наиболее производного класса до исправной схемы (0 относительный)

**Идентификатор DISPID** делится на две части. **Ловорд** **идентификатора DISPID** содержит первый компонент, расстояние от верхнего края схемы диспетчеризации. **HIWORD** содержит расстояние от наиболее производного класса. Пример:

```cpp
class CDispPoint : public CCmdTarget
{
public:
    short m_x, m_y;
    // ...
    DECLARE_DISPATCH_MAP()
    // ...
};

class CDisp3DPoint : public CDispPoint
{
public:
    short m_z;
    // ...
    DECLARE_DISPATCH_MAP()
    // ...
};

BEGIN_DISPATCH_MAP(CDispPoint, CCmdTarget)
    DISP_PROPERTY(CDispPoint, "x", m_x, VT_I2)
    DISP_PROPERTY(CDispPoint, "y", m_y, VT_I2)
END_DISPATCH_MAP()

BEGIN_DISPATCH_MAP(CDisp3DPoint, CDispPoint)
    DISP_PROPERTY(CDisp3DPoint, "z", m_z, VT_I2)
END_DISPATCH_MAP()
```

Как видите, существует два класса, оба из которых предоставляют интерфейсы OLE Automation. Один из этих классов является производным от другого и, таким же, использует функциональность базового класса, включая компонент OLE-автоматизации (в данном случае это свойства x и y).

MFC создаст **DISPID** для класса кдисппоинт следующим образом:

```cpp
property X    (DISPID)0x00000001
property Y    (DISPID)0x00000002
```

Поскольку свойства не находятся в базовом классе, **HIWORD** **DISPID** всегда равен нулю (расстояние от самого последнего производного класса для кдисппоинт равно нулю).

MFC создаст **DISPID** для класса CDisp3DPoint следующим образом:

```cpp
property Z    (DISPID)0x00000001
property X    (DISPID)0x00010001
property Y    (DISPID)0x00010002
```

Свойству Z присваивается **DISPID** с нулевым **HIWORD** , так как он определен в классе, предоставляющем свойства CDisp3DPoint. Поскольку свойства X и Y определены в базовом классе, **HIWORD** **DISPID** имеет значение 1, так как класс, в котором определены эти свойства, находится на расстоянии от одного производного класса от самого последнего.

> [!NOTE]
> **Ловорд** всегда определяется положением на карте, даже если в карте есть записи с явным **идентификатором DISPID** (Дополнительные сведения о **_id** версиях `DISP_PROPERTY` макросов и см. в следующем разделе `DISP_FUNCTION` ).

## <a name="advanced-mfc-dispatch-map-features"></a>Расширенные функции карт диспетчеризации MFC

Существует ряд дополнительных функций, которые ClassWizard не поддерживаются в этом выпуске Visual C++. ClassWizard поддерживает `DISP_FUNCTION` , `DISP_PROPERTY` и, `DISP_PROPERTY_EX` определяющие метод, свойство переменной-члена и свойство функции-члена Get/Set соответственно. Обычно эти возможности необходимы для создания большинства серверов автоматизации.

Если макросы, поддерживаемые ClassWizard, недостаточны, можно использовать следующие дополнительные макросы: `DISP_PROPERTY_NOTIFY` , и `DISP_PROPERTY_PARAM` .

## <a name="disp_property_notify--macro-description"></a>DISP_PROPERTY_NOTIFY — описание макроса

```cpp
DISP_PROPERTY_NOTIFY(
    theClass,
    pszName,
    memberName,
    pfnAfterSet,
    vtPropType)
```

### <a name="parameters"></a>Параметры

*секласс*<br/>
Имя класса.

*pszName*<br/>
Внешнее имя свойства.

*memberName*<br/>
Имя переменной-члена, в которой хранится свойство.

*пфнафтерсет*<br/>
Имя функции-члена, вызываемой при изменении свойства.

*втпроптипе*<br/>
Значение типа, указывающее тип свойства.

### <a name="remarks"></a>Комментарии

Этот макрос во многом похож на DISP_PROPERTY, за исключением того, что он принимает дополнительный аргумент. Дополнительный аргумент *пфнафтерсет* должен быть функцией-членом, возвращающей Nothing и не принимающей параметров, "void онпропертинотифи ()". Он будет вызван **после** изменения переменной члена.

## <a name="disp_property_param--macro-description"></a>DISP_PROPERTY_PARAM — описание макроса

```cpp
DISP_PROPERTY_PARAM(
    theClass,
    pszName,
    pfnGet,
    pfnSet,
    vtPropType,
    vtsParams)
```

### <a name="parameters"></a>Параметры

*секласс*<br/>
Имя класса.

*pszName*<br/>
Внешнее имя свойства.

*мембержет*<br/>
Имя функции члена, используемой для получения свойства.

*memberSet*<br/>
Имя функции члена, используемой для задания свойства.

*втпроптипе*<br/>
Значение типа, указывающее тип свойства.

*втспарамс*<br/>
Строка, разделенная пробелами VTS_ для каждого параметра.

### <a name="remarks"></a>Комментарии

Подобно макросу DISP_PROPERTY_EX, этот макрос определяет свойство, доступ к которому осуществляется с помощью отдельных функций-членов Get и Set. Однако этот макрос позволяет указать список параметров для свойства. Это полезно для реализации свойств, которые индексируются или параметризованы каким-либо другим способом. Параметры всегда помещаются первыми, за которым следует новое значение свойства. Пример:

```cpp
DISP_PROPERTY_PARAM(CMyObject, "item", GetItem, SetItem, VT_DISPATCH, VTS_I2 VTS_I2)
```

будет соответствовать функциям для получения и установки элементов:

```cpp
LPDISPATCH CMyObject::GetItem(short row, short col)
void CMyObject::SetItem(short row, short col, LPDISPATCH newValue)
```

## <a name="disp_xxxx_id--macro-descriptions"></a>DISP_XXXX_ID — описания макросов

```cpp
DISP_FUNCTION_ID(
    theClass,
    pszName,
    dispid,
    pfnMember,
    vtRetVal,
    vtsParams)
DISP_PROPERTY_ID(
    theClass,
    pszName,
    dispid,
    memberName,
    vtPropType)
DISP_PROPERTY_NOTIFY_ID(
    theClass,
    pszName,
    dispid,
    memberName,
    pfnAfterSet,
    vtPropType)
DISP_PROPERTY_EX_ID(
    theClass,
    pszName,
    dispid,
    pfnGet,
    pfnSet,
    vtPropType)
DISP_PROPERTY_PARAM_ID(
    theClass,
    pszName,
    dispid,
    pfnGet,
    pfnSet,
    vtPropType,
    vtsParams)
```

### <a name="parameters"></a>Параметры

*секласс*<br/>
Имя класса.

*pszName*<br/>
Внешнее имя свойства.

*DISPID*<br/>
Фиксированный идентификатор DISPID для свойства или метода.

*пфнжет*<br/>
Имя функции члена, используемой для получения свойства.

*пфнсет*<br/>
Имя функции члена, используемой для задания свойства.

*memberName*<br/>
Имя переменной члена, сопоставляемой со свойством

*втпроптипе*<br/>
Значение типа, указывающее тип свойства.

*втспарамс*<br/>
Строка, разделенная пробелами VTS_ для каждого параметра.

### <a name="remarks"></a>Комментарии

Эти макросы позволяют указать **идентификатор DISPID** вместо того, чтобы позволить MFC автоматически назначить его. Эти дополнительные макросы имеют одинаковые имена, за исключением того, что идентификатор добавляется к имени макроса (например, **DISP_PROPERTY_ID**), а идентификатор определяется параметром, заданным сразу после параметра *pszName* . См. АФКСДИСП. H. Дополнительные сведения об этих макросах. Записи **_id** должны размещаться в конце схемы диспетчеризации. Они будут влиять на автоматическое создание **SPID** таким же образом, как и **не_IDная** версия макроса ( **идентификаторы DISPID** определяются по положению). Пример:

```cpp
BEGIN_DISPATCH_MAP(CDisp3DPoint, CCmdTarget)
    DISP_PROPERTY(CDisp3DPoint, "y", m_y, VT_I2)
    DISP_PROPERTY(CDisp3DPoint, "z", m_z, VT_I2)
    DISP_PROPERTY_ID(CDisp3DPoint, "x", 0x00020003, m_x, VT_I2)
END_DISPATCH_MAP()
```

MFC создаст идентификаторы DISPID для класса CDisp3DPoint следующим образом:

```cpp
property X    (DISPID)0x00020003
property Y    (DISPID)0x00000002
property Z    (DISPID)0x00000001
```

Указание фиксированного **идентификатора DISPID** полезно для обеспечения обратной совместимости с ранее существующим интерфейсом диспетчеризации или для реализации определенных системных методов или свойств (обычно обозначается отрицательным **идентификатором DISPID**, таким как коллекция **DISPID_NEWENUM** ).

## <a name="retrieving-the-idispatch-interface-for-a-coleclientitem"></a>Получение интерфейса IDispatch для COleClientItem

Многие серверы поддерживают автоматизацию в своих объектах документов, а также функции OLE Server. Чтобы получить доступ к этому интерфейсу автоматизации, необходимо получить прямой доступ к `COleClientItem::m_lpObject` переменной-члену. Приведенный ниже код извлечет `IDispatch` интерфейс для объекта, производного от `COleClientItem` . Если вы нашли необходимые функции, вы можете включить приведенный ниже код в приложение.

```cpp
LPDISPATCH CMyClientItem::GetIDispatch()
{
    ASSERT_VALID(this);
    ASSERT(m_lpObject != NULL);

    LPUNKNOWN lpUnk = m_lpObject;

    Run();      // must be running

    LPOLELINK lpOleLink = NULL;
    if (m_lpObject->QueryInterface(IID_IOleLink,
        (LPVOID FAR*)&lpOleLink) == NOERROR)
    {
        ASSERT(lpOleLink != NULL);
        lpUnk = NULL;
        if (lpOleLink->GetBoundSource(&lpUnk) != NOERROR)
        {
            TRACE0("Warning: Link is not connected!\n");
            lpOleLink->Release();
            return NULL;
        }
        ASSERT(lpUnk != NULL);
    }

    LPDISPATCH lpDispatch = NULL;
    if (lpUnk->QueryInterface(IID_IDispatch, &lpDispatch) != NOERROR)
    {
        TRACE0("Warning: does not support IDispatch!\n");
        return NULL;
    }

    ASSERT(lpDispatch != NULL);
    return lpDispatch;
}
```

Интерфейс диспетчеризации, возвращаемый этой функцией, можно затем использовать напрямую или присоединить к `COleDispatchDriver` для строго типизированного доступа. Если вы используете его напрямую, убедитесь, что вы вызываете его `Release` член, когда через указатель ( `COleDispatchDriver` деструктор делает это по умолчанию).

## <a name="see-also"></a>См. также раздел

[Технические примечания по номеру](../mfc/technical-notes-by-number.md)<br/>
[Технические примечания по категориям](../mfc/technical-notes-by-category.md)
