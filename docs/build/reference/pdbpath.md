---
description: Дополнительные сведения о:/ПДБПАС
title: /PDBPATH
ms.date: 11/04/2016
f1_keywords:
- /pdbpath
helpviewer_keywords:
- .pdb files, path
- -PDBPATH dumpbin option
- /PDBPATH dumpbin option
- PDBPATH dumpbin option
- PDB files, path
ms.assetid: ccf67dcd-0b23-4250-ad47-06c48acbe82b
ms.openlocfilehash: 41207d7cfce3d72ecb9517d9ad3af8bcd3f901d7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97226055"
---
# <a name="pdbpath"></a>/PDBPATH

```
/PDBPATH[:VERBOSE] filename
```

### <a name="parameters"></a>Параметры

*filename*<br/>
Имя DLL-или EXE-файла, для которого необходимо найти соответствующий PDB-файл.

**: Verbose**<br/>
Используемых Сообщает обо всех каталогах, в которых была предпринята попытка выполнить обнаружение PDB-файла.

## <a name="remarks"></a>Комментарии

/ПДБПАС будет искать на компьютере те же пути, которые отладчик будет искать PDB-файл, и будет сообщать, какие PDB-файлы соответствуют файлу, указанному в поле *filename*.

При использовании отладчика Visual Studio может возникнуть проблема, связанная с тем, что отладчик использует PDB-файл для другой версии отлаживаемого файла.

/ПДБПАС будет искать PDB-файлы по следующим путям:

- Проверьте папку, в которой находится исполняемый файл.

- Проверьте расположение PDB-файла, записанного в исполняемый файл. Обычно это расположение на момент связывания образа.

- Проверьте путь поиска, настроенный в интегрированной среде разработки Visual Studio.

- Проверьте пути в переменных среды _NT_SYMBOL_PATH и _NT_ALT_SYMBOL_PATH.

- Проверьте каталог Windows.

## <a name="see-also"></a>См. также раздел

[Параметры DUMPBIN](dumpbin-options.md)<br/>
[/PDBALTPATH (использовать альтернативный путь к PDB-файлу)](pdbaltpath-use-alternate-pdb-path.md)
