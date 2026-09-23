---
date: 2026-09-23
description: Aspose.Drawing for .NET kullanarak görüntü üzerine metin nasıl çizilir
  öğrenin. Metin içeren bir görüntü oluşturun, bitmap'e metin ekleyin ve bitmap'i
  özel yazı tipleriyle PNG olarak kaydedin.
keywords:
- draw text on image
- generate image with text
- custom font on image
- save bitmap as png
- add text to bitmap
lastmod: 2026-09-23
linktitle: Aspose.Drawing ile Metin Çizme
og_description: Aspose.Drawing for .NET kullanarak görüntü üzerine metin nasıl çizilir
  öğrenin. Bu öğreticide, metin içeren bir görüntü oluşturma, bitmap'e metin ekleme
  ve bitmap'i özel yazı tipleriyle PNG olarak kaydetme adımları gösterilmektedir.
og_image_alt: Screenshot of a PNG image created with Aspose.Drawing showing custom
  text
og_title: Aspose.Drawing for .NET ile görüntü üzerine metin çizme – Quick guide
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to draw text on image using Aspose.Drawing for .NET. Generate
    image with text, add text to bitmap, and save bitmap as PNG with custom fonts.
  headline: How to draw text on image with Aspose.Drawing for .NET
  type: TechArticle
- questions:
  - answer: Replace the `.png` extension with `.jpg` in the `Save` method and optionally
      specify an `ImageCodecInfo` for JPEG quality.
    question: How do I change the output format to JPEG?
  - answer: Yes, include line‑break characters (`\n`) in the string or use `StringFormat`
      with `FormatFlags.LineLimit`.
    question: Can I draw multi‑line text?
  - answer: Use `Graphics.MeasureString` to get the exact dimensions of the rendered
      text.
    question: Is there a way to measure text size before drawing?
  - answer: Absolutely. Provide a font that contains the required glyphs and the library
      will render them correctly.
    question: Does Aspose.Drawing support Unicode characters?
  - answer: The examples were tested with Aspose.Drawing 24.11 for .NET.
    question: What version of Aspose.Drawing was used for testing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- draw text on image
- Aspose.Drawing
- .NET image processing
- generate image with text
- custom font on image
title: Aspose.Drawing for .NET ile görüntü üzerine metin çizme
url: /tr/net/text-and-fonts/draw-text/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing for .NET ile görüntü üzerine metin çizme

## Giriş

Bu adım‑adım kılavuzda Aspose.Drawing for .NET kullanarak **görüntü üzerine metin çizme** öğrenirsiniz. *Dinamik metin görüntüsü* oluşturmanız, mevcut bir bitmap'e metin eklemeniz veya özel yazı tipleriyle bir grafik üretmeniz gerekirse, bu öğretici her ayrıntıyı size gösterir, böylece dakikalar içinde metin çizmeye başlayabilirsiniz. Kütüphane 30’dan fazla GDI+ metodunu destekler, Windows, Linux ve macOS'ta çalışır ve **sıfır dış bağımlılık** içerir; bu da sunucu‑tarafı görüntü üretimi için güvenilir bir seçim olmasını sağlar.

