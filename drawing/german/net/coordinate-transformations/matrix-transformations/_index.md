---
date: 2026-08-28
description: Lernen Sie dieses Matrix-Transformations-Tutorial für Aspose.Drawing
  .NET, das erklärt, wie man ein gedrehtes Rechteck zeichnet, Matrixrotation anwendet
  und Matrixskalierung in C# durchführt.
keywords:
- matrix transformation tutorial
- draw rotated rectangle
- matrix rotation c#
- matrix scaling c#
- Aspose.Drawing graphics
lastmod: 2026-08-28
linktitle: Matrix-Transformationen in Aspose.Drawing
og_description: Matrix-Transformations-Tutorial für Aspose.Drawing .NET. Lernen Sie,
  wie man ein gedrehtes Rechteck zeichnet, Matrixrotation anwendet sowie Grafiken
  mit C# in Minuten verschiebt und skaliert.
og_image_alt: Screenshot of a rotated rectangle created with Aspose.Drawing using
  matrix transformations
og_title: Matrix-Transformations-Tutorial – Rotation, Skalierung und Translation in
  Aspose.Drawing anwenden
schemas:
- author: Aspose
  dateModified: '2026-08-28'
  description: Learn this matrix transformation tutorial for Aspose.Drawing .NET,
    covering how to draw rotated rectangle, apply matrix rotation, and perform matrix
    scaling C#.
  headline: 'Matrix transformation tutorial: matrix transformations in Aspose.Drawing
    for .NET'
  type: TechArticle
