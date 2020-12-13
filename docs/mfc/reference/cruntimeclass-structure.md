---
description: 'Дополнительные сведения о: структура Крунтимекласс'
title: Структура Крунтимекласс
ms.date: 11/04/2016
f1_keywords:
- CRuntimeClass
helpviewer_keywords:
- CRuntimeClass structure [MFC]
- dynamic class information [MFC]
- runtime [MFC], class information
- run-time class [MFC], CRuntimeClass structure
ms.assetid: de62b6ef-90d4-420f-8c70-f58b36976a2b
ms.openlocfilehash: e02732ec595026f028ad4b8f9bd3d8898a40cbc0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97342921"
---
# <a name="cruntimeclass-structure"></a>Структура Крунтимекласс

Каждый класс, производный от `CObject` , связан со `CRuntimeClass` структурой, которую можно использовать для получения сведений об объекте или его базовом классе во время выполнения.

## <a name="syntax"></a>Синтаксис

```
struct CRuntimeClass
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Крунтимекласс:: CreateObject](#createobject)|Создает объект во время выполнения.|
|[Крунтимекласс:: Фромнаме](#fromname)|Создает объект во время выполнения с помощью привычного имени класса.|
|[Крунтимекласс:: Исдериведфром](#isderivedfrom)|Определяет, является ли класс производным от указанного класса.|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[Крунтимекласс:: m_lpszClassName](#m_lpszclassname)|Имя класса.|
|[Крунтимекласс:: m_nObjectSize](#m_nobjectsize)|Размер объекта в байтах.|
|[Крунтимекласс:: m_pBaseClass](#m_pbaseclass)|Указатель на `CRuntimeClass` структуру базового класса.|
|[Крунтимекласс:: m_pfnCreateObject](#m_pfncreateobject)|Указатель на функцию, которая динамически создает объект.|
|[Крунтимекласс:: m_pfnGetBaseClass](#m_pfngetbaseclass)|Возвращает `CRuntimeClass` структуру (доступна только при динамической компоновке).|
|[Крунтимекласс:: m_wSchema](#m_wschema)|Номер схемы класса.|

## <a name="remarks"></a>Комментарии

`CRuntimeClass` является структурой и поэтому не имеет базового класса.

Возможность определить класс объекта во время выполнения полезна, если требуется проверка дополнительных типов аргументов функции или если необходимо написать специальный код на основе класса объекта. Сведения о классе времени выполнения не поддерживаются непосредственно языком C++.

`CRuntimeClass` предоставляет сведения о связанном объекте C++, например указатель на `CRuntimeClass` базовый класс и имя класса ASCII связанного класса. Эта структура также реализует различные функции, которые можно использовать для динамического создания объектов, указания типа объекта с помощью привычного имени и определения того, является ли связанный класс производным от конкретного класса.

Дополнительные сведения об использовании см `CRuntimeClass` . в статье [доступ к Run-Time сведениям о классе](../../mfc/accessing-run-time-class-information.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`CRuntimeClass`

## <a name="requirements"></a>Требования

**Заголовок:** AFX. h

## <a name="cruntimeclasscreateobject"></a><a name="createobject"></a> Крунтимекласс:: CreateObject

Вызывайте эту функцию для динамического создания указанного класса во время выполнения.

```
CObject* CreateObject();

static CObject* PASCAL CreateObject(LPCSTR lpszClassName);

static CObject* PASCAL CreateObject(LPCWSTR lpszClassName);
```

### <a name="parameters"></a>Параметры

*лпсзкласснаме*<br/>
Знакомое имя создаваемого класса.

### <a name="return-value"></a>Возвращаемое значение

Указатель на только что созданный объект или значение NULL, если имя класса не найдено или недостаточно памяти для создания объекта.

### <a name="remarks"></a>Комментарии

Классы, производные от `CObject` , могут поддерживать динамическое создание, что является возможностью создания объекта указанного класса во время выполнения. Например, классы документов, представлений и фреймов должны поддерживать динамическое создание. Дополнительные сведения о динамическом создании и `CreateObject` члене см. в разделе [класс CObject](../../mfc/using-cobject.md) и [класс CObject: указание уровней функциональности](../../mfc/specifying-levels-of-functionality.md).

### <a name="example"></a>Пример

  См. пример для [исдериведфром](#isderivedfrom).

## <a name="cruntimeclassfromname"></a><a name="fromname"></a> Крунтимекласс:: Фромнаме

Вызовите эту функцию, чтобы получить `CRuntimeClass` структуру, связанную с привычным именем.

```
static CRuntimeClass* PASCAL FromName(LPCSTR lpszClassName);

