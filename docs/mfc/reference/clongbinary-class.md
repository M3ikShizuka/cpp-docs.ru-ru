---
description: 'Дополнительные сведения о: CLongBinary Class'
title: Класс CLongBinary
ms.date: 11/04/2016
f1_keywords:
- CLongBinary
- AFXDB_/CLongBinary
- AFXDB_/CLongBinary::CLongBinary
- AFXDB_/CLongBinary::m_dwDataLength
- AFXDB_/CLongBinary::m_hData
helpviewer_keywords:
- CLongBinary class [MFC]
ms.assetid: f4320059-aeb4-4ee5-bc2b-25f19d898ef5
ms.openlocfilehash: ad6836ce6ee7e95929f69d226dcab61fc5482277
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97336717"
---
# <a name="clongbinary-class"></a>Класс CLongBinary

Упрощает работу с очень большими объектами двоичных данных (BLOB-объектами) в базе данных.

## <a name="syntax"></a>Синтаксис

```
class CLongBinary : public CObject
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CLongBinary:: CLongBinary](#clongbinary)|Формирует объект `CLongBinary`.|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[CLongBinary:: m_dwDataLength](#m_dwdatalength)|Содержит фактический размер объекта данных в байтах, в котором хранится его обработчик `m_hData` .|
|[CLongBinary:: m_hData](#m_hdata)|Содержит обработчик ХГЛОБАЛ Windows для фактического объекта Image.|

## <a name="remarks"></a>Комментарии

Например, поле записи в таблице SQL может содержать точечный рисунок, представляющий изображение. `CLongBinary`Объект хранит такой объект и отслеживает его размер.

> [!NOTE]
> Как правило, рекомендуется использовать [CByteArray](../../mfc/reference/cbytearray-class.md) в сочетании с функцией [DFX_Binary](record-field-exchange-functions.md#dfx_binary) . Вы по-прежнему можете использовать `CLongBinary` , но в целом `CByteArray` предоставляет больше функциональных возможностей в Win32, так как отсутствует ограничение размера, обнаруженное 16-разрядным `CByteArray` . Это рекомендации применимы к программированию с помощью объектов доступа к данным (DAO) и ODBC.

Чтобы использовать `CLongBinary` объект, объявите элемент данных поля типа `CLongBinary` в классе набора записей. Этот член будет внедренным элементом класса Recordset и будет создан при создании набора записей. После создания `CLongBinary` объекта механизм обмена полями записей (RFX) загружает объект данных из поля текущей записи в источнике данных и сохраняет его обратно в запись при обновлении записи. RFX запрашивает у источника данных размер большого двоичного объекта, выделяет для него хранилище (через `CLongBinary` `m_hData` элемент данных объекта) и сохраняет в `HGLOBAL` нем обработчик `m_hData` . RFX также хранит фактический размер объекта данных в элементе `m_dwDataLength` данных. Работа с данными в объекте `m_hData` с помощью тех же методов, которые обычно используются для работы с данными, хранящимися в `HGLOBAL` обработчике Windows.

При уничтожении набора записей внедренный `CLongBinary` объект также уничтожается, и его деструктор освобождает `HGLOBAL` маркер данных.

Дополнительные сведения о больших объектах и использовании см `CLongBinary` . в статьях [набор записей (ODBC)](../../data/odbc/recordset-odbc.md) и [набор записей. Работа с большими элементами данных (ODBC)](../../data/odbc/recordset-working-with-large-data-items-odbc.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

`CLongBinary`

## <a name="requirements"></a>Требования

**Заголовок:** afxdb_. h

## <a name="clongbinaryclongbinary"></a><a name="clongbinary"></a> CLongBinary:: CLongBinary

Формирует объект `CLongBinary`.

```
CLongBinary();
```

## <a name="clongbinarym_dwdatalength"></a><a name="m_dwdatalength"></a> CLongBinary:: m_dwDataLength

Сохраняет фактический размер в байтах данных, хранящихся в ХГЛОБАЛном маркере в `m_hData` .

```
SQLULEN m_dwDataLength;
```

### <a name="remarks"></a>Комментарии

Этот размер может быть меньше, чем размер блока памяти, выделенного для данных. Вызовите функцию Win32 [глобалсизе](/windows/win32/api/winbase/nf-winbase-globalsize) , чтобы получить выделенный размер.

## <a name="clongbinarym_hdata"></a><a name="m_hdata"></a> CLongBinary:: m_hData

Сохраняет обработчик ХГЛОБАЛ Windows для фактических данных больших двоичных объектов.

```
HGLOBAL m_hData;
```

## <a name="see-also"></a>См. также раздел

[CObject, класс](../../mfc/reference/cobject-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Класс CRecordset](../../mfc/reference/crecordset-class.md)
