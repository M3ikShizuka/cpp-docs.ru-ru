---
title: Использование библиотек DLL расширений MFC для баз данных, OLE и сокетов в обычных библиотеках DLL MFC
description: В этой статье описывается, как использовать библиотеки DLL расширения MFC для баз данных, OLE и сокетов в обычных библиотеках DLL MFC.
ms.date: 11/30/2020
helpviewer_keywords:
- DLLs [C++], initializing
- DLLs [C++], extension
- DLLs [C++], regular
ms.openlocfilehash: a28e80c4d554a86f45f708e661382ee4a54eca9e
ms.sourcegitcommit: 432c24dde31c400437c4320e8432b1ddb232f844
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/01/2020
ms.locfileid: "96440277"
---
# <a name="using-database-ole-and-sockets-mfc-extension-dlls-in-regular-mfc-dlls"></a>Использование библиотек DLL расширений MFC для баз данных, OLE и сокетов в обычных библиотеках DLL MFC

Если вы используете библиотеку DLL расширения MFC из обычной библиотеки DLL MFC и библиотека DLL расширения MFC не привязана к цепочке объектов `CDynLinkLibrary` обычной библиотеки DLL MFC, вы можете столкнуться с проблемами. Так как отладочные версии библиотек DLL MFC для баз данных, OLE и сокетов реализуются как библиотеки DLL расширения MFC, при использовании этих функций MFC могут возникнуть аналогичные проблемы, даже если вы не используете явно какие-либо собственные библиотеки расширения MFC. Некоторые симптомы:

- При попытке десериализации объекта типа класса, определенного в библиотеке DLL расширения MFC, в окне отладки TRACE выдается сообщение: "Предупреждение. Не удается загрузить CYourClass из архива. Класс не определен". В результате не удается выполнить сериализацию объекта.

- Может быть вызвано исключение, указывающее на недопустимый класс.

- Не удается загрузить ресурсы, хранящиеся в библиотеке DLL расширения MFC, так как `AfxFindResourceHandle` возвращает `NULL` или неправильный дескриптор ресурса.

- `DllGetClassObject`, `DllCanUnloadNow` и функции-члены `UpdateRegistry`, `Revoke`, `RevokeAll` и `RegisterAll` в `COleObjectFactory` не могут найти фабрику класса, определенную в библиотеке DLL расширения MFC.

- `AfxDoForAllClasses` не работает для классов в библиотеке DLL расширения MFC.

- Не удается загрузить стандартные базы данных MFC, сокеты или ресурсы OLE. Например, `AfxLoadString(AFX_IDP_SQL_CONNECT_FAIL)` возвращает пустую строку, даже если обычная библиотека DLL MFC правильно использует классы базы данных MFC.

Решение этих проблем заключается в создании и экспорте функции инициализации в библиотеке DLL расширения MFC, которая создает объект `CDynLinkLibrary`. Вызывайте эту функцию инициализации ровно один раз из каждой обычной библиотеки DLL MFC, использующей библиотеку DLL расширения MFC.

## <a name="mfc-ole-mfc-database-or-dao-or-mfc-sockets-support"></a>Поддержка MFC OLE, базы данных MFC (или DAO) или сокетов MFC

Если вы используете поддержку OLE MFC, базы данных (или DAO) MFC или сокетов MFC соответственно, отладочные библиотеки DLL расширения MFC *`MFCOxxD.dll`* , *`MFCDxxD.dll`* и *`MFCNxxD.dll`* (где *xx* — номер версии) связываются автоматически. Вызовите предопределенную функцию инициализации для каждой используемой библиотеки DLL:

- Для поддержки базы данных добавьте вызов `AfxDbInitModule` в функцию `CWinApp::InitInstance` для обычной библиотеки DLL MFC. Убедитесь, что этот вызов происходит перед вызовом базового класса или любым добавленным кодом, который обращается к *`MFCDxxD.dll`* . Эта функция не принимает параметры и возвращает `void`.

- Для поддержки OLE добавьте вызов `AfxOleInitModule` в функцию `CWinApp::InitInstance` для обычной библиотеки DLL MFC. Функция `COleControlModule::InitInstance` уже содержит вызов `AfxOleInitModule`, поэтому если вы создаете элемент управления OLE и используете `COleControlModule`, этот вызов не нужно добавлять в `AfxOleInitModule`.

- Для поддержки сокетов добавьте вызов `AfxNetInitModule` в функцию `CWinApp::InitInstance` для обычной библиотеки DLL MFC.

Сборки выпусков библиотек DLL и приложений MFC не используют отдельные библиотеки DLL для поддержки баз данных, сокетов и OLE. Тем не менее, в режиме выпуска можно спокойно вызывать эти функции инициализации.

## <a name="cdynlinklibrary-objects"></a>Объекты CDynLinkLibrary

При выполнении каждой операции, упомянутой в начале этой статьи, MFC необходимо найти нужное значение или объект. Например, во время десериализации MFC должен выполнять поиск по всем доступным в настоящее время классам среды выполнения для сопоставления объектов в архиве с соответствующим классом времени выполнения.

