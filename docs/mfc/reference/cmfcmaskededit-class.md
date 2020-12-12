---
description: 'Дополнительные сведения о: У функции CMFCMaskedEdit Class'
title: Класс У функции CMFCMaskedEdit
ms.date: 11/04/2016
f1_keywords:
- CMFCMaskedEdit
- AFXMASKEDEDIT/CMFCMaskedEdit
- AFXMASKEDEDIT/CMFCMaskedEdit::DisableMask
- AFXMASKEDEDIT/CMFCMaskedEdit::EnableGetMaskedCharsOnly
- AFXMASKEDEDIT/CMFCMaskedEdit::EnableMask
- AFXMASKEDEDIT/CMFCMaskedEdit::EnableSelectByGroup
- AFXMASKEDEDIT/CMFCMaskedEdit::EnableSetMaskedCharsOnly
- AFXMASKEDEDIT/CMFCMaskedEdit::GetWindowText
- AFXMASKEDEDIT/CMFCMaskedEdit::SetValidChars
- AFXMASKEDEDIT/CMFCMaskedEdit::SetWindowText
- AFXMASKEDEDIT/CMFCMaskedEdit::IsMaskedChar
helpviewer_keywords:
- CMFCMaskedEdit [MFC], DisableMask
- CMFCMaskedEdit [MFC], EnableGetMaskedCharsOnly
- CMFCMaskedEdit [MFC], EnableMask
- CMFCMaskedEdit [MFC], EnableSelectByGroup
- CMFCMaskedEdit [MFC], EnableSetMaskedCharsOnly
- CMFCMaskedEdit [MFC], GetWindowText
- CMFCMaskedEdit [MFC], SetValidChars
- CMFCMaskedEdit [MFC], SetWindowText
- CMFCMaskedEdit [MFC], IsMaskedChar
ms.assetid: 13b1a645-2d5d-4c37-8599-16d5003f23a5
ms.openlocfilehash: 7ac61240e2941eafbbac3cbb03a4884e282cbca3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97265159"
---
# <a name="cmfcmaskededit-class"></a>Класс У функции CMFCMaskedEdit

`CMFCMaskedEdit`Класс поддерживает элемент управления "поле с маской", который проверяет вводимые пользователем данные на наличие маски и отображает проверенные результаты в соответствии с шаблоном.

## <a name="syntax"></a>Синтаксис

