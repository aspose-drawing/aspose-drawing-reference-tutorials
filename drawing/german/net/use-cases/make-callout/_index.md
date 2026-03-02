---
date: 2026-03-02
description: Verbessern Sie Ihre Dokumentillustrationen mit Aspose.Drawing für .NET!
  Lernen Sie Schritt für Schritt, wie Sie Anmerkungen hinzufügen, um klarere und informativere
  Visualisierungen zu erhalten.
linktitle: Making Callouts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Wie man Callouts mit Aspose.Drawing für .NET hinzufügt
url: /de/net/use-cases/make-callout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Callouts in Aspose.Drawing erstellen

## Einführung
Wenn Sie sich fragen **wie man Callouts** zu Ihren Bildern oder Diagrammen mit Aspose.Drawing für .NET hinzufügt, sind Sie hier genau richtig. In diesem Tutorial führen wir Sie durch den gesamten Prozess – vom Laden eines Bildes bis zum Zeichnen wunderschön gestalteter Callouts – damit Sie Ihre Illustrationen klarer und informativer machen können.

## Schnelle Antworten
- **Welche Bibliothek benötige ich?** Aspose.Drawing für .NET (von der offiziellen Website herunterladbar).  
- **Welche .NET-Versionen werden unterstützt?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Benötige ich eine Lizenz?** Eine kostenlose Testversion funktioniert für die Entwicklung; für die Produktion ist eine kommerzielle Lizenz erforderlich.  
- **Wie lange dauert die Implementierung?** In der Regel weniger als 10 Minuten für einen einfachen Callout.  
- **Kann ich Farben und Schriftarten anpassen?** Ja – alles wird von Standard‑GDI+‑Objekten (Pen, Font, Brush) gesteuert.

## So fügen Sie Callouts in Aspose.Drawing hinzu
Unten finden Sie eine kompakte Schritt‑für‑Schritt‑Anleitung, die genau zeigt **wie man Callouts** zu einem Bild hinzufügt. Sie können den Code gerne kopieren, mit den Positionen experimentieren und das Styling an Ihre Marke anpassen.

## Voraussetzungen
- Grundkenntnisse der Programmiersprache C#.  
- Aspose.Drawing‑Bibliothek installiert. Sie können sie [hier](https://releases.aspose.com/drawing/net/) herunterladen.  
- Ein Dokument oder Bild, dem Sie Callouts hinzufügen möchten.

## Namespaces importieren
Stellen Sie sicher, dass die erforderlichen Namespaces in Ihrem Projekt eingebunden sind:

```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```

## Schritt 1: Bild laden
Beginnen Sie damit, das Bild zu laden, dem Sie Callouts hinzufügen möchten. Ersetzen Sie `"Your Document Directory"` und `"gears.png"` durch Ihr tatsächliches Verzeichnis und den Bilddateinamen.

```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Your code here
}
```

## Schritt 2: Graphics‑Objekt erstellen
Erstellen Sie ein `Graphics`‑Objekt aus dem Bild, um Zeichenoperationen auszuführen.

```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```

## Schritt 3: Callout‑Positionen definieren
Definieren Sie die Start‑ und Endpunkte für jeden Callout sowie den Callout‑Wert und die Einheit.

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

## Schritt 4: Callouts zeichnen
Implementieren Sie die Methode `DrawCallOut`, um Callouts auf dem Bild zu zeichnen.

```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```

## Schritt 5: Bild speichern
Speichern Sie das Bild mit den Callouts in Ihrem gewünschten Verzeichnis.

```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```

## Quellcode für DrawCallout
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

## Häufige Probleme & Tipps
- **Falsche Ankerkoordinaten** – stellen Sie sicher, dass die Start‑ und Endpunkte innerhalb der Bildgrenzen liegen; sonst könnte der Callout abgeschnitten werden.  
- **Textüberlagerung** – passen Sie `spaceSize` oder die Schriftgröße an, wenn das Label mit anderen Grafiken kollidiert.  
- **Leistung** – bei sehr großen Bildern sollten Sie nach Gebrauch die Objekte `Pen`, `Font` und `Brush` freigeben, um Ressourcen zu schonen.

## Fazit
Herzlichen Glückwunsch! Sie wissen jetzt **wie man Callouts** zu einem Bild mit Aspose.Drawing für .NET hinzufügt. Experimentieren Sie gern mit verschiedenen Positionen, Farben und Schriftarten, um Ihren visuellen Stil anzupassen.

## FAQ

### Kann ich Aspose.Drawing für andere Arten von Illustrationen verwenden?
Ja, Aspose.Drawing unterstützt eine breite Palette von Zeichenoperationen für verschiedene Arten von Illustrationen.

### Ist Aspose.Drawing mit verschiedenen Bildformaten kompatibel?
Absolut! Aspose.Drawing unterstützt gängige Bildformate wie PNG, JPEG, GIF und weitere.

### Wo finde ich weitere Beispiele und Dokumentation?
Durchstöbern Sie die umfassende Dokumentation [hier](https://reference.aspose.com/drawing/net/).

### Wie erhalte ich Unterstützung, wenn ich auf Probleme stoße?
Besuchen Sie das [Aspose.Drawing‑Forum](https://forum.aspose.com/c/drawing/44) für Community‑Support.

### Kann ich Aspose.Drawing vor dem Kauf testen?
Natürlich! Beginnen Sie mit einer kostenlosen Testversion [hier](https://releases.aspose.com/).

**Zusätzliche Fragen & Antworten**

**F: Kann ich den Linienstil des Callouts (gestrichelt, punktiert) ändern?**  
**A: Ja – konfigurieren Sie einfach die Eigenschaft `Pen.DashStyle`, bevor Sie die Linie zeichnen.**

**F: Ist es möglich, dem Callout‑Label eine Hintergrundfarbe hinzuzufügen?**  
**A: Auf jeden Fall. Erstellen Sie einen `SolidBrush` mit Ihrer gewünschten Farbe und füllen Sie ein Rechteck hinter dem Text, bevor Sie `DrawString` aufrufen.**

**F: Wie stelle ich sicher, dass der Callout auf hochauflösenden Displays gleich aussieht?**  
**A: Setzen Sie `graphics.PageUnit = GraphicsUnit.Pixel` (wie gezeigt) und verwenden Sie vektorbasierte Maße, um die Skalierung konsistent zu halten.**

---

**Zuletzt aktualisiert:** 2026-03-02  
**Getestet mit:** Aspose.Drawing 24.11 für .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}