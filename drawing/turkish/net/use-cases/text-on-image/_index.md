---
title: Aspose.Drawing'de Görsellere Metin Ekleme
linktitle: Aspose.Drawing'de Görsellere Metin Ekleme
second_title: Aspose.Drawing .NET API - System.Drawing.Common'a alternatif
description: Aspose.Drawing for .NET ile metnin görsellere kusursuz entegrasyonunu keşfedin. Zahmetsiz görüntü işleme için adım adım kılavuzumuzu izleyin. Şimdi İndirin!
type: docs
weight: 12
url: /tr/net/use-cases/text-on-image/
---
## giriiş
.NET geliştirmenin dinamik dünyasında Aspose.Drawing, görüntüleri kolaylıkla değiştirmek için güçlü bir araç olarak öne çıkıyor. İster filigran ekleme, açıklama ekleme veya kişiselleştirilmiş grafikler oluşturma olsun, görüntülere metin eklemek yaygın bir gereksinimdir. Bu eğitimde, C# kullanarak metni resimlerinize sorunsuz bir şekilde entegre etmek için Aspose.Drawing'den nasıl yararlanabileceğinizi keşfedeceğiz.
## Önkoşullar
Eğiticiye dalmadan önce aşağıdakilerin yerinde olduğundan emin olun:
1.  Aspose.Drawing Kütüphanesi: Aspose.Drawing kütüphanesini şuradan indirip yükleyin:[Aspose.Drawing for .NET belgeleri](https://reference.aspose.com/drawing/net/).
2. Geliştirme Ortamı: Visual Studio veya başka herhangi bir uyumlu IDE dahil, çalışan bir .NET geliştirme ortamına sahip olun.
Şimdi adım adım kılavuza başlayalım.
## Ad Alanlarını İçe Aktar
Gerekli ad alanlarını C# projenize aktararak başlayın:
```csharp
using System;
using System.Drawing;
using System.Drawing.Text;
using System.Linq;
```
## 1. Adım: Görüntüyü Yükleyin
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "UseCases", "girl.jpg")))
{
    var graphics = Graphics.FromImage(image);
    graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
    graphics.PageUnit = GraphicsUnit.Pixel;
```
Burada görüntüyü belirtilen dosya yolundan yüklüyoruz ve grafik nesnesini daha ileri işlemler için başlatıyoruz.
## Adım 2: Metin Özelliklerini Ayarlayın
```csharp
SolidBrush brush = new SolidBrush(Color.Navy);
Font font = new Font("Calibri", 20, FontStyle.Italic);
int padding = 5;
```
Renk, yazı tipi ve dolgu gibi metin özelliklerini tanımlayın. Bu parametreleri tercihlerinize göre ayarlayın.
## 3. Adım: Metin Boyutunu Ölçün
```csharp
string text = "Happy Birthday!";
var words = text.Split(' ');
int extentWidth = 0;
int extentHeight = 0;
words.ToList().ForEach(word =>
{
    var stringSize = graphics.MeasureString(word, font);
    extentWidth = Math.Max(extentWidth, (int)stringSize.Width + padding);
    extentHeight += (int)stringSize.Height;
});
```
Her kelimeyi ayrı ayrı ölçerek metin için gereken boyutu hesaplayın. Bu, doğru yerleştirmeyi sağlar ve metin çakışmasını önler.
## Adım 4: Görüntünün Üzerine Metin Çizin
```csharp
Rectangle rectangle = new Rectangle(image.Width - padding - extentWidth, image.Height - padding - extentHeight, extentWidth, extentHeight);
graphics.DrawString(text, font, brush, rectangle);
```
Şimdi metni hesaplanan boyuta göre görselin üzerine konumlandırın ve belirtilen yazı tipi ve rengi kullanarak çizin.
## Adım 5: Görüntüyü Kaydedin
```csharp
image.Save(Path.Combine("Your Document Directory", "UseCases", "girl_card_out.jpg"));
}
```
Değiştirilen görüntüyü istediğiniz dizine kaydedin.
Bu adım adım kılavuz, Aspose.Drawing for .NET kullanarak görüntülere metin eklemenin basit sürecini göstermektedir. İstenilen görsel efekti elde etmek için farklı yazı tipleri, renkler ve metin içeriğiyle denemeler yapın.
## Çözüm
Aspose.Drawing, .NET'teki görüntü işleme görevlerini basitleştirerek geliştiricilere güçlü bir araç seti sağlar. Resimlere metin eklemek, kitaplığın grafik öğeleri işlemedeki çok yönlülüğünü gösteren yeteneklerinin yalnızca bir örneğidir.
## Sıkça Sorulan Sorular
### Aspose.Drawing tüm resim formatlarıyla uyumlu mu?
 Aspose.Drawing, JPEG, PNG ve GIF gibi popüler olanlar da dahil olmak üzere çok çeşitli görüntü formatlarını destekler. Bakın[dokümantasyon](https://reference.aspose.com/drawing/net/) tam bir liste için.
### Aspose.Drawing'i ticari projeler için kullanabilir miyim?
Evet, Aspose.Drawing hem kişisel hem de ticari projeler için uygundur. Lisans ayrıntıları için şu adresi ziyaret edin:[satın alma sayfası](https://purchase.aspose.com/buy).
### Test amaçlı geçici lisanslar mevcut mu?
 Evet, adresini ziyaret ederek test için geçici bir lisans alabilirsiniz.[Geçici Lisans](https://purchase.aspose.com/temporary-license/).
### Aspose.Drawing için topluluk desteğini nerede bulabilirim?
 Toplulukla etkileşime geçin ve bu konuda destek alın[Aspose.Çizim forumu](https://forum.aspose.com/c/diagram/17).
### Aspose.Drawing'e nasıl başlayabilirim?
 Kütüphaneyi şuradan indirerek başlayın:[Burada](https://releases.aspose.com/drawing/net/) ve kapsamlı olanı keşfedin[dokümantasyon](https://reference.aspose.com/drawing/net/).