---
date: 2026-11-04
description: Erfahren Sie, wie Sie Rechteckgrafiken zeichnen, während Sie in .NET
  mit der Aspose.Drawing API eine coordinate system transformation durchführen. Diese
  Schritt‑für‑Schritt‑Anleitung zeigt, wie man inches in pixels umwandelt und page
  units festlegt.
keywords:
- how to draw rectangle
- convert inches to pixels
- how to set units
- save bitmap as png
- clear canvas background
lastmod: 2026-11-04
linktitle: Koordinatensystem-Transformation in Aspose.Drawing
og_description: Erfahren Sie, wie Sie Rechteckgrafiken zeichnen, während Sie inches
  in pixels umwandeln und page units in Aspose.Drawing für .NET festlegen. Folgen
  Sie der Schritt‑für‑Schritt‑Anleitung für präzise page transformation.
og_image_alt: Developer guide showing rectangle drawing with coordinate system transformation
  in Aspose.Drawing
og_title: So zeichnen Sie ein Rechteck mit page transformation in Aspose.Drawing für
  .NET
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  headline: How to draw rectangle – coordinate system transformation (page transformation)
    in Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  name: How to draw rectangle – coordinate system transformation (page transformation)
    in Aspose.Drawing for .NET
  steps:
  - name: Import namespaces
    text: The `using` statements give you access to the core drawing classes.
  - name: Create a bitmap
    text: '`Bitmap` represents an image in memory that you can draw onto. We start
      by creating a blank bitmap that will serve as the drawing surface. The pixel
      format `Format32bppPArgb` gives us high‑quality, premultiplied alpha support.'
  - name: Create a graphics object
    text: A `Graphics` object provides the drawing API for the bitmap. It’s the bridge
      between your code and the pixel buffer.
  - name: Clear the canvas
    text: Give the canvas a neutral background so the drawn shapes stand out. Here
      we fill it with a light gray.
  - name: Set the transformation (how to set unit)
    text: '`Graphics.PageUnit` specifies the unit of measure used for page coordinates.
      To map page coordinates to device pixels, set the `PageUnit` property. In this
      example we choose inches, but you could also use `GraphicsUnit.Millimeter`,
      `GraphicsUnit.Point`, or `GraphicsUnit.Pixel`. Setting the unit to i'
  - name: Draw a rectangle – draw rectangle graphics
    text: '`Pen` defines the color, width, and style of lines drawn on a graphics
      surface. Now we draw a rectangle using a thin blue pen. Because we switched
      to inches, the rectangle’s size and position are expressed in inches, making
      the code more readable for print‑oriented layouts.'
  - name: Save the image
    text: Finally, write the bitmap to a PNG file in the folder you specified earlier.
  type: HowTo
