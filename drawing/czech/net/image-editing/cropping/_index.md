---
date: 2026-02-07
description: Krok za krokem návod, jak oříznout obrázek do PNG pomocí Aspose.Drawing,
  alternativy k System.Drawing pro vývojáře .NET. Obsahuje hromadné ořezávání a základní
  techniky.
linktitle: Image Cropping Tutorial – Aspose.Drawing
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
title: Jak oříznout obrázek do PNG pomocí Aspose.Drawing pro .NET
url: /cs/net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak oříznout obrázek na PNG pomocí Aspose.Drawing pro .NET

Pokud potřebujete **oříznout obrázek na PNG** rychle a spolehlivě v prostředí .NET, jste na správném místě. V tomto tutoriálu vás provedeme přesnými kroky, jak načíst obrázek, definovat oblast ořezu a uložit výsledek jako soubor PNG — vše pomocí Aspose.Drawing, moderní **alternativy k System.Drawing**, která funguje napříč platformami.

## Rychlé odpovědi
- **Jakou knihovnu použít?** Aspose.Drawing pro .NET (plnohodnotná alternativa k System.Drawing.Common)  
- **Jak dlouho trvá základní ořez?** Obvykle méně než sekunda pro jeden obrázek na moderním procesoru  
- **Mohu ořezat do PNG?** Ano — uložte oříznutý bitmap jako soubor PNG (viz Krok 6)  
- **Potřebuji licenci?** Bezplatná zkušební verze funguje pro vývoj; pro produkci je vyžadována komerční licence  
- **Je možný hromadný (batch) processing?** Rozhodně — zabalte stejné kroky do smyčky pro zpracování více souborů  

## Co je „oříznutí obrázku na PNG“?

Oříznutí obrázku znamená vyříznutí obdélníkové oblasti z původního bitmapu. Když tuto oblast uložíte jako PNG, zachováte průhlednost a získáte bezztrátovou kompresi — ideální pro miniatury, ikony nebo jakýkoli UI prvek.

## Proč je Aspose.Drawing alternativou k System.Drawing?

- **Podpora napříč platformami** — běží na Windows, Linuxu i macOS bez nativních závislostí na GDI+.  
- **Pokročilá manipulace s formáty pixelů** — 32‑bit, 24‑bit, indexované a další.  
- **API zaměřené na výkon** — ideální jak pro úpravy jednotlivých obrázků, tak pro rozsáhlé hromadné úlohy.  

## Požadavky

Než se pustíme dál, ujistěte se, že máte:

- **Knihovnu Aspose.Drawing** integrovanou ve vašem .NET projektu. Můžete si ji stáhnout [zde](https://releases.aspose.com/drawing/net/).  
- Složku, která obsahuje zdrojové obrázky, které chcete oříznout. Nahraďte `"Your Document Directory"` v ukázkách kódu skutečnou cestou na vašem počítači.

## Importování jmenných prostorů

```csharp
using System.Drawing;
```

Jmenný prostor `System.Drawing` nám poskytuje přístup k typům `Bitmap`, `Graphics` a dalším, které Aspose.Drawing rozšiřuje.

## Průvodce krok za krokem

### Krok 1: Vytvoření bitmapové plátna

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

Začínáme s prázdným plátnem o rozměrech, které pojmou oříznutý výsledek. Nastavte šířku a výšku tak, aby odpovídaly rozměrům oblasti, kterou chcete vyříznout.

### Krok 2: Vytvoření objektu Graphics

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

Objekt `Graphics` nám umožňuje kreslit na plátno. `InterpolationMode` řídí, jak jsou během škálování nebo transformace počítány hodnoty pixelů — `NearestNeighbor` funguje dobře pro ostré hrany.

### Krok 3: Načtení obrázku k ořezu

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

Načtěte zdrojový obrázek. Ujistěte se, že cesta ukazuje na existující soubor; jinak bude vyvolána výjimka.

### Krok 4: Definování zdrojových a cílových obdélníků

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

`sourceRectangle` určuje API, kterou část původního obrázku zachovat. Zde vybíráme oblast 50 × 40 pixelů v levém horním rohu. Přiřazením stejného obdélníku do `destinationRectangle` zachováme oříznutou oblast v původní velikosti.

### Krok 5: Provedení operace ořezu

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

`Graphics.DrawImage` zkopíruje definovanou část `image` na naše prázdné `bitmap`. Toto je jádro operace **oříznutí obrázku na PNG**.

### Krok 6: Uložení oříznutého obrázku (oříznutí obrázku na PNG)

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

Nakonec zapíšeme plátno na disk jako soubor PNG. PNG zachovává alfa kanál a poskytuje bezztrátovou kvalitu — ideální pro UI prvky.

## Jak ořezávat obrázky ve scénáři hromadného zpracování

Když máte desítky nebo stovky obrázků, stačí celý úryvek umístit do smyčky `foreach`, která prochází kolekcí cest k souborům. Stejná logika `Graphics.DrawImage` se použije, což dělá **hromadné ořezávání obrázků** triviální rozšíření tohoto tutoriálu.

## Časté úskalí a tipy

- **Neshody formátů pixelů** — zajistěte, aby zdrojový obrázek a bitmapa plátna sdílely kompatibilní formát pixelů, aby nedošlo k posunu barev.  
- **Uvolňování GDI objektů** — zabalte `Bitmap` a `Graphics` do `using` bloků nebo zavolejte `Dispose()` ručně; jinak můžete uniknout neřízené prostředky.  
- **Chyby souřadnic** — souřadnice obdélníku jsou nulové. Výběr obdélníku, který přesahuje hranice zdrojového obrázku, vyvolá výjimku.  

## Často kladené otázky

**Q: Mohu ořezávat obrázky libovolného formátu pomocí Aspose.Drawing?**  
A: Ano, Aspose.Drawing podporuje širokou škálu formátů (PNG, JPEG, BMP, GIF, TIFF atd.), takže můžete ořezávat prakticky jakýkoli typ obrázku.

**Q: Existují pokročilé možnosti ořezu?**  
A: Rozhodně. Můžete kombinovat `GraphicsPath`, transformace `Matrix` nebo použít třídu `ImageProcessor` pro složitější výběry, jako jsou kruhové ořezy.

**Q: Mohu na jeden obrázek aplikovat více ořezových operací?**  
A: Ano. Po prvním ořezu můžete výsledek bitmapy použít jako nový zdroj a proces opakovat, čímž vytvoříte řetězec více ořezů.

**Q: Je Aspose.Drawing vhodný pro hromadné zpracování obrázků?**  
A: Ano. Jeho lehké API a absence nativních závislostí ho činí ideálním pro zpracování velkých kolekcí obrázků na serverech.

**Q: Jak mohu získat podporu pro dotazy související s Aspose.Drawing?**  
A: Navštivte [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44), kde můžete požádat o pomoc a spojit se s komunitou.

**Poslední aktualizace:** 2026-02-07  
**Testováno s:** Aspose.Drawing 24.11 pro .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}