---
date: 2026-07-22
description: Aspose.Drawing ile bitmap'i PNG olarak kaydetmeyi ve görüntüyü JPEG'ye
  dışa aktarmayı öğrenin. Adım adım rehber, drawing paths, görüntü oluşturmayı ve
  exporting formats gösterir.
keywords:
- save bitmap as png
- export image to jpeg
- Aspose.Drawing graphicspath
- .NET image processing
lastmod: 2026-07-22
linktitle: Aspose.Drawing'de Drawing Paths
og_description: Aspose.Drawing for .NET kullanarak bitmap'i PNG olarak kaydedin ve
  görüntüyü JPEG'ye dışa aktarın. Bu öğreticiyi izleyerek complex paths çizin, high‑quality
  images oluşturun ve multiple formats çıktısı alın.
og_image_alt: 'Guide: Save bitmap as PNG and export JPEG using Aspose.Drawing'
og_title: Bitmap'i PNG Olarak Kaydet – Aspose.Drawing ile Drawing Paths
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to save bitmap as PNG and export image to JPEG with Aspose.Drawing.
    Step‑by‑step guide shows drawing paths, creating images, and exporting formats.
  headline: Save Bitmap as PNG – Using GraphicsPath in Aspose.Drawing
  type: TechArticle
- questions:
  - answer: Absolutely – use `path.AddBezier(...)` to define smooth curves.
    question: Can I draw custom Bezier curves with GraphicsPath?
  - answer: Call `path.Reset()` to remove all figures and start fresh.
    question: How do I clear a GraphicsPath before reusing it?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- save bitmap as png
- Aspose.Drawing
- .NET graphics
- image export
title: Bitmap'i PNG Olarak Kaydet – Aspose.Drawing'de GraphicsPath Kullanarak
url: /tr/net/lines-curves-and-shapes/draw-path/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing'de Yolları Çizme

## GraphicsPath Nasıl Kullanılır – Giriş

**Save bitmap as PNG**, genellikle kayıpsız bir görüntüye ihtiyaç duyduğunuzda ve bunu daha sonra işlemek ya da yayınlamak istediğinizde ilk adımdır. Bu öğreticide `GraphicsPath` ile karmaşık vektör yollarını nasıl çizeceğinizi, bunları bir bitmap üzerine nasıl render edeceğinizi ve ardından **save bitmap as PNG** ya da hatta **export image to JPEG** yapacağınızı öğreneceksiniz. Raporlama motoru, özel bir grafik kütüphanesi oluşturuyor ya da sadece dinamik grafikler üretmeniz gerekiyorsa, Aspose.Drawing, System.Drawing.Common yerine geçen tam yönetilen, çapraz‑platform API sağlar.

## Hızlı Yanıtlar
- **What can I draw with GraphicsPath?** Satırlar, dikdörtgenler, elipsler, eğriler ve özel şekiller.  
- **Do I need a license?** Deneme ücretsizdir; üretim için ticari lisans gereklidir.  
- **Which .NET versions are supported?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6+.  
- **Is System.Drawing.Common required?** Hayır, Aspose.Drawing bağımsız çalışır.  
- **Can I save to different formats?** Evet – PNG, JPEG, BMP, GIF ve daha fazlası.

## GraphicsPath Nedir?

`GraphicsPath`, Aspose.Drawing'in bir vektör konteyneridir ve çizim primitive'lerinin (çizgiler, yaylar ve eğriler gibi) bir dizisini tek bir nesne olarak depolar. Bu primitive'leri gruplayarak dönüşümler, doldurma kuralları ve kenar ayarlarını tutarlı bir şekilde uygulayabilir, bu da karmaşık grafiklerin oluşturulmasını basitleştirir ve farklı çıktı formatları arasında tutarlı render edilmesini sağlar.

