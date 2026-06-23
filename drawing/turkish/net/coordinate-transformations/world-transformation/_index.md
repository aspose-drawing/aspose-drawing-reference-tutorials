---
date: 2026-06-23
description: Aspose.Drawing kullanarak PNG nasıl kaydedilir, dünya dönüşümleri nasıl
  uygulanır ve grafikler PNG'ye nasıl dönüştürülür öğrenin. Çeviri dönüşümü C# örnekleri
  ve birden fazla grafik dönüşümünü içerir.
keywords:
- how to save png
- translate transform c#
- multiple graphics transformations
- convert graphics to png
- how to rotate bitmap
linktitle: Aspose.Drawing'de Dünya Dönüşümü
schemas:
- author: Aspose
  dateModified: '2026-06-23'
  description: Learn how to save PNG using Aspose.Drawing, apply world transformations,
    and convert graphics to PNG. Includes translate transform C# examples and multiple
    graphics transformations.
  headline: How to Save PNG with Aspose.Drawing – World Transformation
  type: TechArticle
- description: Learn how to save PNG using Aspose.Drawing, apply world transformations,
    and convert graphics to PNG. Includes translate transform C# examples and multiple
    graphics transformations.
  name: How to Save PNG with Aspose.Drawing – World Transformation
  steps:
  - name: Create a Bitmap
    text: We start by creating a blank canvas that will hold our drawing. `new Bitmap(width,
      height, PixelFormat.Format32bppPArgb)` creates a 32‑bit per pixel bitmap with
      premultiplied alpha, which is the optimal format for PNG output because it preserves
      transparency without extra conversion steps. - **Why 3
  - name: Set the World Transformation (Graphics Translate Example)
    text: '`TranslateTransform` moves the origin of the coordinate system to a new
      location. `graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height / 2)`
      shifts the (0,0) point to the canvas centre. After this call, any shape you
      draw using coordinates (0,0) will appear in the middle of the image. - This'
  - name: Draw a Rectangle Using the Transformed Coordinates
    text: '`DrawRectangle` draws a rectangle using the specified pen and coordinates.
      `graphics.DrawRectangle(pen, -150, -100, 300, 200)` draws a rectangle centered
      on the canvas because its top‑left corner is offset by half its width and height
      from the transformed origin. - The rectangle’s top‑left corner st'
  - name: Save the Result – Convert Graphics to PNG
    text: '`Save` writes the bitmap to a file in the specified image format. `ImageFormat`
      specifies the file format for saving images, such as PNG. `bitmap.Save(outputPath,
      ImageFormat.Png)` writes a lossless PNG file that can be used directly in web
      pages or UI components. - PNG preserves the exact colors an'
  type: HowTo
- questions:
  - answer: Yes – you can chain `TranslateTransform`, `RotateTransform`, and `ScaleTransform`
      to achieve complex effects in a single graphics pipeline.
    question: Can I apply more than one transformation?
  - answer: A free trial is available for evaluation, but a commercial license is
      required for production use.
    question: Is Aspose.Drawing free for commercial projects?
  - answer: Absolutely. Aspose.Drawing supports all modern .NET runtimes, including
      .NET Core, .NET 5, .NET 6, and .NET 7.
    question: Does this work with .NET Core and .NET 5/6/7?
  - answer: The complete documentation is available [here](https://reference.aspose.com/drawing/net/).
    question: Where can I find the full API reference?
  - answer: Verify the path string, ensure write permissions, and confirm the directory
      exists before calling `Save`.
    question: How do I troubleshoot a missing output file?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Aspose.Drawing ile PNG Kaydetme – Dünya Dönüşümü
url: /tr/net/coordinate-transformations/world-transformation/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing ile PNG Kaydetme – Dünya Dönüşümü

## PNG Olarak Bitmap Kaydetme – Giriş

**PNG nasıl kaydedilir** using Aspose.Drawing is a common requirement when you need high‑quality, transparent images generated on the fly. In this tutorial you’ll learn how to **save bitmap as PNG**, apply world transformations such as translate, rotate, and scale, and finally convert graphics to PNG—all with clean, maintainable C# code. Whether you’re building a reporting engine, a charting component, or a custom UI renderer, mastering these steps lets you create dynamic images that look great on any device.

## Hızlı Yanıtlar
- **“dünya dönüşümü” ne anlama gelir?** Bu, çiziminizin mantıksal (dünya) koordinatlarını sayfa (cihaz) koordinatlarına eşler.  
- **Sonucu PNG olarak dışa aktarabilir miyim?** Evet – çizimden sonra sadece `bitmap.Save(...)` metodunu `.png` uzantısıyla çağırırsınız.  
- **Aspose.Drawing için lisansa ihtiyacım var mı?** Geliştirme için ücretsiz deneme sürümü çalışır; üretim için ticari lisans gereklidir.  
- **Bu .NET 6/7 ile uyumlu mu?** Kesinlikle – Aspose.Drawing .NET Framework 4.5+ ve .NET Core/5/6/7'yi destekler.  
- **Kaç dönüşümü zincirleyebilirim?** **birden fazla grafik dönüşümünü** sıralı olarak uygulayabilirsiniz (çevirme, döndürme, ölçekleme vb.).

## Aspose.Drawing'de Dünya Dönüşümü Nedir?

Bir dünya dönüşümü, çizim komutlarınızın kullandığı koordinat sistemini değiştirir. Varsayılan olarak, (0,0) bitmap'in sol‑üst köşesidir. `TranslateTransform`, `RotateTransform` veya `ScaleTransform` ile bu başlangıç noktasını yeniden konumlandırabilir, şekilleri döndürebilir veya yeniden boyutlandırabilirsiniz; orijinal geometriyi değiştirmeden.

## Aspose.Drawing Kullanarak PNG Nasıl Kaydedilir?

`Bitmap` nesnesini yükleyin, `Graphics` örneği üzerinde istediğiniz dünya dönüşümlerini ayarlayın, şekillerinizi çizin ve sonunda `bitmap.Save("output.png", ImageFormat.Png)` metodunu çağırın. Bu tek satırlık kaydetme çağrısı, şeffaflığı ve renk doğruluğunu koruyan kayıpsız bir PNG dosyası yazar; bu da web varlıkları ve UI bindirmeleri için idealdir.

## Neden Bir Grafik Çevirme Örneği Kullanılır?

Bir grafik çevirme örneği, her noktayı yeniden hesaplamak yerine çizim başlangıç noktasını bir kez hareket ettirmenizi sağlar. Bu yaklaşım kod karmaşıklığını azaltır, okunabilirliği artırır ve grafik motorunun matris hesaplamalarını verimli bir şekilde yapmasına izin verir; bu da büyük tuvallerde render performansını %30'a kadar artırabilir.

## Grafik Çevirme Örneği

**Grafik çevirme örneği**, başlangıç noktasını hareket ettirmenin konumlandırmayı nasıl basitleştirdiğini gösterir. Her noktayı yeniden hesaplamak yerine, koordinat sistemini bir kez kaydırır ve yeni başlangıç noktasının tuvalin ortasıymış gibi çizersiniz.

## Önkoşullar

Before we begin, ensure you have:

- **Aspose.Drawing kütüphanesini** .NET projenize entegre edin – resmi [Aspose.Drawing sürüm sayfasından](https://releases.aspose.com/drawing/net/) indirin.  
- Çıktı görüntüsünün kaydedileceği bir **belge dizini**.  
- **C#** sözdizimi ve Visual Studio ya da tercih ettiğiniz IDE hakkında temel bilgi.  

Şimdi, koda dalalım!

## Ad Alanlarını İçe Aktarma

`Bitmap`, `Graphics` ve Aspose çizim yardımcıları bu ad alanlarında bulunur.  
**Tanım:** `System.Drawing` temel GDI+ tiplerini sağlar, `Aspose.Drawing` ise bunları çapraz platform yetenekleriyle genişletir.

## Adım‑Adım Kılavuz

### Adım 1: Bitmap Oluşturma

Çizimimizi tutacak boş bir tuval oluşturarak başlıyoruz.

`new Bitmap(width, height, PixelFormat.Format32bppPArgb)` 32‑bit piksel başına önceden çarpılmış alfa içeren bir bitmap oluşturur; bu, şeffaflığı ekstra dönüşüm adımları olmadan koruduğu için PNG çıktısı için optimal formattır.

- **Neden 32bppPArgb?** Bu piksel formatı alfa şeffaflığını ve yüksek kaliteli renk renderını destekler, PNG çıktısı için mükemmeldir.  
- **İpucu:** Genişlik/yüksekliği hedef görüntü boyutunuza göre ayarlayın.

### Adım 2: Dünya Dönüşümünü Ayarla (Grafik Çevirme Örneği)

`TranslateTransform` koordinat sisteminin başlangıç noktasını yeni bir konuma taşır.  
`graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height / 2)` (0,0) noktasını tuvalin ortasına kaydırır. Bu çağrıdan sonra, (0,0) koordinatlarıyla çizdiğiniz herhangi bir şekil görüntünün ortasında görünecektir.

- Bu, (0,0) noktasını (500, 400) konumuna taşır – 1000 × 800 bir tuvalin ortası.  
- Ek dönüşümler zincirleyebilirsiniz: `RotateTransform` koordinat sistemini döndürür, `ScaleTransform` ise ölçeklendirir; bu da **birden fazla grafik dönüşümünü** etkinleştirir.

### Adım 3: Dönüştürülmüş Koordinatları Kullanarak Dikdörtgen Çizme

`DrawRectangle` belirtilen kalem ve koordinatlarla bir dikdörtgen çizer.

`graphics.DrawRectangle(pen, -150, -100, 300, 200)` dikdörtgeni tuvalin ortasına çizer çünkü sol‑üst köşesi, dönüştürülmüş başlangıç noktasından (görüntünün merkezi) yarı genişlik ve yarı yükseklik kadar kaydırılmıştır.

- Dikdörtgenin sol‑üst köşesi, dönüştürülmüş başlangıç noktasında (görüntünün ortası) başlar.  
- Diğer şekillerle (elips, çizgi veya özel yollar) denemeler yapmaktan çekinmeyin.

### Adım 4: Sonucu Kaydet – Grafikleri PNG'ye Dönüştür

`Save` bitmap'i belirtilen görüntü formatında bir dosyaya yazar.  
`ImageFormat` görüntüleri kaydetmek için dosya formatını belirtir, örneğin PNG.

`bitmap.Save(outputPath, ImageFormat.Png)` doğrudan web sayfalarında veya UI bileşenlerinde kullanılabilecek kayıpsız bir PNG dosyası yazar.

- PNG, daha önce ayarladığımız tam renkleri ve şeffaflığı korur.  
- `"Your Document Directory"` ifadesini makinenizdeki gerçek yol ile değiştirin.

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden Oluşur | Çözüm |
|-------|----------------|-----|
| **Dosya bulunamadı hatası** kaydederken | Hedef klasör mevcut değil. | `Save` metodunu çağırmadan önce klasörü programlı olarak (`Directory.CreateDirectory`) oluşturun. |
| **Dönüşümden sonra boş görüntü** | `TranslateTransform` çizimden sonra çağrıldı. | Dönüşümün herhangi bir çizim komutundan **önce** ayarlandığından emin olun. |
| **Bozulmuş renkler** | Uyumsuz bir piksel formatı kullanılıyor. | PNG çıktısı için `Format32bppPArgb` formatını kullanın. |

## Sıkça Sorulan Sorular

**S: Birden fazla dönüşüm uygulayabilir miyim?**  
C: Evet – `TranslateTransform`, `RotateTransform` ve `ScaleTransform`'ı zincirleyerek tek bir grafik işlem hattında karmaşık efektler elde edebilirsiniz.

**S: Aspose.Drawing ticari projeler için ücretsiz mi?**  
C: Değerlendirme için ücretsiz bir deneme sürümü mevcuttur, ancak üretim kullanımı için ticari lisans gereklidir.

**S: Bu .NET Core ve .NET 5/6/7 ile çalışır mı?**  
C: Kesinlikle. Aspose.Drawing tüm modern .NET çalışma zamanlarını destekler, .NET Core, .NET 5, .NET 6 ve .NET 7 dahil.

**S: Tam API referansını nerede bulabilirim?**  
C: Tam dökümantasyon [burada](https://reference.aspose.com/drawing/net/) mevcuttur.

**S: Eksik çıktı dosyasını nasıl gideririm?**  
C: Yol dizesini doğrulayın, yazma izinlerini kontrol edin ve `Save` metodunu çağırmadan önce dizinin var olduğundan emin olun.

## Sonuç

Artık Aspose.Drawing ile **PNG nasıl kaydedilir** öğrendiniz, bir **dünya dönüşümü** uyguladınız ve **grafik çevirme örneği** yaptınız; bu örnek döndürme veya ölçekleme ile genişletilebilir. Bu yapı taşlarını ustalıkla kullanarak dinamik görüntüler üretebilir, özel grafikler oluşturabilir veya herhangi bir .NET uygulaması için anlık grafikler oluşturabilirsiniz.

---

**Last Updated:** 2026-06-23  
**Test Edilen:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  
**İlgili Kaynaklar:** [Aspose.Drawing API Reference](https://reference.aspose.com/drawing/net/) | [Download Free Trial](https://releases.aspose.com/drawing/net/)

```csharp
using System.Drawing;
using Aspose.Drawing;
```

```csharp
//ExStart: WorldTransformation
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

```csharp
// Set the transformation that maps world coordinates to page coordinates:
graphics.TranslateTransform(500, 400);
```

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawRectangle(pen, 0, 0, 300, 200);
```

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\WorldTransformation_out.png");
//ExEnd: WorldTransformation
```

## İlgili Öğreticiler

- [Matris Dönüşümü Öğreticisi: Aspose.Drawing için .NET'te Matris Dönüşümleri](/drawing/net/coordinate-transformations/matrix-transformations/)
- [Aspose.Drawing Global Dönüşümü ile Görüntüyü Nasıl Döndürürsünüz](/drawing/net/coordinate-transformations/global-transformation/)
- [Koordinat Sistemi Dönüşümü – Aspose.Drawing için .NET'te Sayfa Dönüşümü](/drawing/net/coordinate-transformations/page-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}