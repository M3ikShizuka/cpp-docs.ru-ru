---
description: 'Дополнительные сведения: Библиотека'
title: LIBRARY
ms.date: 11/04/2016
f1_keywords:
- LIBRARY
helpviewer_keywords:
- LIBRARY .def file statement
ms.assetid: 1d7ccc92-e088-4ef7-9ef0-25c3862cc051
ms.openlocfilehash: 3d8c63f323568949cf2fb30935d2557755346422
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97199536"
---
# <a name="library"></a>LIBRARY

Указывает ссылку на создание библиотеки DLL. В то же время LINK создает библиотеку импорта, если в сборке не используется EXP-файл.

```
LIBRARY [library][BASE=address]
```

## <a name="remarks"></a>Комментарии

Аргумент *Library* указывает имя библиотеки DLL. Можно также использовать параметр компоновщика [/out](out-output-file-name.md) для указания имени выхода библиотеки DLL.

Аргумент BASE =*Address* задает базовый адрес, используемый операционной системой для загрузки библиотеки DLL. Этот аргумент переопределяет расположение библиотеки DLL по умолчанию 0x10000000. Дополнительные сведения об основных адресах см. в описании параметра [/base](base-base-address.md) .

Не забывайте использовать параметр компоновщика [/DLL](dll-build-a-dll.md) при ПОСТРОЕНИИ библиотеки DLL.

## <a name="see-also"></a>См. также раздел

[Правила для Module-Definitionных инструкций](rules-for-module-definition-statements.md)
