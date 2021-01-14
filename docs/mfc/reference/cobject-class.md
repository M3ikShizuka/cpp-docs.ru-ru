---
description: Дополнительные сведения о классе CObject
title: CObject, класс
ms.date: 1/12/2021
f1_keywords:
- CObject
- AFX/CObject
- AFX/CObject::CObject
- AFX/CObject::AssertValid
- AFX/CObject::Dump
- AFX/CObject::GetRuntimeClass
- AFX/CObject::IsKindOf
- AFX/CObject::IsSerializable
- AFX/CObject::Serialize
helpviewer_keywords:
- CObject [MFC], CObject
- CObject [MFC], AssertValid
- CObject [MFC], Dump
- CObject [MFC], GetRuntimeClass
- CObject [MFC], IsKindOf
- CObject [MFC], IsSerializable
- CObject [MFC], Serialize
ms.openlocfilehash: ba152a9cbbe6e2fa217d6c2e24d13ea48dd37c87
ms.sourcegitcommit: b51f79b5394e12cd90cb65c85cc01716f90bfc90
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/13/2021
ms.locfileid: "98167012"
---
# <a name="cobject-class"></a>Класс `CObject`

Основной базовый класс для всех исключений библиотеки классов Microsoft Foundation.

## <a name="syntax"></a>Синтаксис

```cpp
class AFX_NOVTABLE CObject
```

## <a name="members"></a>Члены

### <a name="protected-constructors"></a>Защищенные конструкторы

