---
date: 2026-09-23
description: Erfahren Sie, wie Sie Text auf ein Bild mit Aspose.Drawing für .NET zeichnen.
  Erzeugen Sie ein Bild mit Text, fügen Sie Text zu einem Bitmap hinzu und speichern
  Sie das Bitmap als PNG mit benutzerdefinierten Schriftarten.
keywords:
- draw text on image
- generate image with text
- custom font on image
- save bitmap as png
- add text to bitmap
lastmod: 2026-09-23
linktitle: So Text mit Aspose.Drawing zeichnen
og_description: Erfahren Sie, wie Sie Text auf ein Bild mit Aspose.Drawing für .NET
  zeichnen. Dieses Tutorial zeigt Ihnen, wie Sie ein Bild mit Text erzeugen, Text
  zu einem Bitmap hinzufügen und das Bitmap als PNG mit benutzerdefinierten Schriftarten
  speichern.
og_image_alt: Screenshot of a PNG image created with Aspose.Drawing showing custom
  text
og_title: Text auf Bild mit Aspose.Drawing für .NET – Schnellleitfaden
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to draw text on image using Aspose.Drawing for .NET. Generate
    image with text, add text to bitmap, and save bitmap as PNG with custom fonts.
  headline: How to draw text on image with Aspose.Drawing for .NET
  type: TechArticle
- questions:
  - answer: Replace the `.png` extension with `.jpg` in the `Save` method and optionally
      specify an `ImageCodecInfo` for JPEG quality.
    question: How do I change the output format to JPEG?
  - answer: Yes, include line‑break characters (`\n`) in the string or use `StringFormat`
      with `FormatFlags.LineLimit`.
    question: Can I draw multi‑line text?
  - answer: Use `Graphics.MeasureString` to get the exact dimensions of the rendered
      text.
    question: Is there a way to measure text size before drawing?
  - answer: Absolutely. Provide a font that contains the required glyphs and the library
      will render them correctly.
    question: Does Aspose.Drawing support Unicode characters?
  - answer: The examples were tested with Aspose.Drawing 24.11 for .NET.
    question: What version of Aspose.Drawing was used for testing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- draw text on image
- Aspose.Drawing
- .NET image processing
- generate image with text
- custom font on image
title: So zeichnen Sie Text auf ein Bild mit Aspose.Drawing für .NET
url: /de/net/text-and-fonts/draw-text/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man Text auf ein Bild mit Aspose.Drawing für .NET zeichnet

## Einleitung

In diesem Schritt‑für‑Schritt‑Leitfaden lernen Sie **wie man Text auf ein Bild zeichnet** mit Aspose.Drawing für .NET. Egal, ob Sie ein *dynamisches Textbild* erstellen, Text zu einem bestehenden Bitmap hinzufügen oder eine Grafik mit benutzerdefinierten Schriftarten erzeugen müssen, führt Sie dieses Tutorial durch jedes Detail, sodass Sie in wenigen Minuten mit dem Zeichnen von Text beginnen können. Die Bibliothek unterstützt über 30 GDI+-Methoden, läuft unter Windows, Linux und macOS und hat **keine externen Abhängigkeiten**, was sie zu einer zuverlässigen Wahl für serverseitige Bildgenerierung macht.

## Schnelle Antworten
- **Welche Bibliothek wird verwendet?** Aspose.Drawing for .NET  
- **Primäre Aufgabe?** Text auf ein Bild zeichnen (Bild mit Text erstellen)  
- **Schlüssel­methode?** `Graphics.DrawString` (String auf Bild zeichnen)  
- **Ausgabeformat?** PNG (Bitmap als PNG speichern)  
- **Voraussetzungen?** .NET-Entwicklungsumgebung und Aspose.Drawing-Bibliothek  

## Was bedeutet das Zeichnen von Text mit Aspose.Drawing?

