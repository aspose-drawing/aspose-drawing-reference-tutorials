---
date: 2026-02-09
description: Aspose.Drawing lisansını .NET’te nasıl ayarlayacağınızı öğrenin. Su işareti
  olmadan tam özellikleri açmak için lisanslama yöntemlerinde uzmanlaşın.
linktitle: Licensing in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Aspose.Drawing Lisansını Ayarlama – Aspose.Drawing Lisansını Nasıl Ayarlarsınız
url: /tr/net/licensing/licensing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing Lisansını Ayarlama

## Giriş

Güçlü grafik ve görüntü işleme özelliklerine dayanan .NET uygulamaları geliştiriyorsanız, **Aspose.Drawing lisansını ayarlamak**, değerlendirme sınırlamalarını kaldırmanın ve tam özellik setine erişmenin ilk adımıdır. Bu öğreticide, Aspose.Drawing lisansını ayarlamanın üç pratik yolunu öğreneceksiniz—dosyadan yükleme, akıştan (stream) yükleme ve ölçülen kullanım (metered‑usage) modelini kullanma—böylece kütüphaneyi güvenle entegre edebilirsiniz.

## Hızlı Yanıtlar
- **Aspose.Drawing'i etkinleştirmenin temel yolu nedir?** `License.SetLicense("Aspose.Drawing.lic")` kullanarak bir lisans dosyası yükleyin.  
- **Çalışma zamanında lisans uygulayabilir miyim?** Evet, dinamik senaryolar için lisansı bir `Stream`'den yükleyebilirsiniz.  
- **Ölçülen (metered) lisans destekleniyor mu?** Kesinlikle; tüketim tabanlı faturalandırmayı etkinleştirmek için `Metered.SetMeteredKey(publicKey, privateKey)` kullanın.  
- **Geliştirme sürümleri için lisansa ihtiyacım var mı?** Test için bir deneme sürümü çalışır, ancak geçerli bir lisans filigranları kaldırır ve tüm API'leri açar.  
- **Hangi .NET sürümleri uyumludur?** Aspose.Drawing, .NET Framework 4.x, .NET Core 3.1+ ve .NET 5/6+ sürümlerini destekler.

## Önkoşullar

Başlamadan önce, şunların olduğundan emin olun:

