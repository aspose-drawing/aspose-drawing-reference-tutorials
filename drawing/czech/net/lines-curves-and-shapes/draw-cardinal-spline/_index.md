---
date: 2026-05-29
description: Naučte se, jak uložit PNG a kreslit kardinalní spline v .NET s Aspose.Drawing.
  Uložte křivku jako PNG, vytvořte plynulé grafiky a snadno generujte bitmapu do souboru.
keywords:
- how to save png
- save bitmap to file
- create smooth curve
- draw curve c#
- generate png graphics
linktitle: Kreslení kardinalních spline v Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn how to save PNG and draw cardinal splines in .NET with Aspose.Drawing.
    Save curve as PNG, create smooth graphics, and generate bitmap to file effortlessly.
  headline: How to Save PNG and Draw Cardinal Splines with Aspose.Drawing
  type: TechArticle
- questions:
  - answer: '`Graphics.DrawCurve` interpolates a series of points into a smooth cardinal
      spline.'
    question: What does the primary method do?
  - answer: PNG via `Bitmap.Save`.
    question: Which format is used to save the image?
  - answer: A trial works for development; a commercial license is required for production.
    question: Do I need a license to save images?
  - answer: Yes, overloads of `DrawCurve` let you specify tension.
    question: Can I change the curve tension?
  - answer: Absolutely – it supports .NET Framework and .NET Core/5/6.
    question: Is Aspose.Drawing compatible with .NET 6+?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Jak uložit PNG a kreslit kardinalní spline pomocí Aspose.Drawing
url: /cs/net/lines-curves-and-shapes/draw-cardinal-spline/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak uložit PNG a kreslit kardinální spline pomocí Aspose.Drawing

## Úvod

V tomto tutoriálu se dozvíte **jak uložit PNG** soubory při kreslení hladkých kardinálních spline pomocí Aspose.Drawing pro .NET. Ať už vytváříte komponentu pro grafy, editor diagramů nebo jen potřebujete exportovat vlastní křivku jako PNG, níže uvedené kroky vás provedou vytvořením bitmapového plátna, kreslením spline perem a uložením výsledku na disk. Také uvidíte, proč je Aspose.Drawing spolehlivou multiplatformní alternativou k System.Drawing.Common.

## Rychlé odpovědi
- **Co dělá hlavní metoda?** `Graphics.DrawCurve` interpoluje sérii bodů do hladké kardinální spline.  
- **Jaký formát se používá pro uložení obrázku?** PNG pomocí `Bitmap.Save`.  
- **Potřebuji licenci pro ukládání obrázků?** Zkušební verze funguje pro vývoj; pro produkci je vyžadována komerční licence.  
- **Mohu změnit napětí křivky?** Ano, přetížení `DrawCurve` vám umožní zadat napětí.  
- **Je Aspose.Drawing kompatibilní s .NET 6+?** Naprosto – podporuje .NET Framework i .NET Core/5/6.

## Co znamená „jak uložit PNG“ v kontextu Aspose.Drawing?

Uložení PNG znamená převod bitmapy v paměti, na které kreslíte, do fyzického PNG souboru na disku. Proces zapisuje data pixelů pomocí bezztrátové komprese, zachovává přesné barvy a informace o alfa kanálu. Metoda `Bitmap.Save` v Aspose.Drawing automaticky zpracuje PNG kódování, takže nemusíte sami spravovat podrobnosti formátu.

## Proč kreslit kardinální spline pomocí Aspose.Drawing?

Kardinální spline vytváří hladkou, plynulou křivku, která úzce sleduje sadu řídících bodů, což ji činí ideální pro vizualizaci dat, UI grafiku a vlastní tvary. Aspose.Drawing podporuje **více než 30 formátů obrázků** a dokáže vykreslit grafiku o stovkách stránek, aniž by načítal celý soubor do paměti, což vám poskytuje jak rychlost, tak flexibilitu.

## Požadavky

- Visual Studio (jakákoli aktuální verze) nainstalováno.  
- Knihovna Aspose.Drawing pro .NET. Můžete si ji stáhnout [zde](https://releases.aspose.com/drawing/net/).  
- Základní znalost programování v C#.

## Importovat jmenné prostory

Ve vašem souboru C# začněte importováním potřebného jmenného prostoru:

Jmenný prostor `Aspose.Drawing` obsahuje všechny základní typy jako `Bitmap`, `Graphics` a `Pen`.  
```csharp
using Aspose.Drawing;
```
```csharp
using System.Drawing;
```

## Krok 1: Vytvořit bitmapu (plátno)

Nejprve vytvořte bitmapu, která bude sloužit jako plátno pro vaše kreslení. Tato bitmapa je místem, kde bude spline vykreslena, než **uložíte obrázek**.

Bitmap představuje obrázek v paměti s definovaným formátem pixelů a rozměry.  
```csharp
int width = 800;
int height = 600;
Bitmap bitmap = new Bitmap(width, height, PixelFormat.Format32bppPArgb);
```
```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## Krok 2: Vytvořit objekt Graphics

Dále z bitmapy získejte objekt `Graphics`. Tento objekt poskytuje kreslicí plochu.

Graphics poskytuje kreslicí plochu pro vykreslování tvarů, textu a obrázků na bitmapu.  
```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.Transparent);
```
```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## Krok 3: Definovat pero a kreslit křivku

