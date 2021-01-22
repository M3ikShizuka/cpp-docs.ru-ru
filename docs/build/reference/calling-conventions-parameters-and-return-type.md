---
description: 'Дополнительные сведения: соглашения о вызовах отложенной загрузки, параметры и тип возвращаемого значения'
title: Соглашения о вызовах, параметры и тип возвращаемого значения
ms.date: 01/19/2021
helpviewer_keywords:
- calling conventions, helper functions
- helper functions, calling conventions
- helper functions, return types
ms.openlocfilehash: 68817f2746abccf9ad6ae72c4f189fa29aa4c26f
ms.sourcegitcommit: 3d9cfde85df33002e3b3d7f3509ff6a8dc4c0a21
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "98666931"
---
# <a name="delay-load-helper-calling-conventions-parameters-and-return-type"></a>Соглашения о вызовах, параметры и тип возвращаемого значения в методах задержки загрузки

Прототип подпрограммы для вспомогательной загрузки с задержкой:

```C
FARPROC WINAPI __delayLoadHelper2(
    PCImgDelayDescr pidd,
    FARPROC * ppfnIATEntry
);
```

## <a name="parameters"></a>Параметры

*`pidd`*<br/>
**`const`** Указатель на объект `ImgDelayDescr` , содержащий смещения различных данных, связанных с импортом, отметку времени для данных привязки и набор атрибутов, которые предоставляют дополнительные сведения о содержимом дескриптора. В настоящее время существует только один атрибут, `dlattrRva` который указывает, что адреса в дескрипторе являются относительными виртуальными адресами. Дополнительные сведения см. в объявлениях в разделе *`delayimp.h`* .

Описание `PCImgDelayDescr` структуры см. в разделе [определения структуры и константы](structure-and-constant-definitions.md).

*`ppfnIATEntry`*<br/>
Указатель на слот в таблице адресов импорта с отложенной загрузкой (IAT). Это слот, который обновляется с адресом импортированной функции. Вспомогательная подпрограммы должна хранить то же значение, которое она возвращает в это расположение.

## <a name="expected-return-values"></a>Ожидаемые возвращаемые значения

Если функция выполнена успешно, она возвращает адрес импортированной функции.

Если функция завершается ошибкой, она вызывает структурированное исключение и возвращает 0. Возможны три типа исключений.

- Недопустимый параметр, который происходит, если атрибуты в *`pidd`* заданы неправильно.

- Функции `LoadLibrary` не удалось загрузить указанную библиотеку DLL.

- Ошибка в функции `GetProcAddress`.

Вы отвечаете за обработку этих исключений.

## <a name="remarks"></a>Примечания

Соглашение о вызовах для вспомогательной функции — **`__stdcall`** . Тип возвращаемого значения не важен, поэтому `FARPROC` используется. Эта функция имеет компоновку C, что означает необходимость заключения ее в оболочку `extern "C"` при объявлении в коде C++. `ExternC`Этот упаковщик используется макросом.

Сохраните возвращаемое значение вспомогательной функции в расположении указателя на переданную функцию, если вы не хотите использовать вспомогательную подпрограммы в качестве обработчика уведомлений. В этом случае за поиск необходимого возвращаемого указателя на функцию отвечает пользовательский код. Затем код преобразователя, создаваемый компоновщиком, принимает это возвращаемое значение в качестве действительной цели импорта и переходит непосредственно к ней.

## <a name="sample"></a>Образец

В следующем коде показано, как реализовать базовую функцию-обработчик.

```C
FARPROC WINAPI delayHook(unsigned dliNotify, PDelayLoadInfo pdli)
{
    switch (dliNotify) {
        case dliStartProcessing :

            // If you want to return control to the helper, return 0.
            // Otherwise, return a pointer to a FARPROC helper function
            // that will be used instead, thereby bypassing the rest
            // of the helper.

            break;

        case dliNotePreLoadLibrary :

            // If you want to return control to the helper, return 0.
            // Otherwise, return your own HMODULE to be used by the
            // helper instead of having it call LoadLibrary itself.

            break;

        case dliNotePreGetProcAddress :

            // If you want to return control to the helper, return 0.
            // If you choose you may supply your own FARPROC function
            // address and bypass the helper's call to GetProcAddress.

            break;

        case dliFailLoadLib :

            // LoadLibrary failed.
            // If you don't want to handle this failure yourself, return 0.
            // In this case the helper will raise an exception
            // (ERROR_MOD_NOT_FOUND) and exit.
            // If you want to handle the failure by loading an alternate
            // DLL (for example), then return the HMODULE for
            // the alternate DLL. The helper will continue execution with
            // this alternate DLL and attempt to find the
            // requested entrypoint via GetProcAddress.

            break;

        case dliFailGetProc :

            // GetProcAddress failed.
            // If you don't want to handle this failure yourself, return 0.
            // In this case the helper will raise an exception
            // (ERROR_PROC_NOT_FOUND) and exit.
            // If you choose you may handle the failure by returning
            // an alternate FARPROC function address.

            break;

        case dliNoteEndProcessing :

            // This notification is called after all processing is done.
            // There is no opportunity for modifying the helper's behavior
            // at this point except by longjmp()/throw()/RaiseException.
            // No return value is processed.

            break;

        default :

            return NULL;
    }

    return NULL;
}

/*
and then at global scope somewhere:

ExternC const PfnDliHook __pfnDliNotifyHook2 = delayHook;
ExternC const PfnDliHook __pfnDliFailureHook2 = delayHook;
*/
```

## <a name="see-also"></a>См. также раздел

[Понятие вспомогательной функции](understanding-the-helper-function.md)