```
class CMFCMaskedEdit : public CEdit
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|`CMFCMaskedEdit::CMFCMaskedEdit`|Конструктор по умолчанию.|
|`CMFCMaskedEdit::~CMFCMaskedEdit`|Деструктор.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[У функции CMFCMaskedEdit::D Исаблемаск](#disablemask)|Отключает проверку вводимых пользователем данных.|
|[У функции CMFCMaskedEdit:: Енаблежетмаскедчарсонли](#enablegetmaskedcharsonly)|Указывает, `GetWindowText` извлекает ли метод только маскированные символы.|
|[У функции CMFCMaskedEdit:: Енаблемаск](#enablemask)|Инициализирует элемент управления "поле с маской".|
|[У функции CMFCMaskedEdit:: Енаблеселектбиграуп](#enableselectbygroup)|Указывает, будет ли элемент управления "поле с маской" выбирать определенные группы вводимых пользователем данных или все вводимые пользователем данные.|
|[У функции CMFCMaskedEdit:: Енаблесетмаскедчарсонли](#enablesetmaskedcharsonly)|Указывает, проверяется ли текст на соответствие только маскированным символам или к целой маске.|
|`CMFCMaskedEdit::GetThisClass`|Используется платформой для получения указателя на объект [крунтимекласс](../../mfc/reference/cruntimeclass-structure.md) , связанный с этим типом класса.|
|[У функции CMFCMaskedEdit:: Жетвиндовтекст](#getwindowtext)|Извлекает проверенный текст из элемента управления "поле с маской".|
|[У функции CMFCMaskedEdit:: Сетвалидчарс](#setvalidchars)|Указывает строку допустимых символов, которые может ввести пользователь.|
|[У функции CMFCMaskedEdit:: SetWindowText](#setwindowtext)|Отображает запрос в элементе управления "поле с маской".|

### <a name="protected-methods"></a>Защищенные методы

|Имя|Описание|
|----------|-----------------|
|[У функции CMFCMaskedEdit:: Исмаскедчар](#ismaskedchar)|Вызывается платформой для проверки указанного символа на соответствие соответствующему символу маски.|

## <a name="remarks"></a>Комментарии

Чтобы использовать `CMFCMaskedEdit` элемент управления в приложении, выполните следующие действия.

1. Внедрите `CMFCMaskedEdit` объект в класс Window.

2. Вызовите метод [у функции CMFCMaskedEdit:: енаблемаск](#enablemask) , чтобы указать маску.

3. Вызовите метод [у функции CMFCMaskedEdit:: сетвалидчарс](#setvalidchars) , чтобы указать список допустимых символов.

4. Вызовите метод [у функции CMFCMaskedEdit:: SetWindowText](#setwindowtext) , чтобы указать текст по умолчанию для элемента управления "поле с маской".

5. Вызовите метод [у функции CMFCMaskedEdit:: жетвиндовтекст](#getwindowtext) , чтобы получить проверенный текст.

Если не вызвать один или несколько методов для инициализации маски, допустимых символов и текста по умолчанию, элемент управления "поле редактирования" ведет себя так же, как и стандартный элемент управления "поле ввода".

## <a name="example"></a>Пример

В следующем примере показано, как настроить маску (например, номер телефона) с помощью `EnableMask` метода, чтобы создать маску для элемента управления "поле с маской", `SetValidChars` метод для указания строки допустимых символов, которые пользователь может ввести, и `SetWindowText` метод для отображения запроса в элементе управления "поле маскирования". Этот пример является частью [примера новых элементов управления](../../overview/visual-cpp-samples.md).

[!code-cpp[NVC_MFC_NewControls#11](../../mfc/reference/codesnippet/cpp/cmfcmaskededit-class_1.h)]
[!code-cpp[NVC_MFC_NewControls#12](../../mfc/reference/codesnippet/cpp/cmfcmaskededit-class_2.cpp)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CEdit](../../mfc/reference/cedit-class.md)

[CMFCMaskedEdit](../../mfc/reference/cmfcmaskededit-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксмаскедедит. h

## <a name="cmfcmaskededitdisablemask"></a><a name="disablemask"></a> У функции CMFCMaskedEdit::D Исаблемаск

Отключает проверку вводимых пользователем данных.

```cpp
void DisableMask();
```

### <a name="remarks"></a>Комментарии

Если проверка вводимых пользователем данных отключена, элемент управления маскированием редактирования ведет себя как стандартный элемент управления "поле ввода".

## <a name="cmfcmaskededitenablegetmaskedcharsonly"></a><a name="enablegetmaskedcharsonly"></a> У функции CMFCMaskedEdit:: Енаблежетмаскедчарсонли

Указывает, `GetWindowText` извлекает ли метод только маскированные символы.

```cpp
void EnableGetMaskedCharsOnly(BOOL bEnable=TRUE);
```

### <a name="parameters"></a>Параметры

*bEnable*<br/>
окне Значение TRUE, чтобы указать, что метод [у функции CMFCMaskedEdit:: жетвиндовтекст](#getwindowtext) извлекает только маскированные символы; Значение FALSE, чтобы указать, что метод получает весь текст. Значение по умолчанию — TRUE.

### <a name="remarks"></a>Комментарии

Используйте этот метод, чтобы разрешить получение маскированных символов. Затем создайте элемент управления "поле с маской", соответствующий номеру телефона, например (425) 555-0187. При вызове `GetWindowText` метода возвращается значение «4255550187». Если отключить извлечение маскированных символов, `GetWindowText` метод возвращает текст, отображаемый в элементе управления "поле ввода", например "(425) 555-0187".

## <a name="cmfcmaskededitenablemask"></a><a name="enablemask"></a> У функции CMFCMaskedEdit:: Енаблемаск

Инициализирует элемент управления "поле с маской".

```cpp
void EnableMask(
    LPCTSTR lpszMask,
    LPCTSTR lpszInputTemplate,
    TCHAR chMaskInputTemplate=_T('_'),
    LPCTSTR lpszValid=NULL);
