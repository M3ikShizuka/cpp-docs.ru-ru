---
description: 'Дополнительные сведения о: Кфилетиме Class'
title: Класс Кфилетиме
ms.date: 10/18/2018
f1_keywords:
- CFileTime
- ATLTIME/ATL::CFileTime
- ATLTIME/ATL::CFileTime::CFileTime
- ATLTIME/ATL::CFileTime::GetCurrentTime
- ATLTIME/ATL::CFileTime::GetTime
- ATLTIME/ATL::CFileTime::LocalToUTC
- ATLTIME/ATL::CFileTime::SetTime
- ATLTIME/ATL::CFileTime::UTCToLocal
- ATLTIME/ATL::CFileTime::Day
- ATLTIME/ATL::CFileTime::Hour
- ATLTIME/ATL::CFileTime::Millisecond
- ATLTIME/ATL::CFileTime::Minute
- ATLTIME/ATL::CFileTime::Second
- ATLTIME/ATL::CFileTime::Week
helpviewer_keywords:
- CFileTime class
- shared classes, CFileTime
ms.assetid: 1a358a65-1383-4124-b0d4-59b026e6860f
ms.openlocfilehash: 95b46c188be60da787612a30ebff161a4ecf5966
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97166854"
---
# <a name="cfiletime-class"></a>Класс Кфилетиме

Этот класс предоставляет методы для управления значениями даты и времени, связанными с файлом.

## <a name="syntax"></a>Синтаксис

