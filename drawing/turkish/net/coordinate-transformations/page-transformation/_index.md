---
date: 2025-12-01
description: Aspose.Drawing kullanarak .NET’te koordinat sistemi dönüşümünü nasıl
  gerçekleştireceğinizi ve dikdörtgen grafiklerini nasıl çizeceğinizi öğrenin. Sayfa
  koordinatlarını nasıl dönüştüreceğinize dair adım adım rehber.
language: tr
linktitle: Coordinate System Transformation in Aspose.Drawing
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
title: Koordinat Sistemi Dönüşümü – Aspose.Drawing for .NET'te Sayfa Dönüşümü
url: /net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Koordinat Sistemi Dönüşümü – Aspose.Drawing for .NET'te Sayfa Dönüşümü

## Giriş

Hoş geldiniz! Bu öğreticide **sayfa koordinatlarını nasıl dönüştüreceğinizi** Aspose.Drawing for .NET kullanarak keşfedecek ve **koordinat sistemi dönüşümü** temellerini öğreneceksiniz. Grafik‑ağırlıklı bir uygulama geliştiriyor ya da çizim birimlerinde hassas kontrol ihtiyacınız varsa, bu kılavuz size tuvali ayarlamaktan bir dikdörtgen grafik öğesi çizmeye kadar her adımı gösterir. Sonunda, bu teknikleri kendi projelerinizde güvenle uygulayabileceksiniz.

## Hızlı Yanıtlar
- **Koordinat sistemi dönüşümü nedir?** Sayfa‑seviyesindeki birimleri (inç gibi) cihaz‑seviyesindeki piksellere eşleştirme.  
- **Aspose.Drawing neden kullanılmalı?** System.Drawing.Common'a tamamen yönetilen bir alternatif sunar ve çapraz‑platform desteği sağlar.  
- **Örnek uygulama ne kadar sürer?** Temel bir sayfa dönüşümü için yaklaşık 5‑10 dakika.  
- **Lisans gerekiyor mu?** Geliştirme için ücretsiz deneme yeterlidir; üretim için ticari lisans gereklidir.  
- **Hangi .NET sürümleri destekleniyor?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.

## Koordinat sistemi dönüşümü nedir?

Bir **koordinat sistemi dönüşümü**, mantıksal sayfa birimlerinin (inç, santimetre veya puan gibi) grafik render edilirken cihaz piksellerine nasıl dönüştürüleceğini tanımlar. `Graphics.PageUnit` özelliğini yapılandırarak çizim motoruna sağladığınız koordinatları nasıl yorumlaması gerektiğini söylersiniz; bu da boyut ve yerleşim üzerinde ince ayar yapmanızı sağlar.

## Aspose.Drawing ile koordinat sistemi dönüşümü neden kullanılmalı?

- **Cihaz‑bağımsız tasarım:** Kodu bir kez yazın, Aspose.Drawing herhangi bir ekran veya yazıcı için piksel ölçeklemesini otomatik yapar.  
- **Hassas çizim:** Teknik diyagramlar, CAD‑stil taslaklar veya ölçümlerin kritik olduğu her senaryo için idealdir.  
- **Çapraz‑platform güvenilirliği:** System.Drawing'in GDI+ sınırlamaları olmadan Windows, Linux ve macOS'ta tutarlı çalışır.

## Önkoşullar

Başlamadan önce şunların kurulu olduğundan emin olun:

