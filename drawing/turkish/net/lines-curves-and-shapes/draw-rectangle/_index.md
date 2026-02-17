---
date: 2026-02-17
description: .NET'te Aspose.Drawing kullanarak nasıl dikdörtgen çizeceğinizi öğrenin.
  Bu adım adım kılavuz, bitmap görüntüsü oluşturmayı, bitmap üzerine dikdörtgen çizmeyi
  ve çizilen görüntüyü kaydetmeyi gösterir.
linktitle: Drawing Rectangles in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Aspose.Drawing for .NET ile Dikdörtgen Nasıl Çizilir
url: /tr/net/lines-curves-and-shapes/draw-rectangle/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing for .NET ile Dikdörtgen Çizme

## Giriş

Bu öğreticide Aspose.Drawing kütüphanesini kullanarak .NET uygulamalarınızda **dikdörtgen çizme** şekillerini keşfedeceksiniz. UI öğesi için basit bir dikdörtgen oluşturmanız ya da rapor için karmaşık bir grafik yaratmanız gerekse, aşağıdaki adımlar bir bitmap görüntüsü oluşturmayı, bir graphics nesnesi ayarlamayı, bitmap üzerine dikdörtgen çizmeyi ve sonunda çizilen görüntüyü diske kaydetmeyi size gösterecek.

## Hızlı Cevaplar
- **Gerekli kütüphane nedir?** Aspose.Drawing for .NET  
- **Şekli çizen yöntem hangisidir?** `Graphics.DrawRectangle`  
- **Lisans gerekli mi?** Deneme sürümü ücretsizdir; üretim için ticari lisans gereklidir.  
- **Dikdörtgen boyutunu değiştirebilir miyim?** Evet – genişlik, yükseklik ve konum parametrelerini ayarlayın.  
- **Kod .NET 6+ ile uyumlu mu?** Kesinlikle, Aspose.Drawing modern .NET sürümlerini destekler.

## Aspose.Drawing bağlamında “dikdörtgen çizme” nedir?
Aspose.Drawing ile bir dikdörtgen çizmek, `Graphics` sınıfını kullanarak bir bitmap tuvaline dikdörtgen bir kontur (veya doldurulmuş şekil) çizmeyi ifade eder. Bu yaklaşım, boyut, renk, çizgi kalınlığı ve görüntü formatı üzerinde tam kontrol sağlar ve anlık grafik üretimi için idealdir.

## Neden Aspose.Drawing ile dikdörtgen oluşturmalısınız?
- **Çapraz platform desteği** – Windows, Linux ve macOS'ta çalışır.  
- **GDI+ bağımlılığı yok** – `System.Drawing.Common` sınırlamalarından kaçınır.  
- **Zengin özellik seti** – gelişmiş çizim, anti-aliasing ve yüksek kaliteli çıktı formatları.  
- **Kolay lisanslama** – deneme sürümü mevcut, ticari lisansa sorunsuz geçiş.

## Ön Koşullar

Koda geçmeden önce aşağıdakilere sahip olduğunuzdan emin olun:

- Aspose.Drawing Kütüphanesi: .NET için Aspose.Drawing kütüphanesinin yüklü olduğundan emin olun. [buradan](https://releases.aspose.com/drawing/net/) indirebilirsiniz.  
- Geliştirme Ortamı: Makinenizde Visual Studio gibi çalışan bir .NET geliştirme ortamı kurulu olsun.  
- Temel .NET Bilgisi: .NET programlamanın temellerine aşina olun.

## Ad Alanlarını İçe Aktarın

Projeye gerekli ad alanlarını içe aktararak başlayın. Bu ad alanları grafik ve çizim işlemleri için gereklidir:

```csharp
using System.Drawing;
```

## Adım 1: Bitmap Görüntüsü Oluşturun

İlk olarak, çizim yüzeyi olarak hizmet edecek bir `Bitmap` nesnesi oluşturun. Bu bitmap, **dikdörtgen görüntüsü oluşturma** içeriğini barındıracak.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## Adım 2: Graphics Nesnesi Oluşturun

Sonra, bitmap'ten bir `Graphics` nesnesi alın. Graphics nesnesi, şekil, çizgi ve metin çizme gibi **graphics nesnesi oluşturma** işlemlerine olanak tanıyan motorudur.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## Adım 3: Dikdörtgen İçin Kalem Tanımlayın

Dikdörtgen konturunun renk ve kalınlığını belirlemek için bir `Pen` nesnesi tanımlayın.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
```

## Adım 4: Bitmap Üzerine Dikdörtgen Çizin

Şimdi, `Graphics` nesnesini kullanarak **bitmap üzerine dikdörtgen çizin**. Tasarımınıza uygun olacak şekilde X, Y, genişlik ve yükseklik değerlerini ayarlayın.

```csharp
graphics.DrawRectangle(pen, 10, 10, 900, 700);
```

## Adım 5: Çizilen Görüntüyü Kaydedin

Son olarak, bitmap'i bir dosyaya yazarak sonucu görebilirsiniz. Bu adım **çizilen görüntüyü kaydetme** yeteneğini gösterir.

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawRectangle_out.png");
```

Tebrikler! Aspose.Drawing for .NET kullanarak **dikdörtgen çizme** işlemini başarıyla tamamladınız.

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden | Çözüm |
|-------|-------|----------|
| Boş görüntü çıktısı | Bitmap serbest bırakılmadı veya graphics temizlenmedi | Kaydetmeden önce `graphics.Dispose();` çağırın veya bir `using` bloğu kullanın. |
| Düşük kalite kenarlar | Varsayılan yumuşatma modu | `graphics.SmoothingMode = System.Drawing.Drawing2D.SmoothingMode.AntiAlias;` olarak ayarlayın. |
| Dosya yolu hataları | Geçersiz dizin | Hedef klasörün mevcut olduğundan emin olun veya güvenli bir yol oluşturmak için `Path.Combine` kullanın. |

## Sıkça Sorulan Sorular

**Q: Dikdörtgeni katı bir renk ile doldurabilir miyim?**  
**A:** Evet, bir `SolidBrush` oluşturup konturu çizmeye başlamadan önce veya sonra `graphics.FillRectangle(brush, …)` çağırabilirsiniz.

**Q: Birden fazla dikdörtgen nasıl çizerim?**  
**A:** `Rectangle` yapılarını içeren bir koleksiyon üzerinde döngü kurup her yineleme için `DrawRectangle` çağırın.

**Q: Dikdörtgeni döndürmenin bir yolu var mı?**  
**A:** Çizmeden önce `graphics.RotateTransform(angle)` kullanın, ardından dönüşümünü sıfırlayın.

**Q: Kaydetme için hangi görüntü formatları destekleniyor?**  
**A:** PNG, JPEG, BMP, GIF ve TIFF, uygun `ImageFormat` parametresi ile desteklenir.

**Q: Aspose.Drawing .NET Core üzerinde çalışıyor mu?**  
**A:** Evet, kütüphane .NET Core, .NET 5, .NET 6 ve sonraki sürümlerle tam uyumludur.

## Ek Kaynaklar

Herhangi bir zorlukla karşılaşırsanız veya sorularınız olursa, [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) üzerinden yardım alabilirsiniz.

### SSS

#### Q1: Aspose.Drawing'ı ücretsiz kullanabilir miyim?

**A1:** Aspose.Drawing ticari bir kütüphanedir, ancak özelliklerini bir [ücretsiz deneme](https://releases.aspose.com/) ile keşfedebilirsiniz.

#### Q2: Detaylı belgeleri nerede bulabilirim?

**A2:** Derinlemesine bilgi için [belgelere](https://reference.aspose.com/drawing/net/) bakın.

#### Q3: Geçici bir lisans nasıl alabilirim?

**A3:** Test amaçlı bir [geçici lisans](https://purchase.aspose.com/temporary-license/) edinin.

#### Q4:. Aspose.Drawing karmaşık grafik görevleri için uygun mu?

**A4:** Kesinlikle! Aspose.Drawing karmaşık grafik işlemlerini yönetmek için gelişmiş özellikler sunar.

#### Q5: Aspose.Drawing'ı nereden satın alabilirim?

**A5:** Lisans satın almak için [buraya](https://purchase.aspose.com/buy) gidin.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-02-17  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

---