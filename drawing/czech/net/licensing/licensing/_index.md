---
date: 2026-02-09
description: Naučte se, jak nastavit licenci Aspose.Drawing v .NET. Ovládněte metody
  licencování a odemkněte všechny funkce bez vodoznaků.
linktitle: Licensing in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Nastavení licence Aspose.Drawing – Jak nastavit licenci Aspose.Drawing
url: /cs/net/licensing/licensing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Nastavení licence Aspose.Drawing

## Úvod

Pokud vytváříte .NET aplikace, které spoléhají na výkonnou grafiku a manipulaci s obrázky, **nastavení licence Aspose.Drawing** je první krok k odstranění omezení hodnocení a získání plného souboru funkcí. V tomto tutoriálu se naučíte tři praktické způsoby, jak nastavit licenci Aspose.Drawing — načtení ze souboru, načtení ze streamu a použití modelu měřeného využití — abyste mohli knihovnu integrovat s jistotou.

## Rychlé odpovědi
- **Jaký je hlavní způsob aktivace Aspose.Drawing?** Načtěte licenční soubor pomocí `License.SetLicense("Aspose.Drawing.lic")`.  
- **Mohu licenci použít za běhu?** Ano, můžete načíst licenci ze `Stream` pro dynamické scénáře.  
- **Je podporována měřená licence?** Ano; použijte `Metered.SetMeteredKey(publicKey, privateKey)` k povolení fakturace založené na spotřebě.  
- **Potřebuji licenci pro vývojové sestavení?** Zkušební verze funguje pro testování, ale platná licence odstraňuje vodoznaky a odemyká všechna API.  
- **Které verze .NET jsou kompatibilní?** Aspose.Drawing podporuje .NET Framework 4.x, .NET Core 3.1+ a .NET 5/6+.

## Požadavky

Před začátkem se ujistěte, že máte:

- **Knihovna Aspose.Drawing** – stáhněte nejnovější balíček z [zde](https://releases.aspose.com/drawing/net/).  
- **Licenční soubor** – získejte platný soubor `.lic` od [Aspose](https://purchase.aspose.com/buy).  
- **Vývojové prostředí .NET** – Visual Studio, Rider nebo jakékoli IDE cílící na .NET Framework/.NET Core.

## Importování jmenných prostorů

Potřebujeme standardní .NET jmenné prostory plus jmenný prostor Aspose.Drawing pro licencování. Přidejte následující `using` direktivy na začátek vašeho C# souboru:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
```

## Načtení licence ze souboru

Načtení licence ze souboru je nejužitečnější přístup. Postupujte podle těchto tří kroků:

### Krok 1: Inicializace objektu licence

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

### Krok 2: Nastavení licence ze souboru `.lic`

```csharp
license.SetLicense("Aspose.Drawing.lic");
```

### Krok 3: Ověření úspěchu

```csharp
Console.WriteLine("License set successfully.");
```

> **Tip:** Umístěte soubor `.lic` do stejné složky jako váš spustitelný soubor nebo zadejte absolutní cestu, aby se předešlo chybám „soubor nenalezen“.

## Načtení licence ze streamu

Když je váš licenční soubor vložen jako zdroj nebo získán ze vzdáleného umístění, načtení ze `Stream` vám poskytuje flexibilitu.

### Krok 1: Inicializace objektu licence

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

### Krok 2: Načtení licence pomocí `FileStream`

```csharp
FileStream myStream = new FileStream("Aspose.Drawing.lic", FileMode.Open);
license.SetLicense(myStream);
```

### Krok 3: Ověření úspěchu

```csharp
Console.WriteLine("License set successfully.");
```

> **Varování:** Nezapomeňte uvolnit `FileStream` (nebo použít blok `using`) pro uvolnění souborových handle.

## Použití měřené licence

Měřené licencování je ideální pro SaaS nebo modely platby za použití. Sleduje spotřebu a fakturuje vás na základě skutečného využití.

### Krok 1: Inicializace objektu Metered

```csharp
System.Drawing.AsposeDrawing.Metered metered = new System.Drawing.AsposeDrawing.Metered();
```

### Krok 2: Nastavení veřejného a soukromého klíče

```csharp
metered.SetMeteredKey("your_public_key", "your_private_key");
```

### Krok 3: Proveďte zpracování obrázků

```csharp
// Your image processing logic here
```

### Krok 4: Získání informací o spotřebě

```csharp
decimal amount = System.Drawing.AsposeDrawing.Metered.GetConsumptionQuantity();
decimal credits = System.Drawing.AsposeDrawing.Metered.GetConsumptionCredit();
```

### Krok 5: Zobrazení podrobností o spotřebě

```csharp
Console.WriteLine("Amount Consumed: " + amount.ToString());
Console.WriteLine("Credits Consumed: " + credits.ToString());
```

> **Častý úskalí:** Pokud zapomenete zavolat `SetMeteredKey`, API přejde do zkušebního režimu a ve výstupu uvidíte vodoznaky.

## Proč nastavit licenci Aspose.Drawing správně?

- **Odstraňuje vodoznaky**, které se objevují v zkušebním režimu.  
- **Odemkne prémiová API**, jako jsou pokročilé filtry obrázků a konverze do PDF.  
- **Zajišťuje soulad** s licenčními podmínkami Aspose pro komerční distribuci.  
- **Umožňuje měřené fakturování**, takže platíte jen za to, co používáte.

## Časté problémy a řešení

| Problém | Příčina | Řešení |
|-------|-------|-----|
| Chyba „License file not found“ | Špatná cesta nebo chybějící soubor ve výstupní složce | Použijte absolutní cestu nebo nastavte vlastnost souboru *Copy to Output Directory* na *Copy always*. |
| Vodoznak se stále zobrazuje po nastavení licence | Licence nebyla načtena před prvním voláním API | Načtěte licenci **před** jakoukoli operací Aspose.Drawing. |
| Měřená spotřeba je vždy nula | Klíče nejsou nastaveny nebo jsou špatné proměnné prostředí | Ověřte veřejné/soukromé klíče a zajistěte internetové připojení k měřenému serveru Aspose. |

## Často kladené otázky

**Q1: Mohu používat Aspose.Drawing bez licence?**  
A1: Ano, zkušební licence funguje pro vývoj a hodnocení, ale přidává vodoznaky a omezuje některé funkce.

**Q2: Jak často musím obnovovat licenci Aspose.Drawing?**  
A2: Licence jsou trvalé pro zakoupenou verzi. Obnova je vyžadována pouze pro podporu a aktualizace.

**Q3: Co je měřené licencování a kdy jej použít?**  
A3: Měřené licencování účtuje na základě využití (operace nebo zpracovaná data). Je ideální pro cloudové služby nebo modely platby za použití.

**Q4: Mohu používat Aspose.Drawing v komerčních projektech?**  
A4: Rozhodně — jakmile máte platnou licenci, můžete Aspose.Drawing vložit do jakékoli komerční aplikace.

**Q5: Kde mohu najít komunitní podporu pro Aspose.Drawing?**  
A5: Navštivte [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) pro komunitní pomoc, příklady a diskuze.

## Závěr

Ovládnutí **nastavení licence Aspose.Drawing** — ať už ze souboru, ze streamu nebo pomocí měřeného využití — zajistí, že získáte maximum z této výkonné .NET grafické knihovny. Postupujte podle výše uvedených kroků, dávejte pozor na časté úskalí a budete připraveni vytvářet robustní řešení pro zpracování obrázků bez jakýchkoli licenčních překážek.

---

**Poslední aktualizace:** 2026-02-09  
**Testováno s:** Aspose.Drawing 24.11 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}