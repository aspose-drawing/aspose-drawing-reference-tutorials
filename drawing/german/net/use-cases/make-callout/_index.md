---
title: Callouts in Aspose.Drawing erstellen
linktitle: Callouts in Aspose.Drawing erstellen
second_title: Aspose.Drawing .NET API – Alternative zu System.Drawing.Common
description: Verbessern Sie Ihre Dokumentillustrationen mit Aspose.Drawing für .NET! Erfahren Sie Schritt für Schritt, wie Sie Beschriftungen für klarere und informativere Bilder hinzufügen.
weight: 10
url: /de/net/use-cases/make-callout/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Callouts in Aspose.Drawing erstellen

## Einführung
Willkommen zu unserer Schritt-für-Schritt-Anleitung zum Erstellen von Callouts in Aspose.Drawing für .NET! Wenn Sie Ihre Dokumentillustrationen mit Beschriftungen aufwerten möchten, sind Sie hier richtig. In diesem Tutorial unterteilen wir den Prozess mithilfe der Aspose.Drawing-Bibliothek in überschaubare Schritte.
## Voraussetzungen
Bevor Sie mit dem Tutorial beginnen, stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllen:
- Grundkenntnisse der Programmiersprache C#.
-  Aspose.Drawing-Bibliothek installiert. Sie können es herunterladen[Hier](https://releases.aspose.com/drawing/net/).
- Ein Dokument oder Bild, dem Sie Beschriftungen hinzufügen möchten.
## Namespaces importieren
Stellen Sie sicher, dass in Ihrem Projekt die erforderlichen Namespaces enthalten sind:
```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```
## Schritt 1: Laden Sie das Bild
 Laden Sie zunächst das Bild an der Stelle, an der Sie Beschriftungen hinzufügen möchten. Ersetzen`"Your Document Directory"` Und`"gears.png"` mit Ihrem tatsächlichen Verzeichnis und Bilddateinamen.
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Ihr Code hier
}
```
## Schritt 2: Grafikobjekt erstellen
 Ein ... kreieren`Graphics` Objekt aus dem Bild, um Zeichenvorgänge auszuführen.
```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```
## Schritt 3: Definieren Sie die Callout-Positionen
Definieren Sie die Start- und Endpunkte für jedes Callout sowie den Callout-Wert und die Einheit.
```csharp
PointF startAnchor1 = new PointF(107, 55);
PointF endAnchor1 = new PointF(179, 5);
int value1 = 74;
string unit1 = "mm";
PointF startAnchor2 = new PointF(111, 146);
PointF endAnchor2 = new PointF(29, 180);
int value2 = 28;
string unit2 = "mm";
```
## Schritt 4: Callouts zeichnen
 Implementieren Sie die`DrawCallOut` Methode zum Zeichnen von Beschriftungen auf dem Bild.
```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```
## Schritt 5: Speichern Sie das Bild
Speichern Sie das Bild mit Beschriftungen im gewünschten Verzeichnis.
```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```
## Callout-Quellcode zeichnen
```csharp
void DrawCallOut(Graphics graphic, PointF startAnchor, PointF endAnchor, int value, string unit)
            {
                Pen pen = new Pen(Color.DarkGray, 1);
                Font font = new Font("Arial", 10, FontStyle.Bold);
                string outputValue = $"{value} {unit}";
                var textSize = graphic.MeasureString(outputValue, font);
                int diameterSymbolSize = 12;
                int spaceSize = 3;
                textSize.Width += diameterSymbolSize + spaceSize;
                float callOutMiddleX = endAnchor.X > startAnchor.X ? endAnchor.X - textSize.Width : endAnchor.X + textSize.Width;
                float callOutMiddleY = endAnchor.Y > startAnchor.Y ? endAnchor.Y - textSize.Height : endAnchor.Y + textSize.Height;
                graphic.DrawLine(pen, startAnchor.X, startAnchor.Y, callOutMiddleX, callOutMiddleY);
                float textAnchorX = Math.Min(callOutMiddleX, endAnchor.X);
                float textAnchorY = callOutMiddleY;
                graphic.DrawLine(pen, callOutMiddleX, callOutMiddleY, textAnchorX == callOutMiddleX ? textAnchorX + textSize.Width : textAnchorX, callOutMiddleY);
                graphic.DrawEllipse(pen, new Rectangle((int)textAnchorX + spaceSize, (int)(textAnchorY - textSize.Height) + spaceSize, 10, 10));
                graphic.DrawLine(pen, (int)textAnchorX + 1, (int)textAnchorY - 1, (int)textAnchorX + diameterSymbolSize + 2, (int)textAnchorY - diameterSymbolSize - 2);
                SolidBrush brush = new SolidBrush(Color.DarkGray);
                graphic.DrawString(outputValue, font, brush, (int)textAnchorX + diameterSymbolSize + spaceSize, (int)(textAnchorY - textSize.Height));
            }
```
## Abschluss

Glückwunsch! Sie haben mit Aspose.Drawing für .NET erfolgreich Beschriftungen zu Ihrem Bild hinzugefügt. Experimentieren Sie ruhig mit verschiedenen Positionen und Werten, um Ihre Beschriftungen weiter anzupassen.

## FAQs

### Kann ich Aspose.Drawing für andere Arten von Illustrationen verwenden?

Ja, Aspose.Drawing unterstützt eine breite Palette von Zeichenvorgängen für verschiedene Arten von Illustrationen.

### Ist Aspose.Drawing mit verschiedenen Bildformaten kompatibel?

Absolut! Aspose.Drawing unterstützt gängige Bildformate wie PNG, JPEG, GIF und mehr.

### Wo finde ich weitere Beispiele und Dokumentation?

 Entdecken Sie die umfassende Dokumentation[Hier](https://reference.aspose.com/drawing/net/).

### Wie erhalte ich Unterstützung, wenn ich auf Probleme stoße?

 Besuche den[Aspose.Drawing-Forum](https://forum.aspose.com/c/diagram/17) für die Unterstützung der Gemeinschaft.

### Kann ich Aspose.Drawing vor dem Kauf ausprobieren?

 Sicherlich! Beginnen Sie mit einer kostenlosen Testversion[Hier](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
