---
date: 2025-12-05
description: Aspose.Drawing for .NET ile yaylar ve diğer şekilleri çizmeyi öğrenin.
  Katı fırçaları ustalaşın, Bezier spline, elipsler ve daha fazlasını canlı grafik
  öğreticilerinde çizin.
language: tr
linktitle: How to Draw Arcs and Other Shapes
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Aspose.Drawing for .NET ile Yaylar ve Diğer Şekilleri Çizme
url: /net/lines-curves-and-shapes/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing for .NET ile Yaylar ve Diğer Şekilleri Çizme

## Giriş

Bu kapsamlı rehberde Aspose.Drawing kütüphanesini kullanarak **yayları nasıl çizeceğinizi** ve çizgiler, eğriler ve şekiller bütününü keşfedeceksiniz. İster bir grafik bileşeni, ister özel bir UI öğesi, ister zengin bir rapor grafiği oluşturuyor olun, bu çizim temel öğelerini ustalıkla kullanarak her görsel öğe üzerinde piksel‑tam kontrol sağlayabilirsiniz. Katı fırçalar, yaylar, Bezier splineleri, kardinal splineleri, kapalı eğriler, elipsler, çizgiler, yollar, çokgenler, dikdörtgenler ve bölge doldurma konularını adım adım inceleyecek, dakikalar içinde canlı, üretime hazır grafikler oluşturabileceksiniz.

## Hızlı Yanıtlar
- **Çizim için birincil sınıf nedir?** Aspose.Drawing'den `Graphics`, tüm çizim işlemleri için tuval görevi görür.  
- **Yaylar nasıl çizilir?** `Graphics.DrawArc` metodunu bir `Pen` ve sınırlayıcı elipsi tanımlayan `RectangleF` ile kullanın.  
- **Lisans gerekli mi?** Geliştirme için ücretsiz deneme lisansı yeterlidir; üretim ortamı için ticari lisans gerekir.  
- **Hangi .NET sürümleri destekleniyor?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.  
- **Şekiller gradient ile doldurulabilir mi?** Evet—ileri düzey doldurmalar için `LinearGradientBrush` veya `PathGradientBrush` kullanın.

## Aspose.Drawing'de “yayları nasıl çizerim” nedir?
Bir yay çizmek, bir elips ya da dairenin iki açı arasındaki segmenti oluşturmak demektir. Aspose.Drawing'de başlangıç açısı, süpürme açısı ve tam elipsi sınırlayan dikdörtgeni belirtirsiniz. Bu sayede eğrilik, kalınlık ve stil (katı, kesikli vb.) üzerinde hassas kontrol elde edersiniz.

## Neden Aspose.Drawing ile yaylar ve diğer şekiller?
- **Çapraz‑platform tutarlılığı** – Windows, Linux ve macOS'ta aynı şekilde çalışır.  
- **System.Drawing bağımlılığı yok** – Modern .NET Core/5+ projeler için idealdir.  
- **Zengin fırça ve kalem seçenekleri** – Katı, çapraz, doku ve gradient doldurmalar.  
- **Yüksek performanslı render** – Sunucu‑tarafı görüntü üretimi için optimize edilmiştir.

## Önkoşullar
- .NET geliştirme ortamı (Visual Studio 2022 veya VS Code).  
- Aspose.Drawing for .NET NuGet paketi (`Install-Package Aspose.Drawing`).  
- C# ve GDI‑stil çizim kavramlarına temel aşinalık.

## Adım‑Adım Kılavuz

### Aspose.Drawing'de Yayları Nasıl Çizerim
Yay çizmek için bir görüntüden `Graphics` nesnesi oluşturun, bir `Pen` tanımlayın ve `DrawArc` metodunu çağırın. Metod, sınırlayıcı bir dikdörtgen ile başlangıç ve süpürme açılarını ister.

### Aspose.Drawing'de Kapalı Eğrileri Nasıl Çizerim
Kapalı eğriler, özel çokgenler gibi pürüzsüz, sürekli şekiller oluşturmak için kullanışlıdır. `Graphics.DrawClosedCurve` metodunu `PointF` dizisiyle kullanın.