```

### <a name="parameters"></a>Параметры

*лпсзмаск*<br/>
окне Строка маски, указывающая тип символа, который может отображаться в каждой позиции входных данных пользователя. Длина строк параметров *лпсзинпуттемплате* и *лпсзмаск* должна быть одинаковой. Дополнительные сведения о символах маски см. в разделе "Примечания".

*лпсзинпуттемплате*<br/>
окне Строка шаблона маски, указывающая литеральные символы, которые могут присутствовать в каждой позиции входных данных пользователя. Используйте символ подчеркивания ("_") в качестве заполнителя символа. Длина строк параметров *лпсзинпуттемплате* и *лпсзмаск* должна быть одинаковой.

*чмаскинпуттемплате*<br/>
окне Символ по умолчанию, который платформа заменяет для каждого недопустимого символа в введенных пользователем данных. По умолчанию этот параметр имеет значение подчеркивания ("_").

*лпсзвалид*<br/>
окне Строка, содержащая набор допустимых символов. Значение NULL указывает, что все символы являются допустимыми. Значение этого параметра по умолчанию равно NULL.

### <a name="remarks"></a>Комментарии

Используйте этот метод, чтобы создать маску для элемента управления "поле с маской". Создайте класс, производный от `CMFCMaskedEdit` класса, и переопределите метод [у функции CMFCMaskedEdit:: исмаскедчар](#ismaskedchar) , чтобы использовать собственный код для обработки пользовательской маски.

В следующей таблице перечислены символы маски по умолчанию.

|Символ маски|Определение|
|--------------------|----------------|
|D|Число.|
|d|Цифра или пробел.|
|+|Плюс (' + '), минус ('-') или пробел.|
|C|Алфавитный символ.|
|с|Буквенный символ или пробел.|
|Объект|Буквенно-цифровой символ.|
|а|Буквенно-цифровой символ или пробел.|
|*|Печатный символ.|

## <a name="cmfcmaskededitenableselectbygroup"></a><a name="enableselectbygroup"></a> У функции CMFCMaskedEdit:: Енаблеселектбиграуп

Указывает, разрешает ли элемент управления "поле редактирования" возможность выбора определенных групп или всех входных данных.

```cpp
void EnableSelectByGroup(BOOL bEnable=TRUE);
```

### <a name="parameters"></a>Параметры

*bEnable*<br/>
окне Значение TRUE, чтобы выбрать только группы; Значение FALSE, чтобы выделить весь текст. Значение по умолчанию — TRUE.

### <a name="remarks"></a>Комментарии

Используйте эту функцию, чтобы указать, позволяет ли элемент управления "поле с маской" выбирать пользователя по группе или всему тексту.

По умолчанию выбор по группам включен. В этом случае пользователь может выбрать только непрерывные группы допустимых символов.

Например, для проверки номера телефона можно использовать следующий элемент управления маскированного редактирования:

```cpp
m_wndMaskEdit.EnableMask(
    _T(" ddd  ddd dddd"),  // Mask string
    _T("(___) ___-____"),  // Template string
    _T(' '));              // Default char

m_wndMaskEdit.SetValidChars(NULL); // All characters are valid.

m_wndMaskEdit.SetWindowText(_T("(425) 555-0187")); // Prompt
```

Если выбор по группе включен, пользователь может получить только группы строк "425", "555" или "0187". Если выбор группы отключен, пользователь может получить весь текст номера телефона: "(425) 555-0187".

## <a name="cmfcmaskededitenablesetmaskedcharsonly"></a><a name="enablesetmaskedcharsonly"></a> У функции CMFCMaskedEdit:: Енаблесетмаскедчарсонли

Указывает, проверяется ли текст на соответствие только маскированным символам или к целой маске.

```cpp
void EnableSetMaskedCharsOnly(BOOL bEnable=TRUE);
```

### <a name="parameters"></a>Параметры

*bEnable*<br/>
окне Значение TRUE, чтобы проверить введенные пользователем данные только по маскированным символам; Значение FALSE для проверки по всей маске. Значение по умолчанию — TRUE.

## <a name="cmfcmaskededitgetwindowtext"></a><a name="getwindowtext"></a> У функции CMFCMaskedEdit:: Жетвиндовтекст

Извлекает проверенный текст из элемента управления "поле с маской".

```
int GetWindowText(
    LPTSTR lpszStringBuf,
    int nMaxCount) const;

