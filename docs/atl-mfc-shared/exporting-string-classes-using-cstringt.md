---
description: 'Дополнительные сведения: экспорт строковых классов с помощью CStringT'
title: Экспорт строковых классов с помощью CStringT
ms.date: 11/04/2016
helpviewer_keywords:
- CStringT class, exporting strings
ms.assetid: bdfc441e-8d2a-461c-9885-46178066c09f
ms.openlocfilehash: 8876ea04f1252e4f5861a950b04dabcd99d6a804
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97166997"
---
# <a name="exporting-string-classes-using-cstringt"></a>Экспорт строковых классов с помощью CStringT

В прошлом разработчики MFC производят наследование от `CString` для специализации собственных строковых классов. В Microsoft Visual C++ .NET (MFC 8,0) класс [CString](../atl-mfc-shared/using-cstring.md) был заменен классом шаблона с именем [CStringT](../atl-mfc-shared/reference/cstringt-class.md). Это предоставляет несколько преимуществ.

- Он позволял `CString` использовать класс MFC в проектах ATL без компоновки в более крупной статической библиотеке MFC или библиотеке DLL.

- Новый `CStringT` класс шаблона позволяет настроить `CString` поведение с помощью параметров шаблона, определяющих признаки символов, аналогично шаблонам в стандартной библиотеке C++.

- При экспорте собственного класса строк из библиотеки DLL с помощью `CStringT` компилятор также автоматически экспортирует `CString` базовый класс. Поскольку `CString` сам по себе является классом шаблона, он может быть создан компилятором при использовании, если только компилятор не знает, что `CString` импортируется из библиотеки DLL. Если перенесены проекты из Visual C++ 6,0 в Visual C++ .NET, возможно, обнаружены ошибки символов компоновщика для определенного умножения из- `CString` за конфликта `CString` импорта из библиотеки DLL и версии, созданной локально. Правильный способ этого приведен ниже.

Следующий сценарий приведет к тому, что компоновщик создаст ошибки символов для умножения определенных классов. Предположим, что экспортируется `CString` производный `CMyString` от библиотеки DLL расширения MFC класс ():

[!code-cpp[NVC_MFC_DLL#6](../atl-mfc-shared/codesnippet/cpp/exporting-string-classes-using-cstringt_1.cpp)]

В коде потребителя используется сочетание `CString` и `CMyString` . "MyString. h" не включен в предкомпилированный заголовок, и некоторые случаи использования `CString` не `CMyString` отображаются.

Предположим, что вы используете `CString` `CMyString` классы и в отдельных исходных файлах: Source1. cpp и source2. cpp. В Source1. cpp используется `CMyString` и #include MyString. h. В source2. cpp используется `CString` , но не #include MyString. h. В этом случае компоновщику будет выдастся `CStringT` определенное умножение. Это вызвано `CString` импортом из библиотеки DLL, которая экспортируется `CMyString` и создается локально компилятором через `CStringT` шаблон.

Чтобы устранить эту проблему, выполните следующие действия.

Экспортируйте `CStringA` и `CStringW` (и необходимые базовые классы) из MFC90.DLL. Проекты, включающие MFC, всегда будут использовать экспортированные библиотеки MFC `CStringA` и `CStringW` , как в предыдущих реализациях MFC.

Затем создайте экспортируемый производный класс с помощью `CStringT` шаблона, как показано `CStringT_Exported` ниже, например:

[!code-cpp[NVC_MFC_DLL#7](../atl-mfc-shared/codesnippet/cpp/exporting-string-classes-using-cstringt_2.cpp)]

В Афксстр. h замените предыдущие `CString` , `CStringA` и `CStringW` typedef следующим образом:

[!code-cpp[NVC_MFC_DLL#8](../atl-mfc-shared/codesnippet/cpp/exporting-string-classes-using-cstringt_3.cpp)]

Существует несколько предостережений.

- Не следует экспортировать `CStringT` сам себя, так как это приведет к экспорту специализированного класса в проекты, предназначенные только для ATL `CStringT` .

- Использование экспортируемого производного класса с помощью `CStringT` функции Minimize не требует повторной реализации `CStringT` функциональности. Дополнительный код ограничен перенаправлением конструкторы на `CStringT` базовый класс.

- `CString`, `CStringA` и `CStringW` должны быть помечены только `__declspec(dllexport/dllimport)` при построении с помощью общей библиотеки DLL MFC. При компоновке с помощью статической библиотеки MFC не следует помечать эти классы как экспортированные. в противном случае внутреннее использование `CString` , `CStringA` и `CStringW` внутри пользовательских библиотек DLL также будет помечено `CString` как экспортированное.

## <a name="related-topics"></a>См. также

[Класс CStringT](../atl-mfc-shared/reference/cstringt-class.md)

## <a name="see-also"></a>См. также раздел

[Использование CStringT](../atl-mfc-shared/using-cstringt.md)<br/>
[Использование CString](../atl-mfc-shared/using-cstring.md)
