---
date: 2026-05-29
description: Aspose.Drawing ile .NET'te PNG kaydetmeyi ve kardinal spline'ları çizmeyi
  öğrenin. Eğriyi PNG olarak kaydedin, pürüzsüz grafikler oluşturun ve bitmap'i dosyaya
  zahmetsizce üretin.
keywords:
- how to save png
- save bitmap to file
- create smooth curve
- draw curve c#
- generate png graphics
linktitle: Aspose.Drawing ile Kardinal Spline Çizme
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn how to save PNG and draw cardinal splines in .NET with Aspose.Drawing.
    Save curve as PNG, create smooth graphics, and generate bitmap to file effortlessly.
  headline: How to Save PNG and Draw Cardinal Splines with Aspose.Drawing
  type: TechArticle
- questions:
  - answer: '`Graphics.DrawCurve` interpolates a series of points into a smooth cardinal
      spline.'
    question: What does the primary method do?
  - answer: PNG via `Bitmap.Save`.
    question: Which format is used to save the image?
  - answer: A trial works for development; a commercial license is required for production.
    question: Do I need a license to save images?
  - answer: Yes, overloads of `DrawCurve` let you specify tension.
    question: Can I change the curve tension?
  - answer: Absolutely – it supports .NET Framework and .NET Core/5/6.
    question: Is Aspose.Drawing compatible with .NET 6+?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Aspose.Drawing ile PNG Kaydetme ve Kardinal Spline Çizme
url: /tr/net/lines-curves-and-shapes/draw-cardinal-spline/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PNG Kaydetme ve Aspose.Drawing ile Kardinal Spline Çizme

## Giriş

Bu öğreticide, Aspose.Drawing for .NET kullanarak pürüzsüz kardinal spline'lar çizerken **PNG kaydetme** yöntemini keşfedeceksiniz. İster bir grafik bileşeni, bir diyagram editörü oluşturuyor olun, ister sadece özel bir eğriyi PNG olarak dışa aktarmanız gerekiyor olsun, aşağıdaki adımlar bir bitmap tuvali oluşturmayı, bir kalemle spline çizmeyi ve sonucu diske kaydetmeyi size gösterir. Ayrıca Aspose.Drawing'in System.Drawing.Common'a güvenilir bir çapraz platform alternatifi olduğunu göreceksiniz.

## Hızlı Yanıtlar
- **Birincil yöntem ne yapar?** `Graphics.DrawCurve` bir dizi noktayı pürüzsüz bir kardinal spline'a ara değer alır.  
- **Görüntüyü kaydetmek için hangi format kullanılır?** PNG, `Bitmap.Save` aracılığıyla.  
- **Görüntüleri kaydetmek için lisansa ihtiyacım var mı?** Geliştirme için deneme sürümü çalışır; üretim için ticari lisans gereklidir.  
- **Eğri gerilimini değiştirebilir miyim?** Evet, `DrawCurve` aşırı yüklemeleri gerilimi belirlemenize izin verir.  
- **Aspose.Drawing .NET 6+ ile uyumlu mu?** Kesinlikle – .NET Framework ve .NET Core/5/6'yı destekler.

## Aspose.Drawing bağlamında “PNG kaydetme” nedir?

PNG kaydetmek, çizdiğiniz bellek içi bitmap'i diskte fiziksel bir PNG dosyasına dönüştürmek anlamına gelir. İşlem, piksel verilerini kayıpsız sıkıştırma kullanarak yazar, tam renkleri ve varsa alfa kanal bilgilerini korur. Aspose.Drawing'in `Bitmap.Save` yöntemi PNG kodlamasını otomatik olarak halleder, böylece format detaylarını kendiniz yönetmeniz gerekmez.

## Neden Aspose.Drawing ile bir kardinal spline çizeriz?

Kardinal spline, kontrol noktalarına yakın bir şekilde akıcı, akışkan bir eğri üretir; bu da veri görselleştirmeleri, UI grafikleri ve özel şekiller için mükemmeldir. Aspose.Drawing **30+ görüntü formatını** destekler ve tüm dosyayı belleğe yüklemeden çok sayfalı grafikler oluşturabilir, bu da size hız ve esneklik sağlar.

## Önkoşullar

- Visual Studio (herhangi bir güncel sürüm) yüklü.  
- Aspose.Drawing for .NET kütüphanesi. Bunu [buradan](https://releases.aspose.com/drawing/net/) indirebilirsiniz.  
- C# programlama temelleri.

## Ad Alanlarını İçe Aktarma

C# dosyanızda, gerekli ad alanını içe aktararak başlayın:

`Aspose.Drawing` ad alanı, `Bitmap`, `Graphics` ve `Pen` gibi tüm temel tipleri içerir.  
```csharp
using Aspose.Drawing;
```
```csharp
using System.Drawing;
```

## Adım 1: Bir Bitmap (Tuval) Oluşturma

İlk olarak, çiziminiz için tuval görevi görecek bir bitmap oluşturun. Bu bitmap, spline'ı **görüntüyü kaydetmeden** önce render edeceğiniz yerdir.

Bitmap, tanımlı piksel formatı ve boyutları olan bellek içi bir görüntüyü temsil eder.  
```csharp
int width = 800;
int height = 600;
Bitmap bitmap = new Bitmap(width, height, PixelFormat.Format32bppPArgb);
```
```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## Adım 2: Bir Graphics Nesnesi Oluşturma

Sonra, bitmap'ten bir `Graphics` nesnesi alın. Bu nesne çizim yüzeyini sağlar.

Graphics, şekiller, metin ve görüntüleri bir bitmap üzerine render etmek için bir çizim yüzeyi sağlar.  
```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.Transparent);
```
```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## Adım 3: Pen Tanımlama ve Eğri Çizme

