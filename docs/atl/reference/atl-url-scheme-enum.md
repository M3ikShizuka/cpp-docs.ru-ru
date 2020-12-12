---
description: 'Дополнительные сведения: ATL_URL_SCHEME'
title: Перечисление ATL_URL_SCHEME
ms.date: 11/04/2016
helpviewer_keywords:
- ATLUTIL/ATL::ATL_URL_SCHEME
ms.assetid: f4131046-8ba0-4ec1-8209-84203f05d20e
ms.openlocfilehash: 72c149345a0e1edd41bfc9b32d1e94ab6477d488
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97165138"
---
# <a name="atl_url_scheme"></a>ATL_URL_SCHEME

Члены этого перечисления предоставляют константы для схем, распознаваемых [фигурой](curl-class.md).

## <a name="syntax"></a>Синтаксис

```cpp
enum ATL_URL_SCHEME{
   ATL_URL_SCHEME_UNKNOWN = -1,
   ATL_URL_SCHEME_FTP     = 0,
   ATL_URL_SCHEME_GOPHER  = 1,
   ATL_URL_SCHEME_HTTP    = 2,
   ATL_URL_SCHEME_HTTPS   = 3,
   ATL_URL_SCHEME_FILE    = 4,
   ATL_URL_SCHEME_NEWS    = 5,
   ATL_URL_SCHEME_MAILTO  = 6,
   ATL_URL_SCHEME_SOCKS   = 7
};
```

## <a name="requirements"></a>Требования

**Заголовок:** файлов atlutil. h

## <a name="see-also"></a>См. также раздел

[Основные понятия](../active-template-library-atl-concepts.md)<br/>
[Перелистывание:: Сетсчеме](curl-class.md#setscheme)<br/>
[Прилистывание:: к схеме](curl-class.md#getscheme)
