---
date: 2026-03-02
description: Aspose.Drawing for .NET kullanarak belge illüstrasyonlarınızı geliştirin!
  Daha net ve bilgilendirici görseller için açıklama balonları eklemeyi adım adım
  öğrenin.
linktitle: Making Callouts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Aspose.Drawing for .NET ile Açıklama Balonları Nasıl Eklenir
url: /tr/net/use-cases/make-callout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing'de Açıklama Kutuları Oluşturma

## Giriiş
Aspose.Drawing for .NET kullanarak detaylarınıza veya diyagramlarınıza **açıklama eklemenin** nasıl yapılacağını merak ederek, doğru yerdesiniz. Bu öğreticide, bir resmi kurulumdan şık callout'lar çizmeye kadar tüm süreci adım adım anlatacağız; Böylece çizimlerinizi daha net ve bilgilendirici hâle getirebileceksiniz.

## Hızlı Yanıtlar
- **Hangi kütüphaneye ihtiyacım var?** Aspose.Drawing for .NET (resmi siteden indirilebilir).
- **Hangi .NET sürümleri destekleniyor?** .NET Framework4.5+, .NETCore3.1+, .NET5/6+.
- **Lisansa ihtiyacım var mı?** Ücretsiz deneme sürümü geliştirme amaçlı çalışır; Üretim için ticari lisans gereklidir.
- **Uygulama ne kadar sürer?** Temel bir açıklama için genellikle 10 dakikadan kısa sürer.
- **Renkleri ve yazı tiplerini özelleştirebilir miyim?** Evet—her şey standart GDI+ nesneleri (Kalem, Yazı Tipi, Fırça) tarafından yönlendirilir.

## Aspose.Drawing'de Callout'lar Nasıl Eklenir
Aşağıda, bir görüntüye **açıklama eklemenin** tam olarak nasıl yapılacağını gösteren kısa ve adım adım bir rehber bulacaksınız. Kodu kopyalayıp, konumlarla deney yapın ve stilinizi markanıza uygun şekilde uyarlayın.

## Önkoşullar
Dalışa başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

- Temel C# programlama dili bilgisi.
- Aspose.Drawing kütüphanesi kuruldu. Onu [buradan](https://releases.aspose.com/drawing/net/) indirebilirsiniz.
- Açıklama eklemek istediğiniz bir belge veya resim.

## Ad Alanlarını İçe Aktar
Projenizde gerekli ad alanlarının bulunduğundan emin olun:

```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```

## Adım 1: Resmi Yükleyin
Açıklama balonlarını eklemek istediğiniz resmi yükleyerek başlayın. `"Belge Dizininiz"` ve `"gears.png"` ifadelerini gerçek dizin ve resim dosya adınızla değiştirin.

```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Your code here
}
```

## Adım 2: Grafik Nesnesi Oluşturun
Çizim işlemlerini gerçekleştirmek için resimden bir `Graphics` nesnesi oluşturun.

```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```

## Adım 3: Açıklama Balonu Konumlarını Tanımlayın
Her açıklama balonu için başlangıç ​​ve bitiş noktalarını, açıklama balonu değeri ve birimiyle birlikte tanımlayın.

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

## Adım 4: Açıklama Balonlarını Çizin
Resim üzerine açıklama balonları çizmek için `DrawCallOut` yöntemini uygulayın.

```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```

## Adım 5: Resmi Kaydedin
Açıklama balonları içeren resmi istediğiniz dizine kaydedin.

```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```

## Açıklama Balonu Çizim Kaynak Kodu
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

## Sık Karşılaşılan Sorunlar ve İpuçları
- **Yanlış bağlantı koordinatları** – başlangıç ​​ve bitiş noktalarının resim sınırları içinde olduğundan emin olun; aksi takdirde açıklama metni kırpılabilir.

- **Metin çakışması** – etiket diğer grafiklerle çakışıyorsa `spaceSize` veya yazı tipi boyutunu ayarlayın.

- **Performans** – çok büyük resimler için, kaynakları serbest bırakmak amacıyla kullanımdan sonra `Pen`, `Font` ve `Brush` nesnelerini atmayı düşünün.

## Sonuç
Tebrikler! Artık .NET için Aspose.Drawing kullanarak bir resme **açıklama metni eklemeyi** biliyorsunuz. Görsel stilinize uyması için farklı konumlar, renkler ve yazı tipleriyle denemeler yapmaktan çekinmeyin.

## SSS

### Aspose.Drawing'i diğer illüstrasyon türleri için kullanabilir miyim?

Evet, Aspose.Drawing çeşitli illüstrasyon türleri için geniş bir yelpazede çizim işlemlerini destekler.

### Aspose.Drawing farklı resim formatlarıyla uyumlu mu?

Kesinlikle! Aspose.Drawing, PNG, JPEG, GIF ve daha fazlası gibi popüler resim formatlarını destekler.

### Daha fazla örnek ve dokümantasyona nereden ulaşabilirim?
Kapsamlı dokümantasyona [buradan](https://reference.aspose.com/drawing/net/) ulaşabilirsiniz.

### Sorun yaşarsam nasıl destek alabilirim?
Topluluk desteği için [Aspose.Drawing forumunu](https://forum.aspose.com/c/drawing/44) ziyaret edin.

### Satın almadan önce Aspose.Drawing'i deneyebilir miyim?

Elbette! Ücretsiz deneme sürümüne [buradan](https://releases.aspose.com/) başlayabilirsiniz.

**Ek Soru-Cevap**

**S: Açıklama çizgisi stilini (kesikli, noktalı) değiştirebilir miyim?**
C: Evet—çizgiyi çizmeden önce `Pen.DashStyle` özelliğini yapılandırmanız yeterlidir.

**S: Açıklama etiketine arka plan rengi eklemek mümkün mü?**
C: Kesinlikle. İstediğiniz renkle bir `SolidBrush` oluşturun ve `DrawString`'i çağırmadan önce metnin arkasındaki bir dikdörtgeni doldurun.

**S: Açıklama etiketinin yüksek DPI ekranlarda aynı görünmesini nasıl sağlarım?**
C: `graphics.PageUnit = GraphicsUnit.Pixel` (gösterildiği gibi) olarak ayarlayın ve ölçeklendirmenin tutarlı kalması için vektör tabanlı ölçümler kullanın.

---

**Son Güncelleme:** 2026-03-02
**Test Edilen Sürüm:** Aspose.Drawing 24.11 for .NET
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}