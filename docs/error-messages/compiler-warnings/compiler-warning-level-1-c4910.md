---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4910'
title: Предупреждение компилятора (уровень 1) C4910
ms.date: 11/04/2016
f1_keywords:
- C4910
helpviewer_keywords:
- C4910
ms.assetid: 67963560-fbca-4ca7-93db-06beaf7055f0
ms.openlocfilehash: 4798ba8ae8005239c9cf83e109bdb0f9e4c01928
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97291458"
---
# <a name="compiler-warning-level-1-c4910"></a>Предупреждение компилятора (уровень 1) C4910

" \<identifier> ": "__declspec (dllexport)" и "extern" несовместимы при явном создании экземпляра

Явный экземпляр шаблона с именем *\<identifier>* изменяется как с помощью `__declspec(dllexport)` ключевых слов, так и **`extern`** . Однако эти ключевые слова являются взаимоисключающими. `__declspec(dllexport)`Ключевое слово означает создание экземпляра класса шаблона, а **`extern`** ключевое слово означает, что не создавать экземпляр класса шаблона автоматически.

## <a name="see-also"></a>См. также раздел

[Явное создание экземпляра](../../cpp/explicit-instantiation.md)<br/>
[dllexport, dllimport](../../cpp/dllexport-dllimport.md)<br/>
[Общие правила и ограничения](../../cpp/general-rules-and-limitations.md)
