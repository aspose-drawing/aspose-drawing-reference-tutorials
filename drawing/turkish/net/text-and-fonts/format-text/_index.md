---
date: 2026-07-17
description: Aspose.Drawing for .NET'te text alignment ayarlayarak text overflow'ı
  nasıl önleyeceğinizi ve görüntülere metin eklemeyi öğrenin. Örneklerle adım adım
  rehber.
keywords:
- prevent text overflow
- draw string on image
- center text in rectangle
- vertical text alignment
- replace system drawing
lastmod: 2026-07-17
linktitle: Aspose.Drawing for .NET ile Text Alignment'ı Ayarlayın
og_description: Aspose.Drawing for .NET'te text alignment ayarlayarak text overflow'ı
  önleyin. Görüntü üzerine draw string yapmayı, rectangle içinde metni ortalamayı
  ve System.Drawing'i değiştirmeyi öğrenin.
og_image_alt: 'Developer guide: Prevent text overflow by aligning text in Aspose.Drawing
  for .NET'
og_title: Text Overflow'ı Önleyin – Aspose.Drawing for .NET ile Text Alignment'ı Ayarlayın
schemas:
- author: Aspose
  dateModified: '2026-07-17'
  description: Learn how to prevent text overflow by setting text alignment in Aspose.Drawing
    for .NET and add text to images. Step‑by‑step guide with examples.
  headline: Prevent Text Overflow – Set Text Alignment with Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to prevent text overflow by setting text alignment in Aspose.Drawing
    for .NET and add text to images. Step‑by‑step guide with examples.
  name: Prevent Text Overflow – Set Text Alignment with Aspose.Drawing for .NET
  steps:
  - name: '**Aspose.Drawing Library** – download it [here](https://releases.aspose.com/drawing/net/).'
    text: '**Aspose.Drawing Library** – download it [here](https://releases.aspose.com/drawing/net/).'
  - name: '**Development Environment** – Visual Studio 2022 (or any C# IDE).'
    text: '**Development Environment** – Visual Studio 2022 (or any C# IDE).'
  - name: '**Basic .NET knowledge** – you should be comfortable with C# projects and
      NuGet packages.'
    text: '**Basic .NET knowledge** – you should be comfortable with C# projects and
      NuGet packages.'
  - name: '**Resize the rectangle** – increase `rectangle.Width` or `rectangle.Height`.'
    text: '**Resize the rectangle** – increase `rectangle.Width` or `rectangle.Height`.'
  - name: '**Split the text** – break the string into lines that fit, then call `DrawString`
      for each line with adjusted Y‑coordinates.'
    text: '**Split the text** – break the string into lines that fit, then call `DrawString`
      for each line with adjusted Y‑coordinates.'
  type: HowTo
- questions:
  - answer: Omit the `DrawRectangle` call and pass the desired `PointF` location to
      `Graphics.DrawString`.
    question: How do I draw a string without a surrounding rectangle?
  - answer: Yes—apply a `Matrix` transformation to the `Graphics` object before drawing,
      then reset it afterwards.
    question: Can I rotate the text while keeping alignment?
  - answer: Simply change the file extension in `bitmap.Save` and optionally specify
      `ImageFormat.Jpeg`.
    question: Is it possible to export the image as JPEG instead of PNG?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- prevent text overflow
- Aspose.Drawing
- .NET graphics
- text alignment
title: Text Overflow'ı Önleyin – Aspose.Drawing for .NET ile Text Alignment'ı Ayarlayın
url: /tr/net/text-and-fonts/format-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Metin Taşmasını Önleme – Aspose.Drawing ile Metin Hizalamasını Ayarlama

## Giriş

When you need to **prevent text overflow** while rendering graphics in .NET, Aspose.Drawing gives you fine‑grained control over text placement, alignment, and wrapping. Whether you’re building a badge generator, a dynamic report, or any image‑based output, mastering text alignment ensures that your text stays inside the intended rectangle and looks polished. In this guide we’ll walk through creating a bitmap canvas, configuring `StringFormat`, drawing a rectangle with centered text, handling overflow, and finally saving the image.

## Hızlı Yanıtlar
- **“set text alignment” ne anlama gelir?** Metnin bir çizim dikdörtgeni içinde yatay ve dikey olarak nasıl konumlandırıldığını tanımlar.  
- **Hangi sınıf hizalamayı kontrol eder?** `StringFormat` `Alignment` ve `LineAlignment` ayarlamanızı sağlar.  
- **Bir dizeyi ve bir dikdörtgeni birlikte çizebilir miyim?** Evet—`Graphics.DrawRectangle` ardından `Graphics.DrawString` kullanın.  
- **Metin taşmasını nasıl önleyebilirim?** Dikdörtgen boyutunu ayarlayın veya metni manuel olarak birden fazla satıra bölün.  
- **Üretim için lisansa ihtiyacım var mı?** Değerlendirme dışı kullanım için ticari bir Aspose.Drawing lisansı gereklidir.

