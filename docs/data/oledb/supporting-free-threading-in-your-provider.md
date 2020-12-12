---
description: Дополнительные сведения о поддержке свободных потоков в поставщике
title: Поддержка свободной потоковой модели в поставщике
ms.date: 11/04/2016
helpviewer_keywords:
- OLE DB providers, multithreaded
- threading [C++], providers
ms.assetid: a91270dc-cdf9-4855-88e7-88a54be7cbe8
ms.openlocfilehash: 4f6785dd85ae043ce0ee74c1dda4fa365c566729
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97286479"
---
# <a name="supporting-free-threading-in-your-provider"></a>Поддержка свободной потоковой модели в поставщике

Все классы поставщиков OLE DB являются потокобезопасными, а записи реестра задаются соответствующим образом. Рекомендуется поддерживать бесплатные потоки, чтобы обеспечить высокий уровень производительности в многопользовательской ситуации. Чтобы обеспечить потокобезопасность поставщика, необходимо убедиться в том, что код заблокирован правильно. Каждый раз при записи или хранении данных необходимо заблокировать доступ с критически важными разделами.

Каждый объект шаблона поставщика OLE DB имеет свой собственный критический раздел. Чтобы упростить блокировку, каждый новый создаваемый класс должен быть классом шаблона, принимающим имя родительского класса в качестве аргумента.

В следующем примере показано, как заблокировать код:

```cpp
template <class T>
class CMyObject<T> : public...

HRESULT MyObject::MyMethod(void)
{
   T* pT = (T*)this;      // this gets the parent class

// You don't need to do anything if you are only reading information

// If you want to write information, do the following:
   pT->Lock();         // engages critical section in the object
   ...;                // write whatever information you wish
   pT->Unlock();       // disengages the critical section
}
```

Дополнительные сведения о защите критических разделов с помощью `Lock` и `Unlock` см. в разделе [многопоточность. Использование классов синхронизации](../../parallel/multithreading-how-to-use-the-synchronization-classes.md).

Убедитесь, что переопределяемые методы (например, `Execute` ) являются потокобезопасными.

## <a name="see-also"></a>См. также раздел

[Работа с шаблонами поставщика OLE DB](../../data/oledb/working-with-ole-db-provider-templates.md)