Text mit Aspose.Drawing zu zeichnen bedeutet, die GDI+‑kompatible API der Bibliothek zu verwenden, um Unicode‑Zeichenketten auf eine Raster‑Leinwand zu rendern. Die Methode `Graphics.DrawString` schreibt den Text in ein Bitmap und ermöglicht die Steuerung von Schriftart, Farbe, Ausrichtung und Anti‑Aliasing. Dieser Ansatz erlaubt es, hochwertige Bilder zu erzeugen, ohne System.Drawing.Common zu installieren.

## Warum Aspose.Drawing zum Hinzufügen von Text zu Bildern verwenden?

Aspose.Drawing bietet eine zuverlässige, plattformübergreifende Möglichkeit, Text auf Bildern zu rendern, ohne native GDI+-Bibliotheken zu benötigen, und liefert konsistente Qualität und Leistung auf jedem Betriebssystem. Es unterstützt fortschrittliches Anti‑Aliasing, Unicode‑Zeichen und benutzerdefinierte Schriftarten und lässt sich nahtlos in .NET‑Anwendungen integrieren, wodurch es sowohl für serverseitige Bildgenerierung als auch für Desktop‑Tools ideal ist.

- **Plattformübergreifende Zuverlässigkeit** – funktioniert unter Windows, Linux und macOS.  
- **Erweiterte Darstellung** – Anti‑Aliasing und Sub‑Pixel‑Textglättung für gestochen scharfe Ausgabe.  
- **Keine externen Abhängigkeiten** – die Bibliothek enthält alles, was Sie benötigen, um *Bild mit Text zu erstellen*.

## Voraussetzungen

Bevor Sie beginnen, stellen Sie sicher, dass Sie folgendes haben:

- **Aspose.Drawing for .NET** – laden Sie es von der [Aspose.Drawing documentation](https://reference.aspose.com/drawing/net/) herunter.  
- **Eine .NET‑IDE** wie Visual Studio oder VS Code.  

## Namespaces importieren

Beginnen Sie damit, die erforderlichen Namespaces zu importieren:

Diese Namespaces stellen die Kern‑GDI+-Typen wie `Bitmap`, `Graphics` und Text‑Rendering‑Hilfsmittel bereit.  
```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Schritt 1: Bitmap‑ und Graphics‑Objekte erstellen

`Bitmap` ist der Raster‑Bild‑Container von Aspose.Drawing für Pixeldaten, und `Graphics` liefert Zeichenmethoden, um Formen und Text darauf zu rendern.

`Bitmap` stellt ein Bild im Speicher dar, während `Graphics` Zeichenmethoden bereitstellt, um auf dieses Bitmap zu rendern.  
```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

Hier erstellen wir ein `Bitmap`, das das endgültige Bild hält, und ein `Graphics`‑Objekt, mit dem wir darauf zeichnen können. Der Anti‑Aliasing‑Hinweis sorgt dafür, dass der Text glatt aussieht.

## Schritt 2: Pinsel, Stift und Schriftart einrichten

`Brush` definiert die Füllfarbe, `Pen` umreißt Formen, und `Font` gibt Schriftart, Größe und Stil für das Rendern von Text an.

`Brush` füllt Formen mit Farbe, `Pen` umreißt Formen, und `Font` definiert die Schriftart und Größe für das Text‑Rendering.  
```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

- **Brush** definiert die Textfarbe.  
- **Pen** wird später verwendet, um ein Rechteck um den Text zu zeichnen (optional).  
- **Font** gibt die Schriftart, Größe und den Stil für die *String‑Zeichnung auf Bild*‑Operation an.

## Schritt 3: Text und Rechteck definieren

`Rectangle` definiert das Begrenzungs‑Rechteck, in dem der Text platziert wird, und gibt X/Y‑Koordinaten sowie Breite/Höhe an.

`Rectangle` gibt die Position und Größe eines rechteckigen Bereichs an, der hier verwendet wird, um den gezeichneten Text zu begrenzen.  
```csharp
string text = "Lorem ipsum..."; // (Your desired text)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
```

Das `Rectangle` bestimmt, wo der Text platziert wird. Passen Sie die Koordinaten und die Größe an Ihr Layout an.

## Schritt 4: Rechteck und Text zeichnen

`Graphics.DrawString` rendert den angegebenen Text innerhalb des angegebenen Rechtecks unter Verwendung der bereitgestellten Schriftart und des Pinsels.

`Graphics.DrawString` rendert eine Textzeichenkette innerhalb eines spezifizierten Rechtecks unter Verwendung der angegebenen Schriftart und des Pinsels.  
```csharp
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle);
```

Zuerst umreißen wir den Bereich mit einem blauen Rechteck, dann **fügen wir Text zum Bitmap hinzu** indem wir `DrawString` aufrufen. Dies ist der Kern des *Textzeichnens* auf dem Bild.

## Schritt 5: Ergebnis speichern

Das Bild wird als PNG‑Datei gespeichert, wodurch die Anforderung *Bitmap als PNG speichern* erfüllt wird. Ersetzen Sie den Platzhalter‑Pfad durch den tatsächlichen Ordner, in dem Sie die Datei speichern möchten.

`bitmap.Save` schreibt das Bild in eine Datei im gewählten Format, z. B. PNG.  
```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\DrawText_out.png");
```

## Häufige Anwendungsfälle

- **Erzeugen von Zertifikaten** mit personalisierten Namen.  
- **Erstellen von Wasserzeichen‑Thumbnails** für Webgalerien.  
- **Erstellen dynamischer Diagramme**, die Beschriftungen oder Anmerkungen enthalten.  

## Fehlerbehebung & Tipps

- **Schriftart nicht gefunden?** Stellen Sie sicher, dass die Schriftart auf dem Host‑Rechner installiert ist, oder verwenden Sie eine private Schriftartsammlung.  
- **Text abgeschnitten?** Vergrößern Sie die Rechteckgröße oder reduzieren Sie die Schriftgröße.  
- **Leistungsbedenken?** Verwenden Sie nach Möglichkeit dasselbe `Graphics`‑Objekt für mehrere Zeichenoperationen erneut.  

## Häufig gestellte Fragen

**F: Wie ändere ich das Ausgabeformat zu JPEG?**  
A: Ersetzen Sie die `.png`‑Erweiterung durch `.jpg` in der `Save`‑Methode und geben Sie optional ein `ImageCodecInfo` für die JPEG‑Qualität an.

**F: Kann ich mehrzeiligen Text zeichnen?**  
A: Ja, fügen Sie Zeilenumbruch‑Zeichen (`\n`) in die Zeichenkette ein oder verwenden Sie `StringFormat` mit `FormatFlags.LineLimit`.

**F: Gibt es eine Möglichkeit, die Textgröße vor dem Zeichnen zu messen?**  
A: Verwenden Sie `Graphics.MeasureString`, um die genauen Abmessungen des gerenderten Textes zu erhalten.

**F: Unterstützt Aspose.Drawing Unicode‑Zeichen?**  
A: Absolut. Stellen Sie eine Schriftart bereit, die die erforderlichen Glyphen enthält, und die Bibliothek rendert sie korrekt.

**F: Welche Version von Aspose.Drawing wurde für die Tests verwendet?**  
A: Die Beispiele wurden mit Aspose.Drawing 24.11 für .NET getestet.

---

**Zuletzt aktualisiert:** 2026-09-23  
**Getestet mit:** Aspose.Drawing 24.11 für .NET  
**Autor:** Aspose

## Verwandte Tutorials

- [Bitmap‑Grafiken in C# erstellen – PNG‑Bild speichern und mit installierten Schriftarten in Aspose.Drawing arbeiten](/drawing/net/text-and-fonts/installed-fonts/)
- [Wie man ein Bitmap als PNG mit der Aspose.Drawing‑API für .NET speichert](/drawing/net/image-editing/display/)
- [Text auf Bild](/drawing/net/use-cases/text-on-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}