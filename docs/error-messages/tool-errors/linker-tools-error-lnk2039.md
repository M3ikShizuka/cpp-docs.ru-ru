---
description: 'Дополнительные сведения: Ошибка средств компоновщика LNK2039'
title: Ошибка средств компоновщика LNK2039
ms.date: 11/04/2016
f1_keywords:
- LNK2039
helpviewer_keywords:
- LNK2039
ms.assetid: eaa296bd-4901-41f6-8410-6d03ee827144
ms.openlocfilehash: 34bddbd456e8e588ff6f7818d8db1d3522ccd06a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97275637"
---
# <a name="linker-tools-error-lnk2039"></a>Ошибка средств компоновщика LNK2039

Импорт ссылочного класса " \<type> ", определенного в другом obj-файле; он должен быть либо импортирован, либо определен, но не одновременно

Класс ссылки "<`type`>" импортируется в указанный OBJ-файл, но также определяется в другом obj-файле. Это условие может вызвать сбой во время выполнения или другое непредвиденное поведение.

### <a name="to-correct-this-error"></a>Исправление ошибки

1. Проверьте `type` , должен ли быть определен в другом obj-файле, и убедитесь, что он должен быть импортирован из WINMD-файла.

1. Удалите либо определение, либо импорт.

## <a name="see-also"></a>См. также раздел

[Ошибки и предупреждения средств компоновщика](../../error-messages/tool-errors/linker-tools-errors-and-warnings.md)<br/>
[Ошибка средств компоновщика LNK1332](../../error-messages/tool-errors/linker-tools-error-lnk1332.md)
