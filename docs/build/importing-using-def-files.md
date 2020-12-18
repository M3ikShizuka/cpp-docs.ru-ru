---
description: 'Подробнее о следующем: Импорт с помощью DEF-файлов'
title: Импорт с помощью DEF-файлов
ms.date: 11/04/2016
helpviewer_keywords:
- importing DLLs [C++], DEF files
- def files [C++], importing with
- .def files [C++], importing with
- dllimport attribute [C++], DEF files
- DLLs [C++], DEF files
ms.assetid: aefdbf50-f603-488a-b0d7-ed737bae311d
ms.openlocfilehash: 9eb4face47bf999daa8f969282cc621708a76006
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97156155"
---
# <a name="importing-using-def-files"></a>Импорт с помощью DEF-файлов

Если вы решили использовать **`__declspec(dllimport)`** вместе с DEF-файлом, следует изменить DEF-файл так, чтобы в нем вместо раздела CONSTANT использовался раздел DATA. Это снизит вероятность возникновения проблем из-за неправильного написания кода.

```
// project.def
LIBRARY project
EXPORTS
   ulDataInDll   DATA
```

Причины представлены в таблице ниже.

|Ключевое слово|Результат в библиотеке импорта|Экспортируемые элементы|
|-------------|---------------------------------|-------------|
|`CONSTANT`|`_imp_ulDataInDll`, `_ulDataInDll`|`_ulDataInDll`|
|`DATA`|`_imp_ulDataInDll`|`_ulDataInDll`|

При использовании **`__declspec(dllimport)`** и CONSTANT в библиотеке DLL импорта с расширением LIB, создаваемой для обеспечения явной компоновки, указываются как версия `imp`, так и недекорированное имя. При использовании **`__declspec(dllimport)`** и DATA указывается только версия `imp` имени.

При использовании CONSTANT для доступа к `ulDataInDll` можно использовать любую из следующих конструкций кода:

```
__declspec(dllimport) ULONG ulDataInDll; /*prototype*/
if (ulDataInDll == 0L)   /*sample code fragment*/
```

\-или-

```
ULONG *ulDataInDll;      /*prototype*/
if (*ulDataInDll == 0L)  /*sample code fragment*/
```

Однако если в DEF-файле используется DATA, к переменной `ulDataInDll` будет иметь доступ только код, скомпилированный со следующим определением:

```
__declspec(dllimport) ULONG ulDataInDll;

if (ulDataInDll == 0L)   /*sample code fragment*/
```

Использовать CONSTANT опаснее, так как если вы пропустите дополнительный уровень косвенного обращения, то может случиться так, что вы обратитесь к указателю на переменную в таблице адресов импорта, а не к самой переменной. Подобная проблема часто проявляется как нарушение прав доступа, так как таблица адресов импорта в настоящее время доступна компилятору и компоновщику только для чтения.

По этой причине текущая версия компоновщика MSVC выдает предупреждение при обнаружении CONSTANT в DEF-файле. Единственной реальной причиной использования CONSTANT является невозможность перекомпиляции некоторого объектного файла, если в файле заголовка не содержится **`__declspec(dllimport)`** для прототипа.

## <a name="see-also"></a>См. также

[Импорт в приложение](importing-into-an-application.md)
