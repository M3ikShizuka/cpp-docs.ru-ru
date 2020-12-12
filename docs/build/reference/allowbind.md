---
description: Дополнительные сведения о:/ALLOWBIND
title: /ALLOWBIND
ms.date: 11/04/2016
f1_keywords:
- /allowbind_bind
helpviewer_keywords:
- ALLOWBIND editbin option
- /ALLOWBIND editbin option
- -ALLOWBIND editbin option
ms.assetid: eaadbb8c-4339-4281-9a75-3a1ce2352ff8
ms.openlocfilehash: 54f3056240537d765a9212e774a9a313ded49dab
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97179607"
---
# <a name="allowbind"></a>/ALLOWBIND

Указывает, может ли быть привязана библиотека DLL.

```

/ALLOWBIND[:NO]
```

## <a name="remarks"></a>Комментарии

Параметр **/ALLOWBIND** задает бит в заголовке библиотеки DLL, который указывает, Bind.exe что изображение может быть привязано. Привязка позволяет быстрее загружать изображение, когда загрузчику не нужно перегружаться и выполнять исправление адресов для каждой библиотеки DLL, на которую указывает ссылка. Вы не хотите, чтобы библиотека DLL была привязана, если она подписана цифровой подписью, а привязывание сделает сигнатуру недействительной. Привязка не действует, если для образа включен случайный выбор структуры адресного пространства (ASLR) с помощью **/DynamicBase** для версий Windows, поддерживающих ASLR.

Используйте **/ALLOWBIND: No** , чтобы предотвратить ПРИВЯЗКУ библиотеки DLL к Bind.exe.

Дополнительные сведения см. в описании параметра компоновщика [/ALLOWBIND](allowbind-prevent-dll-binding.md) .

## <a name="see-also"></a>См. также раздел

[Параметры EDITBIN](editbin-options.md)
