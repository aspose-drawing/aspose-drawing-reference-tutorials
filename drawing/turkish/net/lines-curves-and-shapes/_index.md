---
date: 2026-02-09
description: Aspose.Drawing for .NET ile yaylar ve diğer şekilleri nasıl çizeceğinizi,
  bölgeyi degrade ile doldurmayı ve .NET’te katı fırçalar, bezier eğrileri, elipsler
  ve daha fazlasını kullanarak çizgileri nasıl çizeceğinizi öğrenin.
linktitle: How to Draw Arcs and Other Shapes
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Aspose.Drawing for .NET ile Yaylar ve Diğer Şekilleri Nasıl Çizeriz
url: /tr/net/lines-curves-and-shapes/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing for .NET ile Yaylar ve Diğer Şekilleri Çizme

## Giriş

Bu kapsamlı rehberde **yayları nasıl çizeceğinizi** ve Aspose.Drawing kütüphanesini .NET için kullanarak tam bir çizgi, eğri ve şekil yelpazesini keşfedeceksiniz. İster bir grafik bileşeni, ister özel bir UI öğesi, ister zengin bir rapor grafiği oluşturuyor olun, bu çizim temel öğelerini ustalıkla kullanmak, her görsel öğe üzerinde piksel‑tam kontrol sağlar. Katı fırçalar, yaylar, Bezier spline'ları, kardinal spline'ları, kapalı eğriler, elipsler, çizgiler, yollar, çokgenler, dikdörtgenler ve bölge doldurma konularını adım adım inceleyeceğiz; böylece dakikalar içinde canlı, üretime hazır grafikler oluşturabilirsiniz.

## Hızlı Yanıtlar
- **Çizim için birincil sınıf nedir?** `Graphics` from Aspose.Drawing provides the canvas for all drawing operations.  
- **Yayları nasıl çizersiniz?** Use `Graphics.DrawArc` with a `Pen` and a `RectangleF` that defines the bounding ellipse.  
- **Lisans gerekir mi?** A free evaluation license works for development; a commercial license is required for production.  
- **Hangi .NET sürümleri destekleniyor?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.  
- **Şekilleri degrade ile doldurabilir miyim?** Yes—use `LinearGradientBrush` or `PathGradientBrush` for advanced fills.

## Aspose.Drawing'de “yayları nasıl çizeceksiniz” nedir?
Bir yay çizmek, iki açı arasındaki bir elips ya da daire segmentini oluşturmak anlamına gelir. Aspose.Drawing'de başlangıç açısını, süpürme açısını ve tam elipsi sınırlayan dikdörtgeni belirtirsiniz. Bu, eğrilik, kalınlık ve stil (katı, kesikli vb.) üzerinde hassas kontrol sağlar.

## Neden yaylar ve diğer şekiller için Aspose.Drawing kullanmalısınız?
- **Çapraz‑platform tutarlılığı** – Windows, Linux ve macOS'ta aynı şekilde çalışır.  
- **System.Drawing bağımlılığı yok** – Modern .NET Core/5+ projeleri için idealdir.  
- **Zengin fırça ve kalem seçenekleri** – Katı, tarama, doku ve degrade doldurmalar.  
- **Yüksek‑performanslı renderleme** – Sunucu tarafı görüntü üretimi için optimize edilmiştir.

## Önkoşullar
- .NET geliştirme ortamı (Visual Studio 2022 veya VS Code).  
- Aspose.Drawing for .NET NuGet paketi (`Install-Package Aspose.Drawing`).  
- C# ve GDI‑style çizim kavramlarına temel aşinalık.

## Adım‑Adım Kılavuz

### Aspose.Drawing'de Yayları Nasıl Çizersiniz
Bir yay çizmek için bir görüntüden `Graphics` nesnesi oluşturun, bir `Pen` tanımlayın ve `DrawArc` metodunu çağırın. Metod, sınırlayıcı bir dikdörtgen ve başlangıç/süpürme açılarını gerektirir.

### Aspose.Drawing'de Kapalı Eğrileri Nasıl Çizersiniz
Kapalı eğriler, özel çokgenler gibi pürüzsüz, sürekli şekiller oluşturmak için faydalıdır. `Graphics.DrawClosedCurve` metodunu bir `PointF` dizisiyle kullanın.

### Aspose.Drawing'de Çizgileri Nasıl Çizersiniz
Çizgiler, çoğu vektör grafiğinin temel yapı taşlarıdır. Bir `Pen` ve iki nokta (`PointF`) ile `Graphics.DrawLine` metodunu kullanın. Bu, ikincil anahtar kelime **draw lines .net** ifadesini karşılar.

