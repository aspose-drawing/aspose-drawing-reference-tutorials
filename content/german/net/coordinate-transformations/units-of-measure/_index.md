---
title: Maßeinheiten in Aspose.Drawing für .NET
linktitle: Maßeinheiten in Aspose.Drawing
second_title: Aspose.Drawing .NET API – Alternative zu System.Drawing.Common
description: Entdecken Sie in diesem ausführlichen Tutorial die Vielseitigkeit von Aspose.Drawing für .NET und lernen Sie Maßeinheiten für Präzisionsgrafiken kennen.
type: docs
weight: 14
url: /de/net/coordinate-transformations/units-of-measure/
---
## Einführung

Willkommen in der Welt von Aspose.Drawing für .NET, wo Präzision und Flexibilität bei der grafischen Bearbeitung aufeinandertreffen. In diesem Tutorial befassen wir uns mit den Feinheiten der Maßeinheiten in Aspose.Drawing und geben Ihnen eine Schritt-für-Schritt-Anleitung, wie Sie die Leistungsfähigkeit dieser bemerkenswerten Bibliothek nutzen können.

## Voraussetzungen

Bevor wir uns mit dem Tutorial befassen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

-  Aspose.Drawing für .NET: Stellen Sie sicher, dass Sie die Bibliothek installiert haben. Sie können es herunterladen[Hier](https://releases.aspose.com/drawing/net/).

- Dokumentenverzeichnis: Legen Sie ein bestimmtes Verzeichnis fest, in dem Sie Ihre erstellten Dokumente speichern möchten.

- Grundlegende C#-Kenntnisse: Um dieses Handbuch optimal nutzen zu können, werden grundlegende Kenntnisse von C# empfohlen.

## Namespaces importieren

Bevor wir beginnen, importieren wir die notwendigen Namespaces, um Aspose.Drawing effektiv nutzen zu können:

```csharp
using System.Drawing;
```

Lassen Sie uns nun jedes Beispiel in mehrere Schritte unterteilen:

## Punkte als Maßeinheiten

1. Erstellen Sie eine Bitmap: Initialisieren Sie eine Bitmap mit einer angegebenen Breite und Höhe.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

2. Grafiken erstellen: Generieren Sie ein Grafikobjekt aus der Bitmap, um darauf zu zeichnen.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

3. Stellen Sie die Seiteneinheit auf Punkte ein: Definieren Sie Punkte als Maßeinheit (1 Punkt = 1/72 Zoll).

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

4. Rechteck zeichnen: Zeichnen Sie ein Rechteck mit Punkten als Einheit.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

## Millimeter als Maßeinheiten

1. Stellen Sie die Seiteneinheit auf Millimeter ein: Ändern Sie die Maßeinheit in Millimeter (1 mm = 1/25,4 Zoll).

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

2. Rechteck in Millimetern zeichnen: Zeichnen Sie ein weiteres Rechteck mit der Einheit Millimeter.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

## Zoll als Maßeinheiten

1. Seiteneinheit auf Zoll einstellen: Ändern Sie die Maßeinheit auf Zoll.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

2. Rechteck in Zoll zeichnen: Zeichnen Sie ein Rechteck mit Zoll als Einheit.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## Speichern Sie das Ergebnis

Speichern Sie nach Abschluss der Beispiele das resultierende Bild in Ihrem Dokumentverzeichnis:

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

Jetzt haben Sie erfolgreich durch die verschiedenen Maßeinheiten in Aspose.Drawing für .NET navigiert und eine visuelle Darstellung von Rechtecken mithilfe von Punkten, Millimetern und Zoll erstellt.

## Abschluss

In diesem Tutorial haben wir untersucht, wie Aspose.Drawing für .NET mit verschiedenen Maßeinheiten umgeht. Durch die Bearbeitung von Punkten, Millimetern und Zoll können Sie Präzision und Anpassungsfähigkeit in Ihren grafischen Kreationen erreichen. Experimentieren Sie mit diesen Konzepten, um das volle Potenzial von Aspose.Drawing auszuschöpfen.

## FAQs

### F1: Kann ich Aspose.Drawing für .NET mit anderen .NET-Frameworks verwenden?

A1: Ja, Aspose.Drawing ist mit verschiedenen .NET-Frameworks kompatibel und bietet so Flexibilität in Ihrer Entwicklungsumgebung.

### F2: Gibt es eine kostenlose Testversion?

 A2: Ja, Sie können Aspose.Drawing mit einer kostenlosen Testversion erkunden[Hier](https://releases.aspose.com/).

### F3: Wie erhalte ich Unterstützung für Aspose.Drawing für .NET?

 A3: Besuchen Sie die[Aspose.Drawing Forum](https://forum.aspose.com/c/diagram/17) für Community-Unterstützung und Diskussionen.

### F4: Kann ich eine temporäre Lizenz für kurzfristige Projekte erwerben?

 A4: Ja, Sie können eine temporäre Lizenz erhalten[Hier](https://purchase.aspose.com/temporary-license/).

### F5: Wo finde ich eine ausführliche Dokumentation zu Aspose.Drawing?

 A5: Die umfassende Dokumentation ist vorhanden[Hier](https://reference.aspose.com/drawing/net/).