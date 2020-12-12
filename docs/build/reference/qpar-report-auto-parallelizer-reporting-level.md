---
description: Дополнительные сведения о:/Qpar-report (уровень отчетов Auto-Параллелизатора)
title: /Qpar-report (уровень отчетности автоматического параллелизатора)
ms.date: 11/04/2016
ms.assetid: 562673b9-02da-4bf8-bb64-70bc25ef4651
ms.openlocfilehash: 573ab7535b63ba8d3f19f2917c17709ac7726b38
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97225535"
---
# <a name="qpar-report-auto-parallelizer-reporting-level"></a>/Qpar-report (уровень отчетности автоматического параллелизатора)

Включает функцию создания отчетов в [Auto-параллелизатора](../../parallel/auto-parallelization-and-auto-vectorization.md) компилятора и задает уровень информационных сообщений для вывода во время компиляции.

## <a name="syntax"></a>Синтаксис

```
/Qpar-report:{1}{2}
```

## <a name="remarks"></a>Remarks

**/Qpar-report: 1**<br/>
Выводит информационное сообщение для распараллеленных циклов.

**/Qpar-report: 2**<br/>
Выводит информационное сообщение для распараллеленных циклов, а также для тех циклов, которые не были распараллелены, с указанием кода причины.

Сообщения выводятся в stdout. Если информационные сообщения отсутствуют, то либо код не содержит циклов, либо уровень отчетности не настроен для передачи отчетов о циклах, которые не удалось распараллелить. Дополнительные сведения о кодах причин и сообщениях см. в разделе [сообщения векторизатора и параллелизатора](../../error-messages/tool-errors/vectorizer-and-parallelizer-messages.md).

### <a name="to-set-the-qpar-report-compiler-option-in-visual-studio"></a>Настройка параметра компилятора /Qpar-report в Visual Studio

1. В области **Обозреватель решений** откройте контекстное меню для проекта и выберите пункт **Свойства**.

1. В диалоговом окне **страницы свойств** в разделе **C/C++** выберите пункт **Командная строка**.

1. В поле **Дополнительные параметры** введите `/Qpar-report:1` или `/Qpar-report:2` .

### <a name="to-set-the-qpar-report-compiler-option-programmatically"></a>Настройка параметра компилятора /Qpar-report программным способом

- Используйте пример кода в <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalOptions%2A>.

## <a name="see-also"></a>См. также раздел

[Параметры/q (низкоуровневые операции)](q-options-low-level-operations.md)<br/>
[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)<br/>
[Вектор машинного кода в Visual Studio](/archive/blogs/nativeconcurrency/auto-vectorizer-in-visual-studio-2012-overview)
