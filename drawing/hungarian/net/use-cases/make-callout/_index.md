---
date: 2026-08-01
description: Ismerje meg, hogyan adhat feliratokat képekhez az Aspose.Drawing for
  .NET használatával – lépésről‑lépésre útmutató kódrészletekkel, tippekkel és GYIK‑kel.
keywords:
- how to add callouts
- Aspose.Drawing callout tutorial
- .NET image annotation
lastmod: 2026-08-01
linktitle: Feliratok készítése az Aspose.Drawing‑ben
og_description: Fedezze fel, hogyan adhat feliratokat az Aspose.Drawing for .NET‑ben.
  Ez az oktatóanyag bemutatja az előfeltételeket, a lépésről‑lépésre megvalósítást,
  tippeket és fejlesztőknek szóló GYIK‑ot.
og_image_alt: Screenshot showing callout annotation on an image using Aspose.Drawing
og_title: Hogyan adjunk feliratokat az Aspose.Drawing for .NET használatával – Gyors
  útmutató
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to add callouts to images using Aspose.Drawing for .NET –
    step‑by‑step guide with code placeholders, tips, and FAQs.
  headline: How to Add Callouts with Aspose.Drawing for .NET
  type: TechArticle
- questions:
  - answer: Yes, Aspose.Drawing supports a wide range of drawing operations for diagrams,
      charts, and custom graphics beyond simple callouts.
    question: Can I use Aspose.Drawing for other types of illustrations?
  - answer: Absolutely! Aspose.Drawing handles PNG, JPEG, GIF, BMP, TIFF, and many
      more formats.
    question: Is Aspose.Drawing compatible with different image formats?
  - answer: Explore the comprehensive documentation [here](https://reference.aspose.com/drawing/net/).
    question: Where can I find more examples and documentation?
  - answer: Visit the [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44)
      for community assistance and official support.
    question: How do I get support if I encounter issues?
  - answer: Certainly! Get started with a free trial [here](https://releases.aspose.com/).
    question: Can I try Aspose.Drawing before purchasing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- callout
- Aspose.Drawing
- .NET graphics
- image annotation
title: Hogyan adjunk feliratokat az Aspose.Drawing for .NET használatával
url: /hu/net/use-cases/make-callout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan adjunk felhívásokat az Aspose.Drawing for .NET használatával

## Bevezetés
Ha **hogyan adjunk felhívásokat** a képeihez vagy diagramjaihoz az Aspose.Drawing for .NET használatával keres, jó helyen jár. Ebben az útmutatóban minden lépésen végigvezetünk – a bitmap betöltésétől, egy `Graphics` vászon létrehozásáig, a felhívás geometriájának meghatározásáig, a stílusos felhívások megjelenítéséig – hogy a vizuális elemei tisztábbak és informatívabbak legyenek.

## Gyors válaszok
- **Milyen könyvtárra van szükségem?** Aspose.Drawing for .NET (letölthető a hivatalos oldalról).  
- **Mely .NET verziók támogatottak?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Szükségem van licencre?** Egy ingyenes próba verzió fejlesztéshez megfelelő; a termeléshez kereskedelmi licenc szükséges.  
- **Mennyi időt vesz igénybe a megvalósítás?** Általában 10 perc alatt egy alap felhívás elkészítéséhez.  
- **Testreszabhatom a színeket és betűtípusokat?** Igen – minden a standard GDI+ objektumok (Pen, Font, Brush) alapján működik.

## Mi az a Callout?
A callout egy grafikus annotáció, amely egy vonalat (vagy nyilat) egy szövegcímkével kombinál, hogy kiemeljen egy adott részt a képen. Gyakran használják technikai diagramokban, képernyőképeken és prezentációkban, hogy felhívják a figyelmet egy konkrét elemre, magyarázzanak egy funkciót, vagy mérési információkat nyújtsanak, ezáltal a vizuális kommunikáció tisztábbá és hatékonyabbá válik.

## Miért használjuk az Aspose.Drawing-et Callout-okhoz?
Az Aspose.Drawing magas teljesítményű képfeldolgozásra készült, és széles körű formátumtámogatást nyújt, így ideális a callout-ok hozzáadásához nagy vagy összetett grafikákhoz. Memóriahatékony architektúrája akár **500 MB** méretű fájlok kezelését is lehetővé teszi anélkül, hogy az egész bitmapet RAM-ba töltené, és finomhangolt vezérlést biztosít a rajzolási primitívek, színek és szövegmegjelenítés felett, garantálva a tiszta, professzionális megjelenésű annotációkat.

## Előfeltételek
- Alapvető C# programozási nyelvi ismeretek.  
- Telepített Aspose.Drawing könyvtár. Letöltheti [itt](https://releases.aspose.com/drawing/net/).  
- Egy dokumentum vagy kép, amelyhez felhívásokat szeretne hozzáadni.

## Névterek importálása
Az alábbi névterek biztosítják a hozzáférést a fő rajzolási osztályokhoz:

`System.Drawing` GDI+ típusokat biztosít, mint a `Bitmap`, `Graphics`, `Pen`, `Font` és `Brush`. Importálja őket, mielőtt elkezdené a kódolást.

```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```

## Hogyan adjunk felhívásokat az Aspose.Drawing-ben
Töltse be a forrásképet, hozzon létre egy `Graphics` vászont, határozza meg a kezdő/végpontokat, és hívjon meg egy segédmetódust, amely megrajzolja a vonalat, a nyílfejet és a címkét – mindezt néhány tömör utasításban. Ez a megközelítés PNG, JPEG, BMP és GIF fájlok esetén működik, és lehetővé teszi a színek, betűtípusok és vonalstílusok teljes testreszabását.

## 1. lépés: Kép betöltése
Az `Image` egy raszteres képet képvisel, és módszereket biztosít a bitmap adatok betöltésére, mentésére és manipulálására. Kezdje a kép betöltésével, amelyhez felhívásokat szeretne hozzáadni. Cserélje le a `"Your Document Directory"` és a `"gears.png"` értékeket a saját könyvtárára és képfájl nevére.

```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Your code here
}
```

## 2. lépés: Graphics objektum létrehozása
A `Graphics` rajzolási felület metódusokat biztosít alakzatok, szöveg és képek bitmapre való megjelenítéséhez. A képből származó `Graphics` objektum lehetővé teszi a rajzolási műveletek végrehajtását.

```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```

## 3. lépés: Callout pozíciók meghatározása
A `PointF` egy pontot definiál kétdimenziós térben lebegőpontos koordinátákkal. Adja meg a kezdő (horgony) és vég (címke) pontokat minden egyes callout-hoz. Ezeknek a koordinátáknak a kép határain belül kell lenniük; ellenkező esetben a callout levágásra kerül.

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

## 4. lépés: Callout-ok rajzolása
Valósítsa meg a `DrawCallOut` metódust a vonal, az opcionális nyílfej és a szövegcímke megjelenítéséhez. A metódus a `Pen`-t használja a vonalhoz, a `Font`-ot a címkéhez, és a `SolidBrush`-t a kitöltő színekhez.

```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```

## 5. lépés: Kép mentése
Mentse el a megjegyzett bitmapet a lemezre. Választhat bármely támogatott formátumot, például PNG vagy JPEG.

```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```

## Callout forráskód megjelenítése
Az összes lépést összekapcsoló teljes forráskód az alábbi helyőrzőben található. Helyezze be saját megvalósítási részleteit a jelzett helyeken.

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
- **Helytelen horgony koordináták** – győződjön meg róla, hogy a kezdő és végpontok a kép határain belül vannak; ellenkező esetben a callout levágásra kerül.  
- **Szöveg átfedés** – állítsa be a `spaceSize`-t vagy a betűméretet, ha a címke más grafikákkal ütközik.  
- **Teljesítmény** – nagyon nagy képek esetén fontolja meg a `Pen`, `Font` és `Brush` objektumok használat után történő eldobását az erőforrások felszabadítása érdekében.

## Következtetés
Most már rendelkezik egy teljes, termelésre kész mintával arra, **hogyan adjunk felhívásokat** bármely képre az Aspose.Drawing for .NET használatával. Nyugodtan kísérletezzen különböző színekkel, vonalstílusokkal és betűcsaládokkal, hogy megfeleljen a márkájának.

## Gyakran Ismételt Kérdések

**Q:** Használhatom az Aspose.Drawing-et más típusú illusztrációkhoz?  
**A:** Igen, az Aspose.Drawing széles körű rajzolási műveleteket támogat diagramok, diagramok és egyedi grafikák esetén, nem csak egyszerű callout-okhoz.

**Q:** Kompatibilis az Aspose.Drawing különböző képformátumokkal?  
**A:** Teljes mértékben! Az Aspose.Drawing kezeli a PNG, JPEG, GIF, BMP, TIFF és még sok más formátumot.

**Q:** Hol találok további példákat és dokumentációt?  
**A:** Tekintse meg a részletes dokumentációt [itt](https://reference.aspose.com/drawing/net/).

**Q:** Hogyan kaphatok támogatást, ha problémáim vannak?  
**A:** Látogassa meg az [Aspose.Drawing fórumot](https://forum.aspose.com/c/drawing/44) a közösségi segítségért és a hivatalos támogatásért.

**Q:** Próbálhatom ki az Aspose.Drawing-et vásárlás előtt?  
**A:** Természetesen! Kezdje el egy ingyenes próba verzióval [itt](https://releases.aspose.com/).

---

**Utoljára frissítve:** 2026-08-01  
**Tesztelve:** Aspose.Drawing 24.11 for .NET  
**Szerző:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Kapcsolódó oktatóanyagok

- [Hogyan rajzolj íveket és egyéb alakzatokat az Aspose.Drawing for .NET használatával](/drawing/net/lines-curves-and-shapes/)
- [Mátrix transzformációs útmutató: Mátrix transzformációk az Aspose.Drawing for .NET-ben](/drawing/net/coordinate-transformations/matrix-transformations/)
- [Hogyan kapcsoljunk össze útvonalakat Pen-nel az Aspose.Drawing .NET-ben](/drawing/net/pens/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}