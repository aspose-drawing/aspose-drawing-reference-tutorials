---
date: 2026-02-27
description: Naučte se, jak vytvořit obrázek narozeninové karty pomocí Aspose.Drawing
  pro .NET. Tento průvodce vám ukáže, jak nakreslit text na obrázek, překrýt text
  na fotografii a rychle přidat titulek k fotografii.
linktitle: Adding Text on Images in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Jak vytvořit obrázek narozeninové karty pomocí Aspose.Drawing
url: /cs/net/use-cases/text-on-image/
weight: 12
---

Tested With:" -> "Testováno s:" (maybe "Testováno s:")

"Author:" -> "Autor:"

Now produce final content with all translations.

Be careful to keep code block placeholders unchanged.

Let's craft final answer.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak vytvořit obrázek narozeninové karty pomocí Aspose.Drawing

## Úvod
Ve dynamickém světě vývoje v .NET vyniká Aspose.Drawing jako výkonný nástroj pro snadnou manipulaci s obrázky. Ať už potřebujete **vytvořit obrázek narozeninové karty**, přidat vodoznak nebo jen překrýt textem obrázek, tento tutoriál vás provede přesnými kroky, jak pomocí C# **nakreslit řetězec na obrázek**. Na konci tohoto průvodce budete mít personalizovanou narozeninovou kartu připravenou ke sdílení.

## Rychlé odpovědi
- **Jakou knihovnu mám použít?** Aspose.Drawing for .NET  
- **Mohu přidat titulek k fotografii?** Yes – use `Graphics.DrawString` with custom fonts.  
- **Je pro produkci vyžadována licence?** Yes, a commercial license is needed.  
- **Jaké verze .NET jsou podporovány?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Jak dlouho trvá implementace?** Typically under 10 minutes for a simple card.

## Co je obrázek narozeninové karty?
Obrázek narozeninové karty je personalizovaná fotografie, která kombinuje pozadí s vlastním textem – například pozdrav, jméno příjemce nebo slavnostní zprávu. Pomocí Aspose.Drawing můžete tyto karty generovat programově bez ručních grafických nástrojů.

## Proč použít Aspose.Drawing k překrytí textu na obrázku?
- **Cross‑platform support:** Works on Windows, Linux, and macOS.  
- **Rich drawing API:** Full control over fonts, colors, and layout.  
- **No external dependencies:** Replaces `System.Drawing.Common` with a fully managed library.  
- **High performance:** Optimized for bulk image processing.

## Předpoklady
Předtím, než se ponoříte do tutoriálu, ujistěte se, že máte připraveno následující:

1. Aspose.Drawing Library: Download and install the Aspose.Drawing library from the [Aspose.Drawing for .NET documentation](https://reference.aspose.com/drawing/net/).  
2. Development Environment: A working .NET development environment, such as Visual Studio or Visual Studio Code, with .NET 6 SDK or later installed.

Nyní si projděte krok za krokem návod, jak přidat text k obrázku a uložit jej jako narozeninovou kartu.

## Importujte jmenné prostory
Začněte importováním potřebných jmenných prostorů do vašeho C# projektu:

```csharp
using System;
using System.Drawing;
using System.Drawing.Text;
using System.Linq;
```

## Krok 1: Načtení obrázku
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "UseCases", "girl.jpg")))
{
    var graphics = Graphics.FromImage(image);
    graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
    graphics.PageUnit = GraphicsUnit.Pixel;
```
Zde načteme obrázek ze zadané cesty k souboru a inicializujeme grafický objekt pro další zpracování.

## Krok 2: Nastavení vlastností textu
```csharp
SolidBrush brush = new SolidBrush(Color.Navy);
Font font = new Font("Calibri", 20, FontStyle.Italic);
int padding = 5;
```
Definujte vlastnosti textu, jako jsou barva, písmo a odsazení. Přizpůsobte tyto parametry podle svých designových preferencí.

## Krok 3: Změření velikosti textu
```csharp
string text = "Happy Birthday!";
var words = text.Split(' ');
int extentWidth = 0;
int extentHeight = 0;
words.ToList().ForEach(word =>
{
    var stringSize = graphics.MeasureString(word, font);
    extentWidth = Math.Max(extentWidth, (int)stringSize.Width + padding);
    extentHeight += (int)stringSize.Height;
});
```
Vypočítejte požadovanou velikost textu měřením každého slova jednotlivě. To zajišťuje správné umístění a zabraňuje překrývání textu.

## Krok 4: Nakreslení textu na obrázek
```csharp
Rectangle rectangle = new Rectangle(image.Width - padding - extentWidth, image.Height - padding - extentHeight, extentWidth, extentHeight);
graphics.DrawString(text, font, brush, rectangle);
```
Nyní umístěte text na obrázek na základě vypočtené velikosti a nakreslete jej pomocí zvoleného písma a barvy.

## Krok 5: Uložení obrázku
```csharp
image.Save(Path.Combine("Your Document Directory", "UseCases", "girl_card_out.jpg"));
}
```
Uložte upravený obrázek do požadovaného adresáře. Výsledný soubor je připravený k odeslání jako obrázek narozeninové karty.

## Běžné případy použití a tipy
- **Add caption to photo:** Replace `text` with any caption you need, such as “Celebrating 30 Years!”.  
- **Draw text on bitmap:** The same approach works for `Bitmap` objects created from scratch.  
- **Overlay multiple lines:** Loop through an array of strings and adjust the `Rectangle` Y‑coordinate for each line.  
- **Pro tip:** Use `Graphics.SmoothingMode = SmoothingMode.AntiAlias` for even smoother text rendering.

## Závěr
Aspose.Drawing zjednodušuje úlohy manipulace s obrázky v .NET a poskytuje vývojářům robustní sadu nástrojů. Přidání textu k obrázkům – ať už **vytvořit obrázek narozeninové karty**, **nakreslit řetězec na obrázek** nebo **přidat titulek k fotografii** – je jen jedním příkladem jeho všestrannosti při práci s grafickými prvky.

## Často kladené otázky
### Je Aspose.Drawing kompatibilní se všemi formáty obrázků?
Aspose.Drawing podporuje širokou škálu formátů obrázků, včetně populárních jako JPEG, PNG a GIF. Podívejte se do [documentation](https://reference.aspose.com/drawing/net/) pro kompletní seznam.

### Mohu použít Aspose.Drawing pro komerční projekty?
Ano, Aspose.Drawing je vhodný jak pro osobní, tak pro komerční projekty. Pro podrobnosti o licencování navštivte [purchase page](https://purchase.aspose.com/buy).

### Jsou k dispozici dočasné licence pro testovací účely?
Ano, můžete získat dočasnou licenci pro testování na stránce [Temporary License](https://purchase.aspose.com/temporary-license/).

### Kde mohu najít komunitní podporu pro Aspose.Drawing?
Zapojte se do komunity a získejte podporu na [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44).

### Jak začít s Aspose.Drawing?
Začněte stažením knihovny z [here](https://releases.aspose.com/drawing/net/) a prozkoumejte komplexní [documentation](https://reference.aspose.com/drawing/net/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Poslední aktualizace:** 2026-02-27  
**Testováno s:** Aspose.Drawing 24.11 for .NET  
**Autor:** Aspose  

---