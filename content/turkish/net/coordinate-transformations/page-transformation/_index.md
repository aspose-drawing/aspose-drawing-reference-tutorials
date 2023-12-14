---
title: Aspose.Drawing for .NET'te Sayfa Dönüşümü
linktitle: Aspose.Drawing'de Sayfa Dönüşümü
second_title: Aspose.Drawing .NET API - System.Drawing.Common'a alternatif
description: Aspose.Drawing'i kullanarak .NET'te adım adım sayfa dönüşümlerini öğrenin. Bu kapsamlı eğitimle grafik becerilerinizi geliştirin.
type: docs
weight: 13
url: /tr/net/coordinate-transformations/page-transformation/
---
## giriiş

Aspose.Drawing for .NET kullanarak sayfa dönüşümü hakkındaki bu kapsamlı eğitime hoş geldiniz. Grafikler ve bitmap dönüşümleriyle çalışma becerilerinizi geliştirmek istiyorsanız doğru yerdesiniz. Bu eğitimde Aspose.Drawing'i kullanarak sayfaları dönüştürme sürecinde size rehberlik edeceğiz ve her adımı net bir şekilde kavramanızı sağlayacağız.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

-  Aspose.Drawing Kütüphanesi: Aspose.Drawing kütüphanesini indirip yükleyin. En son sürümü bulabilirsiniz[Burada](https://releases.aspose.com/drawing/net/).

- Geliştirme Ortamı: Geliştirme ortamınızı Visual Studio veya tercih edilen herhangi bir başka .NET geliştirme aracıyla kurun.

- Belge Dizininiz: Koddaki "Belge Dizininiz"i dönüştürülen görüntüyü kaydetmek istediğiniz gerçek dizinle değiştirin.

Artık önkoşullarımızı sıraladığımıza göre adım adım kılavuza geçelim.

## Ad Alanlarını İçe Aktar

.NET projenizde gerekli ad alanlarını içe aktararak başlayın:

```csharp
using System.Drawing;
```

## 1. Adım: Bitmap Oluşturun

Belirli boyutlara ve piksel biçimine sahip yeni bir bitmap oluşturarak başlayın:

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

Bu, dönüşümünüz için boş bir tuval başlatır.

## Adım 2: Grafik Nesnesi Oluşturun

Üzerinde çizim yapmak için bitmap'ten bir Graphics nesnesi oluşturun:

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## 3. Adım: Kanvası Temizleyin

Tuvali belirli bir renkle (bu durumda gri) doldurarak temizleyin:

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

## Adım 4: Dönüşümü Ayarlayın

Sayfa koordinatlarını cihaz koordinatlarına eşleyen dönüşümü ayarlayın. Bu örnekte inç kullanıyoruz:

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

## Adım 5: Bir Dikdörtgen Çizin

Belirtilen kalemle bir dikdörtgen çizmek için Graphics nesnesini kullanın:

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

## Adım 6: Görüntüyü Kaydedin

Dönüştürülen görüntüyü belirttiğiniz dizine kaydedin:

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

Tebrikler! Aspose.Drawing for .NET'i kullanarak bir sayfayı başarıyla dönüştürdünüz.

## Çözüm

Bu eğitimde Aspose.Drawing'i kullanarak sayfa dönüşümü gerçekleştirmenin temel adımlarını ele aldık. Bu adımları takip ederek bu dönüşümleri .NET uygulamalarınıza sorunsuz bir şekilde entegre edebilirsiniz.

## SSS'ler

### S1: Aspose.Drawing'i ücretsiz kullanabilir miyim?

 Cevap1: Aspose.Drawing, erişebileceğiniz ücretsiz bir deneme sunuyor[Burada](https://releases.aspose.com/).

### S2: Aspose.Drawing'in ayrıntılı belgelerini nerede bulabilirim?

 A2: Belgeler mevcut[Burada](https://reference.aspose.com/drawing/net/).

### S3: Aspose.Drawing için nasıl destek alabilirim?

 C3: Destek için şu adresi ziyaret edin:[Aspose.Çizim Forumu](https://forum.aspose.com/c/diagram/17).

### S4: Aspose.Drawing için geçici bir lisans mevcut mu?

 Cevap4: Evet, geçici lisans alabilirsiniz[Burada](https://purchase.aspose.com/temporary-license/).

### S5: Aspose.Drawing'i nereden satın alabilirim?

 Cevap5: Aspose.Drawing'i satın alabilirsiniz[Burada](https://purchase.aspose.com/buy).