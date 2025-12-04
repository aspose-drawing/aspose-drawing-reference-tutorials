---
title: Aspose.Drawing'de Açıklamalar Yapma
linktitle: Aspose.Drawing'de Açıklamalar Yapma
second_title: Aspose.Drawing .NET API - System.Drawing.Common'a alternatif
description: Aspose.Drawing for .NET'i kullanarak belge çizimlerinizi geliştirin! Daha net ve bilgilendirici görseller için belirtme çizgilerinin nasıl ekleneceğini adım adım öğrenin.
weight: 10
url: /tr/net/use-cases/make-callout/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing'de Açıklamalar Yapma

## giriiş
Aspose.Drawing for .NET'te belirtme çizgileri oluşturmaya ilişkin adım adım kılavuzumuza hoş geldiniz! Belge çizimlerinizi belirtme çizgileriyle geliştirmek istiyorsanız doğru yerdesiniz. Bu eğitimde Aspose.Drawing kütüphanesini kullanarak süreci yönetilebilir adımlara ayıracağız.
## Önkoşullar
Eğiticiye dalmadan önce aşağıdaki önkoşullara sahip olduğunuzdan emin olun:
- Temel C# programlama dili bilgisi.
-  Aspose.Drawing kütüphanesi kuruldu. İndirebilirsin[Burada](https://releases.aspose.com/drawing/net/).
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
## 1. Adım: Görüntüyü Yükleyin
 Açıklama eklemek istediğiniz görseli yükleyerek başlayın. Yer değiştirmek`"Your Document Directory"` Ve`"gears.png"` gerçek dizininiz ve resim dosya adınızla birlikte.
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Kodunuz burada
}
```
## Adım 2: Grafik Nesnesi Oluşturun
 Oluşturmak`Graphics` Çizim işlemlerini gerçekleştirmek için görüntüdeki nesneyi seçin.
```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```
## 3. Adım: Belirtme Bilgisi Konumlarını Tanımlayın
Bilgi değeri ve birimiyle birlikte her bilgi için başlangıç ve bitiş noktalarını tanımlayın.
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
## Adım 4: Açıklamaları Çizin
 Uygulamak`DrawCallOut` Görüntünün üzerine belirtme çizgileri çizme yöntemi.
```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```
## Adım 5: Görüntüyü Kaydedin
Görüntüyü belirtme çizgileriyle birlikte istediğiniz dizine kaydedin.
```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```
## Ek Bilgi Kaynak Kodunu Çiz
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
## Çözüm

Tebrikler! Aspose.Drawing for .NET'i kullanarak görüntünüze başarıyla belirtme çizgileri eklediniz. Açıklamalarınızı daha da özelleştirmek için farklı konumlar ve değerlerle denemeler yapmaktan çekinmeyin.

## SSS

### Aspose.Drawing'i diğer illüstrasyon türleri için kullanabilir miyim?

Evet, Aspose.Drawing, çeşitli illüstrasyon türleri için çok çeşitli çizim işlemlerini destekler.

### Aspose.Drawing farklı resim formatlarıyla uyumlu mu?

Kesinlikle! Aspose.Drawing PNG, JPEG, GIF ve daha fazlası gibi popüler görüntü formatlarını destekler.

### Daha fazla örnek ve belgeyi nerede bulabilirim?

 Kapsamlı belgeleri keşfedin[Burada](https://reference.aspose.com/drawing/net/).

### Sorunla karşılaşırsam nasıl destek alabilirim?

 Ziyaret edin[Aspose.Çizim forumu](https://forum.aspose.com/c/drawing/44) topluluk desteği için.

### Satın almadan önce Aspose.Drawing'i deneyebilir miyim?

 Kesinlikle! Ücretsiz denemeyle başlayın[Burada](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
