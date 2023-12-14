---
title: Aspose.Drawing'de Bölgelerin Doldurulması
linktitle: Aspose.Drawing'de Bölgelerin Doldurulması
second_title: Aspose.Drawing .NET API - System.Drawing.Common'a alternatif
description: Bu adım adım eğitimle Aspose.Drawing for .NET'te bölgeleri nasıl dolduracağınızı öğrenin. Grafik tasarım becerilerinizi zahmetsizce geliştirin.
type: docs
weight: 20
url: /tr/net/lines-curves-and-shapes/fill-region/
---
## giriiş

Görsel olarak çekici grafikler oluşturmak genellikle bölgelerin renklerle, desenlerle veya degradelerle doldurulmasını içerir. Aspose.Drawing for .NET, bunu verimli bir şekilde gerçekleştirmek için güçlü araçlar sağlar. Bu derste, .NET uygulamalarındaki grafik işlemlerini kolaylaştıran çok yönlü bir kütüphane olan Aspose.Drawing'i kullanarak bölgeleri doldurma sürecini inceleyeceğiz.

## Önkoşullar

Başlamadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

1.  Aspose.Drawing Kütüphanesi: Aspose.Drawing kütüphanesini indirip yükleyin. Kütüphaneyi ve belgelerini bulabilirsiniz.[Burada](https://reference.aspose.com/drawing/net/).

2. Geliştirme Ortamı: Aspose.Drawing'i projelerinize entegre etmek için Visual Studio gibi bir .NET geliştirme ortamı kurun.

## Ad Alanlarını İçe Aktar

Gerekli ad alanlarını projenize aktararak başlayın. Bu ad alanları Aspose.Drawing ile çalışmak için gereken sınıflara ve yöntemlere erişim sağlar.

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```


Şimdi, açık ve kapsamlı bir anlayış için örnek kodu birden çok adıma ayıralım.

## Adım 1: Bitmap ve Grafik Nesnesi Oluşturun

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

Bu adımda yeni bir bitmap ve üzerine çizilecek bir grafik nesnesi başlatıyoruz.

## Adım 2: GraphicsPath Tanımlayın ve Bölge Oluşturun

```csharp
GraphicsPath path = new GraphicsPath();
path.AddPolygon(new Point[] { new Point(100, 400), new Point(500, 100), new Point(900, 400), new Point(500, 700) });
Region region = new Region(path);
```

Bir dizi noktaya sahip bir çokgen belirterek bir grafik yolu tanımlayın. Bu yolu kullanarak bir bölge oluşturun.

## 3. Adım: Bir İç Bölgeyi Hariç Tut

```csharp
GraphicsPath innerPath = new GraphicsPath();
innerPath.AddRectangle(new Rectangle(300, 300, 400, 200));
region.Exclude(innerPath);
```

Bir iç dikdörtgeni temsil eden başka bir grafik yolu oluşturun ve onu ana bölgenin dışında bırakın.

## Adım 4: Bir Fırça Seçin ve Bölgeyi Doldurun

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Blue));
graphics.FillRegion(brush, region);
```

Bir fırça seçin (bu durumda düz mavi renk) ve önceden tanımlanmış bölgeyi seçilen fırçayla doldurun.

## Adım 5: Ortaya Çıkan Resmi Kaydedin

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\FillRegion_out.png");
```

Son görüntüyü istediğiniz dizine kaydedin.

## Çözüm

Aspose.Drawing for .NET'te bölgeleri doldurmak basit bir işlemdir ve size karmaşık ve görsel olarak çekici grafikler oluşturma esnekliği sağlar. Yaratıcılığınızı ortaya çıkarmak için farklı şekiller, renkler ve desenlerle denemeler yapın.

## SSS'ler

### S1: Aspose.Drawing'i ticari projeler için kullanabilir miyim?

 Cevap1: Evet, Aspose.Drawing hem kişisel hem de ticari projeler için kullanılabilir. Lisans ayrıntıları için şu adresi ziyaret edin:[Burada](https://purchase.aspose.com/buy).

### S2: Ücretsiz deneme sürümü var mı?

 C2: Evet, ücretsiz deneme sürümüne erişebilirsiniz[Burada](https://releases.aspose.com/).

### S3: Aspose.Drawing için nasıl destek alabilirim?

 A3: Ziyaret edin[Aspose.Çizim forumu](https://forum.aspose.com/c/diagram/17) toplumdan ve uzmanlardan yardım almak.

### S4: Aspose.Drawing'i kullanarak dinamik görüntüler oluşturabilir miyim?

A4: Kesinlikle. Aspose.Drawing, .NET uygulamalarınızda görüntüleri dinamik olarak oluşturmanıza ve değiştirmenize olanak sağlar.

### S5: Geçici lisanslar mevcut mu?

 Cevap5: Evet, geçici lisanslar alınabilir[Burada](https://purchase.aspose.com/temporary-license/).