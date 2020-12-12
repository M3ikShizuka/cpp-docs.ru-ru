---
description: 'Дополнительные сведения о:/Zc: __cplusplus (включение обновленного макроса __cplusplus)'
title: /Zc:__cplusplus (включить обновленный макрос __cplusplus)
ms.date: 05/16/2019
f1_keywords:
- /Zc:__cplusplus
helpviewer_keywords:
- -Zc:__cplusplus compiler option (C++)
- __cplusplus macro (C++)
ms.openlocfilehash: 3aa5579a0315c2bba5e74a8a3c191801328fc589
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97114680"
---
# <a name="zc__cplusplus-enable-updated-__cplusplus-macro"></a>/Zc:__cplusplus (включить обновленный макрос __cplusplus)

Параметр компилятора **/Zc: __cplusplus** позволяет макросу препроцессора **\_ \_ кплусплус** сообщить обновленное значение для последней поддержки стандартов языка C++. По умолчанию Visual Studio всегда возвращает значение "199711L" для макроса препроцессора **\_ \_ кплусплус** .

## <a name="syntax"></a>Синтаксис

> **/Zc: __cplusplus**[ **-** ]

## <a name="remarks"></a>Комментарии

Макрос препроцессора **\_ \_ кплусплус** обычно используется для передачи поддержки определенной версии стандарта C++. Так как значительная часть существующего кода требует, чтобы этот макрос имел значение 199711L, компилятор не меняет его, если только вы явно не указали параметр компилятора **/Zc:__cplusplus**. Параметр **/Zc:__cplusplus** доступен начиная с версии 15.7 Visual Studio 2017 и по умолчанию отключен. В более ранних версиях Visual Studio и по умолчанию или, если указан параметр **/Zc: __cplusplus-** , Visual Studio возвращает значение "199711L" для макроса препроцессора **\_ \_ кплусплус** . Параметр [/permissive-](permissive-standards-conformance.md) не включает параметр **/Zc:__cplusplus**.

Если параметр **/Zc: __cplusplus** включен, значение, сообщаемое макросом **\_ \_ кплусплус** , зависит от параметра версии [/std](std-specify-language-standard-version.md) . В таблице ниже представлены возможные значения макроса.

|Параметр /Zc:__cplusplus|Параметр /std:c++|Значение __cplusplus|
|-|-|-|
Zc:__cplusplus|/std:c++14 (по умолчанию)|201402L
Zc:__cplusplus|/std:c++17|201703L
Zc:__cplusplus|/std:c++latest|201704L
Zc:__cplusplus- (отключено)|Любое значение|199711L
Не указано|Любое значение|199711L

Компилятор не поддерживает параметры стандартов C++98, C++03 и C++11.

Для более детального определения изменений в наборе средств компилятора используйте предварительно определенный макрос [_MSC_VER](../../preprocessor/predefined-macros.md). Значение этого встроенного макроса увеличивается при каждом обновлении набора средств в Visual Studio 2017 и более поздних версий. Предварительно определенный макрос [_MSVC_LANG](../../preprocessor/predefined-macros.md) сообщает версию стандарта независимо от того, включен ли параметр **/Zc:__cplusplus**. Когда параметр **/Zc:__cplusplus** включен, `__cplusplus == _MSVC_LANG`.

### <a name="to-set-this-compiler-option-in-visual-studio"></a>Установка параметра компилятора в Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите страницу свойств **Свойства конфигурации**  >  **C/C++**  >  **Командная строка** .

1. Добавьте **/Zc:__cplusplus** или **/Zc:__cplusplus-** в область **Дополнительные параметры**.

## <a name="see-also"></a>См. также раздел

- [/Zc (соответствие)](zc-conformance.md)
- [/std (определение стандартной версии языка)](std-specify-language-standard-version.md)
- [Предустановленные макросы](../../preprocessor/predefined-macros.md)