```
class CFileTime :  public FILETIME
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кфилетиме:: Кфилетиме](#cfiletime)|Конструктор.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кфилетиме:: Жеткурренттиме](#getcurrenttime)|Вызовите эту статическую функцию, чтобы получить `CFileTime` объект, представляющий текущую системную дату и время.|
|[Кфилетиме:: во время](#gettime)|Вызовите этот метод, чтобы получить время из `CFileTime` объекта.|
|[Кфилетиме:: Локалтаутк](#localtoutc)|Вызовите этот метод, чтобы преобразовать время местного файла в файловый момент на основе времени в формате UTC.|
|[Кфилетиме:: SetTime](#settime)|Вызовите этот метод, чтобы задать дату и время, хранимые в `CFileTime` объекте.|
|[Кфилетиме:: Утктолокал](#utctolocal)|Вызывайте этот метод для преобразования времени, основанного на времени в формате UTC, в местное время файла.|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[Кфилетиме:: operator —](#operator_-)|Этот оператор используется для выполнения вычитания `CFileTime` `CFileTimeSpan` объекта или.|
|[Кфилетиме:: operator! =](#operator_neq)|Этот оператор сравнивает два `CFileTime` объекта на неравенство.|
|[Кфилетиме:: operator +](#operator_add)|Этот оператор используется для сложения объекта `CFileTimeSpan`.|
|[Кфилетиме:: operator + =](#operator_add_eq)|Этот оператор используется для сложения объекта `CFileTimeSpan` и назначения ему результата.|
|[Кфилетиме:: operator &lt;](#operator_lt)|Этот оператор сравнивает два объекта `CFileTime`, чтобы определить меньший из них.|
|[Кфилетиме:: operator &lt;=](#operator_lt_eq)|Этот оператор сравнивает два объекта `CFileTime`, чтобы определить равенство или меньший из них.|
|[Кфилетиме:: operator =](#operator_eq)|Оператор присваивания.|
|[Кфилетиме:: operator-=](#operator_-_eq)|Этот оператор используется для выполнения вычитания `CFileTimeSpan` объекта и присвоения результата текущему объекту.|
|[Кфилетиме:: operator = =](#operator_eq_eq)|Этот оператор сравнивает два объекта `CFileTime` на равенство.|
|[Кфилетиме:: operator &gt;](#operator_gt)|Этот оператор сравнивает два объекта `CFileTime`, чтобы определить больший из них.|
|[Кфилетиме:: operator &gt;=](#operator_gt_eq)|Этот оператор сравнивает два объекта `CFileTime`, чтобы определить равенство или больший из них.|

### <a name="public-constants"></a>Открытые константы

|Имя|Описание|
|----------|-----------------|
|[Кфилетиме::D гг](#day)|Статический элемент данных, в котором хранится число 100-наносекундных интервалов, которые составляют один день.|
|[Кфилетиме:: Hour](#hour)|Статический элемент данных, в котором хранится число 100-наносекундных интервалов, составляющих один час.|
|[Кфилетиме:: миллисекунда](#millisecond)|Статический элемент данных, в котором хранится число 100-наносекундных интервалов, составляющих одну миллисекунду.|
|[Кфилетиме:: Minute](#minute)|Статический элемент данных, в котором хранится число 100-наносекундных интервалов, составляющих одну минуту.|
|[Кфилетиме:: Second](#second)|Статический элемент данных, в котором хранится число 100-наносекундных интервалов, которые составляют одну секунду.|
|[Кфилетиме:: неделя](#week)|Статический элемент данных, в котором хранится число 100-наносекундных интервалов, которые составляют одну неделю.|

## <a name="remarks"></a>Комментарии

Этот класс предоставляет методы для управления значениями даты и времени, связанными с созданием, доступом и изменением файлов. Методы и данные этого класса часто используются вместе с `CFileTimeSpan` объектами, которые имеют отношение к относительным значениям времени.

Значение даты и времени сохраняется как 64-разрядное значение, представляющее число 100-наносекундных интервалов с 1 января 1601 г. Это формат всеобщего скоординированного времени (UTC).

Для упрощения вычислений предоставляются следующие статические переменные членов константы:

|Переменная-член|Число интервалов в 100-наносекундных|
|---------------------|-----------------------------------------|
|Миллисекунда|10 000|
|Second|Миллисекунда \* 1 000|
|Минута|Второй \* 60|
|Час|Минута \* 60|
|День|Час \* 24|
|Неделя|День \* 7|

**Примечание** . Не все файловые системы могут записывать время создания и последнего доступа, а не все файловые системы записывают их одинаковым образом. Например, в файловой системе Windows NT FAT время создания имеет разрешение 10 миллисекунд, время записи имеет разрешение 2 секунды, а время доступа имеет разрешение в 1 день (Дата доступа). В файловой системе NTFS время доступа имеет разрешение 1 час. Кроме того, FAT записывает время на диск по местному времени, но NTFS записывает время на диск в формате UTC. Дополнительные сведения см. в разделе [время файла](/windows/win32/SysInfo/file-times).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`FILETIME`

`CFileTime`

## <a name="requirements"></a>Требования

**Заголовок:** атлтиме. h

## <a name="cfiletimecfiletime"></a><a name="cfiletime"></a> Кфилетиме:: Кфилетиме

Конструктор.

```
CFileTime() throw();
CFileTime(const FILETIME& ft) throw();
CFileTime(ULONGLONG nTime) throw();
```

### <a name="parameters"></a>Параметры

*ФТ*<br/>
Структура [fileTime](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .

*Nвремя*<br/>
Дата и время, выраженные в виде 64-разрядного значения.

### <a name="remarks"></a>Комментарии

`CFileTime`Объект можно создать с помощью существующей даты и времени из `FILETIME` структуры или выражается в виде 64-разрядного значения (в формате UTC). Конструктор по умолчанию устанавливает время равным 0.

## <a name="cfiletimeday"></a><a name="day"></a> Кфилетиме::D гг

Статический элемент данных, в котором хранится число 100-наносекундных интервалов, которые составляют один день.

```
static const ULONGLONG Day = Hour* 24;
```

### <a name="example"></a>Пример

См. пример для [кфилетиме:: миллисекунд](#millisecond).

## <a name="cfiletimegetcurrenttime"></a><a name="getcurrenttime"></a> Кфилетиме:: Жеткурренттиме

Вызовите эту статическую функцию, чтобы получить `CFileTime` объект, представляющий текущую системную дату и время.

```
static CFileTime GetCurrentTime() throw();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает текущую системную дату и время в формате всеобщего скоординированного времени (UTC).

### <a name="example"></a>Пример

