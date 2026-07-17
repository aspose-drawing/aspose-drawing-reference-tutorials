---
date: 2026-07-17
description: Erfahren Sie, wie Sie Textüberlauf verhindern, indem Sie die Textausrichtung
  in Aspose.Drawing für .NET festlegen und Text zu Bildern hinzufügen. Schritt‑für‑Schritt‑Anleitung
  mit Beispielen.
keywords:
- prevent text overflow
- draw string on image
- center text in rectangle
- vertical text alignment
- replace system drawing
lastmod: 2026-07-17
linktitle: Textausrichtung festlegen mit Aspose.Drawing für .NET
og_description: Verhindern Sie Textüberlauf, indem Sie die Textausrichtung in Aspose.Drawing
  für .NET festlegen. Erfahren Sie, draw string on image, center text in rectangle
  und replace System.Drawing.
og_image_alt: 'Developer guide: Prevent text overflow by aligning text in Aspose.Drawing
  for .NET'
og_title: Verhindern von Textüberlauf – Textausrichtung festlegen mit Aspose.Drawing
  für .NET
schemas:
- author: Aspose
  dateModified: '2026-07-17'
  description: Learn how to prevent text overflow by setting text alignment in Aspose.Drawing
    for .NET and add text to images. Step‑by‑step guide with examples.
  headline: Prevent Text Overflow – Set Text Alignment with Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to prevent text overflow by setting text alignment in Aspose.Drawing
    for .NET and add text to images. Step‑by‑step guide with examples.
  name: Prevent Text Overflow – Set Text Alignment with Aspose.Drawing for .NET
  steps:
  - name: '**Aspose.Drawing Library** – download it [here](https://releases.aspose.com/drawing/net/).'
    text: '**Aspose.Drawing Library** – download it [here](https://releases.aspose.com/drawing/net/).'
  - name: '**Development Environment** – Visual Studio 2022 (or any C# IDE).'
    text: '**Development Environment** – Visual Studio 2022 (or any C# IDE).'
  - name: '**Basic .NET knowledge** – you should be comfortable with C# projects and
      NuGet packages.'
    text: '**Basic .NET knowledge** – you should be comfortable with C# projects and
      NuGet packages.'
  - name: '**Resize the rectangle** – increase `rectangle.Width` or `rectangle.Height`.'
    text: '**Resize the rectangle** – increase `rectangle.Width` or `rectangle.Height`.'
  - name: '**Split the text** – break the string into lines that fit, then call `DrawString`
      for each line with adjusted Y‑coordinates.'
    text: '**Split the text** – break the string into lines that fit, then call `DrawString`
      for each line with adjusted Y‑coordinates.'
  type: HowTo
- questions:
  - answer: Omit the `DrawRectangle` call and pass the desired `PointF` location to
      `Graphics.DrawString`.
    question: How do I draw a string without a surrounding rectangle?
  - answer: Yes—apply a `Matrix` transformation to the `Graphics` object before drawing,
      then reset it afterwards.
    question: Can I rotate the text while keeping alignment?
  - answer: Simply change the file extension in `bitmap.Save` and optionally specify
      `ImageFormat.Jpeg`.
    question: Is it possible to export the image as JPEG instead of PNG?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- prevent text overflow
- Aspose.Drawing
- .NET graphics
- text alignment
title: Verhindern von Textüberlauf – Textausrichtung festlegen mit Aspose.Drawing
  für .NET
url: /de/net/text-and-fonts/format-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Verhindern von Textüberlauf – Textausrichtung mit Aspose.Drawing festlegen

## Einleitung

Wenn Sie in .NET beim Rendern von Grafiken **Textüberlauf verhindern** müssen, bietet Aspose.Drawing Ihnen eine feinkörnige Kontrolle über Textpositionierung, Ausrichtung und Zeilenumbruch. Egal, ob Sie einen Badge‑Generator, einen dynamischen Bericht oder irgendeine bildbasierte Ausgabe erstellen, die Beherrschung der Textausrichtung stellt sicher, dass Ihr Text innerhalb des vorgesehenen Rechtecks bleibt und professionell aussieht. In diesem Leitfaden führen wir Sie durch das Erstellen einer Bitmap‑Leinwand, das Konfigurieren von `StringFormat`, das Zeichnen eines Rechtecks mit zentriertem Text, das Handhaben von Überlauf und schließlich das Speichern des Bildes.

