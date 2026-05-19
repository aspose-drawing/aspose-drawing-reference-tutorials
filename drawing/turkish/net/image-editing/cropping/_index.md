---
date: 2026-05-19
description: Aspose.Drawing kullanarak, .NET geliştiricileri için System.Drawing'in
  alternatifi, görüntüleri PNG'ye toplu olarak kesmek için adım adım öğretici.
keywords:
- how to batch crop
- crop image to png
- alternative to system drawing
- batch image cropping .net
linktitle: Görüntü Kesme Öğreticisi – Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Step‑by‑step tutorial on how to batch crop images to PNG using Aspose.Drawing,
    the alternative to System.Drawing for .NET developers.
  headline: How to Batch Crop Images to PNG Using Aspose.Drawing for .NET
  type: TechArticle
- description: Step‑by‑step tutorial on how to batch crop images to PNG using Aspose.Drawing,
    the alternative to System.Drawing for .NET developers.
  name: How to Batch Crop Images to PNG Using Aspose.Drawing for .NET
  steps:
  - name: Create a Bitmap Canvas
    text: '`Bitmap` is Aspose.Drawing''s in‑memory representation of an image, providing
      pixel‑level access and format control. We start with a blank canvas sized to
      hold the cropped result. Adjust the width and height to match the dimensions
      of the area you plan to extract.'
  - name: Create a Graphics Object
    text: '`Graphics` is the drawing surface that lets you render shapes, text, or
      other images onto a Bitmap. A `Graphics` object lets us draw onto the canvas.
      The `InterpolationMode` controls how pixel values are calculated during scaling
      or transformation—`NearestNeighbor` works well for sharp edges.'
  - name: Load the Image to Crop
    text: '`Image` (or `Bitmap`) loads the source file into memory, ready for manipulation.
      Load the source image. Make sure the path points to an existing file; otherwise
      an exception will be thrown.'
  - name: Define Source and Destination Rectangles
    text: '`Rectangle` objects describe the region of the source image to keep and
      where it should be placed on the destination canvas. The `sourceRectangle` tells
      the API which part of the original image to keep. Here we pick the top‑left
      50 × 40 pixel area. By assigning the same rectangle to `destinationRect'
  - name: Perform the Crop Operation
    text: '`Graphics.DrawImage` copies the defined portion of `image` onto our blank
      `bitmap`. `Graphics.DrawImage` copies the defined portion of `image` onto our
      blank `bitmap`. This is the core **crop image to PNG** operation.'
  - name: Save the Cropped Image (Crop Image to PNG)
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
title: Aspose.Drawing for .NET ile Görüntüleri PNG'ye Toplu Kesme
url: /tr/net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing for .NET kullanarak PNG'ye Toplu Kırpma İşlemi Nasıl Yapılır

Eğer .NET ortamında **görüntüyü PNG'ye kırpma** işlemini hızlı, güvenilir ve ölçeklenebilir bir şekilde yapmak istiyorsanız doğru yerdesiniz. Bu öğreticide bir görüntüyü nasıl yükleyeceğinizi, kırpma alanını nasıl tanımlayacağınızı ve sonucu PNG dosyası olarak nasıl kaydedeceğinizi adım adım göstereceğiz—hepsi Aspose.Drawing kullanarak, **System.Drawing**'e modern bir **alternatif** olan ve çapraz platform çalışan bir kütüphane. Ayrıca tek görüntü akışını tam bir **toplu kırpma** hattına nasıl genişletebileceğinizi de göreceksiniz.

## Hızlı Yanıtlar
- **Hangi kütüphaneyi kullanmalıyım?** Aspose.Drawing for .NET (System.Drawing.Common'a tam özellikli bir alternatif)  
- **Temel kırpma ne kadar sürer?** Modern bir CPU'da tek bir görüntü için genellikle bir saniyenin altında  
- **PNG'ye kırpabilir miyim?** Evet – kırpılan bitmap'i PNG dosyası olarak kaydedin (Bkz. Adım 6)  
- **Lisans gerekli mi?** Geliştirme için ücretsiz deneme sürümü çalışır; üretim için ticari lisans gerekir  
- **Toplu işleme mümkün mü?** Kesinlikle – aynı adımları bir döngü içinde tekrarlayarak birden çok dosyayı işleyebilirsiniz  

## Görüntüleri PNG'ye Toplu Kırpmak Nasıl Yapılır?

Her kaynak dosyayı `new Bitmap(path)` ile yükleyin, kırpma alanı için eşleşen boş bir `Bitmap` oluşturun, seçilen dikdörtgeni `Graphics.DrawImage` ile çizin ve sonunda `Save("output.png", ImageFormat.Png)` çağrısını yapın. Bu altı satırı bir `foreach` döngüsü içinde, bir klasördeki tüm dosyalar üzerinde çalıştırdığınızda, saniyeler içinde onlarca görüntüyü işleyen tam bir toplu‑kırpma çözümünüz olur.

## Aspose.Drawing'i Toplu Kırpmada Neden Kullanmalıyım?

Aspose.Drawing **3 büyük işletim sistemi** (Windows, Linux, macOS) destekler ve tipik bir sunucu‑sınıfı CPU'da **500‑pixel üzerindeki görüntüleri 0.5 saniyenin altında** işleyebilir. API'si yerel GDI+ bağımlılıklarını ortadan kaldırır, bu sayede aynı kodu konteynerlere, Azure App Service'e veya AWS Lambda'ya ek kütüphane gerektirmeden dağıtabilirsiniz. Kütüphane ayrıca **50+ görüntü formatı** ve **tam alfa‑kanalı koruması** sunar; bu da şeffaf PNG kırpma işlemlerini ölçekli bir şekilde yapmayı ideal kılar.

## “crop image to PNG” Nedir?

`crop image to PNG` işlemi, kaynak bitmap'ten dikdörtgen bir bölgeyi ayırır ve bu bölgeyi bir PNG dosyasına yazar. PNG, alfa kanalını korur ve kayıpsız sıkıştırma sağlar; bu da ortaya çıkan görüntünün küçük resimler, simgeler, UI varlıkları veya kalite ve şeffaflığın gerektiği her durum için ideal olmasını sağlar.

## Aspose.Drawing, System.Drawing'e Alternatif Neden?

Aspose.Drawing, System.Drawing'in yerini alacak şekilde tam çapraz‑platform uyumluluğu sunar ve yerel GDI+ kütüphanelerine ihtiyaç duymaz. Geniş bir piksel formatı yelpazesi destekler, yüksek performanslı görüntü işleme sağlar ve alfa‑kanalı yönetimi ile kapsamlı format desteği gibi gelişmiş özellikler içerir; bu da hem basit düzenlemeler hem de büyük ölçekli toplu işleme için uygundur.

## Önkoşullar

Başlamadan önce şunların kurulu olduğundan emin olun:

- **Aspose.Drawing kütüphanesi** .NET projenize entegre edilmiş. İndirmek için [buraya](https://releases.aspose.com/drawing/net/) tıklayın.  
- Kırpmak istediğiniz kaynak görüntüleri içeren bir klasör. Kod örneklerindeki `"Your Document Directory"` ifadesini makinenizdeki gerçek yol ile değiştirin.

## Ad Alanlarını İçe Aktarın

`System.Drawing` ad alanı, Aspose.Drawing'in genişlettiği `Bitmap`, `Graphics` ve ilgili tipleri bize sunar.

```csharp
using System.Drawing;
```

## Adım‑Adım Kılavuz

### Adım 1: Bir Bitmap Tuvali Oluşturun

`Bitmap`, Aspose.Drawing'in bellek içi görüntü temsili olup piksel‑düzeyinde erişim ve format kontrolü sağlar.  

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

Kırpılmış sonucun yer alacağı boş bir tuvalle başlarız. Genişlik ve yüksekliği, çıkarmak istediğiniz alanın boyutlarına göre ayarlayın.

### Adım 2: Bir Graphics Nesnesi Oluşturun

`Graphics`, bir Bitmap üzerine şekil, metin veya diğer görüntüleri çizmeyi sağlayan çizim yüzeyidir.  

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

`Graphics` nesnesi, tuval üzerine çizim yapmamıza izin verir. `InterpolationMode`, ölçekleme veya dönüşüm sırasında piksel değerlerinin nasıl hesaplanacağını kontrol eder—`NearestNeighbor` keskin kenarlar için iyi çalışır.

### Adım 3: Kırpılacak Görüntüyü Yükleyin

`Image` (veya `Bitmap`) kaynak dosyayı belleğe yükler, manipülasyona hazır hâle getirir.  

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

Kaynak görüntüyü yükleyin. Yolun mevcut bir dosyaya işaret ettiğinden emin olun; aksi takdirde bir istisna fırlatılır.

### Adım 4: Kaynak ve Hedef Dikdörtgenlerini Tanımlayın

`Rectangle` nesneleri, kaynak görüntünün hangi bölgesinin tutulacağını ve hedef tuvalde nerede konumlandırılacağını tanımlar.  

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

`sourceRectangle`, API'ye orijinal görüntünün hangi kısmının tutulacağını söyler. Burada üst‑sol 50 × 40 piksel alanını seçiyoruz. Aynı dikdörtgeni `destinationRectangle` olarak atadığımızda, kırpılan bölge orijinal boyutunda kalır.

### Adım 5: Kırpma İşlemini Gerçekleştirin

`Graphics.DrawImage`, tanımlanan bölümü `image`'dan boş `bitmap`'e kopyalar.  

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

`Graphics.DrawImage`, tanımlanan bölümü `image`'dan boş `bitmap`'e kopyalar. Bu, **crop image to PNG** işleminin çekirdek adımıdır.

### Adım 6: Kırpılmış Görüntüyü Kaydedin (Crop Image to PNG)

`Bitmap.Save`, bellek içi bitmap'i belirtilen formatta bir dosyaya yazar.  

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

Son olarak tuvali bir PNG dosyası olarak diske yazın. PNG, alfa kanalını korur ve kayıpsız kalite sunar—UI varlıkları için idealdir.

## Görüntüleri Döngüde Toplu Kırpmak Nasıl Yapılır?

`foreach (var file in Directory.GetFiles(sourceFolder, "*.png"))` ile her dosya yolunu yineleyin, adım 1‑6'yı döngü içinde tekrarlayın ve her sonucu hedef klasöre kaydedin. Bu desen lineer olarak ölçeklenir, `Parallel.ForEach` ile paralelleştirilebilir ve görüntüleri verimli ve hızlı bir şekilde işler.

## Yaygın Tuzaklar ve İpuçları

- **Piksel formatı uyumsuzlukları** – renk kaymalarını önlemek için kaynak görüntü ve tuval bitmap'inin uyumlu bir piksel formatına sahip olduğundan emin olun.  
- **GDI nesnelerinin serbest bırakılması** – `Bitmap` ve `Graphics` nesnelerini `using` ifadeleriyle sarmalayın veya manuel olarak `Dispose()` çağırın; aksi takdirde yönetilmeyen kaynaklar sızabilir.  
- **Koordinat hataları** – dikdörtgen koordinatları sıfır‑tabanlıdır. Kaynak görüntünün sınırlarını aşan bir dikdörtgen seçmek istisna oluşturur.  

## Sık Sorulan Sorular

**S: Aspose.Drawing kullanarak herhangi bir formatta görüntü kırpabilir miyim?**  
C: Evet, Aspose.Drawing geniş bir format yelpazesi (PNG, JPEG, BMP, GIF, TIFF vb.) destekler; bu sayede neredeyse her görüntü tipini kırpabilirsiniz.

**S: Gelişmiş kırpma seçenekleri var mı?**  
C: Kesinlikle. `GraphicsPath`, `Matrix` dönüşümleriyle birleştirebilir veya daha karmaşık seçimler (örneğin dairesel kırpma) için `ImageProcessor` sınıfını kullanabilirsiniz.

**S: Tek bir görüntüye birden fazla kırpma işlemi uygulayabilir miyim?**  
C: Evet. İlk kırpmadan sonra elde edilen bitmap'i yeni kaynak olarak yeniden kullanabilir ve işlemi tekrarlayarak birden fazla kırpma zinciri oluşturabilirsiniz.

**S: Aspose.Drawing toplu görüntü işleme için uygun mu?**  
C: Evet. Hafif API'si ve yerel bağımlılıkları olmaması, sunucularda büyük görüntü koleksiyonlarını işlemek için mükemmeldir.

**S: Aspose.Drawing ile ilgili sorular için destek nasıl alınır?**  
C: Yardım ve topluluk desteği için [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) adresine göz atabilirsiniz.

---

**Son Güncelleme:** 2026-05-19  
**Test Edilen Versiyon:** Aspose.Drawing 24.11 for .NET  
**Yazar:** Aspose

## İlgili Öğreticiler

- [Aspose.Drawing for .NET ile PNG'ye Görüntü Kırpma](/drawing/net/image-editing/cropping/)
- [Aspose.Drawing for .NET ile Görüntü Ölçekleme](/drawing/net/image-editing/scale/)
- [Aspose.Drawing ile BMP'yi PNG ve Diğer Formatlara Dönüştürme](/drawing/net/image-editing/load-save/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}