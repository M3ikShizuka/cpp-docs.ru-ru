---
description: 'Дополнительные сведения: структура AFX_EXTENSION_MODULE'
title: Структура AFX_EXTENSION_MODULE
ms.date: 11/04/2016
f1_keywords:
- AFX_EXTENSION_MODULE
helpviewer_keywords:
- AFX_EXTENSION_MODULE structure [MFC]
ms.assetid: b85a989c-d0c5-4b28-b53c-dad45b75704e
ms.openlocfilehash: d3a5abd449f13a06aa5d7388b2dd2926a6011973
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97248233"
---
# <a name="afx_extension_module-structure"></a>Структура AFX_EXTENSION_MODULE

`AFX_EXTENSION_MODULE`Используется во время инициализации библиотек DLL расширения MFC для хранения состояния модуля DLL расширения MFC.

## <a name="syntax"></a>Синтаксис

```
struct AFX_EXTENSION_MODULE
{
    BOOL bInitialized;
    HMODULE hModule;
    HMODULE hResource;
    CRuntimeClass* pFirstSharedClass;
    COleObjectFactory* pFirstSharedFactory;
};
```

#### <a name="parameters"></a>Параметры

*бинитиализед*<br/>
Значение TRUE, если модуль DLL был инициализирован с помощью `AfxInitExtensionModule` .

*хмодуле*<br/>
Задает маркер модуля DLL.

*хресаурце*<br/>
Указывает обработчик настраиваемого модуля ресурсов библиотеки DLL.

*пфирстшаредкласс*<br/>
Указатель на информацию ( `CRuntimeClass` структуру) о первом классе среды выполнения модуля DLL. Используется для задания начала списка классов среды выполнения.

*пфирстшаредфактори*<br/>
Указатель на первую фабрику объектов модуля DLL ( `COleObjectFactory` объект). Используется для предоставления начала списка фабрик класса.

## <a name="remarks"></a>Комментарии

Библиотеки DLL расширения MFC должны выполнять два действия в своей `DllMain` функции:

- Вызовите [афксинитекстенсионмодуле](extension-dll-macros.md#afxinitextensionmodule) и проверьте возвращаемое значение.

- Создайте `CDynLinkLibrary` объект, если библиотека DLL будет экспортировать объекты [крунтимекласс](../../mfc/reference/cruntimeclass-structure.md) или имеет собственные пользовательские ресурсы.

`AFX_EXTENSION_MODULE`Структура используется для хранения копии состояния модуля библиотеки DLL расширения MFC, включая копию объектов класса среды выполнения, которые были инициализированы библиотекой DLL расширения MFC в рамках обычного создания статического объекта, выполняемого перед `DllMain` входом. Пример:

[!code-cpp[NVC_MFC_DLL#2](../../atl-mfc-shared/codesnippet/cpp/afx-extension-module-structure_1.cpp)]

Сведения о модуле, хранящиеся в `AFX_EXTENSION_MODULE` структуре, можно скопировать в `CDynLinkLibrary` объект. Пример:

[!code-cpp[NVC_MFC_DLL#5](../../atl-mfc-shared/codesnippet/cpp/afx-extension-module-structure_2.cpp)]

## <a name="requirements"></a>Требования

**Заголовок:** AFX. h

## <a name="see-also"></a>См. также раздел

[Структуры, стили, обратные вызовы и схемы сообщений](../../mfc/reference/structures-styles-callbacks-and-message-maps.md)<br/>
[AfxInitExtensionModule](extension-dll-macros.md#afxinitextensionmodule)<br/>
[AfxTermExtensionModule](extension-dll-macros.md#afxtermextensionmodule)
