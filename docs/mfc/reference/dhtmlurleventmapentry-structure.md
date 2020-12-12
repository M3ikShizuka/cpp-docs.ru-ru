---
description: 'Дополнительные сведения о: структура Дхтмлурлевентмапентри'
title: DHtmlUrlEventMapEntry Structure
ms.date: 11/04/2016
f1_keywords:
- DHtmlUrlEventMapEntry
helpviewer_keywords:
- DHtmlUrlEventMapEntry structure [MFC]
ms.assetid: 43117c1f-1a51-406c-aa2f-fea647080049
ms.openlocfilehash: c35e3ac70d8530042ca73397b0f7c6df13501497
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97220062"
---
# <a name="dhtmlurleventmapentry-structure"></a>DHtmlUrlEventMapEntry Structure

Эта `DHtmlUrlEventMapEntry` структура обеспечивает поддержку схемы событий с несколькими URL-адресами.

## <a name="syntax"></a>Синтаксис

```
struct DHtmlUrlEventMapEntry
{
LPCTSTR szUrl;
const DHtmlEventMapEntry *pEventMap;
};
```

#### <a name="parameters"></a>Параметры

*сзурл*<br/>
URL-адрес.

*певентмап*<br/>
Схема событий, связанная с URL-адресом.

## <a name="requirements"></a>Требования

**Заголовок:** афксдхтмл. h

## <a name="see-also"></a>См. также раздел

[Структуры, стили, обратные вызовы и схемы сообщений](../../mfc/reference/structures-styles-callbacks-and-message-maps.md)