## Schnelle Antworten
- **Was bedeutet “set text alignment”?** Sie definiert, wie Text horizontal und vertikal innerhalb eines Zeichenrechtecks positioniert wird.  
- **Welche Klasse steuert die Ausrichtung?** `StringFormat` ermöglicht das Setzen von `Alignment` und `LineAlignment`.  
- **Kann ich einen String und ein Rechteck zusammen zeichnen?** Ja – verwenden Sie `Graphics.DrawRectangle` gefolgt von `Graphics.DrawString`.  
- **Wie verhindere ich Textüberlauf?** Passen Sie die Rechteckgröße an oder teilen Sie den Text manuell in mehrere Zeilen.  
- **Benötige ich eine Lizenz für die Produktion?** Für den nicht‑evaluativen Einsatz ist eine kommerzielle Aspose.Drawing‑Lizenz erforderlich.

## Was bedeutet **set text alignment** in Aspose.Drawing?

`set text alignment` konfiguriert die horizontale (`StringAlignment`) und vertikale (`LineAlignment`) Platzierung von Text innerhalb eines `Rectangle` oder Zeichenbereichs. Durch Anpassen dieser Eigenschaften steuern Sie, ob Text linksbündig, zentriert, rechtsbündig, obenbündig, mittig oder untenbündig angezeigt wird, was ein präzises Layout in Grafiken, Badges und Berichten ermöglicht, die mit Aspose.Drawing erzeugt werden.

## Warum Aspose.Drawing für Textausrichtung verwenden?

Aspose.Drawing beseitigt die GDI+‑Einschränkungen, die `System.Drawing.Common` plagen. Es unterstützt **5 wichtige .NET‑Laufzeiten** – .NET Framework 4.6+, .NET Core 2.0+, .NET 5, .NET 6 und .NET 7 – und kann Bilder bis zu **4000 × 4000 px** (≈ 100 MB) rendern, ohne den Speicher zu erschöpfen. Anti‑Aliasing, Hoch‑DPI‑Skalierung und vollständige Linux‑Container‑Kompatibilität ermöglichen die Erzeugung pixelperfekter Grafiken in jedem Bereitstellungsszenario.

## Voraussetzungen