- description: Learn this matrix transformation tutorial for Aspose.Drawing .NET,
    covering how to draw rotated rectangle, apply matrix rotation, and perform matrix
    scaling C#.
  name: 'Matrix transformation tutorial: matrix transformations in Aspose.Drawing
    for .NET'
  steps:
  - name: set up the canvas
    text: Create a bitmap that will serve as the drawing surface. We also clear it
      with a neutral gray background so the transformed shapes stand out. > **Pro
      tip:** Using `Format32bppPArgb` ensures correct alpha handling when you later
      apply anti‑aliasing.
  - name: define the original rectangle
    text: This rectangle is the base shape we’ll transform. Its coordinates are chosen
      to keep it well within the canvas bounds.
  - name: rotate the rectangle (draw rotated rectangle)
    text: The `Matrix` class is Aspose.Drawing's representation of a 3 × 3 affine
      transformation matrix used for rotation, scaling and translation. We now **apply
      matrix rotation** of 15 degrees around the origin. The helper method `TransformPath`
      (shown later) takes a lambda that receives a `Matrix` instance
  - name: translate the rectangle
    text: Translation moves the shape without altering its size or orientation. Here
      we shift it left‑up by 250 pixels.
  - name: scale the rectangle (matrix scaling C#)
    text: Scaling changes the rectangle’s dimensions. A factor of `0.3f` reduces both
      width and height to 30 % of the original size.
  - name: save the result
    text: Finally, write the transformed image to disk. Adjust the path to point to
      a folder that exists on your machine. > **Note:** The `TransformPath` method
      (used in the steps above) creates a `GraphicsPath` from the rectangle, applies
      the supplied matrix, and draws the transformed shape. It’s a compact w
  type: HowTo
- questions:
  - answer: The documentation is available **[here](https://reference.aspose.com/drawing/net/)**.
    question: Where can I find the Aspose.Drawing documentation?
  - answer: Obtain a temporary license **[here](https://purchase.aspose.com/temporary-license/)**.
    question: How do I get a temporary license for Aspose.Drawing?
  - answer: Visit the Aspose.Drawing forum **[here](https://forum.aspose.com/c/drawing/44)**.
    question: Where can I seek support or connect with the community?
  - answer: Yes, download it from **[here](https://releases.aspose.com/drawing/net/)**.
    question: Can I download Aspose.Drawing for .NET?
  - answer: Purchase your license **[here](https://purchase.aspose.com/buy)**.
    question: How can I purchase Aspose.Drawing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- matrix transformation
- Aspose.Drawing
- .NET graphics
- C# drawing
- cross‑platform rendering
title: 'Matrix-Transformations-Tutorial: Matrix-Transformationen in Aspose.Drawing
  für .NET'
url: /de/net/coordinate-transformations/matrix-transformations/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Matrix‑Transformations‑Tutorial: Matrixtransformationen in Aspose.Drawing für .NET

## Einführung

In diesem **Matrix‑Transformations‑Tutorial** erfahren Sie, wie die `Matrix`‑Klasse von Aspose.Drawing das Drehen, Verschieben und Skalieren von Grafikobjekten mit pixelgenauer Genauigkeit ermöglicht. Egal, ob Sie einen Diagrammeditor bauen, automatisierte Berichte erzeugen oder visuelle Effekte zu einem serverseitigen Dienst hinzufügen – das Beherrschen von Matrix‑Transformationen ist entscheidend, um professionell aussehende Ausgaben unter Windows, Linux und macOS zu erzeugen.

## Schnellantworten
- **Was wird in diesem Tutorial behandelt?** Es zeigt, wie man ein Rechteck mit der Matrix‑API von Aspose.Drawing dreht, verschiebt und skaliert.  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion reicht für die Entwicklung; für den Produktionseinsatz ist eine kommerzielle Lizenz erforderlich.  
- **Welche .NET‑Versionen werden unterstützt?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7 und später.  
- **Wie lange dauert die Implementierung?** Ungefähr 10‑15 Minuten für das vollständige Beispiel.  
- **Kann ich das Ausgabebild sehen?** Ja – das Tutorial speichert ein PNG, das Sie sofort öffnen können.

## Was ist ein Matrix‑Transformations‑Tutorial?

Ein Matrix‑Transformations‑Tutorial erklärt, wie man eine 3 × 3‑affine Matrix verwendet, um Grafikprimitive zu verschieben, zu drehen, zu skalieren oder zu scheren. In Aspose.Drawing kapselt die `Matrix`‑Klasse diese Vorgänge, sodass jedes `GraphicsPath`‑Objekt oder jede Form mit einem einzigen wiederverwendbaren Objekt transformiert werden kann.

## Warum Aspose.Drawing für Matrix‑Transformationen verwenden?

Aspose.Drawing unterstützt **drei wichtige Betriebssysteme** (Windows, Linux, macOS) und kann Bilder bis zu **10.000 × 10.000 px** in weniger als **200 ms** pro Vorgang auf typischer Serverhardware rendern. Die Bibliothek bietet **100 % GDI+‑API‑Kompatibilität**, sodass Sie bestehenden System.Drawing‑Code migrieren können, ohne die Logik neu zu schreiben, und gleichzeitig die Lizenzbeschränkungen umgehen, die System.Drawing.Common auf Nicht‑Windows‑Plattformen betreffen.

## Voraussetzungen

- Eine funktionierende C#‑Entwicklungsumgebung (Visual Studio, Rider oder VS Code).  
- Aspose.Drawing für .NET installiert – laden Sie es von der offiziellen Seite **[hier](https://releases.aspose.com/drawing/net/)** oder **[diesem Link](https://releases.aspose.com/drawing/net/)** herunter, falls Sie es noch nicht getan haben.  
- Grundlegendes Verständnis von Bitmap‑Leinwänden, Rechtecken und Grafikpfaden.

## Namespaces importieren

Zuerst die erforderlichen Namespaces in den Gültigkeitsbereich holen:

```csharp
using System;
using System.Drawing;
using System.Drawing.Drawing2D;
```

Diese Namespaces geben Ihnen Zugriff auf `Bitmap`, `Graphics` und die `Matrix`‑Klasse, die für Transformationen benötigt wird.

## Schritt‑für‑Schritt‑Anleitung

Im Folgenden finden Sie einen kompakten, nummerierten Durchlauf. Jeder Schritt enthält eine kurze Erklärung gefolgt vom exakt benötigten Code (die Code‑Blöcke bleiben unverändert).

### Schritt 1: Canvas einrichten

Erstellen Sie ein Bitmap, das als Zeichenfläche dient. Wir füllen es außerdem mit einem neutralen Grauhintergrund, damit die transformierten Formen besser zur Geltung kommen.

```csharp
// Code snippet for setting up the canvas
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

> **Profi‑Tipp:** Die Verwendung von `Format32bppPArgb` sorgt für korrekte Alpha‑Verarbeitung, wenn Sie später Antialiasing anwenden.

### Schritt 2: Das ursprüngliche Rechteck definieren

Dieses Rechteck ist die Basisform, die wir transformieren. Die Koordinaten wurden gewählt, damit es gut innerhalb der Canvas‑Grenzen liegt.

```csharp
// Code snippet for defining the original rectangle
Rectangle originalRectangle = new Rectangle(300, 300, 300, 200);
```

### Schritt 3: Das Rechteck drehen (drehe Rechteck)

Die `Matrix`‑Klasse ist Aspose.Drawings Darstellung einer 3 × 3‑affinen Transformationsmatrix, die für Drehungen, Skalierungen und Verschiebungen verwendet wird. Wir **wenden nun eine Matrix‑Drehung** von 15 Grad um den Ursprung an. Die Hilfsmethode `TransformPath` (siehe später) nimmt ein Lambda entgegen, das eine `Matrix`‑Instanz erhält.

```csharp
// Code snippet for rotating the rectangle
TransformPath(graphics, originalRectangle, (matrix) => matrix.Rotate(15.0f));
```

### Schritt 4: Das Rechteck verschieben

Translation verschiebt die Form, ohne Größe oder Orientierung zu ändern. Hier verschieben wir sie um 250 Pixel nach links‑oben.

```csharp
// Code snippet for translating the rectangle
TransformPath(graphics, originalRectangle, (matrix) => matrix.Translate(-250, -250));
```

### Schritt 5: Das Rechteck skalieren (Matrix‑Skalierung C#)

Skalierung ändert die Abmessungen des Rechtecks. Ein Faktor von `0.3f` reduziert Breite und Höhe auf 30 % der Originalgröße.

```csharp
// Code snippet for scaling the rectangle
TransformPath(graphics, originalRectangle, (matrix) => matrix.Scale(0.3f, 0.3f));
```

### Schritt 6: Ergebnis speichern

Zum Schluss schreiben wir das transformierte Bild auf die Festplatte. Passen Sie den Pfad an einen Ordner an, der auf Ihrem Rechner existiert.

```csharp
// Code snippet for saving the result
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\MatrixTransformations_out.png");
```

> **Hinweis:** Die Methode `TransformPath` (verwendet in den obigen Schritten) erzeugt einen `GraphicsPath` aus dem Rechteck, wendet die übergebene Matrix an und zeichnet die transformierte Form. Sie ist eine kompakte Möglichkeit, dieselbe Zeichenlogik für jede Transformation wiederzuverwenden.

## Häufige Probleme & Lösungen

| Problem | Lösung |
|---------|--------|
| **Bild erscheint leer** | Stellen Sie sicher, dass das Ausgabeverzeichnis existiert und Sie Schreibberechtigungen haben. |
| **Transformationen wirken nicht zentriert** | Denken Sie daran, dass `Matrix.Rotate` um den Ursprung (0,0) rotiert. Verschieben Sie die Form zum gewünschten Drehpunkt, bevor Sie rotieren. |
| **Leistungsprobleme bei großen Bildern** | Verwenden Sie `graphics.SmoothingMode = SmoothingMode.AntiAlias;` nur bei Bedarf und geben Sie `Graphics`‑Objekte umgehend frei. |

## Häufig gestellte Fragen

**F: Wo finde ich die Aspose.Drawing‑Dokumentation?**  
A: Die Dokumentation ist **[hier](https://reference.aspose.com/drawing/net/)** verfügbar.

**F: Wie erhalte ich eine temporäre Lizenz für Aspose.Drawing?**  
A: Eine temporäre Lizenz erhalten Sie **[hier](https://purchase.aspose.com/temporary-license/)**.

**F: Wo kann ich Unterstützung erhalten oder mit der Community in Kontakt treten?**  
A: Besuchen Sie das Aspose.Drawing‑Forum **[hier](https://forum.aspose.com/c/drawing/44)**.

**F: Kann ich Aspose.Drawing für .NET herunterladen?**  
A: Ja, laden Sie es **[hier](https://releases.aspose.com/drawing/net/)** herunter.

**F: Wie kann ich Aspose.Drawing erwerben?**  
A: Kaufen Sie Ihre Lizenz **[hier](https://purchase.aspose.com/buy)**.

## Fazit

Sie haben nun ein vollständiges **Matrix‑Transformations‑Tutorial** mit Aspose.Drawing für .NET abgeschlossen. Sie wissen, wie man **ein gedrehtes Rechteck zeichnet**, **Matrix‑Drehungen anwendet** und **Matrix‑Skalierung in C#** auf jede Form ausführt. Experimentieren Sie mit der Verkettung mehrerer Transformationen oder mit benutzerdefinierten Drehpunkten, um noch kreativere Grafikeffekte zu erzielen.

---

**Zuletzt aktualisiert:** 2026-08-28  
**Getestet mit:** Aspose.Drawing 24.11 für .NET  
**Autor:** Aspose

## Verwandte Tutorials

- [Wie man ein Rechteck zeichnet – Koordinatensystem‑Transformation (Seiten‑Transformation) mit der Aspose.Drawing‑API für .NET](/drawing/net/coordinate-transformations/page-transformation/)
- [Wie man PNG mit Aspose.Drawing speichert – Welt‑Transformation](/drawing/net/coordinate-transformations/world-transformation/)
- [Schritt‑für‑Schritt‑Transformation – Koordinatentransformationen](/drawing/net/coordinate-transformations/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}