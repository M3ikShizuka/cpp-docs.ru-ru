---
description: 'Дополнительные сведения о: progress_reporter классе'
title: Класс progress_reporter
ms.date: 11/04/2016
f1_keywords:
- progress_reporter
- PPLTASKS/concurrency::progress_reporter
- PPLTASKS/concurrency::progress_reporter::progress_reporter
- PPLTASKS/concurrency::progress_reporter::report
helpviewer_keywords:
- progress_reporter class
ms.assetid: b836efab-2d05-4649-b6fa-d15236f1f813
ms.openlocfilehash: 40ae3dba0c804381478d8c32da4425b20a9825d9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97169363"
---
# <a name="progress_reporter-class"></a>Класс progress_reporter

Класс формирования отчетов о ходе выполнения позволяет формировать уведомления о ходе выполнения определенного типа. Каждый объект progress_reporter привязан к конкретному асинхронному действию или операции.

## <a name="syntax"></a>Синтаксис

```cpp
template<typename _ProgressType>
class progress_reporter;
```

### <a name="parameters"></a>Параметры

*_ProgressType*<br/>
О типе полезных данных каждого уведомления о ходе выполнения сообщается посредством формирования отчетов о ходе выполнения.

## <a name="members"></a>Элементы

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[progress_reporter](#ctor)||

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[report](#report) (отчет).|Отправляет отчет о ходе выполнения в асинхронное действие или операцию, к которому привязано это средство формирования отчетов.|

## <a name="remarks"></a>Комментарии

Этот тип доступен только для среда выполнения Windows приложений.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`progress_reporter`

## <a name="requirements"></a>Требования

**Заголовок:** из ppltasks. h

**Пространство имен:** параллелизм

## <a name="progress_reporter"></a><a name="ctor"></a> progress_reporter

```cpp
progress_reporter();
```

## <a name="report"></a><a name="report"></a> передачи

Отправляет отчет о ходе выполнения в асинхронное действие или операцию, к которому привязано это средство формирования отчетов.

```cpp
void report(const _ProgressType& val) const;
```

### <a name="parameters"></a>Параметры

*Val*<br/>
Полезные данные для отчета о ходе выполнения.

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)
