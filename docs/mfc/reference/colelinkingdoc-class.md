---
description: 'Дополнительные сведения о: Колелинкингдок Class'
title: Класс Колелинкингдок
ms.date: 11/04/2016
f1_keywords:
- COleLinkingDoc
- AFXOLE/COleLinkingDoc
- AFXOLE/COleLinkingDoc::COleLinkingDoc
- AFXOLE/COleLinkingDoc::Register
- AFXOLE/COleLinkingDoc::Revoke
- AFXOLE/COleLinkingDoc::OnFindEmbeddedItem
- AFXOLE/COleLinkingDoc::OnGetLinkedItem
helpviewer_keywords:
- COleLinkingDoc [MFC], COleLinkingDoc
- COleLinkingDoc [MFC], Register
- COleLinkingDoc [MFC], Revoke
- COleLinkingDoc [MFC], OnFindEmbeddedItem
- COleLinkingDoc [MFC], OnGetLinkedItem
ms.assetid: 9f547f35-2f95-427f-b9c0-85c31940198b
ms.openlocfilehash: 10cf9bb81c4cbbd324b95a13dc2fa44548266583
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97226913"
---
# <a name="colelinkingdoc-class"></a>Класс Колелинкингдок

Базовый класс для документов OLE-контейнера, которые поддерживают связывание со встроенными элементами, которые их содержат.

## <a name="syntax"></a>Синтаксис

```
class COleLinkingDoc : public COleDocument
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Колелинкингдок:: Колелинкингдок](#colelinkingdoc)|Формирует объект `COleLinkingDoc`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Колелинкингдок:: Register](#register)|Регистрирует документ в DLL-библиотеках системы OLE.|
|[Колелинкингдок:: REVOKE](#revoke)|Отменяет регистрацию документа.|

### <a name="protected-methods"></a>Защищенные методы

|Имя|Описание|
|----------|-----------------|
|[Колелинкингдок:: Онфиндембеддедитем](#onfindembeddeditem)|Находит указанный внедренный элемент.|
|[Колелинкингдок:: Онжетлинкедитем](#ongetlinkeditem)|Находит указанный связанный элемент.|

## <a name="remarks"></a>Комментарии

Приложение-контейнер, поддерживающее связывание с внедренными элементами, называется "контейнером ссылок". Пример приложения [OCLIENT](../../overview/visual-cpp-samples.md) является примером контейнера ссылок.

Если источником связанного элемента является внедренный элемент в другом документе, для редактирования внедренного элемента необходимо загрузить документ, содержащий его. По этой причине контейнер связи должен быть запущен другим приложением-контейнером, когда пользователь хочет изменить источник связанного элемента. Приложение также должно использовать класс [COleTemplateServer](../../mfc/reference/coletemplateserver-class.md) , чтобы он мог создавать документы при программном запуске.

Чтобы сделать контейнер контейнером ссылок, создайте класс документа, производный от, `COleLinkingDoc` вместо [коледокумент](../../mfc/reference/coledocument-class.md). Как и в случае с любым другим контейнером OLE, необходимо спроектировать класс для хранения собственных данных приложения, а также внедренных или связанных элементов. Кроме того, необходимо спроектировать структуры данных для хранения собственных данных. При определении `CDocItem` производного класса для собственных данных приложения можно использовать интерфейс, определенный `COleDocument` в, для хранения собственных данных, а также данных OLE.

Чтобы приложение было запущено программно другим контейнером, объявите `COleTemplateServer` объект как член класса, производного от приложения `CWinApp` :

[!code-cpp[NVC_MFCOleContainer#23](../../mfc/codesnippet/cpp/colelinkingdoc-class_1.h)]

В `InitInstance` функции-члене `CWinApp` производного класса создайте шаблон документа и укажите `COleLinkingDoc` класс, производный от класса Document:

[!code-cpp[NVC_MFCOleContainer#24](../../mfc/codesnippet/cpp/colelinkingdoc-class_2.cpp)]

Подключите `COleTemplateServer` объект к шаблонам документов, вызвав `ConnectTemplate` функцию члена объекта, и зарегистрируйте все объекты класса в системе OLE, вызвав `COleTemplateServer::RegisterAll` :

[!code-cpp[NVC_MFCOleContainer#25](../../mfc/codesnippet/cpp/colelinkingdoc-class_3.cpp)]

`CWinApp`Определение и функция класса, производного от образца `InitInstance` , см. в разделе OCLIENT. H и OCLIENT. CPP в образце [OCLIENT](../../overview/visual-cpp-samples.md)MFC.

Дополнительные сведения об использовании см `COleLinkingDoc` . в разделе [контейнеры статей: Реализация контейнера](../../mfc/containers-implementing-a-container.md) и [контейнеров: дополнительные возможности](../../mfc/containers-advanced-features.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CDocument](../../mfc/reference/cdocument-class.md)

[COleDocument](../../mfc/reference/coledocument-class.md)

`COleLinkingDoc`

## <a name="requirements"></a>Требования

**Заголовок:** афксоле. h

## <a name="colelinkingdoccolelinkingdoc"></a><a name="colelinkingdoc"></a> Колелинкингдок:: Колелинкингдок

Конструирует `COleLinkingDoc` объект без начала взаимодействия с системными библиотеками DLL OLE.

```
COleLinkingDoc();
```

### <a name="remarks"></a>Комментарии

`Register`Чтобы сообщить OLE о том, что документ открыт, необходимо вызвать функцию-член.

## <a name="colelinkingdoconfindembeddeditem"></a><a name="onfindembeddeditem"></a> Колелинкингдок:: Онфиндембеддедитем

Вызывается платформой для определения, содержит ли документ внедренный элемент OLE с указанным именем.

```
virtual COleClientItem* OnFindEmbeddedItem(LPCTSTR lpszItemName);
```

### <a name="parameters"></a>Параметры

*лпсзитемнаме*<br/>
Указатель на имя запрошенного внедренного элемента OLE.

### <a name="return-value"></a>Возвращаемое значение

Указатель на указанный элемент; Значение NULL, если элемент не найден.

### <a name="remarks"></a>Комментарии

Реализация по умолчанию выполняет поиск элемента с указанным именем в списке внедренных элементов (сравнение имен выполняется с учетом регистра). Переопределите эту функцию, если у вас есть собственный метод хранения или именования внедренных элементов OLE.

## <a name="colelinkingdocongetlinkeditem"></a><a name="ongetlinkeditem"></a> Колелинкингдок:: Онжетлинкедитем

Вызывается платформой для проверки, содержит ли документ связанный серверный элемент с указанным именем.

```
virtual COleServerItem* OnGetLinkedItem(LPCTSTR lpszItemName);
```

### <a name="parameters"></a>Параметры

*лпсзитемнаме*<br/>
Указатель на имя запрошенного связанного элемента OLE.

### <a name="return-value"></a>Возвращаемое значение

Указатель на указанный элемент; Значение NULL, если элемент не найден.

### <a name="remarks"></a>Комментарии

Реализация по умолчанию `COleLinkingDoc` всегда возвращает значение null. Эта функция переопределена в производном классе `COleServerDoc` для поиска связанного элемента в списке элементов OLE-сервера с указанным именем (сравнение имен выполняется с учетом регистра). Переопределите эту функцию, если реализуется собственный метод хранения или извлечения элементов связанного сервера.

## <a name="colelinkingdocregister"></a><a name="register"></a> Колелинкингдок:: Register

Информирует о наличии открытого документа библиотекой DLL системы OLE.

```
BOOL Register(
    COleObjectFactory* pFactory,
    LPCTSTR lpszPathName);
