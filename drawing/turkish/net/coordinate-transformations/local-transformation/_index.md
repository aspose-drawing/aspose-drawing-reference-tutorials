---
date: 2026-01-27
description: Aspose.Drawing for .NET kullanarak elipsi nasıl döndüreceğinizi ve grafikleri
  PNG'ye nasıl dönüştüreceğinizi öğrenin. Kod örnekleriyle adım adım kılavuz.
linktitle: Local Transformation in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 'Elipsi Döndürme: Aspose.Drawing for .NET''te Yerel Dönüşüm'
url: /tr/net/coordinate-transformations/local-transformation/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ellips Döndürme: Aspose.Drawing for .NET'te Yerel Dönüşüm

## Giriş

Bir .NET uygulamasında **bir elipsi döndürmeniz** gerektiğinde, Aspose.Drawing bunu basit ve güvenilir bir şekilde yapmanızı sağlar. Bu öğreticide **elipsi nasıl döndüreceğinizi** bir dönüşüm matrisi kullanarak öğrenecek, sonucu render edecek ve sonunda **grafikleri PNG'ye dönüştürerek** depolama veya daha ileri işleme için kaydedeceksiniz. Sonunda, herhangi bir yerel dönüşüm senaryosu için yeniden kullanılabilir bir deseniniz olacak.

## Hızlı Yanıtlar
- **Yerel dönüşüm nedir?** Belirli bir çizim öğesine (döndürme, ölçekleme, çevirme, eğme) tüm tuval üzerinde etkisi olmadan uygulanan matris‑tabanlı bir işlemdir.  
- **.NET'te bunu hangi kütüphane destekliyor?** Aspose.Drawing for .NET, desteklenen tüm .NET sürümlerinde çalışan tam özellikli bir API sunar.  
- **Sonucu PNG olarak kaydedebilir miyim?** Evet—sadece “.png” uzantılı bir dosya adıyla `Bitmap.Save` metodunu çağırın, Aspose.Drawing dönüşümü halleder.  
- **Geliştirme için lisansa ihtiyacım var mı?** Ücretsiz deneme sürümü test için çalışır; üretim kullanımı için ticari lisans gereklidir.  
- **Uygulama ne kadar sürer?** Temel bir örnek için yaklaşık 10‑15 dakikadır.

## Aspose.Drawing ile elipsi nasıl döndürürüz
Elips döndürmek temelde **bir şekli matris kullanarak döndürmek** anlamına gelir. Bir `Matrix` oluşturur, dönüş açısını ayarlarsınız, elipsin merkez noktasını belirlersiniz ve ardından bu matrisi `GraphicsPath`'e uygularsınız. Bu, dönüşümün sadece elipse uygulanmasını sağlar, geri kalan tuval değişmeden kalır.

## “Dönüşüm nasıl uygulanır?” grafik programlamada ne demektir?
Bir dönüşüm uygulamak, bir **Matrix** kullanarak bir çizim nesnesinin koordinat sistemini değiştirmek demektir. Matris, noktaların nasıl döndürüleceğini, ölçekleneceğini veya taşınacağını tanımlar ve minimal kodla sofistike görsel efektler oluşturmanıza imkan tanır.

## Aspose.Drawing ile **grafikleri PNG'ye dönüştürmek** neden tercih edilmeli?
- **Çapraz‑platform**: .NET Framework, .NET Core ve .NET 5/6+ üzerinde çalışır.  
- **GDI+ bağımlılığı yok**: `System.Drawing.Common`'ın Windows dışı platformlardaki sorunlarından kaçınır.  
- **Yüksek‑kaliteli render**: PNG dosyaları için anti‑aliasing ve piksel‑tam çıktı.  
- **Zengin API**: Yollar, kalemler, fırçalar ve dönüşüm matrisleri için tam destek.

## Ön Koşullar

Başlamadan önce şunların kurulu olduğundan emin olun:

1. **Aspose.Drawing for .NET** – [indirme bağlantısı](https://releases.aspose.com/drawing/net/) üzerinden indirin ve kurun.  
2. Çıktı görüntüsünün kaydedileceği bir klasör (örnek: `C:\MyImages\`).  
3. C# ve .NET proje kurulumu hakkında temel bilgi.

## Ad Alanlarını İçe Aktarma

İlk olarak, C# dosyanıza gerekli ad alanlarını ekleyin:

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

Bu ad alanları, dönüşüm iş akışı için gereken `Bitmap`, `Graphics`, `GraphicsPath` ve `Matrix` sınıflarına erişim sağlar.

## Adım‑Adım Kılavuz

### Adım 1: Bir Bitmap Oluşturun

Boş bir tuvalle başlarız. Bitmap boyutu ve piksel formatı, alfa şeffaflığını destekleyen yüksek‑kaliteli, 32‑bit bir görüntü elde etmemizi sağlar.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

> **İpucu:** `Format32bppPArgb` kullanmak, görüntünün önceden çarpılmış alfa içermesini sağlar; bu, PNG çıktısı için idealdir.

### Adım 2: Bir Graphics Nesnesi Oluşturun

`Graphics` nesnesi, bitmap üzerinde çalışan çizim metodlarını sunar. Arka planı nötr bir griye temizleyerek dönüştürülmüş şeklin öne çıkmasını sağlarız.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

### Adım 3: Bir GraphicsPath Oluşturun

`GraphicsPath`, karmaşık şekiller tanımlamanıza olanak verir. Burada (300, 300) konumunda, genişliği 400 ve yüksekliği 200 olan bir elips ekliyoruz.

```csharp
GraphicsPath path = new GraphicsPath();
path.AddEllipse(300, 300, 400, 200);
```

### Adım 4: Yerel Dönüşüm Uygulayın (matris ile şekli döndür)

Şimdi temel soruya yanıt veriyoruz: **elipsi nasıl döndürürüz**. Bir `Matrix` oluşturur, elipsin merkezi (500, 400) etrafında 45° döndürür ve matrisi yola uygularız.

```csharp
Matrix matrix = new Matrix();
matrix.RotateAt(45, new Point(500, 400));
path.Transform(matrix);
```

> **Neden bir noktada döndürülür?** Şeklin merkezinde döndürmek, şeklin orijinden dolaşmasını engeller ve doğal bir görünüm kazandırır.

### Adım 5: Dönüştürülmüş Yolu Çizin

Dönüşüm yerinde olduğunda, kalınlığı 2 olan mavi bir kalemle yolu render ederiz.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawPath(pen, path);
```

### Adım 6: Dönüştürülmüş Görüntüyü Kaydedin (grafikleri PNG'ye dönüştürün)

Son olarak bitmap'i PNG dosyası olarak kalıcı hâle getiririz. Yol, seçtiğiniz dizini dönüşüm örnekleri için bir alt klasörle birleştirir.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\LocalTransformation_out.png");
```

> **Not:** Bu satır aynı zamanda **bitmap'i PNG olarak kaydetmeyi** gösterir. `.png` uzantısı, Aspose.Drawing'in PNG kodlayıcısını otomatik olarak tetikler ve **grafikleri PNG'ye dönüştürme** gereksinimini karşılar.

## Yaygın Sorunlar & Çözümler

| Sorun | Neden | Çözüm |
|-------|-------|------|
| **Boş çıktı görüntüsü** | Graphics temizlenmemiş veya kalem rengi arka planla aynı | `graphics.Clear` ile zıt bir renk kullanın ve kalem renginin görünür olduğundan emin olun. |
| **Bozuk dönüşüm** | `Rotate` yerine `RotateAt` kullanılması | `RotateAt` kullanın ve şeklin merkez noktasını belirtin. |
| **Dosya kaydedilmiyor** | Geçersiz dizin yolu veya yazma izni eksikliği | Dizin varlığını kontrol edin ve uygulamanın yazma izni olduğundan emin olun. |
| **PNG bulanık görünüyor** | Bitmap'in düşük DPI ayarı | Daha yüksek çözünürlükte bitmap oluşturun veya `graphics.SmoothingMode = SmoothingMode.AntiAlias` ayarlayın. |

## Sık Sorulan Sorular

**S:** Birden fazla dönüşümü (ör. ölçekle ardından döndür) zincirleyebilir miyim?  
**C:** Evet. Tek bir `Matrix` oluşturup `Scale`, `RotateAt` ve `Translate` gibi metodları ihtiyacınıza göre sırayla çağırın, ardından `path.Transform(matrix);` ile uygulayın.

**S:** Aspose.Drawing yüksek performanslı render için uygun mu?  
**C:** Kesinlikle. Kütüphane hem hız hem de kalite açısından optimize edilmiştir ve Windows dışı platformlarda GDI+ sınırlamalarından kaçınır.

**S:** Başka hangi dönüşüm türleri destekleniyor?  
**C:** Döndürme dışında, aynı `Matrix` sınıfı ile çevirme (translation), ölçekleme (scaling) ve eğme (skewing) de yapılabilir.

**S:** Dönüşüm sırasında oluşabilecek istisnalar nasıl ele alınır?  
**C:** Çizim kodunu bir `try‑catch` bloğuna sarın ve `System.Drawing.Drawing2D` istisnalarını inceleyin. Ayrıntılı hata yönetimi için resmi [Aspose.Drawing belgelerine](https://reference.aspose.com/drawing/net/) bakın.

**S:** Aspose.Drawing'i satın almadan deneyebilir miyim?  
**C:** Evet, [ücretsiz deneme](https://releases.aspose.com/) bağlantısı üzerinden tam işlevsel bir deneme sürümü mevcuttur.

## Sonuç

Bu kılavuzu izleyerek **elipsi nasıl döndürürsünüz** ve **grafikleri PNG'ye nasıl dönüştürürsünüz** konusunda bilgi sahibi oldunuz. Aynı desen, ölçekleme, çevirme veya eğme gibi diğer şekiller için de yeniden kullanılabilir; böylece uygulamalarınızda zengin, etkileşimli görsel bileşenler oluşturabilirsiniz.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Son Güncelleme:** 2026-01-27  
**Test Edilen Versiyon:** Aspose.Drawing 24.11 for .NET  
**Yazar:** Aspose  

---