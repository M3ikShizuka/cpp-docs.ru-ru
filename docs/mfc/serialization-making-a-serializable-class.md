---
description: 'Дополнительные сведения см. в статье сериализация: создание сериализуемого класса'
title: Сериализация. Создание сериализуемого класса
ms.date: 11/04/2016
helpviewer_keywords:
- serializable class [MFC]
- DECLARE_SERIAL macro [MFC]
- default constructor [MFC]
- VERSIONABLE_SCHEMA macro [MFC]
- classes [MFC], derived
- IMPLEMENT_SERIAL macro [MFC]
- no-arguments constructor [MFC]
- Serialize method, overriding
- defaults [MFC], constructor
- CObject class [MFC], deriving serializable classes
- constructors [MFC], defining with no arguments
- serialization [MFC], serializable classes
- no default constructor
ms.assetid: 59a14d32-1cc8-4275-9829-99639beee27c
ms.openlocfilehash: 21c45887199768094953066818acfe1b87d8d45d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97217540"
---
# <a name="serialization-making-a-serializable-class"></a>Сериализация. Создание сериализуемого класса

Чтобы сделать класс сериализуемым, необходимо выполнить пять основных шагов. Они перечислены ниже и описаны в следующих разделах.

1. [Наследование класса от CObject](#_core_deriving_your_class_from_cobject) (или от некоторого класса, производного от `CObject` ).

1. [Переопределение функции, которая является членом сериализации](#_core_overriding_the_serialize_member_function).

1. [С помощью макроса DECLARE_SERIAL](#_core_using_the_declare_serial_macro) в объявлении класса.

1. [Определение конструктора, не принимающего аргументов](#_core_defining_a_constructor_with_no_arguments).

1. [Использование макроса IMPLEMENT_SERIAL в файле реализации](#_core_using_the_implement_serial_macro_in_the_implementation_file) для класса.

Если вы вызываете `Serialize` напрямую, а не с помощью операторов >> и << [CArchive](../mfc/reference/carchive-class.md), то последние три шага не требуются для сериализации.

## <a name="deriving-your-class-from-cobject"></a><a name="_core_deriving_your_class_from_cobject"></a> Наследование класса от CObject

Базовый протокол и функциональные возможности сериализации определяются в `CObject` классе. Путем наследования класса от `CObject` (или от класса, производного от `CObject` ), как показано в следующем объявлении класса `CPerson` , вы получаете доступ к протоколу сериализации и функциональным возможностям `CObject` .

## <a name="overriding-the-serialize-member-function"></a><a name="_core_overriding_the_serialize_member_function"></a> Переопределение функции сериализации элемента

`Serialize`Функция-член, определенная в `CObject` классе, отвечает за фактическую сериализацию данных, необходимых для захвата текущего состояния объекта. `Serialize`Функция имеет `CArchive` аргумент, который используется для чтения и записи данных объекта. Объект [CArchive](../mfc/reference/carchive-class.md) имеет функцию-член, `IsStoring` которая указывает, сохраняется ли `Serialize` (запись данных) или загружается (считывание данных). Используя результаты в `IsStoring` качестве направляющей, вы вставляете данные объекта в `CArchive` объект с помощью оператора вставки ( **<\<**) or extract data with the extraction operator (**>>** ).

Рассмотрим класс, производный от `CObject` и имеющий две новые переменные-члены типов `CString` и **Word**. В следующем фрагменте объявления класса показаны новые переменные члена и объявление переопределенной `Serialize` функции члена:

[!code-cpp[NVC_MFCSerialization#1](../mfc/codesnippet/cpp/serialization-making-a-serializable-class_1.h)]

#### <a name="to-override-the-serialize-member-function"></a>Переопределение функции сериализации элемента

1. Вызовите версию базового класса, `Serialize` чтобы убедиться, что унаследованная часть объекта сериализуется.

1. Вставка или извлечение переменных члена, относящихся к классу.

   Операторы вставки и извлечения взаимодействуют с классом Archive для чтения и записи данных. В следующем примере показано, как реализовать `Serialize` класс, `CPerson` объявленный выше:

   [!code-cpp[NVC_MFCSerialization#2](../mfc/codesnippet/cpp/serialization-making-a-serializable-class_2.cpp)]

Для чтения и записи больших объемов нетипизированных данных можно также использовать функции членов [CArchive:: Read](../mfc/reference/carchive-class.md#read) и [CArchive:: Write](../mfc/reference/carchive-class.md#write) .

## <a name="using-the-declare_serial-macro"></a><a name="_core_using_the_declare_serial_macro"></a> Использование макроса DECLARE_SERIAL

Макрос DECLARE_SERIAL требуется в объявлении классов, которые будут поддерживать сериализацию, как показано ниже:

[!code-cpp[NVC_MFCSerialization#3](../mfc/codesnippet/cpp/serialization-making-a-serializable-class_3.h)]

## <a name="defining-a-constructor-with-no-arguments"></a><a name="_core_defining_a_constructor_with_no_arguments"></a> Определение конструктора без аргументов

MFC требует конструктора по умолчанию при повторном создании объектов при их десериализации (Загрузка с диска). Процесс десериализации будет заполнять все переменные-члены значениями, необходимыми для повторного создания объекта.

Этот конструктор может быть объявлен как открытый, защищенный или частный. Если вы сделаете ее защищенной или закрытой, убедитесь, что она будет использоваться только функциями сериализации. Конструктор должен перевести объект в состояние, позволяющее удалять его при необходимости.

> [!NOTE]
> Если вы забыли определить конструктор без аргументов в классе, который использует макросы DECLARE_SERIAL и IMPLEMENT_SERIAL, в строке, где используется макрос IMPLEMENT_SERIAL, будет выдано предупреждение о недоступности конструктора по умолчанию.

## <a name="using-the-implement_serial-macro-in-the-implementation-file"></a><a name="_core_using_the_implement_serial_macro_in_the_implementation_file"></a> Использование макроса IMPLEMENT_SERIAL в файле реализации

Макрос IMPLEMENT_SERIAL используется для определения различных функций, необходимых при наследовании сериализуемого класса от `CObject` . Этот макрос используется в файле реализации (. CPP) для класса. Первыми двумя аргументами макроса являются имя класса и имя его непосредственного базового класса.

Третьим аргументом этого макроса является номер схемы. Номер схемы по сути является номером версии для объектов класса. Используйте целое число, большее или равное 0, для номера схемы. (Не путайте этот номер схемы с терминологией базы данных.)

Код сериализации MFC проверяет номер схемы при считывании объектов в память. Если номер схемы объекта на диске не соответствует номеру схемы класса в памяти, Библиотека выдает исключение `CArchiveException` , предотвращая считывание программой неверной версии объекта.

Если требуется `Serialize` , чтобы функция-член могла считывать несколько версий, то есть файлы, написанные с разными версиями приложения, можно использовать значение *VERSIONABLE_SCHEMA* в качестве аргумента для макроса IMPLEMENT_SERIAL. Сведения об использовании и пример см. в разделе `GetObjectSchema` функция Member класса `CArchive` .

В следующем примере показано, как использовать IMPLEMENT_SERIAL для класса, `CPerson` который является производным от `CObject` :

[!code-cpp[NVC_MFCSerialization#4](../mfc/codesnippet/cpp/serialization-making-a-serializable-class_4.cpp)]

После создания сериализуемого класса можно сериализовать объекты класса, как описано в статье [сериализация: сериализация объекта](../mfc/serialization-serializing-an-object.md).

## <a name="see-also"></a>См. также

[Сериализация](../mfc/serialization-in-mfc.md)
