---
description: 'Дополнительные сведения о: или TLS'
title: /TLS
ms.date: 11/04/2016
f1_keywords:
- /TLS
helpviewer_keywords:
- /TLS dumpbin option
- -TLS dumpbin option
ms.assetid: 2b3f48f9-cac4-4351-b15c-2833b43bc709
ms.openlocfilehash: a21ef03210a65bb50899ba3907911272ac52b0db
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97229955"
---
# <a name="tls"></a>/TLS

Отображает структуру IMAGE_TLS_DIRECTORY из исполняемого файла.

## <a name="remarks"></a>Комментарии

Или TLS отображает поля структуры TLS, а также адреса функций обратного вызова TLS.

Если программа не использует локальное хранилище потока, ее образ не будет содержать структуру TLS.  Дополнительные сведения см. в разделе [Thread](../../cpp/thread.md) .

IMAGE_TLS_DIRECTORY определен в Winnt. h.

## <a name="see-also"></a>См. также раздел

[Параметры DUMPBIN](dumpbin-options.md)