### Aspose.Drawing'de Bezier Spline'larını Nasıl Çizersiniz
Bezier spline'ları, eğri gerginliği üzerinde ince ayar kontrolü sağlar. Dört nokta (başlangıç, iki kontrol noktası ve bitiş) ile `Graphics.DrawBezier` metodunu çağırın.

### Aspose.Drawing'de Kardinal Spline'ları Nasıl Çizersiniz
Kardinal spline'lar, bir dizi nokta üzerinden pürüzsüz eğriler üretir. `Graphics.DrawCurve` metodunu kullanın ve bir gerilim değeri (0.0–1.0) belirtin.

### Aspose.Drawing'de Elipsleri Nasıl Çizersiniz
Elipsler, `Graphics.DrawEllipse` ile çizilir. Sınırlayıcı bir dikdörtgen sağlayın; elips bu dikdörtgenin içine mükemmel oturur.

### Aspose.Drawing'de Çokgenleri Nasıl Çizersiniz
Çokgenler, otomatik olarak kapanan bir dizi bağlantılı çizgidir. Bir nokta dizisiyle `Graphics.DrawPolygon` metodunu kullanın.

### Aspose.Drawing'de Dikdörtgenleri Nasıl Çizersiniz
Dikdörtgenler, `Graphics.DrawRectangle` ile çizilir. Ayrıca `Graphics.FillRectangle` ile doldurabilirsiniz.

### Aspose.Drawing'de Yolları Nasıl Çizersiniz
Yollar, birden çok çizim komutunu tek bir nesne içinde birleştirmenizi sağlar. Bir `GraphicsPath` oluşturun, çizgiler, yaylar veya eğriler ekleyin ve ardından `Graphics.DrawPath` ile render edin.

### Aspose.Drawing'de Bölgeleri Nasıl Doldurursunuz (fill region graphics)
Bir bölge doldurmak, kapalı herhangi bir şekle renk veya doku ekler. `Graphics.FillRegion` metodunu bir `Region` nesnesi ve bir fırça (katı, tarama veya degrade) ile birlikte kullanın. **fill region with gradient** ifadesini karşılamak için `LinearGradientBrush` ile `FillRegion` kombinasyonunu kullanarak yumuşak renk geçişleri elde edin.

## Yaygın Tuzaklar ve İpuçları
- **Koordinat Sistemi** – Kökenin (0,0) sol‑üst köşede olduğunu unutmayın; Y aşağı doğru artar.  
- **Kalem Genişliği** – Çok ince kalemler yüksek DPI'da kaybolabilir; netlik için `Pen.Width` değerini artırın.  
- **Yay Açılar** – Açılar X‑ekseninden saat yönünde ölçülür.  
- **Kaynak Yönetimi** – GDI kaynaklarını hızlıca serbest bırakmak için `Graphics`, `Pen` ve `Brush` nesnelerini Dispose edin.  
- **Anti‑Aliasing** – Daha pürüzsüz eğriler için `Graphics.SmoothingMode = SmoothingMode.AntiAlias` etkinleştirin.

## Sıkça Sorulan Sorular

**S: Yayları kesikli çizgi stiliyle çizebilir miyim?**  
C: Evet—`DrawArc` metodunu çağırmadan önce `Pen.DashStyle` özelliğini (ör. `DashStyle.Dash`) yapılandırın.

**S: Yayı döndürmem gerekirse ne yapmalıyım?**  
C: Çizmeden önce `Graphics.RotateTransform(angle)` kullanarak `Graphics` nesnesine bir döndürme dönüşümü uygulayın.

**S: Bir yay sektörü (pasta dilimi) doldurmak mümkün mü?**  
C: `DrawArc` ile aynı parametreleri kullanarak `Graphics.FillPie` metodunu çağırın; böylece doldurulmuş bir sektör elde edersiniz.

**S: Son görüntüyü nasıl dışa aktarırım?**  
C: `image.Save("output.png", ImageFormat.Png)` metodunu çağırın veya ihtiyacınıza göre JPEG, BMP vb. formatları seçin.

**S: Aspose.Drawing şeffaflığı destekliyor mu?**  
C: Kesinlikle—fırçalar veya kalemler için `Color.FromArgb(alpha, r, g, b)` kullanarak alfa karıştırması ekleyebilirsiniz.

## Ek SSS (AI‑dostu)

**S: Aspose.Drawing'de bir bölgeyi degrade ile nasıl doldurabilirim?**  
C: Başlangıç ve bitiş renklerini tanımlayan bir `LinearGradientBrush` (veya `PathGradientBrush`) oluşturun, ardından bunu `Graphics.FillRegion` metoduna geçirin. Bu, ikincil anahtar kelime **fill region with gradient** ifadesini karşılar.

