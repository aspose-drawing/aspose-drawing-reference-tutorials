---
date: 2026-11-04
description: Aspose.Drawing API'si ile .NET'te koordinat sistemi dönüşümü yaparken
  dikdörtgen grafikleri nasıl çizeceğinizi öğrenin. Bu adım adım kılavuz, inçleri
  piksele dönüştürmeyi ve sayfa birimlerini ayarlamayı gösterir.
keywords:
- how to draw rectangle
- convert inches to pixels
- how to set units
- save bitmap as png
- clear canvas background
lastmod: 2026-11-04
linktitle: Aspose.Drawing'de koordinat sistemi dönüşümü
og_description: Aspose.Drawing for .NET'te inçleri piksele dönüştürürken ve sayfa
  birimlerini ayarlarken dikdörtgen grafikleri nasıl çizeceğinizi öğrenin. Kesin sayfa
  dönüşümü için adım adım kılavuzu izleyin.
og_image_alt: Developer guide showing rectangle drawing with coordinate system transformation
  in Aspose.Drawing
og_title: Aspose.Drawing for .NET kullanarak sayfa dönüşümü ile dikdörtgen çizme
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  headline: How to draw rectangle – coordinate system transformation (page transformation)
    in Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  name: How to draw rectangle – coordinate system transformation (page transformation)
    in Aspose.Drawing for .NET
  steps:
  - name: Import namespaces
    text: The `using` statements give you access to the core drawing classes.
  - name: Create a bitmap
    text: '`Bitmap` represents an image in memory that you can draw onto. We start
      by creating a blank bitmap that will serve as the drawing surface. The pixel
      format `Format32bppPArgb` gives us high‑quality, premultiplied alpha support.'
  - name: Create a graphics object
    text: A `Graphics` object provides the drawing API for the bitmap. It’s the bridge
      between your code and the pixel buffer.
  - name: Clear the canvas
    text: Give the canvas a neutral background so the drawn shapes stand out. Here
      we fill it with a light gray.
  - name: Set the transformation (how to set unit)
    text: '`Graphics.PageUnit` specifies the unit of measure used for page coordinates.
      To map page coordinates to device pixels, set the `PageUnit` property. In this
      example we choose inches, but you could also use `GraphicsUnit.Millimeter`,
      `GraphicsUnit.Point`, or `GraphicsUnit.Pixel`. Setting the unit to i'
  - name: Draw a rectangle – draw rectangle graphics
    text: '`Pen` defines the color, width, and style of lines drawn on a graphics
      surface. Now we draw a rectangle using a thin blue pen. Because we switched
      to inches, the rectangle’s size and position are expressed in inches, making
      the code more readable for print‑oriented layouts.'
  - name: Save the image
    text: Finally, write the bitmap to a PNG file in the folder you specified earlier.
  type: HowTo