## Aspose.Drawing'de **set text alignment** nedir?

`set text alignment` configures horizontal (`StringAlignment`) and vertical (`LineAlignment`) placement of text within a `Rectangle` or drawing region. By adjusting these properties you control whether text appears left‑aligned, centered, right‑aligned, top‑aligned, middle‑aligned, or bottom‑aligned, enabling precise layout in graphics, badges, and reports generated with Aspose.Drawing.

## Metin hizalaması için Aspose.Drawing'i neden kullanmalısınız?

Aspose.Drawing eliminates the GDI+ limitations that plague `System.Drawing.Common`. It supports **5 major .NET runtimes** – .NET Framework 4.6+, .NET Core 2.0+, .NET 5, .NET 6, and .NET 7 – and can render images up to **4000 × 4000 px** (≈ 100 MB) without exhausting memory. Anti‑aliasing, high‑DPI scaling, and full Linux container compatibility let you generate pixel‑perfect graphics in any deployment scenario.

## Önkoşullar

1. **Aspose.Drawing Kütüphanesi** – [buradan](https://releases.aspose.com/drawing/net/) indirin.  
2. **Geliştirme Ortamı** – Visual Studio 2022 (veya herhangi bir C# IDE).  
3. **Temel .NET bilgisi** – C# projeleri ve NuGet paketleriyle rahat olmalısınız.

## Ad Alanlarını İçe Aktarma

To start, bring the required namespaces into scope. These give you access to graphics, text rendering, and drawing primitives.

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Aspose.Drawing ile metin taşmasını nasıl önleyebilirsiniz?

Bitmap, bellekte depolanan bir görüntüyü temsil eden bir sınıftır, `RectangleF` ise çizim için kayan noktalı bir dikdörtgen alanı tanımlar. `StringFormat` içinde `Trimming` özelliği `StringTrimming.EllipsisCharacter` olarak ayarlandığında, fazla karakterler otomatik olarak üç nokta (…) ile değiştirilir ve metnin dikdörtgen sınırlarını aşması engellenir. Diziyi önce ölçmek, dikdörtgeni küçültüp küçültmeyeceğinize veya metni birden fazla satıra bölüp bölmeyeceğinize karar vermenizi sağlar ve taşma olmadan temiz bir düzen garantiler.

Load your bitmap, define a suitably sized `RectangleF`, and use a `StringFormat` with `Trimming` set to `StringTrimming.EllipsisCharacter` to automatically cut off excess characters. For full control, measure the string with `Graphics.MeasureString` and shrink the rectangle or split the text into lines before drawing. This approach guarantees that no characters spill outside the visual bounds.

## Adım 1: Bitmap ve Graphics Nesnelerini Oluşturma  

Bitmap represents an in‑memory image, while Graphics provides drawing methods for that bitmap. Creating a bitmap provides a canvas you can draw on. The `Graphics` object is the drawing surface, and we enable high‑quality text rendering with `TextRenderingHint`.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

## Adım 2: **StringFormat** ve Stil Tanımlama  

StringFormat specifies text layout options such as alignment, line spacing, and trimming. Here we **set text alignment** by configuring a `StringFormat` instance. We also prepare brushes, pens, and a font that will be used when drawing the string.

```csharp
StringFormat stringFormat = new StringFormat();
stringFormat.Alignment = StringAlignment.Center;          // Horizontal alignment
stringFormat.LineAlignment = StringAlignment.Center;      // Vertical alignment

Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

## Adım 3: Metni Oluşturma ve Biçimlendirme – **how to draw string** ve **draw rectangle with text**

Graphics.DrawString renders text onto the canvas, and Graphics.DrawRectangle draws a rectangle shape. We compose the text, define the rectangle that will contain it, and then draw both the rectangle border and the string itself.

```csharp
string text = "Lorem ipsum ...";  // (Your lengthy text goes here)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle, stringFormat);
```

### Metin taşmasını nasıl ele alabilirsiniz

If the supplied `text` exceeds the rectangle’s bounds, you have two common options:

1. **Dikdörtgeni yeniden boyutlandırın** – `rectangle.Width` veya `rectangle.Height` değerini artırın.  
2. **Metni bölün** – dizeyi sığacak satırlara ayırın, ardından her satır için Y koordinatlarını ayarlayarak `DrawString` çağırın.

## Aspose.Drawing kullanarak görüntü üzerine dize nasıl çizilir?

Graphics.DrawString draws the specified text using a font and formatting options. Instantiate a `Graphics` object from your bitmap, then call `DrawString` with the prepared `StringFormat`. This single call renders the text exactly where you want it, respecting alignment, trimming, and any transformation matrix you have applied. Adding a high‑quality rendering hint ensures the output remains crisp on high‑DPI displays.

## Dikdörtgen içinde metni nasıl ortalarsınız?

StringAlignment determines horizontal alignment of text within a layout rectangle. Set `stringFormat.Alignment = StringAlignment.Center` and `stringFormat.LineAlignment = StringAlignment.Center`. This centers the text horizontally and vertically inside the rectangle, making it ideal for badges, buttons, or label overlays. The centered placement works consistently across different image sizes and DPI settings, providing a balanced visual appearance.

## Dikey metin hizalamasını nasıl elde edersiniz?

LineAlignment controls vertical placement of text inside the rectangle. Use `stringFormat.LineAlignment` with values `StringAlignment.Near`, `Center`, or `Far` to position text at the top, middle, or bottom of the rectangle. Combine this with `Graphics.TranslateTransform` if you need to rotate the text while preserving vertical alignment. Adjusting the line alignment ensures that multi‑line blocks line up exactly where you expect them to, even after transformations.

## Adım 4: Çıktıyı Kaydet – **add text to image**

Finally, write the bitmap to disk. This step demonstrates **add text to image** in a single call.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\FormatText_out.png");
```

## Yaygın Sorunlar ve Çözümler

| Sorun | Çözüm |
|-------|----------|
| **Metin bulanık görünüyor** | `graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;` ayarlandığından emin olun. |
| **Metin kesiliyor** | Dikdörtgen boyutunu artırın veya dize boyutunu ölçerek (`Graphics.MeasureString`) kelime kaydırma mantığını etkinleştirin. |
| **Yazı tipi bulunamadı** | Yazı tipinin ana bilgisayarda yüklü olduğunu doğrulayın veya `PrivateFontCollection` kullanarak özel bir yazı tipi gömün. |
| **Beklenmeyen renkler** | Fırça ve kalem renklerini tekrar kontrol edin; `Color.FromKnownColor` sistem tanımlı renkler kullandığını unutmayın. |

## Sıkça Sorulan Sorular

**S1: Aspose.Drawing tüm .NET sürümleriyle uyumlu mu?**  
C1: Evet, Aspose.Drawing, geliştiricilere esneklik sağlamak için geniş bir .NET sürüm yelpazesiyle uyumlu olacak şekilde tasarlanmıştır.

**S2: Yazı tipi stilini daha da özelleştirebilir miyim?**  
C2: Kesinlikle! İstediğiniz yazı tipi boyutu, stili ve ailesini elde etmek için `Font` nesnesi parametrelerini ayarlayın.

**S3: Tanımlı dikdörtgen içinde metin taşmasını nasıl yönetebilirim?**  
C3: Dikdörtgenin boyutunu ayarlayarak veya uzun metinleri işlemek için özel mantık uygulayarak metin taşmasını yönetebilirsiniz.

**S4: Aspose.Drawing'de başka biçimlendirme seçenekleri var mı?**  
C4: Evet, Aspose.Drawing, metin, şekiller ve daha fazlası için çeşitli biçimlendirme seçenekleri dahil olmak üzere grafik manipülasyonu için kapsamlı bir araç seti sunar.

**S5: Aspose.Drawing için ek destek nereden bulunabilir?**  
C5: Topluluk desteği ve tartışmalar için Aspose.Drawing forumunu [burada](https://forum.aspose.com/c/drawing/44) keşfedin.

**Ekstra Soru & Cevap**

**S: Çevreleyen bir dikdörtgen olmadan dizeyi nasıl çizerim?**  
C: `DrawRectangle` çağrısını atlayın ve istediğiniz `PointF` konumunu `Graphics.DrawString`'e geçirin.

**S: Hizalamayı korurken metni döndürebilir miyim?**  
C: Evet—çizmeye başlamadan önce `Graphics` nesnesine bir `Matrix` dönüşümü uygulayın, ardından sonrasında sıfırlayın.

**S: Görüntüyü PNG yerine JPEG olarak dışa aktarmak mümkün mü?**  
C: `bitmap.Save` içinde dosya uzantısını değiştirin ve isteğe bağlı olarak `ImageFormat.Jpeg` belirtin.

---

**Son Güncelleme:** 2026-07-17  
**Test Edilen:** Aspose.Drawing 24.11 for .NET  
**Yazar:** Aspose  

{{< blocks/products/products-backtop-button >}}

## İlgili Öğreticiler

- [Aspose.Drawing for .NET ile Metin Çizme](/drawing/net/text-and-fonts/draw-text/)
- [Aspose.Drawing'de Görsellere Metin Ekleme](/drawing/net/use-cases/text-on-image/)
- [Aspose.Drawing for .NET ile Metin ve Yazı Tipleri Çizme](/drawing/net/text-and-fonts/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}