---
date: 2025-12-04
description: Ovládněte načítání obrázků, hromadnou konverzi obrázků a změny formátů
  v .NET pomocí Aspose.Drawing. Naučte se převádět BMP na PNG a další.
linktitle: Loading and Saving Images in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Převést BMP na PNG a další formáty pomocí Aspose.Drawing
url: /cs/net/image-editing/load-save/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod BMP na PNG a další formáty pomocí Aspose.Drawing

## Úvod

Vítejte v našem podrobném průvodci, jak **převést BMP na PNG** (a mnoho dalších formátů obrázků) pomocí Aspose.Drawing pro .NET. Ať už potřebujete **změnit formát obrázku** pro jediný soubor nebo provést **hromadný převod obrázků** u desítek fotografií, tento tutoriál vám přesně ukáže, jak načíst, transformovat a uložit obrázky s čistým, udržovatelným kódem.

## Rychlé odpovědi
- **Může Aspose.Drawing převést BMP na PNG?** Ano – stačí načíst BMP a zavolat `Save` s příponou .png.  
- **Je podporován hromadný převod?** Rozhodně; projděte soubory ve smyčce a znovu použijte stejnou metodu `LoadAndSave`.  
- **Potřebuji licenci pro produkci?** Licence je vyžadována pro produkční použití; dočasná licence je k dispozici pro hodnocení.  
- **Které verze .NET jsou kompatibilní?** Funguje s .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.  
- **Kde si mohu stáhnout knihovnu?** Získejte nejnovější balíček Aspose.Drawing z oficiální stránky ke stažení.

## Co je převod formátu obrázku v C# s Aspose.Drawing?

Aspose.Drawing je vysoce výkonná, plně spravovaná .NET knihovna, která nahrazuje starší `System.Drawing.Common`. Poskytuje vám plnou kontrolu nad scénáři **load image ASP.NET**, podporuje více než 100 formátů obrázků a odstraňuje platformově specifická omezení.

## Proč použít Aspose.Drawing pro hromadný převod obrázků?

- **Cross‑platform spolehlivost** – bez závislostí na GDI+.  
- **Bohatá podpora formátů** – BMP, GIF, JPG, PNG, TIFF a mnoho dalších.  
- **Konzistentní API** – stejný kód funguje na Windows, Linuxu i macOS.  
- **Výkon** – optimalizováno pro zpracování obrázků ve velkém měřítku.

## Požadavky

Než se pustíme dál, ujistěte se, že máte:

- **Aspose.Drawing pro .NET** – stáhněte si jej [zde](https://releases.aspose.com/drawing/net/).  
- Funkční **.NET vývojové prostředí** (Visual Studio, VS Code nebo Rider).  

Nyní, když máme vše připravené, importujme požadované jmenné prostory a začněme kódovat.

## Import jmenných prostorů

Ve vašem .NET projektu začněte importováním potřebného jmenného prostoru:

```csharp
using System.Drawing;
```

Tyto třídy poskytují základní funkčnost pro načítání a ukládání obrázků.

## Krok 1: Načtení obrázku

Prvním krokem je načíst soubor obrázku. Níže uvedený příklad ukazuje načítání obrázků v různých formátech, včetně BMP, který později převedeme na PNG.

```csharp
public static void Run()
{
    LoadAndSave("bmp");
    LoadAndSave("gif");
    LoadAndSave("jpg");
    LoadAndSave("png");
    LoadAndSave("tiff");
}
```

## Jak převést BMP na PNG pomocí Aspose.Drawing

Metoda `LoadAndSave` zajišťuje jak načtení zdrojového souboru, tak jeho uložení do požadovaného výstupního formátu. Předáním argumentu `"bmp"` metoda automaticky vytvoří PNG soubor, když změníte příponu v `outputPath`.

### Krok 2.1: Načtení obrázku

```csharp
private static void LoadAndSave(string graphicsFileFormats)
{
    string inputPath = "Your Document Directory" + @"GraphicsFileFormats\image." + graphicsFileFormats;
    Bitmap loadedImage = new Bitmap(inputPath);
}
```

### Krok 2.2: Uložení obrázku (změna formátu obrázku)

```csharp
private static void LoadAndSave(string graphicsFileFormats)
{
    string inputPath = "Your Document Directory" + @"GraphicsFileFormats\image." + graphicsFileFormats;
    string outputPath = "Your Document Directory" + @"GraphicsFileFormats\image_out." + graphicsFileFormats;
    
    Bitmap loadedImage = new Bitmap(inputPath);
    
    // Save the image
    loadedImage.Save(outputPath);
}
```

Opakujte volání `LoadAndSave` pro každý formát obrázku, který chcete zpracovat. Úpravou přípony v `outputPath` můžete **převést BMP na PNG**, **změnit formát obrázku** na GIF, JPG atd., vše pomocí stejné metody.

## Časté úskalí a tipy

- **Oddělovače cest** – Používejte `Path.Combine` pro bezpečnost napříč platformami místo ručního spojování řetězců.  
- **Uvolňování Bitmap** – Zabalte `Bitmap` do bloku `using`, aby se rychle uvolnily nativní zdroje.  
- **Nastavení kvality** – Při ukládání JPEGů zvažte specifikaci objektu `EncoderParameters` pro řízení kvality komprese.  
- **Hromadné zpracování** – Umístěte soubory obrázků do složky a iterujte pomocí `Directory.GetFiles`, abyste automatizovali převody ve velkém měřítku.

## Často kladené otázky

### Q1: Je Aspose.Drawing kompatibilní se všemi formáty obrázků?

A1: Aspose.Drawing podporuje širokou škálu formátů, včetně BMP, GIF, JPG, PNG a TIFF.

### Q2: Kde najdu podrobnou dokumentaci k Aspose.Drawing?

A2: Prohlédněte si oficiální dokumentaci [zde](https://reference.aspose.com/drawing/net/).

### Q3: Jak získám dočasnou licenci pro Aspose.Drawing?

A3: Navštivte [zde](https://purchase.aspose.com/temporary-license/) pro podrobnosti o dočasné licenci.

### Q4: Co když narazím na problémy nebo mám otázky během implementace?

A4: Požádejte o pomoc komunitu Aspose.Drawing na [Aspose Forum](https://forum.aspose.com/c/drawing/44).

### Q5: Kde si mohu zakoupit knihovnu Aspose.Drawing?

A5: Můžete ji zakoupit [zde](https://purchase.aspose.com/buy).

**Additional Q&A**

**Q: Mohu tento kód použít v ASP.NET webové aplikaci?**  
A: Ano – stejná logika `LoadAndSave` funguje v ASP.NET, MVC nebo Razor Pages; jen zajistěte, aby souborové cesty byly přístupné webovému procesu.

**Q: Je možné zpracovávat obrázky paralelně pro rychlejší hromadný převod?**  
A: Rozhodně. Zabalte volání `LoadAndSave` do smyčky `Parallel.ForEach`, ale nezapomeňte řešit bezpečné uvolňování `Bitmap` objektů v rámci vláken.

## Závěr

Nyní jste se naučili, jak **převést BMP na PNG**, provádět **hromadný převod obrázků** a **změnit formát obrázku** pomocí Aspose.Drawing pro .NET. Použijte tyto vzory k automatizaci obrazových pipeline, generování miniatur nebo přípravě zdrojů pro webové doručení. Experimentujte s různými formáty, integrujte kód do svých služeb a užívejte si spolehlivost plně spravované kreslicí knihovny.

---

**Last Updated:** 2025-12-04  
**Tested With:** Aspose.Drawing 24.12 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}