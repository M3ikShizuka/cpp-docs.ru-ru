---
description: 'Дополнительные сведения о: Ккритикалсектион Class'
title: Класс Ккритикалсектион
ms.date: 11/04/2016
f1_keywords:
- CCriticalSection
- AFXMT/CCriticalSection
- AFXMT/CCriticalSection::CCriticalSection
- AFXMT/CCriticalSection::Lock
- AFXMT/CCriticalSection::Unlock
- AFXMT/CCriticalSection::m_sect
helpviewer_keywords:
- CCriticalSection [MFC], CCriticalSection
- CCriticalSection [MFC], Lock
- CCriticalSection [MFC], Unlock
- CCriticalSection [MFC], m_sect
ms.assetid: f776f74b-5b0b-4f32-9c13-2b8e4a0d7b2b
ms.openlocfilehash: 0041eea4453ec02159b26805bd5e7a264a410504
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97227797"
---
# <a name="ccriticalsection-class"></a>Класс Ккритикалсектион

Представляет "критическую секцию" — объект синхронизации, который позволяет одному потоку за раз обращаться к ресурсу или разделу кода.

## <a name="syntax"></a>Синтаксис

```
class CCriticalSection : public CSyncObject
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Ккритикалсектион:: Ккритикалсектион](#ccriticalsection)|Формирует объект `CCriticalSection`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ккритикалсектион:: Lock](#lock)|Используйте для получения доступа к `CCriticalSection` объекту.|
|[Ккритикалсектион:: Unlock](#unlock)|Освобождает объект `CCriticalSection`.|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[Ккритикалсектион:: operator CRITICAL_SECTION *](#operator_critical_section_star)|Извлекает указатель на внутренний объект CRITICAL_SECTION.|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[Ккритикалсектион:: m_sect](#m_sect)|Объект CRITICAL_SECTION.|

## <a name="remarks"></a>Комментарии

Критические разделы полезны, когда только одному потоку за раз можно разрешить изменять данные или другие контролируемые ресурсы. Например, Добавление узлов в связанный список — это процесс, который должен быть разрешен только одним потоком за раз. При использовании `CCriticalSection` объекта для управления связанным списком только один поток за раз может получить доступ к списку.

> [!NOTE]
> Функциональные возможности `CCriticalSection` класса предоставляются фактическим объектом Win32 CRITICAL_SECTION.

Критические разделы используются вместо мьютексов (см. [кмутекс](../../mfc/reference/cmutex-class.md)), когда скорость очень важна и ресурс не будет использоваться в границах процессов.

Существует два метода использования `CCriticalSection` объекта: изолированный и встроенный в класс.

- Изолированный метод для использования изолированного `CCriticalSection` объекта конструирует `CCriticalSection` объект при необходимости. После успешного возврата из конструктора явно заблокируйте объект с помощью вызова [Lock](#lock). [Разблокируйте](#unlock) вызов по завершении доступа к критическому разделу. Этот метод, хотя очевидно, что кто-то читает исходный код, более подвержен ошибке, так как необходимо забывать о блокировке и разблокировании критической секции до и после доступа.

   Более предпочтительным методом является использование класса [ксинглелокк](../../mfc/reference/csinglelock-class.md) . Он также имеет `Lock` метод и `Unlock` , но вам не нужно беспокоиться о разблокировке ресурса в случае возникновения исключения.

- Внедренный метод можно также предоставить общий доступ к классу с несколькими потоками, добавив в `CCriticalSection` класс член данных-Type и заблокируя элемент данных при необходимости.

Дополнительные сведения об использовании `CCriticalSection` объектов см. в статье [многопоточность. Использование классов синхронизации](../../parallel/multithreading-how-to-use-the-synchronization-classes.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CSyncObject](../../mfc/reference/csyncobject-class.md)

`CCriticalSection`

## <a name="requirements"></a>Требования

**Заголовок:** афксмт. h

## <a name="ccriticalsectionccriticalsection"></a><a name="ccriticalsection"></a> Ккритикалсектион:: Ккритикалсектион

Формирует объект `CCriticalSection`.

```
CCriticalSection();
```

### <a name="remarks"></a>Комментарии

Чтобы получить доступ к объекту или освободить `CCriticalSection` его, создайте объект [ксинглелокк](../../mfc/reference/csinglelock-class.md) и вызовите его функции-члены [Lock](../../mfc/reference/csinglelock-class.md#lock) и [Unlock](../../mfc/reference/csinglelock-class.md#unlock) . Если `CCriticalSection` объект используется изолированно, вызовите его функцию-член [Unlock](#unlock) , чтобы освободить ее.

Если конструктору не удается выделить требуемую системную память, автоматически создается исключение памяти (типа [CMemoryException](../../mfc/reference/cmemoryexception-class.md)).

### <a name="example"></a>Пример

  См. пример для [ккритикалсектион:: Lock](#lock).

## <a name="ccriticalsectionlock"></a><a name="lock"></a> Ккритикалсектион:: Lock

Вызовите эту функцию члена, чтобы получить доступ к объекту критической секции.

```
BOOL Lock();
BOOL Lock(DWORD dwTimeout);
```

### <a name="parameters"></a>Параметры

*двтимеаут*<br/>
`Lock` игнорирует значение этого параметра.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если функция выполнена успешно; в противном случае — 0.

### <a name="remarks"></a>Комментарии

`Lock` — Это блокирующий вызов, который не будет возвращаться до получения сигнала объектом критического раздела (становится доступным).

Если требуется время ожидания, можно использовать объект [кмутекс](../../mfc/reference/cmutex-class.md) вместо `CCriticalSection` объекта.

Если `Lock` не удается выделить необходимую системную память, автоматически создается исключение памяти (типа [CMemoryException](../../mfc/reference/cmemoryexception-class.md)).

### <a name="example"></a>Пример

В этом примере показан подход к вложенному критическому разделу путем управления доступом к общему ресурсу (статическому `_strShared` объекту) с помощью общего `CCriticalSection` объекта. `SomeMethod`Функция демонстрирует надежный способ обновления общего ресурса.

[!code-cpp[NVC_MFC_Utilities#11](../../mfc/codesnippet/cpp/ccriticalsection-class_1.h)]

## <a name="ccriticalsectionm_sect"></a><a name="m_sect"></a> Ккритикалсектион:: m_sect

Содержит объект критической секции, используемый всеми `CCriticalSection` методами.

```
CRITICAL_SECTION m_sect;
```

## <a name="ccriticalsectionoperator-critical_section"></a><a name="operator_critical_section_star"></a> Ккритикалсектион:: operator CRITICAL_SECTION *

Извлекает объект CRITICAL_SECTION.

```
operator CRITICAL_SECTION*();
```

### <a name="remarks"></a>Комментарии

Вызовите эту функцию, чтобы получить указатель на внутренний объект CRITICAL_SECTION.

## <a name="ccriticalsectionunlock"></a><a name="unlock"></a> Ккритикалсектион:: Unlock

Освобождает `CCriticalSection` объект для использования другим потоком.

```
BOOL Unlock();
```

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если `CCriticalSection` объект был владельцем потока, и выпуск был успешным; в противном случае — 0.

### <a name="remarks"></a>Комментарии

Если `CCriticalSection` используется изолированный метод, он `Unlock` должен вызываться сразу после завершения использования ресурса, управляемого критическим разделом. Если используется объект [ксинглелокк](../../mfc/reference/csinglelock-class.md) , `CCriticalSection::Unlock` он будет вызываться `Unlock` функцией-членом объекта Lock.

### <a name="example"></a>Пример

  См. пример для [ккритикалсектион:: Lock](#lock).

## <a name="see-also"></a>См. также раздел

[Класс Ксинкобжект](../../mfc/reference/csyncobject-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Класс Кмутекс](../../mfc/reference/cmutex-class.md)
