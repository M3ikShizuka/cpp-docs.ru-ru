---
description: Дополнительные сведения о выгрузке библиотеки DLL с отложенной загрузкой
title: Выгрузка DLL, загруженной с задержкой
ms.date: 01/19/2021
helpviewer_keywords:
- __FUnloadDelayLoadedDLL2
- delayed loading of DLLs, unloading
ms.openlocfilehash: 2ac898d56609ebb3aadc57ea8df00fa63fcbc3f0
ms.sourcegitcommit: 3d9cfde85df33002e3b3d7f3509ff6a8dc4c0a21
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "98667245"
---
# <a name="unload-a-delay-loaded-dll"></a>Выгрузка DLL, загруженной с задержкой

Вспомогательный модуль отложенной загрузки по умолчанию проверяет, имеет ли дескрипторы с отложенной загрузкой указатель и копию исходной таблицы адресов импорта (IAT) в `pUnloadIAT` поле. Если это так, вспомогательная функция сохраняет указатель в списке в дескрипторе задержки импорта. Эта запись позволяет вспомогательной функции найти библиотеку DLL по имени, чтобы обеспечить явное выгрузку этой библиотеки DLL.

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
__FUnloadDelayLoadedDLL2("User32.DLL");.
```

## <a name="see-also"></a>См. также раздел

[Понятие вспомогательной функции](understanding-the-helper-function.md)