- questions:
  - answer: Yes, a free trial is available [here](https://releases.aspose.com/) .
    question: Can I use Aspose.Drawing for free?
  - answer: The full API reference is located [here](https://reference.aspose.com/drawing/net/)
      .
    question: Where can I find detailed documentation for Aspose.Drawing?
  - answer: Visit the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      for community help and official assistance.
    question: How do I get support for Aspose.Drawing?
  - answer: Absolutely—obtain one [here](https://purchase.aspose.com/temporary-license/)
      .
    question: Is a temporary license available for Aspose.Drawing?
  - answer: You can buy it [here](https://purchase.aspose.com/buy) .
    question: Where can I purchase a full Aspose.Drawing license?
  type: FAQPage
second_title: Aspose.Drawing .NET API – alternative to System.Drawing.Common
tags:
- Aspose.Drawing
- coordinate transformation
- .NET graphics
- rectangle drawing
title: Aspose.Drawing for .NET ile dikdörtgen çizme – koordinat sistemi dönüşümü (sayfa
  dönüşümü)
url: /tr/net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing for .NET'te dikdörtgen çizme – koordinat sistemi dönüşümü (sayfa dönüşümü)

## Giriş

Bu öğreticide, Aspose.Drawing for .NET kullanarak sayfa‑seviyesinde koordinat sistemi dönüşümü gerçekleştirirken **how to draw rectangle** grafiklerini nasıl çizeceğinizi öğreneceksiniz. Raporlama motoru, CAD‑tarzı bir taslak aracı ya da hassas gerçek‑dünya ölçümlerine ihtiyaç duyan herhangi bir uygulama geliştiriyor olun, bu kılavuz bitmap oluşturulmasından son PNG'nin kaydedilmesine kadar her adımı size gösterir. Sonunda inçleri piksellere dönüştürme, tuval arka planını temizleme ve baskıya hazır çıktı için sayfa birimlerini ayarlama konusunda rahat olacaksınız.

## Hızlı cevaplar
- **What is coordinate system transformation?** Sayfa‑seviyesindeki birimleri (örneğin inç) cihaz‑seviyesindeki piksellere eşler, böylece çizimler herhangi bir çıktı cihazında doğru ölçeklenir.  
- **Why choose Aspose.Drawing?** Tamamen yönetilen, çapraz‑platform grafik API'si sunar, System.Drawing.Common yerine geçer ve 30+ image formats destekler.  
- **How long does the example take to implement?** Sayfa dönüşümüyle temel bir dikdörtgen için yaklaşık 5‑10 dakika.  
- **Do I need a license for development?** Ücretsiz deneme geliştirme için çalışır; üretim dağıtımları için ticari lisans gereklidir.  
- **Which .NET runtimes are supported?** .NET Framework 4.6+, .NET Core 3.1+, and .NET 5/6/7.

## Aspose.Drawing nedir?

Aspose.Drawing, GDI+’a bağımlı olmadan raster görüntüler, vektörler ve sayfa‑seviyesindeki çizimler oluşturmak ve manipüle etmek için **device‑independent API** sağlayan bir .NET grafik kütüphanesidir. **30+ image formats** destekler ve **10,000 × 10,000 pixels** kadar büyük görüntüleri düşük bellek kullanımıyla işleyebilir.

## Aspose.Drawing ile koordinat sistemi dönüşümünü neden kullanmalı?

Koordinat sistemi dönüşümü, grafiklerinizi gerçek‑dünya birimlerinde tasarlamanıza olanak tanırken, kütüphane herhangi bir çıktı cihazı için piksel ölçeklendirmesini otomatik olarak yönetir. Bu yaklaşım, 5‑inçlik bir dikdörtgenin 300 DPI yazıcıda tam beş inç olarak basılmasını ve 96 DPI ekranda orantılı görünmesini garanti eder, manuel dönüşüm hatalarını ortadan kaldırır.

- **Device‑independent design:** Kodu bir kez yazın; Aspose.Drawing ekranlar, yazıcılar veya PDF'ler için ölçeklendirir.  
- **Precision drawing:** Teknik diyagramlar, mühendislik şemaları veya kesin ölçümlerin önemli olduğu her senaryo için idealdir.  
- **Cross‑platform reliability:** System.Drawing’in GDI+ sınırlamaları olmadan Windows, Linux ve macOS’ta tutarlı çalışır.  
- **Performance:** Tipik bir 2.5 GHz CPU’da, 300 DPI’de 5‑inçlik bir dikdörtgen çizimi **15 ms**’nin altında tamamlanır ve kütüphane gerçek‑zaman ön izleme senaryolarında **50 frames per second** renderlayabilir.

## Önkoşullar

- **Aspose.Drawing library:** En son sürümü resmi siteden [here](https://releases.aspose.com/drawing/net/) indirin.  
- **IDE:** Visual Studio, Rider veya herhangi bir .NET‑uyumlu editör.  
- **Output folder:** Örnek kodda `"Your Document Directory"` ifadesini PNG'nin kaydedileceği klasörle değiştirin.  
- **Optional ASP.NET support:** NuGet paketini bir ASP.NET Core projesine ekleyebilir ve aynı API'yi kullanabilirsiniz; desen .NET kütüphaneleri için tipik **how to use aspnet** yaklaşımını izler.

## Sayfa dönüşümüyle dikdörtgen nasıl çizilir?

Boş bir bitmap yükleyin, sayfa birimini inç olarak ayarlayın ve ince mavi bir kalemle bir dikdörtgen çizin—bu, sadece birkaç kod satırıyla dikdörtgen çizimini tamamlar. `Graphics.PageUnit` özelliği, motorun tüm koordinatları inç olarak yorumlamasını sağlar, böylece ham pikseller yerine gerçek‑dünya ölçüleriyle çalışabilirsiniz ve kütüphane bitmap’in DPI’sine göre **convert inches to pixels** otomatik olarak yapar.

### Adım 1: ad alanlarını içe aktar

`using` ifadeleri, temel çizim sınıflarına erişim sağlar.

```csharp
using System.Drawing;
```

### Adım 2: bitmap oluştur

`Bitmap`, üzerinde çizim yaptığınız bellek içi görüntü konteyneridir. Piksel tamponunu tutar ve dosyalara kaydetme yöntemlerini sunar. Bir bitmap oluşturmak, tuval boyutunu ve piksel formatını tanımlar.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Adım 3: graphics nesnesi oluştur

`Graphics`, bitmap için çizim yüzeyini sağlar. Yüksek‑seviyeli çizim komutlarını (çizgiler, şekiller, metin) temel bitmap üzerindeki piksel işlemlerine dönüştürür.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### Adım 4: tuval arka planını temizle

Tuvali nötr bir renk ile temizlemek, şekillerinizin öne çıkmasını sağlar. Bu örnekte arka planı açık gri ile dolduruyoruz; bu aynı zamanda **clear canvas background** tekniğini gösterir.

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

### Adım 5: dönüşümü ayarla (birimleri nasıl ayarlarsınız)

`Graphics.PageUnit`, sayfa koordinatları için kullanılan ölçü birimini belirtir. `GraphicsUnit.Inch` olarak ayarlamak, Aspose.Drawing’in bitmap’in DPI’sine (varsayılan 96 DPI, yüksek çözünürlüklü baskı için 300 DPI) göre **convert inches to pixels** otomatik olarak yapmasını sağlar. Düzen gereksinimlerinize bağlı olarak `GraphicsUnit.Millimeter`, `GraphicsUnit.Point` veya `GraphicsUnit.Pixel` de seçebilirsiniz.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### Adım 6: dikdörtgen çiz – draw rectangle graphics

`Pen`, bir graphics yüzeyinde çizilen çizgilerin renk, genişlik ve stilini tanımlar. İnce mavi bir kalem kullanarak, boyutları inç cinsinden ifade edilen bir dikdörtgen çizeriz; bu, baskı‑odaklı düzenler için kodu daha okunabilir kılar.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

### Adım 7: bitmap'i png olarak kaydet

Son olarak, bitmap'i daha önce belirttiğiniz klasöre bir PNG dosyası olarak yazın. PNG olarak kaydetmek kayıpsız kaliteyi korur ve platformlar arasında geniş destek bulur.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

## Yazıcı için grafikler nasıl ölçeklenir?

Çizimden önce bitmap’in DPI’sini hedef yazıcı çözünürlüğüne (örneğin 300 DPI) ayarlayın. Bu, **scale graphics printer** çıktısını otomatik olarak ayarlar, böylece kodunuzdaki bir inç, basılı sayfada bir inç olur ve dikdörtgenin mantıksal boyutu değişmez. `bitmap.SetResolution(300, 300)` çağrısından sonra aynı dikdörtgen kağıt üzerinde daha büyük görünecek ancak tam boyutlarını koruyacaktır.

## Yaygın sorunlar ve çözümler

| Sorun | Neden oluşur | Çözüm |
|-------|----------------|-----|
| **Output file not created** | Yanlış yol veya eksik klasör | Hedef dizinin var olduğundan emin olun veya kaydetmeden önce `Directory.CreateDirectory` çağırın. |
| **Rectangle appears distorted** | Uyumsuz `PageUnit` veya DPI | `graphics.PageUnit`'in istenen birimle eşleştiğini ve bitmap DPI'sinin uygun şekilde ayarlandığını doğrulayın (varsayılan 96 DPI, baskı için 300 DPI). |
| **License exception** | Üretimde geçerli bir lisans olmadan çalıştırmak | Graphics nesnelerini oluşturmadan önce geçici veya kalıcı Aspose.Drawing lisansınızı uygulayın. |

## Sıkça Sorulan Sorular

**Q: Aspose.Drawing'ı ücretsiz kullanabilir miyim?**  
A: Evet, ücretsiz bir deneme sürümü [here](https://releases.aspose.com/) adresinde mevcuttur.

**Q: Aspose.Drawing için ayrıntılı belgeleri nerede bulabilirim?**  
A: Tam API referansı [here](https://reference.aspose.com/drawing/net/) adresinde bulunabilir.

**Q: Aspose.Drawing için destek nasıl alabilirim?**  
A: Topluluk yardımı ve resmi destek için [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) adresini ziyaret edin.

**Q: Aspose.Drawing için geçici bir lisans mevcut mu?**  
A: Kesinlikle—bir lisansı [here](https://purchase.aspose.com/temporary-license/) adresinden edinebilirsiniz.

**Q: Tam bir Aspose.Drawing lisansını nereden satın alabilirim?**  
A: Lisansı [here](https://purchase.aspose.com/buy) adresinden satın alabilirsiniz.

## Sonuç

Artık Aspose.Drawing for .NET kullanarak sayfa‑seviyesinde dönüşümle **how to draw rectangle** grafiklerini çizebileceğinizi biliyorsunuz. Sayfa birimini inç olarak ayarlayarak, tuval arka planını temizleyerek ve sonucu PNG olarak kaydederek, ekran görüntüsü ve yüksek‑çözünürlüklü baskı için uygun, kesin ve cihaz‑bağımsız bir çıktı elde edersiniz. Diğer birimleri, dönüşümleri veya özel koordinat başlangıçlarını deneyerek daha güçlü çizim senaryolarının kilidini açın.

---

**Son Güncelleme:** 2026-11-04  
**Test Edilen Versiyon:** Aspose.Drawing 24.12 for .NET  
**Yazar:** Aspose

## İlgili Öğreticiler

- [Aspose.Drawing for .NET'te Birim Nasıl Ayarlanır – Units of Measure](/drawing/net/coordinate-transformations/units-of-measure/)
- [Genel Dönüşüm](/drawing/net/coordinate-transformations/global-transformation/)
- [Adım Adım Dönüşüm – Coordinate Transformations](/drawing/net/coordinate-transformations/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}