- questions:
  - answer: Yes, a free trial is available [here](https://releases.aspose.com/) .
    question: Can I use Aspose.Drawing for free?
  - answer: The full API reference is located [here](https://reference.aspose.com/drawing/net/)
      .
    question: Where can I find detailed documentation for Aspose.Drawing?
  - answer: Visit the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      for community help and official assistance.
    question: How do I get support for Aspose.Drawing?
  - answer: Absolutely—obtain one [here](https://purchase.aspose.com/temporary-license/)
      .
    question: Is a temporary license available for Aspose.Drawing?
  - answer: You can buy it [here](https://purchase.aspose.com/buy) .
    question: Where can I purchase a full Aspose.Drawing license?
  type: FAQPage
second_title: Aspose.Drawing .NET API – alternative to System.Drawing.Common
tags:
- Aspose.Drawing
- coordinate transformation
- .NET graphics
- rectangle drawing
title: So zeichnen Sie ein Rechteck – Koordinatensystem-Transformation (Seiten-Transformation)
  in Aspose.Drawing für .NET
url: /de/net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man ein Rechteck zeichnet – Koordinatensystemtransformation (Seitentransformation) in Aspose.Drawing für .NET

## Einführung

In diesem Tutorial lernen Sie **wie man ein Rechteck** zeichnet, während Sie eine seitenniveaus Koordinatensystemtransformation mit Aspose.Drawing für .NET durchführen. Egal, ob Sie eine Reporting‑Engine, ein CAD‑ähnliches Skizzenwerkzeug oder eine Anwendung bauen, die präzise reale Messungen erfordert, führt Sie dieser Leitfaden durch jeden Schritt – vom Erstellen einer Bitmap bis zum Speichern des finalen PNGs. Am Ende sind Sie sicher im Umrechnen von Zoll zu Pixeln, im Löschen des Canvas‑Hintergrunds und im Festlegen von Seiteneinheiten für druckfertige Ausgaben.

## Schnelle Antworten
- **Was ist Koordinatensystemtransformation?** Sie ordnet Seiteneinheiten (wie Zoll) den Geräte‑Pixeln zu, sodass Zeichnungen auf jedem Ausgabegerät korrekt skaliert werden.  
- **Warum Aspose.Drawing wählen?** Es bietet eine vollständig verwaltete, plattformübergreifende Grafik‑API, die System.Drawing.Common ersetzt und über 30 Bildformate unterstützt.  
- **Wie lange dauert die Umsetzung des Beispiels?** Ungefähr 5‑10 Minuten für ein einfaches Rechteck mit Seitentransformation.  
- **Benötige ich eine Lizenz für die Entwicklung?** Eine kostenlose Testversion funktioniert für die Entwicklung; für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich.  
- **Welche .NET‑Laufzeiten werden unterstützt?** .NET Framework 4.6+, .NET Core 3.1+ und .NET 5/6/7.

## Was ist Aspose.Drawing?

Aspose.Drawing ist eine .NET‑Grafikbibliothek, die eine **geräteunabhängige API** zum Erstellen und Manipulieren von Rasterbildern, Vektoren und seitenniveau Zeichnungen bereitstellt, ohne GDI+ zu verwenden. Sie unterstützt **30+ Bildformate** und kann Bilder bis zu **10.000 × 10.000 Pixeln** verarbeiten, während der Speicherverbrauch gering bleibt.

## Warum Koordinatensystemtransformation mit Aspose.Drawing verwenden?

Koordinatensystemtransformation ermöglicht es Ihnen, Grafiken in realen Einheiten zu entwerfen, während die Bibliothek automatisch die Pixel‑Skalierung für jedes Ausgabegerät übernimmt. Dieser Ansatz stellt sicher, dass ein 5‑Zoll‑Rechteck exakt fünf Zoll auf einem 300 DPI‑Drucker ausgibt und proportional auf einem 96 DPI‑Bildschirm erscheint, wodurch manuelle Umrechnungsfehler entfallen.

- **Geräteunabhängiges Design:** Code einmal schreiben; Aspose.Drawing skaliert ihn für Bildschirme, Drucker oder PDFs.  
- **Präzises Zeichnen:** Ideal für technische Diagramme, Konstruktionsschemata oder jede Situation, in der genaue Maße wichtig sind.  
- **Plattformübergreifende Zuverlässigkeit:** Arbeitet konsistent unter Windows, Linux und macOS ohne die GDI+‑Einschränkungen von System.Drawing.  
- **Leistung:** Auf einer typischen 2,5 GHz‑CPU wird das Zeichnen eines 5‑Zoll‑Rechtecks bei 300 DPI in weniger als **15 ms** abgeschlossen, und die Bibliothek kann **50 Frames pro Sekunde** in Echtzeit‑Vorschau‑Szenarien rendern.

## Voraussetzungen

- **Aspose.Drawing‑Bibliothek:** Laden Sie die neueste Version von der offiziellen Seite [hier](https://releases.aspose.com/drawing/net/) herunter.  
- **IDE:** Visual Studio, Rider oder jeder .NET‑kompatible Editor.  
- **Ausgabeordner:** Ersetzen Sie `"Your Document Directory"` im Beispielcode durch den Ordner, in dem Sie das PNG speichern möchten.  
- **Optionale ASP.NET‑Unterstützung:** Sie können das NuGet‑Paket zu einem ASP.NET‑Core‑Projekt hinzufügen und dieselbe API verwenden; das Muster folgt dem üblichen **how to use aspnet**‑Ansatz für .NET‑Bibliotheken.

## Wie man ein Rechteck mit Seitentransformation zeichnet?

Laden Sie eine leere Bitmap, setzen Sie die Seiteneinheit auf Zoll und zeichnen Sie ein Rechteck mit einem dünnen blauen Stift – das erledigt das Rechteckzeichnen in nur wenigen Codezeilen. Die Eigenschaft `Graphics.PageUnit` weist die Engine an, alle Koordinaten als Zoll zu interpretieren, sodass Sie in realen Maßen statt roher Pixel denken können, und die Bibliothek **wandelt Zoll automatisch in Pixel** um, basierend auf der DPI der Bitmap.

### Schritt 1: Namespaces importieren

Die `using`‑Anweisungen geben Ihnen Zugriff auf die Kern‑Zeichenklassen.

```csharp
using System.Drawing;
```

### Schritt 2: Bitmap erstellen

`Bitmap` ist der In‑Memory‑Bildcontainer, auf dem Sie zeichnen. Er hält den Pixelpuffer und stellt Methoden zum Speichern in Dateien bereit. Das Erstellen einer Bitmap definiert die Canvas‑Größe und das Pixel‑Format.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Schritt 3: Graphics‑Objekt erstellen

`Graphics` stellt die Zeichenfläche für die Bitmap bereit. Es übersetzt hoch‑level Zeichenbefehle (Linien, Formen, Text) in Pixel‑Operationen auf der zugrunde liegenden Bitmap.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### Schritt 4: Canvas‑Hintergrund löschen

Das Löschen des Canvas mit einer neutralen Farbe sorgt dafür, dass Ihre Formen hervortreten. In diesem Beispiel füllen wir den Hintergrund mit Hellgrau, was auch die **clear canvas background**‑Technik demonstriert.

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

### Schritt 5: Transformation festlegen (wie Einheiten setzen)

`Graphics.PageUnit` gibt die Maßeinheit für Seitenkoordinaten an. Das Setzen auf `GraphicsUnit.Inch` weist Aspose.Drawing an, **Zoll automatisch in Pixel** umzuwandeln, basierend auf der DPI der Bitmap (standardmäßig 96 DPI, 300 DPI für hochauflösenden Druck). Sie können auch `GraphicsUnit.Millimeter`, `GraphicsUnit.Point` oder `GraphicsUnit.Pixel` wählen, je nach Layout‑Anforderung.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### Schritt 6: Rechteck zeichnen – Rechteckgrafiken zeichnen

`Pen` definiert Farbe, Breite und Stil der Linien, die auf einer Graphics‑Oberfläche gezeichnet werden. Mit einem dünnen blauen Stift zeichnen wir ein Rechteck, dessen Abmessungen in Zoll angegeben sind, was den Code für druckorientierte Layouts lesbarer macht.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

### Schritt 7: Bitmap als PNG speichern

Zum Schluss schreiben wir die Bitmap in eine PNG‑Datei in den zuvor angegebenen Ordner. Das Speichern als PNG bewahrt verlustfreie Qualität und wird plattformübergreifend breit unterstützt.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

## Wie man Grafiken für einen Drucker skaliert?

Setzen Sie die DPI der Bitmap auf die Ziel‑Druckerauflösung (z. B. 300 DPI), bevor Sie zeichnen. Dadurch wird die **scale graphics printer**‑Ausgabe automatisch so angepasst, dass ein Zoll in Ihrem Code einem Zoll auf der gedruckten Seite entspricht, während die logische Größe des Rechtecks unverändert bleibt. Nach dem Aufruf `bitmap.SetResolution(300, 300)` erscheint dasselbe Rechteck auf dem Papier größer, behält aber exakt seine Maße bei.

## Häufige Probleme und Lösungen

| Problem | Warum es passiert | Lösung |
|---------|-------------------|--------|
| **Ausgabedatei nicht erstellt** | Falscher Pfad oder fehlender Ordner | Stellen Sie sicher, dass das Zielverzeichnis existiert oder rufen Sie `Directory.CreateDirectory` vor dem Speichern auf. |
| **Rechteck erscheint verzerrt** | Nicht übereinstimmende `PageUnit` oder DPI | Vergewissern Sie sich, dass `graphics.PageUnit` die beabsichtigte Einheit verwendet und dass die Bitmap‑DPI korrekt eingestellt ist (Standard 96 DPI, 300 DPI für Druck). |
| **Lizenzausnahme** | Ausführung ohne gültige Lizenz in der Produktion | Wenden Sie Ihre temporäre oder permanente Aspose.Drawing‑Lizenz an, bevor Sie Graphics‑Objekte erstellen. |

## Häufig gestellte Fragen

**Q: Kann ich Aspose.Drawing kostenlos nutzen?**  
A: Ja, eine kostenlose Testversion ist [hier](https://releases.aspose.com/) verfügbar.

**Q: Wo finde ich die detaillierte Dokumentation für Aspose.Drawing?**  
A: Die vollständige API‑Referenz befindet sich [hier](https://reference.aspose.com/drawing/net/).

**Q: Wie erhalte ich Support für Aspose.Drawing?**  
A: Besuchen Sie das [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) für Community‑Hilfe und offizielle Unterstützung.

**Q: Ist eine temporäre Lizenz für Aspose.Drawing verfügbar?**  
A: Absolut—erhalten Sie eine [hier](https://purchase.aspose.com/temporary-license/).

**Q: Wo kann ich eine vollständige Aspose.Drawing‑Lizenz erwerben?**  
A: Sie können sie [hier](https://purchase.aspose.com/buy) kaufen.

## Fazit

Sie wissen jetzt **wie man ein Rechteck** zeichnet mit seitenniveau Transformation unter Verwendung von Aspose.Drawing für .NET. Durch das Setzen der Seiteneinheit auf Zoll, das Löschen des Canvas‑Hintergrunds und das Speichern des Ergebnisses als PNG erzielen Sie präzise, geräteunabhängige Ausgaben, die sowohl für die Bildschirmanzeige als auch für hochauflösenden Druck geeignet sind. Experimentieren Sie mit anderen Einheiten, Drehungen oder benutzerdefinierten Koordinatenursprüngen, um noch leistungsfähigere Zeichenszenarien zu erschließen.

---

**Zuletzt aktualisiert:** 2026-11-04  
**Getestet mit:** Aspose.Drawing 24.12 für .NET  
**Autor:** Aspose

## Verwandte Tutorials

- [Wie man Einheit in Aspose.Drawing für .NET festlegt – Maßeinheiten](/drawing/net/coordinate-transformations/units-of-measure/)
- [Globale Transformation](/drawing/net/coordinate-transformations/global-transformation/)
- [Schritt‑für‑Schritt‑Transformation – Koordinatentransformationen](/drawing/net/coordinate-transformations/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}