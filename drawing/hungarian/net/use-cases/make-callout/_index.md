---
date: 2026-03-02
description: Fejlessze dokumentumábrázolásait az Aspose.Drawing for .NET segítségével!
  Tanulja meg lépésről lépésre, hogyan adjon hozzá feliratokat a tisztább és informatívabb
  vizuális elemekhez.
linktitle: Making Callouts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Hogyan adjunk hozzá feliratokat az Aspose.Drawing .NET-hez
url: /hu/net/use-cases/make-callout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Feliratok létrehozása az Aspose.Drawing-ban

## Bevezetés
Ha kíváncsi vagy arra, **hogyan lehet feliratokat (callout-okat) hozzáadni** a képeidhez vagy diagramjaidhoz az Aspose.Drawing for .NET használatával, jó helyen jársz. Ebben az útmutatóban végigvezetünk a teljes folyamaton – a kép betöltésétől a szépen formázott feliratok megrajzolásáig – hogy illusztrációid világosabbak és informatívabbak legyenek.

## Gyors válaszok
- **Milyen könyvtárra van szükségem?** Aspose.Drawing for .NET (letölthető a hivatalos weboldalról).  
- **Mely .NET verziók támogatottak?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Szükségem van licencre?** Egy ingyenes próba megfelelő a fejlesztéshez; a termeléshez kereskedelmi licenc szükséges.  
- **Mennyi időt vesz igénybe a megvalósítás?** Általában 10 perc alatt elkészíthető egy alap felirat.  
- **Testreszabhatom a színeket és betűtípusokat?** Igen – minden a szabványos GDI+ objektumok (Pen, Font, Brush) segítségével szabályozható.

## Hogyan adjunk feliratokat az Aspose.Drawing-hoz
Az alábbi tömör, lépésről‑lépésre útmutató pontosan megmutatja, **hogyan lehet feliratokat hozzáadni** egy képhez. Nyugodtan másold ki a kódot, kísérletezz a pozíciókkal, és igazítsd a stílust a márkádhoz.

## Előfeltételek
Mielőtt belevágnál, győződj meg róla, hogy rendelkezel:

- Alapvető C# programozási ismeretekkel.  
- Aspose.Drawing könyvtárral telepítve. Letöltheted [innen](https://releases.aspose.com/drawing/net/).  
- Egy dokumentummal vagy képpel, amelyhez feliratokat szeretnél hozzáadni.

## Névterek importálása
Győződj meg róla, hogy a szükséges névterek be vannak vonva a projektedbe:

```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```

## 1. lépés: Kép betöltése
Kezdd a kép betöltésével, amelyhez feliratokat szeretnél hozzáadni. Cseréld le a `"Your Document Directory"` és a `"gears.png"` értékeket a saját könyvtáradra és képfájlnevedre.

```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Your code here
}
```

## 2. lépés: Graphics objektum létrehozása
Hozz létre egy `Graphics` objektumot a képből a rajzolási műveletekhez.

```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```

## 3. lépés: Felirat pozíciók meghatározása
Határozd meg az egyes feliratok kezdő‑ és végpontjait, valamint a felirat értékét és egységét.

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

## 4. lépés: Feliratok rajzolása
Implementáld a `DrawCallOut` metódust a feliratok megrajzolásához a képen.

```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```

## 5. lépés: Kép mentése
Mentsd el a feliratokkal ellátott képet a kívánt könyvtárba.

```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```

## Felirat (Callout) forráskód
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

## Gyakori problémák és tippek
- **Helytelen horgonykoordináták** – győződj meg róla, hogy a kezdő‑ és végpontok a kép határain belül vannak; ellenkező esetben a felirat levágódhat.  
- **Szöveg átfedés** – állítsd be a `spaceSize` értékét vagy a betűméretet, ha a címke más grafikákkal ütközik.  
- **Teljesítmény** – nagyon nagy képek esetén fontold meg a `Pen`, `Font` és `Brush` objektumok használat után történő eldobását az erőforrások felszabadítása érdekében.

## Összegzés
Gratulálunk! Most már tudod, **hogyan lehet feliratokat hozzáadni** egy képhez az Aspose.Drawing for .NET segítségével. Nyugodtan kísérletezz különböző pozíciókkal, színekkel és betűtípusokkal, hogy a vizuális stílusodhoz illeszkedjen.

## Gyakran Ismételt Kérdések

### Használhatom az Aspose.Drawing-ot más típusú illusztrációkhoz?
Igen, az Aspose.Drawing számos rajzolási műveletet támogat különféle illusztrációkhoz.

### Kompatibilis-e az Aspose.Drawing különböző képformátumokkal?
Teljesen! Az Aspose.Drawing támogatja a népszerű képformátumokat, mint a PNG, JPEG, GIF és még sok más.

### Hol találok további példákat és dokumentációt?
Fedezd fel a részletes dokumentációt [itt](https://reference.aspose.com/drawing/net/).

### Hogyan kaphatok támogatást, ha problémáim vannak?
Látogasd meg az [Aspose.Drawing fórumot](https://forum.aspose.com/c/drawing/44) a közösségi támogatásért.

### Próbálhatom-e az Aspose.Drawing-ot vásárlás előtt?
Természetesen! Kezdd el egy ingyenes próba verzióval [itt](https://releases.aspose.com/).

**További Kérdések & Válaszok**

**Q: Változtathatom a felirat vonal stílusát (szaggatott, pontozott)?**  
A: Igen – egyszerűen állítsd be a `Pen.DashStyle` tulajdonságot a vonal rajzolása előtt.

**Q: Lehetőség van háttérszínt hozzáadni a felirat címkéhez?**  
A: Teljesen. Hozz létre egy `SolidBrush`-t a kívánt színnel, és tölts ki egy téglalapot a szöveg mögött, mielőtt meghívnád a `DrawString`-et.

**Q: Hogyan biztosíthatom, hogy a felirat ugyanúgy néz ki nagy DPI-s kijelzőkön?**  
A: Állítsd be a `graphics.PageUnit = GraphicsUnit.Pixel` értéket (ahogy a példában látható), és használj vektor‑alapú méréseket a méretezés konzisztenciájának megőrzéséhez.

---

**Utolsó frissítés:** 2026-03-02  
**Tesztelve:** Aspose.Drawing 24.11 for .NET  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}