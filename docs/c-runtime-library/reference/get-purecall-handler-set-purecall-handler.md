---
description: 'Дополнительные сведения: _get_purecall_handler, _set_purecall_handler'
title: _get_purecall_handler, _set_purecall_handler
ms.date: 1/14/2021
api_name:
- _set_purecall_handler
- _set_purecall_handler_m
- _get_purecall_handler
api_location:
- msvcrt.dll
- msvcr80.dll
- msvcr90.dll
- msvcr100.dll
- msvcr100_clr0400.dll
- msvcr110.dll
- msvcr110_clr0400.dll
- msvcr120.dll
- msvcr120_clr0400.dll
- ucrtbase.dll
- api-ms-win-crt-private-l1-1-0.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- _set_purecall_handler
- _set_purecall_handler_m
- set_purecall_handler_m
- set_purecall_handler
- stdlib/_set_purecall_handler
- stdlib/_get_purecall_handler
- _get_purecall_handler
helpviewer_keywords:
- _set_purecall_handler function
- set_purecall_handler function
- purecall_handler
- set_purecall_handler_m function
- _purecall_handler
- _set_purecall_handler_m function
- _get_purecall_handler function
ms.assetid: 2759b878-8afa-4129-86e7-72afc2153d9c
ms.openlocfilehash: d46e5848f440449cedaaa66c591d2814dbac0745
ms.sourcegitcommit: 1cd8f8a75fd036ffa57bc70f3ca869042d8019d4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "98242609"
---
# <a name="_get_purecall_handler-_set_purecall_handler"></a>_get_purecall_handler, _set_purecall_handler

Получает или задает обработчик ошибок для вызова чистой виртуальной функции.

## <a name="syntax"></a>Синтаксис

```cpp
typedef void (__cdecl* _purecall_handler)(void);
_purecall_handler __cdecl _get_purecall_handler(void);
_purecall_handler __cdecl _set_purecall_handler(
   _purecall_handler function
);
```

### <a name="parameters"></a>Параметры

*function*<br/>
Эту функцию необходимо вызывать при вызове чистой виртуальной функции. Функция **_purecall_handler** должна иметь тип возвращаемого значения void.

## <a name="return-value"></a>Возвращаемое значение

Предыдущая **_purecall_handler**. Возвращает **`nullptr`** , если предыдущий обработчик отсутствует.

## <a name="remarks"></a>Комментарии

Функции **_get_purecall_handler** и **_set_purecall_handler** являются специфичными для Microsoft и применяются только к коду C++.

Вызов чистой виртуальной функции является ошибкой, так как она не имеет реализации. По умолчанию компилятор создает код для вызова функции обработчика ошибок при вызове чистой виртуальной функции, который завершает программу. Можно установить собственный обработчик ошибок для вызовов чистых виртуальных функций, который будет перехватывать их в целях отладки или ведения отчетности. Чтобы использовать собственный обработчик ошибок, создайте функцию с сигнатурой **_purecall_handler** , а затем используйте **_set_purecall_handler** , чтобы сделать ее текущим обработчиком.

Поскольку существует только один **_purecall_handler** для каждого процесса, при вызове **_set_purecall_handler** он немедленно влияет на все потоки. Последний вызывающий элемент в любом потоке задает обработчик.

Чтобы восстановить поведение по умолчанию, вызовите **_set_purecall_handler** с помощью **`nullptr`** аргумента.

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**_get_purecall_handler**, **_set_purecall_handler**|\<cstdlib> или \<stdlib.h>|

Сведения о совместимости см. в разделе [Совместимость](../../c-runtime-library/compatibility.md).

## <a name="example"></a>Пример

```cpp
// _set_purecall_handler.cpp
// compile with: /W1
#include <tchar.h>
#include <stdio.h>
#include <stdlib.h>

class CDerived;
class CBase
{
public:
   CBase(CDerived *derived): m_pDerived(derived) {};
   ~CBase();
   virtual void function(void) = 0;

   CDerived * m_pDerived;
};

class CDerived : public CBase
{
public:
   CDerived() : CBase(this) {};   // C4355
   virtual void function(void) {};
};

CBase::~CBase()
{
   m_pDerived -> function();
}

void myPurecallHandler(void)
{
   printf("In _purecall_handler.");
   exit(0);
}

int _tmain(int argc, _TCHAR* argv[])
{
   _set_purecall_handler(myPurecallHandler);
   CDerived myDerived;
}
```

```Output
In _purecall_handler.
```

## <a name="see-also"></a>См. также

[Обработка ошибок](../../c-runtime-library/error-handling-crt.md)<br/>
[_purecall](purecall.md)<br/>
