---
date: 2026-05-24
description: Erfahren Sie, wie Sie die Einheit in Aspose.Drawing für .NET festlegen,
  Grafik‑Einheiten einfach konvertieren und präzise Messungen für die Grafikdarstellung
  meistern.
keywords:
- how to set unit
- convert graphics units
- Aspose.Drawing units of measure
linktitle: Maßeinheiten in Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-24'
  description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  headline: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  type: TechArticle
- description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  name: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  steps:
  - name: Create a Bitmap
    text: The `Bitmap` class represents an in‑memory image that serves as a drawing
      canvas.
  - name: Create a Graphics Object
    text: '`Graphics` provides drawing methods for rendering shapes and text onto
      a `Bitmap`.'
  - name: Set Page Unit to Points
    text: '`PageUnit` is an enumeration that specifies the unit of measure for page
      coordinates. `PageUnit.Point` defines points as the unit of measure (1 point
      = 1/72 inch). This setting applies to all subsequent drawing calls.'
  - name: Draw a Rectangle in Points
    text: When you draw a rectangle after setting the unit, the dimensions you specify
      are interpreted as points, ensuring precise sizing.
  - name: Set Page Unit to Millimeters
    text: Assign `PageUnit.Millimeter` to the `Graphics` object; all coordinates now
      map to the metric system.
  - name: Draw a Rectangle in Millimeters
    text: The rectangle’s width and height are now expressed in millimeters, making
      it easy to align with physical measurements and ensuring that printed output
      matches real‑world sizes.
  - name: Set Page Unit to Inches
    text: '`PageUnit.Inch` changes the coordinate system so that 1 unit equals 1 inch,
      providing a straightforward way to size elements for print‑oriented layouts.
      CODE_BLOCK_PLACEHOLDER_10_END'
  - name: Draw a Rectangle in Inches
    text: Now any shape you draw uses inches as its measurement base, which is ideal
      for print layouts and for communicating dimensions to stakeholders accustomed
      to imperial units. CODE_BLOCK_PLACEHOLDER_11_END
  type: HowTo
- questions:
  - answer: Call `graphics.PageUnit = PageUnit.Point` (or `.Millimeter`, `.Inch`)
      on the `Graphics` object.
    question: What is the primary way to change units?
  - answer: Points.
    question: Which unit equals 1/72 inch?
  - answer: 25.4 mm = 1 inch.
    question: How many millimeters are in an inch?
  - answer: No, the Aspose.Drawing core library provides all unit constants.
    question: Do I need extra libraries to use units?
  - answer: Set the unit once per `Graphics` instance; draw everything using that
      unit for consistency.
    question: Can I mix units in one image?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Wie man die Einheit in Aspose.Drawing für .NET festlegt – Maßeinheiten
url: /de/net/coordinate-transformations/units-of-measure/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Wie man Einheiten in Aspose.Drawing für .NET festlegt – Maßeinheiten

## Einleitung

Willkommen in der Welt von Aspose.Drawing für .NET, wo Präzision und Flexibilität bei der Grafikmanipulation zusammentreffen. In diesem Tutorial entdecken Sie **wie man Einheiten festlegt** für Ihre Zeichnungen, lernen **Grafik‑Einheiten zu konvertieren** zwischen Punkten, Millimetern und Zoll und sehen Praxisbeispiele, die Ihre Bilder pixel‑perfekt machen. Egal, ob Sie Berichte, Miniaturansichten oder benutzerdefinierte Diagramme erstellen, das Beherrschen von Maßeinheiten ist entscheidend für ein konsistentes Rendering auf allen Geräten.

## Schnelle Antworten
- **Was ist die primäre Methode, um Einheiten zu ändern?** Rufen Sie `graphics.PageUnit = PageUnit.Point` (oder `.Millimeter`, `.Inch`) auf dem `Graphics`‑Objekt auf.  
- **Welche Einheit entspricht 1/72 Zoll?** Punkte.  
- **Wie viele Millimeter sind in einem Zoll?** 25,4 mm = 1 Zoll.  
- **Benötige ich zusätzliche Bibliotheken, um Einheiten zu verwenden?** Nein, die Aspose.Drawing‑Kernbibliothek stellt alle Einheit‑Konstanten bereit.  
- **Kann ich Einheiten in einem Bild mischen?** Setzen Sie die Einheit einmal pro `Graphics`‑Instanz; zeichnen Sie alles mit dieser Einheit für Konsistenz.

