---
description: 'Дополнительные сведения: Raise'
title: raise
ms.date: 4/2/2020
api_name:
- raise
- _o_raise
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
- api-ms-win-crt-runtime-l1-1-0.dll
- api-ms-win-crt-private-l1-1-0.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- Raise
helpviewer_keywords:
- signals, sending to executing programs
- raise function
- signals
- programs [C++], sending signals to executing programs
ms.openlocfilehash: eb225e25ef0ff4e04f1ea8877a434c2af240cbfe
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97274870"
---
# <a name="raise"></a>raise

Отправляет сигнал выполняемой программе.

> [!NOTE]
> Не используйте этот метод для завершения работы Microsoft Store приложения, за исключением сценариев тестирования или отладки. В соответствии с [политиками Microsoft Store](/legal/windows/agreements/store-policies)не разрешено закрывать приложения Магазина программным способом или с помощью пользовательского интерфейса. Дополнительные сведения см. в статье [жизненный цикл приложения UWP](/windows/uwp/launch-resume/app-lifecycle).

## <a name="syntax"></a>Синтаксис

```C
int raise(
   int sig
);
```

### <a name="parameters"></a>Параметры

*SIG*<br/>
Сигнал, который требуется инициализировать.

## <a name="return-value"></a>Возвращаемое значение

В случае успеха **raise** возвращает 0. В противном случае возвращается ненулевое значение.

## <a name="remarks"></a>Комментарии

Функция **raise** отправляет сигнал *sig* выполняемой программе. Если предыдущий вызов **signal** установил функцию обработки сигнала для *sig*, **raise** выполняет эту функцию. Если функция обработчика не была установлена, то выполняется действие по умолчанию, связанное со значением сигнала *sig*, как показано ниже.

|Сигнал|Значение|Значение по умолчанию|
|------------|-------------|-------------|
|**SIGABRT**|Аварийное завершение|Завершает вызывающую программу с кодом выхода 3|
|**SIGFPE**|Ошибка с плавающей запятой|Завершает вызывающую программу|
|**SIGILL**|Недопустимая инструкция|Завершает вызывающую программу|
|**SIGINT**|Прерывание CTRL+C|Завершает вызывающую программу|
|**SIGSEGV**|Недопустимый доступ к хранилищу|Завершает вызывающую программу|
|**SIGTERM**|Запрос на прекращение, отправленный в программу|Игнорирует сигнал|

Если аргумент не является допустимым сигналом, как указано выше, вызывается обработчик недопустимого параметра, как описано в статье [Проверка параметров](../../c-runtime-library/parameter-validation.md). Если не обработано, функция **устанавливает значение** « **еинвал** » и возвращает ненулевую величину.

По умолчанию глобальное состояние этой функции ограничивается приложением. Чтобы изменить это, см. раздел [глобальное состояние в CRT](../global-state.md).

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**raise**|\<signal.h>|

Дополнительные сведения о совместимости см. в статье [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="see-also"></a>См. также раздел

[Управление процессами и средой](../../c-runtime-library/process-and-environment-control.md)<br/>
[рвал](abort.md)<br/>
[signal](signal.md);<br/>
