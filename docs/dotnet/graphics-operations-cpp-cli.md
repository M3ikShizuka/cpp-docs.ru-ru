---
description: Дополнительные сведения о графических операциях (C++/CLI)
title: Работа с графикой (C++/CLI)
ms.date: 11/04/2016
helpviewer_keywords:
- GDI+ [C++]
- .NET Framework [C++], graphics
- images [C++], .NET Framework and
- GDI+ [C++], about graphics operations
- graphics [C++], .NET Framework and
- GDI+ [C++], displaying images
- graphics [C++], displaying images
- GDI+, drawing shapes
- drawing, shapes
- shapes
- shapes, drawing
- GDI+ [C++], rotating images
- graphics [C++], rotating images
- GDI+ [C++], converting image file formats
- graphics [C++], converting image file formats
ms.assetid: bba27228-b9b3-4c9c-b31c-a04b76702a95
ms.openlocfilehash: 84dbc75aa306219b8733848ece5c594ca40a0489
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97223546"
---
# <a name="graphics-operations-ccli"></a>Работа с графикой (C++/CLI)

Демонстрируется обработка изображений с помощью Windows SDK.

В следующих разделах демонстрируется использование <xref:System.Drawing.Image?displayProperty=fullName> класса для выполнения манипуляций с изображениями.

## <a name="display-images-with-the-net-framework"></a><a name="display"></a> Отображение изображений с помощью .NET Framework

В следующем примере кода обработчик событий onpain изменяется для получения указателя на <xref:System.Drawing.Graphics> объект главной формы. <xref:System.Windows.Forms.Form.OnPaint%2A>Функция предназначена для приложения Windows Forms, которое, скорее всего, будет создано с помощью мастера приложений Visual Studio.

Изображение представлено <xref:System.Drawing.Image> классом. Данные изображения загружаются из JPG-файла с помощью <xref:System.Drawing.Image.FromFile%2A?displayProperty=fullName> метода. Перед прорисовкой изображения в форму размер формы изменяется в соответствии с изображением. Рисование изображения выполняется с помощью <xref:System.Drawing.Graphics.DrawImage%2A?displayProperty=fullName> метода.

<xref:System.Drawing.Graphics>Классы и <xref:System.Drawing.Image> находятся в <xref:System.Drawing?displayProperty=fullName> пространстве имен.

### <a name="example"></a>Пример

```cpp
#using <system.drawing.dll>

using namespace System;
using namespace System::Drawing;

protected:
virtual Void Form1::OnPaint(PaintEventArgs^ pe) override
{
    Graphics^ g = pe->Graphics;
    Image^ image = Image::FromFile("SampleImage.jpg");
    Form::ClientSize = image->Size;
    g->DrawImage( image, 0, 0, image->Size.Width, image->Size.Height );
}
```

## <a name="draw-shapes-with-the-net-framework"></a><a name="draw"></a> Рисование фигур с помощью .NET Framework

В следующем примере кода класс используется <xref:System.Drawing.Graphics> для изменения <xref:System.Windows.Forms.Form.OnPaint%2A> обработчика событий, чтобы получить указатель на <xref:System.Drawing.Graphics> объект для главной формы. Затем этот указатель используется для задания цвета фона формы и рисования линии и дуги с помощью <xref:System.Drawing.Graphics.DrawLine%2A?displayProperty=fullName> <xref:System.Drawing.Graphics.DrawArc%2A> методов и.

### <a name="example"></a>Пример

```cpp
#using <system.drawing.dll>
using namespace System;
using namespace System::Drawing;
// ...
protected:
virtual Void Form1::OnPaint(PaintEventArgs^ pe ) override
{
   Graphics^ g = pe->Graphics;
   g->Clear(Color::AntiqueWhite);

   Rectangle rect = Form::ClientRectangle;
   Rectangle smallRect;
   smallRect.X = rect.X + rect.Width / 4;
   smallRect.Y = rect.Y + rect.Height / 4;
   smallRect.Width = rect.Width / 2;
   smallRect.Height = rect.Height / 2;

   Pen^ redPen = gcnew Pen(Color::Red);
   redPen->Width = 4;
   g->DrawLine(redPen, 0, 0, rect.Width, rect.Height);

   Pen^ bluePen = gcnew Pen(Color::Blue);
   bluePen->Width = 10;
   g->DrawArc( bluePen, smallRect, 90, 270 );
}
```

## <a name="rotate-images-with-the-net-framework"></a><a name="rotate"></a> Вращение изображений с помощью .NET Framework

В следующем примере кода показано использование <xref:System.Drawing.Image?displayProperty=fullName> класса для загрузки изображения с диска, вращения его 90 градусов и сохранения в виде нового JPG-файла.

### <a name="example"></a>Пример

```cpp
#using <system.drawing.dll>

using namespace System;
using namespace System::Drawing;

int main()
{
   Image^ image = Image::FromFile("SampleImage.jpg");
   image->RotateFlip( RotateFlipType::Rotate90FlipNone );
   image->Save("SampleImage_rotated.jpg");
   return 0;
}
```

## <a name="convert-image-file-formats-with-the-net-framework"></a><a name="convert"></a> Преобразование форматов файлов изображений с помощью .NET Framework

В следующем примере кода демонстрируется <xref:System.Drawing.Image?displayProperty=fullName> класс и <xref:System.Drawing.Imaging.ImageFormat?displayProperty=fullName> перечисление, используемое для преобразования и сохранения файлов изображений. Следующий код загружает изображение из JPG-файла, а затем сохраняет его в форматах GIF и BMP.

### <a name="example"></a>Пример

```cpp
#using <system.drawing.dll>

using namespace System;
using namespace System::Drawing;
using namespace System::Drawing::Imaging;

int main()
{
   Image^ image = Image::FromFile("SampleImage.jpg");
   image->Save("SampleImage.png", ImageFormat::Png);
   image->Save("SampleImage.bmp", ImageFormat::Bmp);

   return 0;
}
```

## <a name="related-sections"></a>Связанные разделы

[Приступая к программированию графики](/dotnet/framework/winforms/advanced/getting-started-with-graphics-programming)

[Управляемый код GDI+](/dotnet/framework/winforms/advanced/about-gdi-managed-code)

## <a name="see-also"></a>См. также раздел

[Программирование .NET с использованием C++/CLI (Visual C++)](../dotnet/dotnet-programming-with-cpp-cli-visual-cpp.md)

<xref:System.Drawing>