## Hızlı cevaplar
- **Hangi kütüphane kullanılıyor?** Aspose.Drawing for .NET  
- **Ana görev?** Bir görüntü üzerine metin çizme (metinli görüntü oluşturma)  
- **Ana yöntem?** `Graphics.DrawString` (görüntü üzerine dize çizme)  
- **Çıktı formatı?** PNG (bitmap'i PNG olarak kaydetme)  
- **Önkoşullar?** .NET geliştirme ortamı ve Aspose.Drawing kütüphanesi  

## Aspose.Drawing ile metin çizmek nedir?

Aspose.Drawing ile metin çizmek, kütüphanenin GDI+‑uyumlu API'sını kullanarak Unicode dizgilerini bir raster kanvas üzerine işlemek anlamına gelir. `Graphics.DrawString` yöntemi metni bir bitmap'e yazar, böylece yazı tipi, renk, hizalama ve anti‑aliasing kontrol edilebilir. Bu yaklaşım, System.Drawing.Common yüklemeden yüksek‑kaliteli görüntüler üretmenizi sağlar.

## Neden Aspose.Drawing'i görüntülere metin eklemek için kullanmalısınız?

Aspose.Drawing, yerel GDI+ kütüphanelerine ihtiyaç duymadan metni görüntülere işlemek için güvenilir, çapraz‑platform bir yol sunar; herhangi bir işletim sisteminde tutarlı kalite ve performans sağlar. Gelişmiş anti‑aliasing, Unicode karakterleri ve özel yazı tiplerini destekler ve .NET uygulamalarıyla sorunsuz entegrasyon sağlar; bu da sunucu‑tarafı görüntü üretimi ve masaüstü araçları için idealdir.

- **Cross‑platform reliability** – Windows, Linux ve macOS'ta çalışır.  
- **Advanced rendering** – keskin çıktı için anti‑aliasing ve alt‑piksel metin yumuşatma.  
- **No external dependencies** – kütüphane, *metinli görüntü oluşturma* için ihtiyacınız olan her şeyi paketler.

## Önkoşullar

İlerlemeye başlamadan önce şunlara sahip olduğunuzdan emin olun:

- **Aspose.Drawing for .NET** – bunu [Aspose.Drawing belgeleri](https://reference.aspose.com/drawing/net/) üzerinden indirin.  
- **Bir .NET IDE** örneğin Visual Studio veya VS Code.  

## Ad alanlarını içe aktar

Gerekli ad alanlarını içe aktararak başlayın:

Bu ad alanları `Bitmap`, `Graphics` ve metin işleme yardımcıları gibi temel GDI+ türlerini sağlar.  
```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Adım 1: bitmap ve graphics nesnelerini oluşturma

`Bitmap`, Aspose.Drawing'in piksel verileri için raster görüntü kapsayıcısıdır ve `Graphics`, şekil ve metin çizmeye yarayan yöntemleri sunar.  

`Bitmap` bellekte bir görüntüyü temsil ederken, `Graphics` o bitmap üzerine çizmeye yarayan yöntemleri sağlar.  
```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

Burada, son resmi tutacak bir `Bitmap` ve üzerine çizmeyi sağlayan bir `Graphics` nesnesi oluşturuyoruz. Anti‑aliasing ipucu, metnin pürüzsüz görünmesini sağlar.

## Adım 2: fırça, kalem ve yazı tipini ayarlama

`Brush` doldurma rengini, `Pen` şekil kenarlarını ve `Font` metin işleme için tipografi, boyut ve stili belirler.  

`Brush` şekilleri renk ile doldurur, `Pen` kenarları çizer ve `Font` metin işleme için tipografi ve boyutu tanımlar.  
```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

- **Brush** metin rengini tanımlar.  
- **Pen** daha sonra metnin etrafına bir dikdörtgen çizmek için kullanılır (isteğe bağlı).  
- **Font** *görüntü üzerine dize çizme* işlemi için tipografi, boyut ve stili belirler.

## Adım 3: metin ve dikdörtgeni tanımlama

`Rectangle` metnin yerleştirileceği sınırlayıcı kutuyu tanımlar; X/Y koordinatları ve genişlik/yükseklik belirlenir.  

`Rectangle` burada çizilen metni sınırlayan dikdörtgenin konum ve boyutunu belirtir.  
```csharp
string text = "Lorem ipsum..."; // (Your desired text)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
```

`Rectangle`, metnin nerede yer alacağını belirler. Düzeninize uygun şekilde koordinatları ve boyutu ayarlayın.

## Adım 4: dikdörtgen ve metni çizme

`Graphics.DrawString` belirtilen metni, verilen font ve fırça ile belirli bir dikdörtgen içinde işler.  

`Graphics.DrawString` verilen font ve fırça ile belirli bir dikdörtgen içinde bir metin dizesi çizer.  
```csharp
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle);
```

İlk olarak alanı mavi bir dikdörtgenle çerçeveliyoruz, ardından `DrawString` çağrısıyla **bitmap'e metin ekliyoruz**. Bu, görüntü üzerine *metin çizme* işleminin çekirdeğidir.

## Adım 5: sonucu kaydetme

Görüntü, *bitmap'i PNG olarak kaydetme* gereksinimini karşılayarak PNG dosyası olarak kaydedilir. Yer tutucu yolu, dosyanın kaydedileceği gerçek klasörle değiştirin.  

`bitmap.Save` görüntüyü seçilen formatta, örneğin PNG, bir dosyaya yazar.  
```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\DrawText_out.png");
```

## Yaygın kullanım senaryoları

- **Kişiselleştirilmiş isimlerle sertifika** oluşturma.  
- **Web galerileri için filigranlı küçük resimler** oluşturma.  
- **Etiket veya açıklama içeren dinamik grafikler** oluşturma.  

## Sorun giderme ve ipuçları

- **Yazı tipi bulunamadı mı?** Yazı tipinin host makinede yüklü olduğundan emin olun veya özel bir yazı tipi koleksiyonu kullanın.  
- **Metin kesiliyor mu?** Dikdörtgen boyutunu artırın veya yazı tipi boyutunu küçültün.  
- **Performans kaygıları?** Mümkün olduğunca aynı `Graphics` nesnesini birden çok çizim işlemi için yeniden kullanın.  

## Sıkça sorulan sorular

**S: Çıktı formatını JPEG olarak nasıl değiştiririm?**  
C: `Save` metodundaki `.png` uzantısını `.jpg` ile değiştirin ve isteğe bağlı olarak JPEG kalitesi için bir `ImageCodecInfo` belirtin.

**S: Çok satırlı metin çizebilir miyim?**  
C: Evet, dizede satır sonu karakterleri (`\n`) ekleyin veya `StringFormat` ile `FormatFlags.LineLimit` kullanın.

**S: Çizmeden önce metin boyutunu ölçmenin bir yolu var mı?**  
C: `Graphics.MeasureString` kullanarak işlenen metnin tam boyutlarını alabilirsiniz.

**S: Aspose.Drawing Unicode karakterleri destekliyor mu?**  
C: Kesinlikle. Gerekli glifleri içeren bir yazı tipi sağlayın, kütüphane bunları doğru şekilde render eder.

**S: Test için hangi Aspose.Drawing sürümü kullanıldı?**  
C: Örnekler Aspose.Drawing 24.11 for .NET ile test edilmiştir.

---

**Son Güncelleme:** 2026-09-23  
**Test Edilen:** Aspose.Drawing 24.11 for .NET  
**Yazar:** Aspose

## İlgili Eğitimler

- [Bitmap Grafik Oluşturma C# – PNG Görüntüsü Kaydetme ve Aspose.Drawing'de Yüklü Yazı Tipleriyle Çalışma](/drawing/net/text-and-fonts/installed-fonts/)
- [Aspose.Drawing API for .NET kullanarak bitmap'i PNG olarak kaydetme](/drawing/net/image-editing/display/)
- [Görüntü Üzerinde Metin](/drawing/net/use-cases/text-on-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}