### Aspose.Drawing'de Çizgileri Nasıl Çizerim
Çizgiler, çoğu vektör grafiğinin temel yapı taşlarıdır. `Graphics.DrawLine` metodunu bir `Pen` ve iki nokta (`PointF`) ile kullanın.

### Aspose.Drawing'de Bezier Splineleri Nasıl Çizerim
Bezier splineleri, eğri gerilimini ince ayar yapmanızı sağlar. `Graphics.DrawBezier` metodunu dört nokta ile çağırın: başlangıç, iki kontrol noktası ve bitiş.

### Aspose.Drawing'de Kardinal Splineleri Nasıl Çizerim
Kardinal splineler, bir dizi nokta üzerinden pürüzsüz eğriler üretir. `Graphics.DrawCurve` metodunu bir gerilim değeri (0.0–1.0) belirterek kullanın.

### Aspose.Drawing'de Elipsleri Nasıl Çizerim
Elipsler, `Graphics.DrawEllipse` ile çizilir. Sınırlayıcı bir dikdörtgen sağlayın; elips bu dikdörtgenin içine mükemmel oturur.

### Aspose.Drawing'de Çokgenleri Nasıl Çizerim
Çokgenler, otomatik olarak kapanan bir dizi bağlı çizgidir. `Graphics.DrawPolygon` metodunu nokta dizisiyle kullanın.

### Aspose.Drawing'de Dikdörtgenleri Nasıl Çizerim
Dikdörtgenler, `Graphics.DrawRectangle` ile çizilir. Ayrıca `Graphics.FillRectangle` ile doldurabilirsiniz.

### Aspose.Drawing'de Yolları Nasıl Çizerim
Yollar, birden çok çizim komutunu tek bir nesnede birleştirmenizi sağlar. Bir `GraphicsPath` oluşturun, çizgiler, yaylar veya eğriler ekleyin ve ardından `Graphics.DrawPath` ile render edin.

### Aspose.Drawing'de Bölgeleri Nasıl Doldururum (bölge grafikleri doldurma)
Bir bölgeyi doldurmak, kapalı bir şekle renk veya doku ekler. `Graphics.FillRegion` metodunu bir `Region` nesnesi ve bir fırça (katı, çapraz veya gradient) ile birlikte kullanın.

## Yaygın Hatalar & İpuçları
- **Koordinat Sistemi** – Kökenin (0,0) sol‑üst köşe olduğunu ve Y ekseninin aşağı doğru arttığını unutmayın.  
- **Kalem Genişliği** – Çok ince kalemler yüksek DPI'da kaybolabilir; netlik için `Pen.Width` değerini artırın.  
- **Yay Açıları** – Açıların ölçümü X‑ekseninden saat yönünde yapılır.  
- **Kaynak Yönetimi** – `Graphics`, `Pen` ve `Brush` nesnelerini zamanında `Dispose` ederek GDI kaynaklarını serbest bırakın.  
- **Anti‑Aliasing** – Daha pürüzsüz eğriler için `Graphics.SmoothingMode = SmoothingMode.AntiAlias` etkinleştirin.

## Sık Sorulan Sorular

**S: Yayları kesikli çizgi stiliyle çizebilir miyim?**  
C: Evet—`DrawArc` çağırmadan önce `Pen.DashStyle` özelliğini (ör. `DashStyle.Dash`) ayarlayın.

**S: Yayı döndürmem gerekirse ne yapmalıyım?**  
C: Çizimden önce `Graphics.RotateTransform(angle)` metodunu kullanarak `Graphics` nesnesine bir döndürme dönüşümü uygulayın.

**S: Yay sektörünü (pie dilimini) doldurabilir miyim?**  
C: `DrawArc` ile aynı parametreleri kullanarak `Graphics.FillPie` metodunu çağırın; böylece doldurulmuş bir dilim elde edersiniz.

**S: Son görüntüyü nasıl dışa aktarırım?**  
C: `image.Save("output.png", ImageFormat.Png)` gibi bir komutla kaydedin; ihtiyacınıza göre JPEG, BMP vb. formatları da seçebilirsiniz.

