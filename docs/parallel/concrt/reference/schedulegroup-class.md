---
description: 'Дополнительные сведения о: ScheduleGroup Class'
title: Класс ScheduleGroup
ms.date: 11/04/2016
f1_keywords:
- ScheduleGroup
- CONCRT/concurrency::ScheduleGroup
- CONCRT/concurrency::ScheduleGroup::Id
- CONCRT/concurrency::ScheduleGroup::Reference
- CONCRT/concurrency::ScheduleGroup::Release
- CONCRT/concurrency::ScheduleGroup::ScheduleTask
helpviewer_keywords:
- ScheduleGroup class
ms.assetid: 86d380ff-f2e8-411c-b1a8-22bd3079824a
ms.openlocfilehash: ca6678cd8d8c13c5d62b3d98b0a0bb1ab14e29c9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97188915"
---
# <a name="schedulegroup-class"></a>Класс ScheduleGroup

Представляет абстракцию для группы расписаний. Группы расписаний организуют набор связанных работ, которые выигрывают от планирования в непосредственной близости друг от друга: во времени (путем выполнения другой задачи в той же группе перед перемещением в другую группу) или в пространстве (путем выполнения нескольких элементов в той же группе в том же узле NUMA или физическом сокете).

## <a name="syntax"></a>Синтаксис

```cpp
class ScheduleGroup;
```

## <a name="members"></a>Члены

### <a name="protected-constructors"></a>Защищенные конструкторы

|Имя|Описание|
|----------|-----------------|
|[Деструктор ~ ScheduleGroup](#dtor)||

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Id](#id)|Возвращает идентификатор для группы расписаний, уникальный в пределах планировщика, к которому принадлежит группа.|
|[Ссылки](#reference)|Увеличивает значение счетчика ссылок группы расписания.|
|[Релиз](#release)|Уменьшает значение счетчика ссылок группы планировщика.|
|[ScheduleTask](#scheduletask)|Планирует облегченную задачу в группе расписаний.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`ScheduleGroup`

## <a name="requirements"></a>Требования

**Заголовок:** ConcRT. h

**Пространство имен:** параллелизм

## <a name="id"></a><a name="id"></a> Удостоверения

Возвращает идентификатор для группы расписаний, уникальный в пределах планировщика, к которому принадлежит группа.

```cpp
virtual unsigned int Id() const = 0;
```

### <a name="return-value"></a>Возвращаемое значение

Идентификатор группы расписаний, уникальный в пределах планировщика, к которому принадлежит группа.

## <a name="operator-delete"></a><a name="operator_delete"></a> оператор DELETE

`ScheduleGroup`Объект внутренне уничтожается средой выполнения, когда все внешние ссылки на него освобождаются. Его невозможно удалить явно.

```cpp
void operator delete(
    void* _PObject);

void operator delete(
    void* _PObject,
    int,
const char *,
    int);
```

### <a name="parameters"></a>Параметры

*_PObject*<br/>
Указатель на удаляемый объект.

## <a name="reference"></a><a name="reference"></a> IsReference

Увеличивает значение счетчика ссылок группы расписания.

```cpp
virtual unsigned int Reference() = 0;
```

### <a name="return-value"></a>Возвращаемое значение

Вновь увеличивающееся число ссылок.

### <a name="remarks"></a>Комментарии

Обычно это используется для управления временем существования группы расписаний для композиции. Если количество ссылок группы расписаний становится равным нулю, Группа расписаний удаляется средой выполнения. Группа расписаний, созданная с помощью метода [CurrentScheduler:: CreateScheduleGroup](currentscheduler-class.md#createschedulegroup) или метода [Scheduler:: CreateScheduleGroup](scheduler-class.md#createschedulegroup) , начинается со счетчика ссылок одного из них.

## <a name="release"></a><a name="release"></a> Отпускании

Уменьшает значение счетчика ссылок группы планировщика.

```cpp
virtual unsigned int Release() = 0;
```

### <a name="return-value"></a>Возвращаемое значение

Вновь уменьшенное число ссылок.

### <a name="remarks"></a>Комментарии

Обычно это используется для управления временем существования группы расписаний для композиции. Если количество ссылок группы расписаний становится равным нулю, Группа расписаний удаляется средой выполнения. После вызова `Release` метода определенное число раз для удаления счетчика ссылок на создание и любых дополнительных ссылок, помещенных с помощью `Reference` метода, вы не сможете использовать группу расписаний дальше. Это приведет к неопределенному поведению.

Группа расписаний связана с определенным экземпляром планировщика. Необходимо убедиться, что все ссылки на группу расписаний освобождены до выпуска всех ссылок на планировщик, так как Последнее может привести к уничтожению планировщика. В противном случае это приведет к неопределенному поведению.

## <a name="schedulegroup"></a><a name="dtor"></a> ~ ScheduleGroup

```cpp
virtual ~ScheduleGroup();
```

## <a name="scheduletask"></a><a name="scheduletask"></a> ScheduleTask

Планирует облегченную задачу в группе расписаний.

```cpp
virtual void ScheduleTask(
    TaskProc _Proc,
    _Inout_opt_ void* _Data) = 0;
```

### <a name="parameters"></a>Параметры

*_Proc*<br/>
Указатель на функцию, которая должна быть выполнена, чтобы выполнить задачу неплотности.

*_Data*<br/>
Указатель типа void на данные, которые будут переданы в качестве параметра в текст задачи.

### <a name="remarks"></a>Комментарии

Вызов `ScheduleTask` метода неявно помещает счетчик ссылок на группу расписаний, которая удаляется средой выполнения в соответствующее время после выполнения задачи.

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)<br/>
[Класс CurrentScheduler](currentscheduler-class.md)<br/>
[Класс Scheduler](scheduler-class.md)<br/>
[Планировщик заданий](../../../parallel/concrt/task-scheduler-concurrency-runtime.md)