İstediğiniz renk ve genişlikte bir `Pen` tanımlayın, ardından `DrawCurve` kullanarak kardinal spline'ı çizin. Bu, **pen ile eğri çizme** tekniğini gösterir ve bir **kardinal spline örneği** olarak hizmet eder.

Pen, çizgi ve eğri çizerken kullanılan renk, genişlik ve çizgi stilini kapsar.  
```csharp
Pen pen = new Pen(Color.Blue, 3);
PointF[] points = {
    new PointF(100, 400), new PointF(200, 100),
    new PointF(300, 300), new PointF(400, 150),
    new PointF(500, 350)
};
graphics.DrawCurve(pen, points, 0.5f); // tension = 0.5
```
```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawCurve(pen, new Point[] {
    new Point(10, 700),
    new Point(250, 500),
    new Point(500, 10),
    new Point(750, 500),
    new Point(990, 700)
});
```

## Adım 4: Görüntüyü Kaydetme (Eğriyi PNG Olarak Kaydetme)

Son olarak, bitmap'i bir PNG dosyasına kaydedin. Bu, bu öğreticideki **PNG kaydetme** konusunun özüdür.

Bitmap.Save, görüntüyü belirtilen formatta (örneğin PNG) bir dosyaya yazar.  
```csharp
string outputPath = Path.Combine(Environment.CurrentDirectory, "cardinal-spline.png");
bitmap.Save(outputPath, ImageFormat.Png);
```
```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawCardinalSpline_out.png");
```

> **İpucu:** Platformlar arasında dosya yollarını güvenli bir şekilde oluşturmak için `Path.Combine` kullanın.

Tebrikler! Aspose.Drawing for .NET kullanarak başarılı bir şekilde bir kardinal spline çizdiniz ve sonucu PNG görüntüsü olarak kaydettiniz. Eğrilerinizi özelleştirmek için farklı nokta dizileri, kalem renkleri veya çizgi kalınlıklarıyla denemeler yapabilirsiniz.

## Yaygın Kullanım Senaryoları

- **Veri görselleştirmeleri** – hassas kontrol noktalarına ihtiyaç duyan pürüzsüz çizgi grafikler.  
- **Özel UI bileşenleri** – düğmeler, kaydırıcılar veya dekoratif kenarlıklar çizme.  
- **Dışa aktarılabilir grafikler** – raporlar veya web içeriği için anlık PNG varlıkları oluşturma.

## Sorun Giderme ve İpuçları

- **Görüntü boş mu görünüyor?** Bitmap'in piksel formatının alfa (`Format32bppPArgb`) desteklediğinden ve gerektiğinde `graphics.Clear(Color.Transparent)` çağırdığınızdan emin olun.  
- **Beklenmeyen eğri şekli?** Gerilim parametresini `DrawCurve(pen, points, tension)` aşırı yüklemesiyle ayarlayın.  
- **Dosya erişim hataları?** Hedef dizinin var olduğunu ve uygulamanızın yazma izinlerine sahip olduğunu doğrulayın.

## Sıkça Sorulan Sorular

**S1: Aspose.Drawing'i ticari projelerde kullanabilir miyim?**  
C1: Evet, Aspose.Drawing hem kişisel hem de ticari projeler için uygundur. Lisans detaylarını [satın alma sayfasında](https://purchase.aspose.com/buy) kontrol edin.

**S2: Test amaçlı geçici bir lisans nasıl alabilirim?**  
C2: Test amaçlı geçici bir lisans [buradan](https://purchase.aspose.com/temporary-license/) edinebilirsiniz.

**S3: Ek destek nereden bulabilirim?**  
C3: Topluluk desteği ve tartışmalar için [Aspose.Drawing forumunu](https://forum.aspose.com/c/drawing/44) ziyaret edin.

**S4: Ücretsiz deneme mevcut mu?**  
C4: Evet, satın almadan önce özellikleri [ücretsiz deneme](https://releases.aspose.com/) sürümüyle keşfedebilirsiniz.

**S5: Dokümantasyona nasıl erişebilirim?**  
C5: Ayrıntılı bilgi ve örnekler için kapsamlı [dokümantasyona](https://reference.aspose.com/drawing/net/) bakın.

---

**Son Güncelleme:** 2026-05-29  
**Test Edilen:** Aspose.Drawing 24.11 for .NET  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
