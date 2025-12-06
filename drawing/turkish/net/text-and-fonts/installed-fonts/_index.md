---
date: 2025-12-06
description: Aspose.Drawing for .NET kullanarak yüklü yazı tiplerini listeleme, yazı
  tipi ailelerini gösterme, bitmap'ten grafik oluşturma ve yazı tipleriyle metin çizme
  sırasında PNG görüntü dosyalarını nasıl kaydedeceğinizi öğrenin.
language: tr
linktitle: Save PNG Image and Work with Installed Fonts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Aspose.Drawing'de PNG Görüntüsü Kaydetme ve Yüklü Yazı Tipleriyle Çalışma
url: /net/text-and-fonts/installed-fonts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PNG Görüntüsü Kaydetme ve Aspose.Drawing'de Yüklü Yazı Tipleriyle Çalışma

## Giriş

Makinede yüklü yazı tipleri hakkında bilgi gösteren **PNG görüntü** dosyalarını kaydetmeniz gerekiyorsa, Aspose.Drawing for .NET size temiz, çapraz‑platform bir yol sunar. Bu öğreticide yüklü yazı tiplerini listeleme, yazı tipi ailelerini gösterme, bir bitmap'ten grafik oluşturma ve yazı tipleriyle metin çizme adımlarını ele alacağız; ardından sonucu PNG olarak kaydedeceğiz. Sonunda, herhangi bir .NET projesine ekleyebileceğiniz yeniden kullanılabilir bir kod parçacığına sahip olacaksınız.

## Hızlı Yanıtlar
- **Bu öğretici ne oluşturur?** Yüklü yazı tipi ailelerini listeleyen bir PNG görüntüsü.  
- **Hangi kütüphane gereklidir?** Aspose.Drawing for .NET (System.Drawing.Common gerekmez).  
- **Özel yazı tipleri kullanabilir miyim?** Evet – sadece onları bir `InstalledFontCollection` içine yükleyin.  
- **Çıktı çözünürlüğü ayarlanabilir mi?** Kesinlikle – bitmap boyutunu veya piksel formatını değiştirin.  
- **Kodu çalıştırmak için lisans gerekir mi?** Değerlendirme için geçici bir lisans yeterlidir; üretim için tam lisans gereklidir.

## “save PNG image” Aspose.Drawing bağlamında ne anlama geliyor?
PNG görüntüsü kaydetmek, çizim yüzeyinizi (bir `Bitmap`) `.png` uzantılı bir dosyaya dönüştürmek demektir. Aspose.Drawing kodlamayı sizin için halleder; sadece istediğiniz yolu belirterek `bitmap.Save(...)` çağırmanız yeterlidir.

## Neden yüklü yazı tiplerini listeleyip yazı tipi ailelerini gösteriyoruz?
Hangi yazı tiplerinin mevcut olduğunu bilmek, son kullanıcı ortamına uyum sağlayan dinamik grafikler oluşturmanıza olanak tanır. Bu, raporlar, sertifikalar veya kurumsal marka kimliğine uygun görsel içerikler üretirken özellikle faydalıdır; ayrı font dosyaları dağıtmanıza gerek kalmaz.

## Ön Koşullar