## Neden Aspose.Drawing ile GraphicsPath Kullanmalı?
Aspose.Drawing ile GraphicsPath kullanmak, kesin, esnek ve yüksek performanslı vektör çizim yetenekleri sunar. Karmaşık şekiller oluşturmanıza, dönüşümler uygulamanıza ve bunları verimli bir şekilde render etmenize olanak tanır; aynı zamanda çapraz‑platform tutarlılığı sağlar ve büyük ölçekli görüntü işleme destekler. Ayrıca diğer .NET kütüphaneleriyle sorunsuz entegrasyon sağlar, tek bir uygulamada raster ve vektör iş akışlarını birleştirmenize imkan verir.

- **Precision:** 50+ vektör primitive'ini alt‑piksel doğrulukla işler, **save bitmap as PNG** yaptığınızda çıktının her çözünürlükte net kalmasını sağlar.  
- **Flexibility:** Çizgileri, yayları ve Bezier eğrilerini tek bir yola birleştirir, ardından tek bir `Graphics.DrawPath` çağrısıyla render eder.  
- **Performance:** Optimize edilmiş render pipeline'ı, tüm dosyayı belleğe yüklemeden 400 MP'ye kadar görüntüyü işler, büyük ölçekli toplu işleri mümkün kılar.  
- **Cross‑Platform:** Windows, Linux ve macOS çalışma zamanlarında aynı sonuçları verir, platform‑spesifik hataları ortadan kaldırır.

## Ön Koşullar

Öğreticiye başlamadan önce aşağıdaki ön koşulları karşıladığınızdan emin olun:

