---
description: 'Дополнительные сведения о: устранением рисков Spectre'
title: spectre
ms.date: 01/23/2018
f1_keywords:
- spectre_cpp
- spectre
- nomitigation
helpviewer_keywords:
- __declspec keyword (C++), spectre
- spectre __declspec keyword
ms.openlocfilehash: fc1f56a59dea1eaa3596a6f7a7c0347ab822e302
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97113822"
---
# <a name="spectre"></a>spectre

**Блок, относящийся только к системам Microsoft**

Сообщает компилятору, что не нужно вставлять инструкции устранением рисков Spectre с непостоянными барьерами выполнения для функции.

## <a name="syntax"></a>Синтаксис

> **__declspec (устранением рисков Spectre (смягчение))**

## <a name="remarks"></a>Комментарии

Параметр компилятора [/Qspectre](../build/reference/qspectre.md) указывает компилятору на необходимость вставки гипотетических инструкций по барьеру выполнения. Они вставляются, когда анализ указывает на наличие уязвимости устранением рисков Spectre с вариантом 1. Определенные инструкции зависят от процессора. Хотя эти инструкции должны оказать минимальное влияние на размер или производительность кода, возможны случаи, когда код не подвержен воздействию уязвимости и требует максимальной производительности.

Экспертный анализ может определить, что функция является надежной из-за дефекта обхода проверки устранением рисков Spectre с вариантом 1. В этом случае можно подавить создание кода устранения проблем в функции, применив `__declspec(spectre(nomitigation))` к объявлению функции.

> [!CAUTION]
> Инструкции по снижению производительности **/Qspectre** обеспечивают важную защиту и значительно влияют на производительность. Поэтому отключать их не рекомендуется, кроме тех редких случаев, когда производительность функции исключительно важна, а сама функция заведомо безопасна.

## <a name="example"></a>Пример

В приведенном ниже коде показано использование `__declspec(spectre(nomitigation))`.

```cpp
// compile with: /c /Qspectre
static __declspec(spectre(nomitigation))
int noSpectreIssues() {
    // No Spectre variant 1 vulnerability here
    // ...
    return 0;
}

int main() {
    noSpectreIssues();
    return 0;
}
```

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[__declspec](../cpp/declspec.md)<br/>
[Ключевые слова](../cpp/keywords-cpp.md)<br/>
[/Qspectre](../build/reference/qspectre.md)