- **Aspose.Drawing Kütüphanesi** – en son paketi [buradan](https://releases.aspose.com/drawing/net/) indirin.  
- **Lisans Dosyası** – geçerli bir `.lic` dosyasını [Aspose](https://purchase.aspose.com/buy) üzerinden edinin.  
- **.NET Geliştirme Ortamı** – Visual Studio, Rider veya .NET Framework/.NET Core hedefleyen herhangi bir IDE.

## Ad Alanlarını İçe Aktarma

Lisanslama için standart .NET ad alanlarının yanı sıra Aspose.Drawing ad alanına da ihtiyacımız var. C# dosyanızın en üstüne aşağıdaki `using` ifadelerini ekleyin:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
```

## Lisansı Dosyadan Yükleme

Lisansı bir dosyadan yüklemek en basit yaklaşımdır. Bu üç adımı izleyin:

### Adım 1: Lisans Nesnesini Başlatma

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

### Adım 2: Lisansı `.lic` Dosyasından Ayarlama

```csharp
license.SetLicense("Aspose.Drawing.lic");
```

### Adım 3: Başarıyı Doğrulama

```csharp
Console.WriteLine("License set successfully.");
```

> **Pro ipucu:** `.lic` dosyasını çalıştırılabilir dosyanızla aynı klasöre koyun veya “dosya bulunamadı” hatalarını önlemek için mutlak bir yol sağlayın.

## Lisansı Akıştan (Stream) Yükleme

Lisans dosyanız bir kaynak olarak gömülü olduğunda veya uzaktan alındığında, bir `Stream`'den yüklemek size esneklik sağlar.

### Adım 1: Lisans Nesnesini Başlatma

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

### Adım 2: Lisansı bir `FileStream` Kullanarak Yükleme

```csharp
FileStream myStream = new FileStream("Aspose.Drawing.lic", FileMode.Open);
license.SetLicense(myStream);
```

### Adım 3: Başarıyı Doğrulama

```csharp
Console.WriteLine("License set successfully.");
```

> **Uyarı:** Dosya tanıtıcılarını serbest bırakmak için `FileStream`'i (veya bir `using` bloğu) dispose etmeyi unutmayın.

## Ölçülen (Metered) Lisans Kullanımı

Ölçülen lisans, SaaS veya kullanım başına ödeme senaryoları için idealdir. Tüketimi izler ve gerçek kullanımınıza göre faturalandırır.

### Adım 1: Ölçülen Nesneyi Başlatma

```csharp
System.Drawing.AsposeDrawing.Metered metered = new System.Drawing.AsposeDrawing.Metered();
```

### Adım 2: Genel ve Özel Anahtarları Ayarlama

```csharp
metered.SetMeteredKey("your_public_key", "your_private_key");
```

### Adım 3: Görüntü İşlemenizi Gerçekleştirin

```csharp
// Your image processing logic here
```

### Adım 4: Tüketim Bilgilerini Alın

```csharp
decimal amount = System.Drawing.AsposeDrawing.Metered.GetConsumptionQuantity();
decimal credits = System.Drawing.AsposeDrawing.Metered.GetConsumptionCredit();
```

### Adım 5: Tüketim Detaylarını Görüntüleyin

```csharp
Console.WriteLine("Amount Consumed: " + amount.ToString());
Console.WriteLine("Credits Consumed: " + credits.ToString());
```

> **Yaygın tuzak:** `SetMeteredKey` çağrısını unutursanız, API deneme moduna geri döner ve çıktıda filigranlar görürsünüz.

## Aspose.Drawing Lisansını Neden Doğru Ayarlamalısınız?

- **Deneme modunda** görülen filigranları kaldırır.  
- **Gelişmiş görüntü filtreleri ve PDF dönüşümü** gibi premium API'leri açar.  
- Aspose'un ticari dağıtım lisans koşullarına **uyumu** sağlar.  
- **Ölçülen faturalandırmayı** etkinleştirir, sadece kullandığınız kadar ödersiniz.

## Yaygın Sorunlar ve Çözümleri

| Sorun | Neden | Çözüm |
|-------|-------|-----|
| “License file not found” hatası | Yanlış yol veya çıkış klasöründe eksik dosya | Mutlak bir yol kullanın veya dosyanın *Copy to Output Directory* özelliğini *Copy always* olarak ayarlayın. |
| Lisans ayarlandıktan sonra hâlâ filigran görünüyor | Lisans ilk API çağrısından önce yüklenmemiş | Lisansı **herhangi bir Aspose.Drawing işlemi** öncesinde yükleyin. |
| Ölçülen tüketim her zaman sıfır | Anahtarlar ayarlanmamış veya ortam değişkenleri yanlış | Genel/özel anahtarları doğrulayın ve Aspose’un ölçülen sunucusuna internet bağlantısının olduğundan emin olun. |

## Sıkça Sorulan Sorular

**Q1: Aspose.Drawing'i lisans olmadan kullanabilir miyim?**  
**A1:** Evet, bir deneme lisansı geliştirme ve değerlendirme için çalışır, ancak filigran ekler ve bazı özellikleri sınırlar.

**Q2: Aspose.Drawing lisansımı ne sıklıkta yenilemem gerekir?**  
**A2:** Lisanslar, satın alınan sürüm için süresizdir. Yenileme sadece destek ve yükseltmeler için gereklidir.

**Q3: Ölçülen lisanslama nedir ve ne zaman kullanmalıyım?**  
**A3:** Ölçülen lisanslama, kullanım (işlemler veya işlenen veri) bazında ücretlendirme yapar. Bulut hizmetleri veya kullanım başına ödeme modelleri için mükemmeldir.

**Q4: Aspose.Drawing'i ticari projelerde kullanabilir miyim?**  
**A4:** Kesinlikle—geçerli bir lisansınız olduğunda, Aspose.Drawing'i herhangi bir ticari uygulamaya entegre edebilirsiniz.

**Q5: Aspose.Drawing için topluluk desteğini nereden bulabilirim?**  
**A5:** Topluluk yardımı, örnekler ve tartışmalar için [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) adresini ziyaret edin.

## Sonuç

Bir **Aspose.Drawing lisansını ayarlamayı**—dosyadan, akıştan veya ölçülen kullanım aracılığıyla—öğrenmek, bu güçlü .NET grafik kütüphanesinden en iyi şekilde yararlanmanızı sağlar. Yukarıdaki adımları izleyin, yaygın tuzaklara dikkat edin ve lisans engelleri olmadan sağlam görüntü işleme çözümleri geliştirmeye hazır olun.

---

**Last Updated:** 2026-02-09  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}