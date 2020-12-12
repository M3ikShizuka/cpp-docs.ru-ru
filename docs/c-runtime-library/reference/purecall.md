---
description: 'Дополнительные сведения: _purecall'
title: _purecall
ms.date: 4/2/2020
api_name:
- _purecall
- _o__purecall
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
- ntoskrnl.exe
- ucrtbase.dll
- api-ms-win-crt-private-l1-1-0.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- purecall
- _purecall
helpviewer_keywords:
- _purecall function
- purecall function
ms.assetid: 56135d9b-3403-4e22-822d-e714523801cc
ms.openlocfilehash: df52d7383685f3ce183562d8789b710fd7587acd
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97209455"
---
# <a name="_purecall"></a>_purecall

Обработчик ошибок вызовов чистой виртуальной функции по умолчанию. При вызове чистой виртуальной функции-члена компилятор создает код для вызова этой функции.

## <a name="syntax"></a>Синтаксис

```C
extern "C" int __cdecl _purecall();
```

## <a name="remarks"></a>Remarks

Функция **_purecall** является подробным описанием реализации компилятора Microsoft C++. Эта функция не предназначена для вызова непосредственно из кода и не содержит объявление открытого заголовка. Она описана здесь, так как это общий экспорт библиотеки времени выполнения C.

Вызов чистой виртуальной функции является ошибкой, так как она не имеет реализации. Компилятор создает код для вызова функции обработчика ошибок **_purecall** при вызове чистой виртуальной функции. По умолчанию **_purecall** прекращает выполнение программы. Перед завершением работы функция **_purecall** вызывает функцию **_purecall_handler** , если она была задана для процесса. Можно установить собственный обработчик ошибок для вызовов чистых виртуальных функций, который будет перехватывать их в целях отладки или ведения отчетности. Чтобы использовать собственный обработчик ошибок, создайте функцию с сигнатурой **_purecall_handler** , а затем используйте [_set_purecall_handler](get-purecall-handler-set-purecall-handler.md) , чтобы сделать ее текущим обработчиком.

По умолчанию глобальное состояние этой функции ограничивается приложением. Чтобы изменить это, см. раздел [глобальное состояние в CRT](../global-state.md).

## <a name="requirements"></a>Требования

Функция **_purecall** не имеет объявления заголовка. Определение **_purecall_handler** typedef определяется в \<stdlib.h> .

## <a name="see-also"></a>См. также раздел

[Алфавитный справочник по функциям](crt-alphabetical-function-reference.md)<br/>
[_get_purecall_handler, _set_purecall_handler](get-purecall-handler-set-purecall-handler.md)<br/>
