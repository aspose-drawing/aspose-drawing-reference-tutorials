---
date: 2025-12-02
description: Aspose.Drawing ile .NET’te resim kırpmayı öğrenin. Bu resim kırpma öğreticisi,
  kırpılmış resmi nasıl kaydedeceğinizi, bitmap ile nasıl çalışacağınızı ve toplu
  resim kırpmayı nasıl yöneteceğinizi adım adım gösterir.
language: tr
linktitle: How to Crop Image .NET Using Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Aspose.Drawing Kullanarak .NET'te Görüntüyü Nasıl Kırpılır
url: /net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET'te Aspose.Drawing Kullanarak Görüntüyü Kırpma

## Giriş

.NET uygulaması geliştiriyor ve hassas görüntü işleme ihtiyacınız varsa, **görüntüyü nasıl kırpılır** dosyalarını öğrenmek çok önemlidir. Aspose.Drawing, eski System.Drawing.Common kütüphanesine ihtiyaç duymadan **crop image .net** projelerinde size yardımcı olacak zengin, tamamen yönetilen bir API sunar. Bu öğreticide, bir bitmap'i yükleme, kırpma alanını tanımlama, işlemi gerçekleştirme ve sonunda **kırpılmış görüntüyü kaydetme** adımlarını içeren eksiksiz bir uçtan uca örnek göreceksiniz. Sonunda, tek bir resim ya da **batch image cropping** iş akışı olsun, görüntü kırpmayı herhangi bir .NET çözümüne entegre etmeye hazır olacaksınız.

## Hızlı Yanıtlar
- **Hangi kütüphaneyi kullanmalıyım?** .NET için Aspose.Drawing  
- **Herhangi bir görüntü formatını kırpabilir miyim?** Evet—en yaygın formatlar (PNG, JPEG, BMP vb.) desteklenir.  
- **Lisans gerekir mi?** Geliştirme için ücretsiz deneme sürümü yeterlidir; üretim için lisans gereklidir.  
- **Toplu işleme mümkün mü?** Kesinlikle—aynı kodu dosya koleksiyonu üzerinde döngüye alabilirsiniz.  
- **Hangi .NET sürümleri destekleniyor?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.

## “crop image .net” nedir?

Görüntüyü kırpmak, daha büyük bir resimden dikdörtgen bir bölgeyi çıkarmak anlamına gelir. .NET'te bu işlem genellikle bir `Bitmap` nesnesi üzerinde gerçekleştirilir. Aspose.Drawing, platformlar arasında tutarlı çalışan yüksek performanslı grafik ilkelileri sağlayarak süreci basitleştirir.

## Aspose.Drawing ile Görüntü Kırpmayı Neden Kullanmalısınız?

- **Çapraz platform güvenilirliği** – Yerel bağımlılık yok, Windows, Linux ve macOS'ta çalışır.  
- **Zengin piksel formatı desteği** – 32‑bit ARGB, PArgb ve birçok diğer formatı işler.  
- **Performans odaklı** – Büyük görüntüler için optimize edilmiş çizim ve enterpolasyon.  
- **Sorunsuz entegrasyon** – PDF, Slides vb. diğer Aspose ürünleriyle yan yana çalışır.

## Ön Koşullar

Başlamadan önce şunların olduğundan emin olun:

- **Aspose.Drawing Kütüphanesi** – Projenize `Aspose.Drawing` NuGet paketini ekleyin veya [resmi siteden](https://releases.aspose.com/drawing/net/) indirin.  
- **Görüntü klasörü** – Kırpmak istediğiniz kaynak görüntüleri içeren bir dizin. Kod örneklerindeki `"Your Document Directory"` ifadesini makinenizdeki gerçek yol ile değiştirin.

## Ad Alanlarını İçe Aktarma

İlk olarak, çizim sınıflarını içeren ad alanını içe aktarın:

```csharp
using System.Drawing;
```

Bu, `Bitmap`, `Graphics`, `Rectangle` ve diğer temel tipleri kullanmanıza olanak tanır.

## Adım‑Adım Kılavuz

### Adım 1: Bir Bitmap Tuvali Oluşturun (crop image bitmap)

Kırpılmış sonucun tutulacağı boş bir bitmap oluşturuyoruz. Genişlik, yükseklik ve piksel formatını çıkarmak istediğiniz bölgenin boyutuna göre ayarlayın.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

> **İpucu:** `Format32bppPArgb` formatı alfa şeffaflığını korur ve yüksek kaliteli render sağlar.

### Adım 2: Bir Graphics Nesnesi Oluşturun

`Graphics` nesnesi, bitmap tuvaline çizmeyi sağlar. `InterpolationMode` ayarı, kırpma sırasında görüntünün nasıl yeniden örnekleneceğini etkiler.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

> **Pro ipucu:** Ölçeklenmiş görüntülerde daha yumuşak sonuçlar için `InterpolationMode.HighQualityBicubic` kullanın.

### Adım 3: Kaynak Görüntüyü Yükleyin

Kırpmak istediğiniz görüntüyü yükleyin. Yol, belge dizininiz ile dosya adını birleştirir.

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

> **Not:** Aspose.Drawing, PNG, JPEG, BMP, GIF, TIFF ve birçok diğer formatı doğrudan okuyabilir.

### Adım 4: Kaynak ve Hedef Dikdörtgenlerini Tanımlayın

`sourceRectangle`, orijinal görüntünün tutulacak kısmını seçer. Burada sol‑üstten 50 × 40 piksel alanını alıyoruz. `destinationRectangle` ise grafik motoruna kırpılmış bölgeyi yeni bitmap üzerinde nereye yerleştireceğini söyler.

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

> **Neden iki dikdörtgen?** Aynı dikdörtgenleri kullanmak basit bir kırpma yapar. `destinationRectangle`'ı değiştirerek kırpılmış parçayı yeniden konumlandırabilir veya ölçeklendirebilirsiniz.

### Adım 5: Kırpma İşlemini Gerçekleştirin

`DrawImage` yöntemi, seçilen bölgeyi kaynak görüntüden hedef bitmap'e kopyalar.

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

> **Yaygın tuzak:** `Graphics` nesnesinin dispose edilmemesi bitmap dosyasını kilitleyebilir. Yöntem bittiğinde otomatik olarak dispose edeceğiz.

### Adım 6: Kırpılmış Görüntüyü Kaydedin (save cropped image)

Son olarak sonucu diske yazın. Dosya adını ve yolunu ihtiyacınıza göre değiştirin.

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

> **Sonuç:** Belirttiğiniz 50 × 40 piksel bölgeyi içeren yeni bir PNG dosyanız oldu.

## Yaygın Sorunlar & Çözümler

| Sorun | Neden | Çözüm |
|-------|-------|------|
| **Boş çıktı dosyası** | Kaynak dikdörtgen görüntünün dışındadır | `sourceRectangle` koordinat ve boyutlarını kontrol edin. |
| **Bellek dışı istisna** | Çok büyük kaynak görüntüler | Görüntüleri parçalar halinde işleyin veya `using` ifadeleriyle kaynakları hızlıca serbest bırakın. |
| **Yanlış renkler** | Piksel formatı uyuşmazlığı | Kaynak bitmap'in piksel formatını eşleştirin veya `Bitmap.Clone` ile dönüştürün. |

## Sık Sorulan Sorular

**S: Aspose.Drawing ile herhangi bir formatta görüntü kırpabilir miyim?**  
C: Evet, Aspose.Drawing PNG, JPEG, BMP, GIF, TIFF ve birçok diğer formatı destekler; böylece **how to crop image** dosyalarını orijinal tiplerinden bağımsız olarak kırpabilirsiniz.

**S: Gelişmiş kırpma seçenekleri var mı?**  
C: Kesinlikle. Dikdörtgen olmayan kırpmalar için `GraphicsPath` kullanabilir, döndürme ekleyebilir veya renk ayarlamaları için `ImageAttributes` uygulayabilirsiniz.

**S: Tek bir görüntüye birden fazla kırpma işlemi uygulayabilir miyim?**  
C: Evet—`DrawImage` çağrısını farklı kaynak dikdörtgenleriyle tekrarlayın veya karmaşık dönüşümler için bir döngüde zincirleyin.

**S: Aspose.Drawing toplu görüntü kırpmada kullanılabilir mi?**  
C: Evet. Yukarıdaki adımları dosya yolu koleksiyonunuza `foreach` döngüsü içinde sararak onlarca ya da yüzlerce görüntüyü otomatik olarak işleyebilirsiniz.

**S: Aspose.Drawing ile ilgili sorular için nasıl destek alabilirim?**  
C: [Aspose.Drawing Forum](https://forum.aspose.com/c/diagram/17) adresini ziyaret ederek sorular sorabilir, kod paylaşabilir ve topluluk ile ürün mühendislerinden yardım alabilirsiniz.

## Sonuç

Bu öğreticide Aspose.Drawing kullanarak eksiksiz bir **crop image .net** iş akışı gösterdik. Artık **how to crop image** dosyalarını nasıl kırpacağınızı, kesin kaynak dikdörtgenlerini tanımlamayı ve **save cropped image** sonuçlarını nasıl kaydedeceğinizi biliyorsunuz. Bu temellerle **batch image cropping** işlemleri, özel dönüşümler ekleyebilir veya mantığı daha büyük görüntü‑işleme hatlarına entegre edebilirsiniz.

---  

**Son Güncelleme:** 2025-12-02  
**Test Edilen Versiyon:** Aspose.Drawing 24.11 for .NET  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}