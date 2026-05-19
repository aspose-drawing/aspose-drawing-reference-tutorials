---
date: 2026-05-19
description: Podrobný návod krok za krokem, jak hromadně oříznout obrázky do PNG pomocí
  Aspose.Drawing, alternativy k System.Drawing pro vývojáře .NET.
keywords:
- how to batch crop
- crop image to png
- alternative to system drawing
- batch image cropping .net
linktitle: Návod na ořezávání obrázků – Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Step‑by‑step tutorial on how to batch crop images to PNG using Aspose.Drawing,
    the alternative to System.Drawing for .NET developers.
  headline: How to Batch Crop Images to PNG Using Aspose.Drawing for .NET
  type: TechArticle
- description: Step‑by‑step tutorial on how to batch crop images to PNG using Aspose.Drawing,
    the alternative to System.Drawing for .NET developers.
  name: How to Batch Crop Images to PNG Using Aspose.Drawing for .NET
  steps:
  - name: Create a Bitmap Canvas
    text: '`Bitmap` is Aspose.Drawing''s in‑memory representation of an image, providing
      pixel‑level access and format control. We start with a blank canvas sized to
      hold the cropped result. Adjust the width and height to match the dimensions
      of the area you plan to extract.'
  - name: Create a Graphics Object
    text: '`Graphics` is the drawing surface that lets you render shapes, text, or
      other images onto a Bitmap. A `Graphics` object lets us draw onto the canvas.
      The `InterpolationMode` controls how pixel values are calculated during scaling
      or transformation—`NearestNeighbor` works well for sharp edges.'
  - name: Load the Image to Crop
    text: '`Image` (or `Bitmap`) loads the source file into memory, ready for manipulation.
      Load the source image. Make sure the path points to an existing file; otherwise
      an exception will be thrown.'
  - name: Define Source and Destination Rectangles
    text: '`Rectangle` objects describe the region of the source image to keep and
      where it should be placed on the destination canvas. The `sourceRectangle` tells
      the API which part of the original image to keep. Here we pick the top‑left
      50 × 40 pixel area. By assigning the same rectangle to `destinationRect'
  - name: Perform the Crop Operation
    text: '`Graphics.DrawImage` copies the defined portion of `image` onto our blank
      `bitmap`. `Graphics.DrawImage` copies the defined portion of `image` onto our
      blank `bitmap`. This is the core **crop image to PNG** operation.'
  - name: Save the Cropped Image (Crop Image to PNG)
    text: '`Bitmap.Save` writes the in‑memory bitmap to a file using the specified
      format. Finally, write the canvas to disk as a PNG file. PNG preserves any alpha
      channel and provides lossless quality—ideal for UI assets.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.Drawing supports a wide range of formats (PNG, JPEG, BMP,
      GIF, TIFF, etc.), so you can crop virtually any image type.
    question: Can I crop images of any format using Aspose.Drawing?
  - answer: Absolutely. You can combine `GraphicsPath`, `Matrix` transformations,
      or use the `ImageProcessor` class for more complex selections like circular
      crops.
    question: Are there advanced cropping options available?
  - answer: Yes. After the first crop, you can reuse the resulting bitmap as the new
      source and repeat the process to chain multiple crops.
    question: Can I apply multiple crop operations to a single image?
  - answer: Indeed. Its lightweight API and lack of native dependencies make it perfect
      for processing large image collections on servers.
    question: Is Aspose.Drawing suitable for batch image processing?
  - answer: Head over to the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      to seek assistance and connect with the community.
    question: How can I get support for Aspose.Drawing‑related queries?
  type: FAQPage
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
title: Jak hromadně oříznout obrázky do PNG pomocí Aspose.Drawing pro .NET
url: /cs/net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak hromadně oříznout obrázky do PNG pomocí Aspose.Drawing pro .NET

Pokud potřebujete **oříznout obrázek do PNG** rychle, spolehlivě a ve velkém měřítku v prostředí .NET, jste na správném místě. V tomto tutoriálu projdeme přesné kroky, jak načíst obrázek, definovat oblast ořezu a uložit výsledek jako soubor PNG – vše pomocí Aspose.Drawing, moderní **alternativy k System.Drawing**, která funguje napříč platformami. Také uvidíte, jak rozšířit tok pro jeden obrázek na kompletní **hromadný ořez**.

## Rychlé odpovědi
- **Jakou knihovnu mám použít?** Aspose.Drawing pro .NET (plnohodnotná alternativa k System.Drawing.Common)  
- **Jak dlouho trvá základní ořez?** Obvykle méně než sekunda pro jeden obrázek na moderním procesoru  
- **Mohu ořezávat do PNG?** Ano – uložte oříznutý bitmap jako soubor PNG (viz Krok 6)  
- **Potřebuji licenci?** Bezplatná zkušební verze funguje pro vývoj; pro produkci je vyžadována komerční licence  
- **Je možné hromadné zpracování?** Rozhodně – zabalte stejné kroky do smyčky pro zpracování více souborů  

## Jak hromadně oříznout obrázky do PNG?

Načtěte každý zdrojový soubor pomocí `new Bitmap(path)`, vytvořte odpovídající prázdný `Bitmap` pro oblast ořezu, nakreslete vybraný obdélník pomocí `Graphics.DrawImage` a nakonec zavolejte `Save("output.png", ImageFormat.Png)`. Zabalte těchto šest řádků do smyčky `foreach`, která prochází adresář, a získáte kompletní řešení hromadného ořezu, které během několika sekund zpracuje desítky obrázků.

## Proč použít Aspose.Drawing pro hromadné ořezávání?

Aspose.Drawing podporuje **3 hlavní operační systémy** (Windows, Linux, macOS) a dokáže zpracovat **obrázky s více než 500 pixely za méně než 0,5 sekundy** na typickém serverovém procesoru. Jeho API nevyžaduje nativní závislosti GDI+, což znamená, že můžete nasadit stejný kód do kontejnerů, Azure App Service nebo AWS Lambda bez dalších knihoven. Knihovna také nabízí **více než 50 formátů obrázků** a **plnou podporu alfa kanálu**, což ji činí ideální pro ořezávání transparentních PNG ve velkém měřítku.

## Co je „oříznout obrázek do PNG“?

Operace **oříznout obrázek do PNG** vyjme obdélníkovou oblast ze zdrojového bitmapu a zapíše tuto oblast do souboru PNG. PNG zachovává alfa kanál a poskytuje bezztrátovou kompresi, což dělá výsledný obrázek ideálním pro náhledy, ikony, UI assety nebo jakoukoli situaci, kde je vyžadována kvalita a transparentnost.

## Proč je Aspose.Drawing alternativou k System.Drawing?

Aspose.Drawing slouží jako drop‑in náhrada za System.Drawing a nabízí plnou multiplatformní kompatibilitu, čímž eliminuje potřebu nativních knihoven GDI+. Podporuje širokou škálu formátů pixelů, poskytuje vysoce výkonné manipulace s obrázky a zahrnuje pokročilé funkce jako zpracování alfa kanálu a rozsáhlou podporu formátů, což ji činí vhodnou jak pro jednoduché úpravy, tak pro rozsáhlé hromadné zpracování.

## Požadavky

Než začneme, ujistěte se, že máte:

- **Aspose.Drawing knihovnu** integrovánu do vašeho .NET projektu. Můžete si ji stáhnout [zde](https://releases.aspose.com/drawing/net/).  
- Složku, která obsahuje zdrojové obrázky, jež chcete oříznout. Nahraďte `"Your Document Directory"` v ukázkách kódu skutečnou cestou na vašem počítači.

## Importovat jmenné prostory

Jmenný prostor `System.Drawing` nám poskytuje přístup k `Bitmap`, `Graphics` a souvisejícím typům, které Aspose.Drawing rozšiřuje.

```csharp
using System.Drawing;
```

## Průvodce krok za krokem

### Krok 1: Vytvořit bitmapové plátno

`Bitmap` je v Aspose.Drawing interní reprezentace obrázku, která poskytuje přístup na úrovni pixelů a kontrolu formátu.  

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

Začínáme s prázdným plátnem, jehož velikost odpovídá oříznutému výsledku. Upravit šířku a výšku tak, aby odpovídaly rozměrům oblasti, kterou plánujete vyjmout.

### Krok 2: Vytvořit objekt Graphics

`Graphics` je kreslicí plocha, která vám umožní vykreslovat tvary, text nebo jiné obrázky na Bitmap.  

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

Objekt `Graphics` nám umožňuje kreslit na plátno. `InterpolationMode` určuje, jak jsou během škálování nebo transformace počítány hodnoty pixelů – `NearestNeighbor` funguje dobře pro ostré hrany.

### Krok 3: Načíst obrázek k oříznutí

`Image` (nebo `Bitmap`) načte zdrojový soubor do paměti a připraví jej k manipulaci.  

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

Načtěte zdrojový obrázek. Ujistěte se, že cesta ukazuje na existující soubor; jinak bude vyvolána výjimka.

### Krok 4: Definovat zdrojové a cílové obdélníky

Objekty `Rectangle` popisují oblast zdrojového obrázku, kterou chcete zachovat, a kam má být umístěna na cílovém plátně.  

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

`sourceRectangle` říká API, kterou část původního obrázku zachovat. Zde vybíráme levý horní obdélník o rozměrech 50 × 40 pixelů. Při přiřazení stejného obdélníku do `destinationRectangle` zachováme oříznutou oblast v její původní velikosti.

### Krok 5: Provedení operace oříznutí

`Graphics.DrawImage` kopíruje definovanou část `image` na náš prázdný `bitmap`.  

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

`Graphics.DrawImage` kopíruje definovanou část `image` na náš prázdný `bitmap`. Toto je jádro operace **oříznout obrázek do PNG**.

### Krok 6: Uložit oříznutý obrázek (oříznout obrázek do PNG)

`Bitmap.Save` zapíše bitmap v paměti do souboru ve zvoleném formátu.  

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

Nakonec zapíšeme plátno na disk jako soubor PNG. PNG zachovává alfa kanál a poskytuje bezztrátovou kvalitu – ideální pro UI assety.

## Jak hromadně oříznout obrázky ve smyčce?

Iterujte přes každou cestu k souboru pomocí `foreach (var file in Directory.GetFiles(sourceFolder, "*.png"))`, opakujte Kroky 1‑6 uvnitř smyčky a uložte každý výsledek do cílové složky. Tento vzor škáluje lineárně, může být paralelizován pomocí `Parallel.ForEach` pro ještě vyšší propustnost a efektivně a rychle zpracovává obrázky.

## Časté úskalí a tipy

- **Neshody formátů pixelů** – ujistěte se, že zdrojový obrázek a bitmap plátno mají kompatibilní formát pixelů, aby nedošlo k posunu barev.  
- **Uvolňování GDI objektů** – zabalte `Bitmap` a `Graphics` do `using` bloků nebo volajte `Dispose()` ručně; jinak můžete uniknout neřízeným prostředkům.  
- **Chyby souřadnic** – souřadnice obdélníku jsou nulové. Výběr obdélníku, který přesahuje hranice zdrojového obrázku, vyvolá výjimku.  

## Často kladené otázky

**Q: Mohu ořezávat obrázky libovolného formátu pomocí Aspose.Drawing?**  
A: Ano, Aspose.Drawing podporuje širokou škálu formátů (PNG, JPEG, BMP, GIF, TIFF atd.), takže můžete ořezávat prakticky jakýkoli typ obrázku.

**Q: Existují pokročilé možnosti ořezávání?**  
A: Rozhodně. Můžete kombinovat `GraphicsPath`, transformace `Matrix` nebo použít třídu `ImageProcessor` pro složitější výběry, například kruhové ořezy.

**Q: Můžu na jednom obrázku provést více ořezů?**  
A: Ano. Po prvním ořezu můžete výsledek použít jako nový zdroj a proces opakovat, čímž vytvoříte řetězec několika ořezů.

**Q: Je Aspose.Drawing vhodný pro hromadné zpracování obrázků?**  
A: Ano. Jeho lehké API a absence nativních závislostí ho činí perfektním pro zpracování velkých kolekcí obrázků na serverech.

**Q: Jak získat podporu pro dotazy související s Aspose.Drawing?**  
A: Navštivte [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44), kde můžete požádat o pomoc a spojit se s komunitou.

---

**Poslední aktualizace:** 2026-05-19  
**Testováno s:** Aspose.Drawing 24.11 pro .NET  
**Autor:** Aspose

## Související tutoriály

- [Jak oříznout obrázek do PNG pomocí Aspose.Drawing pro .NET](/drawing/net/image-editing/cropping/)
- [Jak škálovat obrázky s Aspose.Drawing pro .NET](/drawing/net/image-editing/scale/)
- [Převod BMP na PNG a další formáty s Aspose.Drawing](/drawing/net/image-editing/load-save/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}