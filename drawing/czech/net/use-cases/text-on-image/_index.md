---
title: Přidání textu na obrázky v Aspose.Drawing
linktitle: Přidání textu na obrázky v Aspose.Drawing
second_title: Aspose.Drawing .NET API – alternativa k System.Drawing.Common
description: Prozkoumejte bezproblémovou integraci textu do obrázků s Aspose.Drawing for .NET. Postupujte podle našeho podrobného průvodce pro snadnou manipulaci s obrázky. Stáhnout teď!
weight: 12
url: /cs/net/use-cases/text-on-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Přidání textu na obrázky v Aspose.Drawing

## Úvod
dynamickém světě vývoje .NET vyniká Aspose.Drawing jako výkonný nástroj pro snadnou manipulaci s obrázky. Přidávání textu k obrázkům je běžným požadavkem, ať už jde o vodoznak, anotace nebo vytváření personalizované grafiky. V tomto tutoriálu prozkoumáme, jak využít Aspose.Drawing k bezproblémové integraci textu do vašich obrázků pomocí C#.
## Předpoklady
Než se pustíte do výukového programu, ujistěte se, že máte na místě následující:
1.  Aspose.Drawing Library: Stáhněte si a nainstalujte knihovnu Aspose.Drawing z[Aspose.Drawing pro dokumentaci .NET](https://reference.aspose.com/drawing/net/).
2. Vývojové prostředí: Mějte funkční vývojové prostředí .NET, včetně sady Visual Studio nebo jakéhokoli jiného kompatibilního IDE.
Nyní začneme s průvodcem krok za krokem.
## Importovat jmenné prostory
Začněte importováním potřebných jmenných prostorů do vašeho projektu C#:
```csharp
using System;
using System.Drawing;
using System.Drawing.Text;
using System.Linq;
```
## Krok 1: Načtěte obrázek
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "UseCases", "girl.jpg")))
{
    var graphics = Graphics.FromImage(image);
    graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
    graphics.PageUnit = GraphicsUnit.Pixel;
```
Zde načteme obrázek ze zadané cesty k souboru a inicializujeme grafický objekt pro další zpracování.
## Krok 2: Nastavte vlastnosti textu
```csharp
SolidBrush brush = new SolidBrush(Color.Navy);
Font font = new Font("Calibri", 20, FontStyle.Italic);
int padding = 5;
```
Definujte vlastnosti textu, jako je barva, písmo a odsazení. Upravte tyto parametry podle svých preferencí.
## Krok 3: Změřte velikost textu
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
Vypočítejte požadovanou velikost textu měřením každého slova jednotlivě. To zajistí správné umístění a zabrání překrývání textu.
## Krok 4: Nakreslete text na obrázek
```csharp
Rectangle rectangle = new Rectangle(image.Width - padding - extentWidth, image.Height - padding - extentHeight, extentWidth, extentHeight);
graphics.DrawString(text, font, brush, rectangle);
```
Nyní umístěte text na obrázek na základě vypočítané velikosti a nakreslete jej pomocí určeného písma a barvy.
## Krok 5: Uložte obrázek
```csharp
image.Save(Path.Combine("Your Document Directory", "UseCases", "girl_card_out.jpg"));
}
```
Uložte upravený obrázek do požadovaného adresáře.
Tento podrobný průvodce demonstruje přímočarý proces přidávání textu do obrázků pomocí Aspose.Drawing for .NET. Experimentujte s různými fonty, barvami a textovým obsahem, abyste dosáhli požadovaného vizuálního efektu.
## Závěr
Aspose.Drawing zjednodušuje úlohy manipulace s obrázky v .NET a poskytuje vývojářům robustní sadu nástrojů. Přidávání textu k obrázkům je jen jedním příkladem jejích schopností, který ukazuje všestrannost knihovny při manipulaci s grafickými prvky.
## Často kladené otázky
### Je Aspose.Drawing kompatibilní se všemi formáty obrázků?
 Aspose.Drawing podporuje širokou škálu obrazových formátů, včetně populárních jako JPEG, PNG a GIF. Odkazovat na[dokumentace](https://reference.aspose.com/drawing/net/) pro úplný seznam.
### Mohu použít Aspose.Drawing pro komerční projekty?
Ano, Aspose.Drawing je vhodný pro osobní i komerční projekty. Podrobnosti o licencích naleznete na[nákupní stránku](https://purchase.aspose.com/buy).
### Jsou dočasné licence dostupné pro testovací účely?
 Ano, dočasnou licenci pro testování můžete získat návštěvou[Dočasná licence](https://purchase.aspose.com/temporary-license/).
### Kde najdu podporu komunity pro Aspose.Drawing?
 Zapojte se do komunity a získejte podporu na[Aspose. Kreslící fórum](https://forum.aspose.com/c/drawing/44).
### Jak mohu začít s Aspose.Drawing?
 Začněte stažením knihovny z[tady](https://releases.aspose.com/drawing/net/) a prozkoumat komplexní[dokumentace](https://reference.aspose.com/drawing/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