void GetWindowText(CString& rstrString) const;
```

### <a name="parameters"></a>Параметры

*лпсзстрингбуф*<br/>
заполняет Указатель на буфер, который получает текст из элемента управления "поле ввода".

*нмакскаунт*<br/>
окне Максимальное число получаемых символов.

*рстрстринг*<br/>
заполняет Ссылка на объект String, который получает текст из элемента управления "поле ввода".

### <a name="return-value"></a>Возвращаемое значение

Перегрузка первого метода возвращает число байтов строки, копируемой в буфер параметров *лпсзстрингбуф* . 0, если элемент управления "поле с маской" не имеет текста.

### <a name="remarks"></a>Комментарии

Этот метод копирует текст из элемента управления "поле с маской" в буфер *лпсзстрингбуф* или в строку *рстрстринг* .

Этот метод переопределяет [CWnd:: жетвиндовтекст](../../mfc/reference/cwnd-class.md#getwindowtext).

## <a name="cmfcmaskededitismaskedchar"></a><a name="ismaskedchar"></a> У функции CMFCMaskedEdit:: Исмаскедчар

Вызывается платформой для проверки указанного символа на соответствие соответствующему символу маски.

```
virtual BOOL IsMaskedChar(
    TCHAR chChar,
    TCHAR chMaskChar) const;
```

### <a name="parameters"></a>Параметры

*ччар*<br/>
окне Проверяемый символ.

*чмаскчар*<br/>
окне Соответствующий символ из строки маски.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если параметр *ччар* является типом символа, разрешенного параметром *чмаскчар* . в противном случае — значение FALSE.

### <a name="remarks"></a>Комментарии

Переопределите этот метод для самостоятельной проверки вводимых символов. Дополнительные сведения о символах маски см. в описании метода [у функции CMFCMaskedEdit:: енаблемаск](#enablemask) .

## <a name="cmfcmaskededitsetvalidchars"></a><a name="setvalidchars"></a> У функции CMFCMaskedEdit:: Сетвалидчарс

Указывает строку допустимых символов, которые может ввести пользователь.

```cpp
void SetValidChars(LPCTSTR lpszValid=NULL);
```

### <a name="parameters"></a>Параметры

*лпсзвалид*<br/>
окне Строка, содержащая набор допустимых входных символов. Значение NULL означает, что все символы являются допустимыми. Значение этого параметра по умолчанию равно NULL.

### <a name="remarks"></a>Комментарии

Используйте этот метод, чтобы определить список допустимых символов. Если входной символ отсутствует в этом списке, он не будет принимать маскированный элемент управления Editing.

В следующем примере кода принимаются только шестнадцатеричные числа.

```cpp
//Mask: 0xFFFF
m_wndMaskEdit.EnableMask(
    _T(" AAAA"),                // The mask string.
    _T("0x____"),               // The literal template string.
    _T('_'));                   // The default character that
                                // replaces the backspace character.
// Valid string characters
m_wndMaskEdit.SetValidChars(_T("1234567890ABCDEFabcdef"));m_wndMaskEdit.SetWindowText(_T("0x01AF"));
```

## <a name="cmfcmaskededitsetwindowtext"></a><a name="setwindowtext"></a> У функции CMFCMaskedEdit:: SetWindowText

Отображает запрос в элементе управления "поле с маской".

```cpp
void SetWindowText(LPCTSTR lpszString);
```

### <a name="parameters"></a>Параметры

*лпсзстринг*<br/>
окне Указывает на строку, завершающуюся нулем, которая будет использоваться в качестве подсказки.

### <a name="remarks"></a>Комментарии

Этот метод задает текст элемента управления.

Этот метод переопределяет [CWnd:: SetWindowText](../../mfc/reference/cwnd-class.md#setwindowtext).

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс CEdit](../../mfc/reference/cedit-class.md)
