---
description: Дополнительные сведения о параметре/SAFESEH (image содержит безопасного обработчика исключений).
title: Параметр /SAFESEH (образ содержит обработчики безопасных событий)
ms.date: 11/04/2016
f1_keywords:
- /SAFESEH
helpviewer_keywords:
- /SAFESEH linker option
- -SAFESEH linker option
- SAFESEH linker option
ms.assetid: 7722ff99-b833-4c65-a855-aaca902ffcb7
ms.openlocfilehash: 723b5503bca1d98d7df0c638df1dfc8101fc116f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97224989"
---
# <a name="safeseh-image-has-safe-exception-handlers"></a>Параметр /SAFESEH (образ содержит обработчики безопасных событий)

```
/SAFESEH[:NO]
```

Если указан параметр **/SAFESEH** , то компоновщик создает изображение только в том случае, если оно также может создать таблицу безнадежных обработчиков исключений образа. В этой таблице указывается операционная система, для которой обработчики исключений являются допустимыми для образа.

Параметр **/SAFESEH** допустим только при компоновке для целевых объектов x86. Параметр **/SAFESEH** не поддерживается для платформ, в которых уже есть указанные обработчики исключений. Например, в системах x64 и ARM все обработчики исключений отмечены в PDATA. ML64.exe поддерживает добавление заметок, которые выдают сведения о SEH (XDATA и PDATA) в образ, что позволяет очищать функции ml64. Дополнительные сведения см. в статье [MASM для x64 (ml64.exe)](../../assembler/masm/masm-for-x64-ml64-exe.md) .

Если параметр **/SAFESEH** не указан, компоновщик создаст образ с таблицей обработчиков безопасного исключения, если все модули совместимы с функцией обработки безопасного исключения. Если какие-либо модули несовместимы с функцией безопасного обработчика исключений, полученный образ не будет содержать таблицу безнадежных обработчиков исключений. Если параметр [/SUBSYSTEM](subsystem-specify-subsystem.md) задает WindowsCE или один из параметров EFI_ *, компоновщик не будет пытаться создать образ с таблицей безнадежных исключений, так как ни одна из этих подсистем не сможет использовать эту информацию.

Если параметр **/SAFESEH: No** не указан, компоновщик не будет создавать образ с таблицей безнадежных исключений, даже если все модули совместимы с функцией обработки безопасного исключения.

Наиболее распространенной причиной, по которой компоновщику не удается создать изображение, является то, что один или несколько входных файлов (модулей) компоновщика несовместимы с функцией безнадежных обработчиков исключений. Распространенной причиной, по которой модуль не совместим с безнадежными обработчиками исключений, является то, что он был создан с помощью компилятора из предыдущей версии Visual C++.

Функцию также можно зарегистрировать как структурированный обработчик исключений с помощью [. SAFESEH](../../assembler/masm/dot-safeseh.md).

Невозможно пометить существующий двоичный файл как защищенный обработчик исключений (или без обработчиков исключений). сведения об обработке безопасного исключения должны быть добавлены во время сборки.

Возможность компоновщика создавать таблицу безнадежных обработчиков исключений зависит от приложения, использующего библиотеку времени выполнения C. Если вы связываете с параметром [/NODEFAULTLIB](nodefaultlib-ignore-libraries.md) и хотите создать таблицу безнадежных обработчиков исключений, необходимо указать структуру конфигурации загрузки (например, можно найти в исходном файле лоадкфг. c CRT), которая содержит все записи, определенные для Visual C++. Пример:

```
#include <windows.h>
extern DWORD_PTR __security_cookie;  /* /GS security cookie */

/*
* The following two names are automatically created by the linker for any
* image that has the safe exception table present.
*/

extern PVOID __safe_se_handler_table[]; /* base of safe handler entry table */
extern BYTE  __safe_se_handler_count;  /* absolute symbol whose address is
                                           the count of table entries */
typedef struct {
    DWORD       Size;
    DWORD       TimeDateStamp;
    WORD        MajorVersion;
    WORD        MinorVersion;
    DWORD       GlobalFlagsClear;
    DWORD       GlobalFlagsSet;
    DWORD       CriticalSectionDefaultTimeout;
    DWORD       DeCommitFreeBlockThreshold;
    DWORD       DeCommitTotalFreeThreshold;
    DWORD       LockPrefixTable;            // VA
    DWORD       MaximumAllocationSize;
    DWORD       VirtualMemoryThreshold;
    DWORD       ProcessHeapFlags;
    DWORD       ProcessAffinityMask;
    WORD        CSDVersion;
    WORD        Reserved1;
    DWORD       EditList;                   // VA
    DWORD_PTR   *SecurityCookie;
    PVOID       *SEHandlerTable;
    DWORD       SEHandlerCount;
} IMAGE_LOAD_CONFIG_DIRECTORY32_2;

const IMAGE_LOAD_CONFIG_DIRECTORY32_2 _load_config_used = {
    sizeof(IMAGE_LOAD_CONFIG_DIRECTORY32_2),
    0,
    0,
    0,
    0,
    0,
    0,
    0,
    0,
    0,
    0,
    0,
    0,
    0,
    0,
    0,
    0,
    &__security_cookie,
    __safe_se_handler_table,
    (DWORD)(DWORD_PTR) &__safe_se_handler_count
};
```

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите папку **Компоновщик** .

1. Выберите страницу свойств **Командная строка** .

1. Введите параметр в поле **Дополнительные параметры** .

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.AdditionalOptions%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
