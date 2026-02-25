---
date: 2026-02-25
description: Erfahren Sie, wie Sie Bitmap‑Grafiken in C# erstellen und PNG‑Bilder
  speichern, dabei installierte Schriftarten auflisten, Text mit Schriftarten zeichnen
  und die Bitmap‑Auflösung mit Aspose.Drawing für .NET anpassen.
linktitle: Create Bitmap Graphics C# – Save PNG Image and Work with Installed Fonts
  in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Bitmap-Grafiken in C# erstellen – PNG-Bild speichern und mit installierten
  Schriftarten in Aspose.Drawing arbeiten
url: /de/net/text-and-fonts/installed-fonts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PNG‑Bild speichern und mit installierten Schriftarten in Aspose.Drawing arbeiten

## Einleitung

Wenn Sie **PNG‑Bilder speichern** müssen und gleichzeitig **Bitmap‑Grafiken in C# erstellen** möchten, bietet Aspose.Drawing für .NET eine saubere, plattformübergreifende Möglichkeit, dies zu tun. In diesem Tutorial führen wir Sie durch das Auflisten installierter Schriftarten, das Anzeigen von Schriftfamilien, das Erstellen von Grafiken aus einem Bitmap und das Zeichnen von Text mit Schriftarten – und schließlich das Speichern des Ergebnisses als PNG‑Bild. Am Ende haben Sie ein wiederverwendbares Snippet, das Sie in jedes .NET‑Projekt einbinden können.

## Schnellantworten
- **Was erstellt dieses Tutorial?** Ein PNG‑Bild, das installierte Schriftfamilien auflistet.  
- **Welche Bibliothek wird benötigt?** Aspose.Drawing für .NET (kein System.Drawing.Common erforderlich).  
- **Kann ich benutzerdefinierte Schriftarten verwenden?** Ja – laden Sie sie einfach in eine `InstalledFontCollection`.  
- **Ist die Ausgaberesolution anpassbar?** Absolut – ändern Sie die Bitmap‑Größe oder das Pixel‑Format, um **adjust bitmap resolution C#** style.  
- **Benötige ich eine Lizenz, um den Code auszuführen?** Eine temporäre Lizenz funktioniert für die Evaluierung; für die Produktion ist eine Voll‑Lizenz erforderlich.

## Was bedeutet „save PNG image“ im Kontext von Aspose.Drawing?

Ein PNG‑Bild zu speichern bedeutet, Ihre Zeichenfläche (ein `Bitmap`) in eine Datei mit der Erweiterung `.png` zu rendern. Aspose.Drawing übernimmt die Kodierung für Sie, sodass Sie lediglich `bitmap.Save(...)` mit dem gewünschten Pfad aufrufen müssen.

## Warum installierte Schriftarten auflisten und Schriftfamilien anzeigen?

Zu wissen, welche Schriftarten verfügbar sind, ermöglicht es Ihnen, dynamische Grafiken zu erstellen, die sich an die Umgebung des Endbenutzers anpassen. Das ist besonders praktisch für die Erstellung von Berichten, Zertifikaten oder jeglichen visuellen Inhalten, die dem Corporate Branding entsprechen müssen, ohne Schriftdateien mitzuliefern.

## Wie erstellt man Bitmap‑Grafiken in C# mit Aspose.Drawing?

Im Folgenden finden Sie eine praktische Schritt‑für‑Schritt‑Anleitung, die genau zeigt, wie man **Bitmap‑Grafiken in C# erstellt**, Text mit Schriftarten zeichnet und bei Bedarf die Bitmap‑Auflösung anpasst.

## Voraussetzungen

