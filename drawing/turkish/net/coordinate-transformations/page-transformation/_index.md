---
date: 2025-11-30
description: Aspose.Drawing for .NET kullanarak koordinat sistemi dönüşümünü nasıl
  uygulayacağınızı, dikdörtgen bitmap çizeceğinizi ve sayfaları nasıl dönüştüreceğinizi
  öğrenin.
language: tr
linktitle: Page Transformation in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Aspose.Drawing for .NET'te Koordinat Sistemi Dönüşümü (Sayfa Dönüşümü)
url: /net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing for .NET'te Koordinat Sistemi Dönüşümü (Sayfa Dönüşümü)

## Giriş

Hoş geldiniz! Bu öğreticide Aspose.Drawing for .NET kullanarak bir sayfada **koordinat sistemi dönüşümünün nasıl yapılacağını** keşfedeceksiniz. **draw rectangle bitmap** nesneleri çizmeniz, çizimleri ölçeklemeniz veya sadece sayfa birimlerini cihaz birimlerine eşleştirmeniz gerekse, aşağıdaki adımlar sizi tüm süreç boyunca yönlendirecek—net, öz ve projenize k‑yapıştır yapmaya hazır.

## Hızlı Yanıtlar
- **Çizim için birincil sınıf nedir?** Aspose.Drawing'den `Graphics`.
- **Sayfa birimlerini nasıl ayarlarım?** `graphics.PageUnit = GraphicsUnit.Inch;` kullanın.
- **Dönüştürülmüş bir sayfada dikdörtgen çizebilir miyim?** Evet—bir `Pen` oluşturun ve `DrawRectangle` çağırın.
- **Çıktı nerede kaydedilir?** `bitmap.Save` içinde belirttiğiniz klasöre.
- **Üretim için lisansa ihtiyacım var mı?** Ticari kullanım için geçerli bir Aspose.Drawing lisansı gereklidir.

## Koordinat sistemi dönüşümü nedir?

Bir **coordinate system transformation** (koordinat sistemi dönüşümü), mantıksal sayfa koordinatlarının (inç veya milimetre gibi) fiziksel cihaz koordinatlarına (piksel) nasıl eşlendiğini değiştirir. Dönüşümü ayarlayarak, tüm çizim işlemlerinin ölçeklendirme, döndürme ve çevirme işlemlerini kontrol edersiniz; bu da çözünürlükten bağımsız grafikler tasarlamayı kolaylaştırır.

## Sayfa dönüşümleri için Aspose.Drawing neden kullanılmalı?

- **Tam .NET uyumluluğu** – .NET Framework, .NET Core ve .NET 5/6 ile çalışır.
- **Zengin grafik API'si** – platform kısıtlamaları olmadan System.Drawing.Common ile aynı işlevselliği sunar.
- **Basit birim yönetimi** – tek bir özellik ile inç, milimetre, point vb. arasında geçiş yapar.
- **Yüksek kalite çıktı** – PNG, JPEG, BMP ve diğer formatları hassas kontrol ile üretir.

## Önkoşullar

Önceden aşağıdakilere sahip olduğunuzdan emin olun:

- **Aspose.Drawing Library** – resmi siteden en son sürümü indirin [here](https://releases.aspose.com/drawing/net/).
- **Development Environment** – Visual Studio (herhangi bir sürüm) veya başka bir .NET IDE.
- **Write Access** – dönüştürülmüş görüntünün kaydedileceği makinenizdeki bir klasör (koddaki `"Your Document Directory"` ifadesini gerçek yol ile değiştirin).

Şimdi hazır olduğumuza göre, her adımı birlikte inceleyelim.

## Ad Alanlarını İçe Aktarma

İlk olarak, gerekli ad alanını kapsam içine alın:

```csharp
using System.Drawing;
```

* *Neden önemli?*: `System.Drawing`, öğretici boyunca kullanacağımız `Bitmap`, `Graphics`, `Pen` ve renk yapılarını içerir.

## Adım 1: Bir Bitmap Oluşturun

Dönüştürülmüş çizimi barındıracak boş bir tuval oluşturun. **1000 × 800 piksel** boyutunu ve alfa şeffaflığını destekleyen bir piksel formatını belirtiyoruz.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

Bu bitmap çizim yüzeyi olarak görev yapar. Seçilen piksel formatı (`Format32bppPArgb`), önceden çarpılmış alfa ile yüksek kaliteli render sağlar.

## Adım 2: Bir Graphics Nesnesi Oluşturun

Bir `Graphics` nesnesi çizim yöntemlerini (çizgiler, şekiller, metin) sağlar. Bunu az önce oluşturduğumuz bitmap'ten elde ederiz.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

`Graphics` nesnesi tüm render işlemlerinin çekirdeğidir; bir sonraki adımda uygulayacağımız dönüşüm ayarlarına uyar.

## Adım 3: Tuvali Temizle

Herhangi bir şey çizmeye başlamadan önce tuvali nötr bir arka plan rengine (bu örnekte gri) temizleyin. Bu adım ayrıca tüm bitmap'i katı bir renk ile doldurmayı gösterir.

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

## Adım 4: Dönüşümü Ayarla (Sayfa Dönüşümünü Uygula)

Burada `PageUnit` değerini inç olarak ayarlayarak **sayfa dönüşümünü uyguluyoruz**. Bu, grafik motoruna sonraki tüm koordinatları piksel yerine inç olarak yorumlamasını söyler.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

*İpucu*: `PageUnit`'ı değiştirmek, piksel değerlerini manuel olarak hesaplamadan **sayfa koordinatlarını nasıl dönüştüreceğinizi** basit bir şekilde sağlar.

## Adım 5: Bir Dikdörtgen Çizin (draw rectangle bitmap)

Şimdi (1, 1) inç konumunda **1 inç × 1 inç** ölçülerinde bir dikdörtgen çiziyoruz. `Pen` genişliği `0.1f` inç olarak ayarlanmış, ince ama görünür bir çizgi sağlar.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

Bu, dönüşüm uygulandıktan sonra **draw rectangle bitmap**'i gösterir—dikdörtgenin boyutunun piksel değil inç olarak tanımlandığına dikkat edin.

## Adım 6: Görüntüyü Kaydedin

Son olarak, dönüştürülmüş bitmap'i diske kaydedin. `"Your Document Directory"` ifadesini makinenizdeki gerçek klasör yolu ile değiştirin.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

Çıktı dosyası (`PageTransformation_out.png`), daha önce ayarladığımız koordinat sistemi dönüşümünü kullanarak çizilen dikdörtgeni içerecek.

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden | Çözüm |
|-------|-------|-------|
| **Görüntü boş görünüyor** | Tuval temizlenmemiş veya çizim görünür alanın dışında yapılmış. | `graphics.PageUnit` ve koordinat değerlerini doğrulayın; dikdörtgenin bitmap sınırları içinde olduğundan emin olun. |
| **Yanlış ölçekleme** | Yanlış `GraphicsUnit` kullanılması. | `graphics.PageUnit`'ın istediğiniz birimle (ör. `GraphicsUnit.Inch`) eşleştiğini iki kez kontrol edin. |
| **Dosya yolu hataları** | Klasör eksik veya geçersiz karakterler. | Hedef klasörü önceden oluşturun veya yolu güvenli bir şekilde oluşturmak için `Path.Combine` kullanın. |

## Sıkça Sorulan Sorular

**S: Aspose.Drawing'i ücretsiz kullanabilir miyim?**  
C: Aspose.Drawing ücretsiz bir deneme sürümü sunar; bunu [here](https://releases.aspose.com/) adresinden erişebilirsiniz.

**S: Aspose.Drawing için ayrıntılı belgeleri nerede bulabilirim?**  
C: Dokümantasyon [here](https://reference.aspose.com/drawing/net/) adresinde mevcuttur.

**S: Aspose.Drawing için destek nasıl alabilirim?**  
C: Destek için [Aspose.Drawing Forum](https://forum.aspose.com/c/diagram/17) adresini ziyaret edin.

**S: Aspose.Drawing için geçici bir lisans mevcut mu?**  
C: Evet, geçici lisansı [here](https://purchase.aspose.com/temporary-license/) adresinden alabilirsiniz.

**S: Aspose.Drawing'i nereden satın alabilirim?**  
C: Aspose.Drawing'i [here](https://purchase.aspose.com/buy) adresinden satın alabilirsiniz.

## Sonuç

Artık Aspose.Drawing for .NET kullanarak **koordinat sistemi dönüşümünü uygulamayı**, **draw rectangle bitmap** nesnelerini çizmeyi ve **sonucu kaydetmeyi** öğrendiniz. Bu yapı taşları, çözünürlükten bağımsız grafikler oluşturmanıza olanak tanır; raporlar, UI öğeleri veya kesin boyutlandırmanın önemli olduğu herhangi bir senaryo için mükemmeldir. Çizimlerinizi nasıl etkilediklerini görmek için diğer `GraphicsUnit` değerleriyle (ör. `Millimeter` veya `Point`) deneyler yapın.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Son Güncelleme:** 2025-11-30  
**Test Edilen:** Aspose.Drawing 24.11 for .NET  
**Yazar:** Aspose