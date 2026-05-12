---
date: 2026-02-12
description: Aspose.Drawing kullanarak .NET uygulamalarında yay çizmeyi öğrenin. Bu
  adım adım rehber, C# ile bitmap oluşturmayı, kalem rengini ayarlamayı, bitmap üzerinde
  yay çizmeyi ve bitmap'i PNG olarak kaydetmeyi gösterir.
linktitle: Drawing Arcs in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Aspose.Drawing ile Yay Çizme
url: /tr/net/lines-curves-and-shapes/draw-arc/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing ile Yay Çizme

## Giriş

Bir .NET projesinde **yay nasıl çizilir** ihtiyacınız varsa, Aspose.Drawing süreci basit ve yüksek performanslı hâle getirir. Bu öğreticide C#'ta bir bitmap oluşturmayı, kalem rengini ayarlamayı, bir yay görüntüsü üretmeyi ve son olarak bitmap'i PNG dosyası olarak kaydetmeyi adım adım göstereceğiz. Raporlama aracı, özel bir UI bileşeni oluşturuyor ya da sadece grafiklerle deneme yapıyor olun, bu adımlar size sağlam bir temel sağlayacaktır.

## Hızlı Yanıtlar
- **.NET'te yay çizmek için en iyi kütüphane hangisidir?** Aspose.Drawing for .NET  
- **Yayı oluşturan yöntem hangisidir?** `Graphics.DrawArc`  
- **Geliştirme için lisansa ihtiyacım var mı?** Test için ücretsiz deneme sürümü yeterlidir; üretim için lisans gereklidir.  
- **Sonucu PNG olarak kaydedebilir miyim?** Evet, `.png` uzantısı ile `Bitmap.Save` kullanın.  
- **Hangi .NET sürümleri destekleniyor?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Aspose.Drawing'da “yay nasıl çizilir” nedir?

Bir yay çizmek, bir elips ya da dairenin eğimli bir segmentini bir grafik yüzeyine çizmektir. Aspose.Drawing, tanıdık `Graphics.DrawArc` metodunu sunar ve sınırlayıcı dikdörtgeni, başlangıç açısını ve süpürme açısını piksel‑tam hassasiyetle tanımlamanıza olanak verir.

## Neden Aspose.Drawing'i yaylar için kullanmalısınız?

- **Cross‑platform consistency** – Windows, Linux ve macOS'ta aynı şekilde çalışır.  
- **No System.Drawing.Common dependency** – Modern .NET Core/5+ uygulamaları için idealdir.  
- **Rich API** – Renkler, çizgi kalınlıkları ve görüntü formatları üzerinde tam kontrol sağlar.  

## Önkoşullar

Before we dive in, make sure you have:

- Visual Studio (herhangi bir güncel sürüm).  
- Aspose.Drawing for .NET – indirmek için [website](https://releases.aspose.com/drawing/net/).  
- Temel C# bilgisi (değişkenler, nesneler ve metod çağrıları).  

## Ad Alanlarını İçe Aktarma

To start, bring the required namespace into scope:

```csharp
using System.Drawing;
```

## Adım‑Adım Kılavuz

### Adım 1: Bir bitmap C# nesnesi oluşturun

İlk olarak, çizimimiz için tuval görevi görecek bir `Bitmap` oluştururuz.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

*Açıklama*: Bitmap boyutu (1000 × 800) bize geniş bir alan sağlar ve piksel formatı yüksek kaliteli alfa karışımını garanti eder.

### Adım 2: Bir kalem ayarlayın ve kalem rengini belirleyin

Şimdi çizginin görünümünü belirleyen bir `Pen` tanımlıyoruz. Burada **kalem rengini** mavi olarak ayarlıyor ve 2 piksel genişliğini seçiyoruz.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
```

`KnownColor.Blue` ifadesini başka bir bilinen renk ya da özel bir `Color.FromArgb` değeriyle değiştirebilirsiniz.

### Adım 3: Bitmap üzerine yay çizin

Grafik yüzeyi ve kalem hazır olduğunda, **bitmap üzerine yay çizebiliriz**.

```csharp
graphics.DrawArc(pen, 0, 0, 700, 700, 0, 180);
```

Parametreler şunlardır:

- `pen` – tanımladığımız stil.  
- `0, 0` – sınırlayıcı dikdörtgenin sol‑üst köşesi.  
- `700, 700` – dikdörtgenin genişlik ve yüksekliği (tam bir daire oluşturur).  
- `0` – derece cinsinden başlangıç açısı.  
- `180` – süpürme açısı, yarım daire yayını üretir.

### Adım 4: Bitmap'i PNG olarak kaydedin

Son olarak, **bitmap'i PNG olarak** diske kaydediyoruz. Yolu, projenizin çıktı klasörüne göre ayarlayın.

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawArc_out.png");
```

Kaydedilen dosya (`DrawArc_out.png`) oluşturulan yay görüntüsünü içerir ve UI, raporlar veya daha ileri işleme için hazırdır.

## Yaygın Sorunlar ve Çözümleri

| Sorun | Çözüm |
|-------|----------|
| **Yay bozulmuş görünüyor** | Gerçek bir daire için genişlik ve yükseklik değerlerinin eşit olduğundan emin olun; aksi takdirde eliptik bir yay elde edersiniz. |
| **Dosya bulunamadı hatası** | Hedef dizinin varlığını doğrulayın veya `Save` çağrısı öncesinde programatik olarak oluşturun. |
| **Renkler Linux'ta farklı görünüyor** | Platformlar arası tutarlı render almak için açık RGBA değerleriyle `Color.FromArgb` kullanın. |

## SSS

### S1: Yayı rengini özelleştirebilir miyim?

**Evet, yapabilirsiniz.** `Pen` nesnesi oluştururken renk parametresini değiştirmeniz yeterlidir.

### S2: Yayın farklı bir başlangıç açısı olmasını istersem ne yapmalıyım?

İhtiyacınıza göre `DrawArc` metodundaki başlangıç açısı parametresini ayarlayın.

### S3: Aspose.Drawing diğer grafik öğeleri için uygun mu?

**Kesinlikle.** Aspose.Drawing, çizgiler, eğriler ve şekiller dahil olmak üzere geniş bir grafik öğe yelpazesini destekler.

### S4: Aspose.Drawing'i diğer .NET kütüphaneleriyle entegre edebilir miyim?

**Evet,** Aspose.Drawing diğer .NET kütüphaneleriyle sorunsuz bir şekilde entegre olur ve geliştirme sürecinizde esneklik sağlar.

### S5: Ek destek veya topluluk tartışmalarını nerede bulabilirim?

Topluluk desteği ve tartışmalar için [Aspose.Drawing forumunu](https://forum.aspose.com/c/drawing/44) ziyaret edin.

## Sık Sorulan Sorular

**S: Bu .NET 6 ve sonrası ile çalışır mı?**  
C: Evet, Aspose.Drawing .NET 6, .NET 7 ve .NET 8 çalışma zamanlarını tam olarak destekler.

**S: Bitmap ne kadar büyük olabilir?**  
C: Boyut yalnızca mevcut bellekle sınırlıdır; çok büyük görüntüler için akış veya döşeme tekniklerini düşünün.

**S: Aynı bitmap üzerinde birden fazla yay çizebilir miyim?**  
C: Kesinlikle—farklı koordinat veya açılarla `graphics.DrawArc` metodunu birden çok kez çağırmanız yeterlidir.

**S: Anti‑aliasing otomatik olarak uygulanıyor mu?**  
C: Çizim öncesinde `graphics.SmoothingMode = SmoothingMode.AntiAlias;` ayarlayarak etkinleştirebilirsiniz.

**S: Kaydettikten sonra kaynakları nasıl serbest bırakırım?**  
C: İşiniz bittiğinde yerel kaynakları serbest bırakmak için `graphics.Dispose();` ve `bitmap.Dispose();` çağırın.

## Sonuç

Artık Aspose.Drawing kullanarak **yay nasıl çizilir** konusunu biliyorsunuz; bitmap C# nesnesi oluşturma, kalem rengini ayarlama, yay görüntüsü üretme ve sonucu PNG olarak kaydetme adımlarını uyguladınız. Farklı açı, renk ve çizgi kalınlıklarıyla deneyler yaparak uygulamalarınızı zenginleştiren özel grafikler oluşturabilirsiniz.

---

**Son Güncelleme:** 2026-02-12  
**Test Edilen Sürüm:** Aspose.Drawing 24.11 for .NET  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}