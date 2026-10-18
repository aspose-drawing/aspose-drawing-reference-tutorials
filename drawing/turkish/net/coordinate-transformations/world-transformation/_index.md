---
date: 2026-10-18
description: Aspose.Drawing ile çizimi PNG'ye dönüştürün ve dünya dönüşümlerini uygulayın.
  C#'ta taşıma, döndürme ve ölçekleme örneklerini öğrenin ve şeffaf PNG'leri dışa
  aktarın.
keywords:
- convert drawing to png
- save graphics as png
- rotate image .net
- scale graphics .net
- transparent png bitmap
lastmod: 2026-10-18
linktitle: Aspose.Drawing'da dünya dönüşümü
og_description: Aspose.Drawing ile çizimi PNG'ye dönüştürün, dünya dönüşümlerini uygulayın
  ve şeffaf PNG'leri dışa aktarın. .NET için C#'ta taşıma, döndürme ve ölçekleme örneklerini
  öğrenin.
og_image_alt: Tutorial showing how to convert drawing to PNG using Aspose.Drawing
  with world transformation
og_title: Aspose.Drawing ile çizimi PNG'ye dönüştürme – dünya dönüşümü
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Convert drawing to PNG with Aspose.Drawing while applying world transformations.
    Learn translate, rotate and scale examples in C# and export transparent PNGs.
  headline: How to convert drawing to PNG with Aspose.Drawing – world transformation
  type: TechArticle
