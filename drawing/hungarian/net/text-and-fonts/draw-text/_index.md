---
date: 2026-09-23
description: Ismerje meg, hogyan lehet szöveget rajzolni képre az Aspose.Drawing for
  .NET használatával. Készítsen szöveges képet, adjon szöveget bitmaphez, és mentse
  a bitmapet PNG formátumban egyedi betűtípusokkal.
keywords:
- draw text on image
- generate image with text
- custom font on image
- save bitmap as png
- add text to bitmap
lastmod: 2026-09-23
linktitle: Szöveg rajzolása az Aspose.Drawing segítségével
og_description: Ismerje meg, hogyan lehet szöveget rajzolni képre az Aspose.Drawing
  for .NET használatával. Ez az útmutató bemutatja, hogyan készítsen szöveges képet,
  adjon szöveget bitmaphez, és mentse a bitmapet PNG formátumban egyedi betűtípusokkal.
og_image_alt: Screenshot of a PNG image created with Aspose.Drawing showing custom
  text
og_title: Szöveg rajzolása képre az Aspose.Drawing for .NET – Gyors útmutató
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to draw text on image using Aspose.Drawing for .NET. Generate
    image with text, add text to bitmap, and save bitmap as PNG with custom fonts.
  headline: How to draw text on image with Aspose.Drawing for .NET
  type: TechArticle
- questions:
  - answer: Replace the `.png` extension with `.jpg` in the `Save` method and optionally
      specify an `ImageCodecInfo` for JPEG quality.
    question: How do I change the output format to JPEG?
  - answer: Yes, include line‑break characters (`\n`) in the string or use `StringFormat`
      with `FormatFlags.LineLimit`.
    question: Can I draw multi‑line text?
  - answer: Use `Graphics.MeasureString` to get the exact dimensions of the rendered
      text.
    question: Is there a way to measure text size before drawing?
  - answer: Absolutely. Provide a font that contains the required glyphs and the library
      will render them correctly.
    question: Does Aspose.Drawing support Unicode characters?
  - answer: The examples were tested with Aspose.Drawing 24.11 for .NET.
    question: What version of Aspose.Drawing was used for testing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- draw text on image
- Aspose.Drawing
- .NET image processing
- generate image with text
- custom font on image
title: Szöveg rajzolása képre az Aspose.Drawing for .NET segítségével
url: /hu/net/text-and-fonts/draw-text/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan rajzoljunk szöveget képre az Aspose.Drawing for .NET segítségével

## Bevezetés

Ebben a lépésről‑lépésre útmutatóban megtanulja, **hogyan rajzoljon szöveget képre** az Aspose.Drawing for .NET használatával. Akár egy *dinamikus szöveges képet* szeretne létrehozni, szöveget hozzáadni egy meglévő bitmaphez, vagy egy grafikát egyedi betűtípusokkal generálni, ez a tutorial minden részletet bemutat, így percek alatt elkezdhet szöveget rajzolni. A könyvtár több mint 30 GDI+ metódust támogat, Windows, Linux és macOS rendszereken fut, és **nulla külső függőséggel** rendelkezik, ami megbízható választássá teszi a szerver‑oldali képgeneráláshoz.

## Gyors válaszok

- **Melyik könyvtárat használják?** Aspose.Drawing for .NET  
- **Elsődleges feladat?** Szöveg rajzolása képre (kép létrehozása szöveggel)  
- **Kulcsfontosságú metódus?** `Graphics.DrawString` (szöveg rajzolása képre)  
- **Kimeneti formátum?** PNG (bitmap mentése PNG‑ként)  
- **Előfeltételek?** .NET fejlesztői környezet és Aspose.Drawing könyvtár  

## Mi az a szöveg rajzolása az Aspose.Drawing segítségével?

A szöveg rajzolása az Aspose.Drawing segítségével azt jelenti, hogy a könyvtár GDI+‑kompatibilis API‑ját használjuk Unicode karakterláncok raster vászonra való renderelésére. A `Graphics.DrawString` metódus a szöveget egy bitmapbe írja, lehetővé téve a betűtípus, szín, igazítás és anti‑aliasing szabályozását. Ez a megközelítés lehetővé teszi magas minőségű képek generálását a System.Drawing.Common telepítése nélkül.

## Miért használjuk az Aspose.Drawing‑ot szöveg hozzáadásához a képekhez?

Az Aspose.Drawing megbízható, platform‑független módot kínál a szöveg képekre való renderelésére anélkül, hogy natív GDI+ könyvtárakra lenne szükség, így konzisztens minőséget és teljesítményt biztosít minden operációs rendszeren. Támogatja a fejlett anti‑aliasingot, Unicode karaktereket és egyedi betűtípusokat, valamint zökkenőmentesen integrálódik a .NET alkalmazásokba, ami ideálissá teszi szerver‑oldali képgeneráláshoz és asztali eszközökhöz egyaránt.

- **Platform‑független megbízhatóság** – működik Windows, Linux és macOS rendszereken.  
- **Fejlett renderelés** – anti‑aliasing és alpixel szövegsimítás a tiszta kimenetért.  
- **Nincs külső függőség** – a könyvtár mindent tartalmaz, ami szükséges a *kép létrehozásához szöveggel*.

## Előfeltételek

Mielőtt belemerülne, győződjön meg róla, hogy rendelkezik:

- **Aspose.Drawing for .NET** – töltse le a [Aspose.Drawing dokumentációból](https://reference.aspose.com/drawing/net/).  
- **.NET IDE‑vel**, például Visual Studio vagy VS Code.

## Névterek importálása

Kezdje a szükséges névterek importálásával:

Ezek a névterek biztosítják a GDI+ alapvető típusokat, mint a `Bitmap`, `Graphics`, és a szöveg rendereléshez szükséges segédeszközöket.

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## 1. lépés: bitmap és graphics objektumok létrehozása

`Bitmap` az Aspose.Drawing raszteres kép tárolója a pixeladatokhoz, a `Graphics` pedig rajzolási metódusokat biztosít a formák és szöveg megjelenítéséhez.

A `Bitmap` egy memóriában lévő képet képvisel, míg a `Graphics` rajzolási metódusokat biztosít a bitmapre való rendereléshez.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

Itt hozunk létre egy `Bitmap`‑et, amely a végső képet tárolja, és egy `Graphics` objektumot, amely lehetővé teszi a rajzolást. Az anti‑aliasing beállítás biztosítja, hogy a szöveg simán jelenjen meg.

## 2. lépés: ecset, toll és betűtípus beállítása

`Brush` meghatározza a kitöltő színt, a `Pen` a formák körvonalát, a `Font` pedig a betűtípust, méretet és stílust a szöveg rendereléséhez.

`Brush` színekkel tölti ki a formákat, a `Pen` körvonalazza őket, a `Font` pedig meghatározza a betűtípust és méretet a szöveg rendereléséhez.

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

- **Brush** a szöveg színét határozza meg.  
- **Pen** később egy téglalap rajzolására szolgál a szöveg körül (opcionális).  
- **Font** a betűtípust, méretet és stílust határozza meg a *szöveg rajzolása képre* művelethez.

## 3. lépés: szöveg és téglalap meghatározása

`Rectangle` meghatározza a határoló dobozt, ahol a szöveget elhelyezzük, megadva az X/Y koordinátákat és a szélességet/magasságot.

`Rectangle` meghatározza egy téglalap alakú terület pozícióját és méretét, amelyet itt a rajzolt szöveg körül határolásra használunk.

```csharp
string text = "Lorem ipsum..."; // (Your desired text)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
```

A `Rectangle` határozza meg, hol kerül a szöveg. Állítsa be a koordinátákat és a méretet a saját elrendezéséhez.

## 4. lépés: téglalap és szöveg rajzolása

`Graphics.DrawString` a megadott szöveget a megadott téglalapba rendereli a megadott betűtípussal és ecsettel.

`Graphics.DrawString` egy szövegsorozatot renderel egy meghatározott téglalapba a megadott betűtípussal és ecsettel.

```csharp
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle);
```

Először egy kék téglalappal körvonalazzuk a területet, majd a `DrawString` hívásával **szöveget adunk a bitmaphez**. Ez a *szöveg rajzolása* a képen magja.

## 5. lépés: az eredmény mentése

A kép PNG fájlként kerül mentésre, teljesítve a *bitmap mentése PNG‑ként* követelményt. Cserélje le a helyőrző útvonalat a tényleges mappára, ahová a fájlt menteni szeretné.

`bitmap.Save` a képet a kiválasztott formátumban, például PNG‑ként, fájlba írja.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\DrawText_out.png");
```

## Gyakori felhasználási esetek

- **Tanúsítványok generálása** személyre szabott nevekkel.  
- **Vízjelezett bélyegképek létrehozása** webgalériákhoz.  
- **Dinamikus diagramok építése**, amelyek címkéket vagy megjegyzéseket tartalmaznak.

## Hibakeresés és tippek

- **Betűtípus nem található?** Győződjön meg róla, hogy a betűtípus telepítve van a gépen, vagy használjon privát betűtípus-gyűjteményt.  
- **Szöveg levágva?** Növelje a téglalap méretét vagy csökkentse a betűméretet.  
- **Teljesítmény aggályok?** Amikor csak lehetséges, használja újra ugyanazt a `Graphics` objektumot több rajzolási művelethez.

## Gyakran ismételt kérdések

**K: Hogyan változtathatom meg a kimeneti formátumot JPEG‑re?**  
V: Cserélje le a `.png` kiterjesztést `.jpg`‑re a `Save` metódusban, és opcionálisan adjon meg egy `ImageCodecInfo`‑t a JPEG minőséghez.

**K: Rajzolhatok több soros szöveget?**  
V: Igen, a karakterláncba helyezzen sortörés karaktereket (`\n`), vagy használja a `StringFormat`‑ot a `FormatFlags.LineLimit`‑el.

**K: Van mód a szöveg méretének mérésére rajzolás előtt?**  
V: Használja a `Graphics.MeasureString`‑t a renderelt szöveg pontos méretének meghatározásához.

**K: Támogatja az Aspose.Drawing a Unicode karaktereket?**  
V: Teljes mértékben. Adjon meg egy olyan betűtípust, amely tartalmazza a szükséges glifeket, és a könyvtár helyesen rendereli őket.

**K: Melyik Aspose.Drawing verziót használták a teszteléshez?**  
V: A példák az Aspose.Drawing 24.11 for .NET verzióval lettek tesztelve.

---

**Utoljára frissítve:** 2026-09-23  
**Tesztelve ezzel:** Aspose.Drawing 24.11 for .NET  
**Szerző:** Aspose

## Kapcsolódó tutorialok

- [Bitmap grafika létrehozása C# – PNG kép mentése és telepített betűtípusok használata az Aspose.Drawing‑ban](/drawing/net/text-and-fonts/installed-fonts/)
- [Hogyan mentse a bitmapet PNG‑ként az Aspose.Drawing API‑val .NET‑hez](/drawing/net/image-editing/display/)
- [Szöveg képen](/drawing/net/use-cases/text-on-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}