- **Aspose.Drawing Kütüphanesi** – en yeni sürümü [Aspose Drawing indirme sayfasından](https://releases.aspose.com/drawing/net/) indirin.  
- **IDE** – Visual Studio, Rider veya herhangi bir .NET‑uyumlu editör.  
- **Temel C# bilgisi** – sınıflar, nesneler ve basit döngüler konusunda rahat olmalısınız.

## Ad Alanlarını İçe Aktarma
Yazı tipleri ve grafiklerle çalışmak için C# dosyanızın en üst kısmına şu ad alanlarını ekleyin:

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Adım‑Adım Kılavuz

### Adım 1: Bir bitmap oluşturun (tuval)
İlk olarak, son görüntüyü tutacak bir bitmap oluştururuz. Bitmap'in boyutu ve piksel formatı, kaydedilen PNG'nin kalitesini belirler.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Adım 2: Bitmap'ten grafik oluşturun
Sonra, bitmap'ten bir `Graphics` nesnesi alırız. Bu nesne, tuval üzerine şekil, metin ve görüntü çizmeyi sağlar.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### Adım 3: Fırça ve yazı tipini ayarlayın (yazı tipleriyle metin çizin)
Metin rengi için bir fırça ve tip, boyut, stil tanımlayan bir `Font` nesnesine ihtiyacımız var.

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### Adım 4: Yüklü yazı tiplerini listeleyin ve yazı tipi ailelerini gösterin
Şimdi, bitmap üzerine doğrudan yazı tipi ailelerinin sayısını ve ilk birkaç adını gösteriyoruz. Bu, **list installed fonts** ve **show font families** yeteneklerini sergiler.

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

### Adım 5: PNG görüntüsünü kaydedin
Son olarak, bitmap'i bir PNG dosyası olarak diske yazarız. Bu, temel **save png image** işlemdir.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

> **İpucu:** Farklı işletim sistemlerinde dizin ayırıcılarıyla ilgili sorunları önlemek için dosya yolları oluştururken `Path.Combine` kullanın.

## Yaygın Sorunlar ve Çözümler
| Sorun | Neden | Çözüm |
|-------|-------|------|
| **Yazı tipleri görüntülenmiyor** | `InstalledFontCollection` doldurulmamış (ör. fontsuz bir headless sunucu). | Gerekli yazı tiplerini sunucuya kurun veya özel yazı tiplerini uygulamanıza gömün. |
| **Kaydedilen dosya bozuk** | Yanlış piksel formatı veya yazma izni eksikliği. | Hedef klasörün var olduğundan ve uygulamanın yazma iznine sahip olduğundan emin olun; `Format32bppPArgb` tutun. |
| **Metin bulanık görünüyor** | Düşük DPI ayarları. | Bitmap boyutlarını artırın veya `graphics.SmoothingMode = SmoothingMode.AntiAlias` ayarlayın. |

## Sık Sorulan Sorular

**S: Makinede yüklü olmayan özel yazı tiplerini kullanabilir miyim?**  
C: Evet. Yazı tipi dosyasını bir `PrivateFontCollection` içine yükleyin ve bu koleksiyondan bir `Font` oluşturun.

**S: Yazı tipiyle ilgili istisnaları nasıl ele alırım?**  
C: Yazı tipi oluşturmayı bir `try/catch` bloğuna alın ve eksik aileler için `ArgumentException` kontrol edin.

**S: Aspose.Drawing web uygulamaları için uygun mu?**  
C: Kesinlikle. Kütüphane ASP.NET Core, Azure Functions ve diğer sunucu‑tarafı ortamlarla çalışır.

**S: Metin rengini veya stilini değiştirebilir miyim?**  
C: Evet. farklı `Brush` türleri (ör. `LinearGradientBrush`) kullanın ve `FontStyle` enum'ını değiştirin.

**S: Test için geçici bir lisans nasıl alabilirim?**  
C: [Aspose geçici‑lisans sayfasından](https://purchase.aspose.com/temporary-license/) bir deneme lisansı indirin.

## Sonuç

Bu adımları izleyerek **save PNG image** dosyalarını dinamik olarak **list installed fonts**, **show font families**, **create graphics from bitmap** ve **draw text with fonts** özellikleriyle Aspose.Drawing for .NET kullanarak oluşturmayı öğrendiniz. Projenizin görsel gereksinimlerine uyacak şekilde başka yazı tipleri, renkler ve bitmap boyutlarıyla denemeler yapmaktan çekinmeyin.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Son Güncelleme:** 2025-12-06  
**Test Edilen Versiyon:** Aspose.Drawing 24.11 for .NET  
**Yazar:** Aspose