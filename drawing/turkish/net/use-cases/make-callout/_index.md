---
date: 2026-08-01
description: Aspose.Drawing for .NET kullanarak görüntülere callouts eklemeyi öğrenin
  – adım adım rehber, kod yer tutucuları, ipuçları ve SSS.
keywords:
- how to add callouts
- Aspose.Drawing callout tutorial
- .NET image annotation
lastmod: 2026-08-01
linktitle: Aspose.Drawing'de Callouts Oluşturma
og_description: Aspose.Drawing for .NET'te callouts eklemeyi keşfedin. Bu öğreticide
  ön koşullar, adım adım uygulama, ipuçları ve geliştiriciler için SSS yer alıyor.
og_image_alt: Screenshot showing callout annotation on an image using Aspose.Drawing
og_title: Aspose.Drawing for .NET ile Callouts Nasıl Eklenir – Hızlı Rehber
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to add callouts to images using Aspose.Drawing for .NET –
    step‑by‑step guide with code placeholders, tips, and FAQs.
  headline: How to Add Callouts with Aspose.Drawing for .NET
  type: TechArticle
- questions:
  - answer: Yes, Aspose.Drawing supports a wide range of drawing operations for diagrams,
      charts, and custom graphics beyond simple callouts.
    question: Can I use Aspose.Drawing for other types of illustrations?
  - answer: Absolutely! Aspose.Drawing handles PNG, JPEG, GIF, BMP, TIFF, and many
      more formats.
    question: Is Aspose.Drawing compatible with different image formats?
  - answer: Explore the comprehensive documentation [here](https://reference.aspose.com/drawing/net/).
    question: Where can I find more examples and documentation?
  - answer: Visit the [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44)
      for community assistance and official support.
    question: How do I get support if I encounter issues?
  - answer: Certainly! Get started with a free trial [here](https://releases.aspose.com/).
    question: Can I try Aspose.Drawing before purchasing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- callout
- Aspose.Drawing
- .NET graphics
- image annotation
title: Aspose.Drawing for .NET ile Callouts Nasıl Eklenir
url: /tr/net/use-cases/make-callout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing for .NET ile Çağrı Kutuları Nasıl Eklenir

## Giriş
Aspose.Drawing for .NET kullanarak görüntülerinize veya diyagramlarınıza **çağrı kutuları nasıl eklenir** diye bakıyorsanız, doğru yerdesiniz. Bu öğreticide her adımı—bitmap yüklemekten, bir `Graphics` tuvali oluşturmaya, çağrı kutusu geometrisini tanımlamaya, stilize çağrı kutularını render etmeye—gezerek görsellerinizin daha net ve bilgilendirici olmasını sağlayacağız.

## Hızlı Yanıtlar
- **Hangi kütüphane gerekiyor?** Aspose.Drawing for .NET (resmi siteden indirilebilir).  
- **Hangi .NET sürümleri destekleniyor?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Lisans gerekli mi?** Geliştirme için ücretsiz deneme çalışır; üretim için ticari lisans gereklidir.  
- **Uygulama ne kadar sürer?** Temel bir çağrı kutusu için genellikle 10 dakikadan az.  
- **Renkleri ve yazı tiplerini özelleştirebilir miyim?** Evet—her şey standart GDI+ nesneleri (Pen, Font, Brush) ile kontrol edilir.

## Çağrı Kutusu Nedir?
Çağrı kutusu, bir çizgi (veya ok) ile bir metin etiketi birleştirerek bir görüntünün belirli bir bölümünü vurgulayan bir grafik açıklamadır. Teknik diyagramlarda, ekran görüntülerinde ve sunumlarda belirli bir öğeye dikkat çekmek, bir özelliği açıklamak veya ölçüm bilgisi sağlamak için yaygın olarak kullanılır; bu da görsel iletişimi daha net ve etkili kılar.

## Neden Aspose.Drawing ile Çağrı Kutuları Kullanılır?
Aspose.Drawing, yüksek performanslı görüntü işleme için tasarlanmıştır ve geniş bir format yelpazesini destekler; bu da büyük veya karmaşık grafiklere çağrı kutuları eklemek için idealdir. Bellek‑verimli mimarisi, tüm bitmap'i RAM'e yüklemeden **500 MB**'a kadar dosyaları işleyebilir ve çizim temel öğeleri, renkler ve metin render'ı üzerinde ince kontrol sunar; bu da net ve profesyonel görünümlü açıklamalar sağlar.

## Önkoşullar
İçeriğe girmeden önce şunlara sahip olduğunuzdan emin olun:

- C# programlama dili hakkında temel bilgi.  
- Aspose.Drawing kütüphanesi yüklü. Bunu [buradan](https://releases.aspose.com/drawing/net/) indirebilirsiniz.  
- Çağrı kutuları eklemek istediğiniz bir belge veya görüntü.

## Ad Alanlarını İçe Aktarın
Aşağıdaki ad alanları, temel çizim sınıflarına erişim sağlar:

`System.Drawing`, `Bitmap`, `Graphics`, `Pen`, `Font` ve `Brush` gibi GDI+ türlerini sunar. Kodlamaya başlamadan önce bunları içe aktarın.

```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```

## Aspose.Drawing ile Çağrı Kutuları Nasıl Eklenir
Kaynak görüntünüzü yükleyin, bir `Graphics` tuvali oluşturun, başlangıç/bitiş noktalarını tanımlayın ve çizgi, ok ucu ve etiketi çizen yardımcı yöntemi çağırın—hepsi birkaç özlü ifadeyle. Bu yaklaşım PNG, JPEG, BMP ve GIF dosyaları için çalışır ve renkleri, yazı tiplerini ve çizgi stillerini tamamen özelleştirmenizi sağlar.

## Adım 1: Görüntüyü Yükle
`Image`, bir raster görüntüyü temsil eder ve bitmap verisini yükleme, kaydetme ve manipüle etme yöntemleri sunar. Çağrı kutuları eklemek istediğiniz görüntüyü yükleyerek başlayın. `"Your Document Directory"` ve `"gears.png"` ifadelerini gerçek dizininiz ve görüntü dosya adınızla değiştirin.

```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Your code here
}
```

## Adım 2: Graphics Nesnesi Oluştur
`Graphics`, bir bitmap üzerine şekil, metin ve görüntü render etmek için çizim yüzeyi yöntemleri sunar. Görüntüden elde edilen bir `Graphics` nesnesi, çizim işlemlerini gerçekleştirmenizi sağlar.

```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```

## Adım 3: Çağrı Kutusu Konumlarını Tanımla
`PointF`, kayan nokta koordinatları kullanarak iki boyutlu bir uzayda bir noktayı tanımlar. Her çağrı kutusu için başlangıç (çapa) ve bitiş (etiket) noktalarını belirtin. Bu koordinatlar görüntü sınırları içinde olmalıdır; aksi takdirde çağrı kutusu kırpılır.

```csharp
PointF startAnchor1 = new PointF(107, 55);
PointF endAnchor1 = new PointF(179, 5);
int value1 = 74;
string unit1 = "mm";
PointF startAnchor2 = new PointF(111, 146);
PointF endAnchor2 = new PointF(29, 180);
int value2 = 28;
string unit2 = "mm";
```

## Adım 4: Çağrı Kutularını Çiz
`DrawCallOut` metodunu, çizgi, isteğe bağlı ok ucu ve metin etiketini render edecek şekilde uygulayın. Metot, çizgi için `Pen`, etiket için `Font` ve dolgu renkleri için `SolidBrush` kullanır.

```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```

## Adım 5: Görüntüyü Kaydet
Açıklamalı bitmap'i diske kaydedin. PNG veya JPEG gibi desteklenen herhangi bir formatı seçebilirsiniz.

```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```

## Çağrı Kutusu Kaynak Kodu
Tüm adımları birleştiren tam kaynak kodu aşağıdaki yer tutucuda bulunur. Belirtilen yerlere kendi uygulama detaylarınızı ekleyin.

```csharp
void DrawCallOut(Graphics graphic, PointF startAnchor, PointF endAnchor, int value, string unit)
            {
                Pen pen = new Pen(Color.DarkGray, 1);
                Font font = new Font("Arial", 10, FontStyle.Bold);
                string outputValue = $"{value} {unit}";
                var textSize = graphic.MeasureString(outputValue, font);
                int diameterSymbolSize = 12;
                int spaceSize = 3;
                textSize.Width += diameterSymbolSize + spaceSize;
                float callOutMiddleX = endAnchor.X > startAnchor.X ? endAnchor.X - textSize.Width : endAnchor.X + textSize.Width;
                float callOutMiddleY = endAnchor.Y > startAnchor.Y ? endAnchor.Y - textSize.Height : endAnchor.Y + textSize.Height;
                graphic.DrawLine(pen, startAnchor.X, startAnchor.Y, callOutMiddleX, callOutMiddleY);
                float textAnchorX = Math.Min(callOutMiddleX, endAnchor.X);
                float textAnchorY = callOutMiddleY;
                graphic.DrawLine(pen, callOutMiddleX, callOutMiddleY, textAnchorX == callOutMiddleX ? textAnchorX + textSize.Width : textAnchorX, callOutMiddleY);
                graphic.DrawEllipse(pen, new Rectangle((int)textAnchorX + spaceSize, (int)(textAnchorY - textSize.Height) + spaceSize, 10, 10));
                graphic.DrawLine(pen, (int)textAnchorX + 1, (int)textAnchorY - 1, (int)textAnchorX + diameterSymbolSize + 2, (int)textAnchorY - diameterSymbolSize - 2);
                SolidBrush brush = new SolidBrush(Color.DarkGray);
                graphic.DrawString(outputValue, font, brush, (int)textAnchorX + diameterSymbolSize + spaceSize, (int)(textAnchorY - textSize.Height));
            }
```

## Yaygın Sorunlar ve İpuçları
- **Yanlış çapa koordinatları** – başlangıç ve bitiş noktalarının görüntü sınırları içinde olduğundan emin olun; aksi takdirde çağrı kutusu kırpılabilir.  
- **Metin çakışması** – etiket diğer grafiklerle çarpışıyorsa `spaceSize` veya yazı tipi boyutunu ayarlayın.  
- **Performans** – çok büyük görüntülerde, kaynakları serbest bırakmak için kullanım sonrası `Pen`, `Font` ve `Brush` nesnelerini dispose etmeyi düşünün.

## Sonuç
Artık Aspose.Drawing for .NET kullanarak herhangi bir görüntüye **çağrı kutuları nasıl eklenir** konusunda eksiksiz, üretim‑hazır bir deseniniz var. Markanıza uygun farklı renkler, çizgi stilleri ve yazı tipi aileleriyle denemeler yapmaktan çekinmeyin.

## Sıkça Sorulan Sorular

**S: Aspose.Drawing'ı başka tür illüstrasyonlar için kullanabilir miyim?**  
C: Evet, Aspose.Drawing basit çağrı kutularının ötesinde diyagramlar, grafikler ve özel grafikler için geniş bir çizim operasyonları yelpazesini destekler.

**S: Aspose.Drawing farklı görüntü formatlarıyla uyumlu mu?**  
C: Kesinlikle! Aspose.Drawing PNG, JPEG, GIF, BMP, TIFF ve daha birçok formatı işleyebilir.

**S: Daha fazla örnek ve belgeyi nerede bulabilirim?**  
C: Kapsamlı belgeleri [buradan](https://reference.aspose.com/drawing/net/) inceleyin.

**S: Sorunlarla karşılaşırsam nasıl destek alabilirim?**  
C: Topluluk yardımı ve resmi destek için [Aspose.Drawing forumunu](https://forum.aspose.com/c/drawing/44) ziyaret edin.

**S: Aspose.Drawing'ı satın almadan deneyebilir miyim?**  
C: Elbette! Ücretsiz deneme sürümüyle [buradan](https://releases.aspose.com/) başlayabilirsiniz.

---

**Son Güncelleme:** 2026-08-01  
**Test Edilen Versiyon:** Aspose.Drawing 24.11 for .NET  
**Yazar:** Aspose  

{{< blocks/products/products-backtop-button >}}

## İlgili Öğreticiler

- [Aspose.Drawing for .NET ile Yaylar ve Diğer Şekiller Nasıl Çizilir](/drawing/net/lines-curves-and-shapes/)
- [Matris Dönüşümü Öğreticisi: Aspose.Drawing for .NET'te Matris Dönüşümleri](/drawing/net/coordinate-transformations/matrix-transformations/)
- [Aspose.Drawing .NET'te Pen ile Yollar Nasıl Birleştirilir](/drawing/net/pens/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}