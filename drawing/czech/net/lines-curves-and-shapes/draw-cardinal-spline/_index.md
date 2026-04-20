---
date: 2026-02-12
description: Naučte se, jak uložit obrázek a kreslit kardinální spline v .NET pomocí
  Aspose.Drawing. Uložte křivku jako PNG a vytvořte hladkou grafiku bez námahy.
linktitle: Drawing Cardinal Splines in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Jak uložit obrázek a kreslit kardinální spline v Aspose.Drawing
url: /cs/net/lines-curves-and-shapes/draw-cardinal-spline/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak uložit obrázek a kreslit kardinální spline v Aspose.Drawing

## Úvod

V tomto tutoriálu se dozvíte **jak uložit obrázek** při kreslení hladkých kardinálních spline pomocí Aspose.Drawing pro .NET. Ať už vytváříte komponentu pro grafy, editor diagramů nebo jen potřebujete exportovat vlastní křivku jako PNG, níže uvedené kroky vám přesně ukážou, jak nakreslit křivku perem, přizpůsobit spline a výsledek uložit na disk.

## Rychlé odpovědi
- **Co dělá hlavní metoda?** `Graphics.DrawCurve` interpoluje sérii bodů do hladké kardinální spline.  
- **Jaký formát se používá pro uložení obrázku?** PNG pomocí `Bitmap.Save`.  
- **Potřebuji licenci pro ukládání obrázků?** Zkušební verze funguje pro vývoj; pro produkci je vyžadována komerční licence.  
- **Mohu změnit napětí křivky?** Ano, přetížení `DrawCurve` umožňují zadat napětí.  
- **Je Aspose.Drawing kompatibilní s .NET 6+?** Naprosto – podporuje .NET Framework i .NET Core/5/6.

## Co znamená „jak uložit obrázek“ v kontextu Aspose.Drawing?
Uložení obrázku znamená převést bitmapu v paměti, na které kreslíte, na fyzický soubor, například PNG, JPEG nebo BMP. Aspose.Drawing poskytuje jednoduchou metodu `Bitmap.Save`, která se postará o kódování za vás.

## Proč kreslit kardinální spline pomocí Aspose.Drawing?
Kardinální spline vám poskytuje hladkou, plynulou křivku, která prochází blízko sady řídicích bodů, ideální pro vizualizaci dat, UI grafiku a vlastní tvary. S Aspose.Drawing se vyhnete omezením `System.Drawing.Common` a získáte konzistenci napříč platformami.

## Požadavky

Předtím, než se pustíme do práce, ujistěte se, že máte:

- Visual Studio (jakákoli aktuální verze) nainstalováno.  
- Knihovnu Aspose.Drawing pro .NET. Můžete si ji stáhnout [zde](https://releases.aspose.com/drawing/net/).  
- Základní znalost programování v C#.

## Importování jmenných prostorů

Ve vašem souboru C# začněte importovat potřebný jmenný prostor:

```csharp
using System.Drawing;
```

## Krok 1: Vytvořte Bitmap (plátno)

Nejprve vytvořte bitmapu, která bude sloužit jako plátno pro vaše kreslení. Tato bitmapa je místem, kde bude spline vykreslena, než **uložíte obrázek**.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## Krok 2: Vytvořte objekt Graphics

Dále získejte objekt `Graphics` z bitmapy. Tento objekt poskytuje kreslicí plochu.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## Krok 3: Definujte pero a nakreslete křivku

Definujte `Pen` s požadovanou barvou a šířkou, poté nakreslete kardinální spline pomocí `DrawCurve`. Tím demonstrujete techniku **draw curve with pen** a slouží jako **cardinal spline example**.

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

## Krok 4: Uložte obrázek (uložte křivku jako PNG)

Nakonec uložte bitmapu do souboru PNG. Toto je jádro **how to save image** v tomto tutoriálu.

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawCardinalSpline_out.png");
```

> **Pro tip:** Použijte `Path.Combine` k bezpečnému sestavování cest k souborům napříč platformami.

Gratulujeme! Úspěšně jste nakreslili kardinální spline a uložili výsledek jako PNG obrázek pomocí Aspose.Drawing pro .NET. Nebojte se experimentovat s různými poli bodů, barvami per nebo šířkami čar, abyste své křivky přizpůsobili.

## Běžné případy použití

- **Vizualizace dat** – hladké čárové grafy, které vyžadují přesné řídicí body.  
- **Vlastní UI komponenty** – kreslení knoflíků, posuvníků nebo dekorativních ohraničení.  
- **Exportovatelná grafika** – generování PNG aktiv za běhu pro reporty nebo webový obsah.

## Řešení problémů a tipy

- **Obrázek je prázdný?** Ujistěte se, že formát pixelů bitmapy podporuje alfa kanál (`Format32bppPArgb`) a že voláte `graphics.Clear(Color.Transparent)`, pokud je to potřeba.  
- **Neočekávaný tvar křivky?** Upravit parametr napětí pomocí přetížení `DrawCurve(pen, points, tension)`.  
- **Chyby při přístupu k souboru?** Ověřte, že cílový adresář existuje a že má vaše aplikace oprávnění k zápisu.

## Často kladené otázky

### Q1: Můžu používat Aspose.Drawing v komerčních projektech?
A1: Ano, Aspose.Drawing je vhodný jak pro osobní, tak pro komerční projekty. Podrobnosti o licencování najdete na [stránce nákupu](https://purchase.aspose.com/buy).

### Q2: Jak získám dočasnou licenci pro testování?
A2: Dočasnou licenci pro testovací účely získáte [zde](https://purchase.aspose.com/temporary-license/).

### Q3: Kde mohu najít další podporu?
A3: Navštivte [forum Aspose.Drawing](https://forum.aspose.com/c/drawing/44) pro komunitní podporu a diskuze.

### Q4: Je k dispozici bezplatná zkušební verze?
A4: Ano, před zakoupením můžete vyzkoušet funkce pomocí [bezplatné zkušební verze](https://releases.aspose.com/).

### Q5: Jak získám přístup k dokumentaci?
A5: Odkazujte na komplexní [dokumentaci](https://reference.aspose.com/drawing/net/), kde najdete podrobné informace a příklady.

### Q6: Můžu změnit výstupní formát na JPEG?
A6: Rozhodně. Nahraďte příponu `.png` příponou `.jpg` a v metodě `Save` specifikujte `ImageFormat.Jpeg`.

### Q7: Je možné kreslit více spline na stejnou bitmapu?
A7: Ano, stačí volat `graphics.DrawCurve` několikrát s různými poli bodů a pery.

## Závěr

V tomto průvodci jsme pokryli **jak uložit obrázek** po nakreslení kardinální spline, předvedli praktické **draw curve using C#** a zdůraznili běžné scénáře, kde tato technika vyniká. Nyní máte pevný základ pro integraci hladkých spline grafiky do jakékoli .NET aplikace.

---

**Last Updated:** 2026-02-12  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}