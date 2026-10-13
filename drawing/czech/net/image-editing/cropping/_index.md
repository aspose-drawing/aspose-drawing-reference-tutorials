---
date: 2026-10-13
description: Naučte se, jak hromadně oříznout obrázky do PNG pomocí Aspose.Drawing
  API, multiplatformní alternativy k System.Drawing pro vývojáře .NET.
keywords:
- how to batch crop
- crop images to png
- batch image cropping
- convert images to png
- batch crop images
lastmod: 2026-10-13
linktitle: Tutoriál o ořezávání obrázků – Aspose.Drawing
og_description: Naučte se, jak rychle hromadně oříznout obrázky do PNG pomocí Aspose.Drawing,
  multiplatformní alternativy k System.Drawing pro vývojáře .NET. Postupujte podle
  krok‑za‑krokem návodu a efektivně zpracovávejte více souborů.
og_image_alt: 'Developer guide: batch crop images to PNG using Aspose.Drawing .NET
  API'
og_title: Jak hromadně oříznout obrázky do PNG s Aspose.Drawing pro .NET
schemas:
- author: Aspose
  dateModified: '2026-10-13'
  description: Learn how to batch crop images to PNG using the Aspose.Drawing API,
    the cross‑platform alternative to System.Drawing for .NET developers.
  headline: How to batch crop images to PNG using Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to batch crop images to PNG using the Aspose.Drawing API,
    the cross‑platform alternative to System.Drawing for .NET developers.
  name: How to batch crop images to PNG using Aspose.Drawing for .NET
  steps:
  - name: Create a bitmap canvas
    text: '`Bitmap` is Aspose.Drawing''s in‑memory representation of an image, providing
      pixel‑level access and format control. We start with a blank canvas sized to
      hold the cropped result. Adjust the width and height to match the dimensions
      of the area you plan to extract.'
  - name: Create a graphics object
    text: '`Graphics` is the drawing surface that lets you render shapes, text, or
      other images onto a Bitmap. A `Graphics` object lets us draw onto the canvas.
      The `InterpolationMode` controls how pixel values are calculated during scaling
      or transformation—`NearestNeighbor` works well for sharp edges.'
  - name: Load the image to crop
    text: '`Image` (or `Bitmap`) loads the source file into memory, ready for manipulation.
      Load the source image. Make sure the path points to an existing file; otherwise
      an exception will be thrown.'
  - name: Define source and destination rectangles
    text: '`Rectangle` objects describe the region of the source image to keep and
      where it should be placed on the destination canvas. The `sourceRectangle` tells
      the API which part of the original image to keep. Here we pick the top‑left
      50 × 40 pixel area. By assigning the same rectangle to `destinationRect'
  - name: Perform the crop operation
    text: '`Graphics.DrawImage` copies the defined portion of `image` onto our blank
      `bitmap`. This is the core **crop image to PNG** operation. The method respects
      the source rectangle and writes only the selected pixels to the destination
      bitmap.'
  - name: Save the cropped image (crop image to PNG)
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
tags:
- batch image cropping
- Aspose.Drawing
- .NET image processing
- PNG conversion
title: Jak hromadně oříznout obrázky do PNG pomocí Aspose.Drawing pro .NET
url: /cs/net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak hromadně oříznout obrázky do PNG pomocí Aspose.Drawing pro .NET

Pokud potřebujete **crop image to PNG** rychle, spolehlivě a ve velkém měřítku v .NET prostředí, jste na správném místě. V tomto tutoriálu projdeme přesné kroky načtení obrázku, definování oblasti ořezu a uložení výsledku jako soubor PNG – vše pomocí Aspose.Drawing, moderní **alternative to System.Drawing**, která funguje napříč platformami. Také uvidíte, jak rozšířit tok pro jeden obrázek do kompletní **batch crop** pipeline.

## Rychlé odpovědi
- **What library should I use?** Aspose.Drawing pro .NET (a full‑featured alternative to System.Drawing.Common)  
- **How long does the basic crop take?** Obvykle méně než sekunda pro jeden obrázek na moderním CPU  
- **Can I crop to PNG?** Ano – uložte oříznutý bitmap jako soubor PNG (viz Step 6)  
- **Do I need a license?** Bezplatná zkušební verze funguje pro vývoj; pro produkci je vyžadována komerční licence  
- **Is batch processing possible?** Rozhodně – zabalte stejné kroky do smyčky a zpracujte více souborů během několika sekund  

## Jak hromadně oříznout obrázky do PNG?

Načtěte každý zdrojový soubor pomocí `new Bitmap(path)`, vytvořte odpovídající prázdný `Bitmap` pro oblast ořezu, nakreslete vybraný obdélník pomocí `Graphics.DrawImage` a nakonec zavolejte `Save("output.png", ImageFormat.Png)`. Zabalte těchto šest řádků do `foreach` smyčky, která prochází adresář, a získáte kompletní řešení pro hromadný ořez, které během několika sekund zpracuje desítky obrázků.

## Proč použít Aspose.Drawing pro hromadný ořez?

Aspose.Drawing běží na **Windows, Linux a macOS**, zpracovává **obrázky s více než 500 pixely za méně než 0,5 sekundy** na typickém serverovém CPU a podporuje **více než 50 formátů obrázků** s úplnou zachováním alfa kanálu. Protože eliminuje nativní závislosti na GDI+, můžete nasadit stejný kód do kontejnerů, Azure App Service nebo AWS Lambda bez dalších knihoven, což jej činí ideálním pro velkorozměrné obrazové pipeline.

## Co je „crop image to PNG“?

Operace `crop image to PNG` extrahuje obdélníkovou oblast ze zdrojového bitmapu a zapíše tuto oblast do souboru PNG. PNG zachovává jakýkoli alfa kanál a poskytuje bezztrátovou kompresi, což dělá výsledný obrázek ideálním pro miniatury, ikony, UI assety nebo jakoukoli situaci, kde je vyžadována kvalita a průhlednost.

## Proč je Aspose.Drawing alternativou k System.Drawing?

Aspose.Drawing slouží jako drop‑in náhrada za System.Drawing tím, že nabízí plnou multiplatformní kompatibilitu a eliminuje potřebu nativních knihoven GDI+. Podporuje širokou škálu pixelových formátů, poskytuje vysoce výkonnou manipulaci s obrázky a zahrnuje pokročilé funkce, jako je zpracování alfa kanálu a rozsáhlá podpora formátů, což jej činí vhodným jak pro jednoduché úpravy, tak pro velkorozměrné hromadné zpracování.

## Požadavky

Předtím, než se pustíme do detailů, ujistěte se, že máte:

- **Aspose.Drawing library** integrovaná do vašeho .NET projektu. Můžete si ji stáhnout ze [Aspose.Drawing download page](https://releases.aspose.com/drawing/net/).  
- Složka, která obsahuje zdrojové obrázky, které chcete oříznout. Nahraďte `"Your Document Directory"` v ukázkách kódu skutečnou cestou na vašem počítači.

## Importovat jmenné prostory

Jmenný prostor `System.Drawing` nám poskytuje přístup k `Bitmap`, `Graphics` a souvisejícím typům, které Aspose.Drawing rozšiřuje.

```csharp
using System.Drawing;
```

## Průvodce krok za krokem

### Krok 1: Vytvořit bitmapové plátno

`Bitmap` je v‑paměti reprezentace obrázku v Aspose.Drawing, poskytující přístup na úrovni pixelů a kontrolu formátu.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

Začínáme s prázdným plátnem o rozměrech, které pojmou oříznutý výsledek. Upravit šířku a výšku tak, aby odpovídaly rozměrům oblasti, kterou chcete extrahovat.

### Krok 2: Vytvořit objekt Graphics

`Graphics` je kreslicí plocha, která vám umožňuje vykreslovat tvary, text nebo jiné obrázky na Bitmapu.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

Objekt `Graphics` nám umožňuje kreslit na plátno. `InterpolationMode` řídí, jak jsou během škálování nebo transformace počítány hodnoty pixelů – `NearestNeighbor` funguje dobře pro ostré hrany.

### Krok 3: Načíst obrázek k ořezu

`Image` (nebo `Bitmap`) načte zdrojový soubor do paměti, připravený k manipulaci.

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

Načtěte zdrojový obrázek. Ujistěte se, že cesta ukazuje na existující soubor; jinak bude vyhozena výjimka.

### Krok 4: Definovat zdrojové a cílové obdélníky

Objekty `Rectangle` popisují oblast zdrojového obrázku, která se má zachovat, a kam má být umístěna na cílovém plátně.

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

`sourceRectangle` říká API, kterou část původního obrázku zachovat. Zde vybíráme oblast 50 × 40 pixelů v levém horním rohu. Přiřazením stejného obdélníku do `destinationRectangle` zachováme oříznutou oblast v její původní velikosti.

### Krok 5: Provedení operace ořezu

`Graphics.DrawImage` kopíruje definovanou část `image` na naše prázdné `bitmap`.

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

Toto je jádro operace **crop image to PNG**. Metoda respektuje zdrojový obdélník a zapíše pouze vybrané pixely do cílového bitmapu.

### Krok 6: Uložit oříznutý obrázek (crop image to PNG)

`Bitmap.Save` zapíše bitmap v paměti do souboru pomocí zadaného formátu.

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

Nakonec zapíšete plátno na disk jako soubor PNG. PNG zachovává jakýkoli alfa kanál a poskytuje bezztrátovou kvalitu – ideální pro UI assety.

## Jak hromadně oříznout obrázky ve smyčce?

Iterujte přes každou cestu k souboru pomocí `foreach (var file in Directory.GetFiles(sourceFolder, "*.png"))`, opakujte Kroky 1‑6 uvnitř smyčky a uložte každý výsledek do cílové složky. Tento vzor škáluje lineárně, lze jej paralelizovat pomocí `Parallel.ForEach` pro ještě vyšší propustnost a zpracovává obrázky efektivně a rychle.

## Časté úskalí a tipy

- **Pixel format mismatches** – ujistěte se, že zdrojový obrázek a bitmap plátna mají kompatibilní pixelový formát, aby nedošlo k posunu barev.  
- **Disposal of GDI objects** – zabalte `Bitmap` a `Graphics` do `using` bloků nebo zavolejte `Dispose()` ručně; jinak můžete uniknout neřízené prostředky.  
- **Coordinate errors** – souřadnice obdélníku jsou nulové. Výběr obdélníku, který přesahuje hranice zdrojového obrázku, vyvolá výjimku.  

## Často kladené otázky

**Q: Can I crop images of any format using Aspose.Drawing?**  
A: Ano, Aspose.Drawing podporuje širokou škálu formátů (PNG, JPEG, BMP, GIF, TIFF atd.), takže můžete oříznout prakticky jakýkoli typ obrázku.

**Q: Are there advanced cropping options available?**  
A: Rozhodně. Můžete kombinovat `GraphicsPath`, transformace `Matrix` nebo použít třídu `ImageProcessor` pro složitější výběry, jako jsou kruhové ořezy.

**Q: Can I apply multiple crop operations to a single image?**  
A: Ano. Po prvním ořezu můžete výsledek bitmapy použít jako nový zdroj a opakovat proces pro řetězení více ořezů.

**Q: Is Aspose.Drawing suitable for batch image processing?**  
A: Ano. Jeho lehké API a absence nativních závislostí jej činí ideálním pro zpracování velkých kolekcí obrázků na serverech.

**Q: How can I get support for Aspose.Drawing‑related queries?**  
A: Navštivte [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44), kde můžete požádat o pomoc a spojit se s komunitou.

---

**Poslední aktualizace:** 2026-10-13  
**Testováno s:** Aspose.Drawing 24.11 for .NET  
**Autor:** Aspose

## Související tutoriály

- [Načíst, převést BMP na PNG a další formáty pomocí Aspose.Drawing](/drawing/net/image-editing/load-save/)
- [Jak licencovat Aspose.Drawing pro .NET – jak licencovat aspose.drawing](/drawing/net/licensing/)
- [Jak nakreslit obdélník – Transformace souřadnicového systému (transformace stránky) pomocí Aspose.Drawing API pro .NET](/drawing/net/coordinate-transformations/page-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}