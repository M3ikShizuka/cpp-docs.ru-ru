---
title: Макросы и функции для управления библиотеками DLL
description: Справочное руководство по макросам и функциям MFC для управления библиотеками DLL.
ms.date: 11/30/2020
helpviewer_keywords:
- module macros in MFC
ms.openlocfilehash: b70c4506d49f656e1570f2500cfaa39c28053291
ms.sourcegitcommit: 432c24dde31c400437c4320e8432b1ddb232f844
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/01/2020
ms.locfileid: "96440329"
---
# <a name="macros-and-functions-for-managing-dlls"></a>Макросы и функции для управления библиотеками DLL

| Название | Описание |
|--|--|
| [`AFX_EXT_CLASS`](#afx_ext_class)] | Экспортирует классы. |
| [`AFX_MANAGE_STATE`](#afx_manage_state) | Защита экспортированной функции в библиотеке DLL. |
| [`AfxOleInitModule`](#afxoleinitmodule) | Обеспечивает поддержку OLE из обычной библиотеки DLL MFC, которая динамически связана с MFC. |
| [`AfxNetInitModule`](#afxnetinitmodule) | Предоставляет поддержку сокетов MFC из обычной библиотеки DLL MFC, которая динамически связана с MFC. |
| [`AfxGetAmbientActCtx`](#afxgetambientactctx) | Возвращает текущее состояние флага состояния каждого модуля. |
| [`AfxGetStaticModuleState`](#afxgetstaticmodulestate) | Задает состояние модуля перед инициализацией и восстанавливает предыдущее состояние модуля после очистки. |
| [`AfxInitExtensionModule`](#afxinitextensionmodule) | Инициализирует библиотеку DLL. |
| [`AfxSetAmbientActCtx`](#afxsetambientactctx) | Установите флаг состояния каждого модуля, который влияет на поведение WinSxS в MFC. |
| [`AfxTermExtensionModule`](#afxtermextensionmodule) | Позволяет MFC очищать библиотеку DLL расширения MFC, когда каждый процесс отключается от библиотеки DLL. |

## <a name="afx_ext_class"></a><a name="afx_ext_class"></a> `AFX_EXT_CLASS`

[Библиотеки DLL расширения MFC](../../build/extension-dlls.md) используют макрос `AFX_EXT_CLASS` для экспорта классов; исполняемые файлы, которые связываются с DLL расширения MFC, используют макрос для импорта классов.

### <a name="remarks"></a>Комментарии

С помощью `AFX_EXT_CLASS` макроса те же файлы заголовков, которые используются для сборки библиотеки DLL расширения MFC, можно использовать с исполняемыми файлами, которые связаны с библиотекой DLL.

В файле заголовка для библиотеки DLL добавьте `AFX_EXT_CLASS` ключевое слово в объявление класса следующим образом:

```cpp
class AFX_EXT_CLASS CMyClass : public CDocument
{
// <body of class>
};
```

Дополнительные сведения см. в разделе [Экспорт и импорт `AFX_EXT_CLASS` с помощью ](../../build/exporting-and-importing-using-afx-ext-class.md).

### <a name="requirements"></a>Требования

**Заголовок:**\<afxv_dll.h>

## <a name="afx_manage_state"></a><a name="afx_manage_state"></a> `AFX_MANAGE_STATE`

Вызовите этот макрос, чтобы защитить экспортированную функцию в библиотеке DLL.

### <a name="syntax"></a>Синтаксис

```cpp
AFX_MANAGE_STATE(AFX_MODULE_STATE* pModuleState )
```

### <a name="parameters"></a>Параметры

*`pModuleState`*<br/>
Указатель на `AFX_MODULE_STATE` структуру.

### <a name="remarks"></a>Комментарии

При вызове этого макроса *`pModuleState`* — это действующее состояние модуля для оставшейся части непосредственно содержащей его области. При выходе из этой области предыдущее действующее состояние модуля будет автоматически восстановлено.

`AFX_MODULE_STATE`Структура содержит глобальные данные для модуля, то есть часть состояния модуля, которая помещается или извлекается.

По умолчанию MFC использует для загрузки шаблона ресурса обработчик ресурсов основного приложения. Если в библиотеке DLL есть экспортированная функция, например, которая запускает диалоговое окно в библиотеке DLL, шаблон ресурса сохраняется в модуле DLL. Не забудьте переключить состояние модуля, чтобы использовать правильный маркер. Вы можете переключить состояние, добавив следующий код в начало функции:

```cpp
AFX_MANAGE_STATE(AfxGetStaticModuleState( ));
```

Этот макрос меняет местами текущее состояние модуля на состояние, возвращенное [`AfxGetStaticModuleState`](#afxgetstaticmodulestate) до конца текущей области.

Дополнительные сведения о состояниях модулей и MFC см. [в разделе Управление данными о состоянии модулей MFC](../managing-the-state-data-of-mfc-modules.md) и [техническое примечание 58](../tn058-mfc-module-state-implementation.md).

> [!NOTE]
> Когда MFC создает контекст активации для сборки, он использует [`AfxWinInit`](application-information-and-management.md#afxwininit) для создания контекста и его `AFX_MANAGE_STATE` активации и деактивации. Обратите внимание, что `AFX_MANAGE_STATE` включено для статических библиотек MFC, а также библиотек DLL MFC, чтобы код MFC можно было выполнять в правильном контексте активации, выбранном в библиотеке DLL пользователя. Дополнительные сведения см. [в разделе Поддержка контекстов активации в состоянии модуля MFC](../support-for-activation-contexts-in-the-mfc-module-state.md).

### <a name="requirements"></a>Требования

**Заголовок:**\<afxstat_.h>

## <a name="a-nameafxoleinitmodule-afxoleinitmodule"></a><a name="afxoleinitmodule"><a/> `AfxOleInitModule`

Для поддержки OLE из обычной библиотеки DLL MFC, которая динамически связана с MFC, вызовите эту функцию в функции обычной библиотеки DLL MFC, `CWinApp::InitInstance` чтобы инициализировать БИБЛИОТЕКУ MFC OLE DLL.

### <a name="syntax"></a>Синтаксис

```cpp
void AFXAPI AfxOleInitModule( );
```

### <a name="remarks"></a>Примечания

MFC OLE DLL — это библиотека DLL расширения MFC. чтобы библиотека DLL расширения MFC была подключена к `CDynLinkLibrary` цепочке, она должна создать `CDynLinkLibrary` объект в контексте каждого модуля, который будет его использовать. `AfxOleInitModule` создает `CDynLinkLibrary` объект в контексте обычной библиотеки DLL MFC, чтобы он был подключен в `CDynLinkLibrary` цепочке объектов обычной библиотеки DLL MFC.

Если вы создаете элемент управления OLE и используете `COleControlModule` , то не следует вызывать, `AfxOleInitModule` поскольку `InitInstance` функция-член для `COleControlModule` вызовов `AfxOleInitModule` .

### <a name="requirements"></a>Требования

**Заголовок**: \<afxdll_.h>

## <a name="afxnetinitmodule"></a><a name="afxnetinitmodule"></a> `AfxNetInitModule`

Для поддержки сокетов MFC из обычной библиотеки DLL MFC, которая динамически связана с MFC, добавьте вызов этой функции в функции обычной библиотеки DLL MFC `CWinApp::InitInstance` для инициализации DLL-библиотеки MFC.

### <a name="syntax"></a>Синтаксис

```cpp
void AFXAPI AfxNetInitModule( );
```

### <a name="remarks"></a>Примечания

Библиотека DLL MFC Sockets является библиотекой DLL расширения MFC. чтобы библиотека DLL расширения MFC была подключена к `CDynLinkLibrary` цепочке, она должна создать `CDynLinkLibrary` объект в контексте каждого модуля, который будет его использовать. `AfxNetInitModule` создает `CDynLinkLibrary` объект в контексте обычной библиотеки DLL MFC, чтобы он был подключен в `CDynLinkLibrary` цепочке объектов обычной библиотеки DLL MFC.

### <a name="requirements"></a>Требования

**Заголовок:**\<afxdll_.h>

## <a name="afxgetambientactctx"></a><a name="afxgetambientactctx"></a> `AfxGetAmbientActCtx`

Эта функция используется для получения текущего состояния флага состояния каждого модуля, что влияет на поведение WinSxS в MFC.

### <a name="syntax"></a>Синтаксис

```cpp
BOOL AFXAPI AfxGetAmbientActCtx();
```

### <a name="return-value"></a>Возвращаемое значение

Текущее значение флага состояния модуля.

### <a name="remarks"></a>Комментарии

Если флаг установлен (по умолчанию) и поток входит в модуль MFC (см [`AFX_MANAGE_STATE`](#afx_manage_state) .), то контекст модуля активируется.

Если флаг не задан, контекст модуля не активируется в записи.

Контекст модуля определяется из его манифеста, который часто внедряется в ресурсы модуля.

### <a name="requirements"></a>Требования

**Заголовок:**\<afxcomctl32.h>

## <a name="afxgetstaticmodulestate"></a><a name="afxgetstaticmodulestate"></a> `AfxGetStaticModuleState`

Вызывайте эту функцию, чтобы задать состояние модуля перед инициализацией и восстановить предыдущее состояние модуля после очистки.

### <a name="syntax"></a>Синтаксис

```cpp
AFX_MODULE_STATE* AFXAPI AfxGetStaticModuleState( );
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на `AFX_MODULE_STATE` структуру.

### <a name="remarks"></a>Комментарии

`AFX_MODULE_STATE`Структура содержит глобальные данные для модуля, то есть часть состояния модуля, которая помещается или извлекается.

По умолчанию MFC использует для загрузки шаблона ресурса обработчик ресурсов основного приложения. Если в библиотеке DLL есть экспортированная функция, например, которая запускает диалоговое окно в библиотеке DLL, шаблон ресурса сохраняется в модуле DLL. Не забудьте переключить состояние модуля, чтобы использовать правильный маркер. Вы можете переключить состояние, добавив следующий код в начало функции:

```cpp
AFX_MANAGE_STATE(AfxGetStaticModuleState( ));
```

Этот макрос меняет местами текущее состояние модуля на состояние, возвращенное `AfxGetStaticModuleState` до конца текущей области.

Дополнительные сведения о состояниях модулей и MFC см. [в разделе Управление данными о состоянии модулей MFC](../managing-the-state-data-of-mfc-modules.md) и [техническое примечание 58](../tn058-mfc-module-state-implementation.md).

### <a name="requirements"></a>Требования

**Заголовок:**\<afxstat_.h>

## <a name="afxinitextensionmodule"></a><a name="afxinitextensionmodule"></a> `AfxInitExtensionModule`

Вызовите эту функцию в библиотеке DLL расширения MFC `DllMain` для инициализации библиотеки DLL.

### <a name="syntax"></a>Синтаксис

```cpp
BOOL AFXAPI AfxInitExtensionModule( AFX_EXTENSION_MODULE& state,  HMODULE hModule );
```

### <a name="parameters"></a>Параметры

*`state`*<br/>
Ссылка на структуру [ `AFX_EXTENSION_MODULE` структуры](afx-extension-module-structure.md) , которая будет содержать состояние модуля DLL расширения MFC после инициализации. Состояние включает копию объектов класса среды выполнения, которые были инициализированы библиотекой DLL расширения MFC как часть обычной конструкции статического объекта, выполняемой перед `DllMain` входом.

*`hModule`*<br/>
Маркер модуля DLL расширения MFC.

### <a name="return-value"></a>Возвращаемое значение

`TRUE` значение, если библиотека DLL расширения MFC успешно инициализирована. в противном случае — `FALSE` .

### <a name="remarks"></a>Комментарии

Пример:

```cpp
static AFX_EXTENSION_MODULE NVC_MFC_DLLDLL;
extern "C" int APIENTRY
DllMain(HINSTANCE hInstance, DWORD dwReason, LPVOID lpReserved)
{
    // Remove this if you use lpReserved
    UNREFERENCED_PARAMETER(lpReserved);

    if (dwReason == DLL_PROCESS_ATTACH)
    {
        TRACE0("NVC_MFC_DLL.DLL Initializing!\n");

        // MFC extension DLL one-time initialization
        if (!AfxInitExtensionModule(NVC_MFC_DLLDLL, hInstance))
            return 0;
...
```

`AfxInitExtensionModule` создает копию ХМОДУЛЕ библиотеки DLL и записывает ее классы среды выполнения ( `CRuntimeClass` структуры) и фабрики объектов (объекты), которые будут `COleObjectFactory` использоваться позже при `CDynLinkLibrary` создании объекта.
Библиотеки DLL расширения MFC должны выполнять два действия в своей `DllMain` функции:

- Вызовите [`AfxInitExtensionModule`](#afxinitextensionmodule) и проверьте возвращаемое значение.

- Создайте `CDynLinkLibrary` объект, если библиотека DLL будет экспортировать объекты [ `CRuntimeClass` структуры](cruntimeclass-structure.md) или имеет собственные пользовательские ресурсы.

Можно вызвать `AfxTermExtensionModule` для очистки библиотеки DLL расширения MFC, когда каждый процесс отключается от библиотеки DLL расширения MFC (которая происходит при завершении процесса или при выгрузке библиотеки DLL `AfxFreeLibrary` вызовом).

### <a name="requirements"></a>Требования

**Заголовок:**\<afxdll_.h>

## <a name="afxsetambientactctx"></a><a name="afxsetambientactctx"></a> `AfxSetAmbientActCtx`

Эта функция используется для установки флага состояния каждого модуля, который влияет на поведение WinSxS в MFC.

### <a name="syntax"></a>Синтаксис

```cpp
void AFXAPI AfxSetAmbientActCtx(BOOL bSet);
```

### <a name="parameters"></a>Параметры

*`bSet`*<br/>
Новое значение флага состояния модуля.

### <a name="remarks"></a>Комментарии

Если флаг установлен (по умолчанию) и поток входит в модуль MFC (см [`AFX_MANAGE_STATE`](#afx_manage_state) .), то контекст модуля активируется.
Если флаг не задан, контекст модуля не активируется в записи.
Контекст модуля определяется из его манифеста, который часто внедряется в ресурсы модуля.

### <a name="example"></a>Пример

```cpp
BOOL CMFCListViewApp::InitInstance()
{
   AfxSetAmbientActCtx(FALSE);
   // Remainder of function definition omitted.
}
```

### <a name="requirements"></a>Требования

**Заголовок:**\<afxcomctl32.h>

## <a name="afxtermextensionmodule"></a><a name="afxtermextensionmodule"></a> `AfxTermExtensionModule`

Вызывайте эту функцию, чтобы разрешить MFC очищать библиотеку DLL расширения MFC, когда каждый процесс отключается от библиотеки DLL (что происходит при завершении процесса или при выгрузке библиотеки DLL `AfxFreeLibrary` вызовом).

### <a name="syntax"></a>Синтаксис

```cpp
void AFXAPI AfxTermExtensionModule( AFX_EXTENSION_MODULE& state, BOOL bAll = FALSE );
```

### <a name="parameters"></a>Параметры

*`state`*<br/>
Ссылка на [`AFX_EXTENSION_MODULE`](afx-extension-module-structure.md) структуру, которая содержит состояние модуля DLL расширения MFC.

*`bAll`*<br/>
Если значение — TRUE, очистите все модули DLL расширения MFC. В противном случае очистите только текущий модуль DLL.

### <a name="remarks"></a>Комментарии

`AfxTermExtensionModule` удалит все локальные хранилища, подключенные к модулю, и удалит все записи из кэша схемы сообщений. Пример:

```cpp
static AFX_EXTENSION_MODULE NVC_MFC_DLLDLL;
extern "C" int APIENTRY
DllMain(HINSTANCE hInstance, DWORD dwReason, LPVOID lpReserved)
{
    // Remove this if you use lpReserved
    UNREFERENCED_PARAMETER(lpReserved);

    if (dwReason == DLL_PROCESS_ATTACH)
    {
        TRACE0("NVC_MFC_DLL.DLL Initializing!\n");

        // MFC extension DLL one-time initialization
        if (!AfxInitExtensionModule(NVC_MFC_DLLDLL, hInstance))
            return 0;

        new CMyDynLinkLibrary(NVC_MFC_DLLDLL);

    }
    else if (dwReason == DLL_PROCESS_DETACH)
    {
        TRACE0("NVC_MFC_DLL.DLL Terminating!\n");

        // Terminate the library before destructors are called
        AfxTermExtensionModule(NVC_MFC_DLLDLL);
    }
    return 1;   // ok
}
```

Если приложение загружает и освобождает библиотеки DLL расширения MFC динамически, обязательно вызовите `AfxTermExtensionModule` . Так как большинство библиотек DLL расширения MFC не загружаются динамически (обычно они связаны с помощью библиотек импорта), вызов, `AfxTermExtensionModule` как правило, не требуется.

Библиотеки DLL расширения MFC должны вызываться [`AfxInitExtensionModule`](#afxinitextensionmodule) в `DllMain` . Если библиотека DLL экспортирует [`CRuntimeClass`](cruntimeclass-structure.md) объекты или имеет собственные пользовательские ресурсы, необходимо также создать `CDynLinkLibrary` объект в `DllMain` .

### <a name="requirements"></a>Требования

**Заголовок:**\<afxdll_.h>

## <a name="see-also"></a>См. также раздел

[Макросы и глобальные](mfc-macros-and-globals.md)<br/>
[`AfxMessageBox`](cstring-formatting-and-message-box-display.md#afxmessagebox)<br/>
[Управление данными состояния модулей MFC](../managing-the-state-data-of-mfc-modules.md)<br/>
