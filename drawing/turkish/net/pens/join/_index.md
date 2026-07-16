---
date: 2026-02-19
description: Aspose.Drawing'de kalemlerle yol çizmeyi ve yolları birleştirmeyi öğrenin,
  ardından basit C# kodu kullanarak görüntüyü PNG olarak kaydedin.
linktitle: Joining Paths with Pens in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Aspose.Drawing'de Kalemlerle Yol Çizme ve Yolları Birleştirme
url: /tr/net/pens/join/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing'de Yol Çizme ve Kalemlerle Yolları Birleştirme

## Giriiş

Aspose.Drawing for .NET'te hoş geldiniz! Bu öğretende, **yol çizme** nesnelerini keşfedecek, farklı line‑join stilleriyle birleştirecek ve sonunda **görseli PNG olarak kaydedeceksiniz**. Raporlama aracı, tasarım programlarını oluşturur ya da sadece net görsellerde ihtiyacınız olsun, kalemlerle yol çizimini ustalıkla görsel olarak ortaya çıkarıp üzerinde ince kontrol sağlar.

## Hızlı Yanıtlar
- **“yol çiz” ne anlaşılıyor?** Vektör tabanlı bir çizgi veya şekil tanımı oluşturur ve bir `Grafik` nesnesi tarafından oluşturulabilir.
- **Hangi hat birleştirme seçenekleri mevcut mu?** `Eğim`, `Gönye`, `Yuvarlak` ve `BevelClipped`.
- **Sonucu PNG olarak aktarabilir miyim?** Evet—`.png` uzantısı ile `Bitmap.Save` kullanın.
- **Lisans gerekir mi?** Değerlendirme için bir deneme sürümü çalışır; üretim için ticari lisans gereklidir.
- **Hangi .NET uzantısı destekleniyor mu?** .NET Framework 4.6+, .NET Core 3.1+ ve .NET 6+.

## Aspose.Drawing'de “yol nasıl çizilir” nedir?

Bir yol çizmek, bir dizi çizgi, eğri veya şekil içeren bir `GraphicsPath` oluşturmak anlamına gelir. Yol oluşturulduktan sonra, bir `Pen` kullanarak `Graphics` ile ayrılırsınız. Bu yaklaşımla, tek çizgileri çizmeye göre daha esnektir; Çünkü tüm bileşenleri dönüştürebilir ve farklı birleştirme bileşenlerini uygulayabilirsiniz.

## Yolları birleştirmek için neden Aspose.Drawing'i kullanmalısınız?

- **Tam .NET uyumluluğu** – Windows, Linux ve macOS üzerinde çalışır.
- **Zengin hat-birleştirme seçenekleri** – tek bir özellik ile köşeleri eğimli, yuvarlak veya köşeli hâle getirebilirsiniz.
- **Yüksek kaliteli raster çıktı** – ek dönüşüm adımları olmadan doğrudan PNG, JPEG, BMP vb. formatlarda kaydedebilirsiniz.
- **GDI+ sınırlaması yok** – `System.Drawing.Common` sınırlandırılabilir sunucu tarafı render işlemleri için idealdir.

## Önkoşullar

Kodun içine dalmadan önce kuruluşunuz olduğundan emin olun:

1. **Aspose.Drawing Library** – **[buradan](https://releases.aspose.com/drawing/net/)** indirildi.
2. **.NET Geliştirme Ortamı** – Herhangi bir IDE'yi destekleyen Visual Studio, VS Code veya C#.

Her şeyi hazırlayacağınıza göre, adım adım ilerleyelim.

## Ad Alanlarını İçe Aktar

Dosyanızın en üst düzeydeki kapsamını tamamlayın, böylece derleyici grafik sınıflarını bildirin:

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

## Adım 1: Bir Bitmap ve Grafik Nesnesi Oluşturun

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

Boş bir tuval (`Bitmap`) oluşturuyoruz; boyutu 1000 × 800 piksel ve çizim komutlarımızı işletecek bir `Graphics` nesnesi elde ediyoruz.

## Adım 2: DrawPath Yöntemini Tanımlayın

```csharp
private static void DrawPath(Graphics graphics, LineJoin join, int y)
{
    Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 30);
    GraphicsPath path = new GraphicsPath();
    path.StartFigure();
    path.AddLine(100, y, 200, y);
    path.AddLine(200, y, 200, y + 100);
    pen.LineJoin = join;
    graphics.DrawPath(pen, path);
}
```

Bu yardımcı metod çizim mantığını kapsüller:

- **Pen** – renk ve kalınlığı (30 px) ayarlar.  
- **GraphicsPath** – “L” şekli oluşturan iki bağlı çizgi tanımlar.  
- **LineJoin** – iki çizgi arasındaki köşenin nasıl render edileceğini kontrol eder (`Bevel`, `Round` vb.).  

Herhangi bir `LineJoin` değeriyle bu metodu çağırarak görsel farkı görebilirsiniz.

## Adım 3: Yolları Bevel LineJoin ile Birleştirin

```csharp
DrawPath(graphics, LineJoin.Bevel, 200);
```

`LineJoin.Bevel` kullanmak, iki çizginin buluştuğu noktada düzleştirilmiş bir köşe oluşturur.

## Adım 4: Yolları Round LineJoin ile Birleştirin

```csharp
DrawPath(graphics, LineJoin.Round, 400);
```

`LineJoin.Round` pürüzsüz, yuvarlatılmış bir köşe üretir—daha cilalı bir görünüm için mükemmeldir.

## Adım 5: Sonucu PNG Olarak Kaydedin

```csharp
bitmap.Save("Your Document Directory" + @"Pens\Join_out.png");
```

`Save` çağrısı bitmap'i PNG formatında bir dosyaya yazar. Ortamınıza uygun yolu ayarlayın.

## Yaygın Sorunlar ve Çözümler

| Sayı | Neden Olur | Düzelt |
|----------|-----|-----|
| **Resim boş görünüyor** | `Grafik` nesnesi temizlenmemiş veya bitmap boyutu çok küçük. | Çizimden önce `graphics.Clear(Color.White);` çağırın veya bitmap boyutlarını artırın. |
| **Köşe pürüzlü görünüyor** | Kalın bir kalemle düşük renklerli bitmap kullanımı. | Bitmap DPI'yi (`new Bitmap(width, height, PixelFormat.Format32bppPArgb)`) artırın veya kalem genişliğini azaltın. |
| **Dosya bulunamadı hatası** | Geçersiz kaydetme yolu. | `Path.Combine(Environment.GetFolderPath(Environment.SpecialFolder.MyDocuments), "Pens", "Join_out.png")` gibi bir yol kullanın. |

## Sıkça Sorulan Sorular

### S1: Aspose.Drawing'i ücretsiz kullanabilir miyim?

A1: Aspose.Drawing ticari bir ürünü, ancak **[ücretsiz deneme](https://releases.aspose.com/) ** ile üye olabilirsiniz.

### S2: Aspose.Drawing belgelerini nerede bulabilirim?

A2: Kapsamlı bağlılık için **[dokümantasyon](https://reference.aspose.com/drawing/net/) ** sayfasına bakın.

### S3: Aspose.Drawing için nasıl destek alabilirim?

C3: Topluluk yardımı ve resmi destek için **[Aspose.Drawing forumu](https://forum.aspose.com/c/drawing/44) ** adresini ziyaret edin.

### S4: Aspose.Drawing için geçici lisanslar mevcut mu?

C4: Evet, kısa vadede kullanım için **[geçici lisans](https://purchase.aspose.com/temporary-license/) ** alabilirsiniz.

### S5: Aspose.Drawing'i nereden satın alabilirim?

Cevap5: Aspose.Drawing'i **[buradan](https://purchase.aspose.com/buy) ** satın alabilirsiniz.

## Çözüm

Bu rehberde **yol çizme** nesnelerini ele aldık, farklı `LineJoin` stillerini uyguladık ve Aspose.Drawing for .NET kullanarak son grafiği PNG dosyası olarak kaydettik. Bu adımda ustalaştırarak sunucu‑tarafı kodlayarakzdan doğrudan karmaşık parçalar, özel ikonlar veya dinamik parçalar oluşturabilirsiniz.

---

**Son Güncelleme:** 2026-02-19
**Şunlarla test edilmiştir:** Aspose.Drawing 24.11 for .NET
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}