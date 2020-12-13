---
description: 'Дополнительные сведения о: Command-Line Warning D9035'
title: Предупреждение командной строки D9035
ms.date: 12/10/2018
f1_keywords:
- D9035
helpviewer_keywords:
- D9035
ms.assetid: 6254f933-e37a-45ba-b860-1a870d1bc8e8
ms.openlocfilehash: a5e667406a16c6da89f5552844ee87899aa14ba0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97136101"
---
# <a name="command-line-warning-d9035"></a>Предупреждение командной строки D9035

> параметр "*параметр*" является устаревшим и будет удален в следующем выпуске

## <a name="remarks"></a>Комментарии

Вы указали параметр компилятора, который будет удален в следующем выпуске компилятора. Если предложено заменить *параметр*, это предупреждение должно следовать за предупреждением [D9036](../../error-messages/tool-errors/command-line-warning-d9036.md).

Указанный параметр все еще работает, но вы должны обновить конфигурацию сборки прямо сейчас. В результате проект, скорее всего, будет продолжать создаваться при обновлении компилятора.

## <a name="see-also"></a>См. также раздел

[Нерекомендуемые и удаленные параметры компилятора](../../build/reference/compiler-options-listed-by-category.md#deprecated-and-removed-compiler-options)<br/>
[D9036 предупреждений командной строки](command-line-warning-d9036.md)
