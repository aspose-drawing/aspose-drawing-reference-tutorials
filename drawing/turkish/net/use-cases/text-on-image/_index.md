---
date: 2026-02-27
description: Aspose.Drawing for .NET kullanarak doğum günü kartı resmi oluşturmayı
  öğrenin. Bu rehber, görüntü üzerine metin çizmeyi, fotoğrafın üzerine metin yerleştirmeyi
  ve fotoğrafa hızlıca başlık eklemeyi gösterir.
linktitle: Adding Text on Images in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Aspose.Drawing ile Doğum Günü Kartı Görseli Nasıl Oluşturulur
url: /tr/net/use-cases/text-on-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing ile Doğum Günü Kartı Görseli Nasıl Oluşturulur

## Introduction
.NET geliştirme dünyasının dinamik ortamında, Aspose.Drawing görüntüleri kolayca manipüle etmek için güçlü bir araç olarak öne çıkıyor. **Doğum günü kartı görseli oluşturmak**, bir filigran eklemek ya da sadece bir resme metin bindirmek ister misiniz, bu öğretici C# kullanarak görüntü üzerine metin çizmeyi adım adım gösteriyor. Bu rehberin sonunda paylaşmaya hazır kişiselleştirilmiş bir doğum günü kartınız olacak.

## Quick Answers
- **What library should I use?** Aspose.Drawing for .NET  
- **Can I add a caption to photo?** Yes – use `Graphics.DrawString` with custom fonts.  
- **Is a license required for production?** Yes, a commercial license is needed.  
- **Which .NET versions are supported?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **How long does implementation take?** Typically under 10 minutes for a simple card.

## What is a Birthday Card Image?
Doğum günü kartı görseli, arka plan fotoğrafı ile özel metin—örneğin bir selam, alıcının adı ya da kutlama mesajı—birleştiren kişiselleştirilmiş bir resimdir. Aspose.Drawing kullanarak bu kartları manuel grafik tasarım araçlarına ihtiyaç duymadan programatik olarak oluşturabilirsiniz.

## Why Use Aspose.Drawing to Overlay Text on Picture?
- **Cross‑platform support:** Works on Windows, Linux, and macOS.  
- **Rich drawing API:** Full control over fonts, colors, and layout.  
- **No external dependencies:** Replaces `System.Drawing.Common` with a fully managed library.  
- **High performance:** Optimized for bulk image processing.

## Prerequisites
Tutoriala başlamadan önce aşağıdakilerin hazır olduğundan emin olun:

1. Aspose.Drawing Library: Download and install the Aspose.Drawing library from the [Aspose.Drawing for .NET documentation](https://reference.aspose.com/drawing/net/).  
2. Development Environment: A working .NET development environment, such as Visual Studio or Visual Studio Code, with .NET 6 SDK or later installed.

Şimdi, bir görüntüye metin ekleyip doğum günü kartı olarak kaydetmek için adım adım rehberi inceleyelim.

## Import Namespaces
Projenize gerekli ad alanlarını ekleyerek başlayın:

```csharp
using System;
using System.Drawing;
using System.Drawing.Text;
using System.Linq;
```

## Step 1: Load the Image
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "UseCases", "girl.jpg")))
{
    var graphics = Graphics.FromImage(image);
    graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
    graphics.PageUnit = GraphicsUnit.Pixel;
```
Burada, belirtilen dosya yolundan görüntüyü yüklüyor ve sonraki işlemler için graphics nesnesini başlatıyoruz.

## Step 2: Set Text Properties
```csharp
SolidBrush brush = new SolidBrush(Color.Navy);
Font font = new Font("Calibri", 20, FontStyle.Italic);
int padding = 5;
```
Renk, yazı tipi ve dolgu gibi metin özelliklerini tanımlayın. Tasarım tercihlerinize göre bu parametreleri ayarlayın.

## Step 3: Measure Text Size
```csharp
string text = "Happy Birthday!";
var words = text.Split(' ');
int extentWidth = 0;
int extentHeight = 0;
words.ToList().ForEach(word =>
{
    var stringSize = graphics.MeasureString(word, font);
    extentWidth = Math.Max(extentWidth, (int)stringSize.Width + padding);
    extentHeight += (int)stringSize.Height;
});
```
Her kelimeyi ayrı ayrı ölçerek metnin gerekli boyutunu hesaplayın. Bu, doğru konumlandırma ve metin çakışmasını önler.

## Step 4: Draw Text on Image
```csharp
Rectangle rectangle = new Rectangle(image.Width - padding - extentWidth, image.Height - padding - extentHeight, extentWidth, extentHeight);
graphics.DrawString(text, font, brush, rectangle);
```
Şimdi, hesaplanan boyuta göre metni görüntü üzerine konumlandırın ve belirtilen yazı tipi ve renk ile çizin.

## Step 5: Save the Image
```csharp
image.Save(Path.Combine("Your Document Directory", "UseCases", "girl_card_out.jpg"));
}
```
Değiştirilmiş görüntüyü istediğiniz dizine kaydedin. Ortaya çıkan dosya, gönderilmeye hazır bir doğum günü kartı görselidir.

## Common Use Cases & Tips
- **Add caption to photo:** Replace `text` with any caption you need, such as “Celebrating 30 Years!”.  
- **Draw text on bitmap:** The same approach works for `Bitmap` objects created from scratch.  
- **Overlay multiple lines:** Loop through an array of strings and adjust the `Rectangle` Y‑coordinate for each line.  
- **Pro tip:** Use `Graphics.SmoothingMode = SmoothingMode.AntiAlias` for even smoother text rendering.

## Conclusion
Aspose.Drawing, .NET’te görüntü manipülasyonu görevlerini basitleştirerek geliştiricilere sağlam bir araç seti sunar. **Doğum günü kartı görseli oluşturmak**, **görüntü üzerine metin çizmek** ya da **fotoğrafa başlık eklemek** gibi işlemler, bu kütüphanenin grafik öğelerini yönetmedeki çok yönlülüğünün sadece bir örneğidir.

## Frequently Asked Questions
### Is Aspose.Drawing compatible with all image formats?
Aspose.Drawing supports a wide range of image formats, including popular ones like JPEG, PNG, and GIF. Refer to the [documentation](https://reference.aspose.com/drawing/net/) for a complete list.

### Can I use Aspose.Drawing for commercial projects?
Yes, Aspose.Drawing is suitable for both personal and commercial projects. For licensing details, visit the [purchase page](https://purchase.aspose.com/buy).

### Are temporary licenses available for testing purposes?
Yes, you can obtain a temporary license for testing by visiting [Temporary License](https://purchase.aspose.com/temporary-license/).

### Where can I find community support for Aspose.Drawing?
Engage with the community and get support on the [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44).

### How do I get started with Aspose.Drawing?
Begin by downloading the library from [here](https://releases.aspose.com/drawing/net/) and explore the comprehensive [documentation](https://reference.aspose.com/drawing/net/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-02-27  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

---