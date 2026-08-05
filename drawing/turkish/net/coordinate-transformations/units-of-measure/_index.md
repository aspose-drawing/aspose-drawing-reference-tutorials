---
date: 2026-05-24
description: Aspose.Drawing for .NET’te birimi nasıl ayarlayacağınızı öğrenin, grafik
  birimlerini kolayca dönüştürün ve grafik işleme için hassas ölçümleri ustalaşın.
keywords:
- how to set unit
- convert graphics units
- Aspose.Drawing units of measure
linktitle: Aspose.Drawing’de Ölçü Birimleri
schemas:
- author: Aspose
  dateModified: '2026-05-24'
  description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  headline: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  type: TechArticle
- description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  name: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  steps:
  - name: Create a Bitmap
    text: The `Bitmap` class represents an in‑memory image that serves as a drawing
      canvas.
  - name: Create a Graphics Object
    text: '`Graphics` provides drawing methods for rendering shapes and text onto
      a `Bitmap`.'
  - name: Set Page Unit to Points
    text: '`PageUnit` is an enumeration that specifies the unit of measure for page
      coordinates. `PageUnit.Point` defines points as the unit of measure (1 point
      = 1/72 inch). This setting applies to all subsequent drawing calls.'
  - name: Draw a Rectangle in Points
    text: When you draw a rectangle after setting the unit, the dimensions you specify
      are interpreted as points, ensuring precise sizing.
  - name: Set Page Unit to Millimeters
    text: Assign `PageUnit.Millimeter` to the `Graphics` object; all coordinates now
      map to the metric system.
  - name: Draw a Rectangle in Millimeters
    text: The rectangle’s width and height are now expressed in millimeters, making
      it easy to align with physical measurements and ensuring that printed output
      matches real‑world sizes.
  - name: Set Page Unit to Inches
    text: '`PageUnit.Inch` changes the coordinate system so that 1 unit equals 1 inch,
      providing a straightforward way to size elements for print‑oriented layouts.
      CODE_BLOCK_PLACEHOLDER_10_END'
  - name: Draw a Rectangle in Inches
    text: Now any shape you draw uses inches as its measurement base, which is ideal
      for print layouts and for communicating dimensions to stakeholders accustomed
      to imperial units. CODE_BLOCK_PLACEHOLDER_11_END
  type: HowTo
- questions:
  - answer: Call `graphics.PageUnit = PageUnit.Point` (or `.Millimeter`, `.Inch`)
      on the `Graphics` object.
    question: What is the primary way to change units?
  - answer: Points.
    question: Which unit equals 1/72 inch?
  - answer: 25.4 mm = 1 inch.
    question: How many millimeters are in an inch?
  - answer: No, the Aspose.Drawing core library provides all unit constants.
    question: Do I need extra libraries to use units?
  - answer: Set the unit once per `Graphics` instance; draw everything using that
      unit for consistency.
    question: Can I mix units in one image?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Aspose.Drawing for .NET’te Birim Nasıl Ayarlanır – Ölçü Birimleri
url: /tr/net/coordinate-transformations/units-of-measure/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing for .NET'te Birimi Ayarlama – Ölçü Birimleri

## Giriş

Aspose.Drawing for .NET dünyasına hoş geldiniz, burada hassasiyet ve esneklik grafik manipülasyonunda buluşur. Bu öğreticide çizimleriniz için **birimin nasıl ayarlanacağını** keşfedecek, **grafik birimlerini** nokta, milimetre ve inç arasında dönüştürmeyi öğrenecek ve görüntülerinizi piksel mükemmel hale getiren gerçek dünya örneklerini göreceksiniz. Raporlar, küçük resimler veya özel grafikler oluşturuyor olun, ölçü birimlerinde uzmanlaşmak cihazlar arasında tutarlı render alma için gereklidir.