1. **Aspose.Drawing Library** – laden Sie sie [hier](https://releases.aspose.com/drawing/net/) herunter.  
2. **Entwicklungsumgebung** – Visual Studio 2022 (oder jede C#‑IDE).  
3. **Grundlegende .NET‑Kenntnisse** – Sie sollten mit C#‑Projekten und NuGet‑Paketen vertraut sein.

## Namespaces importieren

Um zu beginnen, importieren Sie die erforderlichen Namespaces. Diese geben Ihnen Zugriff auf Grafik, Textdarstellung und Zeichenprimitive.

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Wie verhindert man Textüberlauf mit Aspose.Drawing?

Bitmap ist eine Klasse, die ein im Speicher gespeichertes Bild darstellt, während `RectangleF` einen Fließkomma‑Rechteckbereich zum Zeichnen definiert. Durch die Verwendung eines `StringFormat` mit `Trimming` auf `StringTrimming.EllipsisCharacter` werden überschüssige Zeichen automatisch durch ein Ellipsis ersetzt, sodass der Text die Rechteckgrenzen nie überschreitet. Das vorherige Messen des Strings ermöglicht es Ihnen zu entscheiden, ob das Rechteck verkleinert oder der Text in mehrere Zeilen aufgeteilt werden soll, was ein sauberes Layout ohne Überlauf garantiert.

Laden Sie Ihr Bitmap, definieren Sie ein passend dimensioniertes `RectangleF` und verwenden Sie ein `StringFormat` mit `Trimming` auf `StringTrimming.EllipsisCharacter`, um überschüssige Zeichen automatisch abzuschneiden. Für volle Kontrolle messen Sie den String mit `Graphics.MeasureString` und verkleinern das Rechteck oder teilen den Text in Zeilen auf, bevor Sie zeichnen. Dieser Ansatz garantiert, dass keine Zeichen außerhalb der visuellen Grenzen erscheinen.

## Schritt 1: Bitmap- und Graphics-Objekte erstellen  

Bitmap repräsentiert ein Bild im Speicher, während Graphics Zeichenmethoden für dieses Bitmap bereitstellt. Das Erstellen eines Bitmaps liefert eine Leinwand, auf der Sie zeichnen können. Das `Graphics`‑Objekt ist die Zeichenfläche, und wir aktivieren die hochwertige Textdarstellung mit `TextRenderingHint`.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

## Schritt 2: **StringFormat** und Stil festlegen  

StringFormat gibt Textlayout‑Optionen wie Ausrichtung, Zeilenabstand und Trimmen an. Hier **set text alignment** wir, indem wir eine `StringFormat`‑Instanz konfigurieren. Wir bereiten außerdem Pinsel, Stifte und eine Schriftart vor, die beim Zeichnen des Strings verwendet werden.

```csharp
StringFormat stringFormat = new StringFormat();
stringFormat.Alignment = StringAlignment.Center;          // Horizontal alignment
stringFormat.LineAlignment = StringAlignment.Center;      // Vertical alignment

Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

## Schritt 3: Text erstellen und formatieren – **how to draw string** und **draw rectangle with text**

Graphics.DrawString rendert Text auf die Leinwand, und Graphics.DrawRectangle zeichnet eine Rechteckform. Wir erstellen den Text, definieren das Rechteck, das ihn enthalten wird, und zeichnen anschließend sowohl den Rechteckrahmen als auch den String selbst.

```csharp
string text = "Lorem ipsum ...";  // (Your lengthy text goes here)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle, stringFormat);
```

### Umgang mit Textüberlauf

Wenn der bereitgestellte `text` die Grenzen des Rechtecks überschreitet, haben Sie zwei gängige Optionen:

1. **Rechteck vergrößern** – `rectangle.Width` oder `rectangle.Height` erhöhen.  
2. **Text aufteilen** – den String in passende Zeilen zerlegen und dann `DrawString` für jede Zeile mit angepassten Y‑Koordinaten aufrufen.

## Wie man einen String auf ein Bild mit Aspose.Drawing zeichnet?

Graphics.DrawString zeichnet den angegebenen Text mit einer Schriftart und Formatierungsoptionen. Instanziieren Sie ein `Graphics`‑Objekt aus Ihrem Bitmap und rufen Sie dann `DrawString` mit dem vorbereiteten `StringFormat` auf. Dieser einzelne Aufruf rendert den Text genau an der gewünschten Stelle und berücksichtigt Ausrichtung, Trimmen und jede angewandte Transformationsmatrix. Das Hinzufügen eines hochwertigen Rendering‑Hinweises sorgt dafür, dass die Ausgabe auf Hoch‑DPI‑Displays scharf bleibt.

## Wie man Text in einem Rechteck zentriert?

StringAlignment bestimmt die horizontale Ausrichtung von Text innerhalb eines Layout‑Rechtecks. Setzen Sie `stringFormat.Alignment = StringAlignment.Center` und `stringFormat.LineAlignment = StringAlignment.Center`. Dadurch wird der Text horizontal und vertikal im Rechteck zentriert, was ihn ideal für Badges, Schaltflächen oder Etiketten‑Overlays macht. Die zentrierte Platzierung funktioniert konsistent über verschiedene Bildgrößen und DPI‑Einstellungen hinweg und liefert ein ausgewogenes visuelles Erscheinungsbild.

## Wie man vertikale Textausrichtung erreicht?

LineAlignment steuert die vertikale Platzierung von Text innerhalb des Rechtecks. Verwenden Sie `stringFormat.LineAlignment` mit den Werten `StringAlignment.Near`, `Center` oder `Far`, um den Text oben, mittig oder unten im Rechteck zu positionieren. Kombinieren Sie dies mit `Graphics.TranslateTransform`, wenn Sie den Text drehen müssen und dabei die vertikale Ausrichtung beibehalten wollen. Das Anpassen der Zeilenausrichtung stellt sicher, dass mehrzeilige Blöcke genau dort ausgerichtet sind, wo Sie es erwarten, selbst nach Transformationen.

## Schritt 4: Ausgabe speichern – **add text to image**

Abschließend schreiben Sie das Bitmap auf die Festplatte. Dieser Schritt demonstriert **add text to image** in einem einzigen Aufruf.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\FormatText_out.png");
```

## Häufige Probleme und Lösungen

| Problem | Lösung |
|-------|----------|
| **Text erscheint unscharf** | Stellen Sie sicher, dass `graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;` gesetzt ist. |
| **Text wird abgeschnitten** | Vergrößern Sie die Rechteckgröße oder aktivieren Sie die Wortumbruch‑Logik, indem Sie die Stringgröße mit (`Graphics.MeasureString`) messen. |
| **Schriftart nicht gefunden** | Prüfen Sie, ob die Schriftart auf dem Host‑Computer installiert ist oder betten Sie eine private Schriftart mit `PrivateFontCollection` ein. |
| **Unerwartete Farben** | Überprüfen Sie die Farben von Pinsel und Stift; beachten Sie, dass `Color.FromKnownColor` systemdefinierte Farben verwendet. |

## Häufig gestellte Fragen

**F1: Ist Aspose.Drawing mit allen .NET‑Versionen kompatibel?**  
A1: Ja, Aspose.Drawing ist so konzipiert, dass es mit einer breiten Palette von .NET‑Versionen kompatibel ist und Entwicklern Flexibilität bietet.

**F2: Kann ich den Schriftstil weiter anpassen?**  
A2: Auf jeden Fall! Passen Sie die Parameter des `Font`‑Objekts an, um die gewünschte Schriftgröße, den Stil und die Familie zu erreichen.

**F3: Wie kann ich Textüberlauf innerhalb des definierten Rechtecks handhaben?**  
A3: Sie können Textüberlauf verwalten, indem Sie die Größe des Rechtecks anpassen oder benutzerdefinierte Logik implementieren, um langen Text zu behandeln.

**F4: Gibt es weitere Formatierungsoptionen in Aspose.Drawing?**  
A4: Ja, Aspose.Drawing bietet ein umfassendes Set an Werkzeugen zur Grafikmanipulation, einschließlich verschiedener Formatierungsoptionen für Text, Formen und mehr.

**F5: Wo finde ich zusätzlichen Support für Aspose.Drawing?**  
A5: Erkunden Sie das Aspose.Drawing‑Forum [hier](https://forum.aspose.com/c/drawing/44) für Community‑Support und Diskussionen.

**Zusätzliche Fragen & Antworten**

**F: Wie zeichne ich einen String ohne umgebendes Rechteck?**  
A: Lassen Sie den Aufruf von `DrawRectangle` weg und übergeben Sie den gewünschten `PointF`‑Standort an `Graphics.DrawString`.

**F: Kann ich den Text drehen und dabei die Ausrichtung beibehalten?**  
A: Ja – wenden Sie vor dem Zeichnen eine `Matrix`‑Transformation auf das `Graphics`‑Objekt an und setzen Sie sie anschließend zurück.

**F: Ist es möglich, das Bild als JPEG statt PNG zu exportieren?**  
A: Ändern Sie einfach die Dateierweiterung in `bitmap.Save` und geben Sie optional `ImageFormat.Jpeg` an.

**Letzte Aktualisierung:** 2026-07-17  
**Getestet mit:** Aspose.Drawing 24.11 for .NET  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Verwandte Tutorials

- [Wie man Text mit Aspose.Drawing für .NET zeichnet](/drawing/net/text-and-fonts/draw-text/)
- [Text zu Bildern in Aspose.Drawing hinzufügen](/drawing/net/use-cases/text-on-image/)
- [Wie man Text und Schriftarten mit Aspose.Drawing für .NET zeichnet](/drawing/net/text-and-fonts/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}