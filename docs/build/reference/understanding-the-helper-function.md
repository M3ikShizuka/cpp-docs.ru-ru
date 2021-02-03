---
description: Дополнительные сведения о вспомогательной функции отложенной загрузки
title: Вспомогательная функция для отложенной загрузки
ms.date: 01/19/2021
helpviewer_keywords:
- delayed loading of DLLs, helper function
- __delayLoadHelper2 function
- delayimp.lib
- __delayLoadHelper function
- delayhlp.cpp
- delayimp.h
- helper functions
ms.openlocfilehash: 6108e896b6d7a370f2b4d6ab8f5baa880112a21e
ms.sourcegitcommit: c20734f18d3d49bb38b1628c68b53b54b3eeeb03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "99522746"
---
# <a name="understand-the-delay-load-helper-function"></a>Вспомогательная функция для отложенной загрузки

Вспомогательная функция для отложенной загрузки, поддерживаемой компоновщиком, фактически загружает библиотеку DLL во время выполнения. Вспомогательную функцию можно изменить, чтобы настроить ее поведение. Вместо использования предоставляемой вспомогательной функции в *`delayimp.lib`* напишите собственную функцию и свяжите ее с программой. Одна вспомогательная функция обслуживает все библиотеки DLL с отложенной загрузкой.

Вы можете предоставить собственную версию вспомогательной функции, если требуется выполнить конкретную обработку на основе имен DLL или импортов.

Вспомогательная функция принимает следующие действия:

- Проверяет сохраненный обработчик на наличие уже загруженного в библиотеку.

- Вызовы `LoadLibrary` для попытки загрузки библиотеки DLL

- Вызовы `GetProcAddress` для попыток получения адреса процедуры

- Возвращает преобразователь отложенных операций импорта для вызова загруженной в данный момент точки входа

Вспомогательная функция может обращаться к обработчику уведомлений в программе после каждого из следующих действий:

- При запуске вспомогательной функции

- Непосредственно перед `LoadLibrary` вызовом в вспомогательной функции

- Непосредственно перед `GetProcAddress` вызовом в вспомогательной функции

- Если вызов `LoadLibrary` в вспомогательной функции завершается с ошибкой

- Если вызов `GetProcAddress` в вспомогательной функции завершается с ошибкой

- После завершения обработки вспомогательной функции

Каждая из этих точек ловушки может возвращать значение, которое каким-либо образом изменяет нормальную обработку вспомогательной процедуры, за исключением того, что возвращается к преобразовательу отложенной загрузки импорта.

Вспомогательный код по умолчанию можно найти в *`delayhlp.cpp`* и *`delayimp.h`* в *`include`* каталоге компилятором MSVC. Он компилируется в *`delayimp.lib`* *`lib`* Каталог компилятором MSVC для целевой архитектуры. Эту библиотеку необходимо включить в компиляции, если не написать собственную вспомогательную функцию.

## <a name="delay-load-helper-calling-conventions-parameters-and-return-type"></a><a name="calling-conventions-parameters-and-return-type"></a> Соглашения о вызовах, параметры и тип возвращаемого значения в методах задержки загрузки

Прототип подпрограммы для вспомогательной загрузки с задержкой:

```C
FARPROC WINAPI __delayLoadHelper2(
    PCImgDelayDescr pidd,
    FARPROC * ppfnIATEntry
);
```

### <a name="parameters"></a>Параметры

*`pidd`*\
**`const`** Указатель на объект `ImgDelayDescr` , содержащий смещения различных данных, связанных с импортом, отметку времени для данных привязки и набор атрибутов, которые предоставляют дополнительные сведения о содержимом дескриптора. В настоящее время существует только один атрибут, `dlattrRva` который указывает, что адреса в дескрипторе являются относительными виртуальными адресами. Дополнительные сведения см. в объявлениях в разделе *`delayimp.h`* .