|Имя|Описание|
|----------|-----------------|
|[`CObject::CObject`](#cobject)|Конструктор по умолчанию.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[`CObject::AssertValid`](#assertvalid)|Проверяет целостность этого объекта.|
|[`CObject::Dump`](#dump)|Создает диагностический дамп этого объекта.|
|[`CObject::GetRuntimeClass`](#getruntimeclass)|Возвращает `CRuntimeClass` структуру, соответствующую классу данного объекта.|
|[`CObject::IsKindOf`](#iskindof)|Проверяет связь этого объекта с заданным классом.|
|[`CObject::IsSerializable`](#isserializable)|Проверяет, можно ли сериализовать этот объект.|
|[`CObject::Serialize`](#serialize)|Загружает или сохраняет объект из или в архив.|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[`CObject::operator delete`](#operator_delete)|Специальный **`delete`** оператор.|
|[`CObject::operator new`](#operator_new)|Специальный **`new`** оператор.|

## <a name="remarks"></a>Примечания

Он выступает в качестве корня не только для классов библиотек, таких как `CFile` и `CObList` , но также и для классов, которые вы пишете. `CObject` предоставляет базовые службы, включая

- Поддержка сериализации
- Сведения о классе времени выполнения
- Вывод диагностики объектов
- Совместимость с классами коллекций

`CObject` не поддерживает множественное наследование. Производные классы могут иметь только один `CObject` базовый класс, который `CObject` должен быть левым в иерархии. Однако допускается наличие структур и классов, не являющихся `CObject` производными, в правой части ветвей с множественным наследованием.

При `CObject` использовании некоторых необязательных макросов в реализации и объявлениях класса вы получите значительные преимущества от наследования.

Макросы первого уровня [`DECLARE_DYNAMIC`](run-time-object-model-services.md#declare_dynamic) и [`IMPLEMENT_DYNAMIC`](run-time-object-model-services.md#implement_dynamic) , разрешив доступ во время выполнения к имени класса и его положению в иерархии. Это, в свою очередь, допускает осмысленную диагностическую копию.

Макросы второго уровня, [`DECLARE_SERIAL`](run-time-object-model-services.md#declare_serial) и [`IMPLEMENT_SERIAL`](run-time-object-model-services.md#implement_serial) , включают все функциональные возможности макросов первого уровня, а также позволяют «сериализовать» объект в «архив» и из него.

Дополнительные сведения о наследовании классов Microsoft Foundation и классов C++ в целом и использовании см `CObject` . в разделе [Использование CObject](../../mfc/using-cobject.md) и [Serialization](../../mfc/serialization-in-mfc.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`CObject`

## <a name="requirements"></a>Требования

**Заголовок:**`afx.h`

## <a name="cobjectassertvalid"></a><a name="assertvalid"></a> CObject:: AssertValid

Проверяет целостность этого объекта.

```cpp
virtual void AssertValid() const;
```

### <a name="remarks"></a>Примечания

`AssertValid` выполняет проверку достоверности этого объекта, проверяя его внутреннее состояние. В отладочной версии библиотеки `AssertValid` может утверждать и завершать программу сообщением, в котором отображается номер строки и имя файла, в котором произошел сбой утверждения.

При написании собственного класса следует переопределить `AssertValid` функцию, чтобы предоставить службы диагностики для себя и других пользователей класса. Переопределение `AssertValid` обычно вызывает `AssertValid` функцию своего базового класса перед проверкой элементов данных, уникальных для производного класса.

Поскольку `AssertValid` является **`const`** функцией, изменение состояния объекта во время теста не допускается. Собственные функции производных классов `AssertValid` не должны вызывать исключения, а должны утверждать, обнаруживают ли они недопустимые данные объекта.

Определение "допустимости" зависит от класса объекта. Как правило, функция должна выполнить полную проверку. То есть, если объект содержит указатели на другие объекты, он должен проверить, нет ли указателей `NULL` , но не должен выполнять проверку на наличие объектов, на которые ссылаются указатели.

### <a name="example"></a>Пример

[`CObList::CObList`](../../mfc/reference/coblist-class.md#coblist)Список `CAge` классов, используемых во всех примерах, см `CObject` . в разделе.

[!code-cpp[NVC_MFCCObjectSample#7](../../mfc/codesnippet/cpp/cobject-class_1.cpp)]

Другой пример см. в разделе [`AfxDoForAllObjects`](diagnostic-services.md#afxdoforallobjects) .

## <a name="cobjectcobject"></a><a name="cobject"></a> CObject:: CObject

Эти функции являются стандартными `CObject` конструкторами.

```cpp
CObject();
CObject(const CObject& objectSrc);
```

### <a name="parameters"></a>Параметры

*обжектсрк*\
Ссылка на другую `CObject`

### <a name="remarks"></a>Примечания

Версия по умолчанию автоматически вызывается конструктором производного класса.

Если класс является сериализуемым (он включает `IMPLEMENT_SERIAL` макрос), то в объявлении класса должен быть конструктор по умолчанию (конструктор без аргументов). Если конструктор по умолчанию не нужен, объявите закрытый или защищенный конструктор "Empty". Дополнительные сведения см. [в разделе `CObject` using ](../../mfc/using-cobject.md).

Стандартный конструктор копирования класса по умолчанию C++ выполняет копирование по элементу. Наличие закрытого `CObject` конструктора копий гарантирует, что если конструктор копии класса необходим, но недоступен, появится сообщение об ошибке компилятора. Если класс требует этой возможности, предоставьте конструктор копии.

### <a name="example"></a>Пример

[`CObList::CObList`](../../mfc/reference/coblist-class.md#coblist)Список `CAge` классов, используемых в `CObject` примерах, см. в разделе.

[!code-cpp[NVC_MFCCObjectSample#8](../../mfc/codesnippet/cpp/cobject-class_2.cpp)]

## <a name="cobjectdump"></a><a name="dump"></a> CObject::D УМП

Выводит содержимое объекта в [`CDumpContext`](../../mfc/reference/cdumpcontext-class.md) объект.

```cpp
virtual void Dump(CDumpContext& dc) const;
```

### <a name="parameters"></a>Параметры

*Постоянный*\
Контекст диагностического дампа для дампа обычно `afxDump` .

### <a name="remarks"></a>Примечания

При написании собственного класса следует переопределить `Dump` функцию, чтобы предоставить службы диагностики для себя и других пользователей класса. `Dump` `Dump` Перед печатью элементов данных, уникальных для производного класса, переопределение обычно вызывает функцию своего базового класса. `CObject::Dump` Выводит имя класса, если класс использует `IMPLEMENT_DYNAMIC` макрос или `IMPLEMENT_SERIAL` .

> [!NOTE]
> `Dump`Функция не должна печатать символ новой строки в конце выходных данных.

`Dump` вызовы имеют смысл только в отладочной версии библиотека Microsoft Foundation Class. Для условной компиляции должны быть заключены вызовы, объявления функций и реализации функций с `#ifdef _DEBUG` `#endif` операторами.

Поскольку `Dump` является **`const`** функцией, изменять состояние объекта во время дампа не разрешается.

[ `CDumpContext` Оператор вставки (<<)](../../mfc/reference/cdumpcontext-class.md#operator_lt_lt) вызывает `Dump` при `CObject` вставке указателя.

`Dump` разрешает только "ациклический" дамп объектов. Можно создать дамп списка объектов, например, но если один из объектов является самим списком, то в конечном итоге стек будет переполнен.

### <a name="example"></a>Пример

[`CObList::CObList`](../../mfc/reference/coblist-class.md#coblist)Список `CAge` классов, используемых во всех примерах, см `CObject` . в разделе.

[!code-cpp[NVC_MFCCObjectSample#9](../../mfc/codesnippet/cpp/cobject-class_3.cpp)]

## <a name="cobjectgetruntimeclass"></a><a name="getruntimeclass"></a> CObject:: Жетрунтимекласс

Возвращает `CRuntimeClass` структуру, соответствующую классу данного объекта.

```cpp
virtual CRuntimeClass* GetRuntimeClass() const;
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на структуру, [`CRuntimeClass`](../../mfc/reference/cruntimeclass-structure.md) соответствующую классу этого объекта, но никогда **`NULL`** .

### <a name="remarks"></a>Примечания

`CRuntimeClass`Для каждого `CObject` производного класса существует одна структура. Члены структуры выглядят следующим образом:

- **`LPCSTR m_lpszClassName`** Строка, заканчивающаяся нулем и содержащая имя класса ASCII.
- **`int m_nObjectSize`** Размер объекта в байтах. Если объект содержит элементы данных, указывающие на выделенную память, размер этой памяти не включается.
- **`UINT m_wSchema`** Номер схемы (-1 для несериализуемых классов). [`IMPLEMENT_SERIAL`](run-time-object-model-services.md#implement_serial)Описание номера схемы см. в макросе.

- **`CObject* (PASCAL* m_pfnCreateObject)()`** Указатель на функцию конструктора по умолчанию, который создает объект класса (действителен, только если класс поддерживает динамическое создание; в противном случае возвращает **`NULL`** ).

- **`CRuntimeClass* (PASCAL* m_pfn_GetBaseClass )()`** Если приложение динамически связано с AFXDLL версией MFC, указатель на функцию, возвращающую `CRuntimeClass` структуру базового класса.

- **`CRuntimeClass* m_pBaseClass`** Если приложение статически связано с MFC, указатель на `CRuntimeClass` структуру базового класса.

Эта функция требует использования [`IMPLEMENT_DYNAMIC`](run-time-object-model-services.md#implement_dynamic) [`IMPLEMENT_DYNCREATE`](run-time-object-model-services.md#implement_dyncreate) [`IMPLEMENT_SERIAL`](run-time-object-model-services.md#implement_serial) макроса, или в реализации класса. В противном случае вы получите неверные результаты.

### <a name="example"></a>Пример

[`CObList::CObList`](../../mfc/reference/coblist-class.md#coblist)Список `CAge` классов, используемых во всех примерах, см `CObject` . в разделе.

[!code-cpp[NVC_MFCCObjectSample#10](../../mfc/codesnippet/cpp/cobject-class_4.cpp)]

## <a name="cobjectiskindof"></a><a name="iskindof"></a> CObject:: IsKindOf

Проверяет связь этого объекта с заданным классом.

```cpp
BOOL IsKindOf(const CRuntimeClass* pClass) const;
```

### <a name="parameters"></a>Параметры

*`pClass`*\
Указатель на структуру, [`CRuntimeClass`](../../mfc/reference/cruntimeclass-structure.md) связанную с `CObject` классом, производным от.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если объект соответствует классу; в противном случае — 0.

### <a name="remarks"></a>Примечания

Эта функция проверяет *`pClass`* , является ли (1) объектом указанного класса, или (2) он является объектом класса, производного от указанного класса. Эта функция работает только для классов, объявленных с помощью [`DECLARE_DYNAMIC`](run-time-object-model-services.md#declare_dynamic) [`DECLARE_DYNCREATE`](run-time-object-model-services.md#declare_dyncreate) [`DECLARE_SERIAL`](run-time-object-model-services.md#declare_serial) макроса, или.

Не используйте эту функцию широко, так как она нарушает функцию полиморфизма C++. Вместо этого используйте виртуальные функции.

### <a name="example"></a>Пример

[`CObList::CObList`](../../mfc/reference/coblist-class.md#coblist)Список `CAge` классов, используемых во всех примерах, см `CObject` . в разделе.

[!code-cpp[NVC_MFCCObjectSample#11](../../mfc/codesnippet/cpp/cobject-class_5.cpp)]

## <a name="cobjectisserializable"></a><a name="isserializable"></a> CObject:: Serializable

Проверяет, подходит ли этот объект для сериализации.

```cpp
BOOL IsSerializable() const;
```

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если этот объект можно сериализовать; в противном случае — 0.

### <a name="remarks"></a>Примечания

Чтобы класс был сериализуемым, его объявление должно содержать [`DECLARE_SERIAL`](run-time-object-model-services.md#declare_serial) макрос, а реализация должна содержать [`IMPLEMENT_SERIAL`](run-time-object-model-services.md#implement_serial) макрос.

> [!NOTE]
> Не переопределяйте эту функцию.

### <a name="example"></a>Пример

[`CObList::CObList`](../../mfc/reference/coblist-class.md#coblist)Список `CAge` классов, используемых во всех примерах, см `CObject` . в разделе.

[!code-cpp[NVC_MFCCObjectSample#12](../../mfc/codesnippet/cpp/cobject-class_6.cpp)]

## <a name="cobjectoperator-delete"></a><a name="operator_delete"></a> Удаление CObject:: operator

Для версии выпуска библиотеки оператор **`delete`** освобождает память, выделенную оператором **`new`** .

```cpp
void PASCAL operator delete(void* p);

void PASCAL operator delete(
    void* p,
    void* pPlace);

void PASCAL operator delete(
    void* p,
    LPCSTR lpszFileName,
    int nLine);
```

### <a name="remarks"></a>Примечания

В отладочной версии оператор **`delete`** участвует в схеме мониторинга распределения, предназначенной для обнаружения утечек памяти.

При использовании строки кода

[!code-cpp[NVC_MFCCObjectSample#14](../../mfc/codesnippet/cpp/cobject-class_7.cpp)]

перед любой из реализаций в. CPP, будет использоваться третья версия, в которой **`delete`** будут храниться имя файла и номер строки в выделенном блоке для последующего создания отчетов. Вам не нужно беспокоиться о предоставлении дополнительных параметров. за вас позаботится макрос.

Даже если вы не используете `DEBUG_NEW` в режиме отладки, вы по-прежнему получаете возможность обнаружения утечек, но без описанных выше отчетов с исходными файлами.

Если вы переопределяете операторы **`new`** и **`delete`** , вы лишаете этой диагностической возможности.

### <a name="example"></a>Пример

[`CObList::CObList`](../../mfc/reference/coblist-class.md#coblist)Список `CAge` классов, используемых в `CObject` примерах, см. в разделе.

[!code-cpp[NVC_MFCCObjectSample#15](../../mfc/codesnippet/cpp/cobject-class_8.cpp)]

## <a name="cobjectoperator-new"></a><a name="operator_new"></a> CObject:: оператор New

Для окончательной версии библиотеки оператор **`new`** выполняет оптимальное выделение памяти таким же образом, как и `malloc` .

```cpp
void* PASCAL operator new(size_t nSize);
void* PASCAL operator new(size_t, void* p);

void* PASCAL operator new(
    size_t nSize,
    LPCSTR lpszFileName,
    int nLine);
```

### <a name="remarks"></a>Примечания

В отладочной версии оператор **`new`** участвует в схеме мониторинга распределения, предназначенной для обнаружения утечек памяти.

При использовании строки кода

[!code-cpp[NVC_MFCCObjectSample#14](../../mfc/codesnippet/cpp/cobject-class_7.cpp)]

перед любой из реализаций в. CPP, используется вторая версия **`new`** , которая сохраняет имя файла и номер строки в выделенном блоке для последующего создания отчетов. Вам не нужно беспокоиться о предоставлении дополнительных параметров. за вас позаботится макрос.

Даже если вы не используете `DEBUG_NEW` в режиме отладки, вы по-прежнему получаете возможность обнаружения утечек, но без описанных выше отчетов с исходными файлами.

> [!NOTE]
> При переопределении этого оператора необходимо также переопределить **`delete`** . Не используйте стандартную `_new_handler` функцию библиотеки.

### <a name="example"></a>Пример

[`CObList::CObList`](../../mfc/reference/coblist-class.md#coblist)Список `CAge` классов, используемых в `CObject` примерах, см. в разделе.

[!code-cpp[NVC_MFCCObjectSample#16](../../mfc/codesnippet/cpp/cobject-class_9.h)]

## <a name="cobjectserialize"></a><a name="serialize"></a> CObject:: Serialize

Считывает этот объект из архива или записывает в него.

```cpp
virtual void Serialize(CArchive& ar);
```

### <a name="parameters"></a>Параметры

*`ar`*\
`CArchive`Объект для сериализации в или из.

### <a name="remarks"></a>Примечания

Переопределите `Serialize` для каждого класса, который предполагается сериализовать. Переопределенный `Serialize` метод должен сначала вызвать `Serialize` функцию своего базового класса.

Кроме того, необходимо использовать [`DECLARE_SERIAL`](run-time-object-model-services.md#declare_serial) макрос в объявлении класса, и необходимо использовать [`IMPLEMENT_SERIAL`](run-time-object-model-services.md#implement_serial) макрос в реализации.

Используйте [`CArchive::IsLoading`](../../mfc/reference/carchive-class.md#isloading) или [`CArchive::IsStoring`](../../mfc/reference/carchive-class.md#isstoring) , чтобы определить, загружается ли архив или сохраняется.

`Serialize` вызывается методами [`CArchive::ReadObject`](../../mfc/reference/carchive-class.md#readobject) и [`CArchive::WriteObject`](../../mfc/reference/carchive-class.md#writeobject) . Эти функции связаны с `CArchive` оператором вставки ( **`<<`** ) и оператором извлечения ( **`>>`** ).

Примеры сериализации см. в статье [сериализация объекта](../../mfc/serialization-serializing-an-object.md).

### <a name="example"></a>Пример

[`CObList::CObList`](../../mfc/reference/coblist-class.md#coblist)Список `CAge` классов, используемых во всех примерах, см `CObject` . в разделе.

[!code-cpp[NVC_MFCCObjectSample#13](../../mfc/codesnippet/cpp/cobject-class_10.cpp)]

## <a name="see-also"></a>См. также

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)
