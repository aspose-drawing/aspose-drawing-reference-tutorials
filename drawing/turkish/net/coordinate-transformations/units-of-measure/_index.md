---
title: Aspose.Drawing for .NET'te Ölçü Birimleri
linktitle: Aspose.Drawing'de Ölçü Birimleri
second_title: Aspose.Drawing .NET API - System.Drawing.Common'a alternatif
description: Hassas grafikler için ölçü birimleri konusunda uzmanlaşan bu ayrıntılı eğitimde Aspose.Drawing for .NET'in çok yönlülüğünü keşfedin.
weight: 14
url: /tr/net/coordinate-transformations/units-of-measure/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing for .NET'te Ölçü Birimleri

## giriiş

Hassasiyet ve esnekliğin grafik manipülasyonunda buluştuğu Aspose.Drawing for .NET dünyasına hoş geldiniz. Bu derste Aspose.Drawing'deki ölçü birimlerinin inceliklerini inceleyeceğiz ve bu olağanüstü kütüphanenin gücünden yararlanmanız için size adım adım bir kılavuz sunacağız.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

-  Aspose.Drawing for .NET: Kütüphanenin kurulu olduğundan emin olun. İndirebilirsin[Burada](https://releases.aspose.com/drawing/net/).

- Belge Dizini: Oluşturduğunuz belgelerinizi kaydetmek istediğiniz belirlenmiş bir dizine sahip olun.

- Temel C# Bilgisi: Bu kılavuzdan en iyi şekilde yararlanmak için temel C# anlayışı önerilir.

## Ad Alanlarını İçe Aktar

Başlamadan önce Aspose.Drawing'i etkili bir şekilde kullanmak için gerekli ad alanlarını içe aktaralım:

```csharp
using System.Drawing;
```

Şimdi her örneği birden fazla adıma ayıralım:

## Ölçü Birimi Olarak Noktalar

1. Bitmap Oluşturun: Belirtilen genişlik ve yüksekliğe sahip bir bitmap başlatın.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

2. Grafik Oluştur: Üzerinde çizim yapmak için bitmap'ten bir Grafik nesnesi oluşturun.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

3. Sayfa Birimini Noktalara Ayarla: Noktaları ölçü birimi olarak tanımlayın (1 nokta = 1/72 inç).

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

4. Dikdörtgen Çiz: Birim olarak noktaları kullanarak bir dikdörtgen çizin.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

## Ölçü Birimi Olarak Milimetre

1. Sayfa Birimini Milimetre Olarak Ayarla: Ölçü birimini milimetre olarak değiştirin (1 mm = 1/25,4 inç).

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

2. Milimetre cinsinden Dikdörtgen Çiz: Birim olarak milimetreyi kullanarak başka bir dikdörtgen çizin.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

## Ölçü Birimi Olarak İnç

1. Sayfa Birimini İnç Olarak Ayarla: Ölçü birimini inç olarak değiştirin.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

2. İnç cinsinden Dikdörtgen Çiz: Birim olarak inç kullanarak bir dikdörtgen çizin.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## Sonucu Kaydet

Örnekleri tamamladıktan sonra ortaya çıkan görüntüyü belge dizininize kaydedin:

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

Artık Aspose.Drawing for .NET'teki çeşitli ölçü birimleri arasında başarıyla gezinerek nokta, milimetre ve inç kullanarak dikdörtgenlerin görsel bir temsilini oluşturdunuz.

## Çözüm

Bu eğitimde Aspose.Drawing for .NET'in farklı ölçü birimlerini nasıl işlediğini inceledik. Noktaları, milimetreleri ve inçleri değiştirerek grafik yaratımlarınızda hassasiyet ve uyarlanabilirlik elde edebilirsiniz. Aspose.Drawing'in tüm potansiyelini ortaya çıkarmak için bu konseptleri deneyin.

## SSS'ler

### S1: Aspose.Drawing for .NET'i diğer .NET çerçeveleriyle kullanabilir miyim?

C1: Evet, Aspose.Drawing çeşitli .NET çerçeveleriyle uyumludur ve geliştirme ortamınıza esneklik sağlar.

### S2: Ücretsiz deneme sürümü var mı?

 Cevap2: Evet, Aspose.Drawing'i ücretsiz deneme sürümüyle keşfedebilirsiniz[Burada](https://releases.aspose.com/).

### S3: Aspose.Drawing for .NET desteğini nasıl alabilirim?

 A3: Ziyaret edin[Aspose.Çizim Forumu](https://forum.aspose.com/c/drawing/44) topluluk desteği ve tartışmalar için.

### S4: Kısa vadeli projeler için geçici lisans satın alabilir miyim?

 Cevap4: Evet, geçici lisans alabilirsiniz[Burada](https://purchase.aspose.com/temporary-license/).

### S5: Aspose.Drawing'in ayrıntılı belgelerini nerede bulabilirim?

 A5: Kapsamlı belgeler mevcut[Burada](https://reference.aspose.com/drawing/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
