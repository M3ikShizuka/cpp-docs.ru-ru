---
description: 'Дополнительные сведения о: интерфейс ICommandTarget'
title: Интерфейс ICommandTarget
ms.date: 11/04/2016
f1_keywords:
- ICommandTarget
- AFXWINFORMS/ICommandTarget
- AFXWINFORMS/ICommandTarget::Initialize
helpviewer_keywords:
- ICommandTarget interface [MFC]
ms.assetid: dd9927f6-3479-4e7c-8ef9-13206cf901f3
ms.openlocfilehash: 6deb11ecca94160ea19225fb955826845a4cdefa
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97219581"
---
# <a name="icommandtarget-interface"></a>Интерфейс ICommandTarget

Предоставляет пользовательский элемент управления с интерфейсом для получения команд из исходного объекта команды.

## <a name="syntax"></a>Синтаксис

```
interface class ICommandTarget
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[ICommandTarget:: Initialize](#initialize)|Инициализирует целевой объект команды.|

## <a name="remarks"></a>Комментарии

При размещении пользовательского элемента управления в представлении MFC [квинформсвиев](../../mfc/reference/cwinformsview-class.md) направляет команды и обновляет сообщения пользовательского интерфейса команды на пользовательский элемент управления, чтобы разрешить обработку команд MFC (например, элементы меню "фрейм" и кнопки панели инструментов). Реализуя `ICommandTarget` , вы предоставляете пользовательскому элементу управления ссылку на объект [ICommandSource](../../mfc/reference/icommandsource-interface.md) .

См. раздел [как добавить маршрутизацию команд в элемент управления Windows Forms,](../../dotnet/how-to-add-command-routing-to-the-windows-forms-control.md) чтобы получить пример использования `ICommandTarget` .

Дополнительные сведения об использовании Windows Forms см. в разделе [Использование пользовательского элемента управления формы Windows в MFC](../../dotnet/using-a-windows-form-user-control-in-mfc.md).

## <a name="requirements"></a>Требования

**Заголовок:** афксвинформс. h (определяется в atlmfc\lib\mfcmifc80.dll сборки)

## <a name="icommandtargetinitialize"></a><a name="initialize"></a> ICommandTarget:: Initialize

Инициализирует целевой объект команды.

```cpp
void Initialize(ICommandSource^ cmdSource);
```

### <a name="parameters"></a>Параметры

*кмдсаурце*<br/>
Маркер для исходного объекта команды.

### <a name="remarks"></a>Комментарии

При размещении пользовательского элемента управления в представлении MFC Квинформсвиев направляет команды и обновляет сообщения пользовательского интерфейса команды в пользовательский элемент управления, чтобы разрешить обработку команд MFC.

Этот метод инициализирует целевой объект команды и связывает его с указанным исходным объектом команды Кмдсаурце. Он должен вызываться в реализации класса пользовательского элемента управления. При инициализации необходимо зарегистрировать обработчики команд в объекте источника команды, вызвав ICommandSource:: Аддкоммандхандлер в реализации инициализации. См. раздел как добавить маршрутизацию команд в элемент управления Windows Forms, чтобы получить пример использования инструкции Initialize для выполнения этого действия.

## <a name="see-also"></a>См. также раздел

[Как добавить маршрутизацию команд в элемент управления Windows Forms](../../dotnet/how-to-add-command-routing-to-the-windows-forms-control.md)<br/>
[Интерфейс ICommandSource](../../mfc/reference/icommandsource-interface.md)
