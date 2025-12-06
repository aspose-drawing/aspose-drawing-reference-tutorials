---
date: 2025-12-06
description: Naučte se, jak ukládat soubory PNG, přičemž vypisujete nainstalovaná
  písma, zobrazujete rodiny písem, vytváříte grafiku z bitmapy a kreslíte text s písmy
  pomocí Aspose.Drawing pro .NET.
language: cs
linktitle: Save PNG Image and Work with Installed Fonts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Uložit PNG obrázek a pracovat s nainstalovanými fonty v Aspose.Drawing
url: /net/text-and-fonts/installed-fonts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Uložení PNG obrázku a práce s nainstalovanými fonty v Aspose.Drawing

## Úvod

Pokud potřebujete **uložit PNG obrázek**, který zároveň zobrazuje informace o fontech nainstalovaných v počítači, Aspose.Drawing pro .NET vám poskytuje čistý, multiplatformní způsob, jak to provést. V tomto tutoriálu projdeme výpis nainstalovaných fontů, zobrazení rodin fontů, vytvoření grafiky z bitmapy a kreslení textu s fonty – a nakonec výsledek uložíme jako PNG obrázek. Na konci budete mít znovupoužitelný úryvek, který můžete vložit do libovolného .NET projektu.

## Rychlé odpovědi
- **Co tento tutoriál vytvoří?** PNG obrázek, který vypisuje nainstalované rodiny fontů.  
- **Která knihovna je vyžadována?** Aspose.Drawing pro .NET (není potřeba System.Drawing.Common).  
- **Mohu použít vlastní fonty?** Ano – stačí je načíst do `InstalledFontCollection`.  
- **Je rozlišení výstupu nastavitelný?** Rozhodně – změňte velikost bitmapy nebo formát pixelů.  
- **Potřebuji licenci pro spuštění kódu?** Dočasná licence stačí pro hodnocení; pro produkci je vyžadována plná licence.

## Co znamená „uložit PNG obrázek“ v kontextu Aspose.Drawing?
Uložení PNG obrázku znamená vykreslení vašeho kreslicího povrchu (objektu `Bitmap`) do souboru s příponou `.png`. Aspose.Drawing se postará o kódování, takže stačí zavolat `bitmap.Save(...)` s požadovanou cestou.

## Proč vypisovat nainstalované fonty a zobrazovat rodiny fontů?
Znalost dostupných fontů vám umožní vytvářet dynamickou grafiku, která se přizpůsobí prostředí koncového uživatele. To je zvláště užitečné při generování reportů, certifikátů nebo jakéhokoli vizuálního obsahu, který musí odpovídat firemnímu brandingu bez nutnosti distribuovat soubory fontů.

## Předpoklady

- **Aspose.Drawing knihovna** – stáhněte si nejnovější verzi ze [stránky ke stažení Aspose Drawing](https://releases.aspose.com/drawing/net/).  
- **IDE** – Visual Studio, Rider nebo jakýkoli editor kompatibilní s .NET.  
- **Základní znalost C#** – měli byste být pohodlní s třídami, objekty a jednoduchými smyčkami.

## Import jmenných prostorů
Pro práci s fonty a grafikou importujte tyto jmenné prostory na začátku vašeho C# souboru:

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Průvodce krok za krokem

### Krok 1: Vytvoření bitmapy (plátna)
Nejprve vytvoříme bitmapu, která bude obsahovat finální obrázek. Velikost bitmapy a formát pixelů určují kvalitu uloženého PNG.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Krok 2: Vytvoření grafiky z bitmapy
Dále získáme objekt `Graphics` z bitmapy. Tento objekt nám umožní kreslit tvary, text a obrázky na plátno.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### Krok 3: Nastavení štětce a fontu (kreslení textu s fonty)
Potřebujeme štětec pro barvu textu a objekt `Font`, který definuje typ písma, velikost a styl.

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### Krok 4: Výpis nainstalovaných fontů a zobrazení rodin fontů
Nyní zobrazíme počet rodin fontů a několik prvních názvů přímo na bitmapě. Tím demonstrujeme schopnosti **list installed fonts** a **show font families**.

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

### Krok 5: Uložení PNG obrázku
Nakonec zapíšeme bitmapu na disk jako PNG soubor. Toto je jádro operace **save png image**.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

> **Tip:** Používejte `Path.Combine` pro sestavování cest k souborům, abyste se vyhnuli problémům s oddělovači adresářů na různých operačních systémech.

## Časté problémy a řešení
| Problém | Příčina | Řešení |
|---------|----------|--------|
| **Nezobrazují se žádné fonty** | `InstalledFontCollection` není naplněna (např. běh na serveru bez grafického rozhraní). | Nainstalujte požadované fonty na server nebo vložte vlastní fonty do aplikace. |
| **Uložený soubor je poškozený** | Nesprávný formát pixelů nebo chybějící oprávnění k zápisu. | Ujistěte se, že cílová složka existuje a aplikace má právo zapisovat; ponechte `Format32bppPArgb`. |
| **Text vypadá rozmazaně** | Nízké DPI nastavení. | Zvyšte rozměry bitmapy nebo nastavte `graphics.SmoothingMode = SmoothingMode.AntiAlias`. |

## Často kladené otázky

**Q: Mohu použít vlastní fonty, které nejsou nainstalované v systému?**  
A: Ano. Načtěte soubor fontu do `PrivateFontCollection` a vytvořte `Font` z této kolekce.

**Q: Jak zacházet s výjimkami souvisejícími s fonty?**  
A: Zabalte vytváření fontu do `try/catch` bloku a kontrolujte `ArgumentException` pro chybějící rodiny.

**Q: Je Aspose.Drawing vhodný pro webové aplikace?**  
A: Rozhodně. Knihovna funguje v ASP.NET Core, Azure Functions a dalších server‑side prostředích.

**Q: Můžu změnit barvu nebo styl textu?**  
A: Ano. Použijte různé typy `Brush` (např. `LinearGradientBrush`) a upravte výčtový typ `FontStyle`.

**Q: Kde získám dočasnou licenci pro testování?**  
A: Stáhněte si zkušební licenci ze [stránky dočasných licencí Aspose](https://purchase.aspose.com/temporary-license/).

## Závěr

Postupným sledováním těchto kroků jste se naučili, jak **uložit PNG obrázek**, který dynamicky **vypisuje nainstalované fonty**, **zobrazuje rodiny fontů**, **vytváří grafiku z bitmapy** a **kreslí text s fonty** pomocí Aspose.Drawing pro .NET. Nebojte se experimentovat s dalšími fonty, barvami a velikostmi bitmapy, aby výsledek odpovídal vizuálním požadavkům vašeho projektu.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Poslední aktualizace:** 2025-12-06  
**Testováno s:** Aspose.Drawing 24.11 pro .NET  
**Autor:** Aspose