Указатели в дескрипторе задержки ( `ImgDelayDescr` в *`delayimp.h`* ) используют относительные виртуальные адреса (RVA) для корректной работы как в 32-разрядных, так и в 64-разрядных программах. Чтобы использовать их, преобразуйте эти RVA обратно в указатели с помощью функции, которую можно `PFromRva` найти в *`delayhlp.cpp`* . Эту функцию можно использовать для каждого поля в дескрипторе, чтобы преобразовать их обратно в 32-разрядные или 64-битовые указатели. Вспомогательная функция задержки загрузки по умолчанию — хороший шаблон для использования в качестве примера.

Описание `PCImgDelayDescr` структуры см. в разделе [определения структуры и константы](#structure-and-constant-definitions).

*`ppfnIATEntry`*\
Указатель на слот в таблице адресов импорта с отложенной загрузкой (IAT). Это слот, который обновляется с адресом импортированной функции. Вспомогательная подпрограммы должна хранить то же значение, которое она возвращает в это расположение.

### <a name="expected-return-values"></a>Ожидаемые возвращаемые значения

Если вспомогательная функция выполнена успешно, возвращается адрес импортированной функции.

Если функция завершается ошибкой, она вызывает структурированное исключение и возвращает 0. Возможны три типа исключений.

- Недопустимый параметр, который происходит, если атрибуты в *`pidd`* заданы неправильно. Считать это неустранимой ошибкой.

- Функции `LoadLibrary` не удалось загрузить указанную библиотеку DLL.

- Ошибка в функции `GetProcAddress`.

Вы отвечаете за обработку этих исключений. Дополнительные сведения см. в разделе [Обработка ошибок и уведомление](error-handling-and-notification.md).

### <a name="remarks"></a>Примечания

Соглашение о вызовах для вспомогательной функции — **`__stdcall`** . Тип возвращаемого значения не важен, поэтому `FARPROC` используется. Эта функция имеет компоновку C, что означает необходимость заключения ее в оболочку `extern "C"` при объявлении в коде C++. `ExternC`Этот упаковщик используется макросом.

Чтобы использовать вспомогательную подпрограмму в качестве обработчика уведомлений, код должен указать соответствующий указатель на функцию для возврата. Затем код преобразователя, создаваемый компоновщиком, принимает это возвращаемое значение в качестве действительной цели импорта и переходит непосредственно к ней. Если вы не хотите использовать вспомогательную подпрограммы в качестве обработчика уведомлений, сохраните возвращаемое значение вспомогательной функции в `ppfnIATEntry` , переданном расположении указателя на функцию.

## <a name="sample-hook-function"></a>Пример функции-ловушки

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
            // If you choose, you may handle the failure by returning
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

## <a name="delay-load-structure-and-constant-definitions"></a><a name="structure-and-constant-definitions"></a> Отложенная загрузка определений структуры и констант

Вспомогательная подсистема отложенной загрузки по умолчанию использует несколько структур для взаимодействия с функциями-обработчиками и во время любых исключений. Эти структуры определяются в *`delayimp.h`* . Ниже приведены макросы, определения типов, значения уведомлений и сбоев, информационные структуры и тип указателя на обработчик функции, передаваемый обработчикам:

```C
#define _DELAY_IMP_VER  2

#if defined(__cplusplus)
#define ExternC extern "C"
#else
#define ExternC extern
#endif

typedef IMAGE_THUNK_DATA *          PImgThunkData;
typedef const IMAGE_THUNK_DATA *    PCImgThunkData;
typedef DWORD                       RVA;

typedef struct ImgDelayDescr {
    DWORD           grAttrs;        // attributes
    RVA             rvaDLLName;     // RVA to dll name
    RVA             rvaHmod;        // RVA of module handle
    RVA             rvaIAT;         // RVA of the IAT
    RVA             rvaINT;         // RVA of the INT
    RVA             rvaBoundIAT;    // RVA of the optional bound IAT
    RVA             rvaUnloadIAT;   // RVA of optional copy of original IAT
    DWORD           dwTimeStamp;    // 0 if not bound,
                                    // O.W. date/time stamp of DLL bound to (Old BIND)
    } ImgDelayDescr, * PImgDelayDescr;

typedef const ImgDelayDescr *   PCImgDelayDescr;

enum DLAttr {                   // Delay Load Attributes
    dlattrRva = 0x1,                // RVAs are used instead of pointers
                                    // Having this set indicates a VC7.0
                                    // and above delay load descriptor.
    };

//
// Delay load import hook notifications
//
enum {
    dliStartProcessing,             // used to bypass or note helper only
    dliNoteStartProcessing = dliStartProcessing,

    dliNotePreLoadLibrary,          // called just before LoadLibrary, can
                                    //  override w/ new HMODULE return val
    dliNotePreGetProcAddress,       // called just before GetProcAddress, can
                                    //  override w/ new FARPROC return value
    dliFailLoadLib,                 // failed to load library, fix it by
                                    //  returning a valid HMODULE
    dliFailGetProc,                 // failed to get proc address, fix it by
                                    //  returning a valid FARPROC
    dliNoteEndProcessing,           // called after all processing is done, no
                                    //  bypass possible at this point except
                                    //  by longjmp()/throw()/RaiseException.
    };

typedef struct DelayLoadProc {
    BOOL                fImportByName;
    union {
        LPCSTR          szProcName;
        DWORD           dwOrdinal;
        };
    } DelayLoadProc;

typedef struct DelayLoadInfo {
    DWORD               cb;         // size of structure
    PCImgDelayDescr     pidd;       // raw form of data (everything is there)
    FARPROC *           ppfn;       // points to address of function to load
    LPCSTR              szDll;      // name of dll
    DelayLoadProc       dlp;        // name or ordinal of procedure
    HMODULE             hmodCur;    // the hInstance of the library we have loaded
    FARPROC             pfnCur;     // the actual function that will be called
    DWORD               dwLastError;// error received (if an error notification)
    } DelayLoadInfo, * PDelayLoadInfo;

typedef FARPROC (WINAPI *PfnDliHook)(
    unsigned        dliNotify,
    PDelayLoadInfo  pdli
    );
```

## <a name="calculate-necessary-values-for-delay-loading"></a><a name="calculate-necessary-values"></a> Вычисление необходимых значений для отложенной загрузки

Вспомогательная подсистема с отложенной загрузкой должна вычислить два важных фрагмента информации. Чтобы вычислить эту информацию, в можно получить две встроенные функции *`delayhlp.cpp`* .

- Первый, `IndexFromPImgThunkData` ,, вычисляет индекс текущего импорта в трех различных таблицах (импорт таблицы адресов (IAT), связанную таблицу адресов импорта (Биат) и несвязанную таблицу адресов импорта (уиат)).

- Во втором, `CountOfImports` , подсчитывается количество импортов в допустимой IAT.

```C
// utility function for calculating the index of the current import
// for all the tables (INT, BIAT, UIAT, and IAT).
__inline unsigned
IndexFromPImgThunkData(PCImgThunkData pitdCur, PCImgThunkData pitdBase) {
    return pitdCur - pitdBase;
    }

// utility function for calculating the count of imports given the base
// of the IAT. NB: this only works on a valid IAT!
__inline unsigned
CountOfImports(PCImgThunkData pitdBase) {
    unsigned        cRet = 0;
    PCImgThunkData  pitd = pitdBase;
    while (pitd->u1.Function) {
        pitd++;
        cRet++;
        }
    return cRet;
    }
```

## <a name="support-unload-of-a-delay-loaded-dll"></a><a name="unload-a-delay-loaded-dll"></a> Поддержка выгрузки библиотеки DLL с отложенной загрузкой

При загрузке библиотеки DLL с отложенной загрузкой вспомогательный модуль отложенной загрузки по умолчанию проверяет, имеют ли дескрипторы с отложенной загрузкой указатель и копию исходной таблицы адресов импорта (IAT) в `pUnloadIAT` поле. Если это так, вспомогательная функция сохраняет указатель в списке в дескрипторе задержки импорта. Эта запись позволяет вспомогательной функции найти библиотеку DLL по имени, чтобы обеспечить явное выгрузку этой библиотеки DLL.

Ниже приведены связанные структуры и функции для явной загрузки библиотеки DLL с отложенной загрузкой.

```cpp
//
// Unload support from delayimp.h
//

// routine definition; takes a pointer to a name to unload

ExternC
BOOL WINAPI
__FUnloadDelayLoadedDLL2(LPCSTR szDll);

// structure definitions for the list of unload records
typedef struct UnloadInfo * PUnloadInfo;
typedef struct UnloadInfo {
    PUnloadInfo     puiNext;
    PCImgDelayDescr pidd;
    } UnloadInfo;

// from delayhlp.cpp
// the default delay load helper places the unloadinfo records in the
// list headed by the following pointer.
ExternC
PUnloadInfo __puiHead;
```

`UnloadInfo`Структура реализуется с помощью класса C++, который использует `LocalAlloc` и `LocalFree` реализации в качестве `operator new` и `operator delete` соответственно. Эти параметры хранятся в стандартном связанном списке, который использует в `__puiHead` качестве заголовка списка.

При вызове `__FUnloadDelayLoadedDLL` он пытается найти имя, которое вы задают в списке загруженных библиотек DLL. (Требуется точное совпадение.) Если объект найден, копия IAT в копируется `pUnloadIAT` поверх выполняющейся IAT, чтобы восстановить указатели преобразователей. Затем библиотека освобождается с помощью `FreeLibrary` , соответствующая `UnloadInfo` запись удаляется из списка и удаляется и `TRUE` возвращается.

Аргумент функции `__FUnloadDelayLoadedDLL2` учитывает регистр. Например, можно указать:

```cpp
__FUnloadDelayLoadedDLL2("user32.dll");
```

не так:

```cpp
__FUnloadDelayLoadedDLL2("User32.DLL");
```

Пример выгрузки библиотеки DLL, загруженной с задержкой, см. [в разделе Явная выгрузка библиотеки DLL, загруженной с задержкой](linker-support-for-delay-loaded-dlls.md).

## <a name="develop-your-own-delay-load-helper-function"></a><a name="develop-your-own-helper-function"></a> Разработка собственной вспомогательной функции отложенной загрузки

Может потребоваться предоставить собственную версию подпрограммы для вспомогательной загрузки с задержкой. В собственной подсистеме можно выполнять определенную обработку на основе имен библиотек DLL или импортов. Существует два способа вставки собственного кода: код собственной вспомогательной функции, возможно, на основе прилагаемого кода. Или подключите предоставленный вспомогательный метод для вызова собственной функции с помощью [обработчиков уведомлений](error-handling-and-notification.md#notification-hooks).

### <a name="code-your-own-helper"></a>Код собственного вспомогательного приложения

Создать собственную вспомогательную подпрограммы очень просто. Существующий код можно использовать в качестве инструкции для новой функции. Функция должна использовать те же соглашения о вызовах, что и у существующего вспомогательного метода. И, если он возвращается к преобразователям, созданным компоновщиком, он должен возвращать правильный указатель на функцию. После создания кода вы можете либо удовлетворить вызов, либо выйти из него, но вам нравится.

### <a name="use-the-start-processing-notification-hook"></a>Использование обработчика уведомлений о запуске обработки

Вероятно, проще всего предоставить новый указатель на функцию пользовательского обработчика уведомлений, которая принимает те же значения, что и вспомогательный модуль по умолчанию для `dliStartProcessing` уведомления. На этом этапе функция-обработчик может стать новой вспомогательной функцией, так как успешный возврат к вспомогательному модулю по умолчанию обходит всю дальнейшую обработку в вспомогательном модуле по умолчанию.

## <a name="see-also"></a>См. также

[Поддержка компоновщика для библиотек DLL с отложенной загрузкой](linker-support-for-delay-loaded-dlls.md#explicitly-unload-a-delay-loaded-dll)