В рамках этого поиска MFC сканирует все библиотеки DLL расширения MFC, проходя по цепочке объектов `CDynLinkLibrary`. Объекты `CDynLinkLibrary` автоматически присоединяются к цепочке во время создания и создаются каждой библиотекой DLL расширения MFC по очереди во время инициализации. Каждый модуль (приложение или обычная библиотека DLL MFC) имеет собственную цепочку объектов `CDynLinkLibrary`.

Чтобы библиотека DLL расширения MFC была подключена к цепочке `CDynLinkLibrary`, она должна создать объект `CDynLinkLibrary` в контексте каждого модуля, использующего библиотеку DLL расширения MFC. Чтобы вы могли использовать библиотеку DLL расширения MFC в обычных библиотеках DLL MFC, библиотека DLL расширения должна предоставлять экспортированную функцию инициализации, которая создает объект `CDynLinkLibrary`. Каждая обычная библиотека DLL MFC, использующая библиотеку DLL расширения MFC, должна вызывать экспортированную функцию инициализации.

Если библиотека DLL расширения MFC будет использоваться только из приложения MFC и никогда не будет использоваться из обычной библиотеки DLL MFC, достаточно создать объект `CDynLinkLibrary` в функции `DllMain` библиотеки DLL расширения MFC. Это задача кода библиотеки DLL расширения MFC в мастере библиотеки DLL MFC. При неявной загрузке библиотеки DLL расширения MFC `DllMain` загружается и выполняется перед запуском приложения. Все созданные `CDynLinkLibrary` собраны в цепочку по умолчанию, которую библиотека DLL MFC резервирует для приложения MFC.

Не следует включать несколько объектов `CDynLinkLibrary` из DLL расширения MFC в одну цепочку. Это особенно важно, если возможна динамическая выгрузка библиотеки DLL расширения MFC из памяти. Не вызывайте функцию инициализации более одного раза из любого модуля.

## <a name="sample-code"></a>Пример кода

В этом примере кода предполагается, что обычная библиотека DLL MFC неявно связывается с библиотекой DLL расширения MFC. Для неявной привязки нужно установить связь с библиотекой импорта (LIB-файл) библиотеки DLL расширения MFC при сборке обычной библиотеки DLL MFC.

В источнике библиотеки DLL расширения MFC должны находиться следующие строки:

```cpp
// YourExtDLL.cpp:

// standard MFC extension DLL routines
#include "afxdllx.h"

static AFX_EXTENSION_MODULE extensionDLL;

extern "C" int APIENTRY
DllMain(HINSTANCE hInstance, DWORD dwReason, LPVOID lpReserved)
{
    if (dwReason == DLL_PROCESS_ATTACH)
    {
        // MFC extension DLL one-time initialization
        if (!AfxInitExtensionModule(extensionDLL, hInstance))
           return 0;
    }
    return 1;   // ok
}

// Exported DLL initialization is run in context of
// application or regular MFC DLL
extern "C" void WINAPI InitYourExtDLL()
{
    // create a new CDynLinkLibrary for this app
    new CDynLinkLibrary(extensionDLL);

    // add other initialization here
}
```

Обязательно экспортируйте функцию **InitYourExtDLL**. Вы можете использовать **`__declspec(dllexport)`** или экспортировать функцию в DEF-файл для библиотеки DLL, как показано ниже:

```def
// YourExtDLL.Def:
LIBRARY      YOUREXTDLL
CODE         PRELOAD MOVEABLE DISCARDABLE
DATA         PRELOAD SINGLE
EXPORTS
    InitYourExtDLL
```

Добавьте вызов члена `InitInstance` объекта, производного от `CWinApp`, в каждой обычной библиотеке DLL MFC с помощью библиотеки DLL расширения MFC:

```cpp
// YourRegularDLL.cpp:

class CYourRegularDLL : public CWinApp
{
public:
    virtual BOOL InitInstance(); // Initialization
    virtual int ExitInstance();  // Termination

    // nothing special for the constructor
    CYourRegularDLL(LPCTSTR pszAppName) : CWinApp(pszAppName) { }
};

BOOL CYourRegularDLL::InitInstance()
{
    // any DLL initialization goes here
    TRACE0("YOUR regular MFC DLL initializing\n");

    // wire any MFC extension DLLs into CDynLinkLibrary chain
    InitYourExtDLL();

    return TRUE;
}
```

### <a name="what-do-you-want-to-do"></a>Выберите действие

- [Инициализация библиотеки DLL расширения MFC](run-time-library-behavior.md#initializing-extension-dlls)

- [Инициализация обычных библиотек DLL MFC](run-time-library-behavior.md#initializing-regular-dlls)

### <a name="what-do-you-want-to-know-more-about"></a>Дополнительные сведения

- [Библиотеки DLL расширений MFC](extension-dlls.md)

- [Обычные DLL-библиотеки MFC, статически связанные с MFC](regular-dlls-statically-linked-to-mfc.md)

- [Обычные DLL-библиотеки MFC, динамически связанные с MFC](regular-dlls-dynamically-linked-to-mfc.md)

- [Использование MFC как части библиотеки DLL](../mfc/tn011-using-mfc-as-part-of-a-dll.md)

- [Версия библиотеки DLL MFC](../mfc/tn033-dll-version-of-mfc.md)

## <a name="see-also"></a>См. также

[Библиотеки DLL расширений MFC](extension-dlls.md)
