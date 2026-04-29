---
date: 2026-02-07
description: Aspose.Drawing kullanarak görüntüyü PNG formatına kırpmak için adım adım
  öğretici, .NET geliştiricileri için System.Drawing'in alternatifi. Toplu kırpma
  ve temel teknikleri içerir.
linktitle: Image Cropping Tutorial – Aspose.Drawing
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
title: Aspose.Drawing for .NET ile Görüntüyü PNG Olarak Kırpma
url: /tr/net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing for .NET ile PNG'ye Görüntü Kırpma Nasıl Yapılır

Eğer .NET ortamında **görüntüyü PNG'ye kırpmak** istiyorsanız ve hızlı, güvenilir bir çözüm arıyorsanız doğru yerdesiniz. Bu öğreticide bir görüntüyü nasıl yükleyeceğinizi, kırpma alanını nasıl tanımlayacağınızı ve sonucu PNG dosyası olarak nasıl kaydedeceğinizi adım adım göstereceğiz—hepsi Aspose.Drawing kullanarak, **System.Drawing**'e modern bir **alternatif** ve çapraz platform desteği sunan bir kütüphane.

## Hızlı Yanıtlar
- **Hangi kütüphaneyi kullanmalıyım?** Aspose.Drawing for .NET (System.Drawing.Common'a tam özellikli bir alternatif)  
- **Temel kırpma işlemi ne kadar sürer?** Modern bir CPU'da tek bir görüntü için genellikle bir saniyenin altında  
- **PNG'ye kırpabilir miyim?** Evet – kırpılmış bitmap'i PNG dosyası olarak kaydedin (bkz. Adım 6)  
- **Lisans gerekiyor mu?** Geliştirme için ücretsiz deneme sürümü yeterli; üretim için ticari lisans gereklidir  
- **Toplu işleme mümkün mü?** Kesinlikle – aynı adımları bir döngü içinde tekrarlayarak birden çok dosyayı işleyebilirsiniz  

## “crop image to PNG” nedir?

Görüntüyü kırpmak, orijinal bitmap'ten dikdörtgen bir bölgeyi çıkarmak anlamına gelir. Bu bölgeyi PNG olarak kaydettiğinizde şeffaflığı korur ve kayıpsız sıkıştırma elde edersiniz—küçük resimler, simgeler veya herhangi bir UI varlığı için mükemmeldir.

## Aspose.Drawing, System.Drawing'e alternatif olarak neden tercih edilmeli?

- **Çapraz platform desteği** – Windows, Linux ve macOS'ta yerel GDI+ bağımlılıkları olmadan çalışır.  
- **Zengin piksel formatı işleme** – 32‑bit, 24‑bit, indeksli ve daha fazlası.  
- **Performansa odaklı API** – tek görüntü düzenlemelerinden büyük ölçekli toplu işlere kadar ideal.  

## Önkoşullar

İlerlemeye başlamadan önce şunların kurulu olduğundan emin olun:

- **Aspose.Drawing kütüphanesi** .NET projenize entegre edilmiş. İndirmek için [buraya](https://releases.aspose.com/drawing/net/) tıklayın.  
- Kırpmak istediğiniz kaynak görüntüleri içeren bir klasör. Kod örneklerindeki `"Your Document Directory"` ifadesini makinenizdeki gerçek yol ile değiştirin.

## Ad Alanlarını İçe Aktarın

```csharp
using System.Drawing;
```

`System.Drawing` ad alanı, Aspose.Drawing'in genişlettiği `Bitmap`, `Graphics` ve ilgili tipleri kullanmamızı sağlar.

## Adım Adım Kılavuz

### Adım 1: Bir Bitmap Tuvali Oluşturun

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

Boş bir tuval oluşturuyoruz; bu tuval kırpılmış sonucun saklanacağı boyutlarda olmalı. Genişlik ve yüksekliği, çıkarmak istediğiniz alanın boyutlarına göre ayarlayın.

### Adım 2: Bir Graphics Nesnesi Oluşturun

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

`Graphics` nesnesi, tuval üzerine çizim yapmamızı sağlar. `InterpolationMode`, ölçekleme veya dönüşüm sırasında piksel değerlerinin nasıl hesaplanacağını kontrol eder—`NearestNeighbor` keskin kenarlar için iyi çalışır.

### Adım 3: Kırpılacak Görüntüyü Yükleyin

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

Kaynak görüntüyü yükleyin. Yolun mevcut bir dosyaya işaret ettiğinden emin olun; aksi takdirde bir istisna fırlatılır.

### Adım 4: Kaynak ve Hedef Dikdörtgenleri Tanımlayın

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

`sourceRectangle`, API'nin orijinal görüntünün hangi kısmını tutacağını belirtir. Burada sol‑üst 50 × 40 piksel alanını seçiyoruz. Aynı dikdörtgeni `destinationRectangle`'a atayarak kırpılmış bölgeyi orijinal boyutunda tutarız.

### Adım 5: Kırpma İşlemini Gerçekleştirin

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

`Graphics.DrawImage`, tanımlanan `image` bölümünü boş `bitmap` üzerine kopyalar. Bu, **crop image to PNG** işleminin çekirdeğidir.

### Adım 6: Kırpılmış Görüntüyü Kaydedin (Crop Image to PNG)

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

Son olarak, tuvali PNG dosyası olarak diske yazın. PNG, alfa kanalını korur ve kayıpsız kalite sunar—UI varlıkları için idealdir.

## Toplu Senaryoda Görüntüleri Nasıl Kırparız

Yüzlerce resimle çalışıyorsanız, tüm kod parçacığını bir `foreach` döngüsü içine alıp dosya yolu koleksiyonunu yineleyebilirsiniz. Aynı `Graphics.DrawImage` mantığı, **toplu görüntü kırpma** işlemini bu öğreticinin doğal bir uzantısı haline getirir.

## Yaygın Tuzaklar ve İpuçları

- **Piksel formatı uyumsuzlukları** – Renk kaymalarını önlemek için kaynak görüntü ve tuval bitmap'inin uyumlu bir piksel formatına sahip olduğundan emin olun.  
- **GDI nesnelerinin serbest bırakılması** – `Bitmap` ve `Graphics` nesnelerini `using` blokları içinde tutun veya manuel olarak `Dispose()` çağırın; aksi takdirde yönetilmeyen kaynaklar sızabilir.  
- **Koordinat hataları** – Dikdörtgen koordinatları sıfır‑tabanlıdır. Kaynak görüntünün sınırlarını aşan bir dikdörtgen seçmek istisna oluşturur.  

## Sıkça Sorulan Sorular

**S: Aspose.Drawing kullanarak herhangi bir formatta görüntü kırpabilir miyim?**  
C: Evet, Aspose.Drawing geniş bir format yelpazesini (PNG, JPEG, BMP, GIF, TIFF vb.) destekler; bu sayede neredeyse her görüntü tipini kırpabilirsiniz.

**S: Daha gelişmiş kırpma seçenekleri var mı?**  
C: Kesinlikle. `GraphicsPath`, `Matrix` dönüşümleriyle birleştirebilir veya daha karmaşık seçimler (örneğin dairesel kırpmalar) için `ImageProcessor` sınıfını kullanabilirsiniz.

**S: Tek bir görüntüye birden fazla kırpma işlemi uygulayabilir miyim?**  
C: Evet. İlk kırpmadan sonra elde edilen bitmap'i yeni kaynak olarak yeniden kullanıp işlemi tekrarlayarak birden çok kırpma zinciri oluşturabilirsiniz.

**S: Aspose.Drawing toplu görüntü işleme için uygun mu?**  
C: Evet. Hafif API'si ve yerel bağımlılıkların olmaması, sunucularda büyük görüntü koleksiyonlarını işlemek için mükemmeldir.

**S: Aspose.Drawing ile ilgili sorularım için nasıl destek alabilirim?**  
C: Yardım ve topluluk desteği için [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) adresine göz atabilirsiniz.

---

**Son Güncelleme:** 2026-02-07  
**Test Edilen Versiyon:** Aspose.Drawing 24.11 for .NET  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}