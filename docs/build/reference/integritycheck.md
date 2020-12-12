---
description: Дополнительные сведения о:/INTEGRITYCHECK
title: /INTEGRITYCHECK
ms.date: 12/28/2017
f1_keywords:
- /INTEGRITYCHECK
helpviewer_keywords:
- -INTEGRITYCHECK editbin options
- /INTEGRITYCHECK editbin options
- INTEGRITYCHECK editbin options
ms.openlocfilehash: b1ea8275bdb356febcf18a2a55b6ab718d8eea96
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97199666"
---
# <a name="integritycheck"></a>/INTEGRITYCHECK

Указывает, что цифровая подпись двоичного образа должна проверяться во время загрузки.

> **/INTEGRITYCHECK**[**: нет**]

## <a name="remarks"></a>Комментарии

В заголовке DLL-файла или исполняемого файла этот параметр задает флаг, для которого диспетчер памяти требует проверку цифровой подписи, чтобы загрузить образ в Windows. В версиях Windows, предшествовавших Windows Vista, этот флаг не учитывается. Этот параметр должен быть установлен для 64-разрядных библиотек DLL, реализующих код режима ядра, и рекомендуется для всех драйверов устройств. Дополнительные сведения см. в разделе [требования подписывания кода в режиме ядра](/windows-hardware/drivers/install/kernel-mode-code-signing-requirements--windows-vista-and-later-).

## <a name="see-also"></a>См. также раздел

[Параметры EDITBIN](editbin-options.md)
