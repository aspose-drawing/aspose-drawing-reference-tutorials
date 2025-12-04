---
title: Füllen von Regionen in Aspose.Drawing
linktitle: Füllen von Regionen in Aspose.Drawing
second_title: Aspose.Drawing .NET API – Alternative zu System.Drawing.Common
description: Erfahren Sie in diesem Schritt-für-Schritt-Tutorial, wie Sie Bereiche in Aspose.Drawing für .NET füllen. Verbessern Sie mühelos Ihre Fähigkeiten im Bereich Grafikdesign.
weight: 20
url: /de/net/lines-curves-and-shapes/fill-region/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Füllen von Regionen in Aspose.Drawing

## Einführung

Beim Erstellen optisch ansprechender Grafiken müssen Bereiche häufig mit Farben, Mustern oder Farbverläufen gefüllt werden. Aspose.Drawing für .NET bietet leistungsstarke Tools, um dies effizient zu erreichen. In diesem Tutorial befassen wir uns mit dem Prozess des Füllens von Regionen mithilfe von Aspose.Drawing, einer vielseitigen Bibliothek, die grafische Vorgänge in .NET-Anwendungen vereinfacht.

## Voraussetzungen

Bevor wir beginnen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

1.  Aspose.Drawing-Bibliothek: Laden Sie die Aspose.Drawing-Bibliothek herunter und installieren Sie sie. Hier finden Sie die Bibliothek und ihre Dokumentation[Hier](https://reference.aspose.com/drawing/net/).

2. Entwicklungsumgebung: Richten Sie eine .NET-Entwicklungsumgebung wie Visual Studio ein, um Aspose.Drawing in Ihre Projekte zu integrieren.

## Namespaces importieren

Beginnen Sie mit dem Importieren der erforderlichen Namespaces in Ihr Projekt. Diese Namespaces bieten Zugriff auf die Klassen und Methoden, die für die Arbeit mit Aspose.Drawing erforderlich sind.

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```


Lassen Sie uns nun den Beispielcode für ein klares und umfassendes Verständnis in mehrere Schritte aufteilen.

## Schritt 1: Erstellen Sie ein Bitmap- und Grafikobjekt

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

In diesem Schritt initialisieren wir eine neue Bitmap und ein Grafikobjekt, um darauf zu zeichnen.

## Schritt 2: Definieren Sie einen GraphicsPath und erstellen Sie eine Region

```csharp
GraphicsPath path = new GraphicsPath();
path.AddPolygon(new Point[] { new Point(100, 400), new Point(500, 100), new Point(900, 400), new Point(500, 700) });
Region region = new Region(path);
```

Definieren Sie einen Grafikpfad, indem Sie ein Polygon mit einer Reihe von Punkten angeben. Erstellen Sie mithilfe dieses Pfads eine Region.

## Schritt 3: Eine innere Region ausschließen

```csharp
GraphicsPath innerPath = new GraphicsPath();
innerPath.AddRectangle(new Rectangle(300, 300, 400, 200));
region.Exclude(innerPath);
```

Erstellen Sie einen weiteren Grafikpfad, der ein inneres Rechteck darstellt, und schließen Sie es aus dem Hauptbereich aus.

## Schritt 4: Wählen Sie einen Pinsel und füllen Sie den Bereich

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Blue));
graphics.FillRegion(brush, region);
```

Wählen Sie einen Pinsel aus (in diesem Fall eine einfarbige blaue Farbe) und füllen Sie den zuvor definierten Bereich mit dem ausgewählten Pinsel.

## Schritt 5: Speichern Sie das resultierende Bild

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\FillRegion_out.png");
```

Speichern Sie das endgültige Bild im gewünschten Verzeichnis.

## Abschluss

Das Füllen von Bereichen in Aspose.Drawing für .NET ist ein unkomplizierter Prozess, der Ihnen die Flexibilität bietet, komplexe und optisch ansprechende Grafiken zu erstellen. Experimentieren Sie mit verschiedenen Formen, Farben und Mustern, um Ihrer Kreativität freien Lauf zu lassen.

## FAQs

### F1: Kann ich Aspose.Drawing für kommerzielle Projekte verwenden?

 A1: Ja, Aspose.Drawing kann sowohl für persönliche als auch für kommerzielle Projekte verwendet werden. Einzelheiten zur Lizenzierung finden Sie unter[Hier](https://purchase.aspose.com/buy).

### F2: Gibt es eine kostenlose Testversion?

 A2: Ja, Sie können auf eine kostenlose Testversion zugreifen[Hier](https://releases.aspose.com/).

### F3: Wie kann ich Unterstützung für Aspose.Drawing erhalten?

 A3: Besuchen Sie die[Aspose.Drawing-Forum](https://forum.aspose.com/c/drawing/44) um Unterstützung von der Community und Experten zu erhalten.

### F4: Kann ich mit Aspose.Drawing dynamische Bilder generieren?

A4: Auf jeden Fall. Mit Aspose.Drawing können Sie Bilder in Ihren .NET-Anwendungen dynamisch erstellen und bearbeiten.

### F5: Sind temporäre Lizenzen verfügbar?

 A5: Ja, temporäre Lizenzen können erworben werden[Hier](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
