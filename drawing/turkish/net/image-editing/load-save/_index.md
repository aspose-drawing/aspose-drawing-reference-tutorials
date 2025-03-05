---
title: Aspose.Drawing'de Görüntüleri Yükleme ve Kaydetme
linktitle: Aspose.Drawing'de Görüntüleri Yükleme ve Kaydetme
second_title: Aspose.Drawing .NET API - System.Drawing.Common'a alternatif
description: Aspose.Drawing ile .NET'te görüntü yükleme ve kaydetme konusunda uzmanlaşın. BMP, GIF, JPG, PNG, TIFF formatlarını zahmetsizce keşfedin.
type: docs
weight: 13
url: /tr/net/image-editing/load-save/
---
## giriiş

Aspose.Drawing for .NET kullanarak görüntü yükleme ve kaydetme konusunda uzmanlaşmaya yönelik adım adım kılavuzumuza hoş geldiniz! Çeşitli görüntü formatlarını zahmetsizce kullanma becerilerinizi geliştirmek istiyorsanız doğru yerdesiniz. Aspose.Drawing for .NET, görüntülerle çalışma sürecini kolaylaştıran güçlü bir kitaplıktır ve bu eğitimde görüntüleri farklı formatlarda yükleme ve kaydetme konularını ele alacağız.

## Önkoşullar

Bu öğrenme yolculuğuna çıkmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

-  Aspose.Drawing for .NET: Kütüphanenin kurulu olduğundan emin olun. İndirebilirsin[Burada](https://releases.aspose.com/drawing/net/).

- .NET Ortamı: Bu eğitimde .NET geliştirme konusunda yeterli bilgiye sahip olduğunuz varsayılmaktadır.

Artık hazır olduğumuza göre, temel ad alanlarını inceleyelim ve adım adım kılavuzu inceleyelim.

## Ad Alanlarını İçe Aktar

.NET projenizde gerekli ad alanlarını içe aktararak başlayın:

```csharp
using System.Drawing;
```

Bu ad alanları, görüntü işleme için gereken temel sınıfları ve yöntemleri sağlar.

## 1. Adım: Görüntü Yükleme

Bir resim yükleyerek başlayalım. Bu örnek, BMP, GIF, JPG, PNG ve TIFF gibi çeşitli formatlardaki görüntüleri yükler.

```csharp
public static void Run()
{
    LoadAndSave("bmp");
    LoadAndSave("gif");
    LoadAndSave("jpg");
    LoadAndSave("png");
    LoadAndSave("tiff");
}
```

## Adım 2: LoadAndSave Yöntemini Uygulama

 Şimdi, parçalayın`LoadAndSave` birden fazla adıma bölünmüş yöntem:

### Adım 2.1: Görüntüyü Yükle

```csharp
private static void LoadAndSave(string graphicsFileFormats)
{
    string inputPath = "Your Document Directory" + @"GraphicsFileFormats\image." + graphicsFileFormats;
    Bitmap loadedImage = new Bitmap(inputPath);
}
```

### Adım 2.2: Görüntüyü Kaydet

```csharp
private static void LoadAndSave(string graphicsFileFormats)
{
    string inputPath = "Your Document Directory" + @"GraphicsFileFormats\image." + graphicsFileFormats;
    string outputPath = "Your Document Directory" + @"GraphicsFileFormats\image_out." + graphicsFileFormats;
    
    Bitmap loadedImage = new Bitmap(inputPath);
    
    // Resmi kaydet
    loadedImage.Save(outputPath);
}
```

Desteklemek istediğiniz her görüntü formatı için bu adımları tekrarlayın.

## Çözüm

Tebrikler! Aspose.Drawing for .NET'i kullanarak görselleri yükleme ve kaydetme sanatında ustalaştınız. Bu beceri, çeşitli görüntü formatlarıyla çalışan geliştiriciler için çok değerlidir. Bu bilgiyi deneyin, keşfedin ve projelerinize entegre edin.

## SSS'ler

### S1: Aspose.Drawing tüm resim formatlarıyla uyumlu mu?

Cevap1: Aspose.Drawing, BMP, GIF, JPG, PNG ve TIFF dahil çok çeşitli formatları destekler.

### S2: Aspose.Drawing'in ayrıntılı belgelerini nerede bulabilirim?

Cevap2: Resmi belgelere göz atın[Burada](https://reference.aspose.com/drawing/net/).

### S3: Aspose.Drawing için nasıl geçici lisans alabilirim?

 A3: Ziyaret edin[Burada](https://purchase.aspose.com/temporary-license/) geçici lisans ayrıntıları için.

### S4: Uygulama sırasında sorunlarla karşılaşırsam veya sorularım olursa ne olur?

 Cevap4: Aspose.Drawing topluluğundan yardım isteyin:[Aspose Forumu](https://forum.aspose.com/c/diagram/17).

### S5: Aspose.Drawing kütüphanesini nereden satın alabilirim?

 A5: Satın alabilirsiniz[Burada](https://purchase.aspose.com/buy).