**S: Aspose.Drawing şeffaflığı destekliyor mu?**  
C: Kesinlikle—fırçalar veya kalemler için `Color.FromArgb(alpha, r, g, b)` kullanarak alfa karışımını ekleyebilirsiniz.

## Sonuç

Artık Aspose.Drawing for .NET ile **yayları nasıl çizerim** ve diğer grafik temel öğelerinin tam bir paletini kullanma konusunda sağlam bir temele sahipsiniz. Kalemleri, fırçaları ve zengin çizim metodlarını birleştirerek basit çizgi grafiklerinden karmaşık vektör illüstrasyonlara kadar her şeyi, eski System.Drawing.Common kütüphanesine ihtiyaç duymadan üretebilirsiniz. Aşağıdaki bağlantılı öğreticileri inceleyerek her şekil türüne daha derinlemesine dalın ve bugün çarpıcı grafikler oluşturmaya başlayın.

## Çizgiler, Eğriler ve Şekiller Öğreticileri
### [Aspose.Drawing'de Katı Fırçalar](./solid-brushes/)
Aspose.Drawing for .NET'in büyüsünü keşfedin. Bu adım‑adım rehberde katı fırçaları ustalıkla kullanarak canlı grafikler oluşturun.
### [Aspose.Drawing'de Yayları Çizme](./draw-arc/)
Aspose.Drawing kullanarak .NET uygulamalarında etkileyici yaylar çizmeyi öğrenin. Çarpıcı görsel sonuçlar için adım‑adım rehberimizi izleyin.
### [Aspose.Drawing'de Bezier Splineleri Çizme](./draw-bezier-spline/)
Aspose.Drawing for .NET ile göz alıcı Bezier splineleri oluşturmanın gücünü keşfedin. Kesintisiz grafik geliştirme için adım‑adım rehberimizi izleyin.
### [Aspose.Drawing'de Kardinal Splineleri Çizme](./draw-cardinal-spline/)
Aspose.Drawing kullanarak .NET uygulamalarında kardinal splineler çizmeyi öğrenin. Pürüzsüz eğrileri zahmetsizce oluşturun.
### [Aspose.Drawing'de Kapalı Eğrileri Çizme](./draw-closed-curve/)
Aspose.Drawing ile .NET uygulamalarında kapalı eğrileri çizmeyi keşfedin. Görsellerinizi zahmetsizce yükseltin.
### [Aspose.Drawing'de Elipsleri Çizme](./draw-ellipse/)
Aspose.Drawing kullanarak .NET'te elips çizimini öğrenin. Çarpıcı grafikler oluşturmak için bu adım‑adım öğreticiyi izleyin.
### [Aspose.Drawing'de Çizgileri Çizme](./draw-lines/)
Aspose.Drawing ile .NET uygulamalarında çizgi çizmeyi öğrenin. Bu adım‑adım öğretici, çarpıcı grafikler oluşturmanız için sizi yönlendirecek.
### [Aspose.Drawing'de Yolları Çizme](./draw-path/)
Aspose.Drawing for .NET ile yolları çizmeyi bu adım‑adım rehberde öğrenin. Çarpıcı grafikler oluşturmayı zahmetsizce gerçekleştirin.
### [Aspose.Drawing'de Çokgenleri Çizme](./draw-polygon/)
Aspose.Drawing for .NET'in gücünü kullanarak çarpıcı grafikler oluşturun. Bu sezgisel kütüphane ile çokgenleri zahmetsizce çizin.
### [Aspose.Drawing'de Dikdörtgenleri Çizme](./draw-rectangle/)
Aspose.Drawing kullanarak .NET'te dikdörtgen çizmeyi öğrenin. Kod örnekleriyle adım‑adım rehber.
### [Aspose.Drawing'de Bölgeleri Doldurma](./fill-region/)
Aspose.Drawing for .NET ile bölgeleri doldurmayı bu adım‑adım öğreticide öğrenin. Grafik tasarım becerilerinizi zahmetsizce geliştirin.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Son Güncelleme:** 2025-12-05  
**Test Edilen Sürüm:** Aspose.Drawing 24.11 for .NET  
**Yazar:** Aspose  

---