- **Aspose.Drawing Library:** Aspose.Drawing kütüphanesini indirin ve kurun. Kütüphaneyi [burada](https://releases.aspose.com/drawing/net/) bulabilirsiniz.
- **Other Aspose Products:** Diğer Aspose ürünlerini keşfedin [burada](https://releases.aspose.com/).
- **Development Environment:** Gerekli araçlarla (.NET SDK, Visual Studio vb.) .NET geliştirme ortamınızı kurun.

## Ad Alanlarını İçe Aktarma

Start by importing the required namespaces in your project:

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

## Adım 1: Bitmap ve Graphics Oluşturma

Bitmap, bellekte bir görüntüyü temsil ederken, Graphics bu görüntü üzerine çizim yöntemleri sağlar. Bir `Bitmap` ve bir `Graphics` nesnesi oluşturarak işe başlayın. Bu bitmap, `GraphicsPath`'in render edileceği tuval olacak ve daha sonra **save bitmap as PNG** yapacaksınız:

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

## Adım 2: Pen ve GraphicsPath Tanımlama

Pen, çizgi rengini, kalınlığını ve stilini tanımlar; GraphicsPath ise çizim primitive'lerinin bir koleksiyonunu tek bir vektör nesnesi olarak depolar. Öncelikle çizim özelliklerini belirlemek için bir `Pen` tanımlayın ve bir `GraphicsPath` örneği oluşturun. `GraphicsPath` nesnesi, çizim yapılmadan önce vektör verilerini tutar:

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
GraphicsPath path = new GraphicsPath();
```

## Adım 3: Çizgiler ve Şekiller Ekleme

`AddLine`, `AddRectangle` ve `AddEllipse` ilgili şekilleri GraphicsPath'e ekler ve daha sonra render edilir. `GraphicsPath`'e çizgiler, dikdörtgenler ve elipsler ekleyerek karmaşık bir yol oluşturun. Ayrıca pürüzsüz şekiller için özel Bezier eğrileri ekleyebilirsiniz:

```csharp
path.AddLine(100, 100, 1000, 400);
path.AddLine(1000, 600, 300, 600);
path.AddRectangle(new Rectangle(500, 350, 200, 400));
path.AddEllipse(10, 250, 450, 300);
```

## Adım 4: Yolu Çizme

`DrawPath`, bir GraphicsPath'ten vektör verilerini belirtilen Pen ile Graphics yüzeyine render eder. Belirtilen `Pen` ile `Graphics` nesnesine yolu çizin. Bu işlem, vektör verilerini bitmap tuvaline rasterleştirir:

```csharp
graphics.DrawPath(pen, path);
```

## Adım 5: Görüntüyü Kaydet – PNG veya JPEG Olarak Dışa Aktarma

`Bitmap.Save` yöntemi, görüntüyü PNG veya JPEG gibi seçilen formatta diske yazar. Çizimden sonra **save bitmap as PNG** yaparak kayıpsız kalite elde edebilir veya **export image to JPEG** yaparak daha küçük dosya boyutu elde edebilirsiniz. Senaryonuza en uygun formatı seçin:

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawPath_out.png");
```

Gerekli olduğunda bu adımları tekrarlayarak karmaşık ve görsel açıdan çekici yollar oluşturabilirsiniz.

## Yaygın Sorunlar ve Çözümler

| Sorun | Çözüm |
|-------|----------|
| **Path not visible** | Pen renginin arka planla kontrast oluşturduğundan ve bitmap'in doğru şekilde kaydedildiğinden emin olun. |
| **Unexpected image size** | Bitmap boyutlarını ve piksel formatını gereksinimlerinize uygun olduğundan doğrulayın. |
| **License exception** | Test için deneme lisansı kullanın; üretime dağıtmadan önce geçerli bir lisans uygulayın. |

## Sıkça Sorulan Sorular

### Q1: Aspose.Drawing'ı diğer .NET kütüphaneleriyle kullanabilir miyim?
A1: Evet, Aspose.Drawing diğer .NET kütüphaneleriyle sorunsuz bir şekilde bütünleşir ve geliştirme projelerinizde çok yönlülük sağlar.

### Q2: Ücretsiz deneme sürümü mevcut mu?
A2: Evet, ücretsiz deneme sürümüne [buradan](https://releases.aspose.com/) ulaşabilirsiniz.

### Q3: Aspose.Drawing için destek nereden bulunur?
A3: Yardım ve topluluk desteği için Aspose.Drawing [forumunu](https://forum.aspose.com/c/drawing/44) ziyaret edin.

### Q4: Geçici bir lisansı nasıl alabilirim?
A4: Geçici bir lisansı [buradan](https://purchase.aspose.com/temporary-license/) edinebilirsiniz.

### Q5: Aspose.Drawing'i satın alabilir miyim?
A5: Evet, Aspose.Drawing'i [buradan](https://purchase.aspose.com/buy) satın alabilirsiniz.

**Ekstra Soru & Cevap**

**Q: GraphicsPath ile özel Bezier eğrileri çizebilir miyim?**  
A: Kesinlikle – pürüzsüz eğrileri tanımlamak için `path.AddBezier(...)` kullanın.

**Q: Bir GraphicsPath'i yeniden kullanmadan önce nasıl temizlerim?**  
A: Tüm şekilleri kaldırıp yeniden başlamak için `path.Reset()` çağırın.

## Sonuç

Tebrikler! **how to use GraphicsPath**'i öğrenerek yolları çizmeyi ve ardından Aspose.Drawing for .NET ile **save bitmap as PNG** ya da **export image to JPEG** yapmayı başardınız. Bu öğreticide bir bitmap oluşturma, bir kalem tanımlama, bir `GraphicsPath` inşa etme, çeşitli şekilleri render etme ve son görüntüyü birden fazla formatta dışa aktarma konularını ele aldık. Farklı koordinatlar, renkler ve çizgi kalınlıklarıyla deneyler yaparak Aspose.Drawing'in tam yaratıcı potansiyelini ortaya çıkarın.

---

**Son Güncelleme:** 2026-07-22  
**Test Edilen Versiyon:** Aspose.Drawing 24.12 for .NET  
**Yazar:** Aspose

## İlgili Öğreticiler

- [Bitmap'i PNG Olarak Kaydet & Aspose.Drawing ile Kapalı Eğriler Çiz](/drawing/net/lines-curves-and-shapes/draw-closed-curve/)
- [Bitmap'i C# Olarak Kaydet – Aspose.Drawing ile Bezier Spline'ları Çiz](/drawing/net/lines-curves-and-shapes/draw-bezier-spline/)
- [Aspose.Drawing'de Görüntüyü Kaydetme ve Kardinal Spline'ları Çizme](/drawing/net/lines-curves-and-shapes/draw-cardinal-spline/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}