static CRuntimeClass* PASCAL FromName(LPCWSTR lpszClassName);
```

### <a name="parameters"></a>Параметры

*лпсзкласснаме*<br/>
Знакомое имя класса, производного от `CObject` .

### <a name="return-value"></a>Возвращаемое значение

Указатель на `CRuntimeClass` объект, соответствующий имени, переданному в *лпсзкласснаме*. Функция возвращает значение NULL, если соответствующее имя класса не найдено.

### <a name="example"></a>Пример

[!code-cpp[NVC_MFCCObjectSample#17](../../mfc/codesnippet/cpp/cruntimeclass-structure_1.cpp)]

## <a name="cruntimeclassisderivedfrom"></a><a name="isderivedfrom"></a> Крунтимекласс:: Исдериведфром

Вызовите эту функцию, чтобы определить, является ли вызывающий класс производным от класса, указанного в параметре *пбасекласс* .

```
BOOL IsDerivedFrom(const CRuntimeClass* pBaseClass) const;
```

### <a name="parameters"></a>Параметры

*пбасекласс*<br/>
Знакомое имя класса, производного от `CObject` .

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если вызов класса `IsDerivedFrom` является производным от базового класса, структура которого задана в `CRuntimeClass` качестве параметра; в противном случае — значение false.

### <a name="remarks"></a>Комментарии

Связь определяется путем "прохода" из класса члена вверх по цепочке производных классов в начало. Эта функция возвращает значение FALSE, только если совпадение для базового класса не найдено.

> [!NOTE]
> Чтобы использовать эту `CRuntimeClass` структуру, необходимо включить макрос IMPLEMENT_DYNAMIC, IMPLEMENT_DYNCREATE или IMPLEMENT_SERIAL в реализацию класса, для которого требуется получить сведения об объекте времени выполнения.

Дополнительные сведения об использовании см `CRuntimeClass` . в статье [класс CObject: доступ к сведениям о классе Run-Time](../../mfc/accessing-run-time-class-information.md).

### <a name="example"></a>Пример

[!code-cpp[NVC_MFCCObjectSample#18](../../mfc/codesnippet/cpp/cruntimeclass-structure_2.cpp)]

## <a name="cruntimeclassm_lpszclassname"></a><a name="m_lpszclassname"></a> Крунтимекласс:: m_lpszClassName

Строка, заканчивающаяся нулем и содержащая имя класса ASCII.

### <a name="remarks"></a>Комментарии

Это имя можно использовать для создания экземпляра класса с помощью `FromName` функции члена.

### <a name="example"></a>Пример

  См. пример для [исдериведфром](#isderivedfrom).

## <a name="cruntimeclassm_nobjectsize"></a><a name="m_nobjectsize"></a> Крунтимекласс:: m_nObjectSize

Размер объекта в байтах.

### <a name="remarks"></a>Комментарии

Если объект содержит элементы данных, указывающие на выделенную память, размер этой памяти не включается.

### <a name="example"></a>Пример

  См. пример для [исдериведфром](#isderivedfrom).

## <a name="cruntimeclassm_pbaseclass"></a><a name="m_pbaseclass"></a> Крунтимекласс:: m_pBaseClass

Если приложение статически ссылается на MFC, этот элемент данных содержит указатель на `CRuntimeClass` структуру базового класса.

### <a name="remarks"></a>Комментарии

Если приложение динамически связывается с библиотекой MFC, см. раздел [m_pfnGetBaseClass](#m_pfngetbaseclass).

### <a name="example"></a>Пример

  См. пример для [исдериведфром](#isderivedfrom).

## <a name="cruntimeclassm_pfncreateobject"></a><a name="m_pfncreateobject"></a> Крунтимекласс:: m_pfnCreateObject

Указатель на функцию конструктора по умолчанию, который создает объект класса.

### <a name="remarks"></a>Комментарии

Этот указатель является допустимым только в том случае, если класс поддерживает динамическое создание; в противном случае функция возвращает значение NULL.

## <a name="cruntimeclassm_pfngetbaseclass"></a><a name="m_pfngetbaseclass"></a> Крунтимекласс:: m_pfnGetBaseClass

Если приложение использует библиотеку MFC в качестве общей библиотеки DLL, этот элемент данных указывает на функцию, которая возвращает `CRuntimeClass` структуру базового класса.

### <a name="remarks"></a>Комментарии

Если приложение статически ссылается на библиотеку MFC, см. раздел [m_pBaseClass](#m_pbaseclass).

### <a name="example"></a>Пример

  См. пример для [исдериведфром](#isderivedfrom).

## <a name="cruntimeclassm_wschema"></a><a name="m_wschema"></a> Крунтимекласс:: m_wSchema

Номер схемы (-1 для несериализуемых классов).

### <a name="remarks"></a>Комментарии

Дополнительные сведения о номерах схем см. в разделе макрос [IMPLEMENT_SERIAL](run-time-object-model-services.md#implement_serial) .

### <a name="example"></a>Пример

  См. пример для [исдериведфром](#isderivedfrom).

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[CObject:: Жетрунтимекласс](../../mfc/reference/cobject-class.md#getruntimeclass)<br/>
[CObject:: IsKindOf](../../mfc/reference/cobject-class.md#iskindof)<br/>
[RUNTIME_CLASS](run-time-object-model-services.md#runtime_class)<br/>
[IMPLEMENT_DYNAMIC](run-time-object-model-services.md#implement_dynamic)<br/>
[IMPLEMENT_DYNCREATE](run-time-object-model-services.md#implement_dyncreate)<br/>
[IMPLEMENT_SERIAL](run-time-object-model-services.md#implement_serial)
