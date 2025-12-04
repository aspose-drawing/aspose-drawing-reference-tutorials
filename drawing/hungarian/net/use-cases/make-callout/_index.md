---
title: Feliratok készítése Aspose.Drawingben
linktitle: Feliratok készítése Aspose.Drawingben
second_title: Aspose.Drawing .NET API – a System.Drawing.Common alternatívája
description: Javítsa dokumentum-illusztrációit az Aspose.Drawing for .NET segítségével! Ismerje meg lépésről lépésre, hogyan adhat hozzá feliratokat a tisztább és informatívabb látvány érdekében.
weight: 10
url: /hu/net/use-cases/make-callout/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Feliratok készítése Aspose.Drawingben

## Bevezetés
Üdvözöljük részletes útmutatónkban az Aspose.Drawing for .NET-ben történő kiemelések készítéséhez! Ha kiemelésekkel szeretné javítani a dokumentum illusztrációit, akkor jó helyen jár. Ebben az oktatóanyagban a folyamatot az Aspose.Drawing könyvtár segítségével kezelhető lépésekre bontjuk.
## Előfeltételek
Mielőtt belevágna az oktatóanyagba, győződjön meg arról, hogy rendelkezik a következő előfeltételekkel:
- C# programozási nyelv alapismerete.
-  Aspose.Drawing könyvtár telepítve. Letöltheti[itt](https://releases.aspose.com/drawing/net/).
- Dokumentum vagy kép, amelyhez kiemeléseket szeretne hozzáadni.
## Névterek importálása
Győződjön meg arról, hogy a szükséges névterek szerepelnek a projektben:
```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```
## 1. lépés: Töltse be a képet
 Kezdje azzal, hogy betölti azt a képet, amelyhez kiemeléseket szeretne hozzáadni. Cserélje ki`"Your Document Directory"` és`"gears.png"` tényleges könyvtárával és képfájlnevével.
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Itt a kódod
}
```
## 2. lépés: Grafikai objektum létrehozása
 Hozzon létre egy`Graphics` objektumot a képből a rajzi műveletek végrehajtásához.
```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```
## 3. lépés: Határozza meg a kiemelések pozícióit
Határozza meg az egyes kiemelések kezdő- és végpontját, valamint a felirat értékét és mértékegységét.
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
## 4. lépés: Rajzolj feliratokat
 Végezze el a`DrawCallOut` módszer, amellyel feliratokat rajzolhat a képre.
```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```
## 5. lépés: Mentse el a képet
Mentse el a képet a feliratokkal a kívánt könyvtárba.
```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```
## Rajzolja meg a kiemelés forráskódját
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
## Következtetés

Gratulálunk! Sikeresen hozzáadott kiemeléseket a képéhez az Aspose.Drawing for .NET segítségével. Nyugodtan kísérletezzen különböző pozíciókkal és értékekkel, hogy tovább testreszabhassa kiemeléseit.

## GYIK

### Használhatom az Aspose.Drawing programot más típusú illusztrációkhoz?

Igen, az Aspose.Drawing a rajzolási műveletek széles skáláját támogatja különféle típusú illusztrációkhoz.

### Az Aspose.Drawing kompatibilis a különböző képformátumokkal?

Teljesen! Az Aspose.Drawing olyan népszerű képformátumokat támogat, mint a PNG, JPEG, GIF stb.

### Hol találok további példákat és dokumentációt?

 Tekintse meg az átfogó dokumentációt[itt](https://reference.aspose.com/drawing/net/).

### Hogyan kaphatok támogatást, ha problémákba ütközöm?

 Meglátogatni a[Aspose.Rajz fórum](https://forum.aspose.com/c/diagram/17) közösségi támogatásért.

### Vásárlás előtt kipróbálhatom az Aspose.Drawing programot?

 Biztosan! Kezdje el egy ingyenes próbaverzióval[itt](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
