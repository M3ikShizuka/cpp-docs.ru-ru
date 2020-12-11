---
description: 'Дополнительные сведения: программирование с помощью CComBSTR (ATL)'
title: Программирование с использованием CComBSTR (ATL)
ms.date: 11/04/2016
helpviewer_keywords:
- CComBSTR class, programming with
- Unicode, using CComBSTR [ATL]
ms.assetid: d3bd0851-d132-4be9-9c4c-6ccba17acb2b
ms.openlocfilehash: 6c348d703aeaeba40f1f47b8f6fd0ee858b7babd
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97159223"
---
# <a name="programming-with-ccombstr-atl"></a>Программирование с использованием CComBSTR (ATL)

Класс ATL [CComBSTR](../atl/reference/ccombstr-class.md) предоставляет оболочку для типа данных BSTR. Хотя `CComBSTR` это полезное средство, существует несколько ситуаций, требующих осторожности.

- [Проблемы преобразования](#programmingwithccombstr_conversionissues)

- [Проблемы с областью действия](#programmingwithccombstr_scopeissues)

- [Явное освобождение объекта CComBSTR](#programmingwithccombstr_explicitlyfreeing)

- [Использование объектов CComBSTR в циклах](#programmingwithccombstr_usingloops)

- [Проблемы с утечкой памяти](#programmingwithccombstr_memoryleaks)

## <a name="conversion-issues"></a><a name="programmingwithccombstr_conversionissues"></a> Проблемы преобразования

Хотя несколько `CComBSTR` методов автоматически преобразуют строковый аргумент ANSI в Юникод, методы всегда возвращают строки формата Юникода. Чтобы преобразовать выходную строку обратно в ANSI, используйте класс преобразования ATL. Дополнительные сведения о классах преобразования ATL см. в статье [макросы преобразования строк ATL и MFC](reference/string-conversion-macros.md).

### <a name="example"></a>Пример

[!code-cpp[NVC_ATL_Utilities#114](../atl/codesnippet/cpp/programming-with-ccombstr-atl_1.cpp)]

Если для изменения объекта используется строковый литерал `CComBSTR` , используйте строки расширенных символов. Это позволит сократить ненужные преобразования.

### <a name="example"></a>Пример

[!code-cpp[NVC_ATL_Utilities#115](../atl/codesnippet/cpp/programming-with-ccombstr-atl_2.cpp)]

## <a name="scope-issues"></a><a name="programmingwithccombstr_scopeissues"></a> Проблемы с областью действия

Как и в случае с правильно настроенным классом, `CComBSTR` освобождает ресурсы при выходе за пределы области действия. Если функция возвращает указатель на `CComBSTR` строку, это может вызвать проблемы, так как указатель будет ссылаться на память, которая уже была освобождена. В этих случаях используйте `Copy` метод, как показано ниже.

### <a name="example"></a>Пример

[!code-cpp[NVC_ATL_Utilities#116](../atl/codesnippet/cpp/programming-with-ccombstr-atl_3.cpp)]

## <a name="explicitly-freeing-the-ccombstr-object"></a><a name="programmingwithccombstr_explicitlyfreeing"></a> Явное освобождение объекта CComBSTR

Можно явно освободить строку, содержащуюся в `CComBSTR` объекте, до того, как объект выйдет из области. Если строка освобождена, то `CComBSTR` объект является недопустимым.

### <a name="example"></a>Пример

[!code-cpp[NVC_ATL_Utilities#117](../atl/codesnippet/cpp/programming-with-ccombstr-atl_4.cpp)]

## <a name="using-ccombstr-objects-in-loops"></a><a name="programmingwithccombstr_usingloops"></a> Использование объектов CComBSTR в циклах

Поскольку `CComBSTR` класс выделяет буфер для выполнения определенных операций, таких как `+=` оператор или `Append` метод, не рекомендуется выполнять обработку строк внутри строгого цикла. В таких ситуациях `CStringT` обеспечивает лучшую производительность.

### <a name="example"></a>Пример

[!code-cpp[NVC_ATL_Utilities#118](../atl/codesnippet/cpp/programming-with-ccombstr-atl_5.cpp)]

## <a name="memory-leak-issues"></a><a name="programmingwithccombstr_memoryleaks"></a> Проблемы с утечкой памяти

Передача адреса, инициализированного `CComBSTR` в функцию в качестве параметра **[out]** , приводит к утечке памяти.

В приведенном ниже примере строка, выделенная для хранения строки, `"Initialized"` была утечкой, когда функция `MyGoodFunction` заменяет строку.

[!code-cpp[NVC_ATL_Utilities#119](../atl/codesnippet/cpp/programming-with-ccombstr-atl_6.cpp)]

Чтобы избежать утечки, вызовите `Empty` метод для существующих `CComBSTR` объектов перед передачей адреса в качестве параметра **[out]** .

Обратите внимание, что один и тот же код не приведет к утечке, если параметр функции был **[in, out]**.

## <a name="see-also"></a>См. также раздел

[Основные понятия](../atl/active-template-library-atl-concepts.md)<br/>
[Класс CStringT](../atl-mfc-shared/reference/cstringt-class.md)<br/>
[wstring](../standard-library/basic-string-class.md)<br/>
[Макросы преобразования строк](../atl/reference/string-conversion-macros.md)