```

### <a name="parameters"></a>Параметры

*pFactory*<br/>
Указатель на объект фабрики OLE (может иметь значение NULL).

*лпсзпаснаме*<br/>
Указатель на полный путь к документу контейнера.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если документ успешно зарегистрирован; в противном случае — 0.

### <a name="remarks"></a>Комментарии

Эта функция вызывается при создании или открытии именованного файла для регистрации документа в библиотеках DLL системы OLE. Нет необходимости вызывать эту функцию, если документ представляет внедренный элемент.

При использовании `COleTemplateServer` в приложении `Register` вызывается для `COleLinkingDoc` реализации `OnNewDocument` , `OnOpenDocument` и `OnSaveDocument` .

## <a name="colelinkingdocrevoke"></a><a name="revoke"></a> Колелинкингдок:: REVOKE

Информирует системные библиотеки DLL OLE о том, что документ больше не открыт.

```cpp
void Revoke();
```

### <a name="remarks"></a>Комментарии

Эта функция вызывается для отмены регистрации документа с помощью системных библиотек OLE.

Эту функцию следует вызывать при закрытии именованного файла, но обычно вызывать его напрямую не требуется. `Revoke` вызывается для `COleLinkingDoc` реализации `OnCloseDocument` , `OnNewDocument` , `OnOpenDocument` и `OnSaveDocument` .

## <a name="see-also"></a>См. также раздел

[Пример OCLIENT MFC](../../overview/visual-cpp-samples.md)<br/>
[Класс Коледокумент](../../mfc/reference/coledocument-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Класс CDocTemplate](../../mfc/reference/cdoctemplate-class.md)