[!code-cpp[NVC_MFCFiles#41](../../atl-mfc-shared/reference/codesnippet/cpp/cfiletime-class_1.cpp)]

## <a name="cfiletimegettime"></a><a name="gettime"></a> Кфилетиме:: во время

Вызовите этот метод, чтобы получить время из `CFileTime` объекта.

```
ULONGLONG GetTime() const throw();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает дату и время в виде 64-разрядного числа, которое может быть в локальном или универсальном формате времени (UTC).

## <a name="cfiletimehour"></a><a name="hour"></a> Кфилетиме:: Hour

Статический элемент данных, в котором хранится число 100-наносекундных интервалов, составляющих один час.

```
static const ULONGLONG Hour = Minute* 60;
```

### <a name="example"></a>Пример

См. пример для [кфилетиме:: миллисекунд](#millisecond).

## <a name="cfiletimelocaltoutc"></a><a name="localtoutc"></a> Кфилетиме:: Локалтаутк

Вызовите этот метод, чтобы преобразовать время местного файла в файловый момент на основе времени в формате UTC.

```
CFileTime LocalToUTC() const throw();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает `CFileTime` объект, содержащий время в формате UTC.

### <a name="example"></a>Пример

См. пример для [кфилетиме:: утктолокал](#utctolocal).

## <a name="cfiletimemillisecond"></a><a name="millisecond"></a> Кфилетиме:: миллисекунда

Статический элемент данных, в котором хранится число 100-наносекундных интервалов, составляющих одну миллисекунду.

```
static const ULONGLONG Millisecond = 10000;
```

### <a name="example"></a>Пример

[!code-cpp[NVC_MFCFiles#44](../../atl-mfc-shared/reference/codesnippet/cpp/cfiletime-class_2.cpp)]

## <a name="cfiletimeminute"></a><a name="minute"></a> Кфилетиме:: Minute

Статический элемент данных, в котором хранится число 100-наносекундных интервалов, составляющих одну минуту.

```
static const ULONGLONG Minute = Second* 60;
```

### <a name="example"></a>Пример

См. пример для [кфилетиме:: миллисекунд](#millisecond).

## <a name="cfiletimeoperator--"></a><a name="operator_-"></a> Кфилетиме:: operator —

Этот оператор используется для выполнения вычитания `CFileTime` `CFileTimeSpan` объекта или.

```
CFileTime operator-(CFileTimeSpan span) const throw();
CFileTimeSpan operator-(CFileTime ft) const throw();
```

### <a name="parameters"></a>Параметры

*размещать*<br/>
Объект `CFileTimeSpan`.

*ФТ*<br/>
Объект `CFileTime`.

### <a name="return-value"></a>Возвращаемое значение

Возвращает `CFileTime` объект или объект, `CFileTimeSpan` представляющий результат разницы во времени между двумя объектами.

## <a name="cfiletimeoperator-"></a><a name="operator_neq"></a> Кфилетиме:: operator! =

Этот оператор сравнивает два `CFileTime` объекта на неравенство.

```
bool operator!=(CFileTime ft) const throw();
```

### <a name="parameters"></a>Параметры

*ФТ*<br/>
Сравниваемый объект `CFileTime`.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение TRUE, если сравниваемый элемент не равен объекту; `CFileTime` в противном случае — значение false.

## <a name="cfiletimeoperator-"></a><a name="operator_add"></a> Кфилетиме:: operator +

Этот оператор используется для сложения объекта `CFileTimeSpan`.

```
CFileTime operator+(CFileTimeSpan span) const throw();
```

### <a name="parameters"></a>Параметры

*размещать*<br/>
Объект `CFileTimeSpan`.

### <a name="return-value"></a>Возвращаемое значение

Возвращает `CFileTime` объект, представляющий результат исходного времени плюс относительное время.

## <a name="cfiletimeoperator-"></a><a name="operator_add_eq"></a> Кфилетиме:: operator + =

Этот оператор используется для сложения объекта `CFileTimeSpan` и назначения ему результата.

```
CFileTime& operator+=(CFileTimeSpan span) throw();
```

### <a name="parameters"></a>Параметры

*размещать*<br/>
Объект `CFileTimeSpan`.

### <a name="return-value"></a>Возвращаемое значение

Возвращает обновленный `CFileTime` объект, представляющий результат исходного времени плюс относительное время.

## <a name="cfiletimeoperator-lt"></a><a name="operator_lt"></a> Кфилетиме:: operator &lt;

Этот оператор сравнивает два объекта `CFileTime`, чтобы определить меньший из них.

```
bool operator<(CFileTime ft) const throw();
```

### <a name="parameters"></a>Параметры

*ФТ*<br/>
Сравниваемый объект `CFileTime`.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение TRUE, если первый объект меньше второго объекта, и FALSE в противном случае.

### <a name="example"></a>Пример

[!code-cpp[NVC_MFCFiles#43](../../atl-mfc-shared/reference/codesnippet/cpp/cfiletime-class_3.cpp)]

## <a name="cfiletimeoperator-lt"></a><a name="operator_lt_eq"></a> Кфилетиме:: operator &lt;=

Этот оператор сравнивает два объекта `CFileTime`, чтобы определить равенство или меньший из них.

```
bool operator<=(CFileTime ft) const throw();
```

### <a name="parameters"></a>Параметры

*ФТ*<br/>
Сравниваемый объект `CFileTime`.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение TRUE, если первый объект меньше (ранее по времени) или равен второму; в противном случае — значение FALSE.

## <a name="cfiletimeoperator-"></a><a name="operator_eq"></a> Кфилетиме:: operator =

Оператор присваивания.

```
CFileTime& operator=(const FILETIME& ft) throw();
```

### <a name="parameters"></a>Параметры

*ФТ*<br/>
`CFileTime`Объект, содержащий новое время и дату.

### <a name="return-value"></a>Возвращаемое значение

Возвращает обновленный `CFileTime` объект.

## <a name="cfiletimeoperator--"></a><a name="operator_-_eq"></a> Кфилетиме:: operator-=

Этот оператор используется для выполнения вычитания `CFileTimeSpan` объекта и присвоения результата текущему объекту.

```
CFileTime& operator-=(CFileTimeSpan span) throw();
```

### <a name="parameters"></a>Параметры

*размещать*<br/>
`CFileTimeSpan`Объект, содержащий относительное время для вычитания.

### <a name="return-value"></a>Возвращаемое значение

Возвращает обновленный `CFileTime` объект.

## <a name="cfiletimeoperator-"></a><a name="operator_eq_eq"></a> Кфилетиме:: operator = =

Этот оператор сравнивает два объекта `CFileTime` на равенство.

```
bool operator==(CFileTime ft) const throw();
```

### <a name="parameters"></a>Параметры

*ФТ*<br/>
Объект `CFileTime`, подлежащий сравнению.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение TRUE, если объекты равны; в противном случае — значение FALSE.

## <a name="cfiletimeoperator-gt"></a><a name="operator_gt"></a> Кфилетиме:: operator &gt;

Этот оператор сравнивает два объекта `CFileTime`, чтобы определить больший из них.

```
bool operator>(CFileTime ft) const throw();
```

### <a name="parameters"></a>Параметры

*ФТ*<br/>
Сравниваемый объект `CFileTime`.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение TRUE, если первый объект больше, чем второй, в противном случае — значение FALSE.

## <a name="cfiletimeoperator-gt"></a><a name="operator_gt_eq"></a> Кфилетиме:: operator &gt;=

Этот оператор сравнивает два объекта `CFileTime`, чтобы определить равенство или больший из них.

```
bool operator>=(CFileTime ft) const throw();
```

### <a name="parameters"></a>Параметры

*ФТ*<br/>
Сравниваемый объект `CFileTime`.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение TRUE, если первый объект больше (позже по времени) или равен второму, в противном случае — FALSE.

## <a name="cfiletimesecond"></a><a name="second"></a> Кфилетиме:: Second

Статический элемент данных, в котором хранится число 100-наносекундных интервалов, которые составляют один день.

```
static const ULONGLONG Second = Millisecond* 1000;
```

### <a name="example"></a>Пример

См. пример для [кфилетиме:: миллисекунд](#millisecond).

## <a name="cfiletimesettime"></a><a name="settime"></a> Кфилетиме:: SetTime

Вызовите этот метод, чтобы задать дату и время, хранимые в `CFileTime` объекте.

```cpp
void SetTime(ULONGLONG nTime) throw();
```

### <a name="parameters"></a>Параметры

*Nвремя*<br/>
64-разрядное значение, представляющее дату и время в формате местного или всеобщего скоординированного времени (UTC).

## <a name="cfiletimeutctolocal"></a><a name="utctolocal"></a> Кфилетиме:: Утктолокал

Вызывайте этот метод для преобразования времени, основанного на времени в формате UTC, в местное время файла.

```
CFileTime UTCToLocal() const throw();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает `CFileTime` объект, содержащий время в формате местного времени файла.

### <a name="example"></a>Пример

[!code-cpp[NVC_MFCFiles#42](../../atl-mfc-shared/reference/codesnippet/cpp/cfiletime-class_4.cpp)]

## <a name="cfiletimeweek"></a><a name="week"></a> Кфилетиме:: неделя

Статический элемент данных, в котором хранится число 100-наносекундных интервалов, которые составляют одну неделю.

```
static const ULONGLONG Week = Day* 7;
```

### <a name="example"></a>Пример

См. пример для [кфилетиме:: миллисекунд](#millisecond).

## <a name="see-also"></a>См. также раздел

[FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime)<br/>
[Класс Кфилетимеспан](../../atl-mfc-shared/reference/cfiletimespan-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Общие классы ATL и MFC](../../atl-mfc-shared/atl-mfc-shared-classes.md)