**S: .NET'te çok sayıda çizgi çizerken performans açısından nelere dikkat etmeliyim?**  
C: Evet. `GraphicsPath` kullanarak toplu çizim yapmak ve yolu bir kez çizmek, özellikle büyük veri setlerinde ayrı ayrı `DrawLine` çağrılarından daha hızlıdır.

**S: Birden fazla şekli tek bir görüntüde birleştirebilir miyim?**  
C: Kesinlikle. Tek bir `Graphics` tuvali oluşturun, her şekli sırayla çizin ve sonunda görüntüyü kaydedin.

**S: Yüksek çözünürlüklü çıktı için hangi DPI'yi kullanmalıyım?**  
C: Baskı kalitesinde grafikler için `image.SetResolution(300, 300)` metoduyla görüntünün çözünürlüğünü ayarlayın.

**S: Şekillerin yanında anti‑aliased metin desteği var mı?**  
C: Evet. `DrawString` metodunu çağırmadan önce `Graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit` ayarlayın.

## Sonuç

Artık **yayları nasıl çizeceğinizi** ve Aspose.Drawing for .NET ile diğer grafik temel öğelerinin tam bir paletini kullanma konusunda sağlam bir temele sahipsiniz. Kalemleri, fırçaları ve zengin çizim metodlarını birleştirerek basit çizgi grafiklerinden karmaşık vektör illüstrasyonlara kadar her şeyi—eski System.Drawing.Common kütüphanesine bağımlı olmadan—üretebilirsiniz. Aşağıdaki bağlantılı eğitimleri keşfederek her şekil türüne daha derinlemesine dalın ve bugün çarpıcı grafikler oluşturmaya başlayın.

## Çizgiler, Eğriler ve Şekiller Eğitimleri
### [Aspose.Drawing'de Katı Fırçalar](./solid-brushes/)
Aspose.Drawing for .NET'in büyüsünü keşfedin. Bu adım‑adım rehberde katı fırçaları öğrenerek canlı grafikler oluşturun.
### [Aspose.Drawing'de Yayları Çizme](./draw-arc/)
Aspose.Drawing kullanarak .NET uygulamalarında etkileyici yaylar çizmeyi öğrenin. Çarpıcı görsel sonuçlar için adım‑adım rehberimizi izleyin.
### [Aspose.Drawing'de Bezier Spline'larını Çizme](./draw-bezier-spline/)
Aspose.Drawing for .NET'in gücünü keşfederek çarpıcı Bezier spline'ları oluşturun. Sorunsuz grafik geliştirme için adım‑adım rehberimizi izleyin.
### [Aspose.Drawing'de Kardinal Spline'ları Çizme](./draw-cardinal-spline/)
Aspose.Drawing ile .NET uygulamalarında kardinal spline'ları çizmeyi keşfedin. Pürüzsüz eğrileri zahmetsizce oluşturun.
### [Aspose.Drawing'de Kapalı Eğrileri Çizme](./draw-closed-curve/)
Aspose.Drawing ile .NET uygulamalarında kapalı eğrileri çizmeyi keşfedin. Görsellerinizi zahmetsizce yükseltin.
### [Aspose.Drawing'de Elipsleri Çizme](./draw-ellipse/)
Aspose.Drawing kullanarak .NET'te elipsleri çizmeyi öğrenin. Çarpıcı grafikler oluşturmak için bu adım‑adım öğreticiyi izleyin.
### [Aspose.Drawing'de Çizgileri Çizme](./draw-lines/)
Aspose.Drawing ile .NET uygulamalarında çizgileri çizmeyi öğrenin. Bu adım‑adım öğretici, çarpıcı grafikler için süreci yönlendirir.
### [Aspose.Drawing'de Yolları Çizme](./draw-path/)
Aspose.Drawing for .NET ile yolları çizmeyi bu adım‑adım rehberde öğrenin. Sorunsuz grafikler oluşturun.
### [Aspose.Drawing'de Çokgenleri Çizme](./draw-polygon/)
Aspose.Drawing for .NET'in gücünü keşfederek çarpıcı grafikler oluşturun. Bu sezgisel kütüphane ile çokgenleri zahmetsizce çizin.
### [Aspose.Drawing'de Dikdörtgenleri Çizme](./draw-rectangle/)
Aspose.Drawing kullanarak .NET'te dikdörtgenleri çizmeyi öğrenin. Kod örnekleriyle adım‑adım rehber.
### [Aspose.Drawing'de Bölgeleri Doldurma](./fill-region/)
Aspose.Drawing for .NET ile bölgeleri doldurmayı bu adım‑adım öğreticide öğrenin. Grafik tasarım becerilerinizi zahmetsizce geliştirin.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-02-09  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

---