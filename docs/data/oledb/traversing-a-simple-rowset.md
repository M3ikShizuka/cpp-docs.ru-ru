---
description: 'Дополнительные сведения: обход простого набора строк'
title: Перебор простого набора строк
ms.date: 10/19/2018
helpviewer_keywords:
- data access [C++], rowsets
- rowsets [C++], accessing
- simple rowsets
- OLE DB consumers [C++], database attributes
- accessors [C++], rowsets
ms.assetid: b45acf16-4029-429d-ab8d-b7fba98b9740
ms.openlocfilehash: f2e0c1f9647e168d8de2a10eaea6425bf9ad5a88
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97272634"
---
# <a name="traversing-a-simple-rowset"></a>Перебор простого набора строк

В следующем примере показан быстрый и простой доступ к базе данных, который не затрагивает команды. Следующий код потребителя в проекте ATL извлекает записи из таблицы с именем « *исполнители* » в базе данных Microsoft Access с помощью поставщика Microsoft OLE DB для ODBC. Код создает объект таблицы [CTable](../../data/oledb/ctable-class.md) с методом доступа на основе класса записей пользователя `CArtists` . Он открывает подключение, открывает сеанс для соединения и открывает таблицу в сеансе.

```cpp
#include <atldbcli.h>
#include <iostream>

using namespace std;

int main()
{
    CDataSource connection;
    CSession session;
    CTable<CAccessor<CArtists>> artists;

    LPCSTR clsid; // Initialize CLSID_MSDASQL here
    LPCTSTR pName = L"NWind";

    // Open the connection, session, and table, specifying authentication
    // using Windows NT integrated security. Hard-coding a password is a major
    // security weakness.
    connection.Open(clsid, pName, NULL, NULL, DBPROP_AUTH_INTEGRATED);

    session.Open(connection);

    artists.Open(session, "Artists");

    // Get data from the rowset
    while (artists.MoveNext() == S_OK)
    {
       cout << artists.m_szFirstName;
       cout << artists.m_szLastName;
    }

    return 0;
}
```

Запись пользователя выглядит, `CArtists` как в следующем примере:

```cpp
class CArtists
{
public:
// Data Elements
   CHAR m_szFirstName[20];
   CHAR m_szLastName[30];
   short m_nAge;

// Column binding map
BEGIN_COLUMN_MAP(CArtists)
   COLUMN_ENTRY(1, m_szFirstName)
   COLUMN_ENTRY(2, m_szLastName)
   COLUMN_ENTRY(3, m_nAge)
END_COLUMN_MAP()
};
```

## <a name="see-also"></a>См. также раздел

[Работа с шаблонами потребителей OLE DB](../../data/oledb/working-with-ole-db-consumer-templates.md)
