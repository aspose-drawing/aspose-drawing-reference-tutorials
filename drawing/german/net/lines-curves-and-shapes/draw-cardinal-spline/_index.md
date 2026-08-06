---
date: 2026-05-29
description: Erfahren Sie, wie Sie PNG speichern und Cardinal Splines in .NET mit
  Aspose.Drawing zeichnen. Speichern Sie Kurven als PNG, erstellen Sie glatte Grafiken
  und generieren Sie Bitmaps mühelos in eine Datei.
keywords:
- how to save png
- save bitmap to file
- create smooth curve
- draw curve c#
- generate png graphics
linktitle: Cardinal Splines in Aspose.Drawing zeichnen
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn how to save PNG and draw cardinal splines in .NET with Aspose.Drawing.
    Save curve as PNG, create smooth graphics, and generate bitmap to file effortlessly.
  headline: How to Save PNG and Draw Cardinal Splines with Aspose.Drawing
  type: TechArticle
- questions:
  - answer: '`Graphics.DrawCurve` interpolates a series of points into a smooth cardinal
      spline.'
    question: What does the primary method do?
  - answer: PNG via `Bitmap.Save`.
    question: Which format is used to save the image?
  - answer: A trial works for development; a commercial license is required for production.
    question: Do I need a license to save images?
  - answer: Yes, overloads of `DrawCurve` let you specify tension.
    question: Can I change the curve tension?
  - answer: Absolutely – it supports .NET Framework and .NET Core/5/6.
    question: Is Aspose.Drawing compatible with .NET 6+?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Wie man PNG speichert und Cardinal Splines mit Aspose.Drawing zeichnet
url: /de/net/lines-curves-and-shapes/draw-cardinal-spline/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man PNG speichert und Kardinalsplines mit Aspose.Drawing zeichnet

## Einführung

In diesem Tutorial erfahren Sie **wie man PNG speichert** Dateien, während Sie glatte Kardinalsplines mit Aspose.Drawing für .NET zeichnen. Egal, ob Sie eine Chart‑Komponente, einen Diagrammeditor erstellen oder einfach eine benutzerdefinierte Kurve als PNG exportieren müssen, die nachfolgenden Schritte führen Sie durch das Erstellen einer Bitmap‑Leinwand, das Zeichnen eines Splines mit einem Stift und das Persistieren des Ergebnisses auf die Festplatte. Außerdem sehen Sie, warum Aspose.Drawing eine zuverlässige plattformübergreifende Alternative zu System.Drawing.Common ist.

## Schnelle Antworten
- **Was macht die primäre Methode?** `Graphics.DrawCurve` interpoliert eine Reihe von Punkten zu einem glatten Kardinalspline.  
- **Welches Format wird zum Speichern des Bildes verwendet?** PNG über `Bitmap.Save`.  
- **Benötige ich eine Lizenz zum Speichern von Bildern?** Eine Testversion funktioniert für die Entwicklung; für die Produktion ist eine kommerzielle Lizenz erforderlich.  
- **Kann ich die Kurvenspannung ändern?** Ja, Überladungen von `DrawCurve` ermöglichen das Festlegen der Spannung.  
- **Ist Aspose.Drawing mit .NET 6+ kompatibel?** Absolut – es unterstützt .NET Framework und .NET Core/5/6.

## Was bedeutet „how to save PNG“ im Kontext von Aspose.Drawing?

Ein PNG zu speichern bedeutet, die im Speicher befindliche Bitmap, auf der Sie zeichnen, in eine physische PNG‑Datei auf der Festplatte zu konvertieren. Der Vorgang schreibt die Pixeldaten mit verlustfreier Kompression und bewahrt die genauen Farben sowie etwaige Alpha‑Kanal‑Informationen. Die `Bitmap.Save`‑Methode von Aspose.Drawing übernimmt die PNG‑Kodierung automatisch, sodass Sie die Formatdetails nicht selbst verwalten müssen.

## Warum ein Kardinalspline mit Aspose.Drawing zeichnen?

Ein Kardinalspline erzeugt eine glatte, fließende Kurve, die einer Menge von Kontrollpunkten genau folgt, und ist damit ideal für Datenvisualisierungen, UI‑Grafiken und benutzerdefinierte Formen. Aspose.Drawing unterstützt **30+ Bildformate** und kann mehrhundertseitige Grafiken rendern, ohne die gesamte Datei in den Speicher zu laden, was Ihnen sowohl Geschwindigkeit als auch Flexibilität bietet.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass Sie folgendes haben:

