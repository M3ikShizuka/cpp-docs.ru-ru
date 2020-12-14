---
description: 'Дополнительные сведения: структура HSE_VERSION_INFO'
title: Структура HSE_VERSION_INFO
ms.date: 11/04/2016
f1_keywords:
- HSE_VERSION_INFO
helpviewer_keywords:
- HSE_VERSION_INFO structure [MFC]
ms.assetid: 4837312d-68c8-4d05-9afa-1934d7d49b20
ms.openlocfilehash: fe03f3c4e00f9af62398993838927ce75410f17b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97219633"
---
# <a name="hse_version_info-structure"></a>Структура HSE_VERSION_INFO

На эту структуру указывает параметр *пвер* в `CHttpServer::GetExtensionVersion` функции-члене. Он предоставляет номер версии ISA и текстовое описание ISA.

## <a name="syntax"></a>Синтаксис

```
typedef struct _HSE_VERSION_INFO {
    DWORD dwExtensionVersion;
    CHAR lpszExtensionDesc[HSE_MAX_EXT_DLL_NAME_LEN];
} HSE_VERSION_INFO, *LPHSE_VERSION_INFO;
```

#### <a name="parameters"></a>Параметры

*двекстенсионверсион*<br/>
Номер версии ISA.

*лпсзекстенсиондеск*<br/>
Текстовое описание ISA. Реализация по умолчанию предоставляет текст заполнителя; Переопределите `CHttpServer::GetExtensionVersion` , чтобы предоставить собственное описание.

## <a name="requirements"></a>Требования

**Заголовок:** хттпекст. h

## <a name="see-also"></a>См. также раздел

[Структуры, стили, обратные вызовы и схемы сообщений](../../mfc/reference/structures-styles-callbacks-and-message-maps.md)