- **Aspose.Drawing Kütüphanesi:** En son sürümü resmi siteden [burada](https://releases.aspose.com/drawing/net/) indirin.  
- **Geliştirme Ortamı:** Visual Studio, Rider veya herhangi bir .NET‑uyumlu IDE.  
- **Belge Dizininiz:** Koddaki `"Your Document Directory"` ifadesini çıktının kaydedileceği klasörle değiştirin.

Her şey hazır olduğuna göre, adım‑adım kılavuza geçelim.

## Ad Alanlarını İçe Aktarma

İlk olarak, gerekli ad alanını projenize ekleyin:

```csharp
using System.Drawing;
```

## Adım 1: Bir Bitmap Oluşturma

Çizim yüzeyi olarak hizmet edecek boş bir bitmap oluşturuyoruz. `Format32bppPArgb` piksel formatı yüksek kalite, ön‑çarpılmış alfa desteği sağlar.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## Adım 2: Bir Graphics Nesnesi Oluşturma

`Graphics` nesnesi bitmap için çizim API'sini sunar. Kodunuz ile piksel tamponu arasındaki köprüdür.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## Adım 3: Tuvali Temizleme

Çizilen şekillerin öne çıkması için tuvale nötr bir arka plan verin. Burada açık gri ile dolduruyoruz.

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

## Adım 4: Dönüşümü Ayarlama (Sayfayı nasıl dönüştürürsünüz)

Sayfa koordinatlarını cihaz piksellerine eşlemek için `PageUnit` özelliğini ayarlayın. Bu örnekte inç seçtik, ancak `GraphicsUnit.Millimeter`, `Point` vb. de kullanılabilir.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

## Adım 5: Bir Dikdörtgen Çizme – draw rectangle graphics

Şimdi ince mavi bir kalemle bir dikdörtgen çiziyoruz. İnç birimlerine geçiş yaptığımız için dikdörtgenin boyutu ve konumu inç cinsinden ifade ediliyor; bu da baskı‑odaklı yerleşimler için kodu daha okunabilir kılıyor.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

## Adım 6: Görüntüyü Kaydetme

Son olarak, bitmap'i daha önce belirttiğiniz klasörde bir PNG dosyası olarak yazın.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

Tebrikler! **Koordinat sistemi dönüşümünü** gerçekleştirdiniz, sayfa birimini inç olarak ayarladınız ve Aspose.Drawing kullanarak bir bitmap üzerinde **draw rectangle graphics** yaptınız.

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden Oluşur | Çözüm |
|-------|--------------|------|
| **Çıktı dosyası oluşturulmadı** | Yanlış yol veya eksik klasör | Hedef dizinin var olduğundan emin olun veya kaydetmeden önce `Directory.CreateDirectory` kullanın. |
| **Dikdörtgen bozulmuş görünüyor** | Yanlış `PageUnit` veya uyumsuz DPI | `graphics.PageUnit`'in kullanmak istediğiniz birimle eşleştiğini ve bitmap DPI'sinin (varsayılan 96 DPI) uygun şekilde ayarlandığını kontrol edin. |
| **Lisans istisnası** | Üretimde geçerli bir lisans olmadan çalışmak | Grafik nesnelerini oluşturmadan önce geçici veya kalıcı Aspose.Drawing lisansınızı uygulayın. |

## Sık Sorulan Sorular

**S: Aspose.Drawing'i ücretsiz kullanabilir miyim?**  
C: Evet, ücretsiz deneme sürümü [burada](https://releases.aspose.com/) mevcuttur.

**S: Aspose.Drawing için ayrıntılı belgeleri nerede bulabilirim?**  
C: Tam API referansı [burada](https://reference.aspose.com/drawing/net/) yer alır.

**S: Aspose.Drawing için destek nasıl alabilirim?**  
C: Topluluk yardımı ve resmi destek için [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) adresini ziyaret edin.

**S: Aspose.Drawing için geçici bir lisans mevcut mu?**  
C: Kesinlikle—geçici lisansı [buradan](https://purchase.aspose.com/temporary-license/) alabilirsiniz.

**S: Tam bir Aspose.Drawing lisansını nereden satın alabilirim?**  
C: Lisansı [buradan](https://purchase.aspose.com/buy) satın alabilirsiniz.

## Sonuç

Bu rehberde Aspose.Drawing'de **koordinat sistemi dönüşümü** hakkında bilmeniz gereken her şeyi ele aldık: tuvali ayarlama, sayfa birimlerini yapılandırma, hassas dikdörtgen grafik çizme ve sonucu kaydetme. Bu teknikleri raporlar, CAD‑stil çizimler veya ölçüm doğruluğunun kritik olduğu herhangi bir uygulama için ölçeklenebilir, cihaz‑bağımsız grafikler oluşturmak amacıyla kullanın.

---

**Son Güncelleme:** 2025-12-01  
**Test Edilen Versiyon:** Aspose.Drawing 24.12 for .NET  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}