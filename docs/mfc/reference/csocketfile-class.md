---
description: 'Дополнительные сведения о: CSocketFile Class'
title: Класс CSocketFile
ms.date: 11/04/2016
f1_keywords:
- CSocketFile
- AFXSOCK/CSocketFile
- AFXSOCK/CSocketFile::CSocketFile
helpviewer_keywords:
- CSocketFile [MFC], CSocketFile
ms.assetid: 7924c098-5f72-40d6-989d-42800a47958f
ms.openlocfilehash: 4ca484545e11502a11acf5f27b00ee2df49fc9d6
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97318654"
---
# <a name="csocketfile-class"></a>Класс CSocketFile

Объект `CFile` , используемый для отправки и получения сведений по сети с помощью Windows Sockets.

## <a name="syntax"></a>Синтаксис

```
class CSocketFile : public CFile
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CSocketFile:: CSocketFile](#csocketfile)|Формирует объект `CSocketFile`.|

## <a name="remarks"></a>Комментарии

`CSocketFile`Для этой цели можно присоединить объект к `CSocket` объекту. Вы также можете и обычно присоединить `CSocketFile` объект к `CArchive` объекту, чтобы упростить отправку и получение данных с помощью сериализации MFC.

Для сериализации (отправки) данных необходимо вставить их в архив, который вызывает функции- `CSocketFile` члены для записи данных в `CSocket` объект. Чтобы десериализовать (получить) данные, извлеките их из архива. Это приводит к тому, что Архив вызывает `CSocketFile` функции членов для считывания данных из `CSocket` объекта.

> [!TIP]
> Помимо использования, `CSocketFile` как описано здесь, его можно использовать как отдельный файловый объект, как и в `CFile` случае с базовым классом. Можно также использовать `CSocketFile` с любыми функциями СЕРИАЛИЗАЦИИ MFC на основе архива. Поскольку не `CSocketFile` поддерживает все `CFile` функции, некоторые функции сериализации MFC по умолчанию несовместимы с `CSocketFile` . Это особенно справедливо для `CEditView` класса. Не пытайтесь сериализовать `CEditView` данные через `CArchive` объект, присоединенный к `CSocketFile` объекту с помощью `CEditView::SerializeRaw` ; `CEditView::Serialize` вместо этого используйте. `SerializeRaw`Функция ждет, что объект File имеет функции, такие как, у `Seek` которых `CSocketFile` нет.

При использовании `CArchive` с `CSocketFile` и `CSocket` может возникнуть ситуация, когда `CSocket::Receive` вводит цикл (by `PumpMessages(FD_READ)` ) в ожидании запрошенного объема байтов. Это обусловлено тем, что сокеты Windows допускают только один вызов recv per FD_READ уведомления, но `CSocketFile` и `CSocket` разрешают несколько вызовов recv per FD_READ. Если при отсутствии данных для чтения появляется FD_READ, приложение зависает. Если вы никогда не получаете другой FD_READ, приложение перестает взаимодействовать через сокет.

Эту проблему можно устранить следующим образом. В `OnReceive` методе класса Socket вызовите `CAsyncSocket::IOCtl(FIONREAD, ...)` метод перед вызовом `Serialize` метода класса сообщений, когда ожидаемые данные, считываемые из сокета, превышают размер одного пакета TCP (максимальная единица передачи, обычно по крайней мере 1096 байт). Если размер доступных данных меньше, чем требуется, дождитесь получения всех данных и запустите операцию чтения только после этого.

В следующем примере `m_dwExpected` — это приблизительное число байтов, которое должен получить пользователь. Предполагается, что вы объявили его в любом расположении в коде.

[!code-cpp[NVC_MFCSocketThread#4](../../mfc/reference/codesnippet/cpp/csocketfile-class_1.cpp)]

Дополнительные сведения см. в статьях [сокеты Windows в MFC](../../mfc/windows-sockets-in-mfc.md), [сокеты Windows: Использование сокетов с архивами](../../mfc/windows-sockets-using-sockets-with-archives.md), а также [API Windows Sockets 2](/windows/win32/WinSock/windows-sockets-start-page-2).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CFile](../../mfc/reference/cfile-class.md)

`CSocketFile`

## <a name="requirements"></a>Требования

**Заголовок:** афкссокк. h

## <a name="csocketfilecsocketfile"></a><a name="csocketfile"></a> CSocketFile:: CSocketFile

Формирует объект `CSocketFile`.

```
explicit CSocketFile(
    CSocket* pSocket,
    BOOL bArchiveCompatible = TRUE);
```

### <a name="parameters"></a>Параметры

*псоккет*<br/>
Сокет для присоединения к `CSocketFile` объекту.

*барчивекомпатибле*<br/>
Указывает, предназначен ли файловый объект для использования с `CArchive` объектом. Значение FALSE следует передавать только в том случае, если вы хотите использовать `CSocketFile` объект изолированно, как и изолированный `CFile` объект, с определенными ограничениями. Этот флаг изменяет способ, `CArchive` которым объект, присоединенный к `CSocketFile` объекту, управляет его буфером для чтения.

### <a name="remarks"></a>Комментарии

Деструктор объекта отменяет связь с объектом Socket, когда объект выходит из области действия или удаляется.

> [!NOTE]
> `CSocketFile`Также можно использовать в качестве файла (с ограниченным доступом) без `CArchive` объекта. По умолчанию `CSocketFile` параметр *барчивекомпатибле* конструктора имеет значение true. Указывает, что файловый объект предназначен для использования с архивом. Чтобы использовать объект File без архива, передайте значение FALSE в параметре *барчивекомпатибле* .

В режиме «архивный» `CSocketFile` объект обеспечивает лучшую производительность и снижает опасность «взаимоблокировки». Взаимоблокировка возникает, когда оба приема сокетов ожидают друг друга или для общего ресурса. Такая ситуация может возникнуть, если `CArchive` объект работал так же, `CSocketFile` как и `CFile` объект. С помощью `CFile` архива можно предположить, что при получении меньшего количества байтов, чем запрошено, достигнут конец файла.

`CSocketFile`Тем не менее, данные основаны на сообщениях; буфер может содержать несколько сообщений, поэтому получение меньшего числа запрошенных байтов не подразумевает конца файла. Приложение не блокируется в этом случае, как это возможно `CFile` , и может продолжать чтение сообщений из буфера до тех пор, пока буфер не будет пустым. Функция [CArchive:: исбуфферемпти](../../mfc/reference/carchive-class.md#isbufferempty) полезна для наблюдения за состоянием буфера архива в таком случае.

Дополнительные сведения об использовании см `CSocketFile` . в статьях [сокеты Windows: Использование сокетов с архивами](../../mfc/windows-sockets-using-sockets-with-archives.md) и [сокетами Windows. Пример использования сокетов с архивами](../../mfc/windows-sockets-example-of-sockets-using-archives.md).

## <a name="see-also"></a>См. также раздел

[Класс Кфиле](../../mfc/reference/cfile-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Класс CAsyncSocket](../../mfc/reference/casyncsocket-class.md)<br/>
[Класс CSocket](../../mfc/reference/csocket-class.md)
