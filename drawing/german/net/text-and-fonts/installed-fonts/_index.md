---
date: 2025-12-06
description: Erfahren Sie, wie Sie PNG‑Bilddateien speichern, installierte Schriftarten
  auflisten, Schriftfamilien anzeigen, Grafiken aus Bitmaps erstellen und Text mit
  Schriftarten mithilfe von Aspose.Drawing für .NET zeichnen.
language: de
linktitle: Save PNG Image and Work with Installed Fonts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: PNG‑Bild speichern und mit installierten Schriftarten in Aspose.Drawing arbeiten
url: /net/text-and-fonts/installed-fonts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PNG‑Bild speichern und mit installierten Schriften in Aspose.Drawing arbeiten

## Einführung

Wenn Sie **PNG‑Bilddateien** speichern müssen, die zudem Informationen über die auf einem Rechner installierten Schriften anzeigen, bietet Aspose.Drawing für .NET eine saubere, plattformübergreifende Möglichkeit dazu. In diesem Tutorial führen wir Sie durch das Auflisten installierter Schriften, das Anzeigen von Schriftfamilien, das Erstellen von Grafiken aus einem Bitmap und das Zeichnen von Text mit Schriften – und schließlich das Speichern des Ergebnisses als PNG‑Bild. Am Ende haben Sie einen wiederverwendbaren Code‑Snippet, den Sie in jedes .NET‑Projekt einbinden können.

## Schnellantworten
- **Was erstellt dieses Tutorial?** Ein PNG‑Bild, das installierte Schriftfamilien auflistet.  
- **Welche Bibliothek wird benötigt?** Aspose.Drawing für .NET (kein System.Drawing.Common nötig).  
- **Kann ich benutzerdefinierte Schriften verwenden?** Ja – laden Sie sie einfach in eine `InstalledFontCollection`.  
- **Ist die Auflösung des Outputs anpassbar?** Absolut – ändern Sie die Bitmap‑Größe oder das Pixel‑Format.  
- **Benötige ich eine Lizenz, um den Code auszuführen?** Eine temporäre Lizenz reicht für die Evaluierung; für die Produktion ist eine Voll‑Lizenz erforderlich.

## Was bedeutet „PNG‑Bild speichern“ im Kontext von Aspose.Drawing?
Ein PNG‑Bild zu speichern bedeutet, Ihre Zeichenfläche (ein `Bitmap`) in eine Datei mit der Endung `.png` zu rendern. Aspose.Drawing übernimmt die Kodierung für Sie, sodass Sie lediglich `bitmap.Save(...)` mit dem gewünschten Pfad aufrufen müssen.

## Warum installierte Schriften auflisten und Schriftfamilien anzeigen?
Zu wissen, welche Schriften verfügbar sind, ermöglicht es Ihnen, dynamische Grafiken zu erstellen, die sich an die Umgebung des End‑Benutzers anpassen. Das ist besonders praktisch für die Erstellung von Berichten, Zertifikaten oder jeglichem visuellen Inhalt, der zur Unternehmens‑Corporate‑Identity passen muss, ohne dass Schriftdateien mitgeliefert werden.

## Voraussetzungen