## Voraussetzungen

Bevor wir in das Tutorial eintauchen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllt haben:

- Aspose.Drawing für .NET: Stellen Sie sicher, dass die Bibliothek installiert ist. Sie können sie [hier](https://releases.aspose.com/drawing/net/) herunterladen.
- Dokumentverzeichnis: Haben Sie ein festgelegtes Verzeichnis, in dem Sie Ihre erstellten Dokumente speichern möchten.
- Grundkenntnisse in C#: Ein grundlegendes Verständnis von C# wird empfohlen, um das Beste aus diesem Leitfaden herauszuholen.

## Namespaces importieren

Bevor wir beginnen, importieren wir die notwendigen Namespaces, um Aspose.Drawing effektiv zu nutzen:

```csharp
using System.Drawing;
```

Nun zerlegen wir jedes Beispiel in mehrere Schritte:

## Wie man die Einheit auf Punkte setzt?

Die Klasse `Bitmap` repräsentiert ein Bild im Speicher, das als Zeichenfläche dient. Laden Sie Ihr Bitmap, erstellen Sie ein `Graphics`‑Objekt und setzen Sie die Seiteneinheit auf Punkte — das weist Aspose.Drawing an, alle Koordinaten als 1/72 Zoll‑Werte zu interpretieren. Die Verwendung von Punkten gibt Ihnen feinkörnige Kontrolle für druckfertige Grafiken und ermöglicht die Angabe von Linienstärken mit hoher Präzision.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Schritt 1: Bitmap erstellen  
Die Klasse `Bitmap` repräsentiert ein Bild im Speicher, das als Zeichenfläche dient.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### Schritt 2: Graphics‑Objekt erstellen  
`Graphics` bietet Zeichenmethoden zum Rendern von Formen und Text auf ein `Bitmap`.

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

### Schritt 3: Seiteneinheit auf Punkte setzen  
`PageUnit` ist eine Aufzählung, die die Maßeinheit für Seitenkoordinaten festlegt. `PageUnit.Point` definiert Punkte als Maßeinheit (1 Punkt = 1/72 Zoll). Diese Einstellung gilt für alle nachfolgenden Zeichenaufrufe.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

### Schritt 4: Rechteck in Punkten zeichnen  
Wenn Sie ein Rechteck nach dem Setzen der Einheit zeichnen, werden die angegebenen Abmessungen als Punkte interpretiert, was eine präzise Größe gewährleistet.

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

## Wie man die Einheit auf Millimeter setzt?

`PageUnit` ist eine Aufzählung, die die Maßeinheit für Seitenkoordinaten festlegt. Das Umschalten auf Millimeter ist hilfreich, wenn Sie metrische Abmessungen benötigen, zum Beispiel beim Erstellen von technischen Diagrammen. Aspose.Drawing behandelt 1 mm als 1/25,4 Zoll, sodass Sie Grafiken an physikalischen Messungen ausrichten können, die in der Fertigung und technischen Dokumentation verwendet werden.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

### Schritt 1: Seiteneinheit auf Millimeter setzen  
Weisen Sie dem `Graphics`‑Objekt `PageUnit.Millimeter` zu; alle Koordinaten werden nun dem metrischen System zugeordnet.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### Schritt 2: Rechteck in Millimetern zeichnen  
Die Breite und Höhe des Rechtecks werden nun in Millimetern angegeben, was die Ausrichtung an physischen Messungen erleichtert und sicherstellt, dass die Druckausgabe den realen Größen entspricht.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## Wie man die Einheit auf Zoll setzt?

`Graphics` bietet Zeichenmethoden zum Rendern von Formen und Text auf ein `Bitmap`. Zoll sind die Standardeinheit für viele US‑basierte Design‑Tools. Das Setzen der Einheit auf Zoll ermöglicht es Ihnen, in vertrauten Begriffen zu denken, wenn Sie UI‑Elemente anordnen, und vereinfacht den Übergang vom Bildschirmdesign zum Druck, wo Zoll häufig verwendet werden.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

### Schritt 1: Seiteneinheit auf Zoll setzen  
`PageUnit.Inch` ändert das Koordinatensystem, sodass 1 Einheit 1 Zoll entspricht, und bietet eine einfache Möglichkeit, Elemente für druckorientierte Layouts zu dimensionieren.

CODE_BLOCK_PLACEHOLDER_10_END

### Schritt 2: Rechteck in Zoll zeichnen  
Jetzt verwendet jede von Ihnen gezeichnete Form Zoll als Messgrundlage, was ideal für Drucklayouts und für die Kommunikation von Abmessungen an Stakeholder ist, die an imperiale Einheiten gewöhnt sind.

CODE_BLOCK_PLACEHOLDER_11_END

## Ergebnis speichern

Nachdem Sie die Beispiele abgeschlossen haben, speichern Sie das resultierende Bild in Ihrem Dokumentverzeichnis. Die Methode `Bitmap.Save` schreibt die Datei im von Ihnen angegebenen Format (PNG, JPEG usw.).

CODE_BLOCK_PLACEHOLDER_12_END

Nun haben Sie die verschiedenen Maßeinheiten in Aspose.Drawing für .NET erfolgreich gemeistert und eine visuelle Darstellung von Rechtecken mit Punkten, Millimetern und Zoll erstellt.

## Warum das Einheitssystem von Aspose.Drawing verwenden?

Aspose.Drawing unterstützt **über 30 Bildformate** und kann Bilder bis zu **5000 × 5000 Pixel** verarbeiten, ohne die gesamte Datei in den Speicher zu laden, und liefert hohe Leistung für die großflächige Grafikgenerierung. Durch das explizite Setzen der Einheit beseitigen Sie Rätselraten, reduzieren Konvertierungsfehler und stellen sicher, dass Ihre Ausgabe exakt den physischen Abmessungen auf allen Plattformen entspricht.

## Häufige Probleme und Lösungen

- **Unerwartete Größe nach dem Speichern** – Stellen Sie sicher, dass Sie `graphics.PageUnit` **vor** allen Zeichenaufrufen setzen; das spätere Ändern der Einheit ändert bereits gezeichnete Formen nicht retroaktiv.  
- **Unscharfe Ausgabe auf hochauflösenden Bildschirmen** – Erhöhen Sie die Auflösung des Bitmaps (z. B. `new Bitmap(width, height, 300)`), um die Ziel‑DPI zu erreichen.  
- **Gemischte Einheiten in einem Bild** – Erstellen Sie separate `Graphics`‑Instanzen für jede Einheit oder führen Sie vor dem Zeichnen eine manuelle Umrechnung durch.

## Häufig gestellte Fragen

### Q1: Kann ich Aspose.Drawing für .NET mit anderen .NET‑Frameworks verwenden?
A1: Ja, Aspose.Drawing ist mit verschiedenen .NET‑Frameworks kompatibel und bietet Flexibilität in Ihrer Entwicklungsumgebung.

### Q2: Gibt es eine kostenlose Testversion?
A2: Ja, Sie können Aspose.Drawing mit einer kostenlosen Testversion [hier](https://releases.aspose.com/) erkunden.

### Q3: Wie erhalte ich Support für Aspose.Drawing für .NET?
A3: Besuchen Sie das [Aspose.Drawing‑Forum](https://forum.aspose.com/c/drawing/44) für Community‑Support und Diskussionen.

### Q4: Kann ich eine temporäre Lizenz für kurzfristige Projekte erwerben?
A4: Ja, Sie können eine temporäre Lizenz [hier](https://purchase.aspose.com/temporary-license/) erhalten.

### Q5: Wo finde ich ausführliche Dokumentation für Aspose.Drawing?
A5: Die umfassende Dokumentation ist [hier](https://reference.aspose.com/drawing/net/) verfügbar.

---

**Zuletzt aktualisiert:** 2026-05-24  
**Getestet mit:** Aspose.Drawing 24.11 für .NET  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Verwandte Tutorials

- [Koordinatensystem-Transformation – Seiten-Transformation in Aspose.Drawing für .NET](/drawing/net/coordinate-transformations/page-transformation/)
- [Matrix-Transformations‑Tutorial: Matrix‑Transformationen in Aspose.Drawing für .NET](/drawing/net/coordinate-transformations/matrix-transformations/)
- [Wie man Transformation anwendet: Lokale Transformation in Aspose.Drawing für .NET](/drawing/net/coordinate-transformations/local-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}