- **Aspose.Drawing Library** – Laden Sie die neueste Version von der [Aspose Drawing Download-Seite](https://releases.aspose.com/drawing/net/) herunter.  
- **IDE** – Visual Studio, Rider oder ein beliebiger .NET‑kompatibler Editor.  
- **Basic C# knowledge** – Sie sollten mit Klassen, Objekten und einfachen Schleifen vertraut sein.

## Namespaces importieren
Um mit Schriftarten und Grafiken zu arbeiten, importieren Sie diese Namespaces am Anfang Ihrer C#‑Datei:

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Schritt‑für‑Schritt‑Anleitung

### Schritt 1: Bitmap erstellen (die Leinwand)
Zuerst erstellen wir ein Bitmap, das das endgültige Bild enthält. Die Bitmap‑Größe und das Pixel‑Format bestimmen die Qualität des gespeicherten PNG und ermöglichen es Ihnen, **adjust bitmap resolution C#** im Stil anzupassen.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Schritt 2: Grafik aus dem Bitmap erstellen
Als Nächstes erhalten wir ein `Graphics`‑Objekt aus dem Bitmap. Dieses Objekt ermöglicht es uns, Formen, Text und Bilder auf die Leinwand zu zeichnen.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### Schritt 3: Pinsel und Schriftart einrichten (Text mit Schriftarten zeichnen)
Wir benötigen einen Pinsel für die Textfarbe und ein `Font`‑Objekt, das die Schriftart, Größe und den Stil definiert. Hier kommt das **draw text with fonts** zum Einsatz.

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### Schritt 4: Installierte Schriftarten auflisten und Schriftfamilien anzeigen
Jetzt zeigen wir die Anzahl der Schriftfamilien und die ersten paar Namen direkt auf dem Bitmap an. Dies demonstriert die **list installed fonts**‑ und **show font families**‑Funktionen.

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

### Schritt 5: PNG‑Bild speichern
Abschließend schreiben wir das Bitmap als PNG‑Datei auf die Festplatte. Dies ist die Kernoperation **save png image**.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

> **Pro tip:** Verwenden Sie `Path.Combine` zum Erstellen von Dateipfaden, um Probleme mit Verzeichnis­trennzeichen auf verschiedenen Betriebssystemen zu vermeiden.

## Häufige Probleme und Lösungen
| Problem | Ursache | Lösung |
|-------|-------|-----|
| **No fonts displayed** | `InstalledFontCollection` not populated (e.g., running on a headless server without fonts). | Installieren Sie die erforderlichen Schriftarten auf dem Server oder betten Sie benutzerdefinierte Schriftarten in Ihre Anwendung ein. |
| **Saved file is corrupted** | Incorrect pixel format or missing write permissions. | Stellen Sie sicher, dass das Zielverzeichnis existiert und die Anwendung Schreibrechte hat; behalten Sie `Format32bppPArgb`. |
| **Text looks blurry** | Low DPI settings. | Erhöhen Sie die Bitmap‑Abmessungen oder setzen Sie `graphics.SmoothingMode = SmoothingMode.AntiAlias`. |

## Häufig gestellte Fragen

**Q: Kann ich benutzerdefinierte Schriftarten verwenden, die nicht auf dem Rechner installiert sind?**  
A: Ja. Laden Sie die Schriftdatei in eine `PrivateFontCollection` und erstellen Sie ein `Font` aus dieser Sammlung.

**Q: Wie gehe ich mit font‑bezogenen Ausnahmen um?**  
A: Wickeln Sie die Schriftart-Erstellung in einen `try/catch`‑Block und prüfen Sie `ArgumentException` auf fehlende Familien.

**Q: Ist Aspose.Drawing für Webanwendungen geeignet?**  
A: Absolut. Die Bibliothek funktioniert in ASP.NET Core, Azure Functions und anderen serverseitigen Umgebungen.

**Q: Kann ich die Textfarbe oder den Stil ändern?**  
A: Ja. Verwenden Sie verschiedene `Brush`‑Typen (z. B. `LinearGradientBrush`) und ändern Sie das `FontStyle`‑Enum.

**Q: Wo kann ich eine temporäre Lizenz für Tests erhalten?**  
A: Laden Sie eine Testlizenz von der [Aspose Temporär‑Lizenz‑Seite](https://purchase.aspose.com/temporary-license/) herunter.

## Fazit

Durch das Befolgen dieser Schritte haben Sie gelernt, wie man **PNG‑Bilder speichert**, die dynamisch **installierte Schriftarten auflisten**, **Schriftfamilien anzeigen**, **Grafiken aus einem Bitmap erstellen** und **Text mit Schriftarten zeichnen** mit Aspose.Drawing für .NET. Sie wissen jetzt, wie man **Bitmap‑Grafiken in C# erstellt**, die Bitmap‑Auflösung anpasst und bei Bedarf benutzerdefinierte Schriftarten einbindet. Experimentieren Sie gern mit anderen Schriftarten, Farben und Bitmap‑Größen, um die visuellen Anforderungen Ihres Projekts zu erfüllen.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Zuletzt aktualisiert:** 2026-02-25  
**Getestet mit:** Aspose.Drawing 24.11 für .NET  
**Autor:** Aspose