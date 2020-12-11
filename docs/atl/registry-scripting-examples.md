---
description: 'Дополнительные сведения о: примеры скриптов для реестра'
title: Примеры сценариев реестра
ms.date: 11/04/2016
helpviewer_keywords:
- scripting, examples
- registrar scripts [ATL]
- scripts, Registrar scripts
- registry, Registrar
ms.assetid: b6df80e1-e08b-40ee-9243-9b381b172460
ms.openlocfilehash: 716aa69ed95c784079e72f9b785fedd8c07b0563
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97157546"
---
# <a name="registry-scripting-examples"></a>Примеры сценариев реестра

В примерах сценариев в этом разделе показано, как добавить ключ в системный реестр, зарегистрировать сервер COM регистратора и указать несколько деревьев синтаксического анализа.

## <a name="add-a-key-to-hkey_current_user"></a>Добавление ключа в HKEY_CURRENT_USER

В следующем дереве синтаксического анализа показан простой скрипт, который добавляет один ключ в системный реестр. В частности, скрипт добавляет ключ, `MyVeryOwnKey` в `HKEY_CURRENT_USER` . Он также присваивает строковое значение по умолчанию `HowGoesIt` новому ключу:

```rgs
HKEY_CURRENT_USER
{
    'MyVeryOwnKey' = s 'HowGoesIt'
}
```

Этот скрипт можно легко расширить для определения нескольких подразделов следующим образом:

```rgs
HKCU
{
    'MyVeryOwnKey' = s 'HowGoesIt'
    {
        'HasASubkey'
        {
            'PrettyCool' = d '55'
            val 'ANameValue' = s 'WithANamedValue'
        }
    }
}
```

Теперь скрипт добавляет подраздел, `HasASubkey` в `MyVeryOwnKey` . Для этого подраздела добавляется `PrettyCool` подраздел (со значением по умолчанию `DWORD` 55) и `ANameValue` именованное значение (со строковым значением `WithANamedValue` ).

## <a name="register-the-registrar-com-server"></a><a name="_atl_register_the_registrar_com_server"></a> Регистрация сервера COM регистратора

Следующий скрипт регистрирует сам COM-сервер регистратора.

```rgs
HKCR
{
    ATL.Registrar = s 'ATL Registrar Class'
    {
        CLSID = s '{44EC053A-400F-11D0-9DCD-00A0C90391D3}'
    }
    NoRemove CLSID
    {
        ForceRemove {44EC053A-400F-11D0-9DCD-00A0C90391D3} = s 'ATL Registrar Class'
        {
            ProgID = s 'ATL.Registrar'
            InprocServer32 = s '%MODULE%'
            {
                val ThreadingModel = s 'Apartment'
            }
        }
    }
}
```

Во время выполнения этот дерево анализа добавляет `ATL.Registrar` ключ в `HKEY_CLASSES_ROOT` . В этот новый раздел:

- Указывает `ATL Registrar Class` в качестве строкового значения по умолчанию для ключа.

- Добавляет `CLSID` в качестве подраздела.

- Указывает `{44EC053A-400F-11D0-9DCD-00A0C90391D3}` для `CLSID` . (Это значение является идентификатором CLSID регистратора для использования с `CoCreateInstance` .)

Поскольку `CLSID` является общим, его не следует удалять в режиме отмены регистрации. Оператор, `NoRemove CLSID` делает это, указывая, что `CLSID` должен быть открыт в режиме Register и проигнорирован в режиме отмены регистрации.

`ForceRemove`Оператор предоставляет функцию обслуживания, удаляя ключ и все его подразделы перед повторной созданием ключа. Это может быть полезно, если имена подразделов изменились. В этом примере скрипта `ForceRemove` проверяет, `{44EC053A-400F-11D0-9DCD-00A0C90391D3}` существует ли уже. Если это так, `ForceRemove` выполните следующие действия:

- Рекурсивно удаляются `{44EC053A-400F-11D0-9DCD-00A0C90391D3}` и все его подразделы.

- Повторное создание `{44EC053A-400F-11D0-9DCD-00A0C90391D3}` .

- Добавляет в `ATL Registrar Class` качестве строкового значения по умолчанию для `{44EC053A-400F-11D0-9DCD-00A0C90391D3}` .

Дерево синтаксического анализа теперь добавляет два новых подраздела в `{44EC053A-400F-11D0-9DCD-00A0C90391D3}` . Первый ключ, `ProgID` , возвращает строковое значение по умолчанию, которое является идентификатором ProgID. Второй ключ, `InprocServer32` , получает строковое значение по умолчанию, `%MODULE%` которое представляет собой значение препроцессора, описанное в разделе [Использование заменяемых параметров (препроцессор регистратора)](../atl/using-replaceable-parameters-the-registrar-s-preprocessor.md)этой статьи. `InprocServer32` также получает именованное значение `ThreadingModel` со строковым значением `Apartment` .

## <a name="specify-multiple-parse-trees"></a>Указание нескольких деревьев синтаксического анализа

Чтобы указать более одного дерева синтаксического анализа в скрипте, просто поместите одно дерево в конец другого. Например, следующий скрипт добавляет ключ `MyVeryOwnKey` в деревья синтаксического анализа для `HKEY_CLASSES_ROOT` и `HKEY_CURRENT_USER` :

```rgs
HKCR
{
    'MyVeryOwnKey' = s 'HowGoesIt'
}
HKEY_CURRENT_USER
{
    'MyVeryOwnKey' = s 'HowGoesIt'
}
```

> [!NOTE]
> В скрипте регистратора 4 КБ — это максимальный размер маркера. (Маркер — это любой распознаваемый элемент в синтаксисе.) В предыдущем примере скрипта,, `HKCR` `HKEY_CURRENT_USER` `'MyVeryOwnKey'` , и `'HowGoesIt'` являются маркерами.

## <a name="see-also"></a>См. также раздел

[Создание скриптов регистратора](../atl/creating-registrar-scripts.md)
