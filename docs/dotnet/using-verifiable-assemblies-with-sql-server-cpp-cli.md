---
description: Дополнительные сведения см. в статье Использование проверяемых сборок с SQL Server (C++/CLI)
title: Использование проверяемых сборок вместе с SQL Server (C++/CLI)
ms.date: 10/17/2018
helpviewer_keywords:
- verifiable assemblies [C++], with SQL Server
ms.assetid: 5248a60d-aa88-4ff3-b30a-b791c3ea2de9
ms.openlocfilehash: b155fb0360fb373f5931f51de3af557d06858a71
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97204203"
---
# <a name="using-verifiable-assemblies-with-sql-server-ccli"></a>Использование проверяемых сборок вместе с SQL Server (C++/CLI)

Расширенные хранимые процедуры, Упакованные в библиотеки динамической компоновки (DLL), предоставляют способ расширения функциональных возможностей SQL Server с помощью функций, разработанных с помощью Visual C++. Расширенные хранимые процедуры реализуются как функции внутри библиотек DLL. Помимо функций, расширенные хранимые процедуры могут также определять [определяемые пользователем типы](../cpp/classes-and-structs-cpp.md) и агрегатные функции (например, Sum или AVG).

Когда клиент выполняет расширенную хранимую процедуру, SQL Server ищет библиотеку DLL, связанную с расширенной хранимой процедурой, и загружает библиотеку DLL. SQL Server вызывает запрошенную расширенную хранимую процедуру и выполняет ее в указанном контексте безопасности. Затем Расширенная хранимая процедура передает результирующие наборы и возвращает параметры обратно на сервер.

SQL Server предоставляет расширения Transact-SQL (T-SQL), позволяющие устанавливать проверяемые сборки в SQL Server. SQL Server набор разрешений определяет контекст безопасности со следующими уровнями безопасности:

- Неограниченный режим: выполнение кода с собственным риском; код не обязательно должен быть проверен типобезопасным.

- Защищенный режим: запустите проверяемый код типесафе. компилируется с/CLR: Сейф.

> [!IMPORTANT]
> Visual Studio 2015 устарела и Visual Studio 2017 не поддерживает создание проверяемых проектов с помощью **/clr: pure** и **/clr:** Если требуется проверяемый код, рекомендуется преобразовать код в C#.

Чтобы создать и загрузить проверяемую сборку в SQL Server, используйте команды Transact-SQL создать СБОРКУ и удалить СБОРКУ следующим образом:

```sql
CREATE ASSEMBLY <assemblyName> FROM <'Assembly UNC Path'> WITH
  PERMISSION_SET <permissions>
DROP ASSEMBLY <assemblyName>
```

Команда PERMISSION_SET указывает контекст безопасности и может иметь значения без ограничений, безопасный или расширенный.

Кроме того, можно использовать команду CREATE FUNCTION для привязки к именам методов в классе:

```sql
CREATE FUNCTION <FunctionName>(<FunctionParams>)
RETURNS returnType
[EXTERNAL NAME <AssemblyName>:<ClassName>::<StaticMethodName>]
```

## <a name="example"></a>Пример

Следующий скрипт SQL (например, "MyScript. SQL") загружает сборку в SQL Server и делает доступным метод класса:

```sql
-- Create assembly without external access
drop assembly stockNoEA
go
create assembly stockNoEA
from
'c:\stockNoEA.dll'
with permission_set safe

-- Create function on assembly with no external access
drop function GetQuoteNoEA
go
create function GetQuoteNoEA(@sym nvarchar(10))
returns real
external name stockNoEA:StockQuotes::GetQuote
go

-- To call the function
select dbo.GetQuoteNoEA('MSFT')
go
```

Скрипты SQL могут выполняться интерактивно в анализаторе запросов SQL или в командной строке с помощью служебной программы sqlcmd.exe. Следующая командная строка подключается к MyServer, использует базу данных по умолчанию, использует доверенное соединение, входные данные MyScript. SQL и выходные данные MyResult.txt.

```cmd
sqlcmd -S MyServer -E -i myScript.sql -o myResult.txt
```

## <a name="see-also"></a>См. также

[Классы и структуры](../cpp/classes-and-structs-cpp.md)
