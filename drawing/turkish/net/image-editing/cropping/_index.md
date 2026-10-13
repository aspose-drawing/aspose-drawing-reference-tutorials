---
date: 2026-10-13
description: Aspose.Drawing API'sini kullanarak PNG'ye toplu görüntü kırpmayı öğrenin;
  .NET geliştiricileri için System.Drawing'in çapraz platform alternatifidir.
keywords:
- how to batch crop
- crop images to png
- batch image cropping
- convert images to png
- batch crop images
lastmod: 2026-10-13
linktitle: Görüntü kırpma öğreticisi – Aspose.Drawing
og_description: Aspose.Drawing'i kullanarak PNG'ye hızlı bir şekilde toplu görüntü
  kırpmayı öğrenin; .NET geliştiricileri için System.Drawing'in çapraz platform alternatifidir.
  Birden fazla dosyayı verimli bir şekilde işlemek için adım adım talimatları izleyin.
og_image_alt: 'Developer guide: batch crop images to PNG using Aspose.Drawing .NET
  API'
og_title: Aspose.Drawing for .NET ile PNG'ye toplu görüntü kırpma
schemas:
- author: Aspose
  dateModified: '2026-10-13'
  description: Learn how to batch crop images to PNG using the Aspose.Drawing API,
    the cross‑platform alternative to System.Drawing for .NET developers.
  headline: How to batch crop images to PNG using Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to batch crop images to PNG using the Aspose.Drawing API,
    the cross‑platform alternative to System.Drawing for .NET developers.
  name: How to batch crop images to PNG using Aspose.Drawing for .NET
  steps:
  - name: Create a bitmap canvas
    text: '`Bitmap` is Aspose.Drawing''s in‑memory representation of an image, providing
      pixel‑level access and format control. We start with a blank canvas sized to
      hold the cropped result. Adjust the width and height to match the dimensions
      of the area you plan to extract.'
  - name: Create a graphics object
    text: '`Graphics` is the drawing surface that lets you render shapes, text, or
      other images onto a Bitmap. A `Graphics` object lets us draw onto the canvas.
      The `InterpolationMode` controls how pixel values are calculated during scaling
      or transformation—`NearestNeighbor` works well for sharp edges.'
  - name: Load the image to crop
    text: '`Image` (or `Bitmap`) loads the source file into memory, ready for manipulation.
      Load the source image. Make sure the path points to an existing file; otherwise
      an exception will be thrown.'
  - name: Define source and destination rectangles
    text: '`Rectangle` objects describe the region of the source image to keep and
      where it should be placed on the destination canvas. The `sourceRectangle` tells
      the API which part of the original image to keep. Here we pick the top‑left
      50 × 40 pixel area. By assigning the same rectangle to `destinationRect'
  - name: Perform the crop operation
    text: '`Graphics.DrawImage` copies the defined portion of `image` onto our blank
      `bitmap`. This is the core **crop image to PNG** operation. The method respects
      the source rectangle and writes only the selected pixels to the destination
      bitmap.'
  - name: Save the cropped image (crop image to PNG)
    text: '`Bitmap.Save` writes the in‑memory bitmap to a file using the specified
      format. Finally, write the canvas to disk as a PNG file. PNG preserves any alpha
      channel and provides lossless quality—ideal for UI assets.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.Drawing supports a wide range of formats (PNG, JPEG, BMP,
      GIF, TIFF, etc.), so you can crop virtually any image type.
    question: Can I crop images of any format using Aspose.Drawing?
  - answer: Absolutely. You can combine `GraphicsPath`, `Matrix` transformations,
      or use the `ImageProcessor` class for more complex selections like circular
      crops.
    question: Are there advanced cropping options available?
  - answer: Yes. After the first crop, you can reuse the resulting bitmap as the new
      source and repeat the process to chain multiple crops.
    question: Can I apply multiple crop operations to a single image?
  - answer: Indeed. Its lightweight API and lack of native dependencies make it perfect
      for processing large image collections on servers.
    question: Is Aspose.Drawing suitable for batch image processing?
  - answer: Head over to the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      to seek assistance and connect with the community.
    question: How can I get support for Aspose.Drawing‑related queries?
  type: FAQPage
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
tags:
- batch image cropping
- Aspose.Drawing
- .NET image processing
- PNG conversion
title: Aspose.Drawing for .NET kullanarak PNG'ye toplu görüntü kırpma
url: /tr/net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PNG'ye toplu görüntü kırpma nasıl yapılır Aspose.Drawing for .NET kullanarak

Eğer .NET ortamında **crop image to PNG** işlemini hızlı, güvenilir ve ölçekli bir şekilde yapmanız gerekiyorsa, doğru yerdesiniz. Bu eğitimde bir görüntüyü yükleme, kırpma alanını tanımlama ve sonucu PNG dosyası olarak kaydetme adımlarını adım adım göstereceğiz—hepsi Aspose.Drawing kullanarak, **System.Drawing**'e modern bir **alternatif** ve çapraz platform çalışabilen bir kütüphane. Ayrıca tek‑görüntü akışını tam bir **toplu kırpma** hattına nasıl genişleteceğinizi de göreceksiniz.

## Hızlı cevaplar
- **Hangi kütüphaneyi kullanmalıyım?** Aspose.Drawing for .NET (System.Drawing.Common'a tam özellikli bir alternatif)  
- **Temel kırpma ne kadar sürer?** Genellikle modern bir CPU'da tek bir görüntü için bir saniyenin altında  
- **PNG'ye kırpabilir miyim?** Evet – kırpılmış bitmap'i PNG dosyası olarak kaydedin (Bkz. Adım 6).  
- **Lisans gerekli mi?** Geliştirme için ücretsiz deneme sürümü çalışır; üretim için ticari lisans gereklidir  
- **Toplu işleme mümkün mü?** Kesinlikle – aynı adımları bir döngü içinde sararak birden fazla dosyayı saniyeler içinde işleyebilirsiniz  

## PNG'ye toplu görüntü kırpma nasıl yapılır?

Her kaynak dosyayı `new Bitmap(path)` ile yükleyin, kırpma alanı için uygun boş bir `Bitmap` oluşturun, seçilen dikdörtgeni `Graphics.DrawImage` ile çizin ve sonunda `Save("output.png", ImageFormat.Png)` çağrısını yapın. Bu altı satırı bir dizini dolaşan bir `foreach` döngüsü içinde sarın ve saniyeler içinde onlarca görüntüyü işleyen tam bir toplu‑kırpma çözümüne sahip olursunuz.

## Neden Aspose.Drawing'ı toplu kırpma için kullanmalısınız?

Aspose.Drawing **Windows, Linux ve macOS** üzerinde çalışır, tipik bir sunucu‑sınıfı CPU'da **500‑üstü piksel görüntüyü 0.5 saniyenin altında** işler ve tam alfa‑kanalı koruması ile **50+ görüntü formatını** destekler. Yerel GDI+ bağımlılıklarını ortadan kaldırdığı için aynı kodu konteynerlere, Azure App Service'e veya AWS Lambda'ya ekstra kütüphaneler olmadan dağıtabilirsiniz; bu da büyük ölçekli görüntü hatları için idealdir.

## “crop image to PNG” nedir?

`crop image to PNG` işlemi, bir kaynak bitmap'ten dikdörtgen bir bölge çıkarır ve bu bölgeyi bir PNG dosyasına yazar. PNG, herhangi bir alfa kanalını korur ve kayıpsız sıkıştırma sağlar; bu da ortaya çıkan görüntüyü küçük resimler, simgeler, UI varlıkları veya kalite ve şeffaflığın gerektiği her durum için ideal kılar.

## Neden Aspose.Drawing, System.Drawing'e bir alternatif?

Aspose.Drawing, tam çapraz platform uyumluluğu sunarak ve yerel GDI+ kütüphanelerine ihtiyaç duymadan System.Drawing için tak‑ası bir değişim sağlar. Geniş bir piksel formatı yelpazesini destekler, yüksek performanslı görüntü işleme sunar ve alfa‑kanalı yönetimi ve kapsamlı format desteği gibi gelişmiş özellikler içerir; bu da hem basit düzenlemeler hem de büyük ölçekli toplu işleme için uygundur.

## Önkoşullar

İçeriğe başlamadan önce şunların olduğundan emin olun:

- **Aspose.Drawing kütüphanesi** .NET projenize entegre edilmiş. Bunu [Aspose.Drawing indirme sayfasından](https://releases.aspose.com/drawing/net/) indirebilirsiniz.  
- Kırpmak istediğiniz kaynak görüntüleri içeren bir klasör. Kod parçacıklarındaki `"Your Document Directory"` ifadesini makinenizdeki gerçek yol ile değiştirin.

## Ad alanlarını içe aktar

`System.Drawing` ad alanı, Aspose.Drawing'ın genişlettiği `Bitmap`, `Graphics` ve ilgili türlere erişim sağlar.

```csharp
using System.Drawing;
```

## Adım adım kılavuz

### Adım 1: Bir bitmap tuvali oluşturun

`Bitmap`, Aspose.Drawing'ın bir görüntünün bellek içi temsili olup, piksel‑düzeyinde erişim ve format kontrolü sağlar.  

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

Kırpılmış sonucu tutacak boş bir tuval ile başlarız. Genişlik ve yüksekliği, çıkarmayı planladığınız alanın boyutlarıyla eşleşecek şekilde ayarlayın.

### Adım 2: Bir graphics nesnesi oluşturun

`Graphics`, bir Bitmap üzerine şekil, metin veya diğer görüntüleri çizebilmenizi sağlayan çizim yüzeyidir.  

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

Bir `Graphics` nesnesi, tuval üzerine çizmeyi sağlar. `InterpolationMode`, ölçekleme veya dönüşüm sırasında piksel değerlerinin nasıl hesaplandığını kontrol eder—`NearestNeighbor` keskin kenarlar için iyi çalışır.

### Adım 3: Kırpılacak görüntüyü yükleyin

`Image` (veya `Bitmap`), kaynak dosyayı belleğe yükler ve manipülasyona hazır hâle getirir.  

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

Kaynak görüntüyü yükleyin. Yolun mevcut bir dosyaya işaret ettiğinden emin olun; aksi takdirde bir istisna fırlatılacaktır.

### Adım 4: Kaynak ve hedef dikdörtgenleri tanımlayın

`Rectangle` nesneleri, kaynak görüntünün korunacak bölgesini ve hedef tuval üzerinde nerede konumlandırılacağını tanımlar.  

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

`sourceRectangle`, API'ye orijinal görüntünün hangi kısmının korunacağını söyler. Burada sol‑üst 50 × 40 piksel alanını seçiyoruz. Aynı dikdörtgeni `destinationRectangle`'a atayarak, kırpılmış bölgeyi orijinal boyutunda tutarız.

### Adım 5: Kırpma işlemini gerçekleştirin

`Graphics.DrawImage`, `image`'in tanımlanan bölümünü boş `bitmap`'imize kopyalar.  

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

Bu, temel **crop image to PNG** işlemidir. Metot, kaynak dikdörtgeni dikkate alır ve yalnızca seçilen pikselleri hedef bitmap'e yazar.

### Adım 6: Kırpılmış görüntüyü kaydedin (crop image to PNG)

`Bitmap.Save`, bellek içi bitmap'i belirtilen formatı kullanarak bir dosyaya yazar.  

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

Son olarak, tuvali bir PNG dosyası olarak diske yazın. PNG, herhangi bir alfa kanalını korur ve kayıpsız kalite sağlar—UI varlıkları için idealdir.

## Döngü içinde toplu görüntü kırpma nasıl yapılır?

Her dosya yolunu `foreach (var file in Directory.GetFiles(sourceFolder, "*.png"))` ile yineleyin, döngü içinde Adım 1‑6'yı tekrarlayın ve her sonucu hedef bir klasöre kaydedin. Bu desen lineer olarak ölçeklenir, daha hızlı bir verim için `Parallel.ForEach` ile paralelleştirilebilir ve görüntüleri verimli ve hızlı bir şekilde işler.

## Yaygın tuzaklar ve ipuçları

- **Piksel formatı uyumsuzlukları** – renk kaymalarını önlemek için kaynak görüntü ve tuval bitmap'inin uyumlu bir piksel formatına sahip olduğundan emin olun.  
- **GDI nesnelerinin imhası** – `Bitmap` ve `Graphics`'i `using` ifadeleri içinde sarın veya manuel olarak `Dispose()` çağırın; aksi takdirde yönetilmeyen kaynaklar sızabilir.  
- **Koordinat hataları** – dikdörtgen koordinatları sıfır‑tabanlıdır. Kaynak görüntünün sınırlarını aşan bir dikdörtgen seçmek istisna oluşturur.  

## Sıkça sorulan sorular

**S: Aspose.Drawing kullanarak herhangi bir formatta görüntüyü kırpabilir miyim?**  
**C: Evet, Aspose.Drawing geniş bir format yelpazesini destekler (PNG, JPEG, BMP, GIF, TIFF vb.), bu yüzden neredeyse her türlü görüntüyü kırpabilirsiniz.**

**S: Gelişmiş kırpma seçenekleri mevcut mu?**  
**C: Kesinlikle. `GraphicsPath`, `Matrix` dönüşümlerini birleştirebilir veya dairesel kırpmalar gibi daha karmaşık seçimler için `ImageProcessor` sınıfını kullanabilirsiniz.**

**S: Tek bir görüntüye birden fazla kırpma işlemi uygulayabilir miyim?**  
**C: Evet. İlk kırpmadan sonra, ortaya çıkan bitmap'i yeni kaynak olarak yeniden kullanabilir ve işlemi tekrarlayarak birden fazla kırpma zinciri oluşturabilirsiniz.**

**S: Aspose.Drawing toplu görüntü işleme için uygun mu?**  
**C: Kesinlikle. Hafif API'si ve yerel bağımlılıkları olmaması, sunucularda büyük görüntü koleksiyonlarını işlemek için mükemmeldir.**

**S: Aspose.Drawing ile ilgili sorular için nasıl destek alabilirim?**  
**C: Yardım almak ve toplulukla iletişime geçmek için [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) adresine gidin.**

---

**Son Güncelleme:** 2026-10-13  
**Test Edilen Versiyon:** Aspose.Drawing 24.11 for .NET  
**Yazar:** Aspose

## İlgili Eğitimler

- [Aspose.Drawing ile BMP'yi PNG ve Diğer Formatlara Yükleme, Dönüştürme](/drawing/net/image-editing/load-save/)
- [Aspose.Drawing'ı .NET için Nasıl Lisanslarsınız – aspose.drawing nasıl lisanslanır](/drawing/net/licensing/)
- [Aspose.Drawing API for .NET ile Dikdörtgen Çizme – Koordinat Sistemi Dönüşümü (Sayfa Dönüşümü)](/drawing/net/coordinate-transformations/page-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}