- **Aspose.Drawing‑Bibliothek** – laden Sie die neueste Version von der [Aspose Drawing‑Download‑Seite](https://releases.aspose.com/drawing/net/) herunter.  
- **IDE** – Visual Studio, Rider oder ein beliebiger .NET‑kompatibler Editor.  
- **Grundkenntnisse in C#** – Sie sollten mit Klassen, Objekten und einfachen Schleifen vertraut sein.

## Namespaces importieren
Um mit Schriften und Grafiken zu arbeiten, importieren Sie diese Namespaces am Anfang Ihrer C#‑Datei:

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Schritt‑für‑Schritt‑Anleitung

### Schritt 1: Bitmap erstellen (die Leinwand)
Zuerst erstellen wir ein Bitmap, das das endgültige Bild enthält. Die Bitmap‑Größe und das Pixel‑Format bestimmen die Qualität des gespeicherten PNG.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Schritt 2: Graphics aus dem Bitmap erzeugen
Als Nächstes erhalten wir ein `Graphics`‑Objekt aus dem Bitmap. Dieses Objekt ermöglicht das Zeichnen von Formen, Text und Bildern auf der Leinwand.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### Schritt 3: Pinsel und Schrift festlegen (Text mit Schriften zeichnen)
Wir benötigen einen Pinsel für die Textfarbe und ein `Font`‑Objekt, das Schriftart, Größe und Stil definiert.

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### Schritt 4: Installierte Schriften auflisten und Schriftfamilien anzeigen
Jetzt geben wir die Anzahl der Schriftfamilien und die ersten paar Namen direkt auf dem Bitmap aus. Das demonstriert die **installierten Schriften auflisten**‑ und **Schriftfamilien anzeigen**‑Funktionen.

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

### Schritt 5: PNG‑Bild speichern
Abschließend schreiben wir das Bitmap als PNG‑Datei auf die Festplatte. Das ist die Kern‑**PNG‑Bild speichern**‑Operation.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

> **Pro Tipp:** Verwenden Sie `Path.Combine`, um Dateipfade zu erstellen und Probleme mit Verzeichnis‑Trennzeichen auf verschiedenen Betriebssystemen zu vermeiden.

## Häufige Probleme und Lösungen
| Problem | Ursache | Lösung |
|-------|-------|-----|
| **Keine Schriften angezeigt** | `InstalledFontCollection` nicht gefüllt (z. B. auf einem headless Server ohne Schriften). | Installieren Sie die benötigten Schriften auf dem Server oder betten Sie benutzerdefinierte Schriften in Ihre Anwendung ein. |
| **Gespeicherte Datei ist beschädigt** | Falsches Pixel‑Format oder fehlende Schreibrechte. | Stellen Sie sicher, dass das Zielverzeichnis existiert und die Anwendung Schreibzugriff hat; behalten Sie `Format32bppPArgb` bei. |
| **Text wirkt unscharf** | Niedrige DPI‑Einstellungen. | Erhöhen Sie die Bitmap‑Abmessungen oder setzen Sie `graphics.SmoothingMode = SmoothingMode.AntiAlias`. |

## Häufig gestellte Fragen

**F: Kann ich benutzerdefinierte Schriften verwenden, die nicht auf dem Rechner installiert sind?**  
A: Ja. Laden Sie die Schriftdatei in eine `PrivateFontCollection` und erstellen Sie daraus ein `Font`.

**F: Wie gehe ich mit schriftenbezogenen Ausnahmen um?**  
A: Umgeben Sie die Schrifterstellung mit einem `try/catch`‑Block und prüfen Sie `ArgumentException` auf fehlende Familien.

**F: Ist Aspose.Drawing für Web‑Anwendungen geeignet?**  
A: Absolut. Die Bibliothek funktioniert in ASP.NET Core, Azure Functions und anderen serverseitigen Umgebungen.

**F: Kann ich die Textfarbe oder den Stil ändern?**  
A: Ja. Verwenden Sie verschiedene `Brush`‑Typen (z. B. `LinearGradientBrush`) und passen Sie das `FontStyle`‑Enum an.

**F: Wo bekomme ich eine temporäre Lizenz zum Testen?**  
A: Laden Sie eine Testlizenz von der [Aspose‑Temporär‑Lizenz‑Seite](https://purchase.aspose.com/temporary-license/) herunter.

## Fazit

Durch das Befolgen dieser Schritte haben Sie gelernt, wie Sie **PNG‑Bilddateien** speichern, die dynamisch **installierte Schriften auflisten**, **Schriftfamilien anzeigen**, **Grafiken aus einem Bitmap erstellen** und **Text mit Schriften zeichnen** – alles mit Aspose.Drawing für .NET. Experimentieren Sie gern mit anderen Schriften, Farben und Bitmap‑Größen, um die visuellen Anforderungen Ihres Projekts zu erfüllen.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Zuletzt aktualisiert:** 2025-12-06  
**Getestet mit:** Aspose.Drawing 24.11 für .NET  
**Autor:** Aspose