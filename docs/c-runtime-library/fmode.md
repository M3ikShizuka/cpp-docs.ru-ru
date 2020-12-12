---
description: 'Дополнительные сведения: _fmode'
title: _fmode
ms.date: 11/04/2016
f1_keywords:
- fmode
- _fmode
helpviewer_keywords:
- file translation [C++], default mode
- fmode function
- _fmode function
ms.assetid: ac6df9eb-e5cc-4c54-aff3-373c21983118
ms.openlocfilehash: c4e7932369a2ad63b5498078e46cd5610b679ee0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97303908"
---
# <a name="_fmode"></a>_fmode

Переменная `_fmode` устанавливает режим преобразования файлов по умолчанию — преобразование текстовых значений в двоичные и наоборот. Использование этой глобальной переменной не рекомендуется в силу наличия более безопасных функциональных версий [_get_fmode](../c-runtime-library/reference/get-fmode.md) и [_set_fmode](../c-runtime-library/reference/set-fmode.md), которые должны использоваться вместо глобальной переменной. Об этом объявляется в файле Stdlib.h описанным ниже образом.

## <a name="syntax"></a>Синтаксис

```
extern int _fmode;
```

## <a name="remarks"></a>Remarks

По умолчанию параметр `_fmode` для преобразования в текстовом режиме имеет значение `_O_TEXT`. Для двоичного режима используется параметр `_O_BINARY`.

Значение `_fmode` можно изменить тремя указанными ниже способами.

- Свяжите с Бинмоде. obj. При этом начальное значение параметра `_fmode` будет изменено на `_O_BINARY` , что приведет к `stdin` открытию всех файлов, кроме, `stdout` и, `stderr` в двоичном режиме.

- Вызовите `_get_fmode` или `_set_fmode`, чтобы соответственно получить или задать глобальную переменную `_fmode`.

- Измените значение `_fmode` напрямую, задав его в своей программе.

## <a name="see-also"></a>См. также раздел

[Глобальные переменные](../c-runtime-library/global-variables.md)<br/>
[_get_fmode](../c-runtime-library/reference/get-fmode.md)<br/>
[_set_fmode](../c-runtime-library/reference/set-fmode.md)