- Visual Studio (eine aktuelle Version) installiert.  
- Aspose.Drawing für .NET Bibliothek. Sie können sie [hier](https://releases.aspose.com/drawing/net/) herunterladen.  
- Grundlegende Kenntnisse in C#‑Programmierung.

## Namespaces importieren

In Ihrer C#‑Datei beginnen Sie mit dem Import des erforderlichen Namespaces:

Der `Aspose.Drawing`‑Namespace enthält alle Kerntypen wie `Bitmap`, `Graphics` und `Pen`.  
```csharp
using Aspose.Drawing;
```
```csharp
using System.Drawing;
```

## Schritt 1: Erstellen einer Bitmap (Leinwand)

Zuerst erstellen Sie eine Bitmap, die als Leinwand für Ihre Zeichnung dient. Diese Bitmap ist der Ort, an dem das Spline gerendert wird, bevor Sie **das Bild speichern**.

Eine Bitmap stellt ein Bild im Speicher mit einem definierten Pixelformat und Abmessungen dar.  
```csharp
int width = 800;
int height = 600;
Bitmap bitmap = new Bitmap(width, height, PixelFormat.Format32bppPArgb);
```
```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## Schritt 2: Erstellen eines Graphics-Objekts

Als Nächstes erhalten Sie ein `Graphics`‑Objekt von der Bitmap. Dieses Objekt stellt die Zeichenfläche bereit.

Graphics bietet eine Zeichenfläche zum Rendern von Formen, Text und Bildern auf einer Bitmap.  
```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.Transparent);
```
```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## Schritt 3: Stift definieren und Kurve zeichnen

Definieren Sie einen `Pen` mit der gewünschten Farbe und Breite und zeichnen Sie dann das Kardinalspline mit `DrawCurve`. Dies demonstriert die **Kurve mit Stift zeichnen**‑Technik und dient als **Beispiel für ein Kardinalspline**.

Ein Pen kapselt die Farbe, Breite und Linienart, die zum Zeichnen von Linien und Kurven verwendet werden.  
```csharp
Pen pen = new Pen(Color.Blue, 3);
PointF[] points = {
    new PointF(100, 400), new PointF(200, 100),
    new PointF(300, 300), new PointF(400, 150),
    new PointF(500, 350)
};
graphics.DrawCurve(pen, points, 0.5f); // tension = 0.5
```
```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawCurve(pen, new Point[] {
    new Point(10, 700),
    new Point(250, 500),
    new Point(500, 10),
    new Point(750, 500),
    new Point(990, 700)
});
```

## Schritt 4: Bild speichern (Kurve als PNG speichern)

Abschließend speichern Sie die Bitmap in einer PNG‑Datei. Dies ist der Kern von **wie man PNG speichert** in diesem Tutorial.

`Bitmap.Save` schreibt das Bild in eine Datei im angegebenen Format, z. B. PNG.  
```csharp
string outputPath = Path.Combine(Environment.CurrentDirectory, "cardinal-spline.png");
bitmap.Save(outputPath, ImageFormat.Png);
```
```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawCardinalSpline_out.png");
```

> **Profi‑Tipp:** Verwenden Sie `Path.Combine`, um Dateipfade plattformübergreifend sicher zu erstellen.

Herzlichen Glückwunsch! Sie haben erfolgreich ein Kardinalspline gezeichnet und das Ergebnis als PNG‑Bild mit Aspose.Drawing für .NET gespeichert. Experimentieren Sie gern mit verschiedenen Punktarrays, Stiftfarben oder Linienstärken, um Ihre Kurven anzupassen.

## Häufige Anwendungsfälle

- **Datenvisualisierungen** – glatte Liniendiagramme, die präzise Kontrollpunkte benötigen.  
- **Benutzerdefinierte UI‑Komponenten** – Zeichnen von Knöpfen, Schiebereglern oder dekorativen Rahmen.  
- **Exportierbare Grafiken** – PNG‑Assets on the fly für Berichte oder Web‑Inhalte erzeugen.

## Fehlerbehebung & Tipps

- **Bild erscheint leer?** Stellen Sie sicher, dass das Pixelformat der Bitmap Alpha unterstützt (`Format32bppPArgb`) und rufen Sie bei Bedarf `graphics.Clear(Color.Transparent)` auf.  
- **Unerwartete Kurvenform?** Passen Sie den Spannungsparameter an, indem Sie die Überladung `DrawCurve(pen, points, tension)` verwenden.  
- **Dateizugriffsfehler?** Vergewissern Sie sich, dass das Zielverzeichnis existiert und Ihre Anwendung Schreibrechte hat.

## Häufig gestellte Fragen

**F1: Kann ich Aspose.Drawing für kommerzielle Projekte verwenden?**  
A1: Ja, Aspose.Drawing ist sowohl für private als auch für kommerzielle Projekte geeignet. Prüfen Sie die Lizenzdetails auf der [Kaufseite](https://purchase.aspose.com/buy).

**F2: Wie kann ich eine temporäre Lizenz zum Testen erhalten?**  
A2: Holen Sie sich eine temporäre Lizenz für Testzwecke [hier](https://purchase.aspose.com/temporary-license/).

**F3: Wo finde ich zusätzlichen Support?**  
A3: Besuchen Sie das [Aspose.Drawing‑Forum](https://forum.aspose.com/c/drawing/44) für Community‑Support und Diskussionen.

**F4: Gibt es eine kostenlose Testversion?**  
A4: Ja, testen Sie die Funktionen mit der [kostenlosen Testversion](https://releases.aspose.com/), bevor Sie einen Kauf tätigen.

**F5: Wie greife ich auf die Dokumentation zu?**  
A5: Konsultieren Sie die umfassende [Dokumentation](https://reference.aspose.com/drawing/net/) für detaillierte Informationen und Beispiele.

**Zuletzt aktualisiert:** 2026-05-29  
**Getestet mit:** Aspose.Drawing 24.11 für .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
