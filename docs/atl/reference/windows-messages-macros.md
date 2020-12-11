---
description: 'Дополнительные сведения: макросы сообщений Windows'
title: Макросы сообщений Windows
ms.date: 11/04/2016
f1_keywords:
- atlbase/ATL::WM_FORWARDMSG
ms.assetid: 63abd22c-372d-4148-bb04-c605950ae64f
ms.openlocfilehash: be5913c5eaa88ca0020a978f2b3f6686a6756715
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97157585"
---
# <a name="windows-messages-macros"></a>Макросы сообщений Windows

Этот макрос пересылает оконные сообщения.

|Имя|Описание|
|-|-|
|[WM_FORWARDMSG](#wm_forwardmsg)|Используется для пересылки сообщения, полученного окном, в другое окно для обработки.|

## <a name="requirements"></a>Требования

**Заголовок:** atlbase. h

## <a name="wm_forwardmsg"></a><a name="wm_forwardmsg"></a> WM_FORWARDMSG

Этот макрос пересылает сообщение, полученное окном, в другое окно для обработки.

```
WM_FORWARDMSG
```

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если сообщение было обработано, ноль, если нет.

### <a name="remarks"></a>Комментарии

Используйте WM_FORWARDMSG для пересылки сообщения, полученного окном, в другое окно для обработки. Параметры LPARAM и WPARAM используются следующим образом:

|Параметр|Использование|
|---------------|-----------|
|WPARAM|Данные, определенные пользователем|
|LPARAM|Указатель на `MSG` структуру, содержащую сведения о сообщении|

### <a name="example"></a>Пример

В следующем примере `m_hWndOther` представляет другое окно, которое получает это сообщение.

[!code-cpp[NVC_ATL_Windowing#137](../../atl/codesnippet/cpp/windows-messages-macros_1.cpp)]

## <a name="see-also"></a>См. также раздел

[Макросы](../../atl/reference/atl-macros.md)
