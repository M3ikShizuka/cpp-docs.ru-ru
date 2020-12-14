---
description: 'Дополнительные сведения о: ЗАГЛУШКа'
title: STUB
ms.date: 11/04/2016
f1_keywords:
- STUB
helpviewer_keywords:
- STUB .def file statement
ms.assetid: 0a3b9643-19ed-47e9-8173-ee16bc8ed056
ms.openlocfilehash: 79a2002c119bf211652e2aab51d9656b36e3d159
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97230293"
---
# <a name="stub"></a>STUB

При использовании в файле определения модуля, который создает драйвер виртуального устройства (VxD), позволяет указать имя файла, содержащего структуру IMAGE_DOS_HEADER (определенную в WINNT. H) для использования в драйвере виртуального устройства (VxD), а не в заголовке по умолчанию.

```
STUB:filename
```

## <a name="remarks"></a>Комментарии

Эквивалентным образом указать *filename* можно с помощью параметра компоновщика [/stub прилагает](stub-ms-dos-stub-file-name.md) .

ЗАГЛУШКа допустима в файле определения модуля только при создании VxD.

## <a name="see-also"></a>См. также раздел

[Правила для Module-Definitionных инструкций](rules-for-module-definition-statements.md)
