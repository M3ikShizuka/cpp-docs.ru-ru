---
description: Дополнительные сведения об pragma директиве Component в Microsoft C/C++
title: см pragma
ms.date: 01/22/2021
f1_keywords:
- vc-pragma.component
- component_CPP
helpviewer_keywords:
- component pragma
- pragma, component
no-loc:
- pragma
ms.openlocfilehash: 68a4117439390c6ec978ae9d766efb395a4ceaa4
ms.sourcegitcommit: a26a66a3cf479e0e827d549a9b850fad99b108d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2021
ms.locfileid: "98712951"
---
# <a name="component-no-locpragma"></a>`component` pragma

Управляет сбором сведений о просмотре или сведений о зависимостях из исходных файлов.

## <a name="syntax"></a>Синтаксис

> **`#pragma component( browser,`** { **`on`** \| **`off`** } \[ **`,`** **`references`** \[ **`,`** *имя* ]] **`)`** \
> **`#pragma component( minrebuild,`** { **`on`** \| **`off`** } **`)`** \
> **`#pragma component( mintypeinfo,`** { **`on`** \| **`off`** } **`)`**

## <a name="remarks"></a>Примечания

### <a name="browser"></a>Браузер

Можно включить или отключить сбор информации и задать игнорирование конкретных имен по мере сбора информации.

Использование функции on или Off управляет сбором сведений для просмотра из pragma перенаправления вперед. Например:

```cpp
#pragma component(browser, off)
```

предотвращает сбор информации о просмотре компилятором.

> [!NOTE]
> Чтобы включить сбор сведений для просмотра pragma , [необходимо сначала включить сведения о](../build/reference/building-browse-information-files-overview.md)просмотре.

**`references`** Параметр можно использовать с аргументом *Name* или без него. **`references`** При использовании без *имени* включается или отключается сбор ссылок (другие данные для просмотра по-другому сохраняются). Например:

```cpp
#pragma component(browser, off, references)
```

предотвращает сбор информации о ссылках компилятором.

Использование **`references`** с *именем* и **`off`** предотвращает отображение ссылок на *имя* в окне просмотра сведений. Используйте этот синтаксис, чтобы игнорировать ненужные имена и типы, уменьшая тем самым размер файлов со сведениями о просмотре. Например:

```cpp
#pragma component(browser, off, references, DWORD)
```

игнорирует ссылки на DWORD с этого момента. Вы можете включить сбор ссылок в параметр DWORD обратно с помощью **`on`** :

```cpp
#pragma component(browser, on, references, DWORD)
```

Это единственный способ возобновления сбора ссылок на *имя*; необходимо явно включить любое *имя* , которое вы отключили.

Чтобы запретить препроцессору расширение *имени* (например, расширение null до 0), заключите его в кавычки:

```cpp
#pragma component(browser, off, references, "NULL")
```

### <a name="minimal-rebuild"></a>Минимальное перестроение

Устаревшая функция [ `/Gm` (включение минимального перестроения)](../build/reference/gm-enable-minimal-rebuild.md) требует от компилятора создания и хранения сведений о зависимостях классов C++, что занимает место на диске. Чтобы сэкономить место на диске, можно использовать `#pragma component( minrebuild, off )` каждый раз, когда не требуется выполнять получение сведений о зависимостях, например, в неизменяемых файлах заголовков. Вставьте `#pragma component( minrebuild, on )` после неизменяемых классов, чтобы снова включить сбор зависимостей.

### <a name="reduce-type-information"></a>Сокращение сведений о типах

**`mintypeinfo`** Параметр сокращает отладочную информацию для указанной области. Эти сведения имеют значительный объем, что влияет на размер PDB- и OBJ-файлов. Нельзя отлаживать классы и структуры в **`mintypeinfo`** регионе. Этот **`mintypeinfo`** параметр можно использовать, чтобы избежать появления следующего предупреждения:

```cmd
LINK : warning LNK4018: too many type indexes in PDB "filename", discarding subsequent type information
```

Дополнительные сведения см. в описании параметра компилятора [ `/Gm` (включение минимального перестроения)](../build/reference/gm-enable-minimal-rebuild.md) .

## <a name="see-also"></a>См. также раздел

[Директивы pragma и `__pragma` `_Pragma` Ключевые слова и](./pragma-directives-and-the-pragma-keyword.md)