## Hızlı Yanıtlar
- **Birimleri değiştirmek için birincil yöntem nedir?** `Graphics` nesnesinde `graphics.PageUnit = PageUnit.Point` (veya `.Millimeter`, `.Inch`) çağırın.  
- **Hangi birim 1/72 inç eşittir?** Noktalar.  
- **Bir inçte kaç milimetre vardır?** 25.4 mm = 1 inç.  
- **Birimleri kullanmak için ekstra kütüphanelere ihtiyacım var mı?** Hayır, Aspose.Drawing çekirdek kütüphanesi tüm birim sabitlerini sağlar.  
- **Bir görüntüde birimleri karıştırabilir miyim?** Birim, `Graphics` örneği başına bir kez ayarlanır; tutarlılık için tüm çizimleri o birimle yapın.

## Önkoşullar

Before we dive into the tutorial, make sure you have the following prerequisites in place:

- Aspose.Drawing for .NET: Kütüphanenin yüklü olduğundan emin olun. Bunu [buradan](https://releases.aspose.com/drawing/net/) indirebilirsiniz.
- Document Directory: Oluşturduğunuz belgeleri kaydetmek istediğiniz belirlenmiş bir dizine sahip olun.
- Basic C# Knowledge: Bu rehberden en iyi şekilde yararlanmak için C#'a temel bir anlayış önerilir.

## Ad Alanlarını İçe Aktarma

Before we start, let's import the necessary namespaces to use Aspose.Drawing effectively:

```csharp
using System.Drawing;
```

Şimdi, her örneği birden fazla adıma ayıralım:

## Birimi Noktalara (Points) Ayarlama

`Bitmap` sınıfı, bir çizim tuvali olarak hizmet veren bellek içi bir görüntüyü temsil eder. Bitmap'inizi yükleyin, bir `Graphics` nesnesi oluşturun ve sayfa birimini noktalara ayarlayın — bu, Aspose.Drawing'in tüm koordinatları 1/72 inç değeri olarak yorumlamasını sağlar. Noktaları kullanmak, baskıya hazır grafikler için ince ayarlı kontrol sağlar ve çizgi kalınlıklarını yüksek hassasiyetle belirlemenize olanak tanır.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Adım 1: Bitmap Oluşturma  
`Bitmap` sınıfı, bir çizim tuvali olarak hizmet veren bellek içi bir görüntüyü temsil eder.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### Adım 2: Graphics Nesnesi Oluşturma  
`Graphics`, bir `Bitmap` üzerine şekil ve metin çizmek için çizim metodları sağlar.

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

### Adım 3: Sayfa Birimini Noktalara Ayarlama  
`PageUnit`, sayfa koordinatları için ölçü birimini belirten bir enum'dur. `PageUnit.Point`, ölçü birimi olarak noktaları tanımlar (1 nokta = 1/72 inç). Bu ayar, sonraki tüm çizim çağrılarına uygulanır.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

### Adım 4: Noktalarda Bir Dikdörtgen Çizin  
Birim ayarlandıktan sonra bir dikdörtgen çizdiğinizde, belirttiğiniz boyutlar nokta olarak yorumlanır ve kesin boyutlandırma sağlanır.

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

## Birimi Milimetrelere (Millimeters) Ayarlama

`PageUnit`, sayfa koordinatları için ölçü birimini belirten bir enum'dur. Milimetrelere geçmek, metrik boyutlara ihtiyacınız olduğunda faydalıdır; örneğin mühendislik diyagramları oluştururken. Aspose.Drawing, 1 mm'yi 1/25.4 inç olarak kabul eder ve grafiklerinizi üretim ve teknik dokümantasyonda kullanılan fiziksel ölçümlerle hizalamanıza olanak tanır.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

### Adım 1: Sayfa Birimini Milimetrelere Ayarlama  
`Graphics` nesnesine `PageUnit.Millimeter` atayın; tüm koordinatlar artık metrik sisteme göre haritalanır.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### Adım 2: Milimetre Cinsinden Bir Dikdörtgen Çizin  
Dikdörtgenin genişliği ve yüksekliği artık milimetre cinsinden ifade edilir, bu da fiziksel ölçümlerle hizalamayı kolaylaştırır ve basılı çıktının gerçek dünya boyutlarıyla eşleşmesini sağlar.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## Birimi İnçlere (Inches) Ayarlama

`Graphics`, bir `Bitmap` üzerine şekil ve metin çizmek için çizim metodları sağlar. İnç, birçok ABD‑tabanlı tasarım aracının varsayılan birimidir. Birimi inç olarak ayarlamak, UI öğelerini düzenlerken tanıdık terimlerle düşünmenizi sağlar ve ekran tasarımından inçlerin yaygın olarak kullanıldığı baskıya geçişi basitleştirir.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

### Adım 1: Sayfa Birimini İnçlere Ayarlama  
`PageUnit.Inch`, koordinat sistemini değiştirir ve 1 birim = 1 inç olur, bu da baskı odaklı düzenler için öğeleri boyutlandırmanın basit bir yolunu sunar.

CODE_BLOCK_PLACEHOLDER_10_END

### Adım 2: İnç Cinsinden Bir Dikdörtgen Çizin  
Şimdi çizdiğiniz her şekil, ölçüm temeli olarak inç kullanır; bu, baskı düzenleri ve imparatorluk birimlerine alışkın paydaşlara boyutları iletmek için idealdir.

CODE_BLOCK_PLACEHOLDER_11_END

## Sonucu Kaydet

Örnekleri tamamladıktan sonra, oluşan görüntüyü belge dizininize kaydedin. `Bitmap.Save` yöntemi, belirttiğiniz formatta (PNG, JPEG vb.) dosyayı yazar.

CODE_BLOCK_PLACEHOLDER_12_END

Artık Aspose.Drawing for .NET'te çeşitli ölçü birimlerini başarıyla yönettiniz ve nokta, milimetre ve inç kullanarak dikdörtgenlerin görsel temsillerini oluşturdunuz.

## Neden Aspose.Drawing'in birim sistemini kullanmalısınız?

Aspose.Drawing, **30+ görüntü formatını** destekler ve **5000 × 5000 piksel**'e kadar olan görüntüleri tüm dosyayı belleğe yüklemeden işleyebilir, büyük ölçekli grafik üretimi için yüksek performans sağlar. Birimi açıkça ayarlayarak, tahminleri ortadan kaldırır, dönüşüm hatalarını azaltır ve çıktınızın tüm platformlarda tam fiziksel boyutlarla eşleşmesini sağlarsınız.

## Yaygın Sorunlar ve Çözümler

- **Kaydetme sonrası beklenmeyen boyut** – `graphics.PageUnit`'i herhangi bir çizim çağrısından **önce** ayarladığınızdan emin olun; birimi daha sonra değiştirmek mevcut şekilleri geriye dönük olarak yeniden boyutlandırmaz.  
- **Yüksek DPI ekranlarda bulanık çıktı** – Hedef DPI'ye uygun olması için bitmap'in çözünürlüğünü artırın (ör. `new Bitmap(width, height, 300)`).  
- **Bir görüntüde karışık birimler** – Her birim için ayrı `Graphics` örnekleri oluşturun veya çizmeden önce manuel dönüşüm yapın.

## Sıkça Sorulan Sorular

### Q1: Aspose.Drawing for .NET'i diğer .NET çerçeveleriyle kullanabilir miyim?
A1: Evet, Aspose.Drawing çeşitli .NET çerçeveleriyle uyumludur ve geliştirme ortamınızda esneklik sağlar.

### Q2: Ücretsiz deneme mevcut mu?
A2: Evet, Aspose.Drawing'i ücretsiz deneme ile keşfedebilirsiniz [burada](https://releases.aspose.com/).

### Q3: Aspose.Drawing for .NET için destek nasıl alabilirim?
A3: Topluluk desteği ve tartışmalar için [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)'u ziyaret edin.

### Q4: Kısa vadeli projeler için geçici lisans satın alabilir miyim?
A4: Evet, geçici bir lisansı [buradan](https://purchase.aspose.com/temporary-license/) edinebilirsiniz.

### Q5: Aspose.Drawing için ayrıntılı belgeleri nerede bulabilirim?
A5: Kapsamlı dokümantasyon [burada](https://reference.aspose.com/drawing/net/) mevcuttur.

---

**Son Güncelleme:** 2026-05-24  
**Test Edilen:** Aspose.Drawing 24.11 for .NET  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