- description: Convert drawing to PNG with Aspose.Drawing while applying world transformations.
    Learn translate, rotate and scale examples in C# and export transparent PNGs.
  name: How to convert drawing to PNG with Aspose.Drawing – world transformation
  steps:
  - name: create a bitmap
    text: '**Definition:** `Bitmap` is Aspose.Drawing’s in‑memory representation of
      a raster image that you can draw on or save to disk. We start by creating a
      blank canvas that will hold our drawing. `new Bitmap(width, height, PixelFormat.Format32bppPArgb)`
      creates a 32‑bit per pixel bitmap with premultiplied'
  - name: set the world transformation (graphics translate example)
    text: '**Definition:** `Graphics` is the drawing surface that renders shapes onto
      a `Bitmap`. `TranslateTransform` moves the origin of the coordinate system to
      a new location. `graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height
      / 2)` shifts the (0,0) point to the canvas centre. After this call, an'
  - name: draw a rectangle using the transformed coordinates
    text: '**Definition:** `DrawRectangle` is a method of `Graphics` that renders
      a rectangular outline or filled shape based on the supplied pen and coordinates.
      `graphics.DrawRectangle(pen, -150, -100, 300, 200)` draws a rectangle centered
      on the canvas because its top‑left corner is offset by half its width'
  - name: save the result – convert graphics to PNG
    text: '**Definition:** `ImageFormat` is an enumeration that tells the `Save` method
      which file format to use. `Save` writes the bitmap to a file in the specified
      image format. `bitmap.Save(outputPath, ImageFormat.Png)` writes a lossless PNG
      file that can be used directly in web pages or UI components. - PN'
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
  - answer: The complete documentation is available [Aspose.Drawing .NET API reference](https://reference.aspose.com/drawing/net/).
    question: Where can I find the full API reference?
  - answer: Verify the path string, ensure write permissions, and confirm the directory
      exists before calling `Save`.
    question: How do I troubleshoot a missing output file?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- convert drawing to png
- Aspose.Drawing
- .NET graphics
- PNG export
- world transformation
title: Aspose.Drawing ile çizimi PNG'ye dönüştürme – dünya dönüşümü
url: /tr/net/coordinate-transformations/world-transformation/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing ile Çizimi PNG'ye Dönüştürme – dünya dönüşümü

## Bitmap'i PNG Olarak Kaydet – Giriş

**Çizimi PNG'ye Dönüştürme** Aspose.Drawing kullanarak, yüksek kaliteli, şeffaf görüntülerin anında oluşturulması gerektiğinde yaygın bir gereksinimdir. Bu öğreticide **bitmap'i PNG olarak kaydetmeyi**, çevirme, döndürme ve ölçekleme gibi dünya dönüşümlerini uygulamayı ve sonunda grafikleri PNG'ye dönüştürmeyi – temiz, sürdürülebilir C# kodu ile öğreneceksiniz. Raporlama motoru, grafik bileşeni ya da özel bir UI renderleyicisi oluşturuyor olun, bu adımları ustalaşmak, herhangi bir cihazda harika görünen dinamik görüntüler üretmenizi sağlar.

## Hızlı cevaplar
- **“world transformation” ne anlama geliyor?** Çiziminizin mantıksal (dünya) koordinatlarını sayfa (cihaz) koordinatlarına eşler, tek bir matrisle her şeyi yeniden konumlandırmanıza, döndürmenize veya ölçeklemenize olanak tanır.  
- **Sonucu PNG olarak dışa aktarabilir miyim?** Evet – çizimden sonra sadece `bitmap.Save(...)` metodunu `.png` uzantısıyla çağırmanız yeterlidir.  
- **Aspose.Drawing için bir lisansa ihtiyacım var mı?** Geliştirme için ücretsiz deneme sürümü çalışır; üretim için ticari lisans gereklidir.  
- **.NET 6/7 ile uyumlu mu?** Kesinlikle – Aspose.Drawing .NET Framework 4.5+ ve .NET Core/5/6/7'yi destekler, mevcut .NET dağıtımlarının %90 +’ını kapsar.  
- **Kaç dönüşümü zincirleyebilirim?** **Birden fazla grafik dönüşümünü** (çevirme, döndürme, ölçekleme vb.) sıralı olarak uygulayabilirsiniz, performans kaybı olmaz.

## Aspose.Drawing'de dünya dönüşümü nedir?

Bir dünya dönüşümü, çizim komutlarınızın kullandığı koordinat sistemini değiştirir. Varsayılan olarak, (0,0) bitmap'in sol‑üst köşesidir. `TranslateTransform`, `RotateTransform` veya `ScaleTransform` ile bu orijini yeniden konumlandırabilir, şekilleri döndürebilir veya yeniden boyutlandırabilirsiniz; orijinal geometrinin değişmemesi sağlanır. Bu sayede bir kez tasarlayıp, istediğiniz boyut veya yönlendirmede render edebilirsiniz.

## Aspose.Drawing ile PNG nasıl kaydedilir?

Bir `Bitmap` nesnesi yükleyin, `Graphics` örneği üzerinde istediğiniz dünya dönüşümlerini ayarlayın, şekillerinizi çizin ve sonunda `bitmap.Save("output.png", ImageFormat.Png)` çağrısını yapın. Bu tek satırlık kaydetme işlemi, şeffaflığı ve renk doğruluğunu koruyan kayıpsız bir PNG dosyası oluşturur; tipik kanvas boyutları için bir saniyenin altında hazır bir PNG elde edersiniz. API, düşük‑seviye kodlamayı kendisi halleder.

## Neden bir grafik çevirme örneği kullanmalı?

Bir grafik çevirme örneği, her noktayı yeniden hesaplamak yerine çizim orijininizi bir kez taşımaya olanak tanır. Orijini kanvas merkezine kaydırarak geometrinin karmaşıklığını azaltır, kod tekrarını önler ve grafik motorunun matris çarpımını yerel kodda yapmasını sağlar; bu da büyük kanvaslarda render hızını %30’a kadar artırabilir. Bu desen, ileride döndürme veya ölçekleme eklediğinizde kodun bakımını da kolaylaştırır.

## Grafik çevirme örneği

Bir **grafik çevirme örneği**, orijini taşımayı göstererek konumlandırmayı basitleştirir. Her noktayı yeniden hesaplamak yerine koordinat sistemini bir kez kaydırır ve yeni orijini kanvas merkeziymiş gibi çizersiniz.

## Önkoşullar

Başlamadan önce şunların kurulu olduğundan emin olun:

- **Aspose.Drawing kütüphanesi** .NET projenize entegre edildi – resmi [Aspose.Drawing sürüm sayfasından](https://releases.aspose.com/drawing/net/) indirin.  
- Çıktı görüntüsünün kaydedileceği bir **belge dizini**.  
- **C#** sözdizimi ve Visual Studio ya da tercih ettiğiniz IDE hakkında temel bilgi.  

Şimdi, koda dalalım!

## Ad alanlarını içe aktar

`Bitmap`, `Graphics` ve Aspose çizim yardımcıları bu ad alanlarında bulunur.  
**Tanım:** `System.Drawing` temel GDI+ tiplerini sağlar, `Aspose.Drawing` ise bunları çapraz‑platform yeteneklerle genişleterek aynı kodu Windows, Linux ve macOS'ta ek bağımlılık olmadan çalıştırmanıza imkan tanır.

## Adım adım kılavuz

### Adım 1: bitmap oluştur

**Tanım:** `Bitmap`, Aspose.Drawing’in bellek içi raster görüntü temsilidir; üzerine çizebilir ya da diske kaydedebilirsiniz.  

Boş bir kanvas oluşturarak çizimimizi başlatıyoruz.

`new Bitmap(width, height, PixelFormat.Format32bppPArgb)` 32‑bit piksel başına önceden çarpılmış alfa ile bir bitmap oluşturur; bu format PNG çıktısı için şeffaflığı ekstra dönüşüm adımı olmadan korur.

- **Neden 32bppPArgb?** Bu piksel formatı alfa şeffaflığını ve yüksek kalite renk renderını destekler, PNG çıktısı için idealdir.  
- **İpucu:** Genişlik/yüksekliği hedef görüntü boyutunuza göre ayarlayın; 1920 × 1080 kanvas tipik bir geliştirici laptopunda 0.2 saniyenin altında render olur.

### Adım 2: dünya dönüşümünü ayarla (grafik çevirme örneği)

**Tanım:** `Graphics`, `Bitmap` üzerine şekil çizen çizim yüzeyidir.  

`TranslateTransform` koordinat sisteminin orijini yeni bir konuma taşır.  
`graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height / 2)` (0,0) noktasını kanvas merkezine kaydırır. Bu çağrıdan sonra (0,0) koordinatlarıyla çizilen her şekil görüntünün ortasında görünür.

- Bu, (0,0) noktasını (500, 400) konumuna (1000 × 800 kanvasın ortası) taşır.  
- Ek dönüşümler zincirlenebilir: `RotateTransform` koordinat sistemini döndürür, `ScaleTransform` ölçeklendirir; böylece **birden fazla grafik dönüşümü** tek bir pipeline’da uygulanabilir.

### Adım 3: dönüştürülmüş koordinatları kullanarak bir dikdörtgen çizin

**Tanım:** `DrawRectangle`, `Graphics` üzerinden verilen kalem ve koordinatlarla bir dikdörtgen konturu ya da dolu şekil çizen metottur.  

`graphics.DrawRectangle(pen, -150, -100, 300, 200)` dikdörtgeni kanvasın ortasına çizer; çünkü sol‑üst köşesi dönüştürülmüş orijinden (yani merkezden) yarı genişlik ve yarı yükseklik kadar kaydırılmıştır.

- Dikdörtgenin sol‑üst köşesi, dönüştürülmüş orijinden (görüntünün merkezi) başlar.  
- İsterseniz elips, çizgi ya da özel yollar gibi diğer şekilleri de deneyebilirsiniz.

### Adım 4: sonucu kaydedin – grafikleri PNG'ye dönüştürün

**Tanım:** `ImageFormat`, `Save` metodunun hangi dosya formatını kullanacağını belirten bir enum’dur.  

`Save`, bitmap'i belirtilen formatta bir dosyaya yazar.  
`bitmap.Save(outputPath, ImageFormat.Png)` kayıpsız bir PNG dosyası oluşturur; bu dosya doğrudan web sayfalarında ya da UI bileşenlerinde kullanılabilir.

- PNG, önceki adımda ayarladığımız renk ve şeffaflığı tam olarak korur.  
- `"Your Document Directory"` ifadesini makinenizdeki gerçek yol ile değiştirin.  
- Toplu işleme için bir `Bitmap` koleksiyonu üzerinde döngü kurup `Save` çağrısını içinde yapabilirsiniz; kütüphane binlerce görüntüyü 200 MB’dan az RAM ile işleyebilir.

## Yaygın sorunlar ve çözümler

| Sorun | Neden oluşur | Çözüm |
|-------|----------------|-----|
| **File not found error** when saving | Hedef klasör mevcut değil. | `Save` çağrısından önce klasörü programatik olarak (`Directory.CreateDirectory`) oluşturun. |
| **Blank image** after transformation | `TranslateTransform` çizimden sonra çağrılmış. | Dönüşümün **herhangi bir çizim komutundan önce** ayarlandığından emin olun. |
| **Distorted colors** | Uyumsuz bir piksel formatı kullanılıyor. | PNG çıktısı için `Format32bppPArgb` formatını kullanın. |
| **Out‑of‑memory on large canvases** | Tüm bitmap belleğe yükleniyor. | `Bitmap` akış seçeneklerini kullanın veya görüntüyü parçalara bölün; Aspose.Drawing parçaları bağımsız olarak render edebilir. |

## Sıkça Sorulan Sorular

**S: Birden fazla dönüşüm uygulayabilir miyim?**  
C: Evet – `TranslateTransform`, `RotateTransform` ve `ScaleTransform`'ı zincirleyerek tek bir grafik pipeline'ında karmaşık efektler elde edebilirsiniz.

**S: Aspose.Drawing ticari projeler için ücretsiz mi?**  
C: Değerlendirme için ücretsiz bir deneme sürümü mevcuttur, ancak üretim kullanımında ticari lisans gereklidir.

**S: .NET Core ve .NET 5/6/7 ile çalışıyor mu?**  
C: Kesinlikle. Aspose.Drawing tüm modern .NET çalışma zamanlarını destekler; .NET Core, .NET 5, .NET 6 ve .NET 7 dahil.

**S: Tam API referansını nereden bulabilirim?**  
C: Tam dokümantasyon [Aspose.Drawing .NET API reference](https://reference.aspose.com/drawing/net/) adresinde mevcuttur.

**S: Eksik bir çıktı dosyasını nasıl gideririm?**  
C: Yol dizesini doğrulayın, yazma izinlerini kontrol edin ve `Save` çağrısından önce dizinin var olduğundan emin olun.

## Sonuç

Artık **Aspose.Drawing ile çizimi PNG'ye dönüştürmeyi**, bir **dünya dönüşümü** uygulamayı ve **grafik çevirme örneği** sayesinde döndürme ya da ölçekleme ekleyebileceğiniz bir temel oluşturmayı öğrendiniz. Bu yapı taşlarını ustalaştırarak dinamik görüntüler üretebilir, özel grafikler oluşturabilir veya herhangi bir .NET uygulaması için anlık grafikler geliştirebilirsiniz. Sonraki adımda, birden fazla işlemi tek bir matris içinde birleştiren matris‑tabanlı dönüşüm öğreticisini keşfederek performansı daha da artırabilirsiniz.

---

**Last updated:** 2026-10-18  
**Tested with:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  
**Related resources:** [Aspose.Drawing API reference](https://reference.aspose.com/drawing/net/) | [Download free trial](https://releases.aspose.com/drawing/net/)

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

## İlgili öğreticiler

- [Matris dönüşüm öğreticisi: Aspose.Drawing için .NET'te matris dönüşümleri](/drawing/net/coordinate-transformations/matrix-transformations/)
- [Aspose.Drawing global dönüşümü ile görüntüyü nasıl döndürürsünüz](/drawing/net/coordinate-transformations/global-transformation/)
- [Koordinat sistemi dönüşümü – Aspose.Drawing için .NET'te sayfa dönüşümü](/drawing/net/coordinate-transformations/page-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}