Definujte `Pen` s požadovanou barvou a šířkou a poté nakreslete kardinální spline pomocí `DrawCurve`. Toto demonstruje techniku **kreslení křivky perem** a slouží jako **příklad kardinální spline**.

Pen zapouzdřuje barvu, šířku a styl čáry používané pro kreslení čar a křivek.  
```csharp
Pen pen = new Pen(Color.Blue, 3);
PointF[] points = {
    new PointF(100, 400), new PointF(200, 100),
    new PointF(300, 300), new PointF(400, 150),
    new PointF(500, 350)
};
graphics.DrawCurve(pen, points, 0.5f); // tension = 0.5
```
```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawCurve(pen, new Point[] {
    new Point(10, 700),
    new Point(250, 500),
    new Point(500, 10),
    new Point(750, 500),
    new Point(990, 700)
});
```

## Krok 4: Uložit obrázek (uložit křivku jako PNG)

Nakonec uložte bitmapu do souboru PNG. To je jádro **jak uložit PNG** v tomto tutoriálu.

Bitmap.Save zapíše obrázek do souboru ve zvoleném formátu, například PNG.  
```csharp
string outputPath = Path.Combine(Environment.CurrentDirectory, "cardinal-spline.png");
bitmap.Save(outputPath, ImageFormat.Png);
```
```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawCardinalSpline_out.png");
```

> **Tip:** Použijte `Path.Combine` pro bezpečnou tvorbu cest k souborům napříč platformami.

Gratulujeme! Úspěšně jste nakreslili kardinální spline a uložili výsledek jako PNG obrázek pomocí Aspose.Drawing pro .NET. Nebojte se experimentovat s různými poli bodů, barvami per nebo šířkami čar pro přizpůsobení vašich křivek.

## Běžné případy použití

- **Vizualizace dat** – hladké čárové grafy, které potřebují přesné řídící body.  
- **Vlastní UI komponenty** – kreslení knoflíků, posuvníků nebo dekorativních okrajů.  
- **Exportovatelná grafika** – generování PNG aktiv za běhu pro reporty nebo webový obsah.

## Řešení problémů a tipy

- **Obrázek je prázdný?** Ujistěte se, že formát pixelů bitmapy podporuje alfa (`Format32bppPArgb`) a v případě potřeby zavolejte `graphics.Clear(Color.Transparent)`.  
- **Neočekávaný tvar křivky?** Upravte parametr napětí pomocí přetížení `DrawCurve(pen, points, tension)`.  
- **Chyby přístupu k souboru?** Ověřte, že cílový adresář existuje a že má vaše aplikace oprávnění k zápisu.

## Často kladené otázky

**Q1: Mohu používat Aspose.Drawing pro komerční projekty?**  
A1: Ano, Aspose.Drawing je vhodný jak pro osobní, tak pro komerční projekty. Podrobnosti o licencování najdete na [stránce nákupu](https://purchase.aspose.com/buy).

**Q2: Jak získám dočasnou licenci pro testování?**  
A2: Získejte dočasnou licenci pro testovací účely [zde](https://purchase.aspose.com/temporary-license/).

**Q3: Kde najdu další podporu?**  
A3: Navštivte [forum Aspose.Drawing](https://forum.aspose.com/c/drawing/44) pro komunitní podporu a diskuze.

**Q4: Je k dispozici bezplatná zkušební verze?**  
A4: Ano, vyzkoušejte funkce pomocí verze [bezplatné zkušební verze](https://releases.aspose.com/) před zakoupením.

**Q5: Jak získám přístup k dokumentaci?**  
A5: Odkazujte na komplexní [dokumentaci](https://reference.aspose.com/drawing/net/) pro podrobné informace a příklady.

---

**Poslední aktualizace:** 2026-05-29  
**Testováno s:** Aspose.Drawing 24.11 pro .NET  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Související tutoriály

- [Uložit bitmapu jako PNG a kreslit uzavřené křivky pomocí Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-closed-curve/)
- [Uložit bitmapu C# – kreslit Bézierovy spline pomocí Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-bezier-spline/)
- [Uložit bitmapu jako PNG s pevnými štětci v Aspose.Drawing](/drawing/net/lines-curves-and-shapes